# FormSG Logic — build sheet

Magic Form Builder imports **fields only**. After it runs, open the form's **Logic** tab and add the rules below — they reproduce the survey's gating. Field names match the question titles in the PDF.

## Selection limits (set on the field, not in Logic)
- **Which ERP modules does your solution provide?** → Checkbox, **min 3** ("Others" excluded)
- **Sales & CRM Module — Sub-modules** → Checkbox, **min 1**
- **Supply Chain & Inventory Management Module — Sub-modules** → Checkbox, **min 1**
- **Human Resources Management Module — Sub-modules** → Checkbox, **min 1**
- **Manufacturing Operations Management — Sub-modules** → Checkbox, **min 1**
- **Fleet Management Module — Sub-modules** → Checkbox, **min 1**

## Show-fields logic (target hidden by default; shown when the condition holds)
### §1a Compliance
- WHEN "Cyber Essentials Mark (CEM)" = Product Principal → SHOW **CEM for Product Principal**
- WHEN "CEM for Product Principal" = Yes → SHOW **CEM for Product Principal: Elaboration**
- WHEN "Cyber Essentials Mark (CEM)" = Reseller → SHOW **CEM for Resellers**
- WHEN "CEM for Resellers" = Yes → SHOW **CEM for Resellers: Elaboration**
### §1c ERP-Wide AI Features
- WHEN **ERP-Wide AI Features umbrella** = Yes → SHOW the AI-features checkbox
- WHEN that checkbox includes **Others — please specify** → SHOW the Others free-text
### §2 Modules — reveal each module's questions when it is selected
_FormSG Show rules don't cascade: in each rule select the module's **Section header**, the questions listed, **and any supporting date/upload fields** shown beneath them._
- WHEN **module scope** includes **Financial Management** → SHOW: Core Finance Module Features; InvoiceNow-Ready Solution Provider Accreditation; Finance Module — AI Features — umbrella; Finance Module — AI Features — features; Finance Module — AI Features — Others
- WHEN **module scope** includes **Sales & CRM** → SHOW: Sales & CRM Module — Sub-modules; Sales & CRM Module — AI Features — umbrella; Sales & CRM Module — AI Features — features; Sales & CRM Module — AI Features — Others
- WHEN **module scope** includes **Supply Chain & Inventory** → SHOW: Supply Chain & Inventory Management Module — Sub-modules; Supply Chain & Inventory Management Module — AI Features — umbrella; Supply Chain & Inventory Management Module — AI Features — features; Supply Chain & Inventory Management Module — AI Features — Others
- WHEN **module scope** includes **Human Resources** → SHOW: Human Resources Management Module — Sub-modules; Human Resources Management Module — AI Features — umbrella; Human Resources Management Module — AI Features — features; Human Resources Management Module — AI Features — Others
- WHEN **module scope** includes **Manufacturing** → SHOW: Manufacturing Operations Management — Sub-modules; Manufacturing Operations Management — AI Features — umbrella; Manufacturing Operations Management — AI Features — features; Manufacturing Operations Management — AI Features — Others
- WHEN **module scope** includes **Asset Management** → SHOW: Asset Management Module Features; Asset Management Module — AI Features — umbrella; Asset Management Module — AI Features — features; Asset Management Module — AI Features — Others
- WHEN **module scope** includes **Field Service** → SHOW: Field Service Management (FSM) Module Features; Field Service Management Module — AI Features — umbrella; Field Service Management Module — AI Features — features; Field Service Management Module — AI Features — Others
- WHEN **module scope** includes **Fleet Management** → SHOW: Fleet Management Module — Sub-modules; Fleet Management Module — AI Features — umbrella; Fleet Management Module — AI Features — features; Fleet Management Module — AI Features — Others
- WHEN **module scope** includes **Project Management** → SHOW: Project Management (PM) Module Features; Project Management Module — AI Features — umbrella; Project Management Module — AI Features — features; Project Management Module — AI Features — Others
- WHEN **module scope** includes **Others / Cross-cutting** → SHOW: Describe the other module(s); Evidence — Track Record; Clients' Sector(s)
### §2 per-module AI Features
- For each module: WHEN its **AI Features umbrella** = Yes → SHOW that module's AI-features checkbox (and the Others free-text when Others is ticked)
### §3 Third-Party Integration
- WHEN **Third-Party Integration Experience** = Yes → SHOW: third-party module types, **Externally-Integrated Modules**, and the integration track-record block

## Disable-submission logic (blocks submit until resolved)
_FormSG disables the whole form's submit while the condition holds — set a clear message._
- WHEN **Personal Data Protection** = No → DISABLE submission
- WHEN **Vulnerability Assessment / Penetration Testing (VA/PT)** = No → DISABLE submission
- WHEN **Core Finance Module Features** (Finance Module) = No → DISABLE submission
- WHEN **InvoiceNow-Ready Solution Provider Accreditation** (Finance Module) = No → DISABLE submission
- WHEN **Asset Management Module Features** (Asset Management Module) = No → DISABLE submission
- WHEN **Field Service Management (FSM) Module Features** (Field Service Management Module) = No → DISABLE submission
- WHEN **Project Management (PM) Module Features** (Project Management Module) = No → DISABLE submission
- WHEN **Evidence — Track Record** (Others) = No → DISABLE submission

> A module is meant to *disqualify* on a mandatory No. FormSG's disable-submission is form-level, so the vendor must resolve it (or deselect that module) before submitting — matching the rule that every selected module must pass.