# Vendor Risk Scoring Matrix

Use this after completing the assessment checklist to calculate a risk rating for the vendor.

---

## Step 1 — Inherent risk score

Inherent risk = the risk **before** any controls are considered.

Score each factor from 1–5 using the table below, then sum.

| Risk Factor | 1 (Very Low) | 3 (Medium) | 5 (Very High) | Your Score |
|---|---|---|---|---|
| **Data sensitivity** | No personal data | Limited personal data | Sensitive/special category data | |
| **Data volume** | <100 records | 1,000–10,000 records | >100,000 records | |
| **System access** | No system access | Read-only / scoped access | Privileged / persistent access | |
| **Operational dependency** | Easily replaceable | Some dependency | Business-critical, no alternative | |
| **Geographic risk** | Low-risk jurisdiction | Mixed | High-risk or sanctions-adjacent jurisdiction | |
| **AI/algorithmic involvement** | No AI used | AI used internally only | AI influences decisions on individuals | |
| **Sub-processor exposure** | No sub-processors | 1–3 known sub-processors | Many sub-processors, limited visibility | |

**Inherent risk total: ___ / 35**

| Total Score | Inherent Risk Rating |
|---|---|
| 7–14 | Low |
| 15–21 | Medium |
| 22–28 | High |
| 29–35 | Critical |

---

## Step 2 — Control effectiveness score

Control effectiveness = how well the vendor's existing controls mitigate the inherent risk.

Score each control area from 1–5. Higher score = stronger controls.

| Control Area | 1 (None / Weak) | 3 (Partial) | 5 (Strong / Certified) | Your Score |
|---|---|---|---|---|
| **Security certification** | No certification | Self-assessment only | ISO 27001 / SOC 2 Type II valid | |
| **Access controls** | No MFA, broad access | MFA in some areas | MFA + PAM + least privilege enforced | |
| **Incident response** | No documented IRP | IRP exists, untested | IRP documented, tested, notified us within SLA | |
| **Data protection** | No DPA, no DPO | DPA in place | DPA + DPO + DPIA process documented | |
| **Business continuity** | No BCP/DRP | BCP exists, untested | BCP + DRP tested, RTO/RPO defined | |
| **AI governance** (if applicable) | No AI governance | Ad hoc oversight | ISO 42001 or equivalent, bias testing documented | |
| **Contract protections** | No audit rights, no notification SLA | Some protections | Right to audit + notification SLA + sub-processor list | |

**Control effectiveness total: ___ / 35**

| Total Score | Control Effectiveness |
|---|---|
| 7–14 | Weak |
| 15–21 | Moderate |
| 22–28 | Strong |
| 29–35 | Very Strong |

---

## Step 3 — Residual risk rating

Residual risk = inherent risk adjusted for control effectiveness.

Use the matrix below:

| | Controls: Weak | Controls: Moderate | Controls: Strong | Controls: Very Strong |
|---|---|---|---|---|
| **Inherent: Low** | Medium | Low | Low | Low |
| **Inherent: Medium** | High | Medium | Low | Low |
| **Inherent: High** | Critical | High | Medium | Low |
| **Inherent: Critical** | Critical | Critical | High | Medium |

**Residual risk rating: ___________**

---

## Step 4 — Recommended action

| Residual Risk | Recommended Action |
|---|---|
| Low | Approve. Standard monitoring. |
| Medium | Approve with documented conditions. Address gaps within 90 days. |
| High | Defer onboarding pending remediation of critical gaps. Re-assess before go-live. |
| Critical | Escalate to senior risk owner. Consider rejecting vendor or requiring independent audit before proceeding. |

---

*This scoring model is qualitative. Calibrate thresholds to your organisation's risk appetite and regulatory context.*
