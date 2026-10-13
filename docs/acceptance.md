# Locked acceptance and handoff

Goal: demonstrate representative GitHub company workflow compatibility of Harness0.93.0.
No actual company or human participants. Separate technical evidence from human effectiveness.

Title contract: trim string, require nonempty, maximum80 after trimming, reject nonstrings.
Locked tests: test/product.test.mjs. Do not modify them to repair seeded candidates.
Quality and deploy-smoke must succeed on current PR head, bound to actual GitHub Actions app.
Failed/missing/pending/old-head CI, stale review snapshot must not merge.
Review-required target must reject absent human/CODEOWNER approval; never lower that policy.
Normal targets have CI-only policy from inception; their success is not approval proof.
Company solo must refuse without altering any policy.

Feature→develop (manual/auto), release→main→develop, hotfix→main→develop.
Tags bind to actual reviewed main merge SHA. Disposable HTTP deploy checks source/hash/health.
All first failures, head/base/policy/check-run IDs, wrapper output and cleanup are retained.

Handoff recipient: read this file, git history and exact PR/CI evidence. Determine the current
candidate, failed criterion and next permitted action without author coaching. Run only local
synthetic tests, diagnose before editing, and preserve tests/policies. Actual human learning
and productivity remain unmeasured.
