# Windows2019Server-CIS-Hardening Script

---
## CIS Hardening
- We all know that Windows2019 Server is widely and all the sys admins are upgrading towards to it and I did the hardening for one my Dev/QA and Prod Env. I thought this script may helps others as well.
- This script  remediates 158 controls.
---

Check the full script before using it - this may break multiple services
Test it in Dev/QA ENV and then go for Prod
If you face any issue - please reach me at aadham.m@outlook.com



*How to use the script : **

    [+] Ensure you have PowerShell version v5 or higher - use this command to check the version : PSVersionTable.PSVersion
    [+] Ensure bypass powershell execution policies :
    Set-ExecutionPolicy `
    -Scope Process `
    -ExecutionPolicy Bypass
    [+] Install the following DSC modules to run PowerShell commands
    
    Get-InstalledModule -Name AuditPolicyDsc
    Get-InstalledModule -Name SecurityPolicyDsc
    Get-InstalledModule -Name NetworkingDsc
    Get-InstalledModule -Name NetworkingDsc
    Get-InstalledModule -Name PSDesiredStateConfiguration
    
    Install-Module -Name  AuditPolicyDsc
    Install-Module -Name  SecurityPolicyDsc
    Install-Module -Name  NetworkingDsc
    Install-Module -Name  NetworkingDsc
    Install-Module -Name  PSDesiredStateConfiguration
    
    [+] download the script
    
    wget https://raw.githubusercontent.com/ha3k4r-sh/Windows2019Server-CIS-Hardening/main/windows2019_server_hardening.ps1
    .\windows2019_server_hardening.ps1
    Start-DscConfiguration -Path .\windows2019_server_hardening.ps1  -Force -Verbose -Wait
    
    
    
    
