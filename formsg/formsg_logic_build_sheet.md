# FormSG Logic - build sheet

Magic Form Builder imports **fields only**. After it runs, open the form's **Logic** tab and add the rules below - they reproduce the survey's gating. Field names match the question titles in the PDF.

## Selection limits (set on the field, not in Logic)
- **Sales & CRM Module - Sub-modules** → Checkbox, **min 1**
- **Supply Chain & Inventory Management Module - Sub-modules** → Checkbox, **min 1**
- Module scope is **10 Yes/No** questions (a checkbox can't be a logic source), so the "at least 3 modules" floor is **not auto-enforced** - state it as an instruction in the §2 intro.

## Show-fields logic
_Each rule's **Show** action takes a **list** of fields - select them all in one rule. Include any supporting date/upload fields shown beneath a question. No section show/hide: list the fields, not the Section._

### §1a Compliance (CEM routing)
- WHEN "Cyber Essentials Mark (CEM)" = Product Principal → SHOW: CEM for Product Principal
- WHEN "CEM for Product Principal" = Yes → SHOW: CEM for Product Principal: Elaboration
- WHEN "Cyber Essentials Mark (CEM)" = Reseller → SHOW: CEM for Resellers
- WHEN "CEM for Resellers" = Yes → SHOW: CEM for Resellers: Elaboration
### §1c ERP-Wide AI Features
- WHEN **ERP-Wide AI Features - does your solution use AI here?** = Yes → SHOW: ERP-Wide AI Features - features; ERP-Wide AI Features - Others (optional)
### §2 Modules - two levels (gate → module fields; AI umbrella → AI features)
- **L1** WHEN **Does your solution provide the Financial Management module?** = Yes → SHOW: Core Finance Module Features; InvoiceNow-Ready Solution Provider Accreditation; Finance Module - AI Features - does your solution use AI here?
    - **L2** WHEN **Finance Module - AI Features - does your solution use AI here?** = Yes → SHOW: Finance Module - AI Features - features; Finance Module - AI Features - Others (optional)
- **L1** WHEN **Does your solution provide the Sales & CRM module?** = Yes → SHOW: Sales & CRM Module - Sub-modules; Sales & CRM Module - AI Features - does your solution use AI here?
    - **L2** WHEN **Sales & CRM Module - AI Features - does your solution use AI here?** = Yes → SHOW: Sales & CRM Module - AI Features - features; Sales & CRM Module - AI Features - Others (optional)
- **L1** WHEN **Does your solution provide the Supply Chain & Inventory module?** = Yes → SHOW: Supply Chain & Inventory Management Module - Sub-modules; Supply Chain & Inventory Management Module - AI Features - does your solution use AI here?
    - **L2** WHEN **Supply Chain & Inventory Management Module - AI Features - does your solution use AI here?** = Yes → SHOW: Supply Chain & Inventory Management Module - AI Features - features; Supply Chain & Inventory Management Module - AI Features - Others (optional)
- **L1** WHEN **Does your solution provide the Human Resources module?** = Yes → SHOW: Human Resource Management System (HRMS); Human Resource e-Scheduling; Applicant Tracking & Sourcing; Employee Rewards and Recognition; Finance Module Integration for Payroll; IRAS Auto-Inclusion Scheme (AIS) Compliance; Human Resources Management Module - AI Features - does your solution use AI here?
    - **L2** WHEN **Human Resources Management Module - AI Features - does your solution use AI here?** = Yes → SHOW: Human Resources Management Module - AI Features - features; Human Resources Management Module - AI Features - Others (optional)
- **L1** WHEN **Does your solution provide the Manufacturing module?** = Yes → SHOW: Manufacturing Execution System (MES); MES Shopfloor Data Collection (Manual); MES Shopfloor Data Collection (Automated); Quality Management (QM); Product Lifecycle Management (PLM); Manufacturing Operations Management - AI Features - does your solution use AI here?
    - **L2** WHEN **Manufacturing Operations Management - AI Features - does your solution use AI here?** = Yes → SHOW: Manufacturing Operations Management - AI Features - features; Manufacturing Operations Management - AI Features - Others (optional)
- **L1** WHEN **Does your solution provide the Asset Management module?** = Yes → SHOW: Asset Management Module Features; Asset Management Module - AI Features - does your solution use AI here?
    - **L2** WHEN **Asset Management Module - AI Features - does your solution use AI here?** = Yes → SHOW: Asset Management Module - AI Features - features; Asset Management Module - AI Features - Others (optional)
- **L1** WHEN **Does your solution provide the Field Service module?** = Yes → SHOW: Field Service Management (FSM) Module Features; Field Service Management Module - AI Features - does your solution use AI here?
    - **L2** WHEN **Field Service Management Module - AI Features - does your solution use AI here?** = Yes → SHOW: Field Service Management Module - AI Features - features; Field Service Management Module - AI Features - Others (optional)
- **L1** WHEN **Does your solution provide the Fleet Management module?** = Yes → SHOW: Fleet Management Module Features; Fleet Management Module Safety Features; Fleet Management Module - AI Features - does your solution use AI here?
    - **L2** WHEN **Fleet Management Module - AI Features - does your solution use AI here?** = Yes → SHOW: Fleet Management Module - AI Features - features; Fleet Management Module - AI Features - Others (optional)
- **L1** WHEN **Does your solution provide the Project Management module?** = Yes → SHOW: Project Management (PM) Module Features; Project Management Module - AI Features - does your solution use AI here?
    - **L2** WHEN **Project Management Module - AI Features - does your solution use AI here?** = Yes → SHOW: Project Management Module - AI Features - features; Project Management Module - AI Features - Others (optional)
- **L1** WHEN **Does your solution provide the Others / Cross-cutting module?** = Yes → SHOW: Describe the other module(s); Evidence - Track Record; Clients' Sector(s)
### §3 Third-Party Integration
- WHEN **Third-Party Integration Experience** = Yes → SHOW: Third-party ERP module types; Externally-Integrated Modules; Overall Integration Track Record; Project Completion - proof page number; Integration Method; Third-Party Application name(s); Sector Record Qualifier

## Disable-submission logic (blocks submit until resolved)
_FormSG disables the whole form's submit while the condition holds - set a clear message._
- WHEN **Personal Data Protection** = No → DISABLE submission
- WHEN **Vulnerability Assessment / Penetration Testing (VA/PT)** = No → DISABLE submission
- WHEN **Core Finance Module Features** (Finance Module) = No → DISABLE submission
- WHEN **InvoiceNow-Ready Solution Provider Accreditation** (Finance Module) = No → DISABLE submission
- WHEN **Human Resource Management System (HRMS)** (Human Resources Management Module) = No → DISABLE submission
- WHEN **Finance Module Integration for Payroll** (Human Resources Management Module) = No → DISABLE submission
- WHEN **IRAS Auto-Inclusion Scheme (AIS) Compliance** (Human Resources Management Module) = No → DISABLE submission
- WHEN **Manufacturing Execution System (MES)** (Manufacturing Operations Management) = No → DISABLE submission
- WHEN **Asset Management Module Features** (Asset Management Module) = No → DISABLE submission
- WHEN **Field Service Management (FSM) Module Features** (Field Service Management Module) = No → DISABLE submission
- WHEN **Fleet Management Module Features** (Fleet Management Module) = No → DISABLE submission
- WHEN **Project Management (PM) Module Features** (Project Management Module) = No → DISABLE submission
- WHEN **Evidence - Track Record** (Others) = No → DISABLE submission

> A module is meant to *disqualify* on a mandatory No. FormSG's disable-submission is form-level, so the vendor must resolve it (or deselect that module) before submitting - matching the rule that every selected module must pass.