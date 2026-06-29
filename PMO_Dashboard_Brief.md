# Corebridge PMO Dashboard Brief

## Purpose
Create a PMO dashboard for the Corebridge project that follows the same color palette, typography, and template standards used for the AI Intern Talent Development dashboard, while supporting PMO operations and leadership reporting.

## Personas
- PMO User: full write access, including create, update, delete, and template maintenance.
- Leadership User: read-only access with a concise summary view.

## Operating Model
1. Practitioner is confirmed by RM.
2. PMO creates or updates the resource tracker entry with core fields such as name, email, mobile number, initiative, manager, feedback provider, onboarded date, offboarded date, and active/inactive status.
3. PMO sends onboarding communications from parameterized templates.
4. PMO tracks status, gaps, and team composition by initiative and manager.

## Dashboard Modules
### 1. Leadership Summary
High-level rollup for leadership with at-a-glance KPIs and trend indicators.

Recommended summary tiles:
- Total team count
- Active team members
- Inactive team members
- Onboarded this period
- Offboarded this period
- Pending onboarding actions

Recommended breakdowns:
- By initiative
- By manager
- By feedback provider
- Active vs inactive
- Onboarded vs offboarded over time

### 2. PMO Control View
Operational view with full management capability.

Recommended actions:
- Add resource tracker entry
- Edit resource details
- Mark active/inactive
- Trigger onboarding emails
- Manage template variations
- Track attachment inclusion for outgoing emails
- Delete records where allowed by process

### 3. Resource Tracker View
Table-first view for daily PMO operations.

Suggested columns:
- Name
- Email ID
- Mobile Number
- Initiative Name
- Manager Name
- Feedback Provider
- Onboarded Date
- Offboarded Date
- Status
- Email Sent Status
- Attachment Sent Status

### 4. Email Template Library
Parameterized email templates that can be reused as new people are added to the portal.

Initial template set:
- Welcome to Corebridge- Onboarding Formalities.msg
- Action RQD Onboarding New Deloitte Team Members - Upcoming Access request.msg
- CRBG- GH  Onboarding  Modernization  Basha Khaleel  6292026.msg

Template requirements:
- Replace person-specific names with parameters.
- Support initiative and manager placeholders.
- Preserve attachment behavior from the source message when enabled.
- Show attachment presence and optional inclusion status in the portal.

Observed source email findings:
- Welcome to Corebridge- Onboarding Formalities.msg
	- Subject: Welcome to Corebridge- Onboarding Formalities
	- Attachments: image001.jpg, image002.png, image003.png, CRBG PMO Referrence Document_v2.pdf
	- Key parameter candidates: practitioner name, functional lead, workstream, role start date, WBS code, leadership names.
- Action RQD Onboarding New Deloitte Team Members - Upcoming Access request.msg
	- Subject: Action RQD: Onboarding New Deloitte Team Members - Upcoming Access request
	- Attachments: image001.jpg, image002.png
	- Key parameter candidates: approver name, practitioner list, team name, contact email.
- CRBG- GH  Onboarding  Modernization  Basha Khaleel  6292026.msg
	- Subject: CRBG- GH | Onboarding | Modernization | Basha, Khaleel | 6/29/2026
	- Attachments: image001.jpg, image002.png
	- Key parameter candidates: team member name, Deloitte email ID, location, workstream, function/sub-function, manager name, WBS code, SOW.

## Wireframe Direction
Keep the same page and section structure pattern as the AI Intern Talent dashboard, with a consistent header, summary strip, operational table area, and supporting detail sections.

Suggested page layout:
1. Header with title, filters, and persona toggle.
2. KPI summary row.
3. Main operations table.
4. Initiative and manager analytics panels.
5. Email template and attachment management section.
6. Audit/activity trail.

## Open Items
- Extract the remaining full body text from each source `.msg` file where needed for exact wording.
- Confirm whether any template-specific attachments should always be included or conditionally included.
- Define the exact KPI set for leadership once the activity list is finalized.
- Confirm whether the dashboard will be implemented as a web app, Excel-backed portal, or another UI surface.
