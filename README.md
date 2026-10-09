# Active-Directory-ServiceNow-Ticketing-Lab
Simulated IT help desk project using **Active Directory**, **Group Policy**, **Remote Desktop Protocol (RDP)**, and **ServiceNow** to document real-world troubleshooting tickets such as password resets, account lockouts, workstation issues, printer problems, folder access permissions, and user offboarding in a Windows Server lab environment.

## Services used
- **Active Directory**
- **ServiceNow Ticketing System**
- **Remote Desktop Protocol (RDP)**
- **DNS & DHCP**
---
## Topology
- **Windows Server 2022 (Domain Controller)**- Configured AD, DNS, DHCP, and Group Policies
- **Windows 10 Client**- Simulated end-user device connecting and troubleshooting via RDP on a host only network
---
## Process
### Windows Server
- Set up **Active Directory Domain Services** and promoted to Domain Controller
- Created an **Organizational Unit** for the IT users and users with intentional misconfigurations
- Applied **Group Policies** for password complexity, account lockout, and screen lock
- Simulated **tickets** such as password resets, access issues, and setting misconfigurations
- Documented steps and resolutions in **ServiceNow**
- Verified fixes before closing tickets
- PASSWORD POLICY AND ACCOUNT LOCKOUT PATH (group policy management> expand the forest> right click default domain policy and select edit> computer configuration> policies> windows settings> security settings> account policies> password policies)
- SCREEN LOCK POLICY PATH (create GPO in domain> edit> user configuration> administrative templates> control panel> personalization)
- ENFORCED POLICIES AFTER IN COMMAND PROMPT WITH `gpupdate /force`
  
### Windows Client
- Connected Windows Client to the Domain Controller (system settings> about> advanced system settings> computer name> change)
- Configured user accounts and misconfigurations, documenting issues and solutions
---
## Tickets in ServiceNow
**Ticket | Description | Resolution**
*********************************
- Password Reset | User forgot password | Reset password in ADUC
- Account Lockout | Multiple failed logins triggered the lockout policy | Unlocked the account in ADUC
- Slow Computer | Workstation was running slowly due to high resource usage | Reviewed Task Manager, closed unnecessary processes, and restarted the computer
- Folder Access | User could not access the shared folder | Updated folder permissions and added the user to the correct access group
- Printer Issue | Printer was not appearing or print jobs were not processing | Restarted the Print Spooler service
- Display Setting Issue | Incorrect display scaling or resolution | Restored the recommended display settings
- Timezone Setting Issue | Wrong time shown on workstation | Corrected the time zone settings
- User offboarding | Employee offboarding request | Disabled the account in ADUC

## Outcome
- Practiced **helpdesk troubleshooting** workflow
- Configured **Active Directory** and **Group Policy** for enterprise-style management
- Gained hands-on experience resolving **realistic end-user tickets**
- Learned to **document and track issues** using a ticketing workflow 
---
