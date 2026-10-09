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
- Practiced **help desk troubleshooting** workflows for password resets, account lockouts, printer issues, folder access problems, workstation performance, and user offboarding
- Configured **Active Directory**, **DNS**, **DHCP**, and **Group Policy** to simulate an enterprise-style Windows domain environment
- Gained hands-on experience resolving **realistic end-user tickets** using Active Directory Users and Computers, RDP, Task Manager, Print Spooler, and Windows settings
- Learned to **document, track, resolve, and verify issues** using a ServiceNow ticketing workflow
- Improved understanding of how help desk technicians troubleshoot user issues, apply fixes, communicate resolutions, and maintain accurate documentation
---
## Screenshot Documentation
![](./screenshots/1.png)
![](./screenshots/2.png)
![](./screenshots/3.png)
![](./screenshots/4.png)
![](./screenshots/5.png)
- **Screenshots above are ServiceNow documentation**
![](./screenshots/6.png)
![](./screenshots/7.png)
![](./screenshots/8.png)
![](./screenshots/9.png)
![](./screenshots/10.png)
![](./screenshots/11.png)
![](./screenshots/12.png)
![](./screenshots/13.png)
![](./screenshots/14.png)
![](./screenshots/15.png)
- **Screenshots above are Windows Server domain and policy configuration**
![](./screenshots/16.png)
![](./screenshots/17.png)
- **Screenshots above show the use of RDP for user troubleshooting tickets**
![](./screenshots/18.png)
- **Screenshot above shows the folder access ticket being resolved by updating permissions for Sally**
![](./screenshots/19.png)
- **Screenshot above shows the printer issue ticket being resolved by restarting the Print Spooler service**
![](./screenshots/20.png)
- **Screenshot above shows the account lockout ticket being resolved in Active Directory**
![](./screenshots/21.png)
- **Screenshot above shows the password reset ticket being resolved in Active Directory**
![](./screenshots/22.png)
- **Screenshot above shows the account disable ticket being resolved in Active Directory**
