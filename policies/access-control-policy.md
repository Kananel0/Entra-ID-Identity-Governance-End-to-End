# Lab Governance Charter — Entra ID Identity Governance Practice Lab (SC-300)

**Classification:** Internal Use - Certification Practice Lab
**Owner:** IAM Engineering (Self-Directed Certification Practice)
**Effective Date:** 2026-08-22
**Version:** 1.0

## 1. Purpose

This charter establishes the configuration discipline followed while building this practice lab, so that every control deployed reflects real operational practice rather than exam-only shortcuts.

## 2. Scope

Applies to all Entra ID configuration performed within this lab tenant: Entra ID, Entra ID (Privileged Identity Management), Entra ID Governance (Entitlement Management, Access Reviews).

## 3. Governance Statements

1. All Conditional Access policies shall be deployed in Report-only mode initially and reviewed via Insights and reporting before enforcement is enabled.
2. Group membership for governed resources shall be dynamic and attribute-driven wherever practical, rather than manually assigned.
3. Application permissions requiring admin consent shall be reviewed against the principle of least privilege before consent is granted.
4. All access granted through entitlement management shall have a defined expiry and a linked access review; indefinite access package assignments are prohibited.
5. Privileged group membership shall be governed through PIM for Groups with mandatory justification and approval, consistent with the standard applied to directory role elevation.

## 4. Roles & Responsibilities

| Role | Responsibility |
|---|---|
| IAM Engineering (Self-Directed Certification Practice) | Owns the lab tenant, performs all configuration, and is accountable for evidence capture. |
| Approver persona (test user) | Plays the role of manager/approver for entitlement management and PIM activation requests, to validate the approval workflow end-to-end. |

## 5. Exceptions

Any deviation from standard deployment practice (e.g., skipping Report-only mode for a Conditional Access policy) shall be noted explicitly in this lab's documentation rather than silently omitted, so the lab remains an honest reference for future review.

## 6. Related Standards

- ISO 27001 A.9.2 - User access provisioning and de-provisioning
- ISO 27001 A.9.4 - System and application access control
- ISO 27001 A.9.2.5 - Review of user access rights

## 7. Document Control

| Version | Date | Author | Change Summary |
|---|---|---|---|
| 1.0 | 2026-08-22 | IAM Engineering (Self-Directed Certification Practice) | Initial version. |

---

[⬅ Back to project README](../README.md)
