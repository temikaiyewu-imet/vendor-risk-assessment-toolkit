# Vendor Risk Assessment Checklist

**Version:** 1.0  
**Framework alignment:** ISO 27001 · NIST CSF · SOC 2 · ISO 42001 · GDPR/NDPR  
**Use with:** [vendor-tiering-guide.md](vendor-tiering-guide.md) to determine which sections apply

---

## Assessment information

| Field | Detail |
|---|---|
| Vendor name | |
| Assessment date | |
| Assessor name | |
| Vendor tier (1 / 2 / 3) | |
| Vendor contact | |
| Services / products provided | |
| Contract start date | |
| Next review date | |

---

## Section 1 — Initial Screening
*Apply to ALL vendors regardless of tier*

### 1.1 Vendor profile
- [ ] Vendor has been in operation for more than 2 years
- [ ] Vendor has a clearly documented business registration / legal entity
- [ ] No active regulatory sanctions, fines, or enforcement actions in the last 3 years
- [ ] Vendor financial stability confirmed (publicly available accounts or self-declaration)
- [ ] Vendor has a named point of contact for security and compliance queries
- [ ] Vendor has a published privacy policy aligned with applicable law (GDPR, NDPR, etc.)

### 1.2 Data handling
- [ ] Confirmed what categories of data the vendor will access, process, or store
- [ ] Confirmed whether vendor will access personal data (if yes, DPA required)
- [ ] Data residency confirmed — where is data stored geographically?
- [ ] Vendor has a documented data retention and deletion policy
- [ ] Vendor will not use your organisation's data to train third-party AI models without consent

### 1.3 Contractual baseline
- [ ] Data Processing Agreement (DPA) in place (if personal data is involved)
- [ ] Right to audit clause included in contract
- [ ] Incident notification clause — vendor must notify within agreed SLA (typically 24–72 hrs)
- [ ] Sub-processor / fourth-party list disclosed and agreed
- [ ] Exit and data return/deletion obligations documented

---

## Section 2 — Information Security Controls
*Apply to Tier 1 and Tier 2 vendors*

### 2.1 Certifications and attestations
- [ ] ISO 27001 certification — valid and in scope for the services provided
- [ ] SOC 2 Type II report available and reviewed — issued within last 12 months
- [ ] PCI DSS compliance confirmed (if vendor handles payment data)
- [ ] Penetration testing conducted within last 12 months — summary or attestation available
- [ ] Vulnerability management programme documented

### 2.2 Access control
- [ ] Multi-factor authentication (MFA) enforced for all staff accessing your organisation's data or systems
- [ ] Principle of least privilege applied — vendor staff access is scoped to what is strictly necessary
- [ ] Privileged access management (PAM) controls documented
- [ ] Joiners/movers/leavers process confirmed — access is revoked within 24 hours of staff departure
- [ ] Remote access via VPN or equivalent secure method only

### 2.3 Encryption
- [ ] Data encrypted at rest (AES-256 or equivalent minimum standard)
- [ ] Data encrypted in transit (TLS 1.2 minimum; TLS 1.3 preferred)
- [ ] Encryption key management policy documented — keys not held by vendor alone if possible

### 2.4 Incident response
- [ ] Vendor has a documented incident response plan (IRP)
- [ ] Vendor has experienced a significant security incident in the last 3 years — if yes, reviewed their response and remediation
- [ ] Vendor can demonstrate incident response test / tabletop exercise conducted in last 12 months
- [ ] Clear escalation path defined for incidents affecting your organisation's data

### 2.5 Business continuity and resilience
- [ ] Business Continuity Plan (BCP) documented and tested within last 12 months
- [ ] Disaster Recovery Plan (DRP) documented — RPO and RTO defined
- [ ] Uptime SLA agreed and monitored — minimum 99.5% for Tier 1 services
- [ ] Geographic redundancy confirmed for critical services

---

## Section 3 — Privacy and Data Protection
*Apply to Tier 1 and Tier 2 vendors where personal data is involved*

### 3.1 Privacy governance
- [ ] Vendor has a designated Data Protection Officer (DPO) or equivalent
- [ ] Privacy impact assessments (PIAs / DPIAs) conducted for high-risk processing activities
- [ ] Records of Processing Activities (ROPA) maintained by vendor
- [ ] Vendor staff receive regular data protection training

### 3.2 Data subject rights
- [ ] Vendor can support data subject access requests (DSARs) within regulatory timelines
- [ ] Vendor can support right to erasure requests — confirmed deletion process
- [ ] Vendor can support data portability where applicable

### 3.3 Cross-border data transfers
- [ ] If data transferred outside EEA or Nigeria — legal basis confirmed (adequacy decision, SCCs, BCRs)
- [ ] Transfer impact assessment (TIA) completed if required
- [ ] Sub-processors in third countries identified and assessed

---

## Section 4 — AI and Algorithmic Risk
*Apply to Tier 1 vendors where AI/ML systems are used in the delivery of services*

*Framework reference: ISO 42001 AI Management System*

### 4.1 AI system transparency
- [ ] Vendor has disclosed which AI/ML systems are used in the services provided to your organisation
- [ ] Purpose and intended use of each AI system documented
- [ ] Human oversight mechanisms in place for AI-assisted decisions that affect individuals
- [ ] Vendor has an AI governance policy or AI management system (ISO 42001 or equivalent)

### 4.2 Bias and fairness
- [ ] Bias testing conducted on AI systems — methodology documented
- [ ] Bias testing covers protected characteristics relevant to the use case
- [ ] Bias testing is recurring — not a one-time pre-launch activity
- [ ] Process for flagging and remediating bias incidents defined

### 4.3 Data used for AI training
- [ ] Vendor confirmed whether your organisation's data is used to train or fine-tune AI models
- [ ] Opt-out from AI training available and exercised if required
- [ ] Third-party training data sources disclosed — licensing and provenance confirmed

### 4.4 AI incident and risk management
- [ ] Vendor has a process for managing AI-specific incidents (model failure, hallucination, adversarial attack)
- [ ] AI risk register maintained by vendor — available for review on request
- [ ] Material changes to AI systems (new models, retraining) trigger a notification to your organisation

---

## Section 5 — Operational and Concentration Risk
*Apply to Tier 1 vendors*

### 5.1 Concentration risk
- [ ] Vendor dependency mapped — assessed whether failure of this vendor would disrupt critical operations
- [ ] Alternative vendor or fallback plan documented
- [ ] Vendor is not sole provider of a critical service without a tested contingency

### 5.2 Sub-processors and fourth parties
- [ ] Full list of sub-processors disclosed
- [ ] Key sub-processors assessed — particularly cloud infrastructure providers (AWS, Azure, GCP)
- [ ] Vendor contractually flows down security requirements to their sub-processors
- [ ] Notification process agreed for changes to sub-processor list

### 5.3 Geopolitical and jurisdiction risk
- [ ] Vendor jurisdiction identified — assessed whether legal or political risk affects service delivery
- [ ] Key personnel or infrastructure not concentrated in a single high-risk jurisdiction
- [ ] Export control and sanctions compliance confirmed

---

## Section 6 — Ongoing Monitoring
*Apply to Tier 1 and Tier 2 vendors post-onboarding*

- [ ] Vendor added to risk register with tier, owner, and next review date
- [ ] Annual (Tier 1) or 18-monthly (Tier 2) reassessment scheduled
- [ ] Vendor security alerts / threat intelligence monitoring set up (e.g. via UpGuard, SecurityScorecard, or manual review)
- [ ] Key contractual dates logged — renewal, audit rights, notice periods
- [ ] Escalation path documented — who owns this vendor relationship internally?

---

## Assessment outcome

| Field | Detail |
|---|---|
| Overall risk rating | ☐ Low  ☐ Medium  ☐ High  ☐ Critical |
| Recommended action | ☐ Approve  ☐ Approve with conditions  ☐ Defer pending remediation  ☐ Reject |
| Conditions / open items | |
| Assessor sign-off | |
| Date | |
| Next review date | |

---

*For scoring methodology, see [vendor-risk-scoring-matrix.md](vendor-risk-scoring-matrix.md)*  
*For register logging, see [vendor-risk-register-template.md](vendor-risk-register-template.md)*
