---
title: "Volume I: The Physics of Governance — Publication Record v2.1"
domain: manuscripts
ip_classification: public
status: pending-publish
created: 2026-08-28
updated: 2026-08-28
authors: "Davis, Matthew A."
orcid: 0009-0000-4309-3874
license: CC BY 4.0
concept_doi: 10.5281/zenodo.18645592
version_doi: "[pending — assigned at Zenodo publish]"
---

# Volume I: The Physics of Governance — Publication Record (v2.1)

Publication record for the version bump of the peer-facing paper. All content is
drawn from the artifact and its verified build chain. Fields marked *pending*
are filled in the session that publishes the Zenodo new version.

## Citation

> Davis, Matthew A. (2026). *Volume I: The Physics of Governance: Thermodynamic
> Limits of Autonomous Agents.* Version 2.1. DOI: 10.5281/zenodo.18645592

| Field | Value |
|-------|-------|
| Version | 2.1 |
| Published | *pending* (built 2026-08-28) |
| License | CC BY 4.0 (inherited from the v2.0 record, verified via Zenodo API) |
| Concept DOI (always latest) | `10.5281/zenodo.18645592` |
| Version DOI (v2.1) | *pending* |
| Version DOI (v2.0) | `10.5281/zenodo.18645593` — the DOI the shipped plates cite; resolves to v2.0 forever |
| Repository | `github.com/MatthewDavisAIArchitect/pog-vol1-paper` tag `v2.1` — *pending push* |
| Candidate PDF sha256 | `a22df4e485afd652d3185c9f8c22e55f81528bc8fab8d76fa3d9a0a44e006f16` |
| Candidate `Source_Code_v2.1.zip` sha256 | `b08d27aaa7a7145911a23581ff920ad8916d711374bcb16adb204c25e5abff56` (md5 `98473bc51011355a6425f9f85bc4ce11`) |
| Release commit | `1e49926` on `feat/pog-vol1-version-bump`, tag `v2.1` |

## Argument

Governance of autonomous agents modeled as thermodynamics, explicitly as
analogy: Alignment (G_E) is enthalpy, Drift (G_I) is entropy, and holding an
agent aligned costs continuous kinetic work (W_Gov, floored by Landauer's
limit). The paper derives a contextual Reynolds number for hallucination onset,
a Jeans-type stability ratio for quadratic (O(N²)) attention collapse, and
closes with the Gibbs Governance Criterion ΔG_Gov = ΔH_Intent − T_Sys·ΔS_Interact.
Sign convention (§8, easy to get backwards, now flagged in-text): **ΔG_Gov > 0 =
Endergonic = stable; ΔG_Gov < 0 = Exergonic = drift spontaneous and
irreversible** — inverted from the ordinary chemical reading.

## Structure (v2.1)

8 sections · **13 numbered equations (1)–(13), frozen** — shipped plates cite
(6), (11), (12), (13) against the v2.0 record · 7 figures · Table 1
(Nomenclature) · 8 references [1]–[8], numbering unchanged from v2.0 · **one
unnumbered theorem environment** (`theorem*`: "Fundamental Theorem of AI
Governance", §8.1 — new in v2.1, deliberately unnumbered so the citable label
set gains no numbers). 13 pages, A4.

## v2.1 change log (vs published v2.0)

**Reproducibility restoration** — the v2.0 deposit was not self-compiling:
- `references.bib` was never deposited; reconstructed rendering-exact from the
  published PDF's typeset reference list (commit `23cb1a0`).
- Fig sources shipped flat while `main.tex` inputs `figures/…`; layout restored.

**Format parity with Intent-Aware Continuity v5.0** (owner-approved):
- Contact `m@ontoramp.com`; ORCID line added; date August 2026.
- Data and code availability paragraph on page 1 (repo + tag + concept DOI).
- Affiliation retained: *The Unified Field Theory of Autonomous Governance
  Project* (owner call).

**Errata for defects that typeset in the published v2.0 PDF:**
- Literal `====…` line before §8 (uncommented rule) — removed.
- Literal `**…**` asterisks in §4.1 and §5.2 — proper bold.
- Orphan en-dash before §4's figure (stray `--`) — removed.
- Fig 3 turbulent lines: invalid TikZ key `decorating` → `decorate`; the snake
  decoration renders for the first time.
- Vault-figure annotation rendered as one jammed token `CryptographicallyLocked`
  (missing `align=`) — now a proper two-line label.

**Polish:** theorem environment for §8.1 (above); one-sentence reader's caution
on the §8 sign convention; Volume II teaser updated to the published title *The
Economics of Autonomous Agency: Volume II — Entropy, Debt, and the Cost of
Truth*; ref [1] gains `{AI}` casing and the COI concept DOI
`10.5281/zenodo.18437153` (verified via Zenodo API; the vault manifest's
`18519246` is the v1.0.2 *version* DOI, not the concept).

## Reproducibility

Self-compiling since v2.1: `pdflatex → bibtex → pdflatex ×2` (nonstop mode) on
`main.tex` with `references.bib` and `figures/` beside it. Requires scalable CM
fonts (`cm-super` — the fonts the published PDFs embed); MiKTeX 25.4 verified.

Verification chain: the v2.0 baseline (tag `v2.0-baseline`, bytes from deposit
`Source_Code_v2.0.zip`, md5 `bdc08ac0ff53178ea2b03dd5361d953c`) rebuilt under
this recipe produces pdftotext output **byte-identical** to the published v2.0
PDF (sha256 `ddfff4ba…`). The v2.1 build's full text diff against v2.0 maps
1:1 to the change log above plus float repagination. Gates at build: 0
compile errors (v2.0 carried 8 recoverable ones), 13 equation environments
with (13) the final number, frozen figure label strings intact, §8 direction
re-verified.

## Version history

| Version | Date | Note |
|---------|------|------|
| 2.1 | *pending* (built 2026-08-28) | Reproducibility restoration; IAC v5.0 format parity; published-defect errata; approved polish. No claim changes; equations unrenumbered. |
| 2.0 | 2026-02-15 | Record `10.5281/zenodo.18645593`. Baseline for this repo (`v2.0-baseline`). |
| 1.0.0 "Preprint" | 2026-02-10 | **Separate duplicate concept** `10.5281/zenodo.18602937` — do not cite; its description gets a pointer to the current concept at v2.1 publish time. |
| 1.2 (visual lineage) | 2026-02-11 | Local zip only (`Volume_I_Law/Published/Davis_2026_Physics_of_Governance_Vol1_Vis_v1.2.zip`); diff ancestor. |

## Post-publish checklist (fill/execute in the publishing session)

1. Zenodo: **New version** under concept `18645592` (never a new record);
   upload `Davis_2026_Volume_I_The_Physics_of_Governance_v2.1.pdf` +
   `Source_Code_v2.1.zip`; record the v2.1 version DOI here and in the
   frontmatter; set `status: active`.
2. Edit old record `18602937`'s description to point at the current concept.
3. Push this repo to `github.com/MatthewDavisAIArchitect/pog-vol1-paper` and
   confirm the availability URL + tag resolve (page 1 cites them).
4. Refresh `deposit/` and `reference/` with the published v2.1 files; verify
   hashes match this record.
5. Fix `C:/VAULT/Manuscripts/CF00_Unified_Field_Theory_DOI_Manifest_v1.md`
   (Vol I row: wrong concept `18602937`, phantom "v2.2"; also COI row lists a
   version DOI as concept — concept is `18437153`).
6. Move misfiled `Volume_I_Law/Published/Source_Code_v4.zip` (Principia v4) to
   the Principia home; file the v2.1 zip + PDF in `Volume_I_Law/Published/`.
7. Brand repo `content/_source/`: cache the v2.1 PDF beside v2.0, write a new
   VERIFIED-STRUCTURE note (do not overwrite the v2.0 note — plates cite v2.0).
8. Update memory `project_physics_of_governance_series.md` with the v2.1
   version DOI beside the v2.0 pointer.
