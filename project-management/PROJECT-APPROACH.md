# Project Approach and Delivery Plan

Project: **Project Anti-Spam** (temporary name)  
Document: PAP-01 | Version: 0.2 | Updated: 2026-09-13  
Custodian and final approver: Project owner / PM / technical manager  
Maintainers: PM and developer / contributor

This is the single living reference for project context, status, evidence, requirements, designs, approvals, and next actions. The sequence below records the owner's instructions. Product findings and phase approvals remain pending. Update this document as work progresses; a completed template does not establish approval.

## 1. Current position

| Item | Current state |
| --- | --- |
| Active phase | Discovery — awaiting source input |
| Completed | Documentation setup and consolidation into this plan |
| What we need to build | Not established; the referenced pain-point image/text was not received |
| Validated user/problem | None yet |
| Approved product scope, solution, technology | None |
| Latest phase approval | None |
| Immediate blocker | Missing pain-point source and user context |
| Next action | PM supplies exact pain point and a real example; complete Section 5 |
| Contributor's current work | Read this plan; identify discovery questions and constraints |
| GitHub | Repository URL, accounts, access, and settings pending; no push performed |

| Action | Owner | Dependency | Completion evidence | Status |
| --- | --- | --- | --- | --- |
| Capture pain point, users, recent example | PM | Source input | Discovery record | Waiting for input |
| Agree research participants and method | Both | Discovery | Research plan | Not started |
| Validate problem and current workflow | PM | G01 | Research evidence | Not started |
| Compare alternatives and assess feasibility | Both | G02 | Feasibility recommendation | Not started |

Replace or extend this action queue at each review. Set dates only after availability is agreed.

## 2. Context and intended product

Greenfield project addressing one or two user pain points, with one owner acting as PM and technical manager and one developer/contributor. The temporary name may change; it does not establish a platform, feature, spam channel, or AI requirement.

We will validate the need, assess alternatives, agree business and functional requirements, approve progressively detailed designs, then develop traceable increments against approved LLDs.

| Context to establish | Answer |
| --- | --- |
| Primary users and other stakeholders | TBD |
| Exact problem and measurable impact | TBD — source missing |
| Intended product and value proposition | TBD after research/feasibility |
| Product scope and non-goals | TBD |
| Budget, currency, timeline, developer capacity | TBD |
| Platform, integrations, data access, geography, obligations | TBD |
| Support and maintenance ownership | TBD |

Do not fill gaps with invented interviews, metrics, dates, or technology decisions. Label assumptions and link evidence.

## 3. Delivery approach and gates

Use a **hybrid approach: sequential requirements and design approval, followed by iterative development**. Feedback can reopen earlier decisions when evidence changes.

**Discovery → research → feasibility → implementation-readiness review → BRD → solution options → SDD → FRD → HLD → approved LLDs → development by LLD → validation → release.**

The initial **implementation-readiness review authorizes requirements and design work only**. Coding starts after the relevant LLD baseline is approved.

| Phase / gate | Required output and exit evidence | Lead | Status |
| --- | --- | --- | --- |
| Discovery / G01 | Specific problem, users, current workflow, investigation boundaries and research questions | PM | Awaiting input |
| Research / G02 | Evidence, validated findings, current alternatives, limitations, outcome baseline or measurement plan | PM | Not started |
| Feasibility / G03 | Alternatives, experiments as needed, cost/capacity ranges, risks, go/revise/defer/no-go recommendation | Both | Not started |
| Readiness / G04 | Prior approvals, constraints, investigation blockers resolved, owners and plan for requirements/design | PM | Not started |
| BRD / G05 | Business Requirements Document approved | PM | Not started |
| Solution options / G06 | Multiple approaches compared against BRD; selection and tradeoffs approved | Both | Not started |
| SDD / G07 | Solution Design Document approved | Developer + PM | Not started |
| FRD / G08 | Functional Requirements Document with testable behavior approved | Both | Not started |
| HLD / G09 | High-Level Design approved | Developer | Not started |
| LLDs / G10 | Low-Level Designs, dependencies, acceptance criteria, and test approach for planned batch approved | Developer | Not started |
| Development / per-LLD review | Approved LLD implemented through issues/PRs, verified and reviewed | Developer | Not started |
| Validation / G12 | Integrated tests, user acceptance, known issues and risk decisions | Both | Not started |
| Release / G13 | Revision/environment, deployment/rollback, support readiness and release authorization | PM | Not started |

The PM approves every gate. A gate authorizes only its stated next activity. All LLDs needed for a planned development batch, including shared prerequisites, must be approved before that batch starts. If no batch is defined, approve the full planned LLD set first. Unapproved LLDs are not implementation work items.

## 4. Ownership and living-document rules

| Role | Responsibility |
| --- | --- |
| PM / technical manager | Context, research, business requirements, scope, budget, priorities; approve designs, phases, merges and releases |
| Developer / contributor | Feasibility evidence, estimates, technical designs, LLDs, implementation and verification |
| Representative users (TBD) | Real examples, workflow validation, prototype and acceptance feedback |

After every meaningful completion, finding, blocker, approval, or scope change:

1. Update the relevant section with evidence and remaining uncertainty.
2. Update the current-position table, action queue, and LLD tracker.
3. Record risks and decisions, including impact on earlier baselines.
4. Record explicit PM approval before advancing a gate.
5. Increment the document revision and append change history.

Preserve earlier decisions and approvals; mark superseded records. Material changes to users, scope, cost, requirements, architecture, or data handling require impact assessment and renewed affected approvals before dependent work resumes.

BRD, SDD, FRD, HLD, and LLD are logical artifacts maintained as sections here initially. Do not create separate context documents. If detailed designs later outgrow this file, agree that change first and retain baseline links, status, decisions, and next actions here.

## 5. Discovery record

Owner: PM | Status: Awaiting input

Problem statement: “[User group] struggles to [job] when [situation], causing [observable impact]. Their workaround is [approach], which falls short because [evidence].”

| Question | Answer / evidence |
| --- | --- |
| Exact pain point in the user's words | TBD — image/text needed |
| One recent real example | TBD |
| Primary user and context | TBD |
| Current steps, tools, and workaround | TBD |
| Frequency, severity, time/cost/opportunity impact | TBD |
| Existing approaches tried: what works and fails | TBD |
| Why now; how can users be reached? | TBD |
| Investigation scope and constraints | TBD |

| Outcome ID | Desired outcome | Baseline / source | Target | Measurement / period | Owner |
| --- | --- | --- | --- | --- | --- |
| OUT-01 | TBD | Unknown | TBD | TBD | PM |

G01 review: source captured, problem specific enough to investigate, users and questions identified, assumptions explicit. Decision pending.

## 6. Research record

Owner: PM | Status: Not started

Plan: identify who experiences the problem, its impact, and whether change is worthwhile. Participant criteria, recruitment, sample rationale, dates, and consent approach: TBD. Use redacted evidence; keep identifiable research outside a public repository. A small qualitative sample is not statistically representative.

Interview prompts: last occurrence; workflow before/during/after; frequency and impact; workarounds and past attempts; what already works; costly mistakes a new solution could make; worthwhile outcomes; follow-up validation.

| Evidence ID | Date / method | Anonymized source | Observation / short quote | Interpretation | Limitation |
| --- | --- | --- | --- | --- | --- |
| E-001 | Pending | Referenced image | Not received | No conclusion | Missing source |

| Journey step | User goal/action | Tool/channel | Friction and consequence | Evidence |
| --- | --- | --- | --- | --- |
| TBD | TBD | TBD | TBD | TBD |

| Finding | Supporting evidence | Contradictory evidence | Segment | Confidence / implication |
| --- | --- | --- | --- | --- |
| No validated findings | TBD | TBD | TBD | Pending |

G02 synthesis: priority problem/rationale, current alternatives, outcome baseline or collection plan, sampling limitations, and feasibility questions: all TBD. Prioritize using evidenced severity, frequency, reach, and workaround quality. Decision pending.

## 7. Feasibility and readiness record

Owners: Both | Status: Not started | Verdict: **Pending**

Agree evaluation criteria and mandatory constraints before comparing concrete candidates. Cite capability, pricing, license, and terms evidence when assessed. Mandatory constraints cannot be outweighed by other scores.

| Alternative | User-need coverage | Technical/data fit | Cost / effort range | Risks / maintenance | Verdict |
| --- | --- | --- | --- | --- | --- |
| Current workaround / do nothing | TBD | TBD | TBD | TBD | Unassessed |
| Process change | TBD | TBD | TBD | TBD | Unassessed |
| Adopt/configure existing product | TBD | TBD | TBD | TBD | Unassessed |
| Custom solution | TBD | TBD | TBD | TBD | Unassessed |

Assess user adoption, platform/API availability, reliability, authorized data access and quality, retention/deletion, economics, skills/capacity, operations/support, security/privacy, and relevant legal/contractual constraints. PM owns business evidence; developer owns technical evidence; both cover data and operations. Findings: TBD.

If spam classification becomes relevant, investigate false positives, false negatives, correction, and evaluation data quality. This is conditional and does not select ML.

### Experiments and business case

Only agreed, timeboxed feasibility experiments may precede LLD approval; they do not authorize production implementation.

| Experiment | Assumption | Method / authorized data | Pass/fail criterion set beforehand | Timebox / owner | Result / evidence |
| --- | --- | --- | --- | --- | --- |
| EXP-01 | TBD | TBD | TBD | TBD | Not run |

Currency, horizon, hourly-cost assumption, budget ceiling, and confidence: TBD. Estimate low/high ranges with sources for one-time design/build/test hours, setup/onboarding, recurring services/licenses, maintenance/support, contingency, and quantifiable benefits.

Initial cost = one-time hours × hourly cost + expenses + contingency. Monthly operating cost = services + maintenance hours × hourly cost. Net monthly benefit = quantifiable benefit − operating cost. Payback = initial cost / positive net monthly benefit; otherwise payback is not established. State exclusions; separate nonfinancial benefits and avoid double counting.

G03 recommendation: preferred direction, rejected alternatives/reasons, tested assumptions, cost/effort confidence, residual risks/owners, and go/revise/defer/no-go decision: pending.

G04 checklist: G01–G03 approved; critical investigation blockers resolved; constraints/capacity understood; BRD/design owners and review plan assigned; remaining unknowns have handling plans. Output: authorization for BRD and design only. Decision pending.

## 8. Requirements and design workspace

Not started. Populate in this order after G04. Each artifact gets its own revision and approval record in Section 10.

### 8.1 BRD — Business Requirements Document

ID: BRD-01 | Revision: Not started | Owner: PM | Gate: G05

Required contents: business background, validated problem/evidence, objectives, stakeholders, scope/non-goals, current/desired processes, business rules, constraints, dependencies, success measures, and business acceptance conditions.

| Requirement ID | Business requirement / rationale | Evidence / outcome | Priority | Acceptance measure |
| --- | --- | --- | --- | --- |
| BR-001 | TBD | TBD | TBD | TBD |

### 8.2 Solution options

ID: OPT-01 | Revision: Not started | Owners: Both | Gate: G06

Compare concrete approaches against approved BRD and feasibility constraints. Reuse evidence and add coverage gaps, complexity, maintainability, costs, security, dependencies, and tradeoffs. Record selected option, rejected alternatives, and PM rationale. Selection: pending.

### 8.3 SDD — Solution Design Document

ID: SDD-01 | Revision: Not started | Owners: Developer + PM | Gate: G07

Document selected end-to-end solution, user journey, business capability coverage, boundaries, major building blocks, external systems, conceptual data flow, deployment concept, assumptions, and decisions. HLD later resolves technical architecture against approved functional requirements. Content: TBD.

### 8.4 FRD — Functional Requirements Document

ID: FRD-01 | Revision: Not started | Owners: Both | Gate: G08

Specify actors, use cases, inputs/outputs, permissions, validation, rules, alternate/error paths, and testable acceptance criteria. Include measurable nonfunctional constraints for architecture and testing.

| Requirement ID | BRD / SDD reference | Behavior and exceptions | Acceptance criteria | Priority |
| --- | --- | --- | --- | --- |
| FR-001 | TBD | TBD | TBD | TBD |

### 8.5 HLD — High-Level Design

ID: HLD-01 | Revision: Not started | Owner: Developer | Gate: G09

Define architecture, component responsibilities, interfaces, stores/data flows, trust boundaries, identity/access, deployment environments, reliability/performance, observability, security/privacy, dependencies, and technical tradeoffs. Map coverage to FRD and nonfunctional constraints. Content: TBD.

### 8.6 LLDs — Low-Level Designs and tracker

Owner: Developer | Approver: PM / technical manager | Gate: G10 for planned batch

Add LLD-001, LLD-002, and later design subsections here as HLD is decomposed. Each must contain purpose/scope, upstream IDs and revisions, detailed behavior, contracts/schema/validation, algorithms or sequences, errors/recovery, relevant security/configuration/logging, dependencies/order, acceptance criteria, test cases, estimates, open questions, revision, and approval evidence.

| LLD | Scope / upstream references | Dependencies | Design revision / approval | Development status | Issue / PR / tests |
| --- | --- | --- | --- | --- | --- |
| LLD-001 | TBD after HLD | TBD | Not drafted / not approved | Not authorized | None |
| LLD-002 | TBD after HLD | TBD | Not drafted / not approved | Not authorized | None |

These IDs are placeholders, not approved modules. Planned batch and required LLD set: TBD.

Design states: Not drafted → Draft → In review → Approved or Changes requested. Development states: Not authorized → Ready → In progress → PR review → Verified / merged. An implementation-affecting LLD change requires renewed approval before dependent coding.

## 9. GitHub handoff, development, and release

At the approved LLD handoff, the PM establishes/pushes the approved baseline and authorizes the planned batch. Documentation can be reviewed locally beforehand. Earlier documentation-only publication, if the PM chooses it, does not authorize coding. This plan does not perform remote actions.

Before handoff confirm repository URL/visibility, contributor accounts/access, default branch, review/merge policy, and appropriate checks when available. Set ownership rules once handles are known. For PM-authored documents, obtain contributor review and separately record the PM gate decision. Remote configuration remains pending.

For each approved LLD:

1. Check revision, upstream baseline, batch approval, and dependencies.
2. Create linked issue(s) with acceptance criteria; use a short-lived branch.
3. Develop to the LLD and perform appropriate verification.
4. Open a PR referencing LLD revision, requirement IDs, and results.
5. Obtain PM technical review; route design changes through approval.
6. Merge after agreed checks/review; update this plan and next actions.

Traceability: evidence → outcome → BRD → solution design → FRD → HLD → LLD → issue → PR → tests → release.

Proposed rhythm: short weekly review, asynchronous status changes, and a small board (Backlog → Ready → In progress → Review → Done). Start with one implementation item in progress for the single developer. Done means criteria/checks satisfied, documentation updated, and reviewed change merged; release is a separate approval.

G12 evidence: integrated tests, relevant functional/failure/security/performance checks, requirements coverage, user acceptance, known issues and residual-risk decisions. G13 evidence: revision/environment, release notes, deployment/rollback, secrets/configuration handling, monitoring/support ownership, and outcome measurement plan. Results and approvals: pending.

## 10. Approvals and decisions

This gate scheme supersedes the initial pack's draft G1–G4 proposal. No old gate was approved.

| Gate | Decision | Reviewed baseline / evidence | Approver / date | Authorization |
| --- | --- | --- | --- | --- |
| G01–G04 | All pending; create separate records when reviewed | None | None | None yet |
| G05–G09 | All pending; create separate records when reviewed | None | None | None yet |
| G10 | Pending; record each planned batch | None | None | No development |
| G12–G13 | Both pending; record separately | None | None | No release |

Each actual record must include gate ID, section/artifact revision or exact Git commit, decision (approved / changes requested / deferred / rejected), rationale/evidence, conditions with owners/dates, approver/date, written approval link or reference, and authorized next activity. Resolve blocking conditions first. File creation, commit, push, or merge alone is not phase approval.

| Decision | Date | Instruction / rationale | Authority | Status |
| --- | --- | --- | --- | --- |
| D-001 | 2026-09-13 | Temporary name Project Anti-Spam | Owner kickoff | Recorded |
| D-002 | 2026-09-13 | Owner is PM/technical manager; contributor develops through GitHub | Owner kickoff | Recorded |
| D-003 | 2026-09-13 | One living context and approach document | Owner follow-up | Recorded |
| D-004 | 2026-09-13 | Discovery/research/feasibility/readiness, then BRD/options/SDD/FRD/HLD/LLDs; develop against approved LLDs | Owner follow-up | Recorded; replaces shorter phase proposal |

## 11. Risks, assumptions, and questions

| Risk | Likelihood / impact | Response / owner | Status |
| --- | --- | --- | --- |
| R-01 Missing source could lead to wrong problem | Unassessed / high | Obtain source and validate / PM | Open |
| R-02 Single developer limits capacity/support | Unassessed / unassessed | Agree availability and estimates / both | Open |
| R-03 Design/code drifts from approved intent | Unassessed / unassessed | Traceability and renewed affected approvals / both | Open |

Assumption A-01: a software change may be worthwhile. Unvalidated; both assess through research and non-build alternatives by G03.

| Question | Owner | Needed by | Answer |
| --- | --- | --- | --- |
| Q-01 Exact pain-point source? | PM | G01 | Pending |
| Q-02 Users and validation access? | PM | G02 | Pending |
| Q-03 Budget, availability, timing? | PM | G03 | Pending |
| Q-04 Platform, data, privacy constraints? | Both | G03 | Pending |
| Q-05 GitHub repository and accounts? | PM | LLD handoff | Pending |

Preserve resolved entries with evidence and decision links.

## 12. Guidance and tailoring

Public guidance consulted in the initial pack on 2026-09-13: [Google Design Sprint](https://designsprintkit.withgoogle.com/methodology), [Google discovery methods](https://designsprintkit.withgoogle.com/methodology/phase1-understand), [Microsoft Cloud Adoption Framework](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/), [Microsoft work tracking](https://learn.microsoft.com/en-us/azure/devops/boards/get-started/plan-track-work?view=azure-devops), and [Microsoft SDL](https://learn.microsoft.com/en-us/compliance/assurance/assurance-microsoft-security-development-lifecycle).

These informed discovery, outcome-led planning, visible work, and early security consideration. This exact document sequence and approval process are tailored to the owner, not a universal Google/Microsoft standard or an ISO compliance claim. No cloud provider or formal Scrum process is mandated.

## 13. Change history

| Date | Revision | Change | Approval implication |
| --- | --- | --- | --- |
| 2026-09-13 | 0.1 | Separate discovery, feasibility, and governance templates | All phase approvals pending |
| 2026-09-13 | 0.2 | Consolidated living plan; owner-requested BRD/options/SDD/FRD/HLD/LLD sequence and LLD handoff | Records process instructions; no product phase approved |
