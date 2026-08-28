# SESSION SEED — Physics of Governance Volume I, version bump

**Work:** version-bump the paper *Volume I: The Physics of Governance: Thermodynamic Limits of
Autonomous Agents* from v2.0, bringing its .tex format into consistency with the Intent-Aware
Continuity paper, and running a polish / gap-fill scan while the file is open.
**Repo (cwd for this session):** `C:/Repos/pog-vol1-paper` — created 2026-08-28 for exactly this work
**Execution mode:** Interactive — version semantics, byline changes and every content edit are owner calls
**Written:** 2026-08-28, at the close of the session that shipped plates 3–5 and the series teasers

---

## A. Where this stands, and why this repo exists

The vault does **not** hold this paper's v2.0 source. Verified 2026-08-28: `Exergonic` appears
nowhere under `C:/VAULT/Manuscripts`, and the zip that claims to be it —
`Governance_as_Physics/Volume_I_Law/Published/Source_Code_v4.zip` — is actually the **Principia v4**
source (title: "THE PRINCIPIA OF AUTONOMOUS GOVERNANCE"), misfiled. **Do not use it.** Filing fix is
open item D.6. The genuinely local PoG source is the v1.2 lineage
(`.../Published/Davis_2026_Physics_of_Governance_Vol1_Vis_v1.2.zip`, 2026-02-11), useful only as a
diff ancestor. The vault's whole `Manuscripts/` tree is **untracked** in the vault's git, which is
why a vault worktree was explicitly rejected for this session — a worktree at any commit contains
zero manuscript files, and an empty tree invites reconstruction-from-absence.

**This repo's baseline is bytes-from-deposit and the chain is closed:** `Source_Code_v2.0.zip`
downloaded from record `10.5281/zenodo.18645593`, md5 `bdc08ac0ff53178ea2b03dd5361d953c` verified
against the deposit manifest; the PDF inside is **sha256-identical** to the board pipeline's cached
primary (`ddfff4ba…`). Committed as `410638c`, tagged **`v2.0-baseline`**. Layout: `main.tex` +
`Fig01…Fig07*.tex` (TikZ, one per figure) at root; `deposit/` holds the pristine zip; `reference/`
holds the published v2.0 PDF. `.gitattributes` sets `* -text` — **never let git convert line
endings**; the baseline's value is that it is the deposit, byte for byte.

Verified structure (matches `content/_source/VERIFIED-STRUCTURE_Physics-of-Governance-VolI_v2.0.md`
in `C:/Repos/mdavis01-brand`): 8 sections, **13 equation environments, 0 theorem environments**,
`\bibliographystyle{plain}`.

---

## B. Five things that will bite, in order of severity

### B.1 🔴 A version bump is a NEW VERSION under concept `10.5281/zenodo.18645592` — never a new record

The standing duplicate (`18602937`, "v1.0.0 Preprint", still live) exists because a new **record**
was created instead of a new **version**. Both records report `is_last: true` inside their own
series. On Zenodo: open record 18645593 → **New version**. While in there, do the long-open fix:
edit the OLD record 18602937's description to point readers at the current concept. The new version
gets its own version DOI; `18645593` keeps resolving to v2.0 forever, which is why the shipped
plates' citations survive the bump untouched.

### B.2 🔴 EQUATION NUMBERS 1–13 ARE FROZEN

Five shipped plates carry composited bylines citing **Equation (6), (11), (12), (13)** against
`zenodo.18645593`, and the weekly articles will repeat those pointers. Any edit that inserts,
deletes or reorders an `equation` environment renumbers everything after it and silently falsifies
shipped public artifacts. New math goes in **starred environments or an appendix**. Post-compile
gate: extract the numbered-equation list and diff it against the baseline's 13 (the table in the
VERIFIED-STRUCTURE note is the reference).

### B.3 🔴 FIGURE LABEL STRINGS ARE FROZEN — the plates lift them verbatim

Each shipped plate carries two labels lifted verbatim from the paper's own figure, and those
strings live in the `Fig0N_*.tex` files in this repo: Fig03 `ENTROPY FLOW` / `GOVERNANCE
VISCOSITY` · Fig04 `SELF ATTENTION LOAD` / `BINDING ENERGY` · Fig05 `RULE SET A` / `RULE SET B` ·
Fig06 `(Read-Only)` / `Amendment` · Fig07 `Governance Enthalpy` / `Context Entropy`. Redraw or
reword freely elsewhere; **these exact strings must survive** or five boards stop being "lifted
verbatim from the paper's own figure." Gate: grep the frozen strings in the Fig files after any
figure edit.

### B.4 🔴 The §8 sign convention stays explicit — and stays THE SAME WAY ROUND

`ΔG_Gov > 0` = Endergonic = **stable**; `< 0` = Exergonic = **unstable, drift spontaneous and
irreversible**. Inverted from the ordinary chemical reading; documented as the easiest thing in the
paper to get backwards. Polish candidate: a one-line reader's caution at the definition. Any edit
here re-runs the direction check letter by letter.

### B.5 🔴 The references mechanism is UNRESOLVED at seed time

`\bibliographystyle{plain}` and `\usepackage{filecontents}` are both present, yet grep finds **no
.bib file, no `\bibliography{}` command, no `thebibliography` environment, no `\bibitem`** — and the
published PDF carries 8 references. Something nonstandard produces them. First compile settles it;
a References section missing from the output is a STOP, not a shrug.

---

## C. Format-consistency targets (donor: Intent-Aware Continuity v5.0)

Verified deltas, PoG v2.0 vs IAC v5.0 page 1 — each an owner-visible change, none silent:

| Element | IAC v5.0 has | PoG v2.0 has |
|---|---|---|
| Affiliation | `Independent Researcher` | `The Unified Field Theory of Autonomous Governance Project` — **owner call which survives** |
| Contact | `m@ontoramp.com` | verify in `main.tex` |
| ORCID | `0009-0000-4309-3874` on byline | **absent** (0 grep hits) |
| Keywords block | yes | **absent** |
| Data/code availability | yes — GitHub repo + Zenodo DOI | **absent** — and no PoG repo existed until this one; owner call whether this repo (pushed) becomes the cited artifact |
| Theorems | numbered environments | none — **additive only if introduced; equations must not renumber (B.2)** |

Donor sources, all verified on disk:
`C:/VAULT/Manuscripts/Paradoxes/Solved/Ship_of_Theseus/` (IAC home: `ids_physics.sty`,
`references.bib`, `Published/Intent-Aware-Continuity_Davis_2026_v5.0.pdf`,
`Intent-Aware-Continuity_v5.0_Publication_Record.md` — PoG has no publication record file; create
one at bump time, same shape) · `C:/VAULT/Manuscripts/CF00_Global_ArXiv_Template_v2.tex` ·
`Canon_Academic_Manuscript_Authoring_Guide_v2.0.md` · `Manuscript_Purity_Mode_Checklist_v1_0.md` ·
`Protocol_Overleaf_Efficiency.md`. Compile locally (MiKTeX is installed — `pdftoppm` came from it)
or per the Overleaf protocol; either way the gates in F run on the produced PDF.

## D. Polish / gap-fill scan — candidates already spotted (decide, don't assume)

1. **"Fundamental Theorem of AI Governance"** (§8.1) is prose-named in a paper with no theorem
   environments. Give it an environment (additive, B.2-safe) or rename the claim.
2. **Keywords + availability + ORCID** per the table above.
3. **Landauer constant** (§2.1, the paper's only hard number) — carries a citation? Verify.
4. **Volume II teaser** in §8.1 ("The Economics of Autonomous Agency") — still the intended
   roadmap? Owner confirm before it ships again in a new version.
5. **CF00_Unified_Field_Theory_DOI_Manifest_v1.md** points at the WRONG concept (18602937) and
   labels it v2.2, a version string existing in neither record. Correct it in the same session the
   new version publishes.
6. **File the misfiled zip:** `Volume_I_Law/Published/Source_Code_v4.zip` belongs to the Principia
   (its `Published/` dir has the matching v4 PDF). Move, don't delete.
7. Version semantics — v2.1 (format + polish) vs v3.0 (content changes) — owner call at session start.

## E. After publish — the derived surfaces that WILL go stale (four precedents this week)

- `C:/Repos/mdavis01-brand/content/_source/`: cache the new PDF beside the old, re-verify structure,
  write a new VERIFIED-STRUCTURE note (do not overwrite the v2.0 one — plates cite v2.0).
- Memory `project_physics_of_governance_series.md` (says v2.0; keyed to `18645593` — still correct
  for the plates, note the new version DOI beside it).
- The teaser renditions cite "Volume I" generically — no change needed; articles drafted after the
  bump cite whichever version DOI they were written against.
- This repo: tag the new version, refresh `deposit/` and `reference/` with the new zip + PDF,
  write the Publication Record.

## F. Gates, in order

1. Baseline compile FIRST — before any edit, prove the deposit compiles and references appear (B.5).
2. After edits: compile · equation-list diff vs the 13 (B.2) · frozen-string grep on Fig files
   (B.3) · §8 direction check (B.4) · page-1 format check vs the C table.
3. sha256 the new PDF; record it in the Publication Record; commit and tag before uploading.
4. Zenodo: NEW VERSION under the concept (B.1) → then D.5, D.6, and every item in E.

## G. Session start prompt

> Working in `C:/Repos/pog-vol1-paper` on the version bump of Physics of Governance Volume I.
> Read `SEED_pog-vol1-version-bump.md` in full first. Baseline is tag `v2.0-baseline`, bytes from
> the Zenodo deposit, chain verified. Compile the baseline before touching anything (B.5). Then:
> owner decides version semantics (D.7) and the affiliation question (C), format pass against the
> IAC donor, polish scan per D. Equations 1–13 and the figure label strings are frozen (B.2, B.3).
> The bump is a NEW VERSION under concept 10.5281/zenodo.18645592, never a new record (B.1).
