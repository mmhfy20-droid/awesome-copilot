---
name: alrubouei-appsec-release
description: "Apply secure-by-design reviews, automated testing, dependency checks, CI pipelines, deployment safeguards, and production readiness gates to web and mobile applications."
---

# Application Security, Testing, and Release

## Security review
1. Map assets, trust boundaries, data sensitivity, and likely abuse cases.
2. Check authentication, authorization, session handling, input validation, output encoding, CSRF, XSS, injection, SSRF, file uploads, and rate limiting as applicable.
3. Apply least privilege to app users, CI tokens, cloud services, and database accounts.
4. Review dependency provenance, lockfiles, known vulnerabilities, and abandoned packages.
5. Ensure secrets are stored in approved secret managers and are never committed.
6. Protect personal and sensitive data in transit and at rest; define retention and deletion behavior.
7. Add security headers and safe cookie settings appropriate to the deployment.
8. Record findings with severity, evidence, affected component, and remediation.

## Quality gates
- Unit tests for business rules
- Integration tests for APIs and persistence
- End-to-end tests for critical journeys
- Type checking and linting
- Dependency and secret scanning
- Build and migration validation
- Accessibility checks
- Performance checks for critical pages

## CI/CD principles
- Run checks on pull requests before merge.
- Use minimal workflow permissions and pin third-party actions to immutable SHAs where practical.
- Separate build, test, and deploy stages.
- Require explicit approval for production deployments and destructive migrations.
- Keep rollback and backup procedures documented.
- Do not expose production credentials to untrusted pull-request code.

## Release decision
Classify each issue as blocker, high, medium, or low. Do not label a release production-ready while a blocker remains unresolved. Report what was actually tested, what was not tested, and the residual risks.
