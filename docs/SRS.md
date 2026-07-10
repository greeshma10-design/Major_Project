# Software Requirements Specification (SRS)

# Virtual Agent–Driven SLA Breach Awareness & Justification System

**Version:** 1.0  
**Prepared By:** Greeshma's team  
**Platform:** ServiceNow  
**Project Type:** Internship Project

---

# 1. Introduction

## 1.1 Purpose

The purpose of this project is to develop an admin-level, zero-code SLA governance solution using ServiceNow that proactively monitors SLA performance, alerts users before SLA breaches, enforces mandatory breach justification, and provides management with actionable reports and dashboards.

The solution aims to improve SLA compliance through automation, conversational assistance, and governance controls.

---

## 1.2 Scope

The system provides:

- SLA monitoring
- Automated SLA warning notifications
- Mandatory breach justification
- Virtual Agent interactions
- Role-based access control
- Executive dashboards
- SLA reporting
- Audit-ready governance

The project is entirely implemented using native ServiceNow capabilities without custom scripting wherever possible.

---

## 1.3 Definitions

| Term | Description |
|------|-------------|
| SLA | Service Level Agreement |
| P1 | Priority 1 Incident |
| P2 | Priority 2 Incident |
| VA | Virtual Agent |
| RBAC | Role-Based Access Control |
| Flow Designer | ServiceNow workflow automation tool |
| UI Policy | Controls form behavior dynamically |

---

# 2. Overall Description

## 2.1 Product Perspective

The system extends ServiceNow Incident Management by introducing proactive SLA governance through automation, notifications, Virtual Agent interactions, and reporting.

It integrates the following ServiceNow components:

- Incident Table
- SLA Definitions
- Flow Designer
- Virtual Agent
- UI Policies
- Notifications
- Reports
- Dashboards

---

## 2.2 Product Objectives

- Detect SLA risks before breaches occur.
- Notify assignees automatically.
- Collect mandatory breach justification.
- Prevent unauthorized modifications.
- Provide real-time SLA visibility.
- Improve organizational accountability.

---

## 2.3 User Classes

### Service Desk Agent

- Works on incidents
- Receives SLA alerts
- Provides breach justification

---

### Incident Manager

- Reviews incidents
- Monitors SLA compliance
- Reviews justifications

---

### ServiceNow Administrator

- Configures workflows
- Maintains Virtual Agent
- Manages dashboards
- Controls permissions

---

### Executive / Management

- Views SLA reports
- Monitors KPIs
- Reviews compliance trends

---

# 3. Functional Requirements

## FR-1 Incident Monitoring

The system shall continuously monitor active incidents and associated SLAs.

---

## FR-2 SLA Warning Detection

The system shall identify incidents approaching SLA breach based on configured thresholds.

---

## FR-3 Automated Notifications

The system shall automatically notify the assigned user before SLA breach.

Notifications may include:

- Email
- ServiceNow Notification

---

## FR-4 SLA Breach Detection

The system shall detect when an SLA has been breached.

---

## FR-5 Mandatory Justification

If an SLA is breached:

- justification becomes mandatory
- incident cannot be closed without justification

---

## FR-6 UI Policy Enforcement

The system shall dynamically display mandatory fields using UI Policies after SLA breach.

---

## FR-7 Virtual Agent Guidance

The Virtual Agent shall:

- Inform users of SLA status
- Warn about upcoming breaches
- Guide users to submit justification
- Answer basic SLA-related questions

---

## FR-8 Reports

The system shall generate reports including:

- Total incidents
- Breached incidents
- Open incidents
- SLA compliance %
- Justification statistics

---

## FR-9 Dashboard

The dashboard shall display:

- Active incidents
- SLA nearing breach
- Breached incidents
- Monthly trends
- Compliance charts

---

## FR-10 Access Control

Only authorized users shall:

- Edit incidents
- Modify SLA configuration
- View administration modules

---

# 4. Non-Functional Requirements

## Performance

- Notifications generated within one minute.
- Dashboard loads within five seconds.
- Virtual Agent responds within three seconds.

---

## Security

- Role-Based Access Control
- Secure authentication
- Admin-only configuration access

---

## Reliability

- System availability of 99%
- Reliable notification delivery
- Accurate SLA calculations

---

## Scalability

The solution shall support increasing incident volume without affecting performance.

---

## Maintainability

The solution shall use standard ServiceNow configurations for easy maintenance.

---

## Usability

The interface shall be simple and require minimal user training.

---

# 5. System Components

- Incident Table
- SLA Definitions
- Flow Designer
- Virtual Agent
- UI Policies
- Notifications
- Reports
- Dashboard

---

# 6. Workflow

```
Incident Created
        │
        ▼
SLA Starts
        │
        ▼
Monitor Remaining Time
        │
        ▼
Near Breach?
     │
 ┌───┴────┐
 │        │
Yes       No
 │         │
 ▼         ▼
Notify User Continue Monitoring
 │
 ▼
Virtual Agent Reminder
 │
 ▼
SLA Breached?
     │
 ┌───┴────┐
 │        │
No       Yes
 │         │
 ▼         ▼
Continue  Mandatory Justification
            │
            ▼
      Manager Review
            │
            ▼
         Incident Closed
```

---

# 7. Business Rules

- Every incident must have an SLA.
- Warning notifications are sent before SLA breach.
- Breached incidents require justification.
- Justification is mandatory before closure.
- Managers can review submitted justifications.
- Dashboards refresh automatically.

---

# 8. Assumptions

- ServiceNow instance is available.
- Users have valid ServiceNow accounts.
- SLA definitions already exist or are configured.
- Email notifications are enabled.

---

# 9. Constraints

- Developed using native ServiceNow features.
- No external databases.
- No custom backend application.
- Limited to internship project scope.

---

# 10. Success Criteria

The project is considered successful if:

- SLA warnings are generated automatically.
- Breach notifications are sent successfully.
- Justification is enforced after breach.
- Virtual Agent assists users effectively.
- Dashboards display real-time SLA metrics.
- Reports accurately reflect SLA performance.

---

# 11. Future Enhancements

- AI-based SLA breach prediction
- Microsoft Teams integration
- Slack integration
- SMS notifications
- Predictive analytics
- Knowledge Base integration
- Multi-language Virtual Agent
- Mobile notifications

---

# 12. References

- ServiceNow Documentation
- ServiceNow Flow Designer Documentation
- ServiceNow Virtual Agent Documentation
- ServiceNow Reporting & Dashboard Documentation