---
name: Jamie
description: A personal dispatch — warm, human, slightly imperfect, with jokes in the margins
colors:
  sealing-wax: "#b22234"
  sealing-wax-bright: "#d4253d"
  sealing-wax-dim: "#8b1a28"
  warm-paper: "#faf7f2"
  ink: "#1c1c1c"
  ink-soft: "#3b3632"
  ink-faint: "#6e6660"
  rule-gray: "#d4cec6"
typography:
  display:
    fontFamily: "Vollkorn, Georgia, Times New Roman, serif"
    fontSize: "clamp(3rem, 8vw, 6.5rem)"
    fontWeight: 800
    lineHeight: 1.04
    letterSpacing: "-0.025em"
  headline:
    fontFamily: "Vollkorn, Georgia, Times New Roman, serif"
    fontSize: "clamp(1.75rem, 4vw, 2.5rem)"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-0.015em"
  body:
    fontFamily: "Vollkorn, Georgia, Times New Roman, serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.75
  label:
    fontFamily: "Courier Prime, Courier New, monospace"
    fontSize: "0.75rem"
    fontWeight: 400
    letterSpacing: "0.06em"
spacing:
  xs: "0.5rem"
  sm: "1rem"
  md: "2rem"
  lg: "4rem"
  xl: "6rem"
components:
  contact-link:
    backgroundColor: transparent
    textColor: "{colors.sealing-wax}"
    typography: "{typography.label}"
    size: "auto"
  contact-link-hover:
    backgroundColor: transparent
    textColor: "{colors.sealing-wax-dim}"
---
## Overview

**Creative North Star: "The Personal Dispatch"**

This is a letter that arrived in the mail — warm paper, dark ink, a wax seal, and handwriting in the margins. The design system treats every visitor as someone worth writing to directly. It refuses the self-marketing brochure, the designer portfolio template, and anything that reads like it was written by committee. The voice is confident and witty, never self-serious.

The surface is typographic above all. Vollkorn carries the letterpress weight — commanding at display sizes, warm and readable in body. Courier Prime handles meta-information: dates, asides, labels, the little typewriter notes in the margin. There are no images, no hero graphics, no gradients. The text is the visual weight. Depth comes from tonal layering of warm paper tones, not from shadows or elevation.

Motion is authored, not scattered. The typewriter greeting types itself line by line. The name stamps into place like a seal pressed into wax. Rules draw themselves from left to right. Sections reveal on scroll, staggered like paragraphs discovered one at a time. Interactive elements — asides, work entries — reward curiosity with hidden text.

**Key Characteristics:**
- Typographic-first: no images, no icons, no hero graphics
- Single accent: Sealing Wax crimson, used on ≤ 5 elements per viewport
- Direct address: "I" and "you," never third person
- Hidden depth: hover reveals, real-talk asides, jokes in the margins
- Flat and warm: tonal paper layers, no shadows, no glass, no radius

## Colors

A restrained palette built around warm paper and dark ink, with one accent that draws the eye only where it matters.

### Primary
- **Sealing Wax** (#b22234): The crimson you'd melt to seal a letter. Used only on the two horizontal rules, contact links, and the aside underline. Appears on ≤ 5 elements per viewport.
- **Sealing Wax (Bright)** (#d4253d): Hover state for interactive accent elements.
- **Sealing Wax (Dim)** (#8b1a28): Pressed state for contact links; deeper, quieter.

### Neutral
- **Warm Paper** (#faf7f2): The page background — warm off-white, like stationery in afternoon light.
- **Ink** (#1c1c1c): Primary text. The name, headings, and anything that leads.
- **Soft Ink** (#3b3632): Body text and secondary reading. Dark enough for contrast, soft enough to not compete with headings.
- **Faint Ink** (#6e6660): Labels, dates, monospace meta-text. The quietest voice on the page.
- **Rule Gray** (#d4cec6): Dividers and section borders. Nearly invisible, just enough to separate.

**The One Accent Rule.** Sealing Wax appears on ≤ 5 elements per viewport. Its rarity is the point. A page where everything is red is a page where nothing is.

## Typography

**Display Font:** Vollkorn (with Georgia, Times New Roman fallback)
**Label/Mono Font:** Courier Prime (with Courier New, monospace fallback)
**Signature Font:** Caveat (cursive, used only for the closing signature)

**Character:** Vollkorn brings letterpress warmth — generous, slightly old-fashioned, substantial at weight 800. Courier Prime provides typewriter texture for the marginalia: dates, asides, labels, meta-commentary. Together they feel like a letter typed on good stationery with handwritten corrections.

### Hierarchy
- **Display** (800, clamp(3rem, 8vw, 6.5rem), 1.04): The name only. Appears once per page at the top. Letter-spacing tightened to -0.025em for impact.
- **Headline** (700, clamp(1.75rem, 4vw, 2.5rem), 1.15): Section headings. Bold but not shouting.
- **Body** (400, 1.0625rem, 1.75): All reading text. Italic for emphasis and opening statements. Max line length 60ch.
- **Label** (Courier Prime 400, 0.75rem, letter-spacing 0.06em): Dates, contexts, meta-information, asides, contact links. The typewriter voice.

**The Weight Rule.** Vollkorn at weight 800 is reserved for the name. Use 700 for section headings, 400 for body. Never use Vollkorn below 400 or between 500–600.

## Layout

The page is a single centered column — like a letter on a desk. The container is `max-width: calc(60ch + 2 × clamp(1.5rem, 6vw, 8rem))` with generous side margins that shrink on mobile. Sections stack vertically with `padding: 6rem 0` and a 1px rule-gray divider between them.

Spacing follows a 2× scale: xs (0.5rem), sm (1rem), md (2rem), lg (4rem), xl (6rem). More space above a heading than below it, always.

The opening section fills the viewport (`min-height: 100svh`) with vertically-centered content. The scroll cue sits at the bottom of the opening, outside the centering flex context.

## Elevation & Depth

This system is **flat**. No shadows, no glass, no blur, no elevation tokens. Depth is conveyed entirely through tonal layering — the warm paper background and slightly warmer section tones carry all the dimensionality the page needs. Interactive depth comes from content reveals (hover expansions, scroll-triggered fades), not from simulated Z-axis.

**The Flat-By-Default Rule.** Surfaces are flat at rest. Any future depth effect must be state-driven (hover, focus, active), never decorative. If you're reaching for `box-shadow`, you're probably solving the wrong problem.

## Shapes

Zero border-radius throughout. Every edge is square. The form language is paper: straight cuts, crisp folds, sharp corners. Dividers are 1px solid lines. The only exception is the aside tooltip bubble, which has a subtle 3px radius to distinguish it as a floating element rather than a page element.

**The Sharp Edge Rule.** Corners are square. If a radius appears, it signals that the element is not part of the page — it's floating above it (tooltips, popovers).

## Components

This is a typographic page, not a component-heavy UI. The few interactive elements that exist are prose-native.

### Contact Links
- **Shape:** Inline text with a 1px solid Sealing Wax underline. No background, no padding block.
- **Hover:** Color shifts to Sealing Wax (Dim), lifts 1px via transform, underline follows.
- **Active:** Presses down 1px (transform: translateY(1px)).
- **Focus:** 2px solid Sealing Wax outline with 3px offset.

### Work Entry
- **Shape:** Full-width prose block with 1px Rule Gray divider between entries.
- **Surface:** Visible description in Soft Ink (Vollkorn body). Hidden "real talk" in Sealing Wax (Courier Prime) expands on hover/focus with max-height animation.
- **States:** Default (surface visible, real talk hidden), hover/focus (real talk expands, opacity transitions in).

### Aside Bubble
- **Shape:** Inline dashed Sealing Wax underline on the trigger word. Tooltip is a dark bubble (Ink background, Warm Paper text) with a downward-pointing arrow.
- **Behavior:** Appears above the trigger on hover via opacity + translateY transition. Courier Prime, 0.6875rem.
- **Mobile:** Bubbles wrap to max-width 14rem and center-align.

### Typewriter Greeting
- **Shape:** Courier Prime text, monospace cursor blinking at end of line.
- **Animation:** Characters type at 50ms ± random jitter per character. Lines pause 300–600ms between them. Cursor blinks at 0.8s step-end while typing, slows to 2s step-end when complete.
- **Completion:** Triggers the name stamp-in, rule draw, and prompt fade sequence.

## Do's and Don'ts

### Do:
- **Do** use generous margins — the letter needs room to breathe (margin-edge: clamp(1.5rem, 6vw, 8rem)).
- **Do** use Courier Prime for all meta-information: dates, asides, labels, contact links, typewriter effects.
- **Do** use Vollkorn 800 for the name only, 700 for section headings, 400 for body text.
- **Do** keep Sealing Wax below 5% of any viewport — a single rule, a single link, an aside underline.
- **Do** address the reader directly — "I" and "you," first and second person.
- **Do** stack more space above a heading than below it.

### Don't:
- **Don't** add images, photos, icons, or hero graphics. Text is the visual weight.
- **Don't** use border-radius on page elements. The page is flat paper.
- **Don't** use shadows, glass effects, gradients, or blur.
- **Don't** introduce a second accent color. Sealing Wax is the only one.
- **Don't** use section labels or kickers above headings.
- **Don't** write in third person. "Jamie does X" is a failure of voice.
- **Don't** use Vollkorn below weight 400 or at weights 500–600.
