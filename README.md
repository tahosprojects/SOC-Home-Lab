# Active Directory SOC Lab with Splunk SIEM

## Overview

This project simulates a Security Operations Center (SOC) environment using Active Directory, Splunk Enterprise, Sysmon, Kali Linux, and Atomic Red Team. The lab focuses on centralized log collection, security monitoring, attack simulation, and threat detection using Windows event logs and custom Splunk searches.

## Objectives

- Deploy and configure an Active Directory environment
- Centralize Windows event logs in Splunk Enterprise
- Configure Sysmon for enhanced endpoint visibility
- Simulate attacker activity against the environment
- Detect and investigate security events using Splunk
- Map attacker behavior to MITRE ATT&CK techniques

## Lab Environment

### Components

- Windows Server 2022 Domain Controller
- Windows Endpoint
- Splunk Enterprise SIEM
- Sysmon
- Kali Linux Attack Machine
- Atomic Red Team

## Tools Used

- Splunk Enterprise
- Sysmon
- Active Directory
- Kali Linux
- Crowbar
- Atomic Red Team
- Windows Event Logs

## Skills Demonstrated

- SIEM Administration
- Log Analysis
- Active Directory Security Monitoring
- Threat Hunting
- Detection Engineering
- Windows Event Investigation
- MITRE ATT&CK Mapping
- Security Operations (SOC) Workflows

## Attack Scenarios

### Brute Force Authentication Attempts

A password-spraying and brute-force simulation was conducted against the Windows environment. Failed authentication events were collected and analyzed within Splunk.

### Account Creation Detection

Atomic Red Team tests were used to simulate malicious account creation activity. Security Event ID 4720 was monitored to validate detection capabilities.

### Process Creation Monitoring

Process creation activity was collected through Sysmon and Windows Security logs. Event ID 4688 was analyzed to identify suspicious process execution.

## Key Findings

- Successfully centralized endpoint and security logs into Splunk.
- Detected failed authentication attempts using Event ID 4625.
- Monitored account creation activity using Event ID 4720.
- Investigated process creation events using Event ID 4688.
- Validated detection coverage through Atomic Red Team simulations.
- Improved visibility into endpoint activity using Sysmon telemetry.

## Screenshots

### Domain Join Configuration

![Domain Join](images/domain-join.png)

### Lab Architecture

![Architecture](images/architecture.png)

### Splunk Log Ingestion

![Log Ingestion](images/splunk-log-ingestion.png)

### Failed Logon Detection (Event ID 4625)

![Event 4625](images/event-4625-failed-logons.png)

### Process Creation Monitoring (Event ID 4688)

![Event 4688](images/event-4688-process-creation.png)

### User Account Creation Detection (Event ID 4720)

![Event 4720](images/event-4720-account-creation.png)

## MITRE ATT&CK Techniques

| Technique | Description |
|------------|------------|
| T1110 | Brute Force |
| T1136 | Create Account |
| T1059 | Command and Scripting Interpreter |
| T1087 | Account Discovery |

## Analyst Output
- [INC-2026-001 Incident Summary](./INC-2026-001_Incident_Summary.pdf) — Multi-stage intrusion report covering brute force detection, persistence, execution, and account discovery across four MITRE ATT&CK techniques.

## Repository Contents

- README.md
- AD_SOC_Lab_WriteUp_v3.pdf
- INC-2026-001 Incident Summary.pdf
- images/

## Key Takeaway

This project provided hands-on experience building a SOC environment, ingesting endpoint telemetry into Splunk, simulating adversary activity, and developing detections for common attack techniques. It strengthened practical skills in SIEM operations, threat hunting, and Windows security monitoring.
