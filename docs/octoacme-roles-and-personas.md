# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## Business Analysts

### Role Summary
Business Analysts bridge the gap between stakeholders and technical teams. They elicit, analyze, and document requirements, ensuring that solutions align with business needs and deliver value.

### Responsibilities
- Elicit and document business requirements from stakeholders
- Analyze business needs and translate them into functional specifications
- Validate deliverables against documented requirements
- Facilitate requirements workshops and stakeholder interviews
- Maintain requirements traceability and change management
- Work with Product Managers to define business problems
- Collaborate with Developers to assess feature feasibility

### Goals
- Ensure alignment between business objectives and technical solutions
- Reduce rework through clear, validated requirements
- Improve stakeholder satisfaction and project outcomes

### Typical Communication
- Requirements documentation and functional specifications
- Stakeholder workshops and validation sessions
- Regular sync meetings with Product and Development teams
- Requirements traceability matrices and impact analyses

---

## UX Designers

### Role Summary
UX Designers own the user experience and interface design, ensuring products are intuitive, accessible, and delightful. They advocate for users throughout the product development lifecycle.

### Responsibilities
- Design user experiences and interfaces that meet user needs
- Conduct user research and usability testing
- Document user flows, wireframes, and prototypes
- Collaborate with Product teams to prioritize design initiatives
- Support Developers through design specifications and reviews
- Maintain design systems and style guides
- Validate implementations against design standards

### Goals
- Create intuitive, accessible user experiences
- Reduce user friction and support costs
- Ensure consistent design language across products

### Typical Communication
- Design specifications, wireframes, and prototypes
- Usability test results and user research findings
- Design review sessions with Development teams
- Design system documentation and guidelines

---

## QA Leads

### Role Summary
QA Leads develop and coordinate the quality assurance strategy, ensuring products meet quality standards before release. They manage testing processes, automation, and defect resolution.

### Responsibilities
- Develop and maintain the overall QA strategy and test plans
- Coordinate test execution across manual and automated testing
- Manage test automation frameworks and continuous integration
- Ensure defect tracking, prioritization, and resolution
- Define quality metrics and acceptance criteria
- Collaborate with Developers to scope testable features
- Support Project Managers with QA progress reporting and risk assessment

### Goals
- Prevent defects from reaching production
- Improve test coverage and automation efficiency
- Reduce time-to-market while maintaining quality standards

### Typical Communication
- Test plans, test cases, and automation reports
- Defect reports and quality metrics dashboards
- QA status updates in sprint planning and standups
- Risk assessments and release readiness reports

---

## Security Champion

### Role Summary
Security Champions are embedded within development teams to advocate for secure software practices throughout the development lifecycle. They serve as the primary point of contact for security concerns, bridging the gap between security teams and engineering, and ensuring security is a shared responsibility rather than an afterthought.

### Responsibilities
- Promote and enforce secure coding standards and practices within the team
- Conduct threat modeling and security risk assessments for new features and architecture changes
- Review pull requests for security vulnerabilities and advise on remediation
- Coordinate with external security teams on penetration testing, audits, and compliance reviews
- Track security findings and manage remediation progress through to closure
- Maintain and communicate the security incident runbook
- Stay current with CVEs, emerging threats, and security tooling relevant to the product
- Facilitate security awareness sessions and share findings with the broader team

### Goals
- Prevent security vulnerabilities from reaching production
- Reduce mean time-to-remediation for security findings
- Embed a security-first culture across engineering and product teams

### Typical Interactions
- **Developers**: Provide secure coding guidance during code reviews and architectural design discussions
- **QA Leads**: Coordinate integration of security testing (SAST, DAST, dependency scanning) into CI/CD pipelines
- **DevOps Engineers**: Define and enforce security controls in deployment pipelines and infrastructure
- **Product Managers**: Advise on security requirements and trade-offs for new features
- **Project Managers**: Report security risks and remediation timelines; escalate critical findings to appropriate stakeholders

### Typical Communication
- Security review comments in pull requests and design docs
- Threat models and security assessment reports
- Vulnerability reports and remediation tracking dashboards
- Incident response runbooks and post-mortem summaries
- Security awareness updates and team brown-bag sessions

### Security Review Checklist
Use this checklist when reviewing features or releases for security readiness:

- [ ] Threat model completed for new features or architecture changes
- [ ] Static code analysis (SAST) passed with no critical findings
- [ ] Dependency vulnerability scan completed; known CVEs assessed and accepted or remediated
- [ ] Secrets and credentials are not hardcoded; secrets management solution is in use
- [ ] Authentication and authorization controls validated
- [ ] Input validation and output encoding reviewed for injection vulnerabilities
- [ ] Sensitive data handling reviewed (encryption at rest and in transit)
- [ ] Security findings from previous audits or penetration tests reviewed and addressed
- [ ] Incident response runbook updated if new attack surface introduced

> See also: [Cross-Functional Engagement Checklists](./octoacme-cross-functional-checklists.md)

---

## DevOps Engineer

### Role Summary
DevOps Engineers build and maintain the infrastructure, tooling, and processes that enable teams to deliver software reliably and continuously. They bridge development and operations by automating pipelines, managing environments, and ensuring system observability and reliability.

### Responsibilities
- Design, build, and maintain CI/CD pipelines and deployment automation
- Manage infrastructure provisioning and configuration using infrastructure-as-code (IaC)
- Monitor system health, performance, availability, and set up alerting
- Define and maintain environment standards (development, staging, production)
- Manage secrets, access controls, and environment-specific configuration
- Respond to and resolve infrastructure and deployment incidents
- Support teams with debugging environment, deployment, and reliability issues
- Contribute to and maintain the deployment runbook and rollback procedures

### Goals
- Maximize deployment frequency while maintaining reliability and safety
- Reduce mean time to recovery (MTTR) for production incidents
- Automate repetitive operational tasks to reduce toil and human error

### Typical Interactions
- **Developers**: Enable fast, safe deployments; support debugging of environment and configuration issues
- **Security Champions**: Integrate security scanning, secrets management, and access controls into pipelines
- **QA Leads**: Maintain test environments and enable automated test execution within CI/CD
- **Project Managers**: Communicate deployment readiness, infrastructure risks, and release window requirements
- **Product Managers**: Support release planning with deployment timelines, risk assessments, and environment capacity

### Typical Communication
- CI/CD pipeline status reports and deployment notifications
- Infrastructure-as-code documentation and environment runbooks
- Incident reports, post-mortem analyses, and action items
- Monitoring dashboards and alerting configuration documentation
- Deployment checklists and release readiness sign-offs

### Deployment Readiness Checklist
Use this checklist before promoting a release to production:

- [ ] All CI checks passing (unit tests, integration tests, security scans)
- [ ] Infrastructure changes reviewed and applied to staging successfully
- [ ] Environment configuration and secrets validated for the target environment
- [ ] Monitoring and alerting configured for new features or services
- [ ] Rollback plan documented and tested
- [ ] Deployment window scheduled and communicated to stakeholders
- [ ] On-call engineer identified and available during deployment window
- [ ] Post-deployment smoke tests defined and ready to execute
- [ ] Release notes reviewed and approved

> See also: [Release and Deployment](./octoacme-release-and-deployment.md) | [Cross-Functional Engagement Checklists](./octoacme-cross-functional-checklists.md)

---

## Customer Support Lead

### Role Summary
Customer Support Leads serve as the voice of the customer within the product team. They manage support operations, synthesize user feedback, and ensure customer issues are resolved efficiently and fed back into the product improvement cycle. They are a critical link between real-world product usage and the teams building the product.

### Responsibilities
- Manage and triage incoming customer support requests and escalations
- Track, categorize, and route bugs and feature requests sourced from customers
- Synthesize customer feedback into actionable insights for Product and Engineering teams
- Define, monitor, and report on support SLAs and customer satisfaction metrics (CSAT, NPS)
- Create and maintain self-service support documentation, FAQs, and knowledge base articles
- Collaborate with Product Managers to ensure high-impact customer issues are prioritized on the roadmap
- Coordinate with Developers and QA on bug triage, reproduction steps, and resolution timelines
- Communicate release updates, known issues, and workarounds to affected customers

### Goals
- Achieve high customer satisfaction and first-contact resolution rates
- Reduce recurring support tickets through product improvements and better self-service documentation
- Ensure customer feedback consistently informs the product roadmap and quality improvements

### Typical Interactions
- **Product Managers**: Share customer feedback trends, usage patterns, and escalate high-impact feature gaps or bugs
- **Developers**: Report and triage bugs with reproduction steps; validate fixes before customer communication
- **QA Leads**: Flag recurring defects and edge cases discovered through customer-reported issues
- **Project Managers**: Provide customer impact input during release planning, go/no-go decisions, and incident management
- **Business Analysts**: Collaborate on translating customer feedback patterns into formal requirements
- **Data Analysts**: Share support volume data for trend analysis and product health dashboards

### Typical Communication
- Weekly support ticket summaries and trend reports shared with Product and Engineering
- Customer satisfaction (CSAT/NPS) dashboards and monthly reports
- Bug reports with reproduction steps and customer impact severity
- Customer feedback digests in sprint planning or product review meetings
- Release notes, known issue communications, and customer-facing workaround documentation

### Customer Feedback Flow
The following process ensures customer insights are captured and actioned:

1. **Capture**: Customer contacts support via ticket, chat, or feedback form
2. **Categorize**: Tag as Bug, Feature Request, Documentation Gap, or Question
3. **Triage**: Assess severity and customer impact; escalate critical issues immediately
4. **Route**: Send bugs to Developers/QA with reproduction steps; send feature requests to Product Manager
5. **Track**: Log all items in the backlog or issue tracker with customer impact noted
6. **Close the Loop**: Notify the customer when their issue is resolved or their feedback is actioned
7. **Report**: Include trends in weekly digest and monthly stakeholder reports

> See also: [Cross-Functional Engagement Checklists](./octoacme-cross-functional-checklists.md)

---

## Data Analyst

### Role Summary
Data Analysts enable data-driven decision making by collecting, analyzing, and visualizing product and business data. They work across teams to surface insights that inform strategy, improve processes, and measure outcomes—ensuring that key decisions are grounded in evidence rather than intuition.

### Responsibilities
- Define, instrument, and maintain product metrics, KPIs, and OKRs in collaboration with stakeholders
- Build and maintain dashboards and automated reports for leadership and cross-functional teams
- Analyze user behavior, feature adoption, funnel performance, and business outcomes
- Collaborate with Product Managers to define and track success metrics for new features
- Identify trends, anomalies, and opportunities from product and operational data
- Ensure data quality, integrity, and consistency across tracking and analytics pipelines
- Design, execute, and analyze A/B tests and experiments
- Support self-service analytics by documenting data models and metrics definitions

### Goals
- Ensure product and business decisions are grounded in reliable, timely data
- Improve visibility into product performance, user outcomes, and operational health
- Reduce time-to-insight for key stakeholders across the organization

### Typical Interactions
- **Product Managers**: Define and track feature success metrics; inform roadmap prioritization with usage and outcome data
- **Developers**: Specify instrumentation requirements for new features; validate tracking implementations
- **Business Analysts**: Align on requirements definitions, KPI frameworks, and success criteria
- **Project Managers**: Provide data on delivery velocity, cycle time, and outcome metrics for stakeholder reporting
- **Customer Support Leads**: Analyze support ticket volume and trends to identify systemic product issues

### Typical Communication
- Metrics dashboards and automated reports for sprint reviews and stakeholder briefings
- A/B test results, experiment summaries, and recommendation reports
- Feature instrumentation specifications shared with Developers
- Data quality reports and anomaly alerts
- Insights presentations and data-driven recommendations in product reviews

### Metrics and Outcomes Checklist
Use this checklist when defining or reviewing feature metrics:

- [ ] Success metrics defined and agreed with Product Manager before development begins
- [ ] Baseline measurements captured for comparison post-launch
- [ ] Instrumentation plan reviewed with Developers and included in feature definition
- [ ] Data pipeline and tracking validated in staging before release
- [ ] Dashboard or report created for ongoing monitoring
- [ ] A/B test hypothesis documented (if applicable): control, variant, expected effect size, and duration
- [ ] Results reviewed against success metrics within agreed timeframe post-launch
- [ ] Insights and recommendations documented and shared with stakeholders

> See also: [Cross-Functional Engagement Checklists](./octoacme-cross-functional-checklists.md)

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- Cross-functional roles (Security Champion, DevOps Engineer, Customer Support Lead, Data Analyst) address gaps in security oversight, deployment reliability, user feedback integration, and data-driven decision making.
- Formal definitions for these roles reduce tribal knowledge and clarify handoffs, escalation paths, and accountability boundaries.

