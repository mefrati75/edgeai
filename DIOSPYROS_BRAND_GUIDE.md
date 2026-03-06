# DIOSPYROS -- Brand Guidelines

## Brand Essence

Diospyros is a boutique AI-first business incubator. The brand communicates exclusivity, precision, and quiet confidence. It should feel like discovering something that wasn't meant to be found -- secretive, minimal, and deliberate.

---

## Logo

**Logo Concept**:
The lock emblem features a leaf, symbolizing nature and data sovereignty. The shape evokes a fruit core and a padlock -- securing data ownership.

**Usage Rules**:
- Primary usage is on dark backgrounds (Ink #0A0A0A recommended).
- The logo should appear large and prominent in hero contexts (minimum 160px).
- Minimum spacing: 0.5x height clear space around the logo.
- Do not distort, rotate, or alter the logo colors.
- A subtle white glow animation is permitted in digital contexts.

---

## Color Palette

| Token   | Hex       | Usage                                    |
|---------|-----------|------------------------------------------|
| Ink     | #0A0A0A   | Primary background, dark sections        |
| Paper   | #FAFAFA   | Light section backgrounds                |
| Smoke   | #141414   | Card backgrounds on dark, subtle depth   |
| Ash     | #8A8A8A   | Secondary/body text, muted content       |
| Silver  | #E0E0E0   | Borders, dividers, step numbers          |
| White   | #FFFFFF   | Headlines on dark, primary text on dark  |
| Accent  | #C8FF00   | Sparingly -- CTA hover, key emphasis     |

**Accent usage**: The accent color (electric lime) should appear rarely and deliberately. It is reserved for interactive states (button hovers) and a single emphasis line. Overuse diminishes its impact.

---

## Typography

**Headlines**: Instrument Serif (Google Fonts)
- Weight: 400 (Regular only)
- Usage: All section headings, hero headline, blockquotes, card titles
- Creates editorial, high-end magazine feel

**Body / UI**: Inter (Google Fonts)
- Weights: 400 (body), 500 (UI elements), 600 (emphasis)
- Usage: Paragraphs, navigation, buttons, labels

**Backup Fonts**:
- Serif: Georgia, serif
- Sans: system-ui, -apple-system, sans-serif

```css
/* Headlines */
font-family: 'Instrument Serif', Georgia, serif;

/* Body */
font-family: 'Inter', system-ui, sans-serif;
```

---

## Layout and Spacing

- **Section padding**: 8-12rem vertical padding between sections
- **Maximum content width**: 72rem (1152px) for grids, 42rem (672px) for text
- **Button radius**: Fully rounded (pill shape) for CTAs
- **Card radius**: 16px (rounded-2xl)
- **Dark/light rhythm**: Sections alternate between Ink and Paper backgrounds

---

## Favicon / Icon Guidelines

- Use the lock-leaf symbol (without text) for:
  - Favicon (favicon.svg, favicon.ico)
  - App icon
  - Browser tab icon

---

## Tone of Voice

- Confident but understated. Never exclamatory.
- Deliberately sparse -- say less than you know.
- Sophisticated vocabulary: "sovereign" not "private", "conceive" not "build", "venture" not "app".
- No emojis. No jargon. No tech-stack listings.

---

## Developer Notes

- All assets should use SVG or high-res PNG.
- Font files imported via Google Fonts CDN.
- Ensure WCAG AA contrast ratios for all text.
- White on Ink (#FFFFFF on #0A0A0A) = 19.3:1 ratio.
- Ash on Ink (#8A8A8A on #0A0A0A) = 5.3:1 ratio (passes AA).
- Ash on Paper (#8A8A8A on #FAFAFA) = 3.5:1 ratio (use for large text only; darken to #737373 for small body text if needed).

---

(c) 2026 Diospyros. All rights reserved.
