# Brand Rules

Rules for applying the Heliotec design system across web, banners, and other
executions. Sourced from measured production CSS on heliotec.energy
(2026-07-06) plus agreed working rules. Each rule notes its origin: **[site]**
= measured from production, **[ours]** = decided for this design system.

## Color

1. **Ink 900 is the default surface.** Dark sections dominate; cream sections
   are the breather between them. **[site]**
2. **Lime 400 is a single accent, not a theme.** It appears as: primary CTA
   fill, key stat numbers, active icon state, and at most one full "callout
   moment" per page. Never two adjacent lime sections. **[site]**
3. **On Lime 400, everything inverts to Ink 900** — text, icons, and buttons
   (primary CTA on lime is ink-filled with lime text). Never white text on
   lime. **[site]**
4. **Stat blocks always sit on Lime 400** with ink-900 content. **[ours]**
5. **Indigo is for links and small highlights only** — never large fills in
   marketing surfaces (the blue metric icons are the one exception). **[site]**
6. **Imagery gets a scrim.** Text over photography requires an overlay:
   `#00000026` for hero backgrounds, up to `rgba(0,0,0,0.55)` gradient scrims
   where copy sits directly on the image. **[site]**

## The signature cut

7. Two shapes, one rule: **signature-lg (`72px 0 0`) only on full-width
   blocks; signature-sm (`24px 0` — the diagonal cut) on everything
   narrower.** [ours, shapes from site]
8. The cut corner is always **top-left**. Don't mirror or rotate it.
9. Pills (`9999px`) are for eyebrow chips and tags only — never buttons.
   Buttons are always `8px`. **[site]**

## Typography

10. **The text stack is fixed:** uppercase eyebrow (0.75–0.85rem, weight 500,
    0.1em tracking) → extrabold headline (line-height 1.15) → one sentence of
    subtext → CTA pair. Nothing else between headline and CTAs. **[site]**
11. **Uppercase is reserved for eyebrows.** Headlines, buttons, and body are
    sentence case (`text-transform: none` is explicit on buttons in
    production). **[site]**
12. **Numbers do the persuading.** Stats render at display sizes
    (2.86–6.4rem, weight 800) with a small quiet label under them — never
    inline in a paragraph. **[site]**
13. Body copy stays at 1rem/1.4–1.5 and never exceeds ~600px measure. **[site]**

## Layout

14. **Containers:** hero 1467px (gutter `calc(100% − 8vw)`), standard content
    1200px, narrow text 900px, prose 600px. **[site]**
15. **Section padding tiers:** 80/40 desktop, 60/24 tablet, 48/20 mobile.
    Heroes get extra headroom (160px top). **[site]**
16. **Hero is a 50/50 split** — text stack left, product image right,
    60px gap. **[site]**
17. **Stat sections are ⅓ + ⅔:** one feature stat block (⅓ width) beside
    supporting copy or secondary stats, 48px gap. **[site]**
18. **Alternate dark/light down the page** — Ink 900 hero, cream proof
    section, ink capabilities, one lime moment, cream case studies, ink
    footer. **[site]**
19. **Gap scale:** 16px between CTAs and small items, 32px between stacked
    cards, 48px between layout columns, 60px in the hero. **[site]**

## CTAs (web and banners)

20. **CTAs travel in pairs:** lime primary + outline secondary, 16px apart.
    On dark: secondary is lime-outlined. On light: secondary is ink-outlined.
    On lime: primary inverts to ink fill. **[site]**
21. Buttons: 8px radius, 2px border (transparent on primary so heights
    match), 700 weight, ~0.85rem label, min-width 120px, `9px 28px` padding.
    Hover is an opacity dip (0.85), not a color change. **[site]**
22. Banner executions with room for only one button use the lime primary.
    The secondary never appears alone. **[ours]**

## Banner quick recipe

Ink 900 ground · eyebrow in lime · extrabold sentence-case headline in
cream/white · one stat at display size if space allows (on a lime
signature-sm block) · lime primary CTA at 8px radius · scrim any photography.
