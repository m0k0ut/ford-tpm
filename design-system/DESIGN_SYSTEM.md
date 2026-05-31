# Ford "Reimagine" Design System

**Canonical design reference for this project.** All visual artifacts (webpages, slides, mockups, prototypes) MUST follow this system so every change stays consistent.

> Source: Ford Design System bundle from Claude Design (claude.ai/design), reconstructed from Ford.com EV-era marketing pages (Mustang Mach-E, F-150 Lightning). Token source of truth: [`colors_and_type.css`](colors_and_type.css) — import it directly rather than re-declaring tokens.

---

## Core Principle — "Reimagine"
**Restraint and breathing room.** Remove, don't add. Give it more space. Show less, larger. Generous negative space is the signature of the modern Ford.com. Lean light and airy; reserve dark for cinematic moments. This is the single most important rule — every token below is tuned for air.

---

## Color

```
--ford-blue:         #003478   Heritage Blue Oval — primary brand (PMS 288C)
--ford-blue-900:     #00142e   Deepest blue / near-black backgrounds, footer
--ford-blue-800:     #001a40
--ford-blue-700:     #002257
--ford-blue-500:     #0b4ea2
--ford-blue-400:     #2a6fd0

--ford-electric:     #066fef   EV-era accent — CTAs, links, Mach-E/Lightning
--ford-electric-600: #0a5ed1   Hover state for primary buttons
--ford-electric-300: #5fa3f7   Light electric blue — accents ON dark surfaces
--ford-electric-100: #d6e7fd   Tint — icon backgrounds, focus ring glow

--white:   #ffffff
--gray-50: #f4f6f9   Subtle background      --gray-500: #6b7480
--gray-100:#e9edf2                          --gray-600: #4d555f  Secondary text
--gray-200:#d4dae2   Default border         --gray-700: #343a42
--gray-300:#b9c1cc   Strong border          --gray-800: #23272c
--gray-400:#939dab   Muted text             --gray-900: #15181b
--black:   #0b0c0e   Cinematic vehicle-hero black

--success: #1e8e3e   --warning: #c77700   --error: #d62d2d   --info: #066fef
```

Neutrals are subtly **cool-tinted**. Red is reserved for errors only — never decorative.

---

## Typography

- **Display / headlines:** `"Archivo Expanded"`, weight 800–900, tight tracking
- **Body / UI:** `"Archivo"`, weight 400–700
- **Mono:** `"JetBrains Mono"`
- _Official Ford face is **Antenna** / **Ford F-1** — not publicly licensed; **Archivo** is the approved substitute._

```
@import url('https://fonts.googleapis.com/css2?family=Archivo:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,400&family=Archivo+Expanded:wght@600;700;800&family=JetBrains+Mono:wght@400;500;700&display=swap');
```

| Role | Size | Weight | Line-height | Tracking |
|------|------|--------|-------------|----------|
| Eyebrow | 13px | 700 | — | `0.14em`, UPPERCASE, `--ford-electric` |
| Display XL | `clamp(40px,6vw,76px)` | 800 | 1.0 | `-0.02em` |
| Display L | 56px | 800 | 1.04 | `-0.02em` |
| H1 | 40px | 800 | 1.08 | `-0.015em` |
| H2 | 30px | 700 | 1.14 | `-0.01em` |
| H3 | 22px | 600 | 1.25 | `-0.005em` |
| Body LG | 19px | 400 | 1.55 | — |
| Body | 16px | 400 | 1.6 | — |
| Body SM | 14px | 400 | 1.5 | — |
| Caption | 12px | 400 | 1.4 | `--fg-muted` |

**Body copy** caps at `--measure` (~56ch). **Stat numbers** go Archivo Expanded 800, oversized, `letter-spacing: -.03em`.

---

## Voice & Copy
- **Confident, plainspoken, capability-forward.** Sells the vehicle, not the website.
- Speaks to **you** ("Build & Price yours"). Brand is **Ford**, rarely "we".
- **Eyebrows** ALL CAPS + wide tracking → **Headline** (short, declarative) → short support line → **CTA**.
- **Numbers sell** — capability stats as hero content, with units, often huge. Footnote with superscript (¹ *).
- **CTAs are verbs** in Title Case with trailing chevron: *Build & Price ›*, *Search Inventory ›*, *Learn More ›*.
- **No emoji.** Unicode chevrons/arrows (`›` `→`) for inline affordances.

---

## Spacing & Layout
- **4px base scale:** `--space-1: 4px` → `--space-12: 200px`.
- **Section vertical padding:** `--section-y: clamp(72px, 9vw, 128px)`; hero `--section-y-lg: clamp(96px, 12vw, 176px)`.
- **Container:** `--content-max: 1240px`; side gutter `--gutter: clamp(20px, 5vw, 48px)`.
- **Body measure:** `--measure: 56ch`.
- Full-bleed bands alternate light/dark. Sticky top utility nav.

---

## Radii & Elevation
```
--radius-sm: 4px   --radius-md: 8px   --radius-lg: 16px   --radius-pill: 999px

--shadow-sm:  0 1px 2px  rgba(0,20,46,.08)
--shadow-md:  0 4px 14px rgba(0,20,46,.10)
--shadow-lg:  0 12px 32px rgba(0,20,46,.14)
--shadow-hero:0 24px 60px rgba(0,20,46,.28)
```
Shadows are restrained, soft, cool-tinted. No hard drop shadows, no neumorphism.

---

## Components

### Buttons — pill-rounded (`border-radius: 999px`), weight 700, `padding: 13px 28px`, `font-size: 15px`
- **Primary:** `background: #066fef; color: #fff` → hover `#0a5ed1`
- **Dark:** `background: #00142e; color: #fff` → hover `#00224a`
- **White** (on dark): `background: #fff; color: #0b0c0e` → hover `--gray-100`
- **Ghost-light** (on dark): `border: 1.5px solid rgba(255,255,255,.45); color: #fff`
- **Outline** (on light): `border: 1.5px solid #b9c1cc; color: #00142e`
- **Link CTA:** `color: #066fef; font-weight: 700` → underline on hover
- Press: `transform: scale(.98)`.

### Cards — `background: #fff; border-radius: 16px; box-shadow: --shadow-md`
- Vehicle card: image header (150px gradient) + name (800, 20px) + price + Build & Price CTA.
- Hover: shadow lift to `--shadow-lg` + slight image zoom (`scale 1.03`) under clip; optional `translateY(-4px)`.

### Inputs — `border: 1.5px solid #d4dae2; border-radius: 8px; padding: 12px 14px; font-size: 15px`
- Focus: `border-color: #066fef; box-shadow: 0 0 0 3px #d6e7fd`.
- Label: 13px / 600 / `--gray-600`. Placeholder: `--gray-400`.

### Badges — pill, 12px / 700, `letter-spacing: .06em`, UPPERCASE, `padding: 6px 12px`
- All-Electric: `bg #d6e7fd / text #0a5ed1` · New: `bg #00142e / #fff` · In Stock: `bg #e7f3ec / #1e8e3e` · Sold Out: `bg #fdeaea / #d62d2d`
- **Selectable chips:** `border: 1.5px solid #d4dae2`; selected → `bg/border #00142e, text #fff`.

### Stat band (dark) — `background: #0b0c0e`, numbers Archivo Expanded 800 ~60px, label 13px UPPERCASE `--ford-electric-300`, dividers `1px rgba(255,255,255,.14)`.

### Nav — sticky, `backdrop-filter: blur(10px)`; dark `rgba(11,12,14,.78)` or light `rgba(255,255,255,.88)`; height ~66px; Build & Price pill at right.

### Footer — `background: #00142e`, 4 link columns, headers 13px UPPERCASE `--ford-electric-300`, Blue Oval + copyright + legal links.

---

## Motion
- **Easing:** `--ease-standard: cubic-bezier(0.2,0,0,1)`; `--ease-emphasized: cubic-bezier(0.3,0,0,1)`.
- **Durations:** `--dur-fast: 140ms` (hover), `--dur-med: 240ms`, `--dur-slow: 420ms`.
- Fades + gentle upward reveals on scroll (`IntersectionObserver`, `translateY(24px)→0`). Smooth/premium, **never bouncy**.

---

## Iconography
- **Lucide** via CDN — closest free match to Ford's custom thin-line set (~1.5–2px stroke, rounded, monochrome).
- `<script src="https://unpkg.com/lucide@latest/dist/umd/lucide.min.js"></script>` then `lucide.createIcons()`.
- Usage: `<i data-lucide="zap" style="width:20px;height:20px"></i>`. Icons inherit `currentColor`.
- **No emoji.** Chevrons via Lucide or Unicode `›`.

---

## Imagery
- Defining motif: **full-bleed cinematic vehicle photography** (3/4 hero angles, moody/golden-hour). None bundled (copyright) — use gradient placeholders:
  - EV/dark: `radial-gradient(130% 110% at 68% 15%, #1b3358 0%, #0c1828 40%, #05070d 100%)`
  - Truck: `radial-gradient(120% 100% at 65% 30%, #2a3340 0%, #161c25 50%, #07090d 100%)`
  - Studio/light: `linear-gradient(135deg, #e9edf2 0%, #cdd6e2 100%)`
- Hero text over image needs a **protection scrim:** `linear-gradient(0deg, rgba(0,0,0,.82) 0%, rgba(0,0,0,.25) 42%, transparent 68%)`.
- No busy patterns, no noise/grain, no rainbow gradients. Subtle single-hue blue gradients only.

---

## Logo
- Ford Blue Oval (transparent PNG) at [`../web/assets/ford-logo.png`](../web/assets/ford-logo.png). Display width ~64–78px in nav/footer. The Oval is a hand-drawn trademark — never redraw it.

---

## Dark Surface Overrides
```css
.ford-dark, [data-theme="dark"] {
  --bg: #0b0c0e; --bg-subtle: #15181b; --surface: #15181b;
  --fg: #ffffff; --fg-secondary: #b9c1cc; --fg-muted: #939dab;
  --link: #5fa3f7;
  --border: rgba(255,255,255,.16); --border-strong: rgba(255,255,255,.30);
}
```

---

## Known Substitutions (swap for production)
1. **Font:** Antenna / Ford F-1 → **Archivo** (visually close, not exact).
2. **Icons:** Ford custom set → **Lucide** (CDN).
3. **Imagery:** no Ford photography bundled — drop real photos into image slots.
4. Reconstructed from the public site, **not** an internal source of truth — treat measurements as faithful approximations.
