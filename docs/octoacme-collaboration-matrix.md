# OctoAcme — Cross-Functional Collaboration & Decision-Making Matrix

## Purpose
Provide a clear reference for how different personas collaborate, who has decision authority, and how to resolve ambiguity across the project management lifecycle.

## Decision Authority Matrix

| Decision | Owner | Consulted | Informed |
|----------|-------|-----------|----------|
| **Project Approval** | Sponsor | Product Manager, Project Manager | Team |
| **Scope Changes** | Sponsor + PM | Technical Lead, QA Lead | Developers, Business Analyst |
| **Feature Prioritization** | Product Manager | Sponsor, Project Manager | Business Analyst, Team |
| **Architecture & Technology** | Technical Lead | Product Manager, Project Manager | Developers, QA Lead |
| **Release Timing** | Project Manager | Sponsor, Tech Lead, QA Lead | Product Manager, Team |
| **Quality Standards** | QA Lead | Technical Lead, Developers | Product Manager, PM |
| **Resource Allocation** | Sponsor + PM | Project Manager | Team |
| **Risk Mitigation** | Project Manager | Sponsor, Tech Lead | All Roles |
| **Acceptance Criteria** | Product Manager + BA | Developers, QA Lead | Team |
| **Definition of Done** | Team + Scrum Master | Technical Lead, QA Lead | Project Manager |

---

## Collaboration Models by Lifecycle Phase

### Initiation Phase

**Primary Personas:** Sponsor, Product Manager, Project Manager, Business Analyst

**Collaboration Activities:**
- Sponsor defines strategic intent and business case
- Business Analyst gathers initial requirements from stakeholders
- Product Manager develops problem statement and success metrics
- Project Manager creates high-level timeline and resource estimate
- Team (optional): Engineering input on feasibility

**Key Output:** Project Charter / One-pager

**Communication:** Kickoff meeting to align all stakeholders

---

### Planning Phase

**Primary Personas:** Product Manager, Project Manager, Technical Lead, Business Analyst, Scrum Master

**Collaboration Activities:**
- Business Analyst refines requirements into user stories
- Product Manager finalizes backlog and prioritization
- Technical Lead designs solution architecture and identifies technical risks
- QA Lead defines test strategy and acceptance criteria validation approach
- Project Manager creates detailed schedule and dependency map
- Scrum Master defines sprint cadence and ceremony schedule
- Team: Participates in planning, story refinement, and estimation

**Key Output:** Detailed backlog, architecture design, release plan, risk register

**Communication:** Planning meeting, backlog refinement sessions, design reviews

---

### Execution Phase

**Primary Personas:** Developers, QA Lead, Technical Lead, Scrum Master, Business Analyst

**Collaboration Activities:**
- **Daily:** Scrum Master facilitates standup, team reports progress and blockers
- **During Sprint:** 
  - Developers implement features, participate in design reviews
  - QA Lead executes testing, reports defects, validates acceptance criteria
  - Technical Lead reviews code and design decisions
  - Business Analyst answers requirement questions, coordinates with stakeholders
  - Scrum Master removes blockers, facilitates collaboration
- **Mid-Sprint:** Scrum Master assesses progress, Project Manager flags risks
- **Sprint End:** Scrum Master facilitates review and retrospective

**Key Output:** Working software, test results, sprint metrics

**Communication:** Daily standups, PR reviews, testing reports, weekly syncs

---

### Release & Deployment Phase

**Primary Personas:** Project Manager, QA Lead, Technical Lead, Product Manager, Sponsor

**Collaboration Activities:**
- QA Lead confirms release readiness (all tests passing, coverage acceptable)
- Technical Lead approves technical readiness (performance, security, stability)
- Product Manager confirms feature completeness against user value
- Project Manager confirms dependencies resolved, rollback plan ready
- Sponsor (for major releases) provides final go/no-go approval
- Business Analyst prepares release notes and stakeholder communication
- Developers on-call for deployment support

**Key Output:** Production release, release notes, stakeholder communication

**Communication:** Release readiness review, go/no-go meeting, post-release verification

---

### Retrospective & Continuous Improvement Phase

**Primary Personas:** Scrum Master, Project Manager, Team, Technical Lead

**Collaboration Activities:**
- Scrum Master facilitates retrospective, team discusses what went well and improvements
- Project Manager captures action items and assigns owners
- Technical Lead discusses technical learnings and debt management
- QA Lead reports on quality trends and process improvements
- Business Analyst gathers feedback on requirement clarity and process
- Product Manager shares learnings on feature success and market feedback
- Sponsor (if included) provides organizational context for improvements

**Key Output:** Action items, process improvements, lessons learned documentation

**Communication:** Retrospective meeting, follow-up on action items weekly

---

## Communication Protocols by Scenario

### When Scope Changes Mid-Project

1. **Business Analyst** documents the change and impact
2. **Product Manager** evaluates priority against existing backlog
3. **Technical Lead** assesses technical feasibility and risks
4. **Project Manager** calculates timeline and resource impact
5. **Sponsor** makes final approval/rejection decision
6. **Scrum Master** communicates decision to team and adjusts sprint if needed
7. **QA Lead** updates test strategy if needed

**Decision Timeline:** 24-48 hours for most changes

---

### When a Critical Defect is Found Late in Development

1. **QA Lead** escalates defect to Scrum Master and Technical Lead with severity assessment
2. **Technical Lead** triages and determines if blockers release
3. If blocking: **Project Manager** escalates to Sponsor for go/no-go decision
4. **Developers** prioritize fix in standup
5. **QA Lead** reverifies after fix
6. **Product Manager** confirms business impact assessment
7. **Scrum Master** tracks resolution and updates risk register

**Response Time:** Same-day triage, 24-hour resolution target for blocking defects

---

### When a Team Member Identifies a Risk

1. **Team Member** reports to **Scrum Master** in standup
2. **Scrum Master** escalates to **Project Manager** same day
3. **Project Manager** adds to risk register with impact/probability assessment
4. **Project Manager** escalates to **Sponsor** if High impact and High probability
5. **Technical Lead** or **QA Lead** proposes mitigation if technical
6. **Project Manager** tracks mitigation progress weekly
7. **Team** executes mitigation actions

**Response Time:** Risk review in weekly PM sync, mitigation plan within 48 hours for high risks

---

### When Architecture Decision is Needed

1. **Technical Lead** gathers requirements from **Developers** and **Product Manager**
2. **Technical Lead** creates Architecture Decision Record (ADR) with options
3. **Technical Lead** presents options to **Team** and **QA Lead** for input
4. **Team** provides feedback on feasibility and maintainability
5. **QA Lead** assesses testing implications
6. **Technical Lead** makes final decision and documents rationale
7. Decision communicated to team in standup

**Response Time:** 3-5 business days for complex decisions, 1 day for standard decisions

---

### When Requirements Are Unclear

1. **Developer** asks **Business Analyst** during standup or in Slack
2. **Business Analyst** checks with **Product Manager** and **Stakeholders** if needed
3. **Business Analyst** clarifies in user story and acceptance criteria
4. **Developer** proceeds with confidence
5. If major clarification: **Scrum Master** flags impact to timeline
6. **Product Manager** decides if scope adjustment needed

**Response Time:** Same-day response for blocking questions, 24 hours for non-urgent clarifications

---

### When Quality Metrics are Below Threshold

1. **QA Lead** reports trend to **Technical Lead** and **Project Manager**
2. **Technical Lead** and **QA Lead** identify root causes (code quality, test design, environment)
3. **Project Manager** escalates timeline risk to **Sponsor** if applicable
4. **Team** and **Scrum Master** brainstorm improvements in retrospective
5. Action items assigned for next sprint/cycle
6. **QA Lead** tracks metrics weekly to confirm improvement

**Response Time:** Weekly quality review in PM sync, corrective action in next sprint

---

## Conflict Resolution Escalation Path

### Level 1: Team Discussion
- **Between:** Two team members (Developer + QA, Dev + Dev, etc.)
- **Facilitated by:** Scrum Master
- **Timeline:** Resolve in standup or same day
- **Example:** Disagreement on test approach, code review feedback

### Level 2: Role Leadership
- **Between:** Role leads (Tech Lead, QA Lead, Product Manager)
- **Facilitated by:** Project Manager
- **Timeline:** Resolve in 1-2 business days
- **Example:** Technical approach vs. timeline trade-off, quality standard disagreement

### Level 3: Project Leadership
- **Between:** Project Manager, Sponsor, Product Manager
- **Facilitated by:** Sponsor
- **Timeline:** Resolve in 2-3 business days
- **Example:** Scope vs. timeline vs. budget trade-off, strategy shift

### Level 4: Organizational Leadership
- **Between:** Sponsor and other organizational leaders
- **Timeline:** Resolve in 3-5 business days
- **Example:** Resource conflict across projects, organizational priority change

---

## Interaction Patterns & Frequency

| Interaction | Participants | Frequency | Duration | Purpose |
|-------------|--------------|-----------|----------|---------|
| Daily Standup | Developers, QA, Scrum Master, Tech Lead | Daily | 15 min | Progress update, blocker identification |
| PM Sync | PM, PdM, Project Manager | Weekly | 30 min | Risk, dependencies, metrics review |
| Technical Review | Tech Lead, Developers | Per feature | 30-60 min | Architecture, design, code quality |
| QA Checkpoint | QA Lead, Developers, Tech Lead | Mid-sprint | 30 min | Testing status, quality assessment |
| Backlog Refinement | PdM, BA, Developers, Tech Lead | Weekly | 60 min | User story clarity, estimation |
| Sprint Planning | Full team, Scrum Master | Sprint start | 120 min | Sprint goal, capacity, commitment |
| Sprint Review | Full team, Stakeholders | Sprint end | 60 min | Demo, feedback, metrics |
| Retrospective | Full team, Scrum Master | Sprint end | 60 min | Process improvement, action items |
| Sponsor Update | PM, Sponsor | Bi-weekly/Monthly | 30 min | Status, risks, decisions |
| Risk Review | PM, Tech Lead, QA Lead | Weekly | 30 min | Risk assessment, mitigation status |

---

## Using This Matrix

1. **At Project Start:** Share matrix with all team members to align on decision authority and collaboration patterns
2. **During Execution:** Reference when unclear who should be involved in a decision
3. **During Conflict:** Follow escalation path to resolve disagreements efficiently
4. **For New Team Members:** Use as onboarding guide to understand interaction patterns
5. **In Retrospectives:** Discuss if collaboration patterns are working and adjust as needed
