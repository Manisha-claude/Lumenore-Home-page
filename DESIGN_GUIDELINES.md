# Lumenore — Design Style Guidelines

> Extracted from `index.html` and `assets/css/v2o/index.css`.
> This document records the **existing** design system as built — colors, type, spacing, components, and patterns — so it can be reused consistently. It is documentation, not a redesign.

---

## 1. Overall Design Style & Visual Tone

A modern, **enterprise SaaS / BI** aesthetic with a premium, editorial feel.

- **Dark-first, with bright "spotlight" sections.** The page opens and closes on a deep navy/violet canvas (`#030d1e` → `#000d22`) and switches to clean white sections (Personas, Pricing, Success, Testimonials) in the middle. Section backgrounds are bridged with smooth multi-stop vertical gradients.
- **Glow & glass accents.** Hero uses translucent "glass" panels (`rgba(255,255,255,.1)` + blur), radial cyan/fuchsia glows, and a cyan-bordered search box.
- **Editorial serif headlines** (Fraunces, light weight) paired with a **clean sans body** (Inter) — the serif/sans contrast is the signature of the brand voice.
- **Subtle motion.** Grain texture overlay, infinite logo marquee, hover lifts, shimmer/pulse in the announcement bar.
- **Color-coded products.** Each product/persona gets its own accent (Violet = Ask Me, Royal Blue = Insights, Turquoise = Data Magnet).

**Tone keywords:** trustworthy, intelligent, premium, calm, data-driven.

---

## 2. Color Palette

All colors are defined as CSS custom properties on `:root` using the Figma-export pattern `var(--Name, #fallback)`.

### Royal Blue ramp (primary brand)
| Token | HEX | RGB | Usage |
|---|---|---|---|
| `--Royal-Blue-Blue-50` | `#e7eef8` | `231,238,248` | Icon tile bg, pill bg, active testimonial bg |
| `--Royal-Blue-Blue-150` | `#b8d0fd` | `184,208,253` | Quote-mark accent |
| `--Royal-Blue-Blue-200` | `#9fbae4` | `159,186,228` | Arc/divider lines (used at low opacity) |
| `--Royal-Blue-Blue-350` | `#5886d0` | `88,134,208` | Gradient bridge stop |
| `--Royal-Blue-Blue-400` | `#4075c9` | `64,117,201` | Gradient mid-stops |
| `--Royal-Blue-Blue-450` | `#2863c3` | `40,99,195` | Active search tag |
| `--Royal-Blue-Blue-500` | `#0e48a5` | `14,72,165` | **Primary action / link / accent** |
| `--Royal-Blue-Blue-550` | `#0c3b87` | `12,59,135` | — |
| `--Royal-Blue-Blue-600` | `#0a3578` | `10,53,120` | — |
| `--Royal-Blue-Blue-750` | `#07214b` | `7,33,75` | Hello bar bg, link hover |
| `--Royal-Blue-Blue-850` | `#04142d` | `4,20,45` | Story arrows, dark stops |
| `--Royal-Blue-Blue-900` | `#030d1e` | `3,13,30` | **Page base background / nav** |

### Violet ramp (secondary brand)
| Token | HEX | RGB | Usage |
|---|---|---|---|
| `--Violet-Violet-50` | `#f0ebf7` | `240,235,247` | Ask Me pill bg |
| `--Violet-Violet-250` | `#b499d7` | `180,153,215` | Feature-card border |
| `--Violet-Violet-450` | `#7747b6` | `119,71,182` | "Request a Demo" border, gradient start |
| `--Violet-Violet-500` | `#55298e` | `85,41,142` | Active product accent, stat block, bottom glow |
| `--Violet-Violet-550` | `#4d2580` | `77,37,128` | Page-finale gradient top |

### Sky Blue / Turquoise (highlight)
| Token | HEX | RGB | Usage |
|---|---|---|---|
| `--SkyBlue-SkyBlue-50` | `#e7f8fe` | `231,248,254` | Data Magnet pill bg |
| `--SkyBlue-SkyBlue-500` | `#12b6f8` | `18,182,248` | **Hover/link highlight**, footer headings, logo accent |
| `--Turquoise-SkyBlue-50` | `#e8f6fa` | `232,246,250` | Chip border |
| `--Turquoise-SkyBlue-500` | `#1ca9c9` | `28,169,201` | Data Magnet accent, search border, glows |

### Core / Neutrals
| Token | HEX | Usage |
|---|---|---|
| `--Penn-Blue` | `#001040` | Deep accent |
| `--Absolute-Black` | `#212121` | Body text on light (also used as `#242424`) |
| `--Base-White` | `#fcfcfc` | **Primary text on dark / white surfaces** |
| `--Grey-Grey-100` | `#fbfbfb` | Near-white text |
| `--Grey-Grey-200` | `#f7f7f7` | Feature-card bg |
| `--Grey-Grey-600` | `#bbbbbb` | Tab borders |
| `--Grey-Grey-700` | `#8c8c8c` | Inactive tab border |
| `--Grey-Grey-800` | `#5e5e5e` | Muted text, search-tag border |
| `--Grey-Grey-900` | `#2f2f2f` | — |
| `--Map-Grey` | `#eaeaea` | Card borders, chip text, FAQ answer text |

### Blue-grey & "cool" greys (used in hero search + dashboard mock)
| Token | HEX | Usage |
|---|---|---|
| `--blueGray-200` | `#E2E8F0` | Placeholder text |
| `--blueGray-400` | `#94A3B8` | Bubble border |
| `--blueGray-500` | `#64748B` | — |
| `--blueGray-600` | `#475569` | Source bubble bg |
| `--blueGray-700` | `#334155` | Icon/tools button bg |
| `--cool-101828` | `#101828` | **Default heading color**, dark stat text |
| `--cool-6a7282` | `#6a7282` | Secondary body text (light) |
| `--cool-99a1af` | `#99a1af` | Tertiary/label text |
| `--cool-e5e7eb` | `#e5e7eb` | Card / tab borders (light) |
| `--cool-f9fafb` | `#f9fafb` | Dashboard inner panels |
| `--cool-d1d5dc` | `#d1d5dc` | Decorative quote marks |

### Standalone semantic colors (literal values in CSS)
| Color | HEX | Usage |
|---|---|---|
| Success green | `#009966` | Positive delta in dashboard |
| Star gold | `#fbbf24` | Testimonial rating stars |
| Tab text grey | `#404450` | Pricing tab labels |
| Role text grey | `#505050` | Testimonial role text |
| Footer-end navy | `#000d22` | Page bottom |

### Gradient tokens
| Token | Definition | Usage |
|---|---|---|
| `--AI-Agents-Text` | `linear-gradient(83.02deg, #4AE7FF 51.42%, #4075C9 63.25%, #E879F9 76.03%)` | "AI Agents" gradient headline text |
| `--Search-Glow` | `linear-gradient(86.83deg, #22d3ee 0.77%, #3b82f6 50%, #e879f9 99.23%)` | Blurred glow behind hero search |
| `--Explore-Button` | `linear-gradient(270deg, #7747b6 0%, #4075c9 50.7%, #1ca9c9 100%)` | **Primary gradient buttons** |
| `--Compare-Button` | same as Explore | Pricing CTA |
| `--Tab-Bar-Bg` | `linear-gradient(165.59deg, #ffffff 2.41%, #eef4ff 100.51%)` | Pricing tab-bar container |
| `--Active-Tab-Bg` | `linear-gradient(157.45deg, #e9eff8 2.41%, #d9e3f5 100.51%)` | Active pricing tab |

**Page background** is a stack of 4 radial glows (cyan top, fuchsia upper-left, blue upper-right, violet bottom) over a vertical navy gradient. The **page-finale** block uses `linear-gradient(180deg, #4D2580 0%, #031430 30%, #000D22 100%)`.

---

## 3. Typography

Two families loaded from Google Fonts:

```
Fraunces  — opsz 9..144, weights 300/400/500/600  (serif, headings)
Inter     — weights 300/400/500/600/700           (sans, body/UI)
Material Symbols Rounded                            (icons, optional)
```

### Family assignment
- **`h1–h4`** → `'Fraunces', serif`, `font-weight: 300`, `font-variation-settings: 'SOFT' 0, 'WONK' 1`, default color `#101828`.
- **`h5, h6, p, a, li, button, input`** → `'Inter', sans-serif`.
- **`body`** → Inter, color `--Base-White`, antialiased (`-webkit-font-smoothing: antialiased`).

### Type scale (as used)
| Role | Font | Size | Line-height | Weight |
|---|---|---|---|---|
| Hero H1 | Fraunces | 52px (inline override 48px) | 62px (58px) | 300 |
| Section H2 | Fraunces | 32px | 44.8px | 300 |
| H3 / sub-headings | Fraunces | 24px | 28–33.6px | 300 |
| Card title (h5) | Fraunces | 20px | 30px | 400 |
| Section sub | Fraunces | 20px | 30px | 300 |
| Big stat number | Fraunces | 52px | 62px | 300 |
| Hero sub | Inter | 20px | 30px | 400 |
| Body / paragraph | Inter | 15px | 26px | 400 |
| Pricing tab | Inter | 18px | — | 400 |
| Story title | Inter | 18px | 27px | 500 |
| Buttons / bold UI | Inter | 15px | 25px | 700 |
| Nav links | Inter | 15px | 26px | 400 |
| Captions / chips / labels | Inter | 12px | 16px | 400 |
| Eyebrow | Inter | 11px | 16.5px | 400, uppercase, letter-spacing 1.165px |
| Small label (footer/legal) | Inter | 14px | 20px | 400 |

**Letter-spacing notes:** eyebrows and uppercase labels use `letter-spacing: .12em` (footer headings/links) or `1.165px` (story eyebrow); some small text uses slight negative tracking (`-.15px` to `-.5px`). Brand wordmark uses `.12em`.

---

## 4. Layout & Grid System

- **Container:** `.container { max-width: 1500px; margin: 0 auto; padding: 0 32px; }` (inline page override sets 1500px width + 40px gutters). Inner content blocks (hero, pricing, stories) cap at **1280px**; testimonial card at **1200px**.
- **Full-bleed bars** (hello bar, header) use a calc gutter to align content to the 1500px zone while keeping the background full width.
- **CSS Grid** drives the multi-column layouts:
  | Section | `grid-template-columns` |
  |---|---|
  | Products | `290px 490px 1fr` (gap 64px) |
  | Personas content | `1fr 1fr` (gap 64px) |
  | Dashboard body | `1fr 148px` |
  | Pricing panel | `420px 1fr` |
  | Stories carousel | `40px 1fr 40px` |
  | Trust row | `1fr auto` |
  | Before-you-decide | `370px 590px` |
  | Footer nav | `1.3fr repeat(5, 1fr)` |
- **Flexbox** drives bars, tab lists, chip rows, card internals, carousels (`.features-track`, `.stories-track` are horizontal flex strips).

---

## 5. Spacing & Padding Scale

Spacing is broadly an **8px-based scale** with a few editorial large values. Common values observed:

`4 · 6 · 8 · 10 · 12 · 14 · 16 · 20 · 24 · 28 · 32 · 40 · 48 · 56 · 64 · 72 · 80 · 120` (px)

- **Container gutters:** 32px (desktop) / 24px (≤991) / 20px (≤575).
- **Section vertical padding:** ~120px desktop default (e.g. `.section-products`, `.section-pricing`, `.section-success`); inline overrides tighten to 88–130px. Reduces to ~64–90px on tablet.
- **Common gaps:** card internals `16px`; chip rows `8–10px`; grid columns `64px`; tab lists `8–20px`.
- **Card padding:** feature card `32px 24px 24px`; story body `24px`; testimonial card `64px 32px`; persona dash `29px`; stat block `32px`.

---

## 6. Border Radius

| Radius | Where |
|---|---|
| `4px` | Hello badge, chart bars (top corners) |
| `8px` | Buttons, product tabs, feature cards, icon tiles |
| `~8.9px` | Hero inner search box |
| `10px` | Pricing inner tab |
| `12px` | Hero search shell, pricing-right card, footer ask-AI box, contact CTA |
| `14px` | Feature icon tile, pricing tab-bar, dashboard chat |
| `16px` | Persona tab, story card, testimonial card/tab, contact CTA, persona-tab |
| `18px` | Pricing stat block |
| `24px` | Persona dashboard card |
| `40px / 50px` | Pills & chips (fully rounded) |
| `50% / 200px / 350px` | Circular: nav arrows, source bubbles, social icons, search glow |

**Convention:** pills/chips/avatars are pill-or-circle (`50px`+); content cards step up `8 → 16 → 24px`.

---

## 7. Shadows & Elevation

Defined as tokens:
| Token | Value | Usage |
|---|---|---|
| `--Card-Shadow` | `0 4px 14px 0 rgba(0,0,0,.25)` | Story card hover, contact CTA |
| `--Card-Shadow-Soft` | `0 2px 6px rgba(0,0,0,.08)` | Light soft elevation |
| `--Tab-Active-Shadow` | `0 10px 15px rgba(0,0,0,.1), 0 4px 6px rgba(0,0,0,.1)` | Active persona tab |
| `--Dash-Card-Shadow` | `0 20px 25px -5px rgba(16,24,40,.05), 0 8px 10px -6px rgba(16,24,40,.05)` | Dashboard mock card |

Other elevation effects:
- Feature card resting: `filter: drop-shadow(0 4px 4px rgba(0,0,0,.12))`; hover: `box-shadow: 0 8px 16px rgba(85,41,142,.18)` (violet-tinted).
- Active testimonial tab: dual-layer shadow `0 4px 6px / 0 10px 15px rgba(0,0,0,.1)`.
- Glows (hero, search) use large `filter: blur(40–125px)` rather than box-shadow.

**Elevation ladder:** flat (borders only) → soft card (`.08`) → hover lift (`.18–.25`) → floating dashboard (layered, low-alpha).

---

## 8. Buttons & Form Styling

### Primary gradient button (`.btn-start`, `.explore-btn`, `.pd-cta`, `.pl-cta`)
```
background: var(--Explore-Button);   /* violet→blue→turquoise */
color: #fcfcfc; font: 700 15px/25px Inter;
padding: 8px 16px; border-radius: 8px; border: none;
hover: filter: brightness(1.1);
```

### Outline / secondary (`.btn-demo`)
```
border: 2px solid #7747b6; background: transparent; color: #fcfcfc;
font: 700 15px/25px Inter; padding: 6px 16px; border-radius: 8px;
hover: background: rgba(119,71,182,.15);
transition: background .25s ease, border-color .25s ease;
```

### Inverted button (`.contact-cta .cta-button`)
White bg + blue text, inverts to transparent + white border on hover.

### Circular nav arrows (`.nav-arrow`, `.stories-arrow`)
`40×40`, `border-radius: 50%`, 1px border. Comes in outline and **filled-primary** variants; primary inverts to brand color on hover. `transition: all .25s ease`.

### Icon/pill buttons (hero search)
`.icon-btn` round 35.5px (`#334155`); `.tools-btn` pill 35.5px high (`#334155`).

### Form / input treatment
There are **no native text inputs** — the hero "search" is a styled mock:
- Outer shell: glass `rgba(255,255,255,.1)`, 1px translucent border, radius 12px.
- Inner field: `rgba(15,23,42,.7)` bg, **1.666px solid `#1ca9c9`** (turquoise) border, radius ~8.9px.
- Placeholder text uses `--blueGray-200`. Use this border/contrast pattern for any real input fields.

---

## 9. Cards & Container Styles

| Card | Background | Border | Radius | Shadow | Notes |
|---|---|---|---|---|---|
| Feature card | `#f7f7f7` | 1px `#b499d7` (violet) | 8px | drop-shadow → violet hover | Fixed 313×278, icon + h5 + p |
| Story card | `#fcfcfc` | 1px `#e5e7eb` | 16px | hover `--Card-Shadow` | 368×424.5, image top + body |
| Testimonial card | `#fcfcfc` | 1px `#eaeaea` | 16px | none | Outer wrapper, padding 64×32 |
| Persona dashboard | `#fcfcfc` | 1px `#e5e7eb` | 24px | `--Dash-Card-Shadow` | Floating mock |
| Pricing-right | `#fcfcfc` | 1px `#eaeaea` | 12px 0 0 12px | none | Asymmetric, half-rounded |
| Stat block | `#55298e` (violet) | none | 18px | none | White text, big number |
| Ask-AI box (footer) | `rgba(252,252,252,.04)` | 1px `rgba(159,186,228,.15)` | 12px | none | Glass on dark |
| Contact CTA | blue gradient | none | 16px | `--Card-Shadow` | Full-width banner |

**Pattern:** light cards = white bg + 1px light-grey border + medium radius + hover lift. Dark cards = low-alpha white bg + low-alpha blue-grey border ("glass").

---

## 10. Navigation Styling

### Hello bar (`.hello-bar`)
- Bg `#07214b`, full-width, bottom border `rgba(252,252,252,.2)`, padding `10px 48px 11px`, flex.
- **Badge:** white bg, blue (`#0e48a5`) text, 700/14px, radius 4px — animated pulse.
- **Message:** `rgba(255,255,255,.8)`, 14px — animated shimmer.
- **CTA:** underlined, white → `#12b6f8` on hover, with nudging arrow.

### Main header (`.site-header`)
- Bg `#030d1e`, height 81px, `padding: 20px 48px 21px`, flex space-between, bottom border `rgba(255,255,255,.1)`. `z-index: 20`.
- **Brand:** Fraunces wordmark, `L` and `AI` superscript in `#12b6f8`.
- **Nav links:** Inter 15px/26px, `rgba(255,255,255,.9)` → `#12b6f8` hover, 32px gap, with caret/AI SVGs.
- **Actions:** outline "Request a Demo" + gradient "Start for Free".

### Footer (`.site-footer`)
- Transparent on finale gradient, 6-col grid (`1.3fr repeat(5,1fr)`), top border `rgba(159,186,228,.12)`.
- Column headings: Inter 700/16px **`#12b6f8`**, underlined with a border.
- Links: white → `#12b6f8` hover, `transition: color .2s`.
- Circular social/ask-AI icons (36px / 32px) with low-alpha bg, hover brighten/blue.

---

## 11. Icon & Image Treatment

- **Icons:** inline SVGs, `stroke="currentColor"` (line) or `fill="currentColor"`, typically `stroke-width: 1.8–2`, `stroke-linecap/linejoin: round`. Sized 12–24px contextually. Color inherits from parent state (e.g. icon tiles flip to brand accent when active).
- **Icon tiles:** rounded squares (8–14px radius) with pale bg (`#e7eef8`) and a brand-color glyph. Persona/feature accents recolor both tile bg and glyph.
- **Logo marquee:** `height: 48px`, `filter: grayscale(100%) brightness(1.6) contrast(.9)`, `opacity: .75` → full color + opacity 1 on hover.
- **Product visuals:** `mix-blend-mode: lighten` to blend onto dark bg; `object-fit: contain`.
- **Story / pricing images:** `object-fit: cover` inside fixed-height, overflow-hidden, rounded frames; gradient placeholder bg behind.
- **Compliance badges:** `140×140`, `object-fit: contain`.
- Global: `img { max-width: 100%; }`, `loading="lazy"` on below-fold images.

---

## 12. Reusable Component Patterns

1. **Pill / chip** — `border-radius: 50px`, `padding: 6px 10px` (or `8px 18px`), 12–14px text, pale brand bg + brand text. Variants: `.pd-chip`, `.persona-pill`, `.chip`, `.pl-chip`, `.hero-search-tag`. Active state swaps to solid/brand fill.
2. **Tab card** — bordered rounded card; `.is-active` adds a 2px brand border + shadow + optional brand bg, and reduces padding by 1px to compensate for the thicker border. Used by personas, testimonials, products (border-left variant), pricing.
3. **Numbered list-tab** (products) — left-border indicator (`2px` grey → `3px` brand on active) + number + icon tile + name/sub.
4. **Carousel** — `overflow:hidden` viewport + flex track translated via `transform` with `transition: transform .55s cubic-bezier(.4,0,.2,1)`, driven by circular prev/next arrows. Used by Features and Success Stories.
5. **Section heading block** — centered Fraunces H2 (32/44.8, weight 300) + Fraunces sub (20/30, muted). Margins tuned per section.
6. **Accent-by-context** — product/persona keyed to Violet / Royal Blue / Turquoise via `data-*` selectors recoloring borders, pills, and icons.
7. **Glow layer** — absolutely positioned, blurred radial gradient, `pointer-events: none`, behind content.
8. **Section-bridge gradient** — `::before`/`::after` pseudo-element with a vertical multi-stop gradient to fade between dark and light sections.

---

## 13. Hover Effects, Transitions & Animations

**Standard transition:** `.25s ease` (most interactive elements); carousels use `.55s cubic-bezier(.4,0,.2,1)`; color-only hovers use `.2s`.

| Effect | Detail |
|---|---|
| Card lift | `transform: translateY(-4px)` + shadow (feature, story cards) |
| Button | gradient buttons `filter: brightness(1.1)`; outline fills with tint |
| Link hover | color → `#12b6f8` (dark UI) or darker blue (light UI) |
| Logo | grayscale → full color on hover |
| Nav arrows | invert fill/color to brand |
| FAQ accordion | `max-height` + `padding` + `opacity` transition; `+` toggle rotates to `–` (vertical bar fades) |

**Keyframe animations (in inline `<style>`):**
- `badgePulse` — 2.4s scale + box-shadow ring on the webinar badge.
- `shimmer` — 4s linear light sweep across the hello message (gradient-clipped text).
- `arrowNudge` — 1.6s arrow translateX on CTA.
- `scroll-left` — 50s linear infinite marquee (`translateX(0 → -50%)`) for the logo track (duplicated set for seamless loop).

---

## 14. Responsive Behavior

Mobile-down breakpoints (max-width):

### `≤ 1199px` (small desktop / large tablet)
- Footer nav → 4 columns, brand spans full row.
- Pricing panel → `380px 1fr`; products → `260px 1fr`; **product visual hidden**.

### `≤ 991px` (tablet)
- Hello message hidden; nav links + "Request a Demo" hidden (mobile-nav territory); header height auto.
- Hero H1 → 40px/50px, sub → 17px; search wrap full width, footer stacks.
- Products / personas / pricing collapse to single column; persona tabs wrap to 2-up.
- Pricing image becomes static full-width; trust row & before-decide stack and center; footer → 2 columns.

### `≤ 575px` (mobile)
- Container padding 20px; hello CTA hidden.
- Hero H1 → 32px/40px, sub → 15px; **all section headings → 26px/36px**.
- Persona tabs 1-up; pricing tabs stack vertically full-width.
- Testimonial padding reduced; contact CTA + copyright stack; footer → 1 column; legal links wrap.

**Inline `index.html` overrides** add tighter section padding and smaller hero type at `≤991` (38/46) and `≤575` (30/38).

---

## 15. Accessibility Basics

Present in the build:
- **Semantic landmarks:** `<header>`, `<nav>`, `<section>`, `<footer>`; lists for nav/footer.
- **`aria-label`** on icon-only controls (`brand-mark`, nav arrows, search buttons) and `aria-hidden="true"` on decorative SVGs/quote marks.
- **`alt` text** on content/logo images.
- **`prefers-reduced-motion: reduce`** media query disables badge pulse, shimmer, and arrow nudge, and restores a solid text color for the shimmer message.
- **Focus/keyboard:** interactive elements are real `<button>`/`<a>` so they're focusable; `cursor: pointer` on actionable items.

Gaps to watch when extending:
- Several links are placeholder `href="#"`.
- No visible custom `:focus-visible` styling defined — rely on UA default; consider adding for keyboard users.
- Verify color contrast for muted text on light (`#99a1af`, `#6a7282`) and low-opacity white text on dark.

---

## 16. CSS Variables / Design Tokens (Quick Reference)

```css
:root{
  /* Royal Blue */
  --Royal-Blue-Blue-50:#e7eef8; --Royal-Blue-Blue-150:#b8d0fd;
  --Royal-Blue-Blue-200:#9fbae4; --Royal-Blue-Blue-350:#5886d0;
  --Royal-Blue-Blue-400:#4075c9; --Royal-Blue-Blue-450:#2863c3;
  --Royal-Blue-Blue-500:#0e48a5; --Royal-Blue-Blue-550:#0c3b87;
  --Royal-Blue-Blue-600:#0a3578; --Royal-Blue-Blue-750:#07214b;
  --Royal-Blue-Blue-850:#04142d; --Royal-Blue-Blue-900:#030d1e;

  --Penn-Blue:#001040; --Absolute-Black:#212121; --Base-White:#fcfcfc;

  /* Violet */
  --Violet-Violet-50:#f0ebf7; --Violet-Violet-250:#b499d7;
  --Violet-Violet-450:#7747b6; --Violet-Violet-500:#55298e; --Violet-Violet-550:#4d2580;

  /* Sky / Turquoise */
  --SkyBlue-SkyBlue-50:#e7f8fe; --SkyBlue-SkyBlue-500:#12b6f8;
  --Turquoise-SkyBlue-50:#e8f6fa; --Turquoise-SkyBlue-500:#1ca9c9;

  /* Neutrals */
  --Grey-Grey-100:#fbfbfb; --Grey-Grey-200:#f7f7f7; --Grey-Grey-600:#bbbbbb;
  --Grey-Grey-700:#8c8c8c; --Grey-Grey-800:#5e5e5e; --Grey-Grey-900:#2f2f2f; --Map-Grey:#eaeaea;

  /* Blue-grey + cool greys */
  --blueGray-50:#F8FAFC; --blueGray-200:#E2E8F0; --blueGray-400:#94A3B8;
  --blueGray-500:#64748B; --blueGray-600:#475569; --blueGray-700:#334155;
  --cool-101828:#101828; --cool-99a1af:#99a1af; --cool-6a7282:#6a7282;
  --cool-e5e7eb:#e5e7eb; --cool-f9fafb:#f9fafb; --cool-d1d5dc:#d1d5dc;

  /* Gradients */
  --AI-Agents-Text: linear-gradient(83.02deg,#4AE7FF 51.42%,#4075C9 63.25%,#E879F9 76.03%);
  --Search-Glow:    linear-gradient(86.83deg,#22d3ee .77%,#3b82f6 50%,#e879f9 99.23%);
  --Explore-Button: linear-gradient(270deg,#7747b6 0%,#4075c9 50.7%,#1ca9c9 100%);
  --Compare-Button: linear-gradient(270deg,#7747b6 0%,#4075c9 50.7%,#1ca9c9 100%);
  --Tab-Bar-Bg:     linear-gradient(165.59deg,#ffffff 2.41%,#eef4ff 100.51%);
  --Active-Tab-Bg:  linear-gradient(157.45deg,#e9eff8 2.41%,#d9e3f5 100.51%);

  /* Effects */
  --Card-Shadow:       0 4px 14px 0 rgba(0,0,0,.25);
  --Card-Shadow-Soft:  0 2px 6px rgba(0,0,0,.08);
  --Tab-Active-Shadow: 0 10px 15px 0 rgba(0,0,0,.1), 0 4px 6px 0 rgba(0,0,0,.1);
  --Dash-Card-Shadow:  0 20px 25px -5px rgba(16,24,40,.05), 0 8px 10px -6px rgba(16,24,40,.05);
}
```

**Token conventions**
- Color tokens follow the Figma export naming `--<Family>-<Family>-<step>` with a fallback hex in usage: `var(--Royal-Blue-Blue-500, #0e48a5)`. Always pass the fallback.
- Numeric steps (50–900) map light → dark; `500` is the canonical brand value of each family.
- Use **gradient tokens** for buttons/accents rather than re-declaring gradients.
- Use **effect tokens** for shadows to keep elevation consistent.

---

*Generated by analyzing the existing HTML/CSS — no design decisions were changed.*
