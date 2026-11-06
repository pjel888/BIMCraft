# Repository relationships

Setup baseline: 6 November 2026, Asia/Manila. GitHub owner: `pjel888`.

All local repositories are separate direct children of `C:\Users\phili\OneDrive\Documents`. None of the reference repositories is embedded in Greyledge.

| Project | GitHub repository | Local folder | Branch | Baseline commit | Setup disposition |
| --- | --- | --- | --- | --- | --- |
| BIMCraft fork | [pjel888/BIMCraft](https://github.com/pjel888/BIMCraft) | `BimCRAFT` | `main` | `149ef9c3e1df2d85e69fa4b551e8121b15abc810` | Existing public fork and clone preserved in place |
| IronCalc | [pjel888/IronCalc](https://github.com/pjel888/IronCalc) | `IronCalc` | `main` | `ae1fccd3dae89ab919e58ed299c525e6d6ba0ad5` | New public fork and clone |
| GPT Image Playground | [pjel888/gpt-image-playground](https://github.com/pjel888/gpt-image-playground) | `GPT Image Playground` | `master` | `47f6f95fb7ea0b20a997eba9f51a4f1f82cf6798` | New public fork and clone |
| SuperDoc | [pjel888/superdoc](https://github.com/pjel888/superdoc) | `SuperDoc` | `main` | `2457e2765d76e231cff7c87a2b2993cb6071e668` | New public fork and clone |
| Greyledge | [pjel888/Greyledge](https://github.com/pjel888/Greyledge) | `Greyledge` | `main` | BIMCraft base `149ef9c3e1df2d85e69fa4b551e8121b15abc810`, followed by the setup documentation commits | New independent private repository and clone |

Greyledge is private by the user's explicit choice. It is a standalone GitHub repository, seeded with BIMCraft's full reachable Git history, rather than another public-network GitHub fork. The source branch was cloned without a depth limit; inherited commits and local tags remain available. The initial publication targets `main`; it does not mirror other branches or publish tags.

## Greyledge remotes

| Remote | URL | Purpose |
| --- | --- | --- |
| `origin` (fetch) | [pjel888/Greyledge.git](https://github.com/pjel888/Greyledge.git) | Private Greyledge fetches |
| `origin` (push) | `ssh://git@ssh.github.com:443/pjel888/Greyledge.git` | Private Greyledge pushes over SSH port 443 |
| `bimcraft-fork` | [pjel888/BIMCraft.git](https://github.com/pjel888/BIMCraft.git) | The user's existing public fork, kept distinct |
| `upstream` | [IPedrax/BIMCraft.git](https://github.com/IPedrax/BIMCraft.git) | Original BIMCraft source and future update retrieval |

The original upstream `main` also pointed to the BIMCraft baseline above when inspected. Future updates can be fetched from `upstream` or `bimcraft-fork`, compared with Greyledge, then merged in a separately authorized task. Preserve ancestry; never overwrite Greyledge work with a reset or force push. The original `BimCRAFT` clone was not moved, renamed or reconfigured.

Each reference clone has `origin` pointing to the user's fork and `upstream` pointing to its original source:

- IronCalc: [ironcalc/IronCalc](https://github.com/ironcalc/IronCalc).
- GPT Image Playground: [alasano/gpt-image-playground](https://github.com/alasano/gpt-image-playground).
- SuperDoc: [superdoc/docx-editor](https://github.com/superdoc/docx-editor). The requested [superdoc-dev/superdoc](https://github.com/superdoc-dev/superdoc) URL redirects to this canonical repository; the fork's parent was verified against it.

Greyledge GitHub Actions were disabled before the first push to prevent inherited build workflows from running during setup. Leave execution settings unchanged until a later task authorizes builds. Pins above describe this setup, not a guarantee that live upstream branches remain unchanged; inspect actual refs before future work.
## Persistent workstation SSH access

The user authorized a persistent write deploy key scoped only to this Greyledge repository. GitHub key ID: `169001813`; public fingerprint: `SHA256:S+2K/Qg1jbteNCAXpiwVhbWjv9N41F0G53mba3Y4FaM`. The private key is kept outside this repository and outside OneDrive, in the user's SSH directory, with user-only file access. No private key material is committed here.

Repository-local `core.sshCommand` selects the already installed Git-bundled OpenSSH client, that key, and a dedicated known-hosts file pinned to GitHub's verified SSH host key. No global SSH configuration or SSH agent service was changed. Origin fetches remain HTTPS; origin pushes use SSH on port 443. The owned BIMCraft fork and IPedrax upstream remain separate HTTPS remotes. The deploy key can be managed or revoked in Greyledge's GitHub Settings > Deploy keys.
