# AGENTS.md

## Agent skills

### Issue tracker

Bluefin OCI issues and PRDs live in [GitHub Issues](https://github.com/projectbluefin/ghostscript-printer-app/issues), not `.scratch/` or upstream OpenPrinting. See `docs/agents/issue-tracker.md`.

### Triage labels

Canonical triage labels are used unchanged. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: `CONTEXT.md` + `docs/adr/` at the repo root, created lazily by domain modeling. See `docs/agents/domain.md`.

### OCI container build

Before changing the BuildStream/FSDK graph or CUPS integration, read `docs/skills/fsdk-cups-patching.md`.

### Branches and releases

Target `testing` for FSDK source updates and development PRs; promote verified commits to `stable`. CI verifies both PR targets and both branches with the full OCI appliance gate. Only version tags on `stable` publish immutable OCI releases. Keep `main` while existing feature branches or workflows still reference it.
