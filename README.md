# ZeeFrames — "Platform vs your own site"

A drop-in comparison section for zeeframes.com: three stats and two lists side by side —
five minuses of renting a place on a platform and five pluses of your own site. Live demo:
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
- The "What's included" bento of the service pages (`.services-offer-grid`): the platform
  is a dark cell (lime glow from the corner on hover), your site the white CTA cell
  (`.service-offer-cta`, turns lime on hover), each with a 44 px `.card-icon`.
  In the cream variant the platform is white and your site is the black CTA cell of Process.
- List rows are FAQ rows: hairline on top, the FAQ's own 16 px minus / plus icons.
  Point N of the platform stands level with point N of the site (CSS subgrid).

## Behaviour and accessibility

- Each side is a `<section>` with its own heading and a `<ul>` labelled
  "Минусы площадки" / "Плюсы своего сайта".
- Below 768 px the lists stack: platform first, your site under it; stats stack too.
- The only motion is the 0.3 s glow on hover; it is off under `prefers-reduced-motion`.
