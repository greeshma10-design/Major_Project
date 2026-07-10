# User Manual

# Virtual Agent–Driven SLA Breach Awareness & Justification System

Version: 1.0

---

# 1. Introduction

This system helps organizations proactively monitor Service Level Agreements (SLAs), notify users before SLA breaches occur, enforce mandatory breach justification, and provide real-time visibility through dashboards and reports.

---

# 2. User Roles

### Service Desk Agent

- Create and update incidents
- View SLA status
- Receive SLA warning notifications
- Submit SLA breach justification

### Incident Manager

- Monitor SLA compliance
- Review breached incidents
- Approve or review justifications
- View reports

### ServiceNow Administrator

- Configure SLAs
- Manage Flow Designer
- Configure Virtual Agent
- Configure dashboards
- Manage user roles

---

# 3. Creating an Incident

1. Navigate to **Incident > Create New**.
2. Enter the required incident details.
3. Assign the incident.
4. Save the record.

Result:
- SLA starts automatically.

---

# 4. Viewing SLA Status

Open the incident record.

The incident displays:

- SLA Name
- Remaining Time
- Current SLA Status
- Assigned User

---

# 5. SLA Warning Notifications

When an SLA approaches its warning threshold:

- Email notification is sent.
- Virtual Agent reminds the assignee.
- Incident remains active.

---

# 6. SLA Breach

When the SLA expires:

- Incident is marked as Breached.
- Justification field becomes mandatory.
- Breach notification is sent.

---

# 7. Providing Breach Justification

1. Open the breached incident.
2. Enter the reason in the **Justification** field.
3. Save the incident.

The incident cannot be closed without a valid justification.

---

# 8. Using the Virtual Agent

The Virtual Agent can:

- Show SLA status
- Warn about upcoming breaches
- Guide users through justification submission
- Answer common SLA-related questions

---

# 9. Dashboard

Managers can monitor:

- Total Incidents
- Active Incidents
- Breached Incidents
- SLA Compliance
- Monthly Trends

---

# 10. Reports

Available reports include:

- Incident Summary
- SLA Performance
- Breached Incidents
- Justification Report
- Compliance Percentage

---

# 11. Troubleshooting

| Problem | Solution |
|----------|----------|
| Notification not received | Verify Flow Designer and notification configuration |
| Justification field missing | Verify UI Policy is active |
| SLA not starting | Check SLA Definition |
| Dashboard empty | Verify report data and permissions |

---

# 12. Best Practices

- Update incidents regularly.
- Respond promptly to SLA warnings.
- Provide meaningful breach justifications.
- Review dashboards periodically.