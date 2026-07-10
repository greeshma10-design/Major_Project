# System Architecture

# Virtual Agent–Driven SLA Breach Awareness & Justification System

**Version:** 1.0  
**Platform:** ServiceNow  
**Project Type:** Internship Project

---

# 1. Overview

The **Virtual Agent–Driven SLA Breach Awareness & Justification System** is a zero-code ServiceNow solution designed to improve SLA governance through automation, proactive notifications, conversational assistance, and reporting.

The architecture leverages native ServiceNow components to monitor incidents, detect SLA risks, notify users, enforce mandatory breach justification, and provide management with real-time visibility into SLA performance.

---

# 2. Architecture Diagram

```text
                          +----------------------+
                          |      End Users       |
                          | (Agents / Managers)  |
                          +----------+-----------+
                                     |
                                     |
                                     ▼
                      +-------------------------------+
                      |      ServiceNow Platform      |
                      +-------------------------------+
                                     |
      -------------------------------------------------------------------
      |              |               |                |                  |
      ▼              ▼               ▼                ▼                  ▼
+-------------+ +--------------+ +--------------+ +-------------+ +-------------+
| Incident    | | SLA Engine   | | Flow Designer| | UI Policies | | Virtual     |
| Management  | |              | |              | |             | | Agent       |
+------+------+ +------+-------+ +------+-------+ +------+------+
       |                |                |                |              |
       |                |                |                |              |
       +----------------+----------------+----------------+--------------+
                                     |
                                     ▼
                        +--------------------------+
                        | Notification Engine      |
                        | (Email / Alerts)         |
                        +------------+-------------+
                                     |
                                     ▼
                        +--------------------------+
                        | Reports & Dashboards     |
                        +--------------------------+
```

---

# 3. System Components

## 3.1 Incident Management

The Incident Management module stores and manages incident records.

### Responsibilities

- Create incidents
- Assign incidents
- Track incident status
- Associate SLA definitions
- Store breach justification

---

## 3.2 SLA Engine

The SLA Engine continuously evaluates the remaining SLA time for every active incident.

### Responsibilities

- Start SLA timers
- Monitor SLA progress
- Detect nearing breach
- Detect SLA breach
- Trigger automation

---

## 3.3 Flow Designer

Flow Designer automates the complete SLA governance process without custom scripting.

### Responsibilities

- Detect SLA warning threshold
- Send notifications
- Trigger Virtual Agent
- Update incident records
- Record SLA events

---

## 3.4 UI Policies

UI Policies dynamically control the behavior of forms.

### Responsibilities

- Make Justification field mandatory
- Show/Hide fields
- Prevent incomplete submissions

---

## 3.5 Virtual Agent

The Virtual Agent provides conversational assistance to users regarding SLA status.

### Responsibilities

- Inform users about SLA status
- Warn users before SLA breach
- Guide users to submit justification
- Answer SLA-related questions

---

## 3.6 Notification Engine

The Notification Engine communicates SLA events to users.

### Notification Types

- SLA Warning Email
- SLA Breach Email
- ServiceNow Notifications

---

## 3.7 Reports & Dashboard

Reports provide operational insights into SLA performance.

### Dashboard Metrics

- Active Incidents
- Open Incidents
- Breached Incidents
- SLA Compliance %
- Monthly Trends
- Incident Distribution
- Justification Statistics

---

# 4. System Workflow

## Step 1

An incident is created in ServiceNow.

↓

## Step 2

An SLA is automatically attached.

↓

## Step 3

The SLA Engine continuously monitors the remaining SLA time.

↓

## Step 4

Flow Designer checks whether the SLA is approaching breach.

↓

## Step 5

If the warning threshold is reached:

- Email notification is sent
- Virtual Agent informs the assignee

↓

## Step 6

If the SLA is breached:

- Incident is marked as breached
- UI Policy makes the Justification field mandatory
- Breach notification is sent

↓

## Step 7

The assignee submits the breach justification.

↓

## Step 8

Managers review the incident.

↓

## Step 9

Dashboard and reports are automatically updated.

---

# 5. Data Flow

```text
Incident Created
        │
        ▼
Incident Table
        │
        ▼
SLA Engine
        │
        ▼
Flow Designer
        │
        ├────────────► Email Notification
        │
        ├────────────► Virtual Agent
        │
        ├────────────► UI Policies
        │
        ▼
Incident Updated
        │
        ▼
Reports & Dashboard
```

---

# 6. Security Architecture

The system uses **Role-Based Access Control (RBAC)**.

| Role | Permissions |
|------|-------------|
| Service Desk Agent | View and update assigned incidents |
| Incident Manager | Review incidents and breach justifications |
| ServiceNow Administrator | Configure tables, flows, dashboards, and Virtual Agent |
| Executive | View reports and dashboards only |

---

# 7. Technology Stack

| Layer | Technology |
|--------|------------|
| Platform | ServiceNow |
| Incident Management | ServiceNow Incident Module |
| Workflow Automation | Flow Designer |
| Conversational Interface | Virtual Agent |
| Form Validation | UI Policies |
| Notifications | ServiceNow Email Notifications |
| Reporting | ServiceNow Reports & Dashboards |
| Security | Role-Based Access Control (RBAC) |
| Version Control | Git & GitHub |

---

# 8. Key Design Principles

- Zero-code implementation using native ServiceNow features
- Automated SLA monitoring and governance
- Proactive notifications before SLA breaches
- Mandatory breach justification for accountability
- Conversational user guidance through Virtual Agent
- Secure access using RBAC
- Real-time reporting and executive dashboards
- Scalable and maintainable architecture

---

# 9. Future Enhancements

- AI-powered SLA breach prediction
- Microsoft Teams integration
- Slack integration
- Mobile push notifications
- Predictive SLA analytics
- Knowledge Base integration
- Multi-language Virtual Agent support
- Executive KPI dashboard enhancements

---

# 10. Conclusion

The architecture combines ServiceNow's Incident Management, SLA Engine, Flow Designer, UI Policies, Virtual Agent, Notifications, and Reporting modules into a unified solution that enables proactive SLA governance, improves accountability, and provides real-time visibility into SLA performance. The modular design ensures scalability, maintainability, and ease of future enhancements while remaining fully aligned with a zero-code implementation approach.