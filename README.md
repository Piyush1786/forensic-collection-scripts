# forensic-collection-scripts
Pre-requisites : Install osquery on your machine

# Forensic Collection Scripts for Windows and Linux

This repository contains ready-to-use forensic data collection scripts for both Windows and Linux systems. These scripts are ideal for cybersecurity analysts, incident responders, or red teamers who need quick system auditing capabilities.

## 🪟 Windows Script: `Windows_ansible.txt`

The Windows script (PowerShell + osquery based) automates:
- Browser extension audits (Chrome, Firefox, Edge)
- System and process inspections via osquery
- Event log parsing for critical security events
- Privilege escalation and user audits
- Persistence mechanism detection

📁 **Output Directory**: `C:\Temp\Forensic`

## 🐧 Linux Script: `Linux_forensic.txt`

The Linux script (osquery + shell commands) performs:
- System and user audits
- Network and process inspection
- SSH and sudo log analysis
- Persistence detection via crontabs, systemd, etc.
- Privilege escalation checks

📁 **Output Directory**: `/var/log/osquery` or `/var/log/forensics/`

## 🛠 Usage

- On **Windows**: Run the PowerShell script as administrator.
- On **Linux**: Ensure `osqueryi` is installed and run the script with sudo privileges.


