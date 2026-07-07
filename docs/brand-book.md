# Brand Book Reference

Distilled from the official **Heliotec Visual Identity / Brand Guide**
(`Heliotec_Identitet_2026_22.01.pdf`, dated 22.01.2026, 58 pp). Key source
pages are rendered in [`brand-book-pages/`](brand-book-pages/) for quick
reference (palette, CTA/shapes, typography rules). This is the
**authoritative** source. Where it disagrees with the reverse-engineered
tokens (which were derived from the live site), the book wins — see
[Reconciliation](#reconciliation-book-vs-live-site) at the bottom for the
specific conflicts, because the live site currently diverges in several
material ways.

---

## Brand strategy & voice

- **Archetype:** the *Controller* (like Rolls-Royce, Harvard) — calm,
  confident, strong messages, inspiring, visionary. **Avoids slang and jargon.**
- **Language:** British English, Oxford grammar.
- **Personality (4):** Innovative · Practical · Transparent · Customer-centered.
- **Belief:** empowerment through energy — "Take control of your energy."
- **Positioning:** future-focused energy solutions with gravitas; a strategic
  energy partner, not just a vendor. "We are more than a company. We are a
  movement."

## Logo

- **Concept:** square (stability, reliable infrastructure) + circle (energy
  flow, movement, renewables). Hand-drawn, sleek, modern.
- **Clear space:** minimum = **X**, where X = the height of the "h" in the
  Heliotec logotype. No text, imagery, icons, borders, or graphics may enter it.
- **Minimum sizes:** digital **120 px** wide; print **25 mm** wide. If space is
  tight, adjust layout hierarchy rather than shrinking the logo.
- **Colour:** white logo on dark/saturated backgrounds; dark logo on light.
- **Never:** stretch/compress, recolour outside the palette, add
  gradients/shadows/outlines/effects, rotate/skew, place on low-contrast
  backgrounds, alter typography, put it inside undefined shapes, or use it
  inline in a sentence.

## Tagline

- **"Take control of your energy"** — positioned beneath the logo on a modular
  square grid: **1 square = width of a primary logo letter**; vertical spacing
  between logo and tagline = 1 square (2X minimum).

## Colour (see `tokens/brand-colors.css` for all values + ramps)

| Name | Hex | Role |
|---|---|---|
| **ENERGY** | `#EAF672` | **Lead.** Neon yellow, "active flow of energy." Use strategically. PANTONE 923 C |
| **VOLTAGE** | `#4A52F2` | Accent. Electrifying blue for highlights. PANTONE 2726 C |
| **ALARM** | `#FF6A61` | Accent. Red for CTAs, urgency, dynamic highlights |
| **DATA** | `#160F3A` | Secondary. Deep purple, used in gradients |
| **TECH** | `#5A5D5B` | Secondary. Authoritative dark-grey anchor |
| **LED** | `#6DD9FD` | Secondary. Luminous glow blue for light sources in imagery |
| **CLOUD** | `#EDEDE3` | Secondary. Clean, open light surface |
| **CONCRETE** | `#F7F7EF` | Near-white surface / deep-black backgrounds (see note below) |

- Every accent/secondary ships a **10-step tint ramp**; LED and CONCRETE have
  extra support colours (`LED MEDIUM/DARK/DARKEST`) for glow effects.
- **Gradients** are a deep purple→indigo glow built from the DATA family
  (`#0D002C → #261D52 → #0F1C7C → #3B589E`), used as dynamic backgrounds.
- *Note:* the palette page labels CONCRETE `#F7F7EF` but also prints
  "R:0 G:0 B:0 (Ordinary black)" beside it — the book treats near-white
  CONCRETE and a deep-black background as a paired system; the live site's
  practical deep background is `#0A0C14`.

## Call to action (the composite CTA)

The book's CTA is **not** a plain button — it's a composite the site does not
yet implement:

- **One outline** encloses a **topic text + a button**, side by side.
- **Topic text** (left) in **CLOUD**; begins exactly where the outline's rounded
  corner ends.
- **Button** (right): fill is **always ENERGY 100%** (non-negotiable), text in
  **BLACK, uppercase** (e.g. `GET STARTED`).
- **Outline stroke:** a **gradient from Cloud (left) → Energy (right)** for the
  primary; solid Cloud for the secondary.
- **Shape:** stadium — corner radius **relies on the box height** (fully rounded).
- **Clear space:** equal on top/bottom/right; left is defined by the topic text.
- One or two lines of topic text are both supported.

## Typography

- **Typeface: Helvetica Neue** — chosen for neutrality, modernity,
  trustworthiness. Used for headlines, body, captions, infographics.
- **Headline weight by format** (important, and counter to the live site):
  - **Large-scale** (posters, billboards, hero): **Regular or Medium** — light
    weights read as confident and premium at size. Bold is for emphasis only.
  - **Medium** (presentations, web sections, print ads): **Medium** default.
  - **Small-scale** (digital ads, social, banners): **Bold** for impact in
    limited space.
- **Split-colour headlines:** part white, part ENERGY yellow — yellow marks the
  single most important word/idea; white carries the rest.
- **Kicker / section label:** short bracketed labels, e.g. `[ + GENERATION ]`.
- **Glowing circle bullets:** bullet points render as subtle luminous circles.
- **Yellow quotation marks / indicators** act as visual anchors for quotes.
- Subheadlines in grey where possible; body in black/grey/white per contrast.

## Iconography

- **Stroke weights: wide 6 px, narrow 4 px.** Two versions: **Primary** (ENERGY
  colour — stands alone) and **Secondary** (TECH 50% — supportive on cards).
- Either can sit on a **dark-grey circle** when used on light backgrounds.
- Official set (~50): Solar, Charge, Arrow Up/Down, Statistics, Candlestick
  graph, Global technology, Re-useability, Industry, Hospitality, Public
  services, Residential, New build, FAQ, Socket, Truck, Conveyer belt, Charging
  station, Cloud storage, Carbon capture, Search, Retail, Carbon savings, Power,
  Hexagon, Sponsorship, Generation, Storage, Monitoring, Reporting, Optimisation,
  Grid, Green energy, Sourcing, Energy, Heliotec logo, Heliotec emblem,
  Distribution, Fork lift, Process, Dimmer switch, Supply level, Electricity
  meter, Cross, V-sign, +Solutions, Charging vehicle.
  *(The repo's `icons/` currently holds ~28 of these as PNGs — see gap in
  Reconciliation.)*

## Content cards / highlight chips

- Background **CONCRETE 100%**, card **CONCRETE 95%**.
- Body text + icon in **TECH 50%**; headline **two-colour Cloud/Energy**.
- Circular **plus/minus** expand buttons; add a **drop shadow** on cards so they
  lift off the background. Fold-out reveals extra content ("+" to expand).

## Graphs & infographics

- Primary chart colours: **yellow (lead) + grey**; accents to differentiate
  segments.
- **Graph lines styled like the icons**; **glowing dots** at line ends mark key
  data points. Blue/purple glows reinforce the high-tech identity.

---

## Reconciliation: book vs live site

The existing tokens were reverse-engineered from heliotec.energy. The brand book
is authoritative, and the live site diverges from it in these material ways —
worth a decision on each:

1. **VOLTAGE blue.** Book `#4A52F2` (PANTONE 2726 C). Site drifts to `#4A54F2` /
   `#4B4EDE`. → Use the book value for brand work; treat the site value as
   implementation drift.
2. **TECH grey.** Book `#5A5D5B`. The reverse-engineered system used `#555555`.
   → Book value is canonical.
3. **CTA pattern.** Book = composite *topic-text + Energy button in one
   gradient-outlined stadium*. Site = plain 8 px lime buttons in primary/
   secondary pairs. → These are genuinely different components; the site has not
   implemented the brand CTA. Decide whether to migrate the site or keep the
   simpler button as a documented web-pragmatic variant.
4. **Headline weight.** Book = Regular/Medium at large scale, Bold only for
   small formats. Site + current style guide = Extrabold (800) heroes. → Direct
   conflict; the book prefers lighter, more premium large headlines.
5. **Deep background.** Book palette centres on CONCRETE (near-white) + a
   deep-black/DATA gradient system; site uses a flat `#0A0C14` near-black. →
   Keep `#0A0C14` as the practical UI background but source marketing
   backgrounds from the DATA gradient.
6. **Icon coverage.** Book defines ~50 icons in Primary + Secondary + circled
   variants at 6/4 px strokes; the repo has ~28 PNGs in grey/yellow/blue only.
   → Gap worth closing if the full set is available as assets.
