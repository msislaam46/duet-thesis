# DUET — thesis (LaTeX source)

LaTeX source for the MSc thesis *"Key Transparency for Signal: Dual-Index
Warnings and Windowed Consistency Proofs"* (DUET).

- **Main file:** `main.tex` (compile with pdfLaTeX; run BibTeX/biber for
  `references.bib`). A typical build: `latexmk -pdf main.tex`.
- **Layout:** `chapters/` (per-chapter `.tex`), `figures/` (`.png` screenshots
  + `figures/tikz/` TikZ sources), `kt-macros.sty` (shared macros),
  `references.bib`.
- Build artifacts (`.pdf`, `.aux`, …) are git-ignored — see `.gitignore`.

## Why this is its own repo

Split out from the DUET monorepo so it can sync with **Overleaf** via GitHub:
Overleaf clones a whole repo (no subfolder selection), and the monorepo's
Signal Desktop fork (~3,800 files) exceeds Overleaf's limits. This repo is the
**source of truth** for the LaTeX; the monorepo includes it as a git submodule
at `thesis/`.
