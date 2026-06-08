---
name: cardinal-design-system
description: >-
  Builds UI matching Cardinal (trycardinal.ai): tokens, typography, components,
  and layout. Use when adding pages, sections, or components for Cardinal-branded
  UI, marketing sites, trycardinal.ai, or cardinal-replica.
---

# Cardinal Design System

## Before editing

1. Read [reference.md](reference.md) for component specs and assets.
2. Read matching files in `C:\Users\tinsl\cardinal-replica\src\components\`.
3. Reuse `Button.tsx` variants — do not invent new button styles.
4. Match layout/copy from https://trycardinal.ai/ (Framer original), not assumptions.

## Quick tokens

| Token | Value | Use |
|-------|-------|-----|
| Orange | `#f96633` | Accents, radar, corners |
| Dark red | `#630704` | Hero, footer |
| Blush | `#f3ded9` | Hero H1, nav CTA text |
| Brown | `#533e3d` | Body, H2 |
| Card surface | `#fa64320d` | Testimonial cards |
| Footer CTA bg | `#f3eeed` | Warm neutral sections |
| Section bg | `white` | Default content sections |

Breakpoints: mobile ≤799px, tablet 800–1199px, desktop ≥1200px (`md:` / `xl:`).

Layout: section max-width **1000px**, page **1200px**, padding `py-[100px]` / `max-xl:py-20` / `max-md:py-[72px]`.

## Typography (Tailwind classes)

| Role | Classes |
|------|---------|
| H1 | `font-serif text-[56px] leading-[110%] text-cardinal-blush max-xl:text-[48px] max-md:text-[30px]` |
| H2 | `font-serif text-[40px] leading-[120%] tracking-[-0.5px] text-cardinal-brown max-xl:text-[32px] max-md:text-2xl` |
| Body | `font-sans text-base tracking-[-0.02em] leading-[1.4]` |
| Quote | `font-sans text-lg leading-[1.4] tracking-[-0.02em] text-cardinal-brown` |
| Hero CTA | `font-mono text-base font-medium tracking-[0.05em] text-white uppercase` → **BOOK A DEMO** |
| Badge | `font-mono text-xs uppercase` (blush or orange) |
| Author | `font-mono text-[13px] leading-[1.3] tracking-[-0.02em] uppercase opacity-50 text-cardinal-brown` |

Nav/CTA buttons: Retni Sans Bold, sentence case ("Book a demo").

## Component reuse

| Need | Use |
|------|-----|
| CTA link | `Button` variant: `nav` / `hero` / `light` / `email` |
| Quote card | `TestimonialCard.tsx` |
| Dark hero | `Hero.tsx` (radar, rings, bottom-anchored copy, logo strip) |
| Testimonials section | `Testimonials.tsx` (static grid, white bg) |
| Warm CTA band | `FooterCTA.tsx` |
| Footer | `Footer.tsx` |

Full per-component specs: [reference.md](reference.md).

## New section workflow

1. Pick the closest existing component in [reference.md](reference.md).
2. Choose background: `white` (default), `#f3eeed` (warm), `#630704` (dark), `#fa64320d` (card).
3. Use H2 + body/quote typography from table above.
4. Reuse `Button.tsx` variant (`light` for most CTAs; `hero` only in dark-red hero).
5. Add to `cardinal-replica/src/components/`, wire in `App.tsx`.
6. Run verification checklist below.

## Verification checklist

- [ ] Colors: `#f96633`, `#630704`, `#f3ded9`, `#533e3d`
- [ ] Nav logo: `3PFDikI2Ov2LfpI40hKguxAGrpw.png` (not `d2FBNUL6`)
- [ ] Hero: radar + rings, not product screenshot
- [ ] Hero CTA: uppercase Roboto Mono
- [ ] Testimonials: static grid, `#fa64320d` cards, white section bg
- [ ] Authors: Roboto Mono uppercase, not Retni Sans
- [ ] Footer CTA: `#f3eeed` background
- [ ] No Inter, gradients, marquee, or generic white shadow cards

## Anti-patterns

- Marquee testimonials, Inter font, purple gradients
- White shadow cards instead of `#fa64320d`
- Product screenshot in hero
- Wrong nav logo (`d2FBNUL6` — use `3PFDik`)
- Roboto Mono orange for names/body copy
- Cream background on testimonial section

## Additional resources

- [reference.md](reference.md) — tokens, assets, component specs
- [examples.md](examples.md) — section templates
- Live site: https://trycardinal.ai/
- Replica: `C:\Users\tinsl\cardinal-replica`
