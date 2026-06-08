# UC Davis Slides Template

A Beamer presentation template in the UC Davis house style — Aggie Blue + Aggie
Gold palette, gold accent rule under frame titles, blue section-divider slides,
and a College of Engineering logo in the top-right of every content slide.

All content is **placeholder**, so the deck compiles out of the box with no
external images (only the bundled `coe_logo.jpg`).

## Files

| File | Purpose |
|------|---------|
| `presentation_template.tex` | The template (edit this) |
| `coe_logo.jpg` | College of Engineering mark shown in the header |
| `presentation_template.pdf` | Compiled preview |

## Build

Compile with **two `pdflatex` passes** — the corner logo and title-page band use
`remember picture` overlays, which need a second pass to position correctly:

```sh
pdflatex presentation_template.tex
pdflatex presentation_template.tex
```

## Customize

1. Edit `\title` / `\subtitle` / `\author` / `\institute` and the
   `\footercontent{...}` block near the top of the preamble.
2. Replace each `Placeholder …` line and every `\placeholderfig{...}` with your
   real content / `\includegraphics{your_figure.png}`.
3. Add or remove `\section{}` and `\begin{frame}{}` blocks as needed.

### Helper commands

- `\placeholderfig[height]{label}` — labeled gray box standing in for a figure.
- `\highlightbox{text}` — the blue goal/takeaway callout.
- `\coemark` — the white-bordered College of Engineering logo (header corner).

The COE logo only appears on slides that have a header bar — not on the title
slide, section dividers, or the thank-you slide.
