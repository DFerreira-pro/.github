# Security Policy

**DFerreira-pro | Repository Security & Coordinated Vulnerability Disclosure**

![Security Policy](https://img.shields.io/badge/SECURITY%20POLICY-09485A?style=flat-square) ![Coordinated Disclosure](https://img.shields.io/badge/COORDINATED%20DISCLOSURE-09485A?style=flat-square) ![Private Reporting](https://img.shields.io/badge/PRIVATE%20REPORTING-09485A?style=flat-square)

This document defines the default vulnerability reporting and handling policy for public repositories maintained by **DFerreira-pro**, unless an individual repository provides a more specific `SECURITY.md`. It applies to publicly released source code, scripts, documentation and other published project artifacts. It does **not** authorize testing of third-party, customer or production systems.

---

## 1. Security Reporting Channel

**Report suspected vulnerabilities privately, using the affected repository's GitHub security advisory interface.**

1. Open the affected repository.
2. Select **Security and quality → Advisories → Report a vulnerability** (the exact labels may vary).
3. Submit the report privately, with the information described below.

GitHub's private vulnerability reporting feature must be enabled for the affected repository for this channel to be available. If it is unavailable, open a **non-sensitive** issue asking the maintainer to establish a private reporting channel. **Do not include vulnerability details, exploit code, credentials or customer data in that public issue.**

![Attention: Review Required](https://raw.githubusercontent.com/DFerreira-pro/.github/main/assets/attention.png)

**Do not report exploitable vulnerabilities in public Issues, Discussions, Pull Requests or comments before coordinated disclosure.** Avoid contacting maintainers through unrelated personal or business channels.

## 2. What to Include in a Private Report

Provide enough detail to support a secure and reproducible assessment:

- Affected repository, component, version, release or commit identifier.
- Clear vulnerability summary and its potential security impact.
- Preconditions, required privileges, affected configurations and assumed threat model.
- Minimal, non-destructive reproduction steps or a sanitized proof of concept.
- Relevant logs, screenshots and evidence with secrets and personal data redacted.
- Suggested mitigation or remediation, if available.
- Whether the issue may already have been publicly disclosed or actively exploited.

Do not upload live credentials, production databases, customer data, private keys or unredacted internal configurations. If such evidence is essential, request a secure transfer arrangement first.

## 3. Scope and Support Boundaries

| Area | Scope |
| --- | --- |
| Public code and automation | Security weaknesses introduced by code published in the affected repository. |
| Deployment and operational scripts | Unsafe defaults, privilege misuse, credential exposure or insecure execution attributable to the published artifacts. |
| Governance and assessment tools | Vulnerabilities affecting data handling, confidentiality, integrity or authorization within published implementations. |
| Examples and documentation | Materially unsafe guidance or examples that could reasonably lead to insecure deployment. |
| Third-party platforms and dependencies | Report upstream vulnerabilities to the appropriate vendor or maintainer; report repository-specific insecure use here. |
| Customer systems and private environments | **Out of scope.** No permission to test or disclose these systems is granted. |

A public repository does not imply that all past releases, experimental branches or third-party dependencies receive ongoing security support. Supported versions, when applicable, are defined in each project's release notes or repository-specific security policy. Where no supported-version statement exists, reports will be evaluated on a best-effort basis.

## 4. Coordinated Disclosure Process

The maintainer aims to handle valid reports through the following stages:

1. **Intake:** receive the private report and confirm that sufficient information is available.
2. **Triage:** assess reproducibility, affected scope, exploitability and impact.
3. **Containment:** identify short-term mitigations when appropriate.
4. **Remediation:** prepare and review a targeted fix or documentation correction.
5. **Validation:** test the correction and check for regressions.
6. **Disclosure:** coordinate a security advisory, patch notes or public notice when justified and safe.
7. **Closure:** document decisions and any follow-up controls.

There is **no guaranteed response or remediation service-level agreement** for these independently maintained projects. Reasonable efforts will be made to acknowledge actionable reports and communicate material updates. Disclosure timing should be coordinated based on severity, exploitability, patch availability and potential harm.

## 5. Severity and Prioritization

Severity is evaluated using context, not solely a scanner score. Relevant factors include confidentiality, integrity, availability, required privileges, attack complexity, exposure, exploit maturity and realistic deployment conditions. CVSS may be used when appropriate, but is not mandatory.

| Classification | Typical handling |
| --- | --- |
| Critical | Immediate risk review; restrict disclosure and prioritize containment or correction. |
| High | Prioritized investigation and remediation planning. |
| Medium | Scheduled validation and risk-based correction. |
| Low / Informational | Documentation, hardening or backlog treatment as appropriate. |

![Critical: Stop and Remediate](https://raw.githubusercontent.com/DFerreira-pro/.github/main/assets/critical.png)

**Stop public release or deployment of affected artifacts when active credential exposure, unauthorized data disclosure, a credible critical exploit path or an equivalent severe risk is confirmed.** Revoke or rotate compromised credentials promptly; removing them from a current file alone does not remove them from Git history.

## 6. Researcher Conduct and Safe Testing

Security research must remain lawful, authorized and proportionate. Reporters are requested to:

- Test only assets they own or are explicitly authorized to assess.
- Prefer isolated environments and synthetic data.
- Avoid service disruption, persistence, privilege escalation beyond what is necessary for proof, social engineering and data exfiltration.
- Minimize data access, retain only essential sanitized evidence and protect it against disclosure.
- Stop testing and notify the maintainer privately if unintended sensitive information is encountered.

**This policy is not a bug bounty program, permission to attack systems or a promise of safe harbor.** No rewards, payments or response-time commitments are implied.

## 7. Secure Development and Release Expectations

Repository maintainers and contributors should apply security measures proportional to the project's risk:

- **Secrets:** use approved secret storage; never commit plaintext credentials, keys or tokens.
- **Least privilege:** minimize permissions for scripts, CI/CD workflows and GitHub tokens.
- **Dependencies:** review vulnerability alerts and update affected components after compatibility testing.
- **Changes:** prefer reviewed Pull Requests and protected branches where supported.
- **Supply chain:** pin or validate dependencies and external downloads when practical; avoid unverified remote execution.
- **Infrastructure automation:** document prerequisites, supported platforms, privileges, expected changes, rollback and post-deployment checks.
- **Privacy:** sanitize logs, screenshots, sample data, metadata and Git history before publishing.
- **AI-assisted work:** subject generated code and configuration to the same review and testing requirements as manually written work.

The presence of a README, badge, test script or published release **does not certify a project as production-ready**. Production suitability must be independently evaluated for the intended environment.

## 8. Handling Sensitive Information and Security Incidents

If sensitive material is accidentally committed or a credible security issue is identified:

1. Limit further distribution and restrict affected access where possible.
2. Revoke or rotate exposed secrets immediately when applicable.
3. Assess whether customers, third parties or production assets could be impacted.
4. Remediate the current repository and investigate Git history, forks, caches and derivative artifacts.
5. Preserve necessary evidence securely and follow legal, contractual or regulatory notification obligations where applicable.
6. Coordinate any public statement or advisory only after risk assessment.

History rewriting may not remove content already copied or retained by hosting platforms or third parties. Escalate unresolved sensitive-data retention to the relevant platform support channel.

## 9. Policy Ownership and Exceptions

**Maintainer:** [DFerreira-pro](https://github.com/DFerreira-pro)

This is the default security policy. Individual repositories may define more specific supported versions, reporting procedures and technical requirements. The more specific repository policy takes precedence where applicable.

Changes to this policy are versioned through Git. Exceptions should be justified, limited in scope and reviewed before adoption; a documented exception does not waive applicable legal, contractual or security obligations.

---

**Professional website:** [Linksafe TI](https://linksafe.com.br)  
**Reference:** [GitHub documentation | privately reporting vulnerabilities](https://docs.github.com/en/code-security/how-tos/report-and-fix-vulnerabilities/report-privately)
