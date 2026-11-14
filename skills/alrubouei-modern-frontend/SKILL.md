---
name: alrubouei-modern-frontend
description: "Build maintainable, responsive production frontends using modern React, Next.js, TypeScript, component architecture, and accessible interaction patterns. Use when implementing or refactoring an app frontend."
---

# Modern Frontend Engineering

## Workflow
1. Inspect the repository, package manager, framework version, existing conventions, and tests before changing files.
2. Preserve the current stack unless there is a documented reason to migrate.
3. Define route structure, component boundaries, data contracts, and state ownership.
4. Use TypeScript with strict types; avoid any and unsafe casts.
5. Build reusable components and separate presentation from data access and business logic.
6. Handle loading, empty, error, offline, and success states explicitly.
7. Implement forms with validation, accessible labels, clear errors, and safe submission behavior.
8. Optimize images, fonts, bundles, caching, and rendering based on measured bottlenecks.
9. Add unit, component, and end-to-end tests for critical user journeys.
10. Run lint, typecheck, tests, and production build; report exact results.

## Engineering standards
- Prefer semantic HTML and progressive enhancement.
- Use server rendering or client rendering intentionally; do not add client state without need.
- Keep secrets out of browser bundles and source control.
- Validate untrusted input at trust boundaries.
- Avoid unnecessary dependencies and pin versions where appropriate.
- Respect reduced-motion, keyboard access, RTL, and localization requirements.

## Completion report
List changed files, implemented behavior, commands/tests run, failures, and remaining risks. Never claim tests passed unless the commands actually completed successfully.
