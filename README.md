# Workday Finance (workday-finance)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

APIs for Workday's cloud-based financial management system, enabling enterprise resource planning, accounting, financial analytics, procurement, grants management, inventory, and settlement services.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/workday-finance/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/workday-finance/refs/heads/main/apis.yml)

## Tags

- Accounting
- Cloud
- Enterprise
- ERP
- Finance
- Financial Management

## Timestamps

- **Created:** 2024-01-01
- **Modified:** 2026-05-19

## APIs

### Workday Financial Management API

Core SOAP API for financial management operations including general ledger, accounts payable, accounts receivable, financial reporting, tax, financial organizations, and worktag management. Exposes data relative to accounts, accounting, business plans, and related financial structures.

- **Human URL:** [https://www.workday.com/en-us/products/financial-management/overview.html](https://www.workday.com/en-us/products/financial-management/overview.html)
- **Base URL:** `https://wd2-impl-services1.workday.com/ccx/service`

#### Tags

- Accounting
- Banking
- Finance
- General Ledger

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Financial_Management/v41.2/index.html)
- [Reference](https://community.workday.com/sites/default/files/file-hosting/productionapi/Financial_Management/v41.2/Financial_Management.html)
- [X-wsdl](https://community.workday.com/sites/default/files/file-hosting/productionapi/Financial_Management/v41.2/Financial_Management.wsdl)
- [OpenAPI](openapi/workday-finance-financial-management-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/workday-finance-financial-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-financial-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Workday Revenue Management API

SOAP API for managing revenue recognition, contracts, and billing processes. Supports revenue accounting workflows and contract analysis within Workday Financial Management.

- **Human URL:** [https://www.workday.com/en-us/products/financial-management/revenue-management.html](https://www.workday.com/en-us/products/financial-management/revenue-management.html)
- **Base URL:** `https://wd2-impl-services1.workday.com/ccx/service`

#### Tags

- Billing
- Contracts
- Revenue

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Revenue_Management/v41.2/index.html)
- [Reference](https://community.workday.com/sites/default/files/file-hosting/productionapi/Revenue_Management/v41.2/Revenue_Management.html)
- [X-wsdl](https://community.workday.com/sites/default/files/file-hosting/productionapi/Revenue_Management/v41.2/Revenue_Management.wsdl)
- [Postman Collection](collections/workday-finance-financial-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-financial-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/workday-finance-procurement.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-procurement.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Workday Expenses API

SOAP API for expense management, including expense reports, approval workflows, and reimbursements. Part of Workday Spend Management for tracking and controlling employee and organizational expenses.

- **Human URL:** [https://www.workday.com/en-us/products/spend-management/expenses.html](https://www.workday.com/en-us/products/spend-management/expenses.html)
- **Base URL:** `https://wd2-impl-services1.workday.com/ccx/service`

#### Tags

- Expenses
- Reimbursement
- Spend Management

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Expenses/v41.2/index.html)
- [X-wsdl](https://community.workday.com/sites/default/files/file-hosting/productionapi/Expenses/v41.2/Expenses.wsdl)
- [Postman Collection](collections/workday-finance-financial-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-financial-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/workday-finance-procurement.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-procurement.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Workday Cash Management API

SOAP API for managing cash positions, bank transactions, and treasury operations. Supports cash flow forecasting, bank account management, and financial reconciliation processes.

- **Human URL:** [https://www.workday.com/en-us/products/financial-management/cash-management.html](https://www.workday.com/en-us/products/financial-management/cash-management.html)
- **Base URL:** `https://wd2-impl-services1.workday.com/ccx/service`

#### Tags

- Banking
- Cash Management
- Treasury

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Cash_Management/v41.2/index.html)
- [Reference](https://community.workday.com/sites/default/files/file-hosting/productionapi/Cash_Management/v41.2/Cash_Management.html)
- [X-wsdl](https://community.workday.com/sites/default/files/file-hosting/productionapi/Cash_Management/v41.2/Cash_Management.wsdl)
- [Postman Collection](collections/workday-finance-financial-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-financial-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/workday-finance-procurement.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-procurement.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Workday Budgets API

SOAP API for budget planning, tracking, and analysis. Enables programmatic management of budgets, budget amendments, and budget structure data within Workday Financial Management.

- **Human URL:** [https://www.workday.com/en-us/products/financial-management/budget-management.html](https://www.workday.com/en-us/products/financial-management/budget-management.html)
- **Base URL:** `https://wd2-impl-services1.workday.com/ccx/service`

#### Tags

- Budgets
- Financial Planning
- Planning

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Budgets/v41.2/index.html)
- [X-wsdl](https://community.workday.com/sites/default/files/file-hosting/productionapi/Budgets/v41.2/Budgets.wsdl)
- [Postman Collection](collections/workday-finance-financial-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-financial-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/workday-finance-procurement.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-procurement.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Workday Projects API

SOAP API for project management, tracking project costs, billing, and resource allocation. Supports project-based accounting, cost capture, and resource planning workflows.

- **Human URL:** [https://www.workday.com/en-us/products/financial-management/projects.html](https://www.workday.com/en-us/products/financial-management/projects.html)
- **Base URL:** `https://wd2-impl-services1.workday.com/ccx/service`

#### Tags

- Cost Tracking
- Project Management
- Projects

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Projects/v41.2/index.html)
- [X-wsdl](https://community.workday.com/sites/default/files/file-hosting/productionapi/Projects/v41.2/Projects.wsdl)
- [Postman Collection](collections/workday-finance-financial-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-financial-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/workday-finance-procurement.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-procurement.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Workday Resource Management API

SOAP API exposing Workday Financials Resource Management data, including suppliers, supplier accounts, procurement, purchase orders, invoicing, business assets, asset depreciation, and travel and entertainment operations. Supports the full procure-to-pay lifecycle and asset management workflows.

- **Human URL:** [https://www.workday.com/en-us/products/spend-management/procure-to-pay.html](https://www.workday.com/en-us/products/spend-management/procure-to-pay.html)
- **Base URL:** `https://wd2-impl-services1.workday.com/ccx/service`

#### Tags

- Business Assets
- Invoicing
- Procurement
- Resource Management
- Suppliers

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Resource_Management/v45.2/index.html)
- [Reference](https://community.workday.com/sites/default/files/file-hosting/productionapi/Resource_Management/v45.2/Resource_Management.html)
- [X-wsdl](https://community.workday.com/sites/default/files/file-hosting/productionapi/Resource_Management/v45.2/Resource_Management.wsdl)
- [OpenAPI](openapi/workday-finance-procurement-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/workday-finance-procurement.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-procurement.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Workday Settlement Services API

SOAP API for settlement management and payment services. Supports payment processing, bank routing, settlement runs, direct debit mandates, payment acknowledgements, cash balance checks, and escheatment management across supplier payments, employee reimbursements, and customer payments.

- **Human URL:** [https://www.workday.com/en-us/products/financial-management/accounting-finance.html](https://www.workday.com/en-us/products/financial-management/accounting-finance.html)
- **Base URL:** `https://wd2-impl-services1.workday.com/ccx/service`

#### Tags

- Banking
- Direct Debit
- Payments
- Settlements

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Settlement_Services/v45.2/index.html)
- [Reference](https://community.workday.com/sites/default/files/file-hosting/productionapi/Settlement_Services/v45.2/Settlement_Services.html)
- [X-wsdl](https://community.workday.com/sites/default/files/file-hosting/productionapi/Settlement_Services/v45.2/Settlement_Services.wsdl)
- [Postman Collection](collections/workday-finance-financial-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-financial-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/workday-finance-procurement.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-procurement.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Workday Inventory API

SOAP API exposing Workday Financials Inventory data. Supports goods delivery, stock tracking, inventory adjustments, cycle counting, par management, directed picks, put-away operations, recalls, and replenishment across storage locations and distribution networks.

- **Human URL:** [https://www.workday.com/en-us/products/spend-management/inventory.html](https://www.workday.com/en-us/products/spend-management/inventory.html)
- **Base URL:** `https://wd2-impl-services1.workday.com/ccx/service`

#### Tags

- Goods Delivery
- Inventory
- Stock Management
- Supply Chain

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Inventory/v45.2/index.html)
- [Reference](https://community.workday.com/sites/default/files/file-hosting/productionapi/Inventory/v45.2/Inventory.html)
- [X-wsdl](https://community.workday.com/sites/default/files/file-hosting/productionapi/Inventory/v45.2/Inventory.wsdl)
- [Postman Collection](collections/workday-finance-financial-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-financial-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/workday-finance-procurement.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-procurement.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Workday Professional Services Automation API

SOAP API for Professional Services Automation integrations. Exposes Workday Financials data for managing client-facing projects, services billing, resource staffing, and expense reporting within professional services organizations.

- **Human URL:** [https://www.workday.com/en-us/products/professional-services-automation/overview.html](https://www.workday.com/en-us/products/professional-services-automation/overview.html)
- **Base URL:** `https://wd2-impl-services1.workday.com/ccx/service`

#### Tags

- Professional Services
- PSA
- Resource Staffing
- Services Billing

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Professional_Services_Automation/v45.2/index.html)
- [Reference](https://community.workday.com/sites/default/files/file-hosting/productionapi/Professional_Services_Automation/v45.2/Professional_Services_Automation.html)
- [X-wsdl](https://community.workday.com/sites/default/files/file-hosting/productionapi/Professional_Services_Automation/v45.2/Professional_Services_Automation.wsdl)
- [Postman Collection](collections/workday-finance-financial-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-financial-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/workday-finance-procurement.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-finance-procurement.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://community.workday.com/api)
- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/index.html)
- [Getting Started](https://doc.workday.com/r/Enterprise_Interface_API_Concepts_and_Resources/Getting_Started_with_Workday_Web_Services)
- [Authentication](https://doc.workday.com/r/Enterprise_Interface_API_Concepts_and_Resources/Authentication)
- [Rate Limits](https://doc.workday.com/r/Enterprise_Interface_API_Concepts_and_Resources/Rate_Limiting)
- [Console](https://developer.workday.com/about)
- [Website](https://www.workday.com/en-us/products/financial-management/overview.html)
- [Sign Up](https://resourcecenter.workday.com/)
- [Blog](https://blog.workday.com/)
- [Support](https://www.workday.com/en-us/services/support.html)
- [Community](https://www.workday.com/en-us/services/community.html)
- [Status Page](https://status.workday.com/)
- [Terms of Service](https://www.workday.com/en-us/legal.html)
- [Privacy Policy](https://www.workday.com/en-us/privacy.html)
- [GitHub Organization](https://github.com/Workday)
- [Marketplace](https://marketplace.workday.com/en-US/home)
- [Changelog](https://community.workday.com/articles/16827)
- [Reference](https://community.workday.com/sites/default/files/file-hosting/productionapi/index.html)
- [Spectral  Rules](rules/workday-finance-rules.yml)
- [JSON-LD](json-ld/workday-finance-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/workday-finance-journal-entry-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/workday-finance-supplier-invoice-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/workday-finance-purchase-order-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Vocabulary](vocabulary/workday-finance-vocabulary.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
