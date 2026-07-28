# Security Policy

Security researchers are essential in identifying vulnerabilities that may
impact Burnt Labs software and the XION network. If you have discovered a
security vulnerability in any repository managed by Burnt Labs, we encourage you
to report it using the process below.

We take all security reports seriously. If a report is confirmed upon
investigation, we will patch the issue within a reasonable amount of time and
publish a security bulletin describing the impact and crediting the discoverer.

> This is the organization-wide default policy. Individual repositories may
> publish their own `SECURITY.md`, which takes precedence for that repository.

## Reporting a Vulnerability

**Do not open a public GitHub issue for a security vulnerability.** Public
disclosure before a patch is available increases the harm to users.

| Type of finding                     | How to report                                         |
| ----------------------------------- | ----------------------------------------------------- |
| Security vulnerability              | Email [security@burnt.com](mailto:security@burnt.com)  |
| Non-sensitive or operational bug    | Open a GitHub issue on the affected repository         |

Where a repository has GitHub private vulnerability reporting enabled, you may
also use the **Security → Report a vulnerability** tab on that repository.

## What to Include

Please include the following to aid our assessment:

- Type of vulnerability
- Description of the vulnerability, and the affected repository and version
- Steps to reproduce the issue
- Impact of the issue, and how an attacker could exploit it
- Any potential mitigations or workarounds

### Proof of Concept

**Reports should include a proof of concept.** Severity is assessed on
demonstrated impact under real-world constraints, not theoretical worst-case
scenarios, and a finding we cannot reproduce is difficult to act on.

For findings in the chain or in on-chain contracts, an end-to-end proof of
concept is expected. Unit tests and simulated environments that bypass
transaction encoding, message routing, or the ante handler chain — including
harnesses such as `cw-multi-test` or direct keeper setup — do not on their own
demonstrate on-chain exploitability. The strongest reports execute the attack
via standard transaction broadcast against a locally running node configured
with mainnet parameters.

For findings in web properties, include screenshots or a video walkthrough
showing end-to-end exploitation. Automated scanner output without demonstrated
exploitability is not actionable.

## Response Process

1. **Acknowledgment** — we acknowledge receipt within **5 business days**
2. **Triage** — we provide a triage decision within **14 days**
3. **Investigation** — our security team confirms the vulnerability and assesses
   severity
4. **Fix development** — we develop and test a fix privately
5. **Coordination** — for critical issues we coordinate with affected parties and
   upstream projects through their non-public channels before public disclosure
6. **Community notification** — we notify the community that a security release
   is coming, so users, validators, and integrators can prepare
7. **Public disclosure** — after a fix is deployed we publish a bulletin with
   details and credit

Active exploitation, or confirmed attacker awareness of an unpatched
vulnerability, escalates the issue to Critical handling regardless of its
original classification.

Where an issue requires a network upgrade, additional time may be needed to
raise a governance proposal and complete the upgrade.

## Responsible Disclosure

We ask that you keep vulnerabilities and related communications confidential
until a fix is developed and deployed. Specifically:

- Do not exploit a vulnerability beyond what is necessary to confirm it exists
- **Do not test against production systems.** Testing that targets XION mainnet
  or live production applications will disqualify the report
- Do not access, modify, or exfiltrate user data
- Do not disrupt or degrade our networks, data, or services
- Do not disclose publicly before a fix is confirmed and deployed
- Allow us a reasonable amount of time to address the issue

## Severity Characterization

| Severity     | Description                                                                  |
| ------------ | ---------------------------------------------------------------------------- |
| **CRITICAL** | Immediate threat to critical systems (e.g. funds at risk, network compromise) |
| **HIGH**     | Significant impact on major functionality or security controls               |
| **MEDIUM**   | Impacts minor features or exposes non-sensitive data                         |
| **LOW**      | Minimal impact or informational issues                                       |

Severity is assessed by Burnt Labs based on demonstrated impact. Where a
published bug bounty program covers the affected asset, that program's terms
govern scope, severity classification, and reward eligibility.

## Scope

This policy applies to all repositories managed by Burnt Labs, including the
XION chain and its modules, smart contracts and the contract execution
environment, SDKs and client libraries, and the services and applications we
operate.

Vulnerabilities in upstream dependencies — including CosmWasm, the Cosmos SDK,
and IBC — should be reported to those projects directly.

## Safe Harbor

Burnt Labs will not pursue legal action against researchers who discover and
report vulnerabilities in good faith under this policy, do not exploit beyond
confirmation, do not access or disclose user data, and do not disrupt production
systems. Good faith research within the scope of this policy is authorized.

## Recognition

We appreciate responsible disclosure and will credit researchers who help us
improve our security. Recognition is included in our security bulletins and may
be featured in our communications.
