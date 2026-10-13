# Team Harness remote acceptance lab

Public disposable synthetic-only test repository. No product, production, DB, credentials or billing.
Pinned Harness source: `207251185a6e828a86106d171c16a4d1b71d152a` / v0.93.0.

Main/develop require strict GitHub Actions CI, administrators included.
A separate review-required branch requires one human/CODEOWNER approval; no solo exception.
The CI-only branches demonstrate technical Git Flow, not a real teammate approval.

`node --test` → `node scripts/build.mjs` → `node scripts/deploy-smoke.mjs`.
Deployment is a short-lived real HTTP server consuming a built artifact in an isolated runner directory.
It is destroyed in finally; cloud staging/production deployment is outside this test.

Acceptance matrix and handoff instructions are in `docs/acceptance.md`.

Synthetic human/CODEOWNER absence probe; never bypass approval.
