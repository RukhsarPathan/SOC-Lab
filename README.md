# SOC-Lab

Building a SOC home lab using Windows 11, Kali Linux, Sysmon, and Splunk to develop hands-on experience in security monitoring, threat detection, log analysis, and SOC analyst workflows.

## Overview

This project documents the creation of a Security Operations Center (SOC) home lab built in VirtualBox. The lab is designed to simulate real-world security monitoring activities and provide practical experience with endpoint telemetry, event analysis, SIEM technologies, and incident investigation.

## Technologies Used

- Windows 11
- Kali Linux
- Oracle VirtualBox
- Microsoft Sysmon
- Splunk (Coming Soon)

## Goals

- Learn SIEM fundamentals
- Analyze Windows event logs
- Monitor endpoint activity with Sysmon
- Detect suspicious behavior
- Practice SOC analyst workflows
- Develop threat detection skills
- Build a cybersecurity portfolio project

## Lab Architecture

Kali Linux VM (Attacker)
        │
        ▼

        
Windows 11 VM (Target)
├── Sysmon
├── Windows Event Logs
└── Event Viewer Analysis
        │
        ▼
        
Splunk (Coming Soon)

## Lab Components

- Windows 11 VM
- Kali Linux VM
- Sysmon
- Windows Event Logs
- Splunk (Planned)

## Project Status

### Phase 1 – Environment Setup ✅

- Installed Oracle VirtualBox
- Created Windows 11 VM
- Imported Kali Linux VM
- Configured virtual environment

### Phase 2 – Endpoint Monitoring ✅

- Installed Microsoft Sysmon
- Verified Sysmon service operation
- Analyzed Process Creation events (Event ID 1)
- Investigated parent-child process relationships
- Generated test activity using Microsoft Edge, Windows Explorer, and Command Prompt

### Phase 3 – SIEM Integration 🚧

- Splunk installation
- Windows Event Log ingestion
- Sysmon log ingestion
- Dashboard creation

## Planned Detection Use Cases

- Failed Login Detection (Event ID 4625)
- Successful Login Monitoring (Event ID 4624)
- Process Creation Monitoring (Sysmon Event ID 1)
- Network Connection Monitoring (Sysmon Event ID 3)
- PowerShell Activity Monitoring
- Basic Threat Hunting



- Windows 11 VM and Kali Linux VM running in VirtualBox.

### Virtual Machines

![VM Overview](Screenshots/Vms%20screenshot.png)

### Windows and Kali Setup

![Windows and Kali](Screenshots/WIndowsKali.png)

### Sysmon Installation

*Sysmon successfully installed and operational.*

![Insert Screenshot](Screenshots/Sysmon-install.png)

### Event ID 1 Analysis

*Process creation monitoring using Sysmon Event ID 1.*

![Event ID](Screenshots/eventid.png)

### Microsoft Edge Process Creation

Sysmon Event ID 1 capturing the execution of Microsoft Edge (msedge.exe) and associated process metadata.
![MS Edge Execution](Screenshots/msedgesysmon.png)

### Splunk Enterprise Installation and Configuration 

## Objective

Install and configure Splunk Enterprise on the host machine to serve as the Security Information and Event Management (SIEM) platform for collecting, indexing, and analyzing security logs from the Windows 11 virtual machine.

## Completed

* Downloaded Splunk Enterprise 10.4.0 for Windows.
* Installed Splunk Enterprise on the Windows host machine.
* Created the Splunk administrator account during installation.
* Successfully launched the Splunk web interface.
* Verified access to the Splunk Enterprise dashboard using a web browser.
* Confirmed the SIEM platform is operational and ready to receive log data.

## Skills Practiced

* SIEM deployment
* Splunk Enterprise installation
* Initial Splunk configuration
* Web interface administration
* Security monitoring infrastructure setup

## Key Learning

Splunk Enterprise serves as the central platform for collecting, indexing, searching, and analyzing security data. Rather than storing logs on individual systems, endpoint devices can forward their logs to Splunk, allowing security analysts to investigate events from a centralized location.

## Outcome

Successfully deployed Splunk Enterprise on the host machine, establishing the core SIEM infrastructure for the SOC lab. The environment is now prepared for integrating the Windows 11 virtual machine using the Splunk Universal Forwarder and ingesting Sysmon and Windows Event Logs for security monitoring.

![Splunk Installation](Screenshots/Splunk-install.png)


## Project Status

🚧 In Progress
