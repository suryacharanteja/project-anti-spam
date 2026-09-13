# Project Approach and Delivery Plan

Project: **Project Anti-Spam** (temporary name)  
Document: PAP-01 | Version: 0.3 | Updated: 2026-09-13  
Custodian and final approver: Project owner / PM / technical manager  
Maintainers: PM and developer / contributor

This is the single living reference for project context, status, evidence, requirements, designs, approvals, and next actions. The sequence below records the owner's instructions. Product findings and phase approvals remain pending. Update this document as work progresses; a completed template does not establish approval.

## 1. Current position

| Item | Current state |
| --- | --- |
| Active phase | Discovery and initial desk research — findings ready for owner review; user validation pending |
| Completed | Living plan; owner pain-point capture; initial market, open-source, and Android constraints review |
| What we need to build | Proposed Android app: assess incoming number risk, let a natural-sounding voice agent screen suspected spam/scams, notify user and enable live takeover for likely genuine callers |
| Validated user/problem | Owner-reported time loss from nuisance/scam calls; independent user evidence not yet collected |
| Approved product scope, solution, technology | Android-first investigation directed by owner; no MVP, model, architecture, or implementation baseline approved |
| Latest phase approval | None |
| Immediate blocker | Initial geography, languages, carriers/devices, and meaning of “counteract” unresolved |
| Next action | Select first market and validate user workflow; review Section 6 findings before closing discovery/research |
| Contributor's current work | Review source-linked candidates and data gaps; prepare platform/routing experiments for later feasibility approval |
| GitHub | Repository URL, accounts, access, and settings pending; no push performed |

| Action | Owner | Dependency | Completion evidence | Status |
| --- | --- | --- | --- | --- |
| Capture business pain point and proposed experience | PM | Owner narrative | Section 5 / E-001 | Complete; real user examples pending |
| Survey products and reusable repositories | Research / developer reviews | Owner authorization D-005 | Section 6 | Initial desk review complete |
| Select initial geography, languages, carriers/devices, and agent behavior | PM | Owner choices | Q-06/Q-07 resolved | Awaiting input |
| Validate user pain and competitor gaps | PM | Defined target segment | Interviews and short call diary | Not started |
| Review G01/G02 findings and agree feasibility experiments | PM + developer | Research synthesis | Gate records and experiment scope | Pending |

Replace or extend this action queue at each review. Set dates only after availability is agreed.

## 2. Context and intended product

Greenfield project addressing time lost to spam and scam calls, with one owner acting as PM and technical manager and one developer/contributor. Android is the owner's first platform. The temporary name may change. Machine learning and a conversational voice agent are proposed solution elements to investigate, not yet selected technologies.

We will validate the need, assess alternatives, agree business and functional requirements, approve progressively detailed designs, then develop traceable increments against approved LLDs.

| Context to establish | Answer |
| --- | --- |
| Primary users and other stakeholders | Android users receiving frequent unwanted calls; first country/segment TBD; genuine callers also affected |
| Exact problem and measurable impact | Interruptions and time spent answering spam/scam calls; owner cites 3–4 minutes and potentially 15 minutes as examples, not measured averages |
| Intended product and value proposition | Reduce user time spent on unwanted calls while preserving access for genuine callers through agent screening and live takeover |
| Product scope and non-goals | Investigate inbound Android phone calls first; exact MVP pending. SMS, iOS, and outbound calling are not requested for this initial scope |
| Budget, currency, timeline, developer capacity | TBD |
| Platform, integrations, data access, geography, obligations | Android-first; ordinary SIM/carrier calls assumed for discovery and must be confirmed. Geography, routing, data rights, and obligations pending |
| Support and maintenance ownership | TBD |

Do not fill gaps with invented interviews, metrics, dates, or technology decisions. Label assumptions and link evidence.

## 3. Delivery approach and gates

Use a **hybrid approach: sequential requirements and design approval, followed by iterative development**. Feedback can reopen earlier decisions when evidence changes.

**Discovery → research → feasibility → implementation-readiness review → BRD → solution options → SDD → FRD → HLD → approved LLDs → development by LLD → validation → release.**

The initial **implementation-readiness review authorizes requirements and design work only**. Coding starts after the relevant LLD baseline is approved.

| Phase / gate | Required output and exit evidence | Lead | Status |
| --- | --- | --- | --- |
| Discovery / G01 | Specific problem, users, current workflow, investigation boundaries and research questions | PM | Draft captured; approval pending |
| Research / G02 | Evidence, validated findings, current alternatives, limitations, outcome baseline or measurement plan | PM | Initial desk review complete; user validation pending |
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

Owner: PM | Status: Draft captured from owner narrative; validation pending

Problem statement: Android users in affected geographies lose valuable time when they answer unwanted promotional or fraudulent calls. They must personally establish the caller's intent, sometimes spending several minutes before realizing the call is unwanted. We want to reduce those interruptions without causing genuine callers to be missed. This is the owner's problem hypothesis; prevalence, severity, and market-specific dissatisfaction remain to be measured.

| Question | Answer / evidence |
| --- | --- |
| Exact pain point in the user's words | “People get a lot of scam and spam calls”; calls waste end users' valuable time. Source: owner narrative, 2026-09-13 |
| One recent real example | Not yet collected from a representative user |
| Primary user and context | Android users in high-nuisance-call geographies; first market TBD |
| Current steps, tools, and workaround | Owner describes user answering and talking before recognizing unwanted intent; actual blocker/caller-ID usage to research |
| Frequency, severity, time/cost/opportunity impact | Owner examples of 3–4 or 15 minutes; no validated daily frequency or average duration |
| Existing approaches tried: what works and fails | Truecaller named as comparison, not evidence that users tried it or found it insufficient |
| Why now; how can users be reached? | Owner wants to investigate; recruitment and timing rationale pending |
| Investigation scope and constraints | Android inbound calls, number reputation/patterns, conversational screening, and same-device live takeover |

| Outcome ID | Desired outcome | Baseline / source | Target | Measurement / period | Owner |
| --- | --- | --- | --- | --- | --- |
| OUT-01 | Reduce time the user spends handling unwanted calls | Unknown | Set after research | Unwanted-call handling minutes per user/week, before vs after | PM |
| OUT-02 | Preserve genuine-call access | Unknown | Set before feasibility testing | Genuine callers interrupted, wrongly blocked, or abandoning screening / all genuine calls | PM |
| OUT-03 | Make genuine-call takeover usable | Unknown | Set before experiment | Successful live takeovers / attempts; time from decision to user connection | Both |

### Proposed experience — hypothesis, not BRD approval

1. Incoming number is assessed using reputation, reports, and available patterns; ML may contribute.
2. Likely normal calls reach the user. Suspected spam/scam calls are screened by a natural-sounding voice agent.
3. The agent converses to assess intent and handles the unwanted caller. “Counteract” needs a product decision: short screening/termination versus extended engagement to occupy the caller.
4. If conversation suggests an initial false positive, alert the user on the same phone and offer live takeover. A notification alone does not transfer the audio session; routing must support it.
5. User corrections can improve later decisions, subject to consent, data quality, and retention choices.

Proposed working labels: **spam** = unwanted solicitation; **scam** = suspected deceptive/fraudulent intent; **normal** = likely legitimate call. Add **unknown/uncertain** as a decision state rather than forcing every new number into a confident label. These definitions need PM approval and consistent annotation. Absence of detected scam evidence is not proof of legitimacy.

G01 review: owner source captured and proposed journey documented. Still needed: target segment, real examples, current alternatives, and agreed research boundary. Decision pending. The owner explicitly authorized the desk research below without declaring G01 complete.

## 6. Research record

Owner: PM | Status: Initial desk research complete; interviews and hands-on product evaluation not performed

Plan: identify who experiences the problem, its impact, and whether change is worthwhile. Participant criteria, recruitment, sample rationale, dates, and consent approach: TBD. Use redacted evidence; keep identifiable research outside a public repository. A small qualitative sample is not statistically representative.

Interview prompts: last occurrence; workflow before/during/after; frequency and impact; workarounds and past attempts; what already works; costly mistakes a new solution could make; worthwhile outcomes; follow-up validation.

| Evidence ID | Date / method | Anonymized source | Observation / short quote | Interpretation | Limitation |
| --- | --- | --- | --- | --- | --- |
| E-001 | 2026-09-13 / owner narrative | Project owner | Time loss from spam/scam calls; Android classification, agent screening, genuine-call takeover proposed | Clear hypothesis and investigation scope | Not independent user validation; original image no longer needed to start |
| E-002 | 2026-09-13 / official product pages | Vendors in Section 6.1 | Caller identification and conversational screening already offered | Need a specific unmet-market hypothesis | Vendor claims; not tested on target devices/carriers |
| E-003 | 2026-09-13 / official Android docs | Section 6.2 | Number screening and cellular audio access are different capabilities | Voice/routing is an early feasibility dependency | No device experiment performed |
| E-004 | 2026-09-13 / repository README and GitHub metadata | Section 6.3 | Reusable components and research pipelines exist | Reuse candidates, not production-ready integrated solution | No code audit, build, benchmark, or dependency audit |

| Journey step | User goal/action | Tool/channel | Friction and consequence | Evidence |
| --- | --- | --- | --- | --- |
| Incoming call | Decide whether to answer | Android phone | Unknown caller/intent interrupts user | E-001 |
| Conversation | Establish purpose | User answers | Several minutes may be wasted | E-001; duration unvalidated |
| Desired screening | Agent assesses suspected caller | Proposed app + routing TBD | Need to preserve genuine callers and enable takeover | E-001; proposed journey |

| Finding | Supporting evidence | Contradictory evidence | Segment | Confidence / implication |
| --- | --- | --- | --- | --- |
| Proposed core flow has close competitors | E-002 / Section 6.1 | Geographic or language gaps may exist | Target TBD | High confidence in feature overlap; differentiation unvalidated |
| Audio/routing is distinct from caller-ID classification | E-003 | OEM products demonstrate capabilities unavailable to an ordinary app by default | Android | High confidence in documented distinction; route not selected |
| Code reuse does not supply a regional reputation dataset or proven three-class model | E-004 | Research examples supply partial approaches | Target TBD | Initial search finding, not proof none exists |

### 6.1 Market discovery — checked 2026-09-13

Scope: a focused landscape of close substitutes, not an exhaustive app-store census. “Available” means an official product page or support guide exists; installation, local subscription prices, language quality, and carrier eligibility have not been tested. Vendor performance percentages are not independently validated and are not used as our targets.

| Product | Relevant capability | Coverage / delivery constraint | Relevance and remaining gap |
| --- | --- | --- | --- |
| [Truecaller Assistant](https://www.truecaller.com/call-screening) | Answers/screens calls, asks purpose, provides information for user pickup decisions; closest third-party comparison | Selected countries; [activation uses call forwarding](https://support.truecaller.com/support/solutions/articles/81000419841-assistant-activation). [Terms describe declined/missed-call conditional forwarding](https://www.truecaller.com/premium-terms-of-service) | Benchmark screening and takeover; verify local carrier, trigger, languages and plan. Do not assume all suspicious calls can be silently diverted before ringing |
| [Google Phone / Pixel Call Screen](https://support.google.com/phoneapp/answer/9118387) | Answers, asks identity/purpose, ends spam or rings user for other calls; live transcript and manual pickup | Automatic screening currently listed for Pixel in Australia, Canada, Ireland, UK, US; manual coverage broader; device/SIM/roaming constraints | Very close desired experience on eligible devices. OEM feature availability does not imply reusable third-party API access |
| [Samsung Galaxy Call screening](https://www.samsung.com/ca/support/mobile-devices/how-to-use-the-call-screening-feature-with-ai-assistant-on-the-samsung-galaxy-s26-series/) | Automatic screening; caller name/purpose; text-to-voice interaction and switch to voice call | Official guide targets Galaxy S26; model/software and language availability vary | Another close OEM substitute; test exact target handset rather than generalizing to all Samsung phones |
| [Hiya Spam Blocker](https://apphelp.hiya.com/en/articles/1-how-to-set-up-hiya-spam-blocker-for-android) / [Hiya AI Phone](https://www.hiya.com/products/apps/hiya-ai-phone) | Android identification/blocking; separate AI Phone page advertises screening and real-time scam protection | Android setup guide requires default phone role; AI Phone page says US-only | Treat product editions separately; do not attribute every AI feature to every Android installation. Target-market availability needs verification |
| [Robokiller Answer Bots](https://robokiller.com/roboradio/) | Bot conversations aimed at occupying spam callers | [Help guide](https://support.robokiller.com/hc/en-us/articles/18763010932372-How-can-I-enable-or-disable-Answer-Bots) ties availability to supported conditional forwarding and Premium+ | Closest “waste caller time” comparison; bot entertainment is not evidence of reliable genuine-call classification or takeover |
| [Whoscall](https://web.whoscall.com/en) | Caller ID and automated spam blocking; [multi-source approach](https://web.whoscall.com/en/security) | Market, database and platform coverage require local check | Reputation-led comparator. Reviewed pages do not establish equivalent conversational agent and live handoff |

Discovery inference: the opportunity is not established merely by adding AI voice to caller ID. Candidate gaps to test are underserved languages/geographies, protection on ordinary Android devices, privacy, affordable routing, and fewer missed genuine calls. Do not claim competitors use only reporting counts; the reviewed offerings include other signals and conversation screening.

### 6.2 Android and call routing — discovery constraints for feasibility

- [CallScreeningService](https://developer.android.com/reference/android/telecom/CallScreeningService?authuser=7) supports pre-answer screening decisions with a five-second response deadline. A network lookup needs a bounded timeout and fallback; a multi-turn voice interview cannot run inside that decision window.
- [Android audio-sharing documentation](https://developer.android.com/media/platform/sharing-audio-input) distinguishes ordinary microphone access from cellular call capture, which requires a privileged preinstalled app with `CAPTURE_AUDIO_OUTPUT`. Caller-ID/default-dialer status alone must not be assumed to supply a bidirectional cellular audio stream. No supported generic voice-injection path was established in this review.
- [Caller verification status](https://developer.android.com/develop/connectivity/telecom/dialer-app/prevent-spoofing) is a possible signal. Number identity verification is not proof that a caller's intent is genuine; unknown or spoofed numbers need uncertainty handling.
- [Google Play call-log policy](https://support.google.com/googleplay/android-developer/answer/10208820) must be checked against the exact permissions and core function before distribution. An open-source example is not evidence of store approval.
- [LiveKit telephony](https://docs.livekit.io/telephony/) supplies SIP-based media/routing concepts and transfer support. This is a candidate for a server-controlled call leg, not access to a phone's existing SIM audio.

Candidate routes to test later: (A) ordinary Android reputation/blocking with a narrower feature set; (B) carrier forwarding to hosted agent and Android takeover via a controlled media connection; (C) OEM/carrier integration. None selected. Route B must prove forwarding eligibility, original caller-ID preservation, cost, and same-phone takeover without a forwarding loop. Taking over via in-app VoIP may differ from returning to the native SIM call and needs owner acceptance. SMS notifications, recordings, and microphone demos do not prove live-call handoff.

### 6.3 Open-source reuse inventory — checked 2026-09-13

Primary repository README and GitHub metadata reviewed. Dates below are GitHub `pushed_at` snapshot dates, not guarantees of stable releases or production quality. All listed repositories were unarchived. License labels are repository-level metadata; dependency, model-weight, voice, and dataset rights require separate verification at a pinned revision before reuse. Nothing cloned, integrated, or executed.

| Repository / component | Potential reuse and location | License / latest push date observed | Assessment / limitation |
| --- | --- | --- | --- |
| [aj3423/SpamBlocker](https://github.com/aj3423/SpamBlocker) | Android 10+ call rules, contacts/patterns, blocklist flow and caller-ID integration reference | MIT / 2026-09-12 | Shortlist for Android screening reference; not an autonomous voice agent; downloaded lists have separate provenance |
| [google/libphonenumber](https://github.com/google/libphonenumber) | Parse/normalize international numbers before matching; Android/Java utility | Apache-2.0 / 2026-09-10 | Shortlist utility; valid number format does not mean safe caller and is not a classifier |
| [k2-fsa/sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) | Android-capable local streaming/nonstreaming speech recognition, synthesis, voice activity detection | Apache-2.0 engine / 2026-09-11 | Shortlist speech runtime; select and verify individual model/language licenses and device performance; supplies no SIM access |
| [ggml-org/whisper.cpp](https://github.com/ggml-org/whisper.cpp) | Speech-to-text reference with Android example | MIT code / 2026-09-11 | Alternative STT benchmark; model size, latency, battery and noisy-call quality untested; transcription is not scam classification |
| [OHF-Voice/piper1-gpl](https://github.com/OHF-Voice/piper1-gpl) | Local neural text-to-speech | GPL-3.0 / 2026-09-09 | Conditional candidate; assess distribution obligations and each voice model's terms. Naturalness and telephony latency untested |
| [pipecat-ai/pipecat](https://github.com/pipecat-ai/pipecat) | Python voice-agent orchestration; STT/conversation/TTS pipeline, Android client option | BSD-2-Clause / 2026-09-12 | Shortlist for a server-side route; requires usable media transport and chosen models/services, not a drop-in native cellular assistant |
| [livekit/agents](https://github.com/livekit/agents) | Server voice agents with telephony/media ecosystem and Android client possibilities | Apache-2.0 framework / 2026-09-13 | Alternative to Pipecat, not automatically both; hosting/telephony and models separate. Turn-detection models have their own LiveKit Model License |
| [BYU-PCCL/scam-call-identification](https://github.com/BYU-PCCL/scam-call-identification) | Research pipeline using transcript features and ML for legitimate/fraudulent calls | MIT code / 2025-09-27 | Research shortlist; explicitly in development, includes external LLM feature extraction. Audit underlying data rights and artifacts; not number-only or validated three-class Android model |
| [ICT-SIT/ScamDetector](https://github.com/ICT-SIT/ScamDetector) | Binary scam/normal transcript experiments including classical ML and transformers | No license detected in metadata / 2024-06-08 | Reference only until license clarified. README describes mixed sources and generated Singapore-style conversations; no assumed commercial data/code reuse or real-world accuracy |
| [salishforge/callscreen](https://github.com/salishforge/callscreen) | Twilio-based self-hosted screening/forwarding architecture example | MIT / 2026-04-07 | Architecture reference only: author explicitly says alpha and not validated end-to-end in real telephony. Landline/VoIP focus; hosted service dependencies remain |

Recommended first inspection set for the contributor: SpamBlocker + libphonenumber for the number-screening layer; sherpa-onnx as a speech benchmark; compare LiveKit Agents **or** Pipecat only if the call route supports server audio; BYU as classification research. Do not fork an entire app or select a stack until feasibility, licensing, and architecture decisions are made.

### 6.4 Classification and data findings

There are two separate prediction problems: **before answer**, number reputation and available metadata estimate risk; **during screening**, conversation content can update that estimate. Caller-number patterns cannot establish fraudulent intent by themselves. New numbers, spoofing, reassignment, biased/malicious reports, and regional coverage are key unknowns.

No ready-to-use, independently validated, geographically applicable normal/spam/scam number classifier was established by this search. The shortlisted research systems use transcripts and mostly binary labels. Speech models supply text/audio capabilities, not scam expertise. SMS classification datasets are not substitutes for natural phone-call evaluation.

Before training, identify an authorized reputation source and consented/lawfully usable call examples; record provenance, label definitions, permitted use, retention, geography/language, class balance, and annotation disagreements. Repository code licenses do not grant rights to referenced datasets or vendor reputation databases. Do not assume a Truecaller SDK grants access to its spam database.

Suggested later benchmark: compare rules/reputation baseline, simple transcript classifier, and a more complex model only if justified. Split evaluations by caller and time (and campaign where known) to reduce leakage. Measure per-class precision/recall, genuine-call false-positive rate, abstention rate, early-decision latency, handoff success, and cost per screened minute. Test legitimate urgent calls, delivery drivers, doctors, unknown businesses, accents, noise, and evasive callers. Thresholds and target dataset remain pending.

### 6.5 Discovery conclusion and next work

**Recommendation: continue targeted discovery; do not begin BRD, model training, or implementation yet.** The owner hypothesis is clear and close competitors exist. The main unanswered business question is which users are still underserved; the main technical question for the next phase is how the call reaches the agent and returns to the user.

Next: PM selects one country, primary language(s), and target Android/carrier profile; resolves “counteract”; recruits a proposed initial 5–8 users (qualitative learning, not statistical validation); collects a short call diary and examples of legitimate unknown calls; compares locally available competitors on that same profile. Record actual costs and user objections to call forwarding/cloud audio. Interview counts/timebox are proposals, not completed research.

G02 remains pending: desk research provides E-002–E-004, but user evidence, target-market gap, outcome baselines, and agreed feasibility boundaries are incomplete.

## 7. Feasibility and readiness record

Owners: Both | Status: Study not started; discovery constraints and proposed experiments recorded below | Verdict: **Pending**

Agree evaluation criteria and mandatory constraints before comparing concrete candidates. Cite capability, pricing, license, and terms evidence when assessed. Mandatory constraints cannot be outweighed by other scores.

| Alternative | User-need coverage | Technical/data fit | Cost / effort range | Risks / maintenance | Verdict |
| --- | --- | --- | --- | --- | --- |
| Current workaround / do nothing | User answers/ignores calls | Baseline to measure | TBD | Continued interruption or missed calls | Unassessed |
| Process change | Contacts, voicemail, existing phone settings | Device-specific | TBD | Genuine unknown calls may be missed | Unassessed |
| Adopt/configure existing product | Section 6.1 candidates | Country/carrier/device check needed | Local price TBD | Coverage, privacy, false positives | Unassessed |
| Custom solution | Proposed classification + voice screening + takeover | Android audio/routing unresolved | TBD | Data access, forwarding, latency, support | Unassessed |

Assess user adoption, platform/API availability, reliability, authorized data access and quality, retention/deletion, economics, skills/capacity, operations/support, security/privacy, and relevant legal/contractual constraints. PM owns business evidence; developer owns technical evidence; both cover data and operations. Findings: TBD.

For the requested classification, assess false positives/negatives, uncertainty, user correction, and evaluation data quality. ML remains an option rather than a prerequisite. Define whether agent handling means brief filtering or longer caller engagement; extended calls increase operating cost and may conflict with a time-saving objective.

### Experiments and business case

Only agreed, timeboxed feasibility experiments may precede LLD approval; they do not authorize production implementation.

| Experiment | Assumption | Method / authorized data | Pass/fail criterion set beforehand | Timebox / owner | Result / evidence |
| --- | --- | --- | --- | --- | --- |
| EXP-01 Android screening boundary | Supported APIs meet pre-answer needs | Controlled calls on target stock devices; inspect role, metadata, blocking and timeout behavior | Respond within documented five-second limit; demonstrate known, unknown, private-number and timeout handling without unsupported permissions | Agree after G02 / developer | Not run |
| EXP-02 Voice route and takeover | A supported route can answer, exchange audio, and connect the same user | Consented test calls using shortlisted carrier/forwarding or other supported route | Demonstrate bidirectional voice and same-phone live takeover without loop/drop; document caller-ID behavior, decline/no-response, network loss, and routing charges | Agree after G02 / developer | Not run; primary technical gate |
| EXP-03 Classification baseline | Data and signals support useful decisions | Licensed/consented dataset; caller/time-separated evaluation | PM sets per-class quality and genuine-call error limits before run; report uncertainty and compare against rules baseline | Agree after G02 / both | Not run |
| EXP-04 Voice experience and unit economics | Agent is understandable, responsive, and affordable | Authorized language/noise samples on proven route | Agree latency, comprehension, naturalness, takeover and per-minute cost limits before run | Agree after EXP-02 / both | Not run |

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
| G01 | Pending | PAP-01 v0.3 Section 5 draft | None | Desk research authorized by D-005; phase not closed |
| G02 | Pending | PAP-01 v0.3 Section 6 desk findings | None | User validation and research refinement only |
| G03–G04 | Both pending; create separate records when reviewed | None | None | No readiness or BRD authorization |
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
| D-005 | 2026-09-13 | Capture Android spam/scam time-loss use case; investigate competing products and open-source reuse first | Owner business-pain-point narrative | Research authorized; not G01/G02 completion approval |

## 11. Risks, assumptions, and questions

| Risk | Likelihood / impact | Response / owner | Status |
| --- | --- | --- | --- |
| R-01 Missing source could lead to wrong problem | Unassessed / high | Owner narrative captured as E-001; independent validation remains R-04 / PM | Source gap resolved 2026-09-13 |
| R-02 Single developer limits capacity/support | Unassessed / unassessed | Agree availability and estimates / both | Open |
| R-03 Design/code drifts from approved intent | Unassessed / unassessed | Traceability and renewed affected approvals / both | Open |
| R-04 Existing products already satisfy target users | Unassessed / high | Validate local competitor gaps with users / PM | Open |
| R-05 Ordinary Android app cannot support proposed SIM voice flow | Material documented constraint / high | Prove supported routing and takeover before design commitment / developer | Open |
| R-06 Genuine caller misclassified or lost during takeover | Unassessed / high | Unknown state, error metrics, recovery and handoff tests / both | Open |
| R-07 Reputation/training data unavailable or unfit | Unassessed / high | Establish rights, regional coverage, labels and leakage-resistant evaluation / both | Open |
| R-08 Long agent conversations create cost and privacy burden | Unassessed / unassessed | Define engagement policy, retention and country-specific review before pilot / PM | Open |

Assumption A-01: a software change may be worthwhile. Unvalidated; both assess through research and non-build alternatives by G03.

| Question | Owner | Needed by | Answer |
| --- | --- | --- | --- |
| Q-01 Exact pain-point source? | PM | G01 | Resolved: owner narrative E-001 |
| Q-02 Users and validation access? | PM | G02 | Android users identified broadly; recruitment pending |
| Q-03 Budget, availability, timing? | PM | G03 | Pending |
| Q-04 Platform, data, privacy constraints? | Both | G03 | Pending |
| Q-05 GitHub repository and accounts? | PM | LLD handoff | Pending |
| Q-06 First country, languages, devices, and carriers? | PM | G01/G02 | Asked; pending. Do not infer from owner's timezone |
| Q-07 Meaning of counteract: short screening/end call, extended engagement, or compare both? | PM | G02 | Asked; pending. No handling policy selected |
| Q-08 Must takeover use native SIM audio, or is in-app VoIP acceptable? Is carrier forwarding acceptable? | PM | G03 | Pending route investigation |
| Q-09 What user tolerance for missed genuine calls, cloud audio, and subscription cost? | PM / users | G02/G03 | Pending user research |

Preserve resolved entries with evidence and decision links.

## 12. Guidance and tailoring

Public guidance consulted in the initial pack on 2026-09-13: [Google Design Sprint](https://designsprintkit.withgoogle.com/methodology), [Google discovery methods](https://designsprintkit.withgoogle.com/methodology/phase1-understand), [Microsoft Cloud Adoption Framework](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/), [Microsoft work tracking](https://learn.microsoft.com/en-us/azure/devops/boards/get-started/plan-track-work?view=azure-devops), and [Microsoft SDL](https://learn.microsoft.com/en-us/compliance/assurance/assurance-microsoft-security-development-lifecycle).

These informed discovery, outcome-led planning, visible work, and early security consideration. This exact document sequence and approval process are tailored to the owner, not a universal Google/Microsoft standard or an ISO compliance claim. No cloud provider or formal Scrum process is mandated.

## 13. Change history

| Date | Revision | Change | Approval implication |
| --- | --- | --- | --- |
| 2026-09-13 | 0.1 | Separate discovery, feasibility, and governance templates | All phase approvals pending |
| 2026-09-13 | 0.2 | Consolidated living plan; owner-requested BRD/options/SDD/FRD/HLD/LLD sequence and LLD handoff | Records process instructions; no product phase approved |
| 2026-09-13 | 0.3 | Captured Android use case; added cited competitor landscape, ten repository candidates with license/activity snapshot, Android constraints, data gaps, and proposed feasibility experiments | Desk research authorized by owner; discovery/research gates still pending; no stack selected or code integrated |
