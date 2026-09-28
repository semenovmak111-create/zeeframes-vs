# ZeeFrames — "Platform vs your own site"

A drop-in comparison section for zeeframes.com: three stats and five numbered rows
"platform / your own site". Live demo:
https://semenovmak111-create.github.io/zeeframes-vs/
(`?theme=light` shows the cream variant).

## Embed

1. Copy the `<section class="zvs" id="platform-vs-site">…</section>` block from `index.html`.
2. Add `vs.css` to the page `<head>`. No JavaScript is needed.
3. For the cream section add the modifier: `<section class="zvs zvs--light" …>`.

The block uses the fonts the site already loads (Geologica for the numbers,
Inter Tight, Inter) and the tokens from `colors.css` (`--color-primary`,
`--color-black-300`, `--color-base-border`, `--color-base-muted`, …) with fallbacks.
All classes are prefixed `zvs-`. No external dependencies.
The side gutter can be overridden with `--zvs-gutter` (60 / 40 / 24 px by default).

## What it is built from

- Section header of the service pages (`.tool-section-header`): lime eyebrow,
  36/44 title, muted paragraph on the right.
- Stat cards of the /about hero (`.about-card-common`, `.hero-counter`): 48 px number,
  the unit in lime at 36 px weight 300; the "0 ₽" card carries the lime glow of the
  "10+ years" card and the dark label chip.
- Numbered rows of "Six reasons why 90% of our clients come back" on /about
  (`.value-item`): number / title / muted text, 0.6 px hairlines, the whole row turns
  lime on hover — exactly as on /about.

## Behaviour and accessibility

- Rows are an `<ol>`; each pair is a `<dl>` with "Площадка" / "Свой сайт" terms.
  On desktop the terms are visually hidden (the column header says it); below 992 px
  they are shown above each text, so a pair never splits.
- 992 px and below: stats stay in three columns, each row shows the pair side by side.
  Below 768 px stats stack; below 576 px the pair stacks, platform first.
- Nothing moves, so there is nothing to switch off for `prefers-reduced-motion`.
