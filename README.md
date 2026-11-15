# Agent run traces

Evidence archives for agent evaluations, stored with Git LFS. Summaries and experiments live in [agent-runs](https://github.com/thi-bot/agent-runs) or the source project.

```text
projects/<owner>/<project>/<evaluation>/<run-id>/
  README.md
  manifest.json
  SHA256SUMS
  evidence.tar.gz
```

Use a date or timestamp for each run ID; add a new folder for subsequent uploads. Manifests record provenance, coverage and archive checksums. Large archives use LFS; metadata stays in ordinary Git.

To download one run:

```sh
GIT_LFS_SKIP_SMUDGE=1 git clone https://github.com/thi-bot/agent-runs-traces.git
cd agent-runs-traces
git lfs pull --include="projects/wagtail/guide/agent-readiness/20261113/*"
cd projects/wagtail/guide/agent-readiness/20261113
sha256sum -c SHA256SUMS
mkdir -p evidence
tar -xzf evidence.tar.gz -C evidence
cd evidence
sha256sum -c SHA256SUMS
```
