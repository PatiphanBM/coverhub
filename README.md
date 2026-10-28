# CoverHub

A CMS-driven web platform for a fictional insurance company: marketing teams build campaign pages in Payload CMS, customers request travel-insurance quotes, and leads are delivered reliably to a CRM.

**Stack:** Next.js (App Router) · TypeScript · Tailwind CSS · Payload CMS · Go · PostgreSQL · AWS (ECS Fargate, RDS) · Terraform · GitHub Actions

🚧 Work in progress.

## Repo layout (target)

```
coverhub/
├── apps/
│   ├── web/                # Next.js App Router + Payload 3 + Tailwind + TS
│   ├── api/                # Go: quote, lead, outbox worker
│   └── legacy-core-mock/   # Go service that is slow/flaky and returns XML
├── infra/                  # Terraform
├── docs/                   # ADRs, runbook, architecture, post-mortems
├── .github/workflows/      # CI / deploy
└── compose.yaml
```

## Contributing

- Every change goes through a short-lived branch + PR into `main` (protected).
- Commits follow [Conventional Commits](https://www.conventionalcommits.org/): `feat`, `fix`, `refactor`, `test`, `docs`, `chore`.
- PRs are squash-merged; roll back with `git revert`, never by rewriting `main`.
