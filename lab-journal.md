# Day 1 – Environment Setup

## Completed
- Installed Oracle VirtualBox.
- Imported and configured Kali Linux virtual machine.
- Downloaded Windows 11 ISO from Microsoft.
- Created Windows 11 virtual machine.
- Allocated VM resources (4 GB RAM, 2 CPUs, 80 GB virtual disk).
- Started Windows 11 installation and completed initial setup.
- Created GitHub repository (SOC-Lab).
- Added project documentation structure (README, lab journal, screenshots).
- Captured initial lab screenshots.

## Skills Practiced
- Virtualization
- Operating system installation
- VM resource management
- GitHub documentation

## Outcome
Successfully built the foundation of a SOC lab with Windows 11 and Kali Linux virtual machines running in VirtualBox.

# Day 2 – Sysmon Deployment

## Objective
Deploy Sysmon on the Windows 11 virtual machine to improve endpoint visibility and generate detailed security telemetry.

## Planned Activities
- Download Microsoft Sysmon.
- Install Sysmon on Windows 11.
- Verify Sysmon service installation.
- Review Sysmon events in Event Viewer.
- Generate test activity and confirm logging.

## Expected Outcome
Establish enhanced endpoint logging that will later be ingested into Splunk for monitoring and threat detection.

Day 3 – Sysmon Event Analysis
Objective

Deploy Sysmon successfully and begin analyzing endpoint telemetry through Windows Event Viewer to understand process creation and network activity monitoring.

Completed
Downloaded and installed Microsoft Sysmon on the Windows 11 VM.
Verified Sysmon service was installed and running correctly.
Opened and navigated the Microsoft-Windows-Sysmon/Operational log in Event Viewer.
Filtered logs using Event ID 1 (Process Creation).
Generated test activity by launching applications including:
Microsoft Edge
Windows Explorer
Command Prompt
Ping utility
Reviewed Sysmon event details including:
Process Name
Process ID
Parent Process
Command Line
User Account
Hash Information
UTC Timestamp
Identified parent-child process relationships between applications.
Verified DNS resolution and internet connectivity inside the Windows 11 VM.
Captured screenshots for documentation.
Skills Practiced
Endpoint monitoring
Sysmon deployment
Event Viewer navigation
Process creation analysis
Parent-child process investigation
Basic threat hunting concepts
Windows logging fundamentals
Key Learning

Sysmon provides significantly more detailed telemetry than standard Windows logs. Event ID 1 records process creation events and allows analysts to track which applications were executed, who launched them, when they ran, and what process spawned them.

Outcome

Successfully deployed Sysmon and confirmed visibility into endpoint activity. Established the foundation for future log ingestion into Splunk and SOC-style monitoring workflows.

# Day 4 – Splunk Enterprise Installation

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

# Day 5 Splunk SIEM Successfully Receiving Windows Logs 
Objective

Configure a basic SOC lab by forwarding Windows Security logs from a Windows 11 virtual machine to Splunk Enterprise running on the host PC.

Environment

Host Machine

Windows 11
Splunk Enterprise

Virtual Machine

Windows 11
Hostname: SOC-WIN11
Splunk Universal Forwarder installed
Tasks Completed

✅ Installed Splunk Universal Forwarder on Windows 11 VM

✅ Configured deployment/output settings

✅ Configured Splunk Enterprise to receive forwarded data on TCP port 9997

✅ Restarted the Universal Forwarder

✅ Verified connectivity between the VM and Splunk Enterprise

✅ Confirmed Windows Event Logs were successfully ingested

Successfully receiving:

Windows Security Logs
Windows System Logs
SPL Searches Tested
index=*
host=*
source="WinEventLog:Security"

Verified Event IDs including:

4624 — Successful Logon
4672 — Special Privileges Assigned
Windows Security Events streaming successfully
Challenges Encountered
Initially no logs appeared in Splunk.
Realized Splunk Enterprise was not configured to receive forwarded data.
Enabled receiving on TCP port 9997.
Restarted the Universal Forwarder.
Successfully confirmed data ingestion.
Skills Practiced
Splunk Enterprise Administration
Splunk Universal Forwarder
Windows Event Logs
Windows Security Logs
Basic SIEM Administration
Log Ingestion
Event Searching using SPL
Troubleshooting data forwarding
Next Steps
Install Sysmon on Windows VM
Generate failed login events (4625)
Simulate attacks from Kali Linux
Build Splunk dashboards
Create detections for authentication events
Begin basic threat hunting exercises
Reflection

Today was one of the biggest milestones in my cybersecurity journey. For the first time, I successfully configured a SIEM to collect real Windows Security logs from a separate virtual machine. Although it took troubleshooting and patience, seeing live security events arrive in Splunk confirmed that the lab is functioning correctly. This setup will serve as the foundation for future detection engineering, incident response, and threat hunting practice.

