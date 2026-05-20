# Security Policy

## Reporting a vulnerability

**Contact:** kraigparkinson@integralproductivity.com

Please do **not** open a public GitHub issue for security vulnerabilities. Send a private
email to the address above with:

- A description of the vulnerability
- Steps to reproduce or a proof-of-concept
- The potential impact

**Expected response time:** Best effort. This org is operated by a solo practitioner. You
can expect an initial acknowledgment within 7 days and a resolution or workaround within
30 days for confirmed vulnerabilities, depending on severity.

## Scope

| In scope | Out of scope |
|---|---|
| Vulnerabilities in code published in this org's repositories | Third-party dependencies (report those to the upstream project) |
| Secrets accidentally committed to this org's repos | GitHub platform vulnerabilities (report to GitHub) |
| CI/CD workflows that could be exploited to access org secrets | Theoretical issues without a realistic attack path |

## Disclosure policy

We follow coordinated disclosure. Once a fix is available, we will publish a brief summary
of the vulnerability and its resolution. Credit will be given to the reporter unless they
prefer to remain anonymous.
