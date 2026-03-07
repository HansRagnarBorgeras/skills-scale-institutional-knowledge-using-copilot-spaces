# OctoAcme Cross-Functional Engagement Checklists

This document provides practical checklists and process guides to support stakeholder engagement, customer feedback flow, and measurable outcomes for cross-functional roles. It is a companion to [OctoAcme Personas](./octoacme-roles-and-personas.md).

---

## Stakeholder Engagement Checklist

Use this checklist to ensure all relevant cross-functional roles are engaged at each project phase.

### Project Initiation
- [ ] Security Champion consulted on security and compliance requirements
- [ ] DevOps Engineer consulted on infrastructure needs, environment setup, and deployment approach
- [ ] Customer Support Lead consulted on known customer pain points and open issues
- [ ] Data Analyst consulted on existing metrics baseline and instrumentation gaps
- [ ] All new roles added to the stakeholder list and communication plan

### Sprint Planning
- [ ] Security Champion flagged any outstanding security findings that affect scope or priority
- [ ] DevOps Engineer confirmed environment availability and pipeline readiness
- [ ] Customer Support Lead shared top customer-reported issues for consideration
- [ ] Data Analyst confirmed success metrics are defined for new features entering the sprint

### Release / Go-No-Go Decision
- [ ] Security Champion: security review completed, no blocking findings open
- [ ] DevOps Engineer: deployment checklist signed off; rollback plan confirmed
- [ ] Customer Support Lead: known issues communicated to support team; customer-facing release notes reviewed
- [ ] Data Analyst: tracking instrumentation validated in staging; monitoring dashboard ready

### Retrospective
- [ ] Security Champion: security incidents, near-misses, or findings from the sprint reviewed
- [ ] DevOps Engineer: deployment reliability and incident metrics reviewed
- [ ] Customer Support Lead: support ticket trends and customer satisfaction scores reviewed
- [ ] Data Analyst: outcome metrics reviewed against success criteria; learnings documented

---

## Customer Feedback Flow

This process ensures that customer insights captured by the Customer Support Lead are efficiently routed and actioned across the team.

```
Customer Contact
       │
       ▼
  [Customer Support Lead]
  Capture & Categorize
  (Bug | Feature Request | Doc Gap | Question)
       │
       ├──── Bug ──────────────────► [Developers + QA Lead]
       │                              Triage, reproduce, fix
       │                              Notify customer on resolution
       │
       ├──── Feature Request ──────► [Product Manager]
       │                              Evaluate against roadmap
       │                              Feed into backlog prioritization
       │
       ├──── Doc Gap ──────────────► [Customer Support Lead]
       │                              Update knowledge base / FAQs
       │
       └──── Trend / Pattern ──────► [Data Analyst + Product Manager]
                                      Analyze volume and impact
                                      Inform roadmap and OKRs
```

### Feedback Loop SLA Targets

| Category       | Initial Response | Resolution Target |
|----------------|-----------------|-------------------|
| Critical Bug   | 2 hours          | 1 business day    |
| Major Bug      | 4 hours          | 3 business days   |
| Feature Request | 1 business day  | Backlog within 1 sprint |
| Documentation  | 1 business day   | 2 business days   |

---

## Measurable Outcomes by Role

Use the following targets to track and assess the effectiveness of each cross-functional role. Review quarterly or during retrospectives.

### Security Champion
| Metric | Target |
|--------|--------|
| Critical/High vulnerabilities open > 30 days | 0 |
| Security review participation rate (PRs/designs) | 100% of high-risk changes |
| Mean time to remediate high vulnerabilities | ≤ 14 days |
| Security incidents caused by known vulnerabilities | 0 |

### DevOps Engineer
| Metric | Target |
|--------|--------|
| Deployment success rate | ≥ 99% |
| Mean time to recovery (MTTR) for production incidents | ≤ 2 hours |
| Deployment frequency | ≥ 1 per week per team |
| Change failure rate | ≤ 5% |

### Customer Support Lead
| Metric | Target |
|--------|--------|
| Customer Satisfaction Score (CSAT) | ≥ 85% |
| First-contact resolution rate | ≥ 70% |
| Average ticket resolution time | ≤ 3 business days |
| Customer-reported bugs escalated to engineering within SLA | 100% |

### Data Analyst
| Metric | Target |
|--------|--------|
| Features shipped with instrumentation on day 1 | 100% |
| Dashboard/report freshness (data lag) | ≤ 24 hours |
| Success metrics defined before feature enters development | 100% |
| Stakeholder satisfaction with data availability | ≥ 80% (survey) |

---

## Cross-Functional RACI Summary

The table below clarifies accountability for key activities across all personas.

| Activity | Developer | PM | PdM | BA | UX | QA Lead | Security Champion | DevOps Eng | Support Lead | Data Analyst |
|---|---|---|---|---|---|---|---|---|---|---|
| Define success metrics | I | A | R | C | I | I | I | I | C | C |
| Security review | C | I | I | I | I | C | R/A | C | - | - |
| Deployment sign-off | I | I | I | - | - | C | C | R/A | I | I |
| Customer feedback triage | - | I | C | C | - | C | - | - | R/A | C |
| Release notes | C | A | C | - | - | C | C | C | R | - |
| Retrospective action items | C | A | C | C | C | C | C | C | C | C |
| Instrumentation spec | R | C | C | - | - | - | - | - | - | A |

**Key**: R = Responsible, A = Accountable, C = Consulted, I = Informed

---

> Related docs: [Roles and Personas](./octoacme-roles-and-personas.md) | [Release and Deployment](./octoacme-release-and-deployment.md) | [Risks and Communication](./octoacme-risks-and-communication.md) | [Retrospective and Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md)
