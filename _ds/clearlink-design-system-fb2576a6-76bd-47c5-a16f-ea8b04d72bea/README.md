# Clearlink Design System

**Clearlink** is a Utah-based performance marketing agency. Their pitch: *"A performance marketing partnership that delivers."* Unlike a traditional agency, Clearlink's business model emphasizes **performance over everything else** — they get paid for results (conversions, not hours), which makes them highly strategic about SEO, paid media, content, and an in-house sales center that closes on chat and phone.

This folder captures the brand's visual system, tone of voice, component library, and a UI kit recreation of the `clearlink.com` marketing surface, so design agents can create on-brand work end-to-end.

## Sources this system was built from

- **Figma file:** `Clearlink.com _performance-marketing.fig` — mounted as a VFS. One page, two frames: `Performance-Marketing — desktop` (1440×3393) and `Performance-Marketing — mobile`. Contains the `clearlink-blue` logo symbol, Standard/Hero/Input button variants, Block Card, Hero section, "Our Services" nav, Accordion FAQ, and Footer.
- **Brand color notes provided by the user:** `#1990FF` (Clearlink Blue), `#0A73EB`, `#0F5CBE`; dark grays `#212121` / `#3D3D3D`; neutrals `#F6F6F6 / #E7E7E7 / #D1D1D1`; black on white for body; Poppins (ExtraLight for headlines, Bold for emphatic headlines).
- **Uploaded fonts:** Full Poppins family in `fonts/`.

> ⚠️ **Font substitution note:** The Figma file uses **Averta Std** (and one stray ATT Aleck Sans). The user instructed us to use **Poppins** — so the system is built on Poppins, and the Figma type is treated as spec for *size, weight, and spacing*, not family. If Averta Std is the real production font, swap the `@font-face` declarations in `colors_and_type.css`; the type scale and weights map 1:1.

---

## Index

| File | What's in it |
|---|---|
| `README.md` | This file — brand context, content fundamentals, visual foundations, iconography |
| `DESIGN.md` | **Portable design dials** — colors, type, spacing, imagery + full photography catalog, voice. The single hand-off file. |
| `SKILL.md` | Cross-compatible skill entry point for Claude Code / Agent Skills |
| `colors_and_type.css` | All color + type CSS vars, `@font-face` rules, base typography |
| `fonts/` | Poppins TTFs (full family, 18 files) |
| `assets/logos/` | `clearlink-logo.svg` — primary wordmark |
| `assets/icons/` | `linkedin.svg`, `youtube.svg` (social) — see Iconography section |
| `assets/images/` | Hero photo, paid-media collage, card imagery (B&W portraits) |
| `preview/` | Design-system cards (colors, type, components, etc.) |
| `ui_kits/clearlink-com/` | Marketing site UI kit — index.html + JSX components |

---

## Content Fundamentals

### The One Clearlink Voice

Clearlink's voice conveys **confidence that comes from knowledge and experience**, with the foresight to always keep an eye on the future. We present information through the viewpoint of a **problem solver, facilitator, and encourager** — never a vendor reading off a brochure.

#### Signature cues

The voice has four signatures. Every piece of copy should land somewhere inside this rectangle:

| Cue | Is | Is **not** |
|---|---|---|
| **Expert** | proficient, experienced, confident | pretentious, condescending, clinical |
| **Mindful** | inclusive, thoughtful, genuine | pandering, overstated, divisive |
| **Dedicated** | invested, responsible, enthusiastic | untrue, overworked, obsessive |
| **Clear** | concise, accessible, transparent | indirect, inconsistent, vague |

If a sentence drifts toward any "is not" — cut it. The voice exists on a spectrum, and the edge of "pretentious" or "pandering" is the wrong side of it.

#### Messaging principles

- **Simple and straightforward language** that stands the test of time. No trend-chasing buzzwords (no "supercharge", "unleash", "revolutionary", "synergy", "10x", "next-gen").
- **Speak with authority.** We know what we're talking about — say it directly. *"We'll find the customers for you."* Not *"We may be able to help you potentially find customers."*
- **Welcoming and approachable.** Professional, never stiff. Mindful, never preachy.
- **Confidence without arrogance.** *"Our paid media team gets results."* — not *"We're the best in the business."* Let the numbers do the bragging.

### Voice in practice

- **Voice:** We / you. Never "I". The agency speaks as a collective; the reader is always "you" / "your brand".
  - *"We'll find the customers for you and drive the metrics that will dramatically grow your business."*
- **Declarative, period-ended.** Headlines land on a full stop, which gives them a "this is settled" vibe — the voice of someone who's done this a hundred times.
  - *"A performance marketing partnership that delivers."*
  - *"More of what makes us tick."*
  - *"Search engine optimization." / "Paid media advertising."*
- **Results-first nouns:** performance, conversions, ROI, growth, customers, results.
- **Plain-English certainty.** *"We are hyper focused on your return on investment."* No hedging ("we try to", "we aim to", "hopefully").
- **Sentence case for everything** — buttons, nav, headlines. **No all-caps** except tiny UI overlines (≤14px).
- **No emoji.** Occasional unicode arrow characters (↓, ›, →) as inline affordances.
  - *"↓  See what we mean  ↓"* (hero CTA)
  - *"More on SEO ›"* (card link)
- **Oxford comma, em-dashes**, conversational contractions ("we'll", "you're", "it's").

**Microcopy patterns**
- Card eyebrow titles are short & declarative: "Dedicated Sales Team: Close the deal", "Automation: Marketing on autopilot".
- Link CTAs on cards use `›` not `→`.
- Hero/standard CTAs are verb-first and concrete: *"Partner With Us"*, *"See what we mean"*.
- FAQ questions are written exactly as a prospect would type them: *"What is a performance marketing agency?"*, *"How much does a performance marketing agency cost?"*
- Form labels + inputs use Title Case for button labels ("Partner With Us"), sentence case for helper text.

**Quick reference: voice test**

Before publishing, ask:
1. Would an **Expert** say this? (Or am I performing expertise?)
2. Would it land for a **Mindful** reader from any background? (Or am I leaving someone out?)
3. Does it sound **Dedicated** — like we'll actually do this? (Or am I overpromising?)
4. Is it **Clear** in one read? (Or do you need to re-read it?)

If any answer is no, rewrite.

---

## Visual Foundations

### Color
- **White is the stage.** Most sections are full-width white with generous vertical padding (`88px` top/bottom desktop). Content never floats on a colored chip.
- **Clearlink Blue (`#1990FF`) is reserved.** It's the logo color, primary buttons, links, and accent — NEVER a background for large areas. When it appears, it's small and confident.
- **Black (`#000`) is the counterweight.** Used for the hero image overlay area, footer, and the "Let's grow together" band. Creates dramatic contrast between sections instead of gradients.
- **Grays build UI, not atmosphere.** `#F6F6F6 / #E7E7E7 / #D1D1D1` live in card borders, input backgrounds, dividers. `#929AA5` is footer link text.
- **No gradients.** Flat color only. Photography is the only "atmospheric" element.

### Typography
- **Poppins ExtraLight (200)** for display and section headlines (48–52px). This is the signature move — big, airy, airy.
- **Poppins Bold (700)** for subheads, card titles, and button text. Short emphatic phrases.
- **Poppins Regular (400)** for body (18px).
- **Negative letter-spacing on display** (`-0.01em`) for tighter optical feel.
- Body line-height is tight-ish (`22–26px` at 18px) — Clearlink body copy stays dense, not airy.

### Imagery
- **Black-and-white portraits**, high contrast, often a headset-wearing call-center rep or team member mid-work. Shot on a black or neutral background so they comp cleanly against the black hero.
- **Environmental, not staged.** People are looking past the camera, working.
- **Product collage:** one hero collage of phones + campaign artwork shows the agency's output. Full-color, confident.
- No illustrations. No iconography-as-imagery. No stock-y gradients.

### Layout
- **1440 grid, 134px side gutters, 1172 content column.**
- **Three-column card grids** at 1172/3 ≈ 372px per card, 28px gaps.
- **Two-column card rows** at 572px each.
- **Sections are stacked horizontal bands.** No side-by-side section layouts.
- **Left-aligned headlines in sections, centered headlines above card grids.**

### Corners, shadows, borders
- **Corners: 4px (buttons) and 8px (cards)**. Pill-shaped radius (999px) reserved for the outlined "Partner With Us" nav chip.
- **No shadows by default.** Cards are defined by whitespace + internal structure, not lift. When a card needs elevation (e.g. modal, dropdown), use `shadow-md: 0 4px 12px rgba(0,0,0,0.08)`.
- **Hairlines only** — `1px solid #E7E7E7`. Borders are used sparingly; whitespace does most of the separation.

### Motion & states
- **Calm, functional motion.** `120ms ease` color fades. No bounces, no parallax.
- **Hover (primary button):** `#1990FF → #0A73EB` darken.
- **Pressed:** `#0F5CBE` deeper blue, no scale change.
- **Hover (link/ghost):** color fades to `#0A73EB`; underline appears on body links (not on nav or CTAs).
- **Accordion expand:** simple `height` + icon toggle (`add_circle` → `do_not_disturb_on`); no easing drama.
- **Nav on dark hero:** white text, 2px white pill border around "Partner With Us" chip. Hover: fills white, text goes blue.

### Transparency & blur
- **Not used.** The hero image is clipped on a solid black section; there is no frosted glass, backdrop-filter, or transparent overlay. High-contrast edges, not dreamy ones.

### Buttons (canonical)
- **Primary (Standard):** `#1990FF` fill, white Bold 18/24 text, **pill radius (`999px`)**, `8px 24px` padding, `40px` tall.
- **Primary (Hero):** same but larger — 24/32 Bold text, pill radius, `16px 48px` padding, `64px` tall.
- **Ghost on dark:** transparent fill, 2px white border, white text, 30px pill radius, 32px tall.
- **Inline link CTA:** Blue text + `›` glyph, no underline, no chip.

### Cards (canonical)
- **Image on top** (3:2 aspect), 8px top corners.
- **24px interior padding**, gap 24 between image + content.
- **Title: Bold 28/36, color `#383D43`** (dark gray, NOT pure black — softens on white).
- **Body: Regular 16/22, color `#383D43`**.
- **Learn More button bottom-left**, Standard Primary variant.

### Footer
- **White background** (yes — unusual: the footer itself is light, and a black "CTA band" sits above it).
- **Columns: Logo | Who We Are | What We Do + Contact | Brands + Join + Privacy | Follow Us (Linkedin + YouTube)**.
- Link text: `#929AA5` (Cool Gray), Regular 16/22. "Follow Us" label is Bold.

---

## Iconography

Clearlink uses a **branded outline icon set** — 50 hand-drawn, single-weight outline icons covering common UI and conceptual needs. The set lives in `assets/icons-brand/` and is the **default icon system** for all Clearlink work.

- **Style:** outline, single-stroke, friendly geometry (rounded terminals, balanced spacing).
- **Variants:**
  - `assets/icons-brand/black/` — 50 outline icons (default, for use on white/light)
  - `assets/icons-brand/blue/` — 46 outline icons + 4 pictograms (Clearlink Blue — for accent / single-icon heroes)
  - `assets/icons-brand/white/` — 46 outline icons + 4 pictograms (for use on dark/blue)
- **Sizing:** designed at ~50×50 source resolution. Render at **24–80px** depending on context; ≥48px when icons sit on their own (stat slides, feature grids), 24–32px inline with text.
- **Color usage:**
  - On **white** backgrounds → use **black** variant
  - On **black/dark/blue** backgrounds → use **white** variant
  - For **accent** in a 2×2 grid or single-icon hero → use **blue** variant
  - Don't recolor with CSS filters; use the correct source file.
- **Pictograms** (white set only): `contact-center`, `international`, `cloud-services`, `connectivity` — these are larger, layered, vertically-stacked illustrations meant for **section dividers** or **service category hero callouts**, not inline. Render at 60–120px.

### Black-only icons (not in blue/white sets)
`pie-chart · pizza · pyramid · search` — only use on light backgrounds, or commission the missing color variants.

### When to use which set
- **Brand icons (this set)** — feature lists, service grids, stat callouts, infographics, anything decorative or conceptual. **Prefer this whenever possible.**
- **Material Symbols Rounded (filled)** — only for system UI affordances Clearlink's set doesn't cover: `add_circle` / `do_not_disturb_on` (accordion), `arrow_right_alt`, `expand_more`. Render at 24px brand blue. Treat this as a fallback, not the default.

### Available icons (50)

`ai · at · attach · award · beaker · bookmark · brain · bubble · calendar · chat · check · cloud · compass · credit-card · data-stack · document · download · eye · fast-forward · files · flag · funnel · gear · gears · give-and-take · global · globe · group · headset · heart · infinity-loop · laptop · lightbulb · lightning · line-graph · link · location · lock · mail · megaphone · microphone · money-up · notification-bell · paper-airplane · pencil-ruler · phone-call · pie-chart · pizza · pyramid · search`

### Social icons (separate)

The two social SVGs in `assets/icons/` (`linkedin.svg`, `youtube.svg`) are footer-only and live outside the brand icon set. Render at 24×24 in `#929AA5`.

## Brand Backgrounds

`assets/backgrounds/` holds canonical **hero/section backgrounds** — black-and-white subject (person + device) anchored bottom-right of a solid-color field with the Clearlink wordmark in a top-centered pill.

| File | When to use |
|---|---|
| `bg-tablet-woman-black.png` | Confident hero on dark — services, performance marketing pitch |
| `bg-tablet-hand-black.png` | Abstract / product-focused hero on dark |
| `bg-hsi-phone-black.png` | Mobile product / case-study hero on dark |
| `bg-tablet-woman-blue.png` | High-energy hero on Clearlink Blue — for callout or campaign slides |
| `bg-phone-woman-blue.png` | High-energy mobile hero on blue |

**Pattern rules:**
- Subject always at right (bottom-right anchor), copy area on left two-thirds.
- The Clearlink wordmark sits in a **rounded pill** at the top-center. Pill is **white-bg + blue logo** on dark/blue fields; **black-bg + white logo** on blue. Don't invent new pill colors.
- These are full-bleed 1920×1080 — drop them into deck slides as `<section class="slide" style="background:url(...) center/cover">` and place copy in the left 60% of the frame.

---

## UI Kits

### `ui_kits/clearlink-com/`
Full recreation of the `clearlink.com` performance-marketing page. Open `index.html`.

Components (all in `.jsx` files, globalised to `window`):

- **Nav** — top navigation on dark hero, ghost pill CTA
- **Hero** — 720px full-bleed B&W photo, 52px ExtraLight headline, hero primary button
- **ServicesSection** — paid-media collage + two service blurbs with `›` CTAs
- **CardGrid / BlockCard** — three image-top cards (8px radius), Learn More button
- **FAQ** — Material Symbols plus/minus accordion; "Expand all" / "Collapse all"
- **Footer** — Black CTA band + white footer with 4-column link grid + social icons

### `ui_kits/slide-deck/`
1920×1080 slide-deck system derived from the **Clearlink Master Slide Deck 2026**. 15 representative slides covering: title, agenda, about-us, section dividers, stat grids, service overview, service breakdown, pull quote, why-partner, process steps, partner logos, author quote, pricing table, meet-our-people, closing CTA. See `ui_kits/slide-deck/README.md` for the slide-only type scale and layout rules.

Open `ui_kits/slide-deck/index.html` — ←/→ to navigate, T for the thumbnail rail.

Interactivity: FAQ expand/collapse, footer email form submit → "Thanks — talk soon.", all buttons hover-darken.

---

## Caveats & open questions

1. **Font family.** Figma = Averta Std; user told us Poppins. Built on Poppins. Swap `@font-face` in `colors_and_type.css` if Averta Std is the real production font.
2. **Icons.** Clearlink uses a very small icon set in the Figma (accordion plus/minus + social). We adopted **Material Symbols Rounded (filled)** to cover general product needs. If the production site uses a different icon font, flag it and we'll rewire `preview/icons.html` + `FAQ.jsx`.
3. **Mobile layout.** The mobile Figma frame exists but no mobile UI kit was built — the desktop kit is 1440px fixed width. Ask if you want a mobile companion.
4. **Imagery** was copied from the Figma as-is. If Clearlink has a higher-res or approved library of brand photography, drop it in `assets/images/` and the cards will pick it up.
