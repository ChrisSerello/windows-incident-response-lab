# windows-incident-response-lab

This project simulates real-world Windows security incidents inside a controlled lab environment.

## Objetivo
Demonstrate detection, log analysis and incident response skills using native Windows logging and security monitoring.

## Lab Architecture
- Windows 10 vm
- Local security auditing enabled
- event viewer analysis
- powershell logging enabled

### Incident 01 — Suspicious PowerShell Execution (Event ID 4104)

Execution with:

  - NoProfile
  - WindowStyle Hidden
  - ExecutionPolicy Bypass
  
#### Detection via:

 - Microsoft-Windows-PowerShell/Operational

#### Risk:

 - Execution policy bypass technique often used by attackers.

## Incident 02 — Failed Logon Attempts Followed by Success (4625 → 4624)

- Multiple failed interactive logons (Logon Type 2)
- Followed by successful authentication

#### Risk:

- Credential guessing behavior
- Potential brute force scenario

## Incident 03 — Sensitive File Access Monitoring (Event ID 4663)

- Object access auditing enabled
- Monitoring access to Financeiro/senhas.txt
- Detection of unauthorized read attempts

### Skills Demonstrated

- Windows Security Log Analysis
- Event ID correlation
- PowerShell forensic analysis
- Object Access auditing
- Incident timeline reconstruction

🚀 Tools Used

- Windows Event Viewer
- Local Security Policy
- PowerShell
- VirtualBox
