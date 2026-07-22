# Xray-core upstream mirror

This repository is a preservation mirror of
[`XTLS/Xray-core`](https://github.com/XTLS/Xray-core). It does not provide an
independent Xray-core distribution or accept feature development on the
control branch.

## Branches

- `main` is the control branch. It contains only the mirror documentation,
  license, and scheduled synchronization workflow.
- `mirror/main` tracks the upstream `main` branch and contains the complete
  source code.

Upstream tags are preserved under their original names. Synchronization runs
every six hours, does not propagate upstream deletions, and leaves existing
tags unchanged if upstream rewrites them. See [MIRROR.md](MIRROR.md) for the
full policy.

## License

Xray-core is licensed under the
[Mozilla Public License 2.0](LICENSE). All project rights and attribution
remain with the upstream project and its contributors.
