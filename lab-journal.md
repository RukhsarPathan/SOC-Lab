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
