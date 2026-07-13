# Active Directory to Entra ID: same concepts, different names

Most identity concepts don't disappear when an organization moves to the cloud — they get renamed and re-implemented. This document is my working translation between on-prem Active Directory concepts and their Azure Entra ID equivalents.

Understanding both sides is the foundation of **hybrid identity** — how most real organizations actually operate: legacy on-prem AD for internal resources, Entra ID for cloud and SaaS, and a sync layer (Entra Connect) tying them together.

---

## Terminology bridge

| On-prem Active Directory | Entra ID (cloud) | What it does |
|---|---|---|
| Domain | Tenant | The boundary that contains all users, groups, and devices |
| Organizational Unit (OU) | Administrative Unit | Groups objects for delegated management |
| Group Policy Object (GPO) | Conditional Access Policy | Enforces rules on users/devices (e.g. require MFA) |
| Domain Controller (DC) | Entra ID (no server) | Authenticates users — AD needs a physical/virtual server, Entra ID is fully cloud-hosted |
| Security Group | Security Group / Microsoft 365 Group | Collections of users for assigning access |
| Kerberos / NTLM | OAuth 2.0 / OpenID Connect | Protocol used to authenticate and issue access tokens |
| Trust relationship | B2B collaboration | Lets two separate directories share access |
| ADUC (Active Directory Users and Computers) | Entra admin center | The console used to manage users, groups, and devices |

---

## Why this matters for IAM/GRC

A control doesn't disappear when infrastructure moves to the cloud — it just gets a new name and a new enforcement point. For example:

- **Least privilege** is enforced with **OU + GPO delegation** on-prem, and with **RBAC + Conditional Access** in Entra ID.
- **Account lifecycle management** (NIST 800-53 AC-2) happens in **ADUC** on-prem, and in the **Entra admin center** or automated provisioning in the cloud.

Being able to map a control across both environments is what hybrid identity work actually requires, since most organizations run both at once during a cloud migration.

## Sources

Microsoft Learn documentation on Active Directory Domain Services and Microsoft Entra ID.
