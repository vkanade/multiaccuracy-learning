# MSR talk: How Global Calibration Strengthens Multiaccuracy

A 20–25 minute talk (plus 5–10 min questions) at MSR, based on the paper
"How Global Calibration Strengthens Multiaccuracy". Also covers prior work:
CDV '24, Gopalan et al., and HKRR.

## Layout
- `talk.tex` — main file; only `\input`s the preamble and sections.
- `preamble.tex` — theme, colours, notation macros. Add new macros here.
- `sections/NN-name.tex` — one file per section, numbered in talk order.
- `notes/` — photos of handwritten notes, named `YYYY-MM-DD-topic.jpg`.
  Each section file starts with a `% Source:` comment naming its photo(s).

## Workflow
- New notes arrive as phone photos: save the photo in `notes/`, transcribe
  faithfully into a new or existing section file, and flag anything that
  was changed or interpreted (e.g. a range or symbol that looked wrong).
- Build with `latexmk -pdf talk.tex`. Build output (`talk.pdf`) is committed
  so the latest deck is viewable on GitHub from a phone.
- Small, descriptive commits ("add HKRR multiaccuracy definition").

## Style
- Minimalist: white background, one blue accent (`accent`), grey (`muted`)
  for asides. No navigation symbols, page numbers only.
- Few words per slide; let the maths carry it. Use `\pause` sparingly.
- Use the macros in `preamble.tex` (`\X`, `\D`, `\F`, `\err`, `\Prob`, `\E`)
  rather than raw symbols.
- Budget roughly one slide per minute: aim for ~20–25 content slides total.
