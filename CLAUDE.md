# Talk: Connections between Multigroup Fairness and Learning

A 20–25 minute talk (plus 5–10 min questions) at MSR, given by Varun Kanade
(University of Oxford). An overview of the connections between multigroup
fairness and learning, covering HKRR and Gopalan et al. The
speaker's own work features only briefly: the main results of CGKR ("How
Global Calibration Strengthens Multiaccuracy") and some results from KK09.

## Layout
- `talk.tex` — main file; only `\input`s the preamble and sections.
- `preamble.tex` — theme, colours, notation macros. Add new macros here.
- `sections/NN-name.tex` — one file per section, numbered in talk order.
  Each opens with a `\section{...}`, which drives the outline slides
  (shown after the title and at the start of every later section).
- `notes/` — photos of handwritten notes, named `YYYY-MM-DD-topic.jpg`.
  Each section file starts with a `% Source:` comment naming its photo(s).

## Workflow
- New notes arrive as phone photos: save the photo in `notes/`, transcribe
  faithfully into a new or existing section file, and flag anything that
  was changed or interpreted (e.g. a range or symbol that looked wrong).
- Build with `latexmk -pdf talk.tex`. Build output (including `talk.pdf`) is
  not committed: derivative files stay out of the repo.
- Small, descriptive commits ("add HKRR multiaccuracy definition").

## Style
- Minimalist: white background, one blue accent (`accent`), grey (`muted`)
  for asides. No navigation symbols, page numbers only.
- Few words per slide; let the maths carry it. Use `\pause` sparingly.
- Use the macros in `preamble.tex` (`\X`, `\D`, `\F`, `\err`, `\Prob`, `\E`)
  rather than raw symbols.
- Never hard-code slide numbers: put `\slidelabel{name}` in the target frame
  and write `slide~\slideref{name}`.
- Budget roughly one slide per minute: aim for ~20–25 content slides total.
