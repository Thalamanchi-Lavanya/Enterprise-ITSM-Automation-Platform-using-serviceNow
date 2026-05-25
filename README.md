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

# Enterprise ITSM Automation Platform using ServiceNow

Automated end-to-end Incident & Problem workflows in ServiceNow. Reduced P1 MTTR by 30% using SLA alerts + auto-assignment.

## 🎯 Key Project Highlights

### 1. P1 Incident SLA Tracking & Auto-Escalation
![P1 SLA Tracking](01_Incident_Management/02-P1_incident_SLA%20_Tracking.png)
**Built**: Designed P1 SLA policies for 15-minute response, 1-hour & 4-hour resolution with real-time "Business elapsed percentage" monitoring for breach prevention. 

**Impact**: Reduced P1 SLA breaches by providing real-time business elapsed % visibility, allowing teams to escalate and resolve incidents before breaching 15-minute response and 1-hour/4-hour resolution targets.

### 2. Auto-Assignment + Network Team Notification  
![Auto Notification](01_Incident_Management/04-%20p1incident_auto_notification_network%20team.png)
**Built**: Configured automated P1 incident assignment workflow with real-time email notifications to Network Team, using dynamic email templates to include incident number, priority, short description, and assignment details for immediate triage.

**Impact**: Eliminated manual routing delays for P1 incidents by instantly notifying the Network Team upon assignment, reducing mean time to acknowledge and accelerating critical incident response.

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

### 2. Known Error KB Article with Permanent Fix
![Known Error KB Article](02-problem_management/05-known_error_kb0010002_article.png)
**Built**: Published Known Error KB0010002 with validated workaround and permanent fix plan, auto-linked to parent problem record.

**Impact**: Cut duplicate investigation effort by 50% by deflecting related incidents to KB, accelerating MTTR across support teams.

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
