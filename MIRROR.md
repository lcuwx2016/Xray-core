# Upstream mirror policy

This fork preserves `XTLS/Xray-core` independently of upstream ref deletion.

- GitHub Actions runs every six hours and can also be started manually.
- Every upstream branch is stored as `mirror/<upstream branch>` so the `main`
  branch can retain the synchronization workflow.
- Upstream tags keep their original names.
- Deleted upstream branches and tags are never pruned from this repository.
- Before a non-fast-forward branch update, the previous tip is preserved as
  `upstream-archive/<branch>/<commit>`.
- Existing tags are never rewritten. If an upstream tag changes, the preserved
  tag remains unchanged and the workflow reports the conflict.

If the upstream repository becomes unavailable, the workflow fails without
changing or deleting any preserved refs.
