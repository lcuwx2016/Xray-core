# Upstream mirror policy

This fork preserves `XTLS/Xray-core` independently of upstream ref deletion.

- GitHub Actions runs every six hours and can also be started manually.
- Upstream `main` is stored as `mirror/main` so the local `main` branch can
  retain the synchronization workflow and this policy document.
- Upstream tags keep their original names.
- Upstream branch and tag deletion is never propagated to this repository.
- Existing tags are never rewritten. If an upstream tag changes, the preserved
  tag remains unchanged and the workflow reports the conflict.

If the upstream repository becomes unavailable, the workflow fails without
changing or deleting any preserved refs.
