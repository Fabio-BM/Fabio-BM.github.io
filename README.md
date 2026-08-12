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

## Publishing on GitHub Pages (free, the standard choice in academia)

1. Create a GitHub account if needed, then create a new **public** repository named
   exactly `YOURUSERNAME.github.io` (e.g. `fabiobmaciel.github.io`).
2. In this folder, run:

   ```
   git init
   git add index.html research.html teaching.html contact.html assets cv/Maciel_CV.pdf cv/Maciel_CV.tex README.md .gitignore
   git commit -m "Academic website and CV"
   git branch -M main
   git remote add origin https://github.com/YOURUSERNAME/YOURUSERNAME.github.io.git
   git push -u origin main
   ```

3. After a minute the site is live at `https://YOURUSERNAME.github.io`.
4. To update later: edit files, recompile the CV if needed, then
   `git add -A && git commit -m "update" && git push`.

Once the site is live, add the URL to the CV header: in `cv/Maciel_CV.tex`,
uncomment the website line in the header block and recompile.

Alternative hosts that serve the same static folder: Netlify (drag-and-drop),
Cloudflare Pages, or your university's personal page space.

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
