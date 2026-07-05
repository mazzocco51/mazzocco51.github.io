---
name: Marco Mazzocco — Portfolio
description: Brutalist-editorial personal portfolio — an engineering datasheet with a pulse.
colors:
  vermilion: "#e0432a"
  vermilion-bright: "#ff5a41"
  vermilion-tile: "#d63f27"
  vermilion-deep: "#b8331d"
  white: "#ffffff"
  carbon: "#1c1c1b"
  chalk: "#ededea"
  graphite: "#8a8a85"
  hairline: "#3a3a37"
  void: "#0e0e0d"
typography:
  display:
    fontFamily: "Space Grotesk, Arial, sans-serif"
    fontSize: "clamp(34px, 10vw, 108px)"
    fontWeight: 700
    lineHeight: 0.9
    letterSpacing: "-0.037em"
  headline:
    fontFamily: "Space Grotesk, Arial, sans-serif"
    fontSize: "21px"
    fontWeight: 700
    letterSpacing: "-0.5px"
  title:
    fontFamily: "Space Grotesk, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 500
  body:
    fontFamily: "Space Grotesk, Arial, sans-serif"
    fontSize: "19px"
    fontWeight: 400
    lineHeight: 1.45
  label:
    fontFamily: "Space Mono, monospace"
    fontSize: "12px"
    fontWeight: 400
    letterSpacing: "2px"
rounded:
  none: "0px"
spacing:
  gap-sm: "12px"
  gap: "16px"
  cell-pad: "22px"
components:
  cell:
    backgroundColor: "{colors.carbon}"
    textColor: "{colors.chalk}"
    rounded: "{rounded.none}"
    padding: "22px 22px 24px"
  cell-hover:
    backgroundColor: "{colors.carbon}"
    textColor: "{colors.chalk}"
  cv-tile:
    backgroundColor: "{colors.vermilion-tile}"
    textColor: "#ffffff"
    rounded: "{rounded.none}"
    padding: "22px 22px 24px"
  cv-tile-hover:
    backgroundColor: "{colors.vermilion-deep}"
    textColor: "#ffffff"
  label:
    textColor: "{colors.graphite}"
    typography: "{typography.label}"
  data-row:
    textColor: "{colors.chalk}"
    padding: "11px 0"
---

# Design System: Marco Mazzocco — Portfolio

## 1. Overview

**Creative North Star: "The Engineering Datasheet"**

This system renders a person the way a spec sheet renders a component: numbered sections (01–07), monospace metadata in uppercase, hard 1.5px borders, coordinates in the header, dates and scores everywhere. Dark carbon ground, chalk-white ink, and a single Vermilion accent that marks only action and achievement. Density is welcome; ornament is banned. Every element carries information.

The system explicitly rejects template grammar: no SaaS gradients, no glassmorphism, no rounded cards, no cream neutrals, no Notion-style timid minimalism. Depth comes from borders and blacker photo wells, never from shadows. Motion is functional — a rotating competitions ticker, borders that ignite on hover — not choreography.

**Key Characteristics:**
- Machined and exact: zero radius, hard borders, precise alignment
- One accent (Vermilion), spent on ≤10% of any screen
- Monospace uppercase labels as the metadata voice
- Numbered-section cadence (01–07) as deliberate brand grammar
- Flat by doctrine; hierarchy by size and border weight

## 2. Colors

A two-voice palette — carbon/chalk for the datasheet, Vermilion for the pulse.

### Primary
- **Vermilion** (#e0432a): The accent for surfaces, borders, and large display text (hero dot, hover borders, progress fill). Print-ink red, never decoration. Only 4.07:1 on Carbon — prohibited for text under 24px.
- **Vermilion Bright** (#ff5a41): The small-text voice of Vermilion — section numbers, results, inline links, hover text. 5.5:1 on Carbon, AA-safe at any size.
- **Vermilion Tile** (#d63f27): The CV tile surface; darkened just enough that 12px white text hits 4.57:1. Visually reads as Vermilion.
- **Vermilion Deep** (#b8331d): Pressed/hover state of Vermilion surfaces only (CV tile hover). Never appears at rest.

### Neutral
- **Carbon** (#1c1c1b): The body ground. Near-black with a hint of warmth; everything sits directly on it — no elevated surface color exists.
- **Chalk** (#ededea): Primary ink. Text, borders, outlined display strokes.
- **Graphite** (#8a8a85): Metadata voice — mono labels, secondary copy, values. Holds ~4.9:1 on Carbon; never use it smaller than 11px.
- **Hairline** (#3a3a37): Interior dividers between data rows. Structure at whisper volume.
- **Void** (#0e0e0d): Photo-cell wells, the only surface darker than the ground.

### Named Rules
**The Vermilion Budget Rule.** Vermilion covers ≤10% of any viewport. The CV tile is the one solid-red surface allowed per page; everything else gets Vermilion only as stroke, glyph, or text.
**The Split Red Rule.** One red identity, three jobs: #e0432a for surfaces/borders/display, #ff5a41 for small text on Carbon, #d63f27 under white text. Never swap their roles; the contrast math is the reason each exists.
**The No New Grays Rule.** Four neutrals exist (Carbon, Chalk, Graphite, Hairline, plus Void for wells). Never interpolate a fifth.

## 3. Typography

**Display/Body Font:** Space Grotesk (with Arial fallback)
**Label/Mono Font:** Space Mono

**Character:** One grotesk carries all reading matter; the mono carries all metadata. The pairing contrasts on axis (geometric grotesk vs. typewriter mono), never competes.

### Hierarchy
- **Display** (700, clamp(38px, 10vw, 108px), 0.9, -4px): The hero name only. Surname rendered as 2px chalk outline (`-webkit-text-stroke`), first name solid — the signature move.
- **Headline** (700, 21px, -0.5px): Entry titles inside cells (degrees, project questions).
- **Title** (500, 16px): Row leads — cert names, language names.
- **Body** (400, 19px about / 12–13.5px dense, 1.45): About copy at 19px max 42ch; supporting prose in Graphite at 12–13.5px, max 58–66ch.
- **Label** (400, 11–12px, +1 to +2px tracking, UPPERCASE, Space Mono): Section labels, values, stack tags, captions, footer. Always Graphite unless hot (Vermilion).

### Named Rules
**The Mono Metadata Rule.** If it's a label, a date, a value, a coordinate, or a stack tag, it is Space Mono, uppercase, tracked. No exceptions; this is the datasheet voice.

## 4. Elevation

Entirely flat. No shadows exist anywhere in the system. Depth is conveyed three ways: border weight (1.5px chalk = cell boundary, 1px hairline = interior divider), surface darkness (Void photo wells sit "below" the Carbon ground), and hover state (borders ignite Vermilion). Photo cells add a radial vignette on hover — a darkness gradient, not a shadow.

### Named Rules
**The Flat Doctrine.** `box-shadow` is prohibited. If a surface needs separation, give it a border or make it darker.

## 5. Components

### Cell (the universal container)
- **Corner Style:** Square (0px — global `border-radius: 0`)
- **Border:** 1.5px solid Chalk (#ededea)
- **Background:** Carbon (transparent to ground)
- **Hover:** Border ignites to Vermilion, `transition: border-color .15s ease`
- **Internal Padding:** 22px 22px 24px
- **Header pattern:** Vermilion mono number (`01`) + Graphite uppercase mono label, then content.

### CV Tile (the one solid surface)
- **Style:** Solid Vermilion background, white text, no border
- **Content:** Mono label top, heavy uppercase "DOWNLOAD CV" display text, diagonal-arrow SVG bottom-right
- **Hover:** Background deepens to Vermilion Deep

### Data Rows
- **Style:** Flex row — Title (500, 16px) left, mono uppercase Graphite value right; 11px vertical padding; 1px Hairline divider between rows, none after last
- **Links:** Inherit color; hover draws a 1px Vermilion underline

### Links (meta bar)
- **Style:** 15px, weight 500, Chalk; Vermilion `→` prefix
- **Hover:** Text and arrow swap colors (text→Vermilion, arrow→Chalk)

### Photo Cells
- **Style:** Zero padding, Void background, image `object-fit: cover` at `grayscale(1) contrast(1.05)`
- **Hover:** Contrast lifts, radial vignette fades in, mono uppercase caption slides up over a bottom black gradient

### Ticker (signature component)
- **Style:** Auto-rotating competitions band — one entry visible, slides in from the right every 5s; name in grotesk, result in Vermilion mono, year in Graphite mono
- **Progress:** 3px track (Hairline) with a Vermilion fill animating width over the 5s interval

## 6. Do's and Don'ts

### Do:
- **Do** keep Vermilion (#e0432a) under 10% of the viewport — stroke, glyph, or text, plus at most one solid tile.
- **Do** set every label, date, value, and tag in Space Mono, uppercase, tracked +1 to +2px, Graphite.
- **Do** use hard borders (1.5px Chalk exterior, 1px Hairline interior) for all structure.
- **Do** keep photos grayscale at rest; color is reserved for Vermilion.
- **Do** provide `prefers-reduced-motion` fallbacks for the ticker, progress bar, and caption reveals (crossfade or static).
- **Do** keep the numbered-section cadence (01–07) coherent — renumber when sections change.

### Don't:
- **Don't** ship anything that reads as template output — "no slop": no SaaS gradients, no glassmorphism, no soft rounded cards, no cream/pastel neutrals (PRODUCT.md anti-references, verbatim).
- **Don't** use `border-radius` above 0px or any `box-shadow`, ever.
- **Don't** reproduce corporate SaaS landing grammar: hero-metric blocks, identical feature-card grids.
- **Don't** drift toward the Notion-minimal portfolio look — centered avatar, gray-on-white timidity.
- **Don't** add new grays or a second accent hue; the palette is closed.
- **Don't** let Graphite text drop below 11px or sit on anything other than Carbon/Void.
- **Audit test:** if a surface has a soft corner, a shadow, or a gradient that isn't a photo vignette, it's off-system.
