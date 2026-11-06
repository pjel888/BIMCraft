# Licenses and attribution

This is a setup inventory for later review, not a decision to integrate any candidate or a complete dependency/license audit. No code was copied from the reference repositories into Greyledge. Private repository visibility does not replace license obligations.

## Source terms at the recorded commits

- **BIMCraft / Greyledge base:** [Cargo.toml](../Cargo.toml) declares `MIT OR Apache-2.0`. Preserve [LICENSE-MIT](../LICENSE-MIT), [LICENSE-APACHE](../LICENSE-APACHE) and [NOTICE](../NOTICE). The Revit reader has its own Apache-2.0 [LICENSE](../crates/rvt/LICENSE) and [NOTICE](../crates/rvt/NOTICE). Other component and asset terms remain relevant, including the DWG bridge's MPL-2.0 dependency and font licenses described in the inherited notices. Do not infer one uniform license for every file.
- **IronCalc:** [README at the baseline](https://github.com/ironcalc/IronCalc/blob/ae1fccd3dae89ab919e58ed299c525e6d6ba0ad5/README.md#license) and crate manifests declare `MIT OR Apache-2.0`; both `LICENSE-MIT` and `LICENSE-Apache-2.0` are preserved. Also retain `base/THIRD-PARTY-NOTICES.md`, package notices, Unicode data notices and font licenses. GitHub's single Apache license label omits this dual-license context.
- **GPT Image Playground:** the baseline [MIT LICENSE](https://github.com/alasano/gpt-image-playground/blob/47f6f95fb7ea0b20a997eba9f51a4f1f82cf6798/LICENSE) includes the original copyright and permission notice. Preserve it and inspect dependencies separately before reuse.
- **SuperDoc:** the baseline [LICENSE](https://github.com/superdoc/docx-editor/blob/2457e2765d76e231cff7c87a2b2993cb6071e668/LICENSE) supplies GNU AGPL version 3. Preserve it, original attribution and [THIRD_PARTY_LICENSES.md](https://github.com/superdoc/docx-editor/blob/2457e2765d76e231cff7c87a2b2993cb6071e668/THIRD_PARTY_LICENSES.md), including the per-font notice/license set in `shared/font-system/assets/`. Font exceptions and third-party licenses have their own scopes.

## SuperDoc review before integration

AGPLv3 is copyleft. Distribution of covered source or binaries has applicable notice, licensing and corresponding-source requirements. Section 13 additionally requires a modified version supporting remote network interaction to offer its corresponding source to the users interacting with it over that network. These provisions must be reviewed against the actual modifications and deployment; a private GitHub repository does not waive them. See the preserved [license sections 4-6 and 13](https://github.com/superdoc/docx-editor/blob/2457e2765d76e231cff7c87a2b2993cb6071e668/LICENSE).

Before choosing SuperDoc, document the proposed integration boundary, which components are combined or modified, intended distribution/hosting, required source availability, all third-party terms and the responsible licensing decision. Do not assume a separate process automatically resolves the question, or that all Greyledge code becomes covered without examining the arrangement. Obtain qualified review for the chosen deployment.

The baseline [SuperDoc README](https://github.com/superdoc/docx-editor/blob/2457e2765d76e231cff7c87a2b2993cb6071e668/README.md#license) offers a commercial licensing route for proprietary deployments. Availability in a README is not an acquired license; terms and suitability remain a later user/vendor decision. SuperDoc remains a candidate only.

## Preservation rules

Keep original license, copyright, provenance and notice files. Record source repository, commit, file scope, modifications and chosen license route before reuse. Preserve required notices in distributions; identify modified files where the applicable license requires it. Do not silently replace upstream terms, assume licenses are interchangeable, or copy Autodesk/proprietary assets. Review updates for changed license terms and bundled assets.

Primary references: the commit-pinned files above and [Apache License 2.0, section 4](https://www.apache.org/licenses/LICENSE-2.0). Setup notes were checked on 6 November 2026; integration and legal acceptance remain future work.
