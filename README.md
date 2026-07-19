# Azure CloudGuard

Azure CloudGuard is an Azure Security Monitoring and Incident Response project built to demonstrate real-world cloud security operations using Microsoft Azure services. The project simulates how security events are collected, analyzed, detected, and automated using Microsoft Sentinel.

---

# Project Objectives

- Configure Azure Monitor Agent (AMA)
- Collect Linux Syslog logs using Data Collection Rules (DCR)
- Store logs in Azure Log Analytics Workspace
- Create custom analytics rules in Microsoft Sentinel
- Generate Security Incidents automatically
- Trigger automated response using Logic Apps
- Send email notifications for detected incidents
- Perform investigation using Kusto Query Language (KQL)

---

# Architecture

![CloudGuard Architecture](docs/architecture/cloudguard-architecture.png)

---

# Azure Services Used

| Service | Purpose |
|----------|----------|
| Azure Virtual Machine | Generates Linux Syslog logs |
| Azure Monitor Agent | Collects telemetry |
| Data Collection Rule | Defines log collection |
| Log Analytics Workspace | Stores collected logs |
| Microsoft Sentinel | SIEM and Incident Management |
| Analytics Rules | Detect suspicious activities |
| Automation Rules | Trigger response workflow |
| Logic Apps | Automated email notification |
| Outlook Connector | Sends incident email |

---

# Project Workflow

```
Linux VM
      │
      ▼
Azure Monitor Agent
      │
      ▼
Data Collection Rule
      │
      ▼
Log Analytics Workspace
      │
      ▼
Microsoft Sentinel
      │
      ▼
Analytics Rule
      │
      ▼
Security Incident
      │
      ▼
Automation Rule
      │
      ▼
Logic App
      │
      ▼
Email Notification
```

---

# Screenshots

## Resource Group

![Resource Group](docs/screenshots/01-resource-group.png)

---

## Azure Virtual Machine

![Virtual Machine](docs/screenshots/02-vm.png)

---

## Data Collection Rule

![DCR](docs/screenshots/03-data-collection-rule.png)

---

## Log Analytics Workspace

![LAW](docs/screenshots/04-log-analytics-workspace.png)

---

## KQL Query Validation

![KQL](docs/screenshots/05-kql-query-results.png)

---

## Sentinel Analytics Rule

![Analytics Rule](docs/screenshots/06-sentinel-analytics-rule.png)

---

## Security Incident

![Incident](docs/screenshots/07-security-incident.png)

---

## Automation Rule

![Automation Rule](docs/screenshots/08-automation-rule.png)

---

## Logic App

![Logic App](docs/screenshots/09-logic-app.png)

---

## Logic App Run History

![Run History](docs/screenshots/10-logic-app-run-history.png)

---

## Email Notification

![Email Notification](docs/screenshots/11-email-notification.png)

---

# KQL Validation Query

```kusto
Syslog
| where TimeGenerated > ago(24h)
| project TimeGenerated, Computer, Facility, ProcessName, SyslogMessage
| order by TimeGenerated desc
```

---

# Skills Demonstrated

- Microsoft Azure
- Microsoft Sentinel
- Azure Monitor
- Azure Monitor Agent
- Data Collection Rules
- Log Analytics Workspace
- Kusto Query Language (KQL)
- Logic Apps
- Security Incident Management
- Cloud Security Monitoring
- Security Operations (SOC)

---

# Future Improvements

- Teams Notifications
- Azure Functions Integration
- Defender for Cloud Integration
- Playbook Enhancements
- Multiple Detection Rules
- Threat Intelligence Integration

---

# Author

**Saravanan K**

Cloud & Azure Security Enthusiast

LinkedIn:
https://linkedin.com/in/saravanankannan10

GitHub:
https://github.com/Saravanagithub10
