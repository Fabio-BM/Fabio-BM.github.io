# Academic website & CV — Fábio Bentz Maciel

## What's here

- `index.html` (About), `research.html`, `teaching.html`, `contact.html` — the website,
  one page per tab; the CV tab links straight to the PDF. When editing the shared
  header/nav/footer, update it in all four pages.
- `assets/style.css` — shared stylesheet for all pages.
- `assets/fabio-maciel.jpg` — web-sized portrait used by the site (cropped/compressed copy;
  the original `Fábio Maciel.jpg` stays out of git).
- `cv/Maciel_CV.tex` — LaTeX source of the CV (compile with `pdflatex`, run twice).
- `cv/Maciel_CV.pdf` — compiled CV, linked from the website. No photo on the CV, by convention.
- `CV_Fábio_2026_en.docx` — original Word CV (kept for reference, excluded from git).

## Where it lives

- **Site:** https://fabio-bm.github.io
- **Repository:** https://github.com/Fabio-BM/Fabio-BM.github.io (GitHub Pages,
  served from the `main` branch root)
- The GitHub CLI (`gh`) on this machine is authenticated as `Fabio-BM`, so Claude
  Code can push updates, manage the repo, etc.

## Updating the site

1. Edit the HTML/CSS files (and recompile the CV if it changed).
2. Then:

   ```
   git add -A
   git commit -m "describe the update"
   git push
   ```

GitHub Pages redeploys automatically within about a minute of each push.
A custom domain can be added later in the repository's Pages settings.

## Recompiling the CV

```
cd cv
pdflatex Maciel_CV.tex
pdflatex Maciel_CV.tex
```

## Things you may want to add over time

- Paper abstracts and PDF/slides links as work matures.
- A Google Scholar / ORCID / GitHub link in the Contact section.
- Expected PhD completion year in the CV once known.
