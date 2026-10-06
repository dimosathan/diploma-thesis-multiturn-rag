# Retrieval Stability and Deferred Commitment in Multi-Turn Retrieval-Augmented Generation Systems

Diploma thesis of **Dimosthenis Athanasiou**, School of Electrical and Computer Engineering, National Technical University of Athens (NTUA), Artificial Intelligence and Learning Systems Laboratory.

Supervisor: Athanasios Voulodimos, Assistant Professor, NTUA.

The thesis builds on the system paper *AILS-NTUA at SemEval-2026 Task 8: Query Diversity via Nested Reciprocal Rank Fusion and Evidence-Guided Agentic Generation for Multi-Turn RAG* (Proceedings of SemEval-2026). Official results on the SemEval-2026 Task 8 (MTRAGEval) leaderboard:

| Task | Metric | Score | Rank |
|------|--------|-------|------|
| A: Retrieval | nDCG@5 | 0.5776 | 1 / 38 |
| B: Generation (reference passages) | Harmonic Mean | 0.7698 | 2 / 26 |
| C: End-to-end RAG | Harmonic Mean | 0.5409 | 11 / 29 |

The compiled thesis is in [`Diploma_Thesis_D_Athanasiou.pdf`](Diploma_Thesis_D_Athanasiou.pdf).

## Repository structure

```
main.tex                  entry point
used-packages.sty         package configuration
packages/                 NTUA title pages, environments, math commands
references.bib            bibliography (biblatex + biber)
chapters/
  0_before/               title matter, abstracts (EN/GR), acknowledgements
  01_greek/               extended summary in Greek (Chapter 1)
  introduction/           Chapter 2
  background/             Chapter 3
  problem_definition/     Chapter 4
  system_architecture/    Chapter 5
  experimental_evaluation/Chapter 6
  conclusion/             Chapter 7
  bibliography/
figures/, images/         figures and the NTUA logo (EPS)
```

## Building

Requires a TeX Live installation with `biber`, Greek babel support and `epstopdf` (the EPS logo is converted at build time, hence `-shell-escape`):

```bash
pdflatex -shell-escape main.tex
biber main
pdflatex -shell-escape main.tex
pdflatex -shell-escape main.tex
```

On Overleaf: upload the repository contents, set the compiler to pdfLaTeX and the main document to `main.tex`.
