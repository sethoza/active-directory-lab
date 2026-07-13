# Active Directory & Entra ID IAM Lab

A hands-on identity and access management lab covering both on-prem Active Directory fundamentals and cloud identity in Microsoft Entra ID — built while transitioning into IAM/GRC. Documenting each task: what I did, why it matters, and which security control it satisfies (mapped to NIST CSF 2.0 and NIST 800-53).

**Focus:** identity lifecycle, role-based access, multi-factor authentication, access reviews, and hybrid identity (on-prem AD + cloud Entra ID).

---

## Labs

| # | Lab | What it shows | Status |
|---|-----|---------------|--------|
|—|[Hybrid Identity Bridge](./00-hybrid-identity-bridge.md)| Hybrid identity: how on-prem AD concepts map to Entra ID || Hybrid identity: how on-prem AD concepts map to Entra ID| ✅ Done |
| 01 | Role-Based Access Control (RBAC) | Assigning users to groups and granting least-privilege roles | ✅ Done |
| 02 | Conditional Access + MFA | Requiring multi-factor authentication via a conditional access policy | 🔧 In progress |
| 03 | Joiner–Mover–Leaver (JML) | Full identity lifecycle: onboard, change access, offboard | 🔧 In progress |
| 04 | Access Review / Recertification | Reviewing who has access to what and removing stale access | 🔧 In progress |

---

## Why this repo exists

Most identity work isn't hacking — it's making sure the right people have the right access, and no one keeps access they no longer need. This lab shows the understanding of identity on both sides of a real hybrid environment: the on-prem Active Directory that most established organizations still run, and Microsoft Entra ID, the cloud identity platform most are moving toward. Every action here is translated into audit-ready control language.

## Control mapping 

Every lab below ends with a short table like this:

| Action | NIST CSF 2.0 | NIST 800-53 |
|--------|--------------|-------------|
| Assigned users to role groups | PR.AA-05 (least privilege) | AC-6 |
| Enforced MFA via conditional access | PR.AA-03 (authentication) | IA-2 |
| Onboarded / offboarded a user | PR.AA-01 (identity management) | AC-2 |
| Ran an access review | ID.AM / PR.AA-05 | AC-2(3), AC-6 |

---
## Core Concepts

**Start here** — [Hybrid Identity Bridge](./00-hybrid-identity-bridge.md)  
How on-prem Active Directory concepts map to Entra ID in real hybrid environments. This is the foundation for most enterprise identity work.

## Tools

Active Directory concepts · Microsoft Entra ID (free developer tenant) · NIST CSF 2.0 · NIST 800-53

## About me

[GitHub](https://github.com/sethoza) · LinkedIn: linkedin.com/in/alvin77
