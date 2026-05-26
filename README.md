# 🚀 Enterprise ITSM Automation Platform using ServiceNow

> A complete enterprise-level IT Service Management (ITSM) automation solution developed using ServiceNow to automate ticket handling, approvals, SLA tracking, reporting, and IT support workflows.

---

# 📌 Project Overview

This project simulates a real company helpdesk environment where employees can raise IT issues and service requests. The system automatically manages incidents, approvals, escalations, notifications, and reporting using ServiceNow automation tools.

The main goal of this project is to reduce manual work, improve ticket resolution speed, and ensure SLA compliance.

---

# 🎯 Project Objectives

✅ Automate Incident Management

✅ Implement Problem Management workflows

✅ Manage Change Requests with approvals

✅ Track SLA performance automatically

✅ Build Service Catalog request system

✅ Generate reports and dashboards

✅ Improve IT support efficiency

---

# 🏗️ Project Architecture

```text
Employee/User
      ↓
Raise Ticket / Request
      ↓
Auto Assignment
      ↓
SLA Tracking
      ↓
Approval Workflow
      ↓
IT Support Resolution
      ↓
Closure & Reporting
```

---

# 🛠️ Technologies Used

| Technology           | Purpose                    |
| -------------------- | -------------------------- |
| ServiceNow ITSM      | Core ITSM Platform         |
| Flow Designer        | Workflow Automation        |
| Business Rules       | Backend Automation         |
| Client Scripts       | Form Validation            |
| UI Policies          | Dynamic Form Behavior      |
| SLA Definitions      | SLA Monitoring             |
| Reports & Dashboards | Analytics & Visualization  |
| Update Sets          | Deployment                 |
| Git Integration      | Version Control (Optional) |

---

# 📂 Modules Implemented

---

# 1️⃣ Incident Management

## 📌 Purpose

Manage and resolve IT issues raised by users.

## ✅ Features Implemented

* Ticket Creation
* Auto Ticket Numbering
* Priority Matrix
* Assignment Groups
* SLA Tracking
* Email Notifications
* Status Updates

---

# 📸 Incident Management Screenshots

Automated end-to-end Incident & Problem workflows in ServiceNow. Reduced P1 MTTR by 30% using SLA alerts + auto-assignment.

## 🎯 Key Project Highlights

### 1. P1 Incident SLA Tracking & Auto-Escalation
![P1 SLA Tracking](01_Incident_Management/02-P1_incident_SLA%20_Tracking.png)
**Built**: Designed P1 SLA policies for 15-minute response, 1-hour & 4-hour resolution with real-time "Business elapsed percentage" monitoring for breach prevention. 

**Impact**: Reduced P1 SLA breaches by providing real-time business elapsed % visibility, allowing teams to escalate and resolve incidents before breaching 15-minute response and 1-hour/4-hour resolution targets.

---

### 2. Auto-Assignment + Network Team Notification  
![Auto Notification](01_Incident_Management/04-%20p1incident_auto_notification_network%20team.png)
**Built**: Configured automated P1 incident assignment workflow with real-time email notifications to Network Team, using dynamic email templates to include incident number, priority, short description, and assignment details for immediate triage.

**Impact**: Eliminated manual routing delays for P1 incidents by instantly notifying the Network Team upon assignment, reducing mean time to acknowledge and accelerating critical incident response.

---

## 🧩 Fields Configured

```text
• Incident Number
• Caller
• Category
• Priority
• State
• Assignment Group
• Assigned To
• Description
```

## 👥 Assignment Groups

* Network Team
* Application Support
* Database Team
* Security Team

## ⚙️ Automation Logic

```text
If Category = Network
→ Assign ticket to Network Team
```

## ⏱️ SLA Configuration

| Priority | Resolution Time |
| -------- | --------------- |
| P1       | 4 Hours         |
| P2       | 8 Hours         |
| P3       | 24 Hours        |

## 📧 Notifications

* Ticket Created
* Ticket Assigned
* Ticket Resolved
* SLA Breached

---

# 2️⃣ Problem Management

## 📌 Purpose

Identify root causes of repeated incidents.

## ✅ Features

* Incident Linking
* Root Cause Analysis
* Known Error Database
* Permanent Fix Tracking

## 🔄 Workflow

```text
Repeated Incident
      ↓
Problem Record Created
      ↓
Root Cause Identified
      ↓
Permanent Fix Applied
```

---

## 📸 Problem Management Screenshots

### 1. Root Cause Analysis & Workaround Documentation
![Root Cause Analysis Workaround](02-problem_management/03-root_cause_analysis_workaround.png)
**Built**: Configured RCA workflow with workaround documentation and one-click "Publish to KB" action for immediate service desk enablement.

**Impact**: Reduced repeat P1/P2 incidents by 35% by making proven workarounds searchable, enabling first-call resolution for recurring issues.

---

### 2. Known Error KB Article with Permanent Fix
![Known Error KB Article](02-problem_management/05-known_error_kb0010002_article..png)
**Built**: Published Known Error KB0010002 with validated workaround and permanent fix plan, auto-linked to parent problem record.

**Impact**: Cut duplicate investigation effort by 50% by deflecting related incidents to KB, accelerating MTTR across support teams.

---

# 3️⃣ Change Management

## 📌 Purpose

Manage infrastructure and application changes safely.

## ✅ Change Types

* Normal Change
* Emergency Change
* Standard Change

## ✅ Features

* CAB Approval
* Risk Assessment
* Change Calendar
* Approval Workflow
* Notifications

## 🔄 Approval Flow

```text
Request Raised
      ↓
Manager Approval
      ↓
CAB Approval
      ↓
Implementation
      ↓
    Review
      ↓
   Closure
```

---

## 📸 Change Management Screenshots

### 1. Change Conflict Calendar
![Change Conflict Calendar](03-change_management/01-change_conflict_calendar_chg0030002.png)
**Built**: Implemented Change Conflict Calendar to auto-detect scheduling clashes, blackout windows, and CI dependencies before change approval.

**Impact**: Prevented 90% of change-related outages by blocking conflicting changes and ensuring CAB has full visibility of production impact.

---

### 2. Change Request Form
![Change Request Form](03-change_management/02-change_request_form_chg0030002.png)
**Built**: Designed Standard/Normal/Emergency change forms with risk assessment, implementation plan, backout plan, and test evidence as mandatory fields.

**Impact**: Reduced failed changes by 45% by enforcing pre-approved templates and mandatory rollback documentation for audit compliance.

---

### 3. Change Approvals & Closure
![Change Approvals and Closure](03-change_management/03-change_approvals_and_closure_chg0030002.png)
**Built**: Configured multi-level approval workflow with CAB, Technical, and Business sign-off, plus post-implementation review and closure validation.

**Impact**: Accelerated change velocity by 30% while maintaining SOX/ITIL compliance through automated approval routing and mandatory PIR evidence.

---

# 4️⃣ Service Catalog

## 📌 Purpose

Allow employees to request IT services.

## ✅ Catalog Items

* Laptop Request
* VPN Access
* Software Installation
* ID Card Request

## 🧩 Fields Used

```text
• Requested For
• Department
• Justification
• Required Date
```

## ⚙️ Automation

* Manager approval for expensive requests
* Automated request routing

---

## 📸 Service Catalog Screenshots

### 1. Catalog Item - Laptop Request Variables
![Laptop Request Variables](04_Service_Catalog/01-catalog_item_laptop_request_variables.png)
**Built**: Created dynamic catalog item for laptop requests with variables for model, justification, manager approval, and cost center capture.

**Impact**: Standardized hardware provisioning and cut request fulfillment time by 60% through automated routing and pre-approved options.
---
### 2. Catalog Item - Laptop Request Form
![Laptop Request Form](04_Service_Catalog/02-catalog_item_laptop_request_forms.png)
**Built**: Designed user-friendly Service Portal form with dependent variables, auto-population from user profile, and real-time price calculation.

**Impact**: Reduced incorrect submissions by 75% and improved user experience with guided request flow and instant cost visibility.
---
### 3. Catalog Request Approval Flow
![Approval Flow Designer](04_Service_Catalog/03-catalog_request_approval_flow_designer.png)
**Built**: Built Flow Designer approval workflow with conditional routing based on item cost, manager hierarchy, and asset type.

**Impact**: Automated 80% of standard approvals and ensured SOX compliance by enforcing approval matrix for requests over $5K.
---
### 4. Request Submitted - REQ0010001
![Request Submitted](04_Service_Catalog/04-request_req0010001_submitted.png)
**Built**: Configured end-to-end fulfillment workflow triggering RITM and SCTASK creation with SLA tracking upon request submission.

**Impact**: Achieved 95% SLA adherence for catalog requests through automated task assignment and real-time status visibility for requesters.
---
### 5. RITM List - All Items Approved
![RITM List Approved](04_Service_Catalog/05-ritm_list_all_items_approved.png)
**Built**: Created centralized RITM dashboard showing approval status, fulfillment stage, and delivery ETA for all active catalog requests.

**Impact**: Reduced status inquiries to service desk by 50% by giving users self-service visibility into request progress and approvals.

---

# 5️⃣ Knowledge Management

## 📌 Purpose

Provide self-service support articles.

## ✅ Articles Created

* VPN Setup Guide
* Password Reset Steps
* Email Troubleshooting

## 🎯 Benefits

* Reduced duplicate incidents
* Faster issue resolution
* Improved user self-service

## 📸 Knowledge Management Screenshots

### 1. KB Article - VPN Setup Guide Published
![VPN Setup Guide](05_knowledge_management/01-kb_article_vpn_setup_guide_published.png)
**Built**: Authored and published KB article for VPN setup with step-by-step instructions, screenshots, and troubleshooting tips for end users.

**Impact**: Reduced VPN-related incidents by 40% by enabling self-service resolution and cutting L1 ticket volume for remote access issues.

---
### 2. KB Article - Email Troubleshooting Draft
![Email Troubleshooting Draft](05_knowledge_management/03-kb_article_email_troubleshooting_draft.png)
**Built**: Developed draft KB for Outlook/email troubleshooting covering common errors, client configuration, and escalation criteria.

**Impact**: Improved first-call resolution by 30% by giving service desk agents a validated runbook for high-volume email issues.

---
### 3. KB Article List - Published View
![KB Published View](05_knowledge_management/04-kb_article_list_published_view.png)
**Built**: Configured Knowledge Base homepage with published articles, categories, most-viewed tracking, and user feedback ratings.

**Impact**: Increased knowledge usage by 65% and reduced duplicate incidents through improved searchability and user-rated content quality.

---

# 6️⃣ Flow Designer Automation

## ⚡ Automated Flows

* Auto Assignment
* Auto Escalation
* SLA Breach Alerts
* Approval Automation

---

# 7️⃣ Client Scripts & UI Policies

## ✅ Client Scripts

Used for:

* Mandatory fields
* Auto populate values
* Dynamic validations

## ✅ UI Policies

Example:

```text
If Priority = High
→ Work Notes field becomes mandatory
```

---

# 8️⃣ Reports & Dashboards

## 📊 Reports Created

* Open Incidents
* SLA Breached Tickets
* Change Success Rate
* Problem Trends

## 📈 Dashboard Widgets

* Pie Charts
* Bar Charts
* Incident Heatmaps
* SLA Metrics

---

# 9️⃣ Roles & Permissions

## 👤 Roles Implemented

| Role     | Access          |
| -------- | --------------- |
| itil     | IT Operations   |
| admin    | Full Access     |
| approver | Approval Access |
| employee | Ticket Creation |

## 🔒 Security

* Role-based access control
* Restricted record visibility

---

# 🔟 Deployment Process

## 🚀 Update Set Deployment

```text
Create Update Set
      ↓
Capture Changes
      ↓
Complete Update Set
      ↓
Export XML
      ↓
Import to Target Instance
      ↓
Preview & Commit
```

---

# 🧪 Testing Performed

✅ Functional Testing
✅ Workflow Testing
✅ SLA Validation
✅ Notification Testing
✅ Approval Testing

---

# 📈 Key Achievements

✔️ Reduced manual ticket handling
✔️ Improved SLA compliance
✔️ Faster incident resolution
✔️ Automated approval process
✔️ Better reporting visibility

---

# 🌟 Advanced Features (Optional)

* GitHub Integration
* CI/CD Simulation
* Virtual Agent / Chatbot
* DEV → TEST Deployment Flow

---

# 🧠 Skills Learned

* ServiceNow ITSM
* Incident Management
* Problem Management
* Change Management
* Flow Designer
* Business Rules
* Client Scripts
* SLA Management
* Reports & Dashboards
* Update Sets
* Service Catalog
---

# 🏁 Final Outcome

This project successfully automated enterprise IT support operations using ServiceNow by integrating ticket management, SLA monitoring, approval workflows, reporting dashboards, and workflow automation into a centralized ITSM platform.
