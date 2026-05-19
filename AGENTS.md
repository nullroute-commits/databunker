# Databunker Agent Source of Truth

This repository adopts [`nullroute-commits/agency-agents`](https://github.com/nullroute-commits/agency-agents) as the upstream source of truth for reusable agent roles and skills.

- Upstream repository: `https://github.com/nullroute-commits/agency-agents`
- Pinned upstream branch: `main`
- Pinned upstream commit: `783f6a72bfd7f3135700ac273c619d92821b419a`

## Repository adapter rules

Use the upstream agent definitions as the baseline behavior. When working in this repository:

1. Repository-specific instructions in this file override generic upstream guidance.
2. Facts must be grounded in this repository's checked-in code, docs, tests, and workflows.
3. Planning deliverables must use the current repository state, not upstream examples.
4. Security and privacy work must prioritize GDPR, auditability, encryption safety, and operational recovery.

## Preferred upstream skills for this repository

- **Codebase Onboarding Engineer**: primary skill for repository discovery, call-path tracing, and onboarding maps.
- **Security Engineer**: primary skill for auth, encryption, secret handling, and abuse-path reviews.
- **Code Reviewer**: primary skill for bug audits, regression review, and maintainability checks.
- **Sprint Prioritizer**: primary skill for roadmap, backlog triage, release planning, and sprint plans.
- **Technical Writer**: primary skill for API, setup, operator, and contributor documentation updates.

## Databunker-specific source material

Treat these repository files as the local source of truth when applying upstream skills:

- `/home/runner/work/databunker/databunker/README.md`
- `/home/runner/work/databunker/databunker/BUILD.md`
- `/home/runner/work/databunker/databunker/INSTALLATION.md`
- `/home/runner/work/databunker/databunker/API.md`
- `/home/runner/work/databunker/databunker/databunker.yaml`
- `/home/runner/work/databunker/databunker/.github/workflows/cy.yml`
- `/home/runner/work/databunker/databunker/src/`

## Minimum audit workflow

For bug discovery, release readiness, or sprint planning:

1. Inspect repository docs and runtime entrypoints.
2. Run the existing validation commands for this repo:
   - `cd /home/runner/work/databunker/databunker/src && go test ./...`
   - `cd /home/runner/work/databunker/databunker/src && go vet ./...`
   - `cd /home/runner/work/databunker/databunker && ./build.sh`
3. Review the current GitHub Actions workflow and recent workflow runs.
4. Classify findings as:
   - confirmed bugs
   - operational blockers
   - feature gaps
5. Convert findings into a prioritized sprint plan with clear deliverables and dependencies.

## Upstream sync process

When upstream `agency-agents` changes:

1. Review the updated upstream agent files that map to this repository.
2. Update the pinned commit in this file.
3. Keep repository-specific constraints and source-material references intact.
4. Re-run the local audit workflow before relying on new planning output.
