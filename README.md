# Heliotec Design System

A design system reverse-engineered from the live production site at
[heliotec.energy](https://www.heliotec.energy/) (captured 2026-07-06).

Heliotec is an energy management platform for UK multi-site operators
(hospitality, leisure, retail, manufacturing). The visual language leans
utilitarian-tech: near-black navy surfaces, a single high-saturation lime
accent, and a distinctive single-corner "cut" shape used instead of uniform
rounded corners.

## Contents

- [`tokens/colors.css`](tokens/colors.css) — color custom properties
- [`tokens/typography.css`](tokens/typography.css) — font stack, weights, type scale
- [`tokens/layout.css`](tokens/layout.css) — radius, spacing, overlay tokens
- [`tokens/tokens.json`](tokens/tokens.json) — same tokens in a flat JSON format (Style Dictionary / Figma Tokens compatible shape)
- [`style-guide.html`](style-guide.html) — open in a browser to see every token rendered (colors, type scale, buttons, stat blocks, cards, radius scale)
- [`docs/voice-and-content.md`](docs/voice-and-content.md) — tone, copy patterns, real CTA/heading examples
- [`docs/brand-rules.md`](docs/brand-rules.md) — numbered rules for color, the signature cut, typography, layout, and CTAs across web/banner executions
- [`icons/`](icons/) — the actual icon assets downloaded from heliotec.energy (see below)
- [`logo/`](logo/) — white Heliotec wordmark (2500×894 PNG, from the site header)
- [`backgrounds/`](backgrounds/) — brand gradient grounds (ink→indigo glow) used on the site and in ad banners

## How these values were sourced

Colors, font sizes, weights, and border-radii were extracted directly from
the site's compiled CSS bundles (Astro output + legacy Squarespace stylesheets
still loaded on the page) via the live hex codes, `font-size`, `font-weight`,
and `border-radius` declarations actually shipping in production — not
estimated from screenshots. Copy patterns in `voice-and-content.md` are
transcribed from the live page text.

**One caveat:** the site currently loads no custom webfont — it renders in
the system `Helvetica Neue, Arial, sans-serif` stack. That's documented here
as the accurate current state. If you're using this design system to *evolve*
the brand rather than just document it, a distinct display typeface paired
with the existing lime/navy palette would likely strengthen differentiation —
worth a conversation before treating the current type stack as permanent.

## Signature shape

Recurring `border-radius` values like `24px 0 0 0` and `72px 0 0 0` (large
radius on exactly one corner, square elsewhere) are used on image containers
and cards site-wide — this diagonal-cut look is a real brand signature, not
an incidental style, and is preserved here as `--radius-signature-sm` /
`--radius-signature-lg`.

## Icons

`icons/` contains the actual icon assets pulled from the live site (not
recreated approximations):

- `icons/grey/` — the default/inactive state icon set (13 icons, PNG)
- `icons/yellow/` — the same icon set in the lime/yellow accent color, used for active states (11 icons, PNG)
- `icons/blue/` — a smaller set of 4 metric icons (lighting, office, portfolio, sourcing) used in a blue variant
- `icons/ui/` — inline SVGs transcribed from the site's markup: `menu.svg`, `chevron-left.svg`, `chevron-right.svg`, `linkedin.svg`
- `favicon.webp` — the site favicon

Not every icon exists in all three colors (e.g. "Statistics" and "Industry"
only appear in yellow) — only the variants actually shipped are included.
See the "Icons" section in `style-guide.html` for a full visual index.

## Usage

Drop the three token stylesheets into any project:

```html
<link rel="stylesheet" href="tokens/colors.css" />
<link rel="stylesheet" href="tokens/typography.css" />
<link rel="stylesheet" href="tokens/layout.css" />
```

Then reference tokens as CSS custom properties, e.g. `var(--color-lime-400)`,
`var(--font-size-4xl)`, `var(--radius-signature-lg)`.
