# Greyledge change record

## 6 November 2026 — repository and agent setup

- Preserved the existing `BimCRAFT` repository in place.
- Created separate reference forks/clones for IronCalc, GPT Image Playground and SuperDoc, retaining their source and notices without integrations.
- Created private `pjel888/Greyledge`, seeded from `pjel888/BIMCraft` at `149ef9c3e1df2d85e69fa4b551e8121b15abc810` with inherited Git history.
- Configured Greyledge `origin`, `bimcraft-fork` and original `upstream` relationships; disabled Greyledge GitHub Actions before publication to prevent inherited builds.
- Added persistent Greyledge-only SSH write access with explicit user approval after HTTPS upload failures; repository-local push configuration uses the existing Git-bundled client on port 443. Private key material remains outside the repository.
- Added only six `.ai` Markdown documents. The inherited application source, manifests, dependency locks, licenses and notices remain unchanged.
- Setup verification covers Git identity/state, repository relationships, ancestry, documentation and license preservation. Dependencies were not installed; no feature development, integration, builds, application launches or long-running services were performed. Runtime behavior remains untested in this setup.

Use Git history for the exact setup commit and current state; [REPOSITORIES.md](REPOSITORIES.md) retains the baseline pins. Later material entries should state the change, reason, evidence and limits without storing secrets or conversation transcripts.
