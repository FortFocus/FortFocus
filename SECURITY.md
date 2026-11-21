# Security Policy

FortFocus takes the security and integrity of our software and user environments seriously. This document describes our vulnerability disclosure process and supported release channels.

---

## Supported Versions

Security updates and patches are actively maintained for the latest release branch:

| Version | Supported | Status |
| :--- | :--- | :--- |
| **0.13.x** | :white_check_mark: | Current Active Release |
| **< 0.13.0** | :x: | Deprecated / End of Support |

---

## Reporting a Vulnerability

If you have discovered a potential security vulnerability, privilege escalation path, service isolation bypass, or privacy leak in FortFocus, please report it privately through GitHub:

1. Navigate to the repository's **[Security](https://github.com/FortFocus/FortFocus/security)** tab.
2. Select **[Advisories](https://github.com/FortFocus/FortFocus/security/advisories)**.
3. Click **Report a vulnerability** (or use the direct link: `https://github.com/FortFocus/FortFocus/security/advisories/new`).
4. Provide a detailed description of the vulnerability, including:
   - Operating system version (e.g., Windows 10 22H2, Windows 11 23H2).
   - Component affected (e.g., Windows service, named pipe IPC, GUI, DPAPI storage).
   - Step-by-step reproduction instructions or proof-of-concept script.
   - Assessment of potential impact and severity.

> [!IMPORTANT]
> **Please do not report security vulnerabilities via public GitHub issues, discussions, or social media channels.** Using the private GitHub Security Advisory mechanism allows the team to verify, remediate, and publish an advisory and fix collaboratively prior to public disclosure.

---

## Security Response SLA

- **Initial Acknowledgment:** Within **48 hours** of receiving the report.
- **Triage & Validation:** Within **5 business days** of initial acknowledgment.
- **Remediation & Patch Release:** Prioritized according to CVSS severity, with critical vulnerabilities targeted for expedited emergency patch release.

---

## Responsible Disclosure & Safe Harbor

We support responsible security research. We commit not to pursue legal action against researchers who:
- Perform testing in good faith and avoid intentional service denial or harm to user data.
- Refrain from accessing, modifying, or destroying third-party or user data.
- Give the maintainers reasonable time to address the issue before making any details public.
