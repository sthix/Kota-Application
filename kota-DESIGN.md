# Kota — Style Reference
> oat-paper desk with a violet rubber stamp — benefits paperwork made friendly, and one decisive purple mark per view

**Theme:** light (with one charcoal band and a black footer)

Source measurements are normalized; roles and recommendations are interpreted. Font summary lists are independent, not paired by position. HTML examples are reconstructions, not source components.

Kota reads like warm stationery for an HR team: the page sits on an oat-paper canvas of #fdfaf6, and content floats in a slightly darker linen (#f9f5f0) inside 1px parchment rules (#efe8de). Nothing is pure white by default. White (#ffffff) is kept for "inner" surfaces such as product screenshots and the hover state of cards, so stepping from cream to white reads as a card being lifted. The type voice is a single geometric grotesk, Neue Faktum, used *light* (300) for running copy and *medium* (500) for headings. The 300 body weight on a warm ground makes long benefits explanations feel unhurried rather than corporate. Colour is rationed to one stamp: violet #7546d5 marks the primary CTA, the announcement bar, and the lavender chips (#eeebfa ground, #7546d5 text). Everything else is ink black, near-black #222222, or cream. Depth comes from tone changes (cream → white, cream → charcoal #222222 → black footer), almost never from shadows. Shapes are soft but disciplined: 8px on cards and ghost buttons, 12px on the violet CTA, 16px on the floating nav pill, and fully round 100px on nav-link hover states.

## Tokens — Colors

| Name | Value | Token | Role |
|------|-------|-------|------|
| Oat Paper | `#fdfaf6` | `--color-oat-paper` | Page canvas (`--_semantic---background--page`). The warm, barely-there cream every section sits on; never replace it with white |
| Linen | `#f9f5f0` | `--color-linen` | Secondary surface (16 occurrences): floating nav bar, benefit cards, hero frame (at 50% alpha), "how it works" panels. One step darker than the canvas, so it reads as a raised sheet |
| Parchment Rule | `#efe8de` | `--color-parchment-rule` | The default 1px border (19 occurrences) on blocks, benefit wraps and panels. Also the nav-link hover fill. Warm hairline, never grey |
| Stamp Violet | `#7546d5` | `--color-stamp-violet` | The only chromatic accent (12 backgrounds, 17 text): primary "Book a demo" CTA, top announcement bar, chip text, timeline lines. Rationed to roughly one mark per viewport |
| Deep Violet | `#4c269a` | `--color-deep-violet` | Pressed/outlined edge of the violet button (`#4b1f85` border) and dark "New Product" badges. Used only next to Stamp Violet |
| Lavender Wash | `#eeebfa` | `--color-lavender-wash` | Chip and tag ground (14 occurrences): benefit-type chips, timeline "Today" tags. Also the hero section wash at 50% alpha |
| Ink | `#000000` | `--color-ink` | Primary text (73 occurrences): h1, body paragraphs, stats. Also the black nav CTA and the footer band |
| Graphite | `#222222` | `--color-graphite` | Nav link text (21) and the full-bleed dark "How to get started" band |
| Pencil | `#333333` | `--color-pencil` | Secondary text: "Log in", ghost button labels, eyebrow labels (11 occurrences) |
| Chalk | `#fbfaf2` | `--color-chalk` | Text on dark surfaces (25 occurrences): footer links, dark-band headings. Footer meta uses 60% alpha |
| Pebble | `#c6c6c1` | `--color-pebble` | 1px border on ghost/secondary buttons ("Watch video"). Hover switches it to Ink |
| Paper White | `#ffffff` | `--color-paper-white` | Inner surfaces (22): video/screenshot frames, FAQ blocks, benefit-card hover. Also text on violet |
| Lime Highlighter | `#e7fe77` | `--color-lime-highlighter` | `--_semantic---brand--accent`. Appears in illustrations and product imagery (lime card stacks), not in UI chrome. Rare but on-brand |

## Tokens — Typography

### Neue Faktum (V2) — the single brand voice, a geometric grotesk with round bowls and a friendly single-storey feel. Light 300 for reading, Medium 500 for headings · `--font-brand`
- **Substitute:** Figtree (Google Fonts). Weight mapping: 300 → 300, 400 → 400, 500 → 600, 700 → 700. Figtree runs slightly lighter, so step headings up one weight
- **Weights:** 300, 400, 500
- **Sizes:** 10px, 12px, 13px, 14px, 16px, 18px, 20px, 22px, 24px, 28px, 38px, 42px, 48px
- **Line height:** 1.0 on the h1 (48/48), ~1.15 on h2 (38/43.5, 48/56), 1.2 on h3 (28/33.6), 1.4–1.5 on body (16/22.4, 16/24, 18/27)
- **Letter spacing:** -0.02em on the h1 and the FAQ heading (-0.96px at 48px, -0.84px at 42px); normal everywhere else
- **Role:** Body copy is weight 300 at 16–18px, an anti-convention for a fintech/insurance product (most use 400). It gives explanations a soft, approachable texture on the cream ground. Headings use 500, not bold. The brand never shouts above 500 in UI text

### Faktum Neue — legacy cut used for eyebrow labels and timeline tags only · `--font-label`
- **Substitute:** same as above (Figtree 600)
- **Weights:** 500
- **Sizes:** 12px, 14px
- **Line height:** 1.5
- **Letter spacing:** normal (eyebrows are typed uppercase in the source, e.g. "HOW IT WORKS")
- **Role:** Small uppercase section eyebrows above h2s, and "Today / Tomorrow / This week" timeline tags

### Type Scale

| Role | Family | Weight | Size | Line Height | Letter Spacing | Token |
|------|--------|--------|------|-------------|----------------|-------|
| micro | Neue Faktum | 300 | 10px | 15px | — | `--text-micro` |
| eyebrow | Faktum Neue | 500 | 12px | 18px | — (uppercase) | `--text-eyebrow` |
| chip | Neue Faktum | 500 | 13px | 19.5px | — | `--text-chip` |
| caption | Neue Faktum | 300 | 14px | 19.6px | — | `--text-caption` |
| body | Neue Faktum | 300 | 16px | 24px | — | `--text-body` |
| body-lg | Neue Faktum | 300 | 18px | 27px | — | `--text-body-lg` |
| subheading | Neue Faktum | 400 | 24px | 33.6px | — | `--text-subheading` |
| heading-sm | Neue Faktum | 500 | 28px | 33.6px | — | `--text-heading-sm` |
| heading | Neue Faktum | 500 | 38px | 43.5px | — | `--text-heading` |
| heading-lg | Neue Faktum | 500 | 48px | 56px | — | `--text-heading-lg` |
| display | Neue Faktum | 500 | 48px | 48px | -0.96px | `--text-display` |

## Tokens — Spacing & Shapes

**Density:** comfortable (generous section padding, tight 6–16px inside components)

### Spacing Scale

| Name | Value | Token |
|------|-------|-------|
| 4 | 4px | `--spacing-4` |
| 6 | 6px | `--spacing-6` |
| 8 | 8px | `--spacing-8` |
| 12 | 12px | `--spacing-12` |
| 16 | 16px | `--spacing-16` |
| 24 | 24px | `--spacing-24` |
| 32 | 32px | `--spacing-32` |
| 48 | 48px | `--spacing-48` |
| 56 | 56px | `--spacing-56` |
| 80 | 80px | `--spacing-80` |
| 100 | 100px | `--spacing-100` |

### Border Radius

| Element | Value |
|---------|-------|
| buttons (violet CTA) | 12px |
| buttons (ghost / nav black) | 8px / 10px |
| inputs | 8px |
| cards | 8px (benefit cards 9px, panels 12px) |
| tags | 5px (chips), 8px (timeline tags) |
| nav bar | 16px |
| nav links | 100px |
| global | 8px |

### Layout

- **Page max-width:** 1340px container (nav pill 1264px)
- **Section gap:** 80–100px
- **Card padding:** 32px 56px (blocks), 30px 27px (panels), 6px (chips)
- **Element gap:** 16px

## Components

### Announcement Bar
**Role:** Site-wide promo strip above the nav

Full-bleed, 34px tall, #7546d5 background, centred 14px/21px weight 300 white text with a trailing "→". This is the only place violet fills edge to edge, so it works as the brand's "stamp" at the very top of every page.

### Floating Nav Pill
**Role:** Primary navigation

A 68px-tall bar, max 1264px wide, centred with margin from the edges. #f9f5f0 fill, 1px #f5efe8 border, 16px radius, no shadow. Kota wordmark at left. Links in the centre: 16px weight 500 #222222, padding 8px 14px, 100px radius, hover fill #efe8de. At right, "Log in" in #333333 weight 300, then a black CTA: #000000 fill, white 16px/400, padding 8px 12px, 10px radius, 1px rgba(198,198,193,.4) border, 42px tall. Sticky while scrolling.

### Primary Button (Violet)
**Role:** Main conversion action ("Book a demo")

#7546d5 fill, 1px #7546d5 border (or #4b1f85 on the secondary variant), white 16px weight 400, padding 10px 20px (46px tall) or 12px 20px (50px). 12px radius, 4px icon gap, no shadow. Never more than one per view.

### Ghost Button
**Role:** Secondary action ("Watch video", "Speak with an expert")

Transparent fill, 1px #c6c6c1 border, 8px radius, 16px weight 400 #333333 text, padding 10–12px 20px. Hover changes only the border colour to #000000. No fill change, no lift.

### Benefit Chip
**Role:** Category labels under the hero and inside panels

#eeebfa ground, #7546d5 text at 13px weight 500, 19.5px line height, 6px padding, 5px radius. Sits in a horizontal wrap with 8–10px gaps, and may itself be framed by a 1px rgba(0,0,0,.15) 9px-radius outline on #f9f5f0.

### Benefit Card
**Role:** Clickable benefit tile (Health Insurance, Pension, …)

#f9f5f0 fill, 1px rgba(0,0,0,.15) border, 9px radius, 6px padding, a 32px icon at 4px radius, and the label in 16–24px weight 300–400. Hover: background to #ffffff, border to #ebe2f5, scale(1.01). This is the system's signature "cream → white lift".

### Hero Frame
**Role:** Contains the h1 and the integration diagram

A large rounded sheet: rgba(249,245,240,.5) on a rgba(238,235,250,.5) lavender section wash, 1px rgba(154,154,154,.5) border, rounded only at the bottom (0 0 14px 14px) so it hangs from the nav. Padding 220px 0 100px. The diagram around it uses dashed violet (#7546d5) connector lines and 6px violet dots.

### Section Eyebrow + Heading
**Role:** Introduces each content section

Eyebrow in 12px weight 500 uppercase #333333 with 16px space below. Then an h2 at 38px weight 500 / 43.5px, left-aligned and wrapped to a max of 600px, often three lines. Body follows in 18px weight 300 / 27px.

### Dark Band
**Role:** Process / "how to get started" timeline

Full-bleed #222222 section. Centred eyebrow in white, h2 at 48px weight 500 in #fbfaf2. Timeline items have violet #eeebfa tags, Chalk headings at 28px/500, and screenshot cards in white with 10px radius and a 1px #d9d9d9 border.

### Footer
**Role:** Sitemap and regulatory text

#000000 band. A 4-column link grid: headings 22px weight 400 #fbfaf2, links 16px weight 300 / 22px #fbfaf2. Column dividers 1px rgba(251,250,242,.2). Legal text 10–12px weight 300 at 60% chalk.

### FAQ Row
**Role:** Expandable question

White block, 1px #ebebed bottom border, question in 18–20px weight 400, chevron at right, 0 padding (the row spacing comes from the inner wrap). Max width 756px.

## Do's and Don'ts

### Do
- Put every page on #fdfaf6 and every raised sheet on #f9f5f0 with a 1px #efe8de border. Depth is cream on cream
- Set body copy in weight 300 at 16px/24px or 18px/27px. Headings use 500, never 700
- Use #7546d5 for exactly one primary action per view and for chips (#eeebfa ground + #7546d5 text)
- Use the black #000000 10px-radius button for persistent nav CTAs, and violet 12px-radius buttons for in-content CTAs
- Show hover by changing tone (cream → white, border pebble → ink, nav-link → #efe8de pill), not by adding shadow
- Keep h1 at 48px/48px with -0.02em tracking. On mobile, keep 48px and centre the hero
- Frame product UI and screenshots in white with 8–10px radius and a 1px #d9d9d9 border, so they read as real software on paper
- Use dashed violet connectors and small violet dots to show integrations and flows

### Don't
- Never use pure white #ffffff as the page background. It kills the warm oat-paper register
- Never use grey borders like #e5e7eb on cream surfaces. Borders are warm (#efe8de, #f5efe8) or alpha-black rgba(0,0,0,.15)
- Never add drop shadows to cards or buttons. The only real shadows on the site are the third-party chat bubble and one inset tab
- Never set UI text above weight 500. The voice is calm, never bold
- Never introduce a second saturated accent in the UI. Lime #e7fe77 lives in imagery, and green #2c5451 appears only as a semantic success colour
- Never use radii above 16px on containers (only nav-link pills go to 100px). Corners stay soft but not bubbly
- Never centre long body paragraphs on desktop. Sections are left-aligned with a 600px text column, and only hero and dark-band headings centre
- Never put violet text on the violet surface. On #7546d5, text is always #ffffff

## Surfaces

| Level | Name | Value | Purpose |
|-------|------|-------|---------|
| 0 | Oat Paper | `#fdfaf6` | Page canvas |
| 1 | Linen | `#f9f5f0` | Nav pill, cards, panels: the raised sheet |
| 2 | Paper White | `#ffffff` | Screenshot frames, FAQ, hovered card: the topmost sheet |
| 3 | Lavender Wash | `#eeebfa` | Chips and hero wash: tinted, branded zones |
| inv-1 | Graphite | `#222222` | Dark process band |
| inv-2 | Ink | `#000000` | Footer |

## Elevation

Kota has almost no shadow system. Of 1,700 elements, only two carry a box-shadow, and both are incidental (an inset tab and the Intercom launcher). Elevation is tonal: #fdfaf6 → #f9f5f0 → #ffffff, each step outlined by a warm 1px rule. Interactive lift is shown by changing tone and adding a tiny scale(1.01), never by a shadow. For drama the page cuts to a charcoal #222222 band and ends on a black footer, which reads like turning the page over rather than raising it.

## Imagery

Three kinds of imagery, all friendly and none stock-corporate:
1. **Product UI**: real Kota dashboards and mobile screens, often on colourful flat backdrops (sky blue, lime) with 8px radius.
2. **Brand-logo constellations**: provider logos (Irish Life, Vitality, Allianz) and HRIS app icons as rounded-square tiles, joined by dashed violet lines to a violet Kota mark.
3. **Hand-drawn mascots**: a purple dartboard, clouds and arrows in a loose illustrated style with violet as the dominant fill, placed at section edges.

Video blocks use 8px radius. No photography of people in the hero, no gradients over imagery.

## Layout

A 1340px max container with 60px side padding (16px on mobile). The nav is a floating pill inset from the edges and sticky on scroll. The hero is a single rounded sheet hanging from the nav: a two-column composition with logos at left and right and copy centred, or copy left with the diagram right. On mobile it stacks and centres. Sections alternate between a left text column (max 600px) with a visual on the right, and 2×2 feature grids of large image cards (730px) with a 28px/500 heading and 16px/300 copy below. One full-bleed dark timeline band sits in the middle third of the page, then testimonials and FAQ on cream, then the black footer. Vertical rhythm is 80–100px between sections and 16px between elements.

## Agent Prompt Guide

Quick Color Reference:
- text: `#000000` (nav `#222222`, secondary `#333333`)
- background: `#fdfaf6`
- surface: `#f9f5f0` / `#ffffff`
- border: `#efe8de` (buttons `#c6c6c1`)
- accent: `#7546d5` on `#eeebfa`
- muted text: `#969696`
- primary action: `#7546d5` (nav action `#000000`)

Example Component Prompts:

1. Create a floating nav: max-width 1264px, centred, 68px tall, background #f9f5f0, 1px solid #f5efe8 border, 16px radius, no shadow. Links in Figtree 16px weight 500 #222222, padding 8px 14px, radius 100px, hover background #efe8de. Right side: "Log in" in 16px/300 #333333, then a button with #000000 fill, #ffffff 16px/400 text, padding 8px 12px, radius 10px.
2. Create a primary CTA: background #7546d5, 1px solid #7546d5, #ffffff text in Figtree 16px weight 400, padding 10px 20px, height 46px, radius 12px, no shadow. Pair it with a ghost button: transparent, 1px solid #c6c6c1, #333333 text, radius 8px, hover border #000000.
3. Create a benefit chip row: chips with #eeebfa background, #7546d5 text at 13px weight 600 (Figtree), padding 6px, radius 5px, gap 8px, each optionally wrapped in a #f9f5f0 frame with 1px rgba(0,0,0,.15) border and 9px radius.
4. Create a feature panel: background #f9f5f0, 1px solid #efe8de, radius 12px, padding 30px 27px. Eyebrow 12px weight 600 uppercase #333333, h3 28px weight 600 #000000 line-height 1.2, body 16px weight 300 line-height 1.5. Inner screenshot frame #ffffff, 1px #d9d9d9, radius 10px.
5. Create a dark process band: full-bleed #222222, centred h2 48px weight 600 #fbfaf2 line-height 1.17, timeline tags #eeebfa / #7546d5 14px weight 600 radius 8px padding 4px 6px, footer of the band transitions to #000000.

## Gradient System

There is no UI gradient system. The only gradients are utility fades in the page colour, used to soften the logo marquee edges: `linear-gradient(90deg, rgba(253,250,246,0), rgba(253,250,246,.7) 50%, #fdfaf6)`. There is also a hairline divider on dark that fades chalk in and out: `linear-gradient(90deg, rgba(251,250,242,0), rgba(251,250,242,.2) 16%, rgba(251,250,242,.2) 84%, rgba(251,250,242,0))`. Colour never comes from gradients.

## Similar Brands

- **Deel (deel.com)**: HR-software warmth with a single purple-violet accent, though Deel uses white grounds and bolder headlines
- **Pleo (pleo.io)**: friendly fintech with illustrated mascots and soft cream surfaces, but Pleo leans into multiple pastel accents
- **Hibob (hibob.com)**: playful HR brand with rounded shapes and purple, though more saturated and gradient-heavy
- **Mercury (mercury.com)**: calm, low-shadow financial UI with light-weight type, cooler and greyer in palette
- **Remote (remote.com)**: benefits/HR positioning with soft rounded cards on warm neutrals and a single blue accent

## Quick Start

### CSS Custom Properties

```css
:root {
  /* Colors */
  --color-oat-paper: #fdfaf6;
  --color-linen: #f9f5f0;
  --color-parchment-rule: #efe8de;
  --color-stamp-violet: #7546d5;
  --color-deep-violet: #4c269a;
  --color-lavender-wash: #eeebfa;
  --color-ink: #000000;
  --color-graphite: #222222;
  --color-pencil: #333333;
  --color-chalk: #fbfaf2;
  --color-pebble: #c6c6c1;
  --color-paper-white: #ffffff;
  --color-lime-highlighter: #e7fe77;

  /* Typography — Font Families */
  --font-brand: 'Neue Faktum', 'Figtree', ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
  --font-label: 'Faktum Neue', 'Figtree', ui-sans-serif, system-ui, sans-serif;

  /* Typography — Scale */
  --text-micro: 10px;       --leading-micro: 15px;
  --text-eyebrow: 12px;     --leading-eyebrow: 18px;
  --text-chip: 13px;        --leading-chip: 19.5px;
  --text-caption: 14px;     --leading-caption: 19.6px;
  --text-body: 16px;        --leading-body: 24px;
  --text-body-lg: 18px;     --leading-body-lg: 27px;
  --text-subheading: 24px;  --leading-subheading: 33.6px;
  --text-heading-sm: 28px;  --leading-heading-sm: 33.6px;
  --text-heading: 38px;     --leading-heading: 43.5px;
  --text-heading-lg: 48px;  --leading-heading-lg: 56px;
  --text-display: 48px;     --leading-display: 48px;  --tracking-display: -0.02em;

  /* Typography — Weights */
  --font-weight-light: 300;
  --font-weight-regular: 400;
  --font-weight-medium: 500;

  /* Spacing */
  --spacing-4: 4px;  --spacing-6: 6px;  --spacing-8: 8px;  --spacing-12: 12px;
  --spacing-16: 16px; --spacing-24: 24px; --spacing-32: 32px; --spacing-48: 48px;
  --spacing-56: 56px; --spacing-80: 80px; --spacing-100: 100px;

  /* Layout */
  --page-max-width: 1340px;
  --section-gap: 80px;
  --card-padding: 32px;
  --element-gap: 16px;

  /* Named Radii */
  --radius-buttons: 12px;
  --radius-ghost: 8px;
  --radius-nav-cta: 10px;
  --radius-inputs: 8px;
  --radius-cards: 8px;
  --radius-panels: 12px;
  --radius-tags: 5px;
  --radius-nav: 16px;
  --radius-pill: 100px;
  --radius-global: 8px;

  /* Surfaces */
  --surface-canvas: #fdfaf6;
  --surface-raised: #f9f5f0;
  --surface-top: #ffffff;
  --surface-tint: #eeebfa;
  --surface-inverted: #222222;
  --surface-footer: #000000;
}
```

### Tailwind v4

```css
@theme {
  /* Colors */
  --color-oat-paper: #fdfaf6;
  --color-linen: #f9f5f0;
  --color-parchment-rule: #efe8de;
  --color-stamp-violet: #7546d5;
  --color-deep-violet: #4c269a;
  --color-lavender-wash: #eeebfa;
  --color-ink: #000000;
  --color-graphite: #222222;
  --color-pencil: #333333;
  --color-chalk: #fbfaf2;
  --color-pebble: #c6c6c1;
  --color-paper-white: #ffffff;
  --color-lime-highlighter: #e7fe77;

  /* Typography */
  --font-brand: 'Neue Faktum', 'Figtree', ui-sans-serif, system-ui, sans-serif;
  --font-label: 'Faktum Neue', 'Figtree', ui-sans-serif, system-ui, sans-serif;

  /* Typography — Scale */
  --text-micro: 10px;
  --text-eyebrow: 12px;
  --text-chip: 13px;
  --text-caption: 14px;
  --text-body: 16px;
  --text-body-lg: 18px;
  --text-subheading: 24px;
  --text-heading-sm: 28px;
  --text-heading: 38px;
  --text-heading-lg: 48px;
  --text-display: 48px;

  /* Spacing */
  --spacing-4: 4px;
  --spacing-6: 6px;
  --spacing-8: 8px;
  --spacing-12: 12px;
  --spacing-16: 16px;
  --spacing-24: 24px;
  --spacing-32: 32px;
  --spacing-48: 48px;
  --spacing-56: 56px;
  --spacing-80: 80px;
  --spacing-100: 100px;
}
```
