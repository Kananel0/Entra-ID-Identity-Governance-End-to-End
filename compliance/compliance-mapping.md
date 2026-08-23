# Compliance Mapping — Entra ID Identity Governance Practice Lab (SC-300)

**Classification:** Internal Use - Certification Practice Lab
**Owner:** IAM Engineering (Self-Directed Certification Practice)

## SC-300 Exam Domain Coverage

| SC-300 Domain | What This Lab Builds |
|---|---|
| Implement identities and access | Dynamic groups, attribute-based membership, user lifecycle (Part 1) |
| Implement authentication and access management | Conditional Access baseline policies, Identity Protection risk policies (Parts 2-3) |
| Implement access management for apps | App registration, app roles, delegated permissions, admin consent (Part 4) |
| Plan and implement identity governance | Entitlement management access packages, access reviews, PIM for Groups (Parts 5-7) |

## Underlying ISO 27001 Control Objectives

The controls configured in this lab are real, not simplified for demonstration — the same Conditional Access, entitlement management, and PIM patterns map directly to these Annex A controls when deployed in a production tenant.

| Requirement | Description |
|---|---|
| ISO 27001 A.9.2 | User access provisioning and de-provisioning |
| ISO 27001 A.9.4 | System and application access control |
| ISO 27001 A.9.2.5 | Review of user access rights |

## Implementation Narrative

- Established an identity foundation: test users, department attributes, and a dynamically-membered security group driven by attribute rules rather than manual assignment.
- Layered access control policies: baseline Conditional Access (MFA, legacy auth blocking, device compliance for admins) plus Identity Protection risk-based policies for user risk and sign-in risk.
- Governed application access: registered a test application, defined app roles, assigned them to users, and walked the delegated-permission admin-consent flow.
- Implemented continuous governance: an entitlement management access package with approval and expiry, a recurring access review with auto-apply, and Privileged Identity Management scoped to group membership rather than directory roles.

## Control Testing Procedure

1. Confirm each Conditional Access policy's current state (Report-only vs. On) and review its Insights and reporting data before any state change.
2. Attempt to request the entitlement management access package as a non-approver test user and confirm the approval step is enforced before access is granted.
3. Confirm PIM for Groups activation requires justification, approval, and expires automatically at the configured duration.

## Evidence Artifacts

- Conditional Access policy configuration exports (Parts 2)
- Identity Protection risk policy configuration and any risk detections captured (Part 3)
- Access package request/approval trail and access review results (Parts 5-6)
- PIM for Groups activation audit history (Part 7)

## Risk Assessment

**Gap before this lab:** Exam-only preparation without hands-on configuration risks a gap between passing a certification and being operationally ready to administer these controls in a live tenant - particularly for judgment-heavy areas like Conditional Access exclusions, risk policy thresholds, and access review auto-apply settings.

**Residual gap after completion:** Low. All four SC-300 governance domains have been configured, tested, and evidenced hands-on in a live (trial-licensed) tenant, not simulated. Residual gap is limited to scale-specific operational experience (e.g., managing thousands of users) that a personal lab cannot replicate.

---

[⬅ Back to project README](../README.md)
