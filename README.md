# Risk Management

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/license-CC0--1.0-lightgrey.svg)](LICENSE)

A curated, practitioner-oriented guide to **enterprise and operational risk management** — how to run gap analysis, qualitative and quantitative risk analysis, heat maps, RACI matrices, a risk register, compensating controls, continuous monitoring, and a periodic review cadence, with starting templates for each. Written for someone building or running a risk programme for the first time, not just someone who already knows the vocabulary.

**Scope:** the risk-management *method* — how to identify, analyse, score, treat, document, and monitor risk — plus the standards (ISO 31000, COSO ERM, NIST SP 800-30/39, FAIR) that formalise it. Framework-specific control catalogues (NIST CSF, ISO 27001, PCI-DSS, CIS Controls) are covered by the companion [Security Frameworks](https://github.com/garynair/security-frameworks) list; sector-specific regulatory risk obligations (GLBA, NYDFS 500, HIPAA, FedRAMP) are covered by the companion sector lists (see Related Lists). This list is the general-purpose method those sector programmes are built on top of.

**Why this list exists:** most risk-management material is either a 300-page ISO standard behind a paywall or a single blog post about "risk matrices." This list sits in between: enough method to actually run a review cycle, with a template to start from rather than a blank page.

Contributions welcome.

---

## Contents

- [Why Risk Management Matters](#why-risk-management-matters)
- [How to Approach a Risk Programme](#how-to-approach-a-risk-programme)
- [Foundational Standards (ISO 31000, COSO ERM, NIST SP 800-30/39)](#foundational-standards-iso-31000-coso-erm-nist-sp-800-3039)
- [Risk Appetite and Risk Tolerance](#risk-appetite-and-risk-tolerance)
- [Risk Taxonomy and Governance (Three Lines of Defense)](#risk-taxonomy-and-governance-three-lines-of-defense)
- [Risk Identification](#risk-identification)
- [Gap Analysis](#gap-analysis)
- [Qualitative Risk Analysis](#qualitative-risk-analysis)
- [Quantitative Risk Analysis (FAIR and ALE)](#quantitative-risk-analysis-fair-and-ale)
- [Risk Heat Maps](#risk-heat-maps)
- [RACI Matrix](#raci-matrix)
- [Risk Register](#risk-register)
- [Risk Treatment and Compensating Controls](#risk-treatment-and-compensating-controls)
- [Key Risk Indicators and Continuous Monitoring](#key-risk-indicators-and-continuous-monitoring)
- [Risk Reporting and Board Governance](#risk-reporting-and-board-governance)
- [Periodic Review Cadence](#periodic-review-cadence)
- [Third-Party and Vendor Risk Management](#third-party-and-vendor-risk-management)
- [Risk Management Policy](#risk-management-policy)
- [Templates in This Repo](#templates-in-this-repo)
- [Cross-Framework Mapping and GRC Platforms](#cross-framework-mapping-and-grc-platforms)
- [Certifications and Training](#certifications-and-training)
- [Government and Standards Bodies](#government-and-standards-bodies)
- [Learning Resources](#learning-resources)
- [Related Lists](#related-lists)

---

## Why Risk Management Matters

Every control framework in the companion lists — NIST CSF, ISO 27001, FedRAMP, HIPAA — eventually asks the same question a different way: "what could go wrong, how bad would it be, and what are you doing about it?" Risk management is the discipline that answers that question systematically instead of reactively. Without it, a security or compliance programme either treats every finding as equally urgent (wasting scarce remediation capacity) or quietly ignores gaps until an auditor or an incident forces the issue.

A mature programme does five things a checklist-driven one does not: it distinguishes risks from issues (a risk is potential, an issue has already happened), it scores likelihood and impact consistently enough that a heat map means the same thing across two different business units, it names a single accountable owner for every open item, it tracks compensating controls with the same rigour as primary ones, and it reviews on a cadence rather than only when something breaks.

---

## How to Approach a Risk Programme

1. **Adopt a framework before you build anything.** Pick ISO 31000 (process-focused, framework-agnostic) or COSO ERM (governance- and strategy-focused) as your organising structure. Do not invent your own taxonomy from scratch — it will not survive contact with an auditor or a new hire.
2. **Set risk appetite and tolerance first.** You cannot score a risk as "acceptable" or "unacceptable" without a stated threshold. This is a leadership decision, not a risk-team decision — escalate it rather than assuming it.
3. **Build your taxonomy and governance structure.** Decide how risk is categorised (strategic, operational, financial, compliance, cyber, third-party) and who owns what under a three-lines-of-defense model before you open a single register entry.
4. **Identify risks.** Run workshops, interviews, control self-assessments, and gap analyses against your control baseline (see Gap Analysis below) to build the initial inventory.
5. **Analyse each risk, both ways.** Score likelihood and impact qualitatively (heat map placement) and, for anything material, quantitatively (FAIR or ALE) so a dollar figure backs the ranking, not just a colour.
6. **Decide treatment.** For each risk: Treat (mitigate), Transfer (insurance, contract), Tolerate (accept), or Terminate (stop the activity). Document the decision and its owner in the risk register.
7. **Document compensating controls wherever a primary control cannot be implemented.** A compensating control needs the same rigour as the control it replaces: what it does, why it's equivalent, who approved the exception, and when it expires.
8. **Stand up continuous monitoring.** Define KRIs with thresholds, not just KPIs — a KRI should trigger a review before the risk becomes an issue, not after.
9. **Report on a cadence.** Different audiences need different frequencies — see Periodic Review Cadence below for what belongs at each interval.
10. **Review and reassess continuously.** A risk register that is not touched between annual audits is a compliance artefact, not a risk-management programme.

---

## Foundational Standards (ISO 31000, COSO ERM, NIST SP 800-30/39)

**Path to adoption:** all three are voluntary and non-certifiable (ISO 31000 has no certification scheme by design). Most organisations pick one as their primary methodology and use the others as reference for specific techniques (NIST SP 800-30 for a detailed qualitative/quantitative scoring method, for example).

- [ISO 31000:2018 — Risk Management Guidelines](https://www.iso.org/iso-31000-risk-management.html) - The internationally recognised, framework-agnostic risk management standard: principles, a generic framework, and a process (identify, analyse, evaluate, treat, monitor, communicate). Not certifiable and not sector-specific — designed to sit underneath any other framework.
- [ISO 31010:2019 — Risk Assessment Techniques](https://www.iso.org/standard/72140.html) - The companion standard cataloguing over 40 named risk-assessment techniques (SWIFT, bow-tie analysis, FMEA, Monte Carlo, and more), each with guidance on when it applies.
- [COSO Enterprise Risk Management — Integrating with Strategy and Performance](https://www.coso.org/guidance-erm) - COSO's 2017 ERM framework, organised around five components (Governance and Culture, Strategy and Objective-Setting, Performance, Review and Revision, Information/Communication/Reporting) and closely tied to board-level strategy, distinct from COSO's separate Internal Control–Integrated Framework used for ITGC/SOX work.
- [NIST SP 800-30 Revision 1](https://csrc.nist.gov/pubs/sp/800/30/r1/final) - "Guide for Conducting Risk Assessments," NIST's detailed methodology for identifying threat sources, vulnerabilities, likelihood, and impact, with worked qualitative and semi-quantitative scoring tables — one of the most practical, free starting points for building your own scoring methodology.
- [NIST SP 800-39](https://csrc.nist.gov/pubs/sp/800/39/final) - "Managing Information Security Risk," the tier-based (Organization, Mission/Business Process, Information System) risk-management process NIST SP 800-30's assessments feed into.

---

## Risk Appetite and Risk Tolerance

**What it is:** risk appetite is the amount and type of risk an organisation is willing to pursue in service of its objectives, set by the board or senior leadership; risk tolerance is the acceptable variation around that appetite for a specific risk or metric — the trigger point at which a KRI breach demands action. Every heat map threshold and every "accept vs. treat" decision in the risk register should trace back to a documented appetite statement, not an individual analyst's judgement call.

**How to build it:**
1. Draft appetite statements per risk category (financial, operational, compliance, cyber, reputational), not one blanket statement — a bank's appetite for credit risk and its appetite for cyber risk are not the same conversation.
2. Express each statement in a way that is testable: "we will not accept single points of failure in payment processing" is testable; "we take security seriously" is not.
3. Set quantitative tolerance thresholds under each qualitative statement wherever possible (e.g., maximum acceptable downtime, maximum unencrypted-data exposure count) so KRIs have something concrete to measure against.
4. Get board or executive sign-off and a review date — appetite statements should be revisited at least annually or after a material change in strategy, M&A activity, or a significant incident.
5. Map appetite to your heat map's accept/escalate line (see Risk Heat Maps) so the two artefacts stay consistent with each other.

- [COSO Risk Appetite — Critical to Success](https://www.coso.org/guidance-erm) - COSO's guidance thought paper on defining and operationalising risk appetite as part of the broader ERM framework.
- [ISO 31000 Risk Criteria Guidance](https://www.iso.org/iso-31000-risk-management.html) - ISO 31000's treatment of "risk criteria" — the reference terms an organisation uses to evaluate risk significance, the standard's equivalent concept to appetite and tolerance.

---

## Risk Taxonomy and Governance (Three Lines of Defense)

**What it is:** a risk taxonomy is a consistent categorisation scheme (strategic, operational, financial, compliance/legal, cyber/technology, third-party) so risks identified in different business units can be aggregated and compared. The Three Lines model defines who owns risk at each layer: the first line (business/operational management) owns and manages risk day-to-day; the second line (risk management and compliance functions) sets policy, provides oversight, and challenges the first line; the third line (internal audit) provides independent assurance to the board that the first two lines are actually working.

**How to build it:**
1. Adopt a taxonomy with no more than 6–8 top-level categories — more than that and aggregation across business units breaks down.
2. Assign every risk in your register a single primary category (secondary tags are fine, but ranking and reporting should run off the primary one).
3. Map your existing organisational functions onto the three lines explicitly — most disputes about "who owns this risk" trace back to an undocumented or contested Three Lines mapping, not a genuine ambiguity in the risk itself.
4. Give the second line (risk/compliance) veto or escalation authority over first-line risk acceptances above a defined threshold, so risk acceptance can't happen silently at the business-unit level.
5. Keep internal audit (third line) independent of both — it should never own remediation of the findings it reports on.

- [IIA Three Lines Model (2020)](https://www.theiia.org/en/content/position-papers/2020/the-iias-three-lines-model-an-update-of-the-three-lines-of-defense/) - The Institute of Internal Auditors' current model (updated from the original "Three Lines of Defense"), defining roles, accountabilities, and the relationship between management, risk functions, and internal audit.
- [COSO ERM — Governance and Culture Component](https://www.coso.org/guidance-erm) - COSO's treatment of the governance structures and organisational culture that make a Three Lines model actually function rather than exist only on paper.

---

## Risk Identification

**How to do it:**
1. Run structured workshops with business-unit owners, not just the risk/security team in a room by itself — the people running a process see risks a control catalogue won't.
2. Use control self-assessments (CSAs) to have first-line owners self-report control effectiveness on a schedule, cross-checked periodically by the second line.
3. Treat every audit finding, incident post-mortem, penetration test result, and vendor assessment as a risk-identification input, not a one-off item to close and forget.
4. Run threat modelling for technical/cyber risk specifically — it surfaces risks a generic workshop will miss. STRIDE (Microsoft's mnemonic — Spoofing, Tampering, Repudiation, Information disclosure, Denial of service, Elevation of privilege) is the most widely used starting method: walk an architecture diagram component by component and ask where each of the six threat types could occur. Attack trees are a complementary technique for a single high-value target, decomposing "how could an attacker achieve X" into a tree of specific paths.
5. Log near-misses and issues (realised risks) as identification triggers for related, not-yet-realised risks elsewhere in the same process.
6. Use root cause analysis — the 5 Whys or a fishbone/Ishikawa diagram — on every material finding so the register captures the underlying cause, not just the symptom a control test happened to catch.

- [5 Whys (ASQ)](https://asq.org/quality-resources/five-whys) - The American Society for Quality's explanation of the iterative "why" technique for tracing a symptom back to its root cause.
- [Fishbone (Ishikawa) Diagram (ASQ)](https://asq.org/quality-resources/fishbone) - ASQ's guide to the cause-and-effect diagram technique, useful when a risk has multiple contributing causes rather than one linear chain.
- [Microsoft Threat Modeling (STRIDE)](https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool-threats) - Microsoft's own reference for the STRIDE mnemonic and its Threat Modeling Tool, the most widely adopted starting method for structured, diagram-driven cyber threat identification.
- [MITRE ATT&CK](https://attack.mitre.org/) - The most widely used threat-behaviour knowledge base for identifying and modelling cyber-specific risk scenarios grounded in observed adversary techniques.

---

## Gap Analysis

**What it is:** a structured comparison between your current control state and a target baseline (a framework, a regulation, or your own policy), producing a list of specific, actionable gaps rather than a general sense that "things could be better."

**How to do it:**
1. Pick the target baseline explicitly (NIST CSF, ISO 27001 Annex A, NIST SP 800-53, your own internal policy) — a gap analysis without a named baseline is just an opinion.
2. Score each requirement on a consistent maturity scale (see the CMMI-style example below) rather than a binary met/not-met, so partial implementation is visible.
3. For every gap, capture: the requirement, current state, target state, the size of the gap, root cause, proposed remediation, owner, and target date — this is exactly the structure of a POA&M (see the companion [Federal Compliance](https://github.com/garynair/federal-compliance) list for the POA&M-specific version of this).
4. Feed every open gap into the risk register as its own risk entry, scored for likelihood and impact like anything else — a gap that never becomes a risk-register entry tends to never get funded.
5. Re-run the gap analysis on a cadence (see Periodic Review Cadence), not just once at programme kickoff.

A common five-level maturity scale for scoring each requirement:

| Level | Name | Description |
|---|---|---|
| 0 | Not Implemented | No process or control exists. |
| 1 | Ad Hoc | Performed inconsistently, undocumented, dependent on an individual. |
| 2 | Repeatable | Performed consistently but not formally documented or standardised. |
| 3 | Defined | Documented, standardised, and communicated across the organisation. |
| 4 | Managed | Measured and monitored with defined metrics and periodic review. |
| 5 | Optimising | Continuously improved based on metrics and changing risk. |

See [`templates/gap-analysis-template.csv`](templates/gap-analysis-template.csv) in this repo for a ready-to-use tracker built on this structure.

- [CMMI Institute — Capability Maturity Model Integration](https://cmmiinstitute.com/) - The origin of the five-level maturity scale widely adapted (as above) for control gap-analysis scoring outside its original software-process-improvement context.
- [NIST SP 800-53A Revision 5](https://csrc.nist.gov/pubs/sp/800/53/a/r5/final) - NIST's assessment-procedures publication, useful as a source of specific, testable assessment objectives when scoring an SP 800-53-based gap analysis.

---

## Qualitative Risk Analysis

**What it is:** scoring likelihood and impact using descriptive scales (e.g., Low/Medium/High or a 1–5 scale) rather than dollar figures — faster to run and easier to apply consistently across risk types that resist precise quantification (reputational risk, for example), at the cost of precision and comparability across risks of very different scale.

**Popular techniques:**
- **Likelihood × Impact matrix** — the standard 5×5 (or 3×3) grid; the basis for the heat map below.
- **Delphi technique** — anonymous, iterative expert polling used to reach a likelihood/impact consensus without groupthink or seniority bias distorting the estimate.
- **SWIFT (Structured What-If Technique)** — a facilitated workshop method using "what if" prompts against a process flow, lighter-weight than a full FMEA.
- **FMEA (Failure Mode and Effects Analysis)** — scores each potential failure mode on severity, occurrence, and detection, multiplied into a Risk Priority Number (RPN); widely used in operational and product risk.
- **Bow-tie analysis** — visually connects causes (left side) through a central risk event to consequences (right side), with preventive controls on the left and mitigating controls on the right — one of the clearest ways to show where a compensating control actually sits.
- **Scenario analysis** — narrative "what would happen if" walkthroughs for specific, high-impact scenarios (a ransomware event, a key-vendor failure), often used to pressure-test whether the current control set actually holds up.

**How to do it well:**
1. Define your scale's anchors in writing before scoring anything — "High likelihood" needs a stated frequency (e.g., "expected more than once per year") or every scorer will calibrate differently.
2. Score likelihood and impact separately, then combine — don't let a scorer jump straight to "this feels like a 4."
3. Score inherent risk (before controls) and residual risk (after controls) separately, and keep both in the register — inherent risk tells you what's at stake; residual risk tells you what's still open.
4. Use at least two scorers for anything landing in the top band, to reduce single-rater bias.

- [ISO 31010:2019 — Risk Assessment Techniques](https://www.iso.org/standard/72140.html) - The authoritative catalogue covering SWIFT, FMEA, bow-tie, Delphi, and dozens of other qualitative and semi-quantitative techniques, each with applicability guidance.
- [NIST SP 800-30 Revision 1](https://csrc.nist.gov/pubs/sp/800/30/r1/final) - Includes fully worked qualitative likelihood and impact scoring tables (Appendix G and H) that can be adopted directly or adapted.

---

## Quantitative Risk Analysis (FAIR and ALE)

**What it is:** expressing risk in financial terms (expected loss in dollars over a defined period) instead of a qualitative band — harder to do credibly, but it lets you compare a cyber risk directly against a market risk or an operational risk on the same axis, and it justifies a control investment in terms a CFO evaluates every other capital request in.

**Popular techniques:**
- **FAIR (Factor Analysis of Information Risk)** — the leading quantitative model for cyber and operational risk, decomposing risk into Loss Event Frequency and Loss Magnitude, each broken into further measurable factors (Threat Event Frequency, Vulnerability, Primary and Secondary Loss).
- **ALE (Annualized Loss Expectancy)** — the classic formula: `ALE = SLE × ARO`, where SLE (Single Loss Expectancy) is the cost of one occurrence and ARO (Annualized Rate of Occurrence) is its expected frequency per year. Simpler than FAIR, and a reasonable starting point before adopting a full FAIR practice.
- **Monte Carlo simulation** — runs thousands of randomised scenarios across a range of inputs (rather than single-point estimates) to produce a loss-exceedance curve, showing the probability of loss exceeding any given dollar amount. FAIR analyses are commonly run this way rather than with single-point averages.
- **Value at Risk (VaR)** — borrowed from financial risk management, expressing the maximum expected loss at a given confidence level over a set time horizon; increasingly applied to cyber risk as "Cyber VaR."

**How to do it well:**
1. Reserve full FAIR/Monte Carlo analysis for your highest-ranked qualitative risks — it is not worth the analyst time for a risk you would tolerate regardless of the exact dollar figure.
2. Use ranges, not point estimates, for every input (minimum, most likely, maximum) and propagate that uncertainty through rather than presenting a single number as if it were precise.
3. Validate loss-magnitude inputs against actual internal loss data or industry loss data (e.g., breach cost reports) wherever available, rather than relying purely on expert judgement.
4. Present results as a range or a loss-exceedance curve to leadership, not a single figure — "there's a 10% chance annual loss exceeds $4M" is more honest and more useful than "expected loss is $1.2M."
5. Re-run the analysis when a material control changes, not just annually — quantitative models decay faster than qualitative ones because they're more sensitive to specific inputs.

- [FAIR Institute](https://www.fairinstitute.org/) - The nonprofit professional organisation maintaining the FAIR standard, publishing the FAIR model documentation, training, and a large practitioner community.
- [Open FAIR Body of Knowledge (The Open Group)](https://www.opengroup.org/certifications/openfair) - The Open Group's formal, standardised version of FAIR (O-RA and O-RT standards), including the certification path referenced under Certifications and Training below.
- [FAIR-U](https://www.fairinstitute.org/fair-u) - The FAIR Institute's free, browser-based tool for learning and running basic FAIR risk quantification without a commercial licence.
- [NIST SP 800-30 Revision 1, Appendix I](https://csrc.nist.gov/pubs/sp/800/30/r1/final) - Includes NIST's semi-quantitative scoring guidance as a bridge between purely qualitative scoring and a full FAIR-style quantitative model.

---

## Risk Heat Maps

**What it is:** a visual grid (typically 5×5) plotting likelihood on one axis and impact on the other, with each cell colour-coded (green/yellow/orange/red) to show risk severity at a glance — the single most common artefact used to communicate risk posture to people who will never read the underlying register.

**How to build one:**
1. Use the same likelihood and impact scales you defined for qualitative analysis — a heat map is a visualisation of that scoring, not a separate exercise.
2. Fix your colour bands to your risk appetite thresholds (see Risk Appetite above), not to an arbitrary even split of the grid — the line between "yellow" and "red" should be the line at which a risk needs escalation.
3. Plot both inherent and residual risk for your top risks, either as two separate maps or as a "before → after" arrow on one map, so the value of existing controls is visible.
4. Label each plotted point with a risk ID that ties back to the register — a heat map with unlabelled dots is decoration, not a management tool.
5. Regenerate it every review cycle, not just for the annual board deck — a heat map that never moves is a sign nothing is actually being tracked underneath it.

A standard 5×5 likelihood/impact scoring grid (values multiply to a risk score of 1–25):

| Likelihood \ Impact | 1 – Negligible | 2 – Minor | 3 – Moderate | 4 – Major | 5 – Severe |
|---|---|---|---|---|---|
| **5 – Almost Certain** | 5 | 10 | 15 | 20 | 25 |
| **4 – Likely** | 4 | 8 | 12 | 16 | 20 |
| **3 – Possible** | 3 | 6 | 9 | 12 | 15 |
| **2 – Unlikely** | 2 | 4 | 6 | 8 | 10 |
| **1 – Rare** | 1 | 2 | 3 | 4 | 5 |

A common banding: 1–4 Low (green), 5–9 Medium (yellow), 10–14 High (orange), 15–25 Critical (red) — adjust the exact cut points to your own risk appetite statement rather than copying these directly.

See [`templates/risk-heatmap-scoring-guide.md`](templates/risk-heatmap-scoring-guide.md) in this repo for the full grid plus scale-anchor definitions you can adapt.

- [ISO 31010:2019 — Risk Assessment Techniques](https://www.iso.org/standard/72140.html) - Covers risk matrix construction and its known limitations (range compression, arbitrary colour bands) as one of its catalogued techniques.

---

## RACI Matrix

**What it is:** a responsibility-assignment chart naming who is **R**esponsible (does the work), **A**ccountable (owns the outcome — exactly one person per activity), **C**onsulted (gives input before a decision), and **I**nformed (told after) for every risk-management activity — risk identification, scoring, treatment decisions, control testing, and reporting.

**How to build one:**
1. List every recurring risk-management activity down the rows (identify risk, score risk, approve treatment, implement control, test control, approve compensating control, report to board) rather than trying to build one RACI for the whole programme in a single row.
2. Name exactly one Accountable person per row — a RACI with two "A"s for one activity has solved nothing; if you can't pick one, that ambiguity is itself a risk worth logging.
3. Map roles, not just names, so the matrix survives personnel turnover — update the name-to-role mapping separately.
4. Validate the matrix against your Three Lines model (see Risk Taxonomy and Governance above) — the first line should dominate "Responsible," the second line "Accountable" and "Consulted" for policy-level decisions, and the third line "Informed" for nearly everything, since independence requires it to stay out of the "R/A" seats it's later meant to audit.
5. Review the RACI whenever the org chart changes materially, not on a fixed schedule — it decays with reorganisations, not with time.

See [`templates/raci-matrix-template.csv`](templates/raci-matrix-template.csv) in this repo for a starting structure covering the core risk-management activities above.

- [PMI Practice Standard for Project Risk Management](https://www.pmi.org/pmbok-guide-standards) - PMI's treatment of RACI-style responsibility assignment as applied specifically to project-level risk management activities.

---

## Risk Register

**What it is:** the single system of record for every identified risk — its description, category, inherent and residual scores, owner, treatment decision, linked controls (including compensating ones), status, and review date. Everything else in this list (heat map, RACI, KRIs, reporting) is a view generated from the register, not a separate source of truth.

**Required fields, at minimum:**

| Field | Purpose |
|---|---|
| Risk ID | Unique, stable identifier used everywhere else the risk is referenced (heat map, reports, POA&M). |
| Description | A specific event-and-consequence statement, not a vague topic (e.g., "loss of the primary payment processor causes a 4+ hour transaction outage," not "vendor risk"). |
| Category (Taxonomy) | Primary risk category, per your taxonomy above. |
| Owner | Single accountable individual (from the RACI), not a team or department. |
| Inherent Likelihood / Impact / Score | Risk before existing controls are considered. |
| Existing Controls | What is already in place, including any compensating controls. |
| Residual Likelihood / Impact / Score | Risk after existing controls. |
| Treatment Decision | Treat, Transfer, Tolerate, or Terminate. |
| Treatment Plan and Target Date | Specific remediation steps and a date, if the decision is Treat. |
| Status | Open, In Progress, Overdue, Closed, Risk-Accepted. |
| Last Reviewed / Next Review Date | Drives your periodic review cadence (see below). |

**How to run it:**
1. Open the register before you open any spreadsheet-of-findings from an audit or assessment — findings become register entries, not a parallel list.
2. Enforce one risk per row — a compound entry ("weak access controls and outdated patching") cannot be scored, owned, or closed cleanly.
3. Distinguish a risk (potential) from an issue (realised) explicitly — many programmes run a linked but separate issues log, with a pointer back to the risk that materialised.
4. Set a mandatory review date on every open entry at the point of creation, scaled to its severity (see Periodic Review Cadence) — an entry with no review date is how registers go stale.
5. Never delete a closed risk — mark it closed with a rationale and keep it for trend analysis and audit history.

See [`templates/risk-register-template.csv`](templates/risk-register-template.csv) in this repo for a ready-to-use register built on the fields above.

- [NIST SP 800-30 Revision 1](https://csrc.nist.gov/pubs/sp/800/30/r1/final) - Appendix K provides a worked risk-assessment report format that maps closely to the register fields above.
- [ISO 31000:2018](https://www.iso.org/iso-31000-risk-management.html) - Establishes the identify-analyse-evaluate-treat-monitor cycle that a risk register operationalises as a running record.

---

## Risk Treatment and Compensating Controls

**Treatment options (the four T's):**
- **Treat (mitigate)** — implement or improve a control to bring residual risk within appetite.
- **Transfer** — shift financial impact via insurance, contractual indemnification, or outsourcing (which does not eliminate the risk, only who bears the cost).
- **Tolerate (accept)** — a documented, time-bound decision to accept residual risk as-is, made by someone with the authority to accept risk at that level (typically scaled: business-unit owner for Low, senior management for Medium, board or risk committee for High/Critical).
- **Terminate** — stop the activity or process generating the risk entirely, when no combination of the above brings it within appetite at an acceptable cost.

**What a compensating control is:** an alternative control implemented because the originally specified control cannot be — for cost, technical, or timeline reasons — that is intended to provide equivalent or acceptable risk reduction. Auditors and assessors (PCI-DSS in particular has a formal Compensating Controls Worksheet) expect it to be justified with the same rigour as the control it replaces, not waved through informally.

**How to document and approve a compensating control:**
1. Name the specific requirement or control that cannot be met, and why (cost, technical constraint, legacy system, timeline).
2. Describe the compensating control in the same operational detail you would use for a primary control — what it does, how it is implemented, and how it is tested.
3. Explain how it meets the *intent* of the original requirement, not just its letter — this is the section assessors scrutinise hardest.
4. State the residual risk that remains even with the compensating control in place, and score it in the register like any other residual risk.
5. Get sign-off from someone with the authority to accept that residual risk (per your treatment-tolerance escalation above), and set an explicit expiry or re-justification date — a compensating control should never be indefinite by default.
6. Track it in the risk register exactly like a primary control, including its own testing and review cycle.

See [`templates/compensating-control-worksheet.md`](templates/compensating-control-worksheet.md) in this repo for a fillable worksheet built on the structure above.

- [PCI-DSS Compensating Controls Worksheet](https://www.pcisecuritystandards.org/document_library/) - PCI SSC's own formal template and instructions for documenting a compensating control against a specific DSS requirement — the most rigorous, widely referenced example of this pattern in any framework.
- [COSO ERM — Performance Component](https://www.coso.org/guidance-erm) - COSO's treatment of selecting and prioritising risk responses (the four T's above) as part of the ERM Performance component.

---

## Key Risk Indicators and Continuous Monitoring

**What it is:** a Key Risk Indicator (KRI) is a leading metric with a defined threshold that signals rising risk *before* it becomes an issue — distinct from a Key Performance Indicator (KPI), which is a lagging measure of how well something already performed. Continuous monitoring is the operational practice of tracking KRIs (and control effectiveness) on an ongoing basis rather than only at the point of a periodic assessment.

**How to build it:**
1. Derive KRIs from your top-ranked risks in the register, not from whatever metrics happen to already exist in a dashboard — a KRI with no linked risk is just a metric.
2. Set a threshold for each KRI that maps to your risk appetite (green/amber/red, mirroring the heat map bands), and define what action an amber or red breach triggers, and who is notified.
3. Prefer a small number of well-chosen KRIs per risk (2–4) over a large dashboard nobody reviews — a KRI that isn't acted on when it breaches is worse than not having it, because it creates false assurance.
4. Automate collection wherever the underlying control has a system of record (vulnerability scan results, access-review completion rate, patch latency) rather than relying on manual quarterly surveys.
5. Review KRI thresholds themselves periodically — a threshold set when the organisation was a tenth of its current size will generate constant false positives or false negatives if never recalibrated.

- [NIST SP 800-137](https://csrc.nist.gov/pubs/sp/800/137/final) - "Information Security Continuous Monitoring (ISCM) for Federal Information Systems and Organizations," NIST's foundational guide to building an ongoing monitoring programme rather than a point-in-time assessment.
- [COSO ERM — Review and Revision Component](https://www.coso.org/guidance-erm) - COSO's component covering ongoing monitoring and the periodic reassessment of the ERM programme itself, not just individual risks.

---

## Risk Reporting and Board Governance

**How to do it:**
1. Tailor content to the audience, not just the frequency: the board wants top risks, trend direction, and appetite-breach flags; a risk committee wants the heat map plus treatment-plan status; an operational risk owner wants their own register entries and KRI trends in detail.
2. Lead with what changed since the last report — new risks, closed risks, risks that moved bands, and any appetite breaches — not a static restatement of the full register.
3. Report residual risk against appetite explicitly, not just a raw score — "12 of 15 top risks are within appetite; 3 require board attention" is more useful than a list of numbers.
4. Include compensating-control status and expiry dates in every material report — an expired, unreviewed compensating control is a common audit finding.
5. Keep a consistent report template across cycles so trend lines are actually comparable quarter to quarter.

- [COSO ERM — Information, Communication, and Reporting Component](https://www.coso.org/guidance-erm) - COSO's component specifically addressing how risk information should be communicated internally and reported externally.
- [NACD Director's Handbook on Cyber-Risk Oversight](https://www.nacdonline.org/cyber) - The National Association of Corporate Directors' widely referenced guide to what a board should expect to see in cyber-risk reporting specifically.

---

## Periodic Review Cadence

Not every artefact needs the same review frequency — matching cadence to volatility and stakes is itself a risk-management decision.

**Monthly (or continuous):**
- KRI dashboard review by the risk/second-line function.
- Vulnerability scan and patch-latency metrics feeding operational/cyber KRIs.
- New-risk intake from incidents, audit findings, and control self-assessments.

**Quarterly:**
- Full risk register review: re-score every open risk, confirm owners are still correct, chase overdue treatment plans.
- Risk committee or leadership-team reporting: heat map refresh, top-risk trend, appetite-breach flags.
- Compensating-control status review: confirm each is still justified and has not silently become permanent.
- KRI threshold sanity check against recent actuals.

**Semi-annually (6 months):**
- Reassess risk appetite and tolerance statements against any strategic or organisational changes since the last full review.
- Re-run gap analysis against your control baseline for medium-priority frameworks or requirements.
- Refresh third-party/vendor risk tiering (see below) for vendors below your highest-criticality tier.
- RACI matrix review, particularly after any organisational restructuring.

**Annually:**
- Full framework re-alignment: confirm ISO 31000/COSO ERM/NIST SP 800-30 methodology is still fit for purpose, and update scoring scales if they've drifted from actual usage.
- Formal reassessment of risk appetite statements with board or executive sign-off.
- Full gap analysis against your highest-priority control baseline(s), independent of the quarterly register churn.
- Independent (third-line/internal audit) assurance review of the risk-management programme itself, not just individual risks.
- Policy review and re-approval (see Risk Management Policy below).
- Highest-criticality third-party/vendor full reassessment, including a fresh due-diligence cycle.

**Event-driven (run regardless of the calendar):**
- Any material incident, breach, or significant near-miss.
- Major organisational change: M&A, new product line, new regulatory obligation, significant system migration.
- Any compensating control approaching its stated expiry date.

---

## Third-Party and Vendor Risk Management

**What it is:** the risk-management lifecycle applied specifically to vendors and other third parties — due diligence before onboarding, contractual risk allocation, and ongoing monitoring for the life of the relationship. Usually run as its own workstream because it has its own triggers (contract renewal, tiering) distinct from the internal risk-register cadence above.

**How to run it:**
1. Tier vendors by criticality and data access (e.g., Critical/High/Medium/Low) before doing anything else — the depth of due diligence and monitoring should scale directly with tier.
2. Run due diligence proportional to tier: for Critical vendors, request SOC 2 reports, security questionnaires, and evidence of their own risk-management programme; for Low-tier vendors, a lighter self-attestation is often sufficient.
3. Build risk allocation into the contract itself: right-to-audit clauses, breach-notification timelines, liability caps, and subcontractor (fourth-party) disclosure requirements.
4. Monitor continuously between reassessment cycles — a SOC 2 report from 18 months ago is not current assurance for a Critical-tier vendor.
5. Feed vendor risk into the same central risk register as everything else, tagged by taxonomy, rather than maintaining it as a disconnected vendor-management artefact.

- [NIST SP 800-161 Revision 1](https://csrc.nist.gov/pubs/sp/800/161/r1/final) - "Cybersecurity Supply Chain Risk Management Practices for Systems and Organizations," NIST's detailed guide to third-party and supply-chain risk specifically.
- [Shared Assessments Standardized Information Gathering (SIG) Questionnaire](https://sharedassessments.org/sig/) - The industry-standard third-party risk questionnaire used across financial services and beyond, scalable by tier.

---

## Risk Management Policy

**What it is:** the top-level governance document that establishes the risk-management programme's authority, scope, roles (tying back to your Three Lines model), methodology (which standard you follow and your scoring scales), and review cadence. Every artefact in this list should be traceable back to something the policy establishes.

**How to write one:**
1. State purpose and scope first: which business units, systems, and risk categories the policy governs.
2. Name the adopted methodology explicitly (ISO 31000, COSO ERM, or a hybrid) and reference the specific scoring scales in use, rather than restating them inline — link out to the scoring-guide template so the two artefacts can't drift apart.
3. Define roles and authorities by title, not name: who can accept risk at each severity band, who owns the register, who approves compensating controls, who chairs the risk committee.
4. State the mandated review cadence for the register, appetite statements, and the policy itself (see Periodic Review Cadence above) as a binding requirement, not a suggestion.
5. Require board or senior-executive approval and a fixed re-approval interval (annually is standard).

See [`templates/risk-management-policy-template.md`](templates/risk-management-policy-template.md) in this repo for a fillable starting structure covering all of the above.

---

## Templates in This Repo

Ready-to-use starting points, referenced throughout the sections above — copy into your own environment and adapt the scales, categories, and approval authorities to your organisation:

- [`templates/risk-register-template.csv`](templates/risk-register-template.csv) - The core risk register, structured on the fields defined under Risk Register above.
- [`templates/raci-matrix-template.csv`](templates/raci-matrix-template.csv) - A RACI starting structure covering the core recurring risk-management activities.
- [`templates/gap-analysis-template.csv`](templates/gap-analysis-template.csv) - A control gap-analysis tracker using the five-level maturity scale from Gap Analysis above.
- [`templates/risk-heatmap-scoring-guide.md`](templates/risk-heatmap-scoring-guide.md) - The 5×5 likelihood/impact grid plus scale-anchor definitions, ready to adapt to your own appetite thresholds.
- [`templates/compensating-control-worksheet.md`](templates/compensating-control-worksheet.md) - A fillable compensating-control justification and approval worksheet.
- [`templates/risk-management-policy-template.md`](templates/risk-management-policy-template.md) - A starting risk-management policy document covering scope, methodology, roles, and cadence.
- [`templates/periodic-review-checklist.md`](templates/periodic-review-checklist.md) - A checklist version of the Periodic Review Cadence section above, organised by monthly/quarterly/semi-annual/annual/event-driven interval.

---

## Cross-Framework Mapping and GRC Platforms

- [Archer (RSA Archer)](https://www.archerirm.com/) - Long-established enterprise GRC platform with dedicated modules for risk register management, KRI tracking, and third-party risk.
- [LogicGate Risk Cloud](https://www.logicgate.com/) - No-code GRC automation platform for building custom risk-register, RACI, and workflow applications without heavy IT involvement.
- [MetricStream](https://www.metricstream.com/) - Enterprise GRC platform covering ERM, operational risk, and third-party risk management with configurable heat maps and dashboards.
- [Resolver](https://www.resolver.com/) - Risk-management platform combining incident management, risk register, and reporting with a stated focus on connecting risk to business context.
- [Secure Controls Framework (SCF)](https://securecontrolsframework.com/) - Free, open (Creative Commons) meta-framework mapping outward to 250+ laws, regulations, and frameworks; useful for tying a risk register's control references back to specific regulatory language. Shared with the companion [Security Frameworks](https://github.com/garynair/security-frameworks) and [IT Audit & Controls](https://github.com/garynair/it-audit-controls) lists.
- [ServiceNow IRM (Integrated Risk Management)](https://www.servicenow.com/products/governance-risk-and-compliance.html) - Risk-management modules built on the ServiceNow platform, commonly adopted by organisations already running ServiceNow for ITSM.

---

## Certifications and Training

- [CRISC (Certified in Risk and Information Systems Control)](https://www.isaca.org/credentialing/crisc) - ISACA's credential focused specifically on IT risk identification, assessment, response, and monitoring — the most directly relevant certification to this list's scope.
- [FAIR Analysis Fundamentals / Open FAIR Certification](https://www.opengroup.org/certifications/openfair) - The Open Group's certification path for the FAIR quantitative risk-analysis model covered under Quantitative Risk Analysis above.
- [ISO 31000 Risk Manager (PECB)](https://pecb.com/en/education-and-certification-for-individuals/iso-31000) - A practitioner certification built directly on the ISO 31000 standard, covering its principles, framework, and process.
- [PMI-RMP (Risk Management Professional)](https://www.pmi.org/certifications/risk-management-rmp) - PMI's certification for project-level risk management, useful for practitioners whose risk work is primarily project- rather than enterprise-scoped.
- [GIAC Enterprise Risk Management (GERM)](https://www.giac.org/certifications/enterprise-risk-management-germ/) - SANS/GIAC's certification for building and running a risk-management programme with a security-practitioner orientation.

---

## Government and Standards Bodies

- [Committee of Sponsoring Organizations of the Treadway Commission (COSO)](https://www.coso.org/) - The body that publishes and maintains the ERM and Internal Control–Integrated Frameworks referenced throughout this list.
- [FAIR Institute](https://www.fairinstitute.org/) - The nonprofit maintaining the FAIR quantitative risk-analysis standard and its practitioner community.
- [Institute of Internal Auditors (IIA)](https://www.theiia.org/) - The professional body maintaining the Three Lines Model and internal-audit standards referenced under Risk Taxonomy and Governance above.
- [International Organization for Standardization (ISO)](https://www.iso.org/) - The standards body publishing ISO 31000 and ISO 31010.
- [National Institute of Standards and Technology (NIST)](https://www.nist.gov/) - Publisher of SP 800-30, SP 800-39, SP 800-137, and SP 800-161, the free federal risk-management methodology referenced throughout this list.

---

## Learning Resources

- [FAIR-U](https://www.fairinstitute.org/fair-u) - Free, browser-based introduction to FAIR quantitative risk analysis, no licence required.
- [ISO 31000 Risk Management — ISO's Own Overview](https://www.iso.org/iso-31000-risk-management.html) - ISO's own plain-language explainer, a faster starting point than the (paywalled) standard itself.
- [NIST Small Business Cybersecurity Corner](https://www.nist.gov/itl/smallbusinesscyber) - Free, plain-language risk-management resources aimed at organisations without a dedicated risk function.
- [NACD Director's Handbook on Cyber-Risk Oversight](https://www.nacdonline.org/cyber) - Free guide aimed at board members, useful context for anyone building the reporting layer described under Risk Reporting and Board Governance above.

---

## Related Lists

- [Security Frameworks](https://github.com/garynair/security-frameworks) - A companion curated list covering NIST CSF, ISO/IEC 27001, PCI-DSS, CIS Critical Security Controls, DISA STIG, and the CRI Profile — the control catalogues a risk-register's treatment plans typically point to.
- [IT Audit & Controls](https://github.com/garynair/it-audit-controls) - A companion curated list covering COBIT, COSO Internal Control, and ITGC/ITAC — the internal-controls and audit-testing discipline closely related to, but distinct from, the risk-analysis method in this list.
- [Federal Compliance](https://github.com/garynair/federal-compliance) - A companion curated list covering FedRAMP, CMMC, and NIST SP 800-53/37 — including the POA&M artefact, the federal-sector-specific version of this list's Gap Analysis and Risk Register sections.
- [FinServ Compliance](https://github.com/garynair/finserv-compliance) - A companion curated list covering GLBA/FFIEC, NYDFS 500, and SR 26-2 model risk management — the financial-sector regulatory context this list's methodology is often run underneath.

---

## Contributing

PRs welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for the criteria a new entry must meet.

## Licence

This list is published under [CC0 1.0 Universal](LICENSE). The linked resources retain their own licences; COSO and ISO standards in particular are largely paywalled and not freely redistributable. Templates in the `templates/` directory are original works released under the same CC0 licence — use, modify, and redistribute them freely.
