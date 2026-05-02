# Quinnipiac University — Computer Science Senior Thesis Template

This template is designed for undergraduate Computer Science students at Quinnipiac University completing their CSC494 Senior Thesis II final paper. It produces a correctly formatted thesis document ready for submission.

---

## Setting Up on Overleaf (Recommended)

Overleaf is the easiest way to use this template since it handles compilation automatically and lets you work from any browser without installing LaTeX locally.

### Upload the zip file

1. Go to [overleaf.com](https://www.overleaf.com) and sign in or create a free account.
2. On your Overleaf dashboard, click **New Project → Upload Project**.
3. Upload the `QU_CS_Thesis_Template.zip` file directly. Overleaf will unzip it automatically.
4. Once the project opens, set the main document to `Thesis.tex`:
   - Click the **Menu** button (top left, three horizontal lines).
   - Under **Settings → Main document**, select `Thesis.tex`.
5. Set the compiler to pdfLaTeX:
   - In the same Menu panel, under **Settings → Compiler**, select `pdfLaTeX`.
6. Click **Recompile**. The template should compile immediately and produce a PDF.
7. Start editing — open `Thesis.tex` first and fill in your name and title.

---

## Quick Start

1. Personalize `Thesis.tex` — fill in your name, thesis title, and degree on the title page.
2. Write your abstract in `Abstract.tex` (75–150 words).
3. Structure your chapters — add, remove, or rename chapter files to match your thesis. Update the `\include{}` calls in `Thesis.tex`.
4. Add your references to `References.bib` following the ACM format examples provided.
5. Recompile in Overleaf by clicking the green **Recompile** button.

> New to LaTeX? Read `LATEX_GUIDE.tex` first. It covers everything you need: figures, tables, equations, code listings, cross-references, and citations — with working examples you can copy directly into your chapters.

---

## File Structure

```
├── Thesis.tex               ← Main file — start here
├── Abstract.tex             ← Abstract (75–150 words)
├── Acknowledgment.tex       ← Acknowledgements
├── Chapter_1.tex            ← Introduction (template provided)
├── Chapter_2.tex            ← Background / Literature Review (template provided)
├── Chapter_3.tex            ← Your first core chapter (template provided)
├── Conclusion.tex           ← Conclusion and Future Directions
├── LATEX_GUIDE.tex          ← LaTeX reference for new users (read this!)
├── Lists.tex                ← Abbreviations and symbols
├── References.bib           ← Bibliography entries
├── ACM-Reference-Format.bst ← Citation style file (do not modify)
└── Images/                  ← Place all figures here
    └── placeholder.png      ← Example — replace with your figures
```

---

## Chapter Structure

This template does **not** enforce a fixed number of chapters. Add or remove chapter files to match your thesis. A typical structure depends on your thesis type:

| Thesis Type | Suggested Structure |
|-------------|---------------------|
| **Research / Survey** | Introduction → Background → Literature Review → Analysis → Conclusion |
| **Systems / Implementation** | Introduction → Background → System Design → Implementation → Evaluation → Conclusion |
| **Experimental / ML / Data Science** | Introduction → Literature Review → Methodology → Results → Discussion → Conclusion |

To add a chapter:
1. Create a new file (e.g., `Chapter_4.tex`) in the project.
2. Add `\include{Chapter_4}` in the appropriate place in `Thesis.tex`.

To remove a chapter: comment out or delete its `\include{}` line in `Thesis.tex`.

The three provided chapter files (`Chapter_1.tex`, `Chapter_2.tex`, `Chapter_3.tex`) are starting points with instructions. Replace their content with your own writing.

---

## Citation Style

This template uses the ACM-SIG 3+ Authors Reference Format with numbered citations.

- In-text: `\cite{smith2024}` produces `[1]`
- Multiple: `\cite{smith2024, jones2023}` produces `[1, 2]`
- In prose: write the author name yourself — `Smith et al. \cite{smith2024}` produces `Smith et al. [1]`

Add your sources to `References.bib`. Examples for every common entry type are provided. See `LATEX_GUIDE.tex` Section 8 for more detail.

For full ACM formatting guidance: https://www.acm.org/publications/authors/reference-formatting

---

## Compiling

### In Overleaf

Set the compiler to pdfLaTeX. Overleaf handles multi-pass compilation automatically so just click **Recompile**.

### Locally (advanced)

Install TeX Live or MiKTeX, then run:

```
pdflatex Thesis
bibtex Thesis
pdflatex Thesis
pdflatex Thesis
```

Four passes are required for cross-references and bibliography to resolve correctly.

---

## Page Layout

| Setting | Value |
|---------|-------|
| Font size | 12pt |
| Paper | A4 |
| Left margin | 40mm (wider for binding) |
| Other margins | 25mm |
| Line spacing | One-and-a-half |
| Page numbers | Centered in header, all pages |

---

## Troubleshooting

### "The PDF does not update after I edit a file."

Click the green **Recompile** button, or enable **Auto-compile** in the Overleaf menu.

### "I see `??` instead of a number in a cross-reference."

Your `\label{}` key does not match your `\ref{}` key. Check for typos and capitalization differences.

### "My bibliography is not showing up."

Try clicking **Recompile** twice. If the issue persists, check the logs & output files panel in Overleaf for BibTeX errors.

### "I see `[?]` instead of a citation number."

The key in your `\cite{}` does not exist in `References.bib`, or the key is misspelled.

### "I added a figure but it does not appear."

Check that the image file is inside the `Images/` folder and that the filename in `\includegraphics{Images/yourfile.png}` matches exactly, including capitalization and extension.

### "My special character is causing an error."

Characters like `%`, `$`, `&`, `_`, `#`, `{` need a backslash: `\%`, `\$`, `\&`, `\_`, `\#`, `\{`. See `LATEX_GUIDE.tex` Section 11.

---

## Questions?

Consult your thesis advisor or the Department of Computer Science at Quinnipiac University.

---

## Attribution

This template was created by Brooks Alexander Jackson (Quinnipiac University, May 2026) for the CSC494 Senior Thesis II course in the Department of Computer Science.

The LaTeX structure was adapted from the KAUST Official Thesis Template, available at:
https://www.overleaf.com/latex/templates/kaust-official-thesis-template/mrcyxjvwpqdn

The KAUST template is used under its original open terms. The Quinnipiac-specific formatting, chapter scaffolding, instructional content, and citation style configuration are original contributions of this template.
