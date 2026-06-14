# Workday Financial Management GraphQL Schema

## Overview

This GraphQL schema represents the Workday Financial Management ERP domain, covering the full spectrum of enterprise financial operations. Workday Financial Management is a cloud-native ERP platform providing general ledger, accounts payable and receivable, procurement, budgeting, cash management, project accounting, and financial reporting.

The schema is derived from the Workday Financial Management SOAP/REST APIs documented at [https://community.workday.com/api](https://community.workday.com/api) and models the core financial data objects surfaced through:

- **Financial Management API** (v41.2) — general ledger, accounts, journals, worktags, financial organizations
- **Revenue Management API** (v41.2) — contracts, billing, revenue recognition
- **Expenses API** (v41.2) — expense reports and reimbursements
- **Cash Management API** (v41.2) — bank accounts, bank transactions, reconciliation
- **Budgets API** (v41.2) — budget plans, budget amounts, fiscal structures
- **Projects API** (v41.2) — project accounting, task codes, project budgets
- **Resource Management API** (v45.2) — suppliers, purchase orders, requisitions, vendor invoices
- **Settlement Services API** (v45.2) — payment runs, bank transfers, settlement
- **Inventory API** (v45.2) — goods receipts, inventory adjustments

Base API endpoint: `https://wd2-impl-services1.workday.com/ccx/service`

---

## Schema Design Principles

- Each Workday financial object maps to a named GraphQL type.
- Workday uses a worktag model for dimensional accounting — `Worktag` is a polymorphic dimension applied to transactions, journals, and budgets to classify spend and revenue across cost centers, funds, programs, regions, and custom dimensions.
- Fiscal structures (`FiscalYear`, `FiscalPeriod`, `Period`) anchor all time-bounded financial data.
- The procure-to-pay lifecycle is represented by: `Requisition` → `PurchaseOrder` → `GoodsReceipt` → `VendorInvoice` → `VendorPayment`.
- The order-to-cash lifecycle is represented by: `Contract` → `CustomerInvoice` → `Payment`.
- Journal entries (`Journal`, `JournalLine`, `Posting`) represent the core accounting record.

---

## Types Summary

| Category | Types |
|---|---|
| Chart of Accounts | Account, AccountCode, AccountSet |
| Journals & Postings | Journal, JournalLine, Posting |
| Fiscal Structure | Period, FiscalYear, FiscalPeriod |
| Budgets | Budget, BudgetAmount, BudgetCategory |
| Organization | OrganizationHierarchy, Company, CostCenter, Fund, Program, Region, Worktag |
| Revenue | Revenue, RevenueRecognitionRule |
| Expense | Expense, SpendCategory, TaskCode |
| Accounts Payable | AccountsPayable, AccountsPayableLine |
| Vendor / Supplier | VendorInvoice, VendorInvoiceLine, VendorPayment, PaymentRun |
| Procurement | Procurement, Requisition, RequisitionLine, PurchaseOrder, PurchaseOrderLine |
| Receipts | GoodsReceipt, GoodsReceiptLine |
| Contracts | Contract, ContractAmendment |
| Billing | Billing, CustomerInvoice, CustomerInvoiceLine |
| Payments & Cash | Payment, Cash, BankStatement, BankTransfer |
| Reconciliation | Reconciliation |
| Intercompany | IntercompanyTransaction |
| Allocation | Allocation |
| Projects | Project, ProjectBudget, ProjectExpense |
| Tax | Tax, TaxCode, TaxRate |
| Reporting | FinancialReport |
| Platform | EffectiveDate, APIKey, Webhook |

---

## Root Operations

### Query

```graphql
type Query {
  # Accounts
  account(id: ID!): Account
  accounts(filter: AccountFilter, page: Int, pageSize: Int): AccountConnection

  # Journals
  journal(id: ID!): Journal
  journals(filter: JournalFilter, page: Int, pageSize: Int): JournalConnection

  # Fiscal structure
  fiscalYear(id: ID!): FiscalYear
  fiscalYears(companyId: ID, page: Int, pageSize: Int): FiscalYearConnection
  fiscalPeriod(id: ID!): FiscalPeriod

  # Budgets
  budget(id: ID!): Budget
  budgets(filter: BudgetFilter, page: Int, pageSize: Int): BudgetConnection

  # Organizations
  company(id: ID!): Company
  companies(page: Int, pageSize: Int): CompanyConnection
  costCenter(id: ID!): CostCenter
  costCenters(companyId: ID, page: Int, pageSize: Int): CostCenterConnection
  worktag(id: ID!): Worktag
  worktags(type: WorktagType, page: Int, pageSize: Int): WorktagConnection

  # Procurement
  purchaseOrder(id: ID!): PurchaseOrder
  purchaseOrders(filter: PurchaseOrderFilter, page: Int, pageSize: Int): PurchaseOrderConnection
  requisition(id: ID!): Requisition
  requisitions(filter: RequisitionFilter, page: Int, pageSize: Int): RequisitionConnection

  # Vendor invoices
  vendorInvoice(id: ID!): VendorInvoice
  vendorInvoices(filter: VendorInvoiceFilter, page: Int, pageSize: Int): VendorInvoiceConnection

  # Customer invoices
  customerInvoice(id: ID!): CustomerInvoice
  customerInvoices(filter: CustomerInvoiceFilter, page: Int, pageSize: Int): CustomerInvoiceConnection

  # Cash & bank
  bankStatement(id: ID!): BankStatement
  bankStatements(filter: BankStatementFilter, page: Int, pageSize: Int): BankStatementConnection

  # Projects
  project(id: ID!): Project
  projects(filter: ProjectFilter, page: Int, pageSize: Int): ProjectConnection

  # Reports
  financialReport(id: ID!): FinancialReport
  financialReports(filter: FinancialReportFilter, page: Int, pageSize: Int): FinancialReportConnection

  # Tax
  taxCode(id: ID!): TaxCode
  taxCodes(page: Int, pageSize: Int): TaxCodeConnection
}
```

### Mutation

```graphql
type Mutation {
  # Journals
  createJournal(input: CreateJournalInput!): Journal
  submitJournal(id: ID!): Journal
  reverseJournal(id: ID!, effectiveDate: String!): Journal

  # Budgets
  createBudget(input: CreateBudgetInput!): Budget
  amendBudget(id: ID!, input: AmendBudgetInput!): Budget

  # Procurement
  createRequisition(input: CreateRequisitionInput!): Requisition
  approveRequisition(id: ID!): Requisition
  createPurchaseOrder(input: CreatePurchaseOrderInput!): PurchaseOrder
  receivePurchaseOrder(input: ReceiveGoodsInput!): GoodsReceipt

  # Vendor invoices
  createVendorInvoice(input: CreateVendorInvoiceInput!): VendorInvoice
  approveVendorInvoice(id: ID!): VendorInvoice

  # Payments
  createPaymentRun(input: CreatePaymentRunInput!): PaymentRun
  createBankTransfer(input: CreateBankTransferInput!): BankTransfer

  # Customer invoices
  createCustomerInvoice(input: CreateCustomerInvoiceInput!): CustomerInvoice

  # Projects
  createProject(input: CreateProjectInput!): Project

  # Webhooks
  registerWebhook(input: RegisterWebhookInput!): Webhook
  deleteWebhook(id: ID!): Boolean
}
```

---

## Schema File

The full type definitions are in `workday-finance-schema.graphql`.

---

## Authentication

Workday APIs use OAuth 2.0 (client credentials grant) for REST endpoints and WS-Security for SOAP endpoints. For a GraphQL layer built over the Workday REST/SOAP surface:

1. Obtain a client credential from the Workday tenant admin at `https://developer.workday.com`.
2. Exchange credentials for a bearer token at the tenant token endpoint.
3. Pass the token as `Authorization: Bearer <token>` on every request.

Reference: [https://doc.workday.com/r/Enterprise_Interface_API_Concepts_and_Resources/Authentication](https://doc.workday.com/r/Enterprise_Interface_API_Concepts_and_Resources/Authentication)

---

## Pagination

All list queries return a connection type following the Relay cursor connection pattern:

```graphql
type PageInfo {
  hasNextPage: Boolean!
  hasPreviousPage: Boolean!
  startCursor: String
  endCursor: String
  totalCount: Int
}
```

---

## References

- Workday Community API Portal: https://community.workday.com/api
- Financial Management API v41.2: https://community.workday.com/sites/default/files/file-hosting/productionapi/Financial_Management/v41.2/index.html
- Resource Management API v45.2: https://community.workday.com/sites/default/files/file-hosting/productionapi/Resource_Management/v45.2/index.html
- Settlement Services API v45.2: https://community.workday.com/sites/default/files/file-hosting/productionapi/Settlement_Services/v45.2/index.html
- Getting Started: https://doc.workday.com/r/Enterprise_Interface_API_Concepts_and_Resources/Getting_Started_with_Workday_Web_Services
