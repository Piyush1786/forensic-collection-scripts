# forensic-collection-scripts
Pre-requisites : Install osquery on your machine

🧠 What is osquery?
osquery is an open-source tool developed by Facebook that lets you query your operating system like a relational database. You can use SQL-like queries to extract system data such as:

Running processes

User accounts

Network connections

Scheduled tasks

Installed software

Kernel modules

Browser plugins

It is widely used in security investigations, forensics, compliance, and threat hunting.

📦 How to Install osquery
🔹 On Windows
Download the latest Windows .msi installer from:

https://pkg.osquery.io/windows/

Run the installer and complete installation.

By default, osqueryi.exe will be installed at:

makefile
Copy
Edit
C:\Program Files\osquery\osqueryi.exe
🔹 On Linux (Debian/Ubuntu)
bash
Copy
Edit
sudo apt update
sudo apt install gnupg -y
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://pkg.osquery.io/gpg.key | gpg --dearmor | sudo tee /etc/apt/keyrings/osquery.gpg > /dev/null

echo "deb [signed-by=/etc/apt/keyrings/osquery.gpg] https://pkg.osquery.io/deb deb main" | sudo tee /etc/apt/sources.list.d/osquery.list
sudo apt update
sudo apt install osquery -y
🔹 On RHEL/CentOS
bash
Copy
Edit
sudo yum install yum-utils -y
sudo yum-config-manager --add-repo https://pkg.osquery.io/rpm/osquery-s3-rpm.repo
sudo yum install osquery -y
You can now run:

bash
Copy
Edit
osqueryi




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


