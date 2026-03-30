# Active Directory & IAM Lab – Windows Server 2022

A home lab where I built a complete Active Directory environment from scratch to understand how identity and access management works in practice – user lifecycle, group policies, and role-based access control in a Windows domain.

---

## Overview

Most enterprise environments run on Active Directory. This lab gave me hands-on experience with the same tools and concepts used in real IT departments, and a practical understanding of how on-premises AD connects to cloud identity platforms like Azure AD / Entra ID and Okta.

---

## Tools & Technologies

- Windows Server 2022 (VirtualBox)
- Active Directory Domain Services (AD DS)
- Group Policy Management Console (GPMC)
- Windows 10 Pro (domain-joined client machine)

---

## What I Did

### Domain Setup
- Installed Windows Server 2022 in VirtualBox
- Configured static IP and promoted the server to a domain controller
- Created a new AD forest and domain (`lab.local`)

### Organizational Structure
- Created Organizational Units (OUs) for HR, IT, and Finance
- Added user accounts and placed them in the correct OUs
- Structured the directory to reflect a realistic company hierarchy

### Groups & RBAC
- Created security groups per department
- Assigned resource permissions to groups, not individual accounts
- Tested role-based access control (RBAC) – verified users could only access what their role allowed

### Group Policy (GPO)
- Configured password policy (minimum length, complexity, expiration)
- Enforced screen lock after inactivity
- Restricted Control Panel access for non-admin users

### User Lifecycle
- Simulated onboarding: create account → assign OU → assign group → verify access
- Simulated offboarding: disable account → remove group memberships → archive

---

## Key Takeaways

- How AD structure with OUs and groups reflects a real organization's permission model
- Why RBAC is more scalable and auditable than per-user permission management
- How GPOs enforce security policies across an entire environment centrally
- The relationship between on-premises AD and cloud identity platforms like Azure AD

---

## Related Concepts

`Active Directory` `IAM` `RBAC` `GPO` `Windows Server` `Identity Management` `Onboarding` `Offboarding` `Azure AD`

