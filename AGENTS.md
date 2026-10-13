# Acceptance lab contract

Synthetic source only. Do not read/upload env files or credentials.
No production, DB/Auth/Storage, payments or existing repository/protection mutations.
Commit on codex/, feature/, fix/, hotfix/, release/ or sync/ branches only.
PR creation/merging must use the pinned Harness pr-create.sh/pr-merge.sh wrappers.
Company mode prohibits solo-merge. Preserve strict required CI and administrator enforcement.
Read docs/acceptance.md; preserve locked tests and failure history. Do not weaken tests to pass.
Review is independent, actual read-only execution. AI review does not equal human approval.

## Build and release commands

Quality: node --test test/product.test.mjs; node scripts/build.mjs.
Disposable health: node scripts/deploy-smoke.mjs. Required CI includes all three.
Version: package.json version; release notes: CHANGELOG.md, version entries before commit.
Feature: codex/ or feature/ to develop by wrappers; auto is allowed only to develop.
Release: release/vVERSION from origin/develop to main, exact merge SHA tag, sync/ PR to develop.
Hotfix rehearsal: hotfix/ from origin/main to main, next patch tag, sync/ PR to develop.
No production exists; operational incident handling and cloud rollout are not tested.
Lab product installation is not applicable; this is a synthetic Node built-in artifact.
Use owned isolated/detached checkout for merge operations; never reset user's branches.
