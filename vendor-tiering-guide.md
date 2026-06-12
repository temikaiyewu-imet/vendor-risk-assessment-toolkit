# Vendor Tiering Guide

Use this guide to classify vendors **before** beginning a full assessment. Tier determines assessment depth, reassessment frequency, and monitoring intensity.

---

## Tier definitions

### Tier 1 — Critical
A vendor is Tier 1 if **any one** of the following applies:

- Processes, stores, or transmits sensitive personal data at scale (>1,000 data subjects or sensitive categories)
- Provides infrastructure or services without which core business operations would halt within 24 hours
- Has privileged or persistent access to your organisation's internal systems or networks
- Delivers AI/ML-powered services that directly influence decisions affecting individuals
- Is subject to regulatory oversight in your sector (e.g. licensed financial institution, certified cloud provider under DORA)
- Processes payment card data or financial transactions

**Assessment:** Full checklist (Sections 1–6)  
**Reassessment:** Annually + after any material incident or significant contract change  
**Monitoring:** Continuous or quarterly scorecard review

---

### Tier 2 — Significant
A vendor is Tier 2 if:

- Processes limited personal data in a well-defined, low-volume context
- Provides services that support but do not directly enable core operations
- Has time-limited or scoped access to internal systems (e.g. for a specific project)
- Is a software-as-a-service provider with standard security controls and no special data access

**Assessment:** Sections 1–3 of checklist  
**Reassessment:** Every 18 months or on contract renewal  
**Monitoring:** Annual scorecard or self-assessment questionnaire

---

### Tier 3 — Low Risk
A vendor is Tier 3 if:

- Processes no personal data, or only publicly available information
- Provides commodity services with no system access (e.g. stationery, basic software licences)
- Can be replaced within 48 hours with no operational impact
- No regulatory or reputational exposure associated with this vendor

**Assessment:** Section 1 (Initial Screening) only  
**Reassessment:** On contract renewal or every 2–3 years  
**Monitoring:** No active monitoring required

---

## Tiering decision flowchart

```
Does the vendor access, process, or store personal data at scale?
├── Yes → Tier 1
└── No ↓

Would failure of this vendor halt core operations within 24 hours?
├── Yes → Tier 1
└── No ↓

Does the vendor have persistent or privileged system access?
├── Yes → Tier 1
└── No ↓

Does the vendor process any personal data, or provide significant operational support?
├── Yes → Tier 2
└── No → Tier 3
```

---

## Notes

- Tier classification should be reviewed at each reassessment — a vendor's footprint can expand over time
- When in doubt between Tier 1 and Tier 2, default to Tier 1
- Regulatory requirements (e.g. FCA outsourcing rules, DORA, CBN guidelines) may impose minimum assessment standards regardless of internal tier classification
- New vendors should be tiered before any contract is signed, not after onboarding
