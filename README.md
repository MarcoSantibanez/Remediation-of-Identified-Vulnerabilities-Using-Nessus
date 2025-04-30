# Remediation-of-Identified-Vulnerabilities-Using-Nessus

🔐 Remediating Critical CVEs Using Nessus and Windows Native Tools
📋 Overview
This project documents the identification and remediation of a critical vulnerabilities using Nessus by Tenable for detection and native Windows tools for mitigation.
<hr>
Multiple Critical Vulnerabilities Identified
<hr>
🛠 Tools & Technologies Used
🔍 Nessus Vulnerability Scanner – For identifying vulnerabilities like CVE-2021-43905 and outdated .NET Framework versions

💻 Windows CMD / PowerShell – Used to investigate app versions, paths, and initiate update processes

🛒 Microsoft Store – For updating Microsoft 365 (Office) and other Store-based apps

🧰 Office Deployment Tool (ODT) – For managing Office installations and configuration via XML

📁 WindowsApps / Click-to-Run Infrastructure – Investigated app installation paths and versioning

🔄 Windows Update – Used to install security updates for Microsoft .NET Framework (Jan 2024 & Nov 2023 patches)
<hr>
🧪 Steps Performed
Conducted a full vulnerability credentialed scans using Nessus.

Confirmed the vulnerabilities via self-reported application version.

Verified affected component:
C:\Program Files\WindowsApps\Microsoft.MicrosoftOfficeHub_18.1903.1152.0_x64__8wekyb3d8bbwe
C:\Program Files (x86)\Microsoft\Edge\Application
C:\Program Files\WindowsApps\Microsoft.HEIFImageExtension_1.0.22742.0_x64__8wekyb3d8bbwe
C:\Program Files\WindowsApps\Microsoft.MSPaint_6.1907.29027.0_x64__8wekyb3d8bbwe
C:\Windows\Microsoft.NET\Framework\v4.0.30319\system.web.dll


Investigated Microsoft Store access to trigger update for OfficeHub.

Used PowerShell and Store troubleshooting to ensure Microsoft Store was functional.

Upgraded the Office app to the patched version via Microsoft Store.

Updated Edge to newer version. 

Updated paint 3D through Microsot Store.

Updated HEIF Image Extension through Microsoft Store. 

Validated the fixes by re-running the Nessus scan.
<hr> 
🔍 OSINT / Research
Researched CVE on the Microsoft Security Update Guide.

Correlated information with patch notes and Microsoft documentation.
<hr> 
Reviewed installation paths and Store app behavior using PowerShell, including:

powershell
Copy
Edit
Get-AppxPackage -Name *office* | Select Name, Version, InstallLocation
📁 Notes
This system used an MSI-based clean OS install with Microsoft 365 installed from the Microsoft Store.

The vulnerability required no user interaction once a malicious file was processed, making it critical to patch promptly.

Bash and Git Bash were not used in this task to remain consistent with the native Windows environment.
<hr> 
✅ Outcome
Vulnerabilities successfully remediated.

System confirmed to be running safe version (18.2110.13110.0) or later.

System prepared for ongoing compliance and patch management.
![ConfiguiringScan](https://github.com/user-attachments/assets/f6796a21-3585-4274-918b-b6286ce5db6b)

![image](https://github.com/user-attachments/assets/0c06b146-fbe8-4a06-af21-45f4ebe07aa9)

![Vulnerabilities ](https://github.com/user-attachments/assets/cd0da4be-5506-414a-b7ea-1c32b5bd997d)

![MicrosoftUpdate](https://github.com/user-attachments/assets/b4495960-92ea-4af9-8f45-523e06148d26)

![RemediationOFEdgeVulnerability](https://github.com/user-attachments/assets/f39722ea-0675-4731-993d-d95c414a3b72)

![RemediationOFVulnerabilityAndNewVulnerabilities](https://github.com/user-attachments/assets/721969d5-4ef6-43e4-97a1-5758bc8992cf)

![image](https://github.com/user-attachments/assets/7c7a4677-7a5a-4455-ad92-b3db5da83c26)
All Critical Vulnerabilities Remediated 
![image](https://github.com/user-attachments/assets/19ce1427-7d78-4b55-b0c2-6740614d703e)


