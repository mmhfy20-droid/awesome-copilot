---
name: alrubouei-fullstack-platform
description: "Design and implement full-stack application architecture, APIs, databases, authentication, commerce workflows, and integrations. Use when a project needs backend services or end-to-end application behavior."
---

# Full-Stack Application Engineering

## Workflow
1. Inspect existing code and infrastructure; document the current architecture before proposing changes.
2. Define domain entities, ownership, relationships, invariants, and lifecycle states.
3. Design API contracts with validation, pagination, filtering, consistent errors, and versioning where needed.
4. Design database schema, indexes, migrations, constraints, and backup/restore expectations.
5. Implement authentication and authorization with least privilege and server-side enforcement.
6. Implement business operations transactionally where consistency matters.
7. Add idempotency and retry-safe behavior for payment, order, and webhook flows.
8. Integrate external services behind adapters; isolate credentials in environment secrets.
9. Add audit logs for sensitive administrative actions without logging secrets or unnecessary personal data.
10. Test API contracts, permissions, failure paths, migrations, and end-to-end workflows.

## Commerce-specific checks
- Model order states explicitly and prevent invalid transitions.
- Recalculate prices and totals on the server; never trust client-submitted totals.
- Track inventory changes atomically and prevent overselling.
- Treat payment callbacks as untrusted until signature and transaction status are verified.
- Do not store raw card credentials.
- Separate delivery fees, discounts, taxes, and item prices.

## Pharmacy and health-domain checks
- Treat medicine catalog facts, dosage, contraindications, substitutions, and prescription status as regulated/high-risk data.
- Use authoritative, jurisdiction-appropriate sources and qualified human review for clinical content.
- Do not generate treatment recommendations or automatic substitutions as if clinically approved.
- Restrict access to prescription and customer health data; minimize retention and log access appropriately.
- Confirm local legal, licensing, prescription, and delivery requirements before launch.

## Guardrails
Do not invent payment-provider APIs, claim an integration works without sandbox/live verification, or expose credentials in code, logs, screenshots, or chat.
