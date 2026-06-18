# Build this as an interactive web app (e.g. in Lovable)

Build a single-page interactive vendor self-assessment from the survey below. No login. Render it section by section, styled cleanly. Apply the gating exactly as annotated:

- **Tiers**: "Mandatory" = required, "Preferred" = optional.
- **"select at least N"**: that question is a multi-select needing >= N picks.
- **"a No disqualifies the module"**: show a per-module status banner - Qualifies / Disqualified / Incomplete - and the whole form is submittable only when every selected module Qualifies.
- **"Display: shown only when X = Y"**: hide that field until the condition holds.
- **§2 module scope** is a checkbox (min 3, "Others" excluded); ticking a module reveals that module's questions.

Show a top banner that turns green only when all selected modules qualify.

--- SURVEY CONTENT (questions + gating) ---

# iERP pre-approval - vendor self-assessment (text spec)

Full survey content with explicit gating, for the FormSG prompt route (see docs/formsg_prompts.md). Tier, min-select, disqualify-on-No, and show/hide conditions are annotated inline.

## §1a · Compliance baseline

### 1a.1 Personal Data Protection  _(Mandatory)_

Can your solution demonstrate compliance with the following Personal Data Protection requirements?

Digital solutions that collect, use, disclose, process or dispose
personal data should incorporate features that support the
obligations under the Personal Data Protection Act (2020). To comply with this requirement, you MUST complete the Personal
Data Protection Requirements form at https://go.gov.sg/pdp.

_Answer:_ [ ] Yes   [ ] No

### 1a.2 Vulnerability Assessment / Penetration Testing (VA/PT)  _(Mandatory)_

Has your solution undergone a comprehensive security vulnerability
assessment/penetration testing (VA/PT) conducted by a qualified
third-party within the last 12 months? The scope of the VA/PT must
cover network security; application security; data protection
measures and access control (if applicable); API security testing
(if applicable); Cloud security configuration review (if applicable).
Specifically, for web application security, the scope must cover
minimally all OWASP Top 10 vulnerabilities.


Please submit the VA/PT report (dated maximum 1 year from the
checklist submission date). The VA/PT Report must include: If you are the reseller of the solution, please obtain the VA/PT
report from your product principal. SOC 2 Type II report can be accepted if the detailed technical
vulnerability assessment results are part of the SOC2 Type II
scope. CREST-certified companies (https://www.crest-approved.org/members/)
or companies with security professionals holding relevant CREST
certifications; security professionals with recognised
certifications such as Offensive Security Certified Professional
(OSCP), EC-Council Certified Penetration Testing Professional
(CPENT), GIAC Penetration Tester (GPEN), or other equivalent
industry-recognised certifications.

_Answer:_ [ ] Yes   [ ] No

### 1a.3 Cyber Essentials Mark (CEM)  _(Preferred)_

Are you the Product Principal of the solution that you are submitting for pre-approval?

_Answer:_ [ ] Product Principal   [ ] Reseller
- [ ] Product Principal
- [ ] Reseller

### 1a.4 CEM for Product Principal  _(Preferred)_
> Display: shown only when Cyber Essentials Mark (CEM) = Product Principal.

Has your organisation achieved CSA Cyber Essentials for ICT Vendor
Mark certification or equivalent recognised cybersecurity
certifications (including but not limited to Cyber Trust Mark or
ISO27001) that validate the implementation of appropriate security
controls against common cyber threats in your organisation and the
solution you are submitting for pre-approval?


Vendors are encouraged to comply at application and are required
to meet this requirement by the Annual Review, where it will be
assessed as mandatory. For more information on the Cyber Essentials Mark, refer to
https://www.csa.gov.sg/cyber-essentials/.

_Answer:_ [ ] Yes   [ ] No

### 1a.5 CEM for Product Principal: Elaboration  _(Mandatory (follow-up))_
> Display: shown only when CEM for Product Principal = Yes.

Please specify the following information.

Please also upload a copy of the Certification and indicate the
Certification Issuance Date in the date field. (Final upload
happens at PSG submission, not in this survey.)

_Answer:_ [ ] Yes   [ ] No

### 1a.6 CEM for Resellers  _(Preferred)_
> Display: shown only when Cyber Essentials Mark (CEM) = Reseller.

Has your organisation achieved CSA Cyber Essentials Mark certification
or equivalent recognised cybersecurity certifications (including but
not limited to Cyber Trust Mark or ISO27001) that validate the
implementation of appropriate security controls against common cyber
threats in your organisation and the solution you are submitting for
pre-approval?


Vendors are encouraged to comply at application and are required
to meet this requirement by the Annual Review, where it will be
assessed as mandatory. For more information on the Cyber Essentials Mark, refer to
https://www.csa.gov.sg/cyber-essentials/.

_Answer:_ [ ] Yes   [ ] No

### 1a.7 CEM for Resellers: Elaboration  _(Mandatory (follow-up))_
> Display: shown only when CEM for Resellers = Yes.

Please specify the following information.

Please also upload a copy of the Certification and indicate the
Certification Issuance Date in the date field. (Final upload
happens at PSG submission, not in this survey.)

_Answer:_ [ ] Yes   [ ] No

## §1b · Internal integration

### 1b.1 Internal Modules  _(Mandatory)_

Does your solution provide robust data integration across all ERP modules within your own application, ensuring a seamless and consistent information flow across all business functions without manual intervention?
• ERP Interoperability (Internal)
• User Documentation (Internal)
• Audit Logging and Monitoring

_Answer:_ [ ] Yes   [ ] No

## §1c · ERP-Wide AI Features

### 1c.1 ERP-Wide AI Features - does your solution use AI here?  _(Preferred)_

_Answer:_ [ ] Yes   [ ] No

### 1c.2 ERP-Wide AI Features - features  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Select all that apply.

_Answer:_ (select all that apply)
- [ ] AI-Enabled Large-Language Model Layer
- [ ] AI Copilot
- [ ] AI Anomaly Detection
- [ ] Predictive Forecasting
- [ ] Agentic Workflow Orchestration

### 1c.3 ERP-Wide AI Features - Others (optional)  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Describe any other AI feature(s).

_Answer:_ Answer: __________________________________________________

## §2 · Module scope gate

### 2.1 Does your solution provide the Financial Management module?  _(Mandatory)_

_Answer:_ [ ] Yes   [ ] No

### 2.2 Does your solution provide the Sales & CRM module?  _(Mandatory)_

_Answer:_ [ ] Yes   [ ] No

### 2.3 Does your solution provide the Supply Chain & Inventory module?  _(Mandatory)_

_Answer:_ [ ] Yes   [ ] No

### 2.4 Does your solution provide the Human Resources module?  _(Mandatory)_

_Answer:_ [ ] Yes   [ ] No

### 2.5 Does your solution provide the Manufacturing module?  _(Mandatory)_

_Answer:_ [ ] Yes   [ ] No

### 2.6 Does your solution provide the Asset Management module?  _(Mandatory)_

_Answer:_ [ ] Yes   [ ] No

### 2.7 Does your solution provide the Field Service module?  _(Mandatory)_

_Answer:_ [ ] Yes   [ ] No

### 2.8 Does your solution provide the Fleet Management module?  _(Mandatory)_

_Answer:_ [ ] Yes   [ ] No

### 2.9 Does your solution provide the Project Management module?  _(Mandatory)_

_Answer:_ [ ] Yes   [ ] No

### 2.10 Does your solution provide the Others / Cross-cutting module?  _(Mandatory)_

_Answer:_ [ ] Yes   [ ] No

## §2 · Financial Management

### 100.1 Core Finance Module Features  _(Mandatory)_
> Gating: a “No” here disqualifies this module (it cannot be submitted).

Does your finance module provide the following functions?
• General Ledger & Chart of Accounts - Record all business transactions in a double-entry general ledger with a configurable chart of accounts
• Accounts Receivable & Customer Invoicing - Record customer invoices and track payments received against them
• Accounts Payable & Vendor Bills - Record vendor bills and schedule payments
• Bank & Cash Management - Reconcile bank statements and cash positions against ledger records
• Budgeting & Forecasting - Create budgets and compare actual spending against budgeted amounts
• Financial Analytics & Dashboards - View financial performance data and drill down to transaction details

_Answer:_ [ ] Yes   [ ] No

### 100.2 InvoiceNow-Ready Solution Provider Accreditation  _(Mandatory)_
> Gating: a “No” here disqualifies this module (it cannot be submitted).

Is your solution listed on IMDA InvoiceNow-Ready Solution Provider (IRSP) Listing?

[1] If you are the Product Principal of the solution, you are required to be accredited as an IRSP by IMDA. [2] If you are the reseller of the solution, your Solution Product Principal must declare to IMDA that you are an authorised reseller of their solution.

Note: For more information on InvoiceNow, refer to: Becoming an InvoiceNow-Ready Solution Provider | E-invoicing | IMDA (https://www.imda.gov.sg/how-we-can-help/nationwide-e-invoicing-framework/becoming-an-invoicenow-ready-solution-provider)


_Answer:_ [ ] Yes   [ ] No

### 100.3 Finance Module - AI Features - does your solution use AI here?  _(Preferred)_

_Answer:_ [ ] Yes   [ ] No

### 100.4 Finance Module - AI Features - features  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Select all that apply.

_Answer:_ (select all that apply)
- [ ] Automated Invoice Processing - AI-powered optical character recognition (OCR) extracts data from invoices, automatically matches them to purchase orders, and routes for approval, reducing manual data entry
- [ ] Automated Journal Entry Suggestions - AI learns from historical accounting patterns to suggest appropriate account codes, cost centre allocations, and journal entries for recurring transactions
- [ ] Anomaly Detection and Fraud Prevention - AI monitors transaction patterns to identify unusual activities, duplicate payments, vendor fraud, or accounting errors in real-time, flagging suspicious transactions for review

### 100.5 Finance Module - AI Features - Others (optional)  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Describe any other AI feature(s).

_Answer:_ Answer: __________________________________________________

## §2 · Sales & CRM

### 101.1 Sales & CRM Module - Sub-modules  _(Mandatory)_
> Gating: select at least 1.

Which Sales & CRM Module sub-modules does your solution provide? Select at least one to qualify for this module.

Sales: Do you provide Sales features?
  • Orders & Invoicing - Record customer orders and generate invoices linked to payment status
  • Sales Reporting, Analytics & Dashboards - View sales performance data and forecasts through customizable reports

CRM: Does your Sales and/or CRM Module provide the following CRM features?
  • Contact, Account & Customer Master - Maintain unified contact and account records with relationship hierarchies and interaction history
  • Customer Interaction Log - Record and track all customer interactions in a single timeline
  • Lead Management - Capture leads and convert qualified ones to opportunities
  • Opportunity & Pipeline Management - Manage active opportunities through a stage-based pipeline

_Answer:_ (select all that apply)
- [ ] Sales
- [ ] CRM

### 101.2 Sales & CRM Module - AI Features - does your solution use AI here?  _(Preferred)_

_Answer:_ [ ] Yes   [ ] No

### 101.3 Sales & CRM Module - AI Features - features  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Select all that apply.

_Answer:_ (select all that apply)
- [ ] Predictive Lead Scoring - AI ranks inbound leads by win probability based on firmographic and behavioural signals, helping sales prioritise the highest-value prospects
- [ ] Opportunity Win-Probability Modeling - AI forecasts deal closure likelihood per opportunity, surfacing pipeline risks and supporting more accurate revenue forecasts
- [ ] Next Best Action Recommendation - AI analyses each customer's history and stage to suggest the most effective follow-up action for the rep, improving engagement consistency

### 101.4 Sales & CRM Module - AI Features - Others (optional)  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Describe any other AI feature(s).

_Answer:_ Answer: __________________________________________________

## §2 · Supply Chain & Inventory

### 102.1 Supply Chain & Inventory Management Module - Sub-modules  _(Mandatory)_
> Gating: select at least 1.

Which Supply Chain & Inventory Management Module sub-modules does your solution provide? Select at least one to qualify for this module.

Procurement & Purchasing: Does your Supply Chain & Inventory Management Module provide Procurement & Purchasing features?
  • Purchase Orders & Procurement - Track purchase orders from creation through invoice payment
  • Vendor & Supplier Master - Maintain vendor records with contact details, payment terms, and lead times

Warehouse & Inventory: Does your Supply Chain & Inventory Management Module provide Warehouse & Inventory features?
  • Inventory Master & Item Management - Maintain a central registry of items with unique identifiers and track their key attributes
  • Stock Levels & Warehouse Management - Track inventory quantities across multiple locations and bins
  • Reorder Rules & Replenishment - Automatically trigger purchase requisitions when inventory falls below defined reorder points
  • Multi-Warehouse Management - Track & allocate stock levels across multiple physical warehouse locations
  • Stock Movement Report Generation - Generate real-time, audit-ready reports tracking all stock inflows, transfers, and outflows
  • Supply Chain Analytics & Dashboards - Provide visibility into inventory, order, and supplier performance metrics

Material Requirements Planning (MRP): Does your Supply Chain & Inventory Management Module provide Material Requirements Planning (MRP) features?
  • Demand Forecasting - Dynamically calculate raw material needs based on demand, supply and production schedules
  • Real-Time Inventory Reordering - Automatically trigger purchase requisitions when stock drops below safety-stock thresholds

_Answer:_ (select all that apply)
- [ ] Procurement & Purchasing
- [ ] Warehouse & Inventory
- [ ] Material Requirements Planning (MRP)

### 102.2 Supply Chain & Inventory Management Module - AI Features - does your solution use AI here?  _(Preferred)_

_Answer:_ [ ] Yes   [ ] No

### 102.3 Supply Chain & Inventory Management Module - AI Features - features  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Select all that apply.

_Answer:_ (select all that apply)
- [ ] Stock Anomaly Detection - AI identifies unusual consumption patterns, theft indicators, or expiry-driven write-off risks, flagging items for review before they hit financial impact

### 102.4 Supply Chain & Inventory Management Module - AI Features - Others (optional)  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Describe any other AI feature(s).

_Answer:_ Answer: __________________________________________________

## §2 · Human Resources

### 103.1 Human Resource Management System (HRMS)  _(Mandatory)_
> Gating: a “No” here disqualifies this module (it cannot be submitted).

Do you provide HRMS features?
• Personnel Management - Maintain a single employee master record and allow for employee self-service for self-updating
• Payroll Management - Process e-payroll, generate Ministry of Manpower (MOM)-standard payslips and comply to policy & statutory requirements
• Leave Management - Configure leave policy and allow for the management of leave applications
• Benefits and Claims Management - Process medical and transport claims & support multiple payment processing (Payroll, GIRO, cheque, and cash payment)
• Performance Appraisal Management - Set KPIs for individual employees for each appraisal cycle, and provide online built-in self-service appraisal forms with employee tagging and manager routing for approval and scoring
• HRMS Dashboards and Reports - Create, customise & view dashboards and/or reports that provide an at-a-glance overview of common HR metrics/indicators to help analyse data through data visualisation

_Answer:_ [ ] Yes   [ ] No

### 103.2 Human Resource e-Scheduling  _(Preferred)_

Do you provide Human Resource e-Scheduling features?
• Roster Scheduling - Create employee scheduling based on business demand & employee availability
• Employee Access - Allows for mobile cloud-based access for employees to access schedules and rosters
• Employee Notification - Allows for the receiving of push messages/notifications for scheduling and roster reminders
• System Setup - Setup user accounts for the administrator and all employee users, manage business units for different employee categories (e.g. geography, division, tenure, etc), and other interface customisations
• HR e-Scheduling Dashboards and Reports - Create, customise & view dashboards and/or reports that provide an at-a-glance overview of overall scheduling statuses, attendance, overtime reporting, and generate attendance & overtime reports

_Answer:_ [ ] Yes   [ ] No

### 103.3 Applicant Tracking & Sourcing  _(Preferred)_

Do you provide Applicant Tracking & Sourcing features?
• Manage Jobs & Postings - Create and edit positions with approval workflows, and publish them to multiple job boards (e.g. LinkedIn, Jobstreet, MyCareersFuture, IHLs, etc.)
• Track & Tag Candidates - Update application statuses, tag candidates, and add recruitment notes directly in the system
• Customise Forms & Communications - Configure application forms with custom questions, and bulk-send templated emails (e.g. for scheduling of interviews, job offers, rejections, etc.) using role-based privacy settings (i.e. HR can determine level of information visible to hiring managers and peer interviewers)
• Offers & Documentation - Accept candidate document uploads and send official job offers directly through the system
• Applicant Tracking & Sourcing Dashboards and Reports - Create, customise & view dashboards and/or reports that provide an overview of all job posts and application statuses, candidate application tracking and recruitment performance analysis (e.g., Application to Vacancies Ratio (AVR), Job Offer Rate, etc.)

_Answer:_ [ ] Yes   [ ] No

### 103.4 Employee Rewards and Recognition  _(Preferred)_

Do you provide Employee Rewards and Recognition features?
• Award Points & Recognition - Employers can award points or dollar value ad-hoc or for specific occasions, and send words of appreciation which can be tagged to the core values of the company
• Merchant Reward Redemption - Employees can redeem points across a diverse network of over 100 Singapore-based retail, F&B, and recreation merchants
• Social Appreciation Board - Features a public posting board to openly announce and celebrate employee appreciations
• Employee Rewards and Recognition Dashboards and Reports - Create, customise & view dashboards and/or reports that allowing for the viewing and tracking of points awarded, redeemed, and balance points as well as rewards utilisation

_Answer:_ [ ] Yes   [ ] No

### 103.5 Finance Module Integration for Payroll  _(Mandatory)_
> Gating: a “No” here disqualifies this module (it cannot be submitted).

Is your module integrated with the Finance Management module to facilitate processing of employees' payroll?


_Answer:_ [ ] Yes   [ ] No

### 103.6 IRAS Auto-Inclusion Scheme (AIS) Compliance  _(Mandatory)_
> Gating: a “No” here disqualifies this module (it cannot be submitted).

Is your solution listed on IRAS's List of Supporting Payroll Software Vendors for the Auto-Inclusion Scheme (AIS) for employment income? (AIS submission auto-includes employees' IR8A income to IRAS.)


_Answer:_ [ ] Yes   [ ] No

### 103.7 Human Resources Management Module - AI Features - does your solution use AI here?  _(Preferred)_

_Answer:_ [ ] Yes   [ ] No

### 103.8 Human Resources Management Module - AI Features - features  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Select all that apply.

_Answer:_ (select all that apply)
- [ ] HR Chatbot - A HR chatbot answers FAQs on company policies, allow Leave and Claims applications to be submitted, approved & automatically updated
- [ ] Roster Scheduling - AI automates and optimises roster scheduling, as well as perform data analytics on scheduling patterns and recommend predictive measures (e.g. prompt to schedule manpower ahead of peak hours in restaurant, etc)
- [ ] Recruitment and Talent Matching - AI automatically recommends candidates based on job requirements

### 103.9 Human Resources Management Module - AI Features - Others (optional)  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Describe any other AI feature(s).

_Answer:_ Answer: __________________________________________________

## §2 · Manufacturing

### 104.1 Manufacturing Execution System (MES)  _(Mandatory)_
> Gating: a “No” here disqualifies this module (it cannot be submitted).

Do you provide MES features?
• Work Order Management - Create, dispatch, manage work orders that include information such as execution sequence, work instructions, resources, etc.
• Work Order Scheduling (Basic) - Plan and modify work order sequences in the relevant shopfloor stations
• Shopfloor Data Entry - Allow operators to view work orders and detailed information of each task, as well as do data input (e.g. via barcode scanners, etc.)
• Work-in-Progress (WIP) Tracking - Track and display real-time work completion status for each operation, based on data input from the shopfloor
• MES Dashboards & Reports - Create, customise & view dashboards and/or reports that provide an at-a-glance overview of various production indicators (e.g. Shopfloor Equipment Status, WIP Tracker, Overall Equipment Efficiency (OEE), etc.)

_Answer:_ [ ] Yes   [ ] No

### 104.2 MES Shopfloor Data Collection (Manual)  _(Preferred)_

Do you provide the following manual shopfloor data collection features?
• Shopfloor Data Entry - Operators view detailed task information and input production data on the shopfloor (e.g. via barcode scanners)
• Work-in-Progress (WIP) Tracking - Track and display real-time work completion status for each operation, based on operator input

_Answer:_ [ ] Yes   [ ] No

### 104.3 MES Shopfloor Data Collection (Automated)  _(Preferred)_

Do you provide the following automated shopfloor data collection features?
• Real-time Equipment Status Monitoring - Monitor equipment status and downtime reason(s) automatically via integration into equipment
• Equipment Data Management - Maintain the details and status of each equipment
• Notification Alerts - Trigger notification alerts (e.g. via email, Whatsapp, SMS etc.) when equipments go down or shows signs of being disrupted

_Answer:_ [ ] Yes   [ ] No

### 104.4 Quality Management (QM)  _(Preferred)_

Do you provide QM features?
• Inspection Plan Configuration - Allow for the configuration of quality standards required (e.g. attributes to record, frequencies, sample sizes, etc.)
• Quality Data Collection - Facilitate the collection of quality data either through manual keying of information on screen by the operator or automatically via an interfaced connection with measurement equipment
• Non-Conformance (NC) Alerting - Notifications and/or alarms are triggered when measurements are out of specification, and NCs are highlighted to user(s) for follow-ups
• Root Cause and Corrective Action (RCCA) Recording - Allows users to record causes and required actions of NCs
• Data Analytics - Allow for the performance of statistical analysis and the detection of trends & deviations for the conclusion of significant influences
• QM Dashboards & Reports - Create, customise & view dashboards and/or reports for recorded quality checks, statistical analysis and/or other relevant QM indicators

_Answer:_ [ ] Yes   [ ] No

### 104.5 Product Lifecycle Management (PLM)  _(Preferred)_

Do you provide PLM features?
• Routing & Work Instruction Management - Provide a centralized source of information on the sequence of processes involved to manufacture or assemble a product (e.g. technical drawings, Bill of Materials (BOM), materials required, and manufacturing processes such as tools, equipment, and work instructions used to build the product, etc.)
• Engineering Drawing Management - Provide the relevant technical drawings of components and materials used in each process
• Work Instruction Management - Provide relevant information on tools, equipment, manpower and instructions that is required in each process
• Engineering Change Management - Manage revisions to product design and update relevant manufacturing process changes that are impacted by the product design change
• PLM Dashboards & Reports - Create, customise & view dashboards and/or reports for the PLM processes

_Answer:_ [ ] Yes   [ ] No

### 104.6 Manufacturing Operations Management - AI Features - does your solution use AI here?  _(Preferred)_

_Answer:_ [ ] Yes   [ ] No

### 104.7 Manufacturing Operations Management - AI Features - features  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Select all that apply.

_Answer:_ (select all that apply)
- [ ] Dynamic Dispatching for Work Order Scheduling - The system autonomously shifts the production sequence, re-routing urgent jobs to alternative work centers and updating operator digital work whenever issues arise that delay existing schedules
- [ ] Dynamic Root Cause Assistance - AI-driven QMS uses Natural Language Processing (NLP) and machine learning to scan historical records, automatically suggesting root causes and proven corrective actions
- [ ] Engineering Change Impact Analysis - AI-driven PLM instantly scans master data to automatically flag downstream assets, tools, contracts, and compliance rules affected by design changes

### 104.8 Manufacturing Operations Management - AI Features - Others (optional)  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Describe any other AI feature(s).

_Answer:_ Answer: __________________________________________________

## §2 · Asset Management

### 108.1 Asset Management Module Features  _(Mandatory)_
> Gating: a “No” here disqualifies this module (it cannot be submitted).

Do you provide the following features?
• Centralized Asset Lifecycle Tracking - Monitor an asset's journey from procurement through maintenance histories down to final decommissioning disposal
• Maintenance Schedule Alerts - Set automated triggers based on time, usage and/or sensor thresholds to service equipment before it breaks down
• Equipment Utilization Monitoring - Continuously track active, idle, or misplaced physical tools and machinery across multiple job sites
• Compliance Tracking - Maintain detailed digital histories of safety audits, calibrations, and protocol approvals to remain audit-ready
• Historical Equipment Maintenance Records - Centralize all past repair data and technician notes to optimize future service lifecycle decisions
• Asset Management Dashboards & Reports - Create, customise & view dashboards and/or reports that provide real-time monitoring of asset indicators (e.g. Track asset health & reliability, maintenance backlogs, etc.)

_Answer:_ [ ] Yes   [ ] No

### 108.2 Asset Management Module - AI Features - does your solution use AI here?  _(Preferred)_

_Answer:_ [ ] Yes   [ ] No

### 108.3 Asset Management Module - AI Features - features  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Select all that apply.

_Answer:_ (select all that apply)

### 108.4 Asset Management Module - AI Features - Others (optional)  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Describe any other AI feature(s).

_Answer:_ Answer: __________________________________________________

## §2 · Field Service

### 106.1 Field Service Management (FSM) Module Features  _(Mandatory)_
> Gating: a “No” here disqualifies this module (it cannot be submitted).

Do you provide the following features?
• Work Order Management - Create, assign, and track work orders from initiation to completion, including details such as customer information, job location, required skills and equipment, priority level, etc
• Work Order Scheduling - Schedule technicians based on their profile such as skill level, availability, or proximity to the job
• Mobile Field Worker App - View work orders, update job status with a digital record (e.g. text, e-signature, images, videos, etc.), receive push notifications and offline/online data entry w/ cloud synchronisation
• FSM Dashboards & Reports - Create, customise & view dashboards and/or reports that provide real-time monitoring of FSM indicators (E.g. job status, technician availability and current locations, scheduling status, attendance and overtime reports, etc.)

_Answer:_ [ ] Yes   [ ] No

### 106.2 Field Service Management Module - AI Features - does your solution use AI here?  _(Preferred)_

_Answer:_ [ ] Yes   [ ] No

### 106.3 Field Service Management Module - AI Features - features  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Select all that apply.

_Answer:_ (select all that apply)
- [ ] Gen-AI Generated Summaries - Generate work order summaries that transform rough notes taken by mobile field workers, into well-organised, concise and easy-to-understand
- [ ] Auto-Scheduling & Dispatch - AI scheduling engine continuously optimizes the daily schedule autonomously

### 106.4 Field Service Management Module - AI Features - Others (optional)  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Describe any other AI feature(s).

_Answer:_ Answer: __________________________________________________

## §2 · Fleet Management

### 105.1 Fleet Management Module Features  _(Mandatory)_
> Gating: a “No” here disqualifies this module (it cannot be submitted).

Do you provide the following features?
• Fleet Tracking via Telematics & GPS - Utilise telematics and GPS tracking to provide a complete real-time fleet overview
• Dispatch Management - Manage the fleet's journey and associated costs
• Dynamic Route Planning - Automate optimised route planning using real-time traffic and historical data
• Fleet Management Dashboards & Reports - Create, customise & view dashboards and/or reports that provide an at-a-glance overview of fleet indicators (e.g. mileage and fuel consumption, vehicle maintenance and servicing tasks, etc.)

_Answer:_ [ ] Yes   [ ] No

### 105.2 Fleet Management Module Safety Features  _(Preferred)_

Do you provide the following safety features?
• Driver Status Monitoring System (DSMS) - Detect and alert the driver of fatigue events (e.g. closing of eyes) and distractions (e.g. making phone calls)
• Advanced Driver Assistance System (ADAS) - Alert the driver of potential collisions (e.g. forward collision warning, lane departure warning, and pedestrian or cyclist collision warning, etc.)
• Blind Spot Detection System - Improve situational awareness by alerting the driver of pedestrians, cyclists, motorcyclists, or workers in the vehicle's blind spots

_Answer:_ [ ] Yes   [ ] No

### 105.3 Fleet Management Module - AI Features - does your solution use AI here?  _(Preferred)_

_Answer:_ [ ] Yes   [ ] No

### 105.4 Fleet Management Module - AI Features - features  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Select all that apply.

_Answer:_ (select all that apply)
- [ ] Predictive Vehicle Maintenance - Machine learning predicts mechanical issues using telematics data points (e.g. fluctuations in battery voltage, engine temperature, etc.)
- [ ] Dynamic Dispatching & Route Optimization - AI continuously calculates routes by cross-referencing live variables (e.g. traffic bottlenecks, severe weather, changing customer delivery windows, etc.) with historical operational patterns

### 105.5 Fleet Management Module - AI Features - Others (optional)  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Describe any other AI feature(s).

_Answer:_ Answer: __________________________________________________

## §2 · Project Management

### 107.1 Project Management (PM) Module Features  _(Mandatory)_
> Gating: a “No” here disqualifies this module (it cannot be submitted).

Do you provide the following features?
• Task Management and Scheduling - Easily create, organize, and assign tasks with clear deadlines and dependencies
• Resource Allocation Tracking - Monitor team workloads and manage budget distribution
• Team Collaboration Tools - Share feedback, discuss updates, and co-edit documents instantly within the team
• PM Dashboards & Reports - Create, customise & view dashboards and/or reports that provide real-time monitoring of PM indicators (e.g. Track project health, milestones, project performance metrics, etc.)

_Answer:_ [ ] Yes   [ ] No

### 107.2 Project Management Module - AI Features - does your solution use AI here?  _(Preferred)_

_Answer:_ [ ] Yes   [ ] No

### 107.3 Project Management Module - AI Features - features  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Select all that apply.

_Answer:_ (select all that apply)
- [ ] Automated Progress & Status Reporting - AI reads task titles, activity logs, descriptions, comments, etc. across entire project boards and compresses information into structured reports
- [ ] Predictive Risk Detection - AI continuously analyzes historical completion rates, current velocity, task dependencies, team capacity, etc. and alerts potential delays ahead of time, proactively

### 107.4 Project Management Module - AI Features - Others (optional)  _(Preferred)_
> Display: shown only when the umbrella above = Yes.

Describe any other AI feature(s).

_Answer:_ Answer: __________________________________________________

## §2 · Others / Cross-cutting

### 1000.1 Describe the other module(s)  _(Mandatory)_

Describe the other module(s) your solution provides that are not covered by the modules above.

_Answer:_ Answer: __________________________________________________

### 1000.2 Evidence - Track Record  _(Mandatory)_
> Gating: a “No” here disqualifies this module (it cannot be submitted).

Submit 3 completed project proposals. Each must include:
• Modules Covered in Proposal (must include the module being applied for)
• Project Completion Signoff Proofs by Clients
• Project Completion Dates
• Total Overall Billed Costs
• Clients' Sector(s)

_Answer:_ [ ] Yes   [ ] No

### 1000.3 Clients' Sector(s)  _(Mandatory)_

Select the sector(s) of the clients in your project proposals.

_Answer:_ (select all that apply)
- [ ] Accountancy
- [ ] Advanced Manufacturing
- [ ] Built Environment
- [ ] Early Childhood
- [ ] Engineering Services
- [ ] Environmental Services
- [ ] Estate Agency
- [ ] Food
- [ ] Marine & Offshore
- [ ] Personal Care Services
- [ ] Precision Engineering
- [ ] Retail
- [ ] Security
- [ ] Wholesale Trade

## §3 · Third-Party Integration

### 3.1 Third-Party Integration Experience  _(Preferred)_

Have you completed any third-party integrations - integrating an external module or application into your solution at a customer's request?

_Answer:_ [ ] Yes   [ ] No

### 3.2 Third-party ERP module types  _(Preferred)_
> Display: shown only when the experience gate above = Yes.

Which third-party ERP module types can your solution integrate with?

_Answer:_ (select all that apply)
- [ ] Financial Management
- [ ] Sales & CRM
- [ ] Supply Chain & Inventory
- [ ] Human Resources
- [ ] Manufacturing
- [ ] Asset Management
- [ ] Field Service
- [ ] Fleet Management
- [ ] Project Management

### 3.3 Externally-Integrated Modules  _(Mandatory)_
> Display: shown only when the experience gate = Yes.

Does your solution provide robust data integration with any externally-integrated third-party ERP modules (integrated at the customer's request), ensuring a seamless and consistent information flow across all business functions without manual intervention?
• ERP Interoperability (Integration)
• User Documentation (Integration)
• Audit Logging and Monitoring

_Answer:_ [ ] Yes   [ ] No

### 3.4 Overall Integration Track Record  _(Mandatory)_
> Display: shown only when the experience gate = Yes.

Do you have at least 1 completed project proposal that includes:
1) Scope of work clearly indicating the integration of the module or application
2) Indication of the integration method (API, Webhooks, Event-Driven, etc.)
3) Clear proof of project completion (e.g. signed handover form, completion letter)

Note: all proposals must be for Singapore-based companies, and at least 1 of your submitted modules must be listed in the proposal.

_Answer:_ [ ] Yes   [ ] No

### 3.5 Project Completion - proof page number  _(Mandatory)_
> Display: shown only when the experience gate = Yes.

The page number for the proof of project completion.

_Answer:_ Answer: ______________________________

### 3.6 Integration Method  _(Mandatory)_
> Display: shown only when the experience gate = Yes.

Method(s) of integration used in the project proposal.

_Answer:_ (select all that apply)
- [ ] API
- [ ] Webhooks
- [ ] Event-Driven Architecture

### 3.7 Third-Party Application name(s)  _(Mandatory)_
> Display: shown only when the experience gate = Yes.

The third-party application name(s) integrated in the project proposal.

_Answer:_ Answer: __________________________________________________

### 3.8 Sector Record Qualifier  _(Mandatory)_
> Display: shown only when the experience gate = Yes.

The industry(s) of the client, to the best of your knowledge.

_Answer:_ (select all that apply)
- [ ] Accountancy
- [ ] Advanced Manufacturing
- [ ] Built Environment
- [ ] Early Childhood
- [ ] Engineering Services
- [ ] Environmental Services
- [ ] Estate Agency
- [ ] Food
- [ ] Marine & Offshore
- [ ] Personal Care Services
- [ ] Precision Engineering
- [ ] Retail
- [ ] Security
- [ ] Wholesale Trade
