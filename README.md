# Wazuh SIEM Home Lab
## Project Overview

This project demonstrates the deployment and configuration of a Wazuh SIEM home lab environment for security monitoring, log analysis, and threat detection. The lab was built using multiple virtual machines in Oracle VirtualBox to simulate a small enterprise monitoring environment.

## The setup includes:

A Wazuh server for centralized monitoring and analytics
A Windows endpoint configured as a monitored agent
A Kali Linux machine used for reconnaissance and testing
VirtualBox host-only networking for isolated communication

## The project focuses on:

Endpoint monitoring
Security event collection
Authentication failure detection
Network reconnaissance
MITRE ATT&CK event correlation
SIEM dashboard analysis
🛠️ Technologies Used
Wazuh SIEM
Kali Linux
Windows Server 2022
Oracle VirtualBox
Nmap
PowerShell
Linux Terminal
Host-Only Networking

## Lab Architecture
Kali Linux VM (Attacker/Test System)
        │
        │ 192.168.56.102
        │
────────────────────────────
Host-Only Virtual Network
────────────────────────────
        │
        │ 192.168.56.106
        │
Windows Server 2022 VM
(Wazuh Agent Installed)
        │
        ▼
Wazuh SIEM Server
(Security Monitoring & Analytics)

## Features Demonstrated
Wazuh server deployment
Agent registration and endpoint monitoring
Security event collection
Authentication failure detection
MITRE ATT&CK mapping
Log analysis and visualization
Nmap reconnaissance scans
Dashboard monitoring and alerting
Virtualized SOC-style environment

## Repository Structure
wazuh-siem-home-lab/
│
├── README.md
│
├── screenshots/
│   ├── wazuh-dashboard.png
│   ├── wazuh-agent-status.png
│   ├── security-events.png
│   ├── failed-login-alert.png
│   ├── nmap-scan.png
│   └── vm-networking.png
│
├── configs/
│   ├── ossec.conf
│   ├── local_internal_options.conf
│   └── network-settings.txt
│
├── logs/
│   ├── sample-alerts.txt
│   ├── authentication-failures.txt
│   └── nmap-results.txt
│
└── documentation/
    ├── setup-steps.md
    ├── architecture.md
    └── troubleshooting.md
    
## Setup Process
1. Create Virtual Machines
Kali Linux VM
Windows Server 2022 VM
Wazuh Server VM
2. Configure Networking
Enable Host-Only Adapter
Assign private IP addresses
Verify connectivity using ping
3. Install Wazuh Server
Install Wazuh manager and dashboard
Verify running services
4. Install Wazuh Agent
Deploy agent on Windows Server
Configure server IP in ossec.conf
Register agent with Wazuh server
5. Generate Security Events
Failed logins
Logon/logoff activity
Service events
Network scans
6. Monitor Events
Analyze logs in Wazuh dashboard
Observe MITRE ATT&CK mappings
Review alert evolution graphs

## Reconnaissance Testing

Nmap was used from the Kali Linux VM to perform:

Host discovery
Service enumeration
Port scanning

Example command:

nmap -A <target-ip>
## Security Monitoring Highlights

The Wazuh dashboard captured:

Authentication failures
Windows logon activity
PAM login events
Privilege escalation activity
MITRE ATT&CK correlations
Alert level evolution

# Screenshots
Wazuh Dashboard

Displays overall agent monitoring and alert analytics.

![]()

Agent Status

Shows registered Windows endpoint information.

![]()

Security Events

Displays collected logs and security alerts.

![]()

Failed Login Detection

Demonstrates authentication failure monitoring.

![Failed-Login-Detection](https://github.com/AdityaDNair/Active-Directory-Lab/blob/main/screenshots/failed-login-alert.png?raw=true)

Nmap Scan

Shows reconnaissance activity from Kali Linux.

![Nmap-Scan](https://github.com/AdityaDNair/Active-Directory-Lab/blob/main/screenshots/kali-nmap-scan.png?raw=true)

VM Networking

Displays isolated lab network communication.

![]()

## Learning Outcomes

Through this project, I gained hands-on experience with:

SIEM deployment and configuration
Endpoint security monitoring
Security event analysis
Threat detection workflows
Virtualized cybersecurity lab environments
Linux and Windows administration
Network troubleshooting
Log management and correlation

## Future Improvements
Add Sysmon integration
Deploy additional Windows/Linux agents
Configure email alerting
Integrate Suricata IDS
Add custom Wazuh rules
Simulate ransomware behavior
Forward logs to external storage
