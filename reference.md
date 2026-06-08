# Cardinal Design Reference

Live site: https://trycardinal.ai/  
Replica: `C:\Users\tinsl\cardinal-replica`

## Colors

| Name | Value | Use |
|------|-------|-----|
| cream | `#fcf7f5` | Secondary surfaces |
| blush | `#f3ded9` | Hero H1, nav CTA |
| orange | `#f96633` | Accents, radar, corners |
| darkRed | `#630704` | Hero, footer |
| brown | `#533e3d` | Body, H2 |
| testimonialCard | `#fa64320d` | Quote cards |
| footerCta | `#f3eeed` | Footer CTA section |
| heroCtaBg | `rgba(250, 100, 50, 0.4)` | Hero button |
| navBorder | `rgba(242, 221, 216, 0.2)` | Nav CTA border |
| lightBorder | `rgba(84, 63, 61, 0.2)` | Light buttons |
| emailButtonBg | `rgba(250, 100, 50, 0.1)` | Footer email button |

## Layout

- Section max-width: `1000px` (`max-w-[1000px]`)
- Page max-width: `1200px`
- Section padding: `py-[100px] max-xl:py-20 max-md:py-[72px]`
- Breakpoints: mobile ≤799px, tablet 800–1199px, desktop ≥1200px

## Assets

| Asset | URL |
|-------|-----|
| Nav logo | `https://framerusercontent.com/images/3PFDikI2Ov2LfpI40hKguxAGrpw.png` |
| Footer wordmark | `https://framerusercontent.com/images/oloTtuJTgF5XaHrugVDBvmJWU.png` |

Hero customer logos (logo strip only, not nav):
- `fryHUvC7hPtaOj9be2LY7iQVUUI.png`
- `d2FBNUL6sHP9gp6XaH6Gis5H2E.png`
- `ONoj0DdG4fZP9lm1HminvgJezNI.png`
- `q3ynQczQClPl90lHApEGwv4q6M.png`
- `z7jfAH8bXSq7Kjqc8rdn4I7nPa8.png`

**Wrong:** `d2FBNUL6` as nav logo. **Wrong:** `3PFDik` as hero graphic.

## Fonts (Framer CDN + Google)

```
Libre Caslon:  framerusercontent.com/assets/EQWaTNALCQPCpHfp0iD2fo11FWI.woff2
Retni Medium:  framerusercontent.com/assets/9rcSuhpbbrUFKUpqUAZgT66Xq8.woff2
Retni Bold:    framerusercontent.com/assets/E5Ltcr76oMO5Y4HTNu5qn8MGyk.woff2
Roboto Mono:   fonts.gstatic.com (see cardinal-replica/src/index.css)
```

## External links

- Book a demo: `https://tally.so/r/5BzXOo`
- Email: `team@trycardinal.ai`
- Arcade Labs: `https://arcade.la/?ref=cardinal`

## Page order

1. Nav → 2. Hero → 3. Testimonials → 4. Footer CTA → 5. Footer

## Component specs

### nav (`Nav.tsx`)
- Fixed, transparent, max-width 1000px
- Logo 140px, white links, `Button variant="nav"`

### hero (`Hero.tsx`)
- Bg `#630704`, height 850px (660px mobile)
- Radar animation, concentric rings, glow orb, notification cards, logo strip
- Copy bottom-center; H1 blush; subtitle white/60%
- `Button variant="hero"` — BOOK A DEMO

### notification-card (`NotificationCards.tsx`)
- Roboto Mono 12px uppercase, bracket SVG icon
- Blush or orange text; desktop only

### testimonial-card (`TestimonialCard.tsx`)
- Bg `#fa64320d`, orange 2px corner accents
- Quote: Retni 18px, top-center
- Author: Roboto Mono uppercase, bottom-left, 50% opacity

### testimonials (`Testimonials.tsx`)
- White bg, static grid (not marquee), max-width 1000px
- `Button variant="light"` — "See more customers"

### footer-cta (`FooterCTA.tsx`)
- Bg `#f3eeed`, concentric circle SVGs
- `Button variant="light"`

### footer (`Footer.tsx`)
- Bg `#630704`, copyright at 30% white
- `Button variant="email"` — team@trycardinal.ai
- Wordmark at 50% opacity

### button (`Button.tsx`)

| Variant | Style |
|---------|-------|
| `nav` | Blush text, `rgba(242,221,216,0.2)` border, Retni Bold |
| `hero` | Roboto Mono uppercase, `rgba(250,100,50,0.4)` bg |
| `light` | Brown text, `rgba(84,63,61,0.2)` border, Retni Bold |
| `email` | Blush text, `rgba(250,100,50,0.1)` bg, mailto |

## Section background rules

| Context | Background |
|---------|------------|
| Default content | `white` |
| Warm accent band | `#f3eeed` |
| Dark brand | `#630704` |
| Card surface | `#fa64320d` |
