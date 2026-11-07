# Security Policy

**DFerreira-pro | Repository Security & Coordinated Vulnerability Disclosure**

![Security Policy](https://img.shields.io/badge/SECURITY%20POLICY-09485A?style=flat-square) ![Coordinated Disclosure](https://img.shields.io/badge/COORDINATED%20DISCLOSURE-09485A?style=flat-square) ![Private Reporting](https://img.shields.io/badge/PRIVATE%20REPORTING-09485A?style=flat-square)

This policy applies to public source code, scripts, documentation and releases under `DFerreira-pro`. Repository-specific security policies may establish additional or stricter requirements. Publication does not authorize testing of customer, third-party or production environments.

---

## 1. Private Vulnerability Reporting

**Report suspected vulnerabilities privately through the affected repository's GitHub security advisory interface.**

1. Open the affected repository and navigate to **Security / Advisories**.
2. Select **Report a vulnerability**, where private vulnerability reporting is enabled.
3. Provide a sanitized report using the criteria in Section 2.

When private reporting is unavailable, open a public Issue requesting a secure reporting channel **without disclosing the vulnerability, exploit details, credentials or protected data**. Do not send sensitive reports through unrelated personal or business channels.

![Attention — review required](https://raw.githubusercontent.com/DFerreira-pro/.github/main/assets/attention.png)

**Do not publish exploitable findings in Issues, Discussions, Pull Requests or comments before coordinated disclosure.**

## 2. Report Content & Evidence

Include sufficient information for an authorized, reproducible assessment:

- Affected repository, component, version, release or commit.
- Vulnerability description and plausible security impact.
- Preconditions, privileges, configuration assumptions and exposure conditions.
- Minimal, non-destructive reproduction steps or a sanitized proof of concept.
- Relevant redacted logs, screenshots and supporting evidence.
- Known mitigations, potential fixes and any earlier public disclosure.

Never attach active credentials, private keys, production databases, customer information or unredacted internal configurations. Arrange an appropriate secure transfer method before sharing evidence that cannot be safely sanitized.

## 3. Scope & Support Boundaries

| Area | Policy scope |
| :--- | :--- |
| **Published source and scripts** | Vulnerabilities introduced by the repository's own code and configurations. |
| **Infrastructure automation** | Insecure defaults, excessive privileges, secret exposure and unsafe deployment behavior in published artifacts. |
| **Governance and assessment tools** | Unauthorized access, integrity failures and confidential-data exposure in published implementations. |
| **Documentation and examples** | Materially unsafe instructions or exposed sensitive configuration. |
| **Third-party dependencies** | Report upstream defects to their maintainers; report unsafe use introduced by this repository here. |
| **Customer, private or production systems** | Outside scope. No authorization for testing or disclosure is granted. |

Maintenance commitments apply only to versions expressly designated as supported by the relevant repository. Otherwise, reports are reviewed on a best-effort basis; no response-time or remediation SLA is established.

## 4. Coordinated Disclosure Procedure

Apply the following process to actionable reports, proportionate to their severity and available evidence:

| Stage | Required activity |
| :--- | :--- |
| **Intake** | Register the private report and determine whether sufficient information is available. |
| **Triage** | Establish scope, reproducibility, exploitability and impact. |
| **Containment** | Identify restrictions or interim mitigations where warranted. |
| **Remediation** | Prepare a targeted code, configuration or documentation correction. |
| **Validation** | Test the correction and relevant regression scenarios. |
| **Disclosure** | Coordinate advisories or release notes after evaluating residual risk and patch availability. |
| **Closure** | Record resolution, unresolved limitations and follow-up actions. |

Do not publish technical exploitation details before appropriate containment or mitigation has been considered. Coordinate disclosure timing according to impact, exploitability and safety; do not imply a fixed remediation deadline.

## 5. Severity & Prioritization

Assess impact in context, including confidentiality, integrity, availability, required privileges, attack complexity, network exposure and realistic deployment conditions. Use CVSS where suitable; a scanner score alone does not determine priority.

| Severity | Handling requirement |
| :--- | :--- |
| **Critical** | Restrict disclosure, assess immediate containment and prioritize remediation. |
| **High** | Prioritize investigation, mitigation and corrective planning. |
| **Medium** | Validate impact and schedule risk-based corrective action. |
| **Low / Informational** | Address through documentation, hardening or maintenance planning. |

![Critical — stop and remediate](https://raw.githubusercontent.com/DFerreira-pro/.github/main/assets/critical.png)

**Suspend release or deployment** when active credential exposure, unauthorized disclosure, a credible critical exploitation path or equivalent severe risk is confirmed. Revoke or rotate compromised credentials; removing them from the latest revision does not eliminate them from Git history.

## 6. Authorized Research & Safe Testing

- Test only systems owned by the researcher or explicitly authorized for assessment.
- Use isolated environments and synthetic data whenever practical.
- Avoid disrupting services, collecting unrelated data, establishing persistence, or accessing privileges beyond the authorized test.
- Minimize, sanitize and protect evidence; stop immediately if unexpected sensitive information is encountered.
- Report findings privately through the designated channel.

**No bug bounty, monetary reward, authorization to test third-party systems or legal safe-harbor commitment is established by this policy.**

## 7. Secure Development & Release Controls

Apply the following safeguards according to project risk:

- **Secrets:** store credentials outside the repository; inspect committed files and history before publication.
- **Access:** enforce least privilege for accounts, tokens, applications and GitHub Actions.
- **Dependencies:** evaluate advisories and validate compatibility before accepting security updates.
- **Change authorization:** retain owner control of merge, release and deployment decisions.
- **Supply chain:** verify external downloads and dependencies where feasible; avoid untrusted remote execution.
- **Infrastructure:** document platform requirements, privileges, changes, service exposure, verification and recovery.
- **Privacy:** sanitize logs, screenshots, example data, author metadata and Git history.
- **AI-assisted work:** subject generated code and configurations to the same review and validation as other contributions.

A successful test, published README or release badge does not constitute certification or approval for production use.

## 8. Sensitive Data Exposure & Incident Response

On suspected disclosure or incident:

1. Contain access and prevent further distribution where practical.
2. Revoke or rotate affected secrets immediately when appropriate.
3. Determine exposure, impacted systems, customers and third parties.
4. Remediate active files and inspect prior commits, branches, forks, caches and derived artifacts.
5. Preserve necessary evidence securely and assess legal, contractual and regulatory duties.
6. Authorize external communication only after evaluating the risk and corrective measures.

History rewriting does not guarantee deletion of objects retained by a hosting provider or copied by third parties. Escalate residual exposure through the appropriate platform support process.

## 9. Policy Authority & Exceptions

**Repository owner:** [DFerreira-pro](https://github.com/DFerreira-pro)

Apply the repository-specific `SECURITY.md` whenever it defines requirements for the affected project. Record exceptions with approval, justification, limited scope, residual risk and review conditions. Exceptions do not override legal obligations, third-party rights or access authorization requirements.

Document updates through normal version control and apply the current policy to new reports.

---

**Professional website:** [Linksafe TI](https://linksafe.com.br)  
**Reference:** [GitHub | Privately reporting vulnerabilities](https://docs.github.com/en/code-security/how-tos/report-and-fix-vulnerabilities/report-privately)
