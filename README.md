# Discrete Mathematics — Homework 1–4

LaTeX sources for a Discrete Mathematics course. Each homework folder contains the assignment source (`hwX.tex`), a short README for that assignment, and optional feedback notes.

- Homework 1: [Homework 1/README.md](Homework%201/README.md) · source: [Homework 1/hw1.tex](Homework%201/hw1.tex) · feedback: [Homework 1/feedback.md](Homework%201/feedback.md)
- Homework 2: [Homework 2/README.md](Homework%202/README.md) · source: [Homework 2/hw2.tex](Homework%202/hw2.tex) · feedback: [Homework 2/feedback.md](Homework%202/feedback.md)
- Homework 3: [Homework 3/README.md](Homework%203/README.md) · source: [Homework 3/hw3.tex](Homework%203/hw3.tex) · images: [Homework 3/images](Homework%203/images) · feedback: [Homework 3/feedback.md](Homework%203/feedback.md)
- Homework 4: [Homework 4/README.md](Homework%204/README.md) · source: [Homework 4/hw4.tex](Homework%204/hw4.tex) · feedback: [Homework 4/feedback.md](Homework%204/feedback.md)

License: [LICENSE](LICENSE)

## Prerequisites

- TeX distribution (TeX Live recommended) with `pdflatex` and `latexmk`
- Optional: VS Code with the “LaTeX Workshop” extension for one-click builds

## Build

From within any homework folder, run one of the following:

- latexmk (recommended)

```bash
latexmk -pdf hw1.tex   # or hw2.tex, hw3.tex, hw4.tex
```

- Or `pdflatex` (run multiple times as needed for references)

```bash
pdflatex hwX.tex
```

The output PDF will be generated alongside the `.tex` file (e.g., `hw1.pdf`).

## Clean

Remove generated files for a given homework:

```bash
latexmk -C hwX.tex
```

## Notes

- Ensure required images exist before building (e.g., `Homework 3/images/checkerboard.png`, `Homework 3/images/dominos.png`).
- If a `.synctex(busy)` file is present (e.g., `hw1.synctex(busy)`), close any open PDF viewers and rebuild. If builds get stuck, try `latexmk -C` followed by `latexmk -pdf`.

---

If you want a repository-wide `.gitignore` for LaTeX artifacts, consider adding typical patterns like `*.aux`, `*.log`, `*.synctex*`, `_minted*`, and `*.fdb_latexmk`. This repo currently tracks some build artifacts per the homework folders; adjust as you prefer. 
