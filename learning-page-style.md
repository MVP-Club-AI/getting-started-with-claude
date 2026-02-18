---
name: mvp-club-learning-page-style
description: Use when creating new tutorial or learning pages for MVP Club. Defines the layout system, component library, interaction patterns, and exact CSS specifications extracted from the existing learning artifacts.
---

# MVP Club Learning Page Style Guide

Use this when building new step-by-step tutorial pages, prompt-along guides, or any interactive learning content for MVP Club.

---

## Page Architecture

Learning pages use a **three-column layout**: a sticky section rail on the left, a scrolling main content column in the center, and an optional sticky sidebar on the right (used when a persistent reference like a target mockup is needed).

### Container

```css
.container {
  display: flex;
  gap: 24px;              /* 32px when sidebar is present */
  max-width: 780px;       /* 1440px when sidebar is present */
  margin: 0 auto;
  padding: 20px 16px 20px 4px;
  min-height: 100vh;
}
```

### Main Column

- `flex: 1; min-width: 0;`
- Contains: sticky nav header, step header (title + subtitle), and step content area
- Step content has a minimum height of `calc(100vh - 240px)` to keep the nav visible

### Section Rail (Left)

A vertical strip of thumbnail-sized step indicators, sticky at `top: 80px`.

**Rail thumb states:**

| State | Background | Color | Border | Extra |
|-------|-----------|-------|--------|-------|
| **Upcoming** | `#f0ebe4` | `#b8a898` | transparent | Icon at 45% opacity |
| **Completed** | `#fef3e2` | `#b45309` | `#eba714` | — |
| **Current** | `#d97706` | white | `#b45309` | `box-shadow: 0 2px 10px rgba(217,119,6,0.4)`, `scale(1.06)` |

- Width: `80–96px`, border-radius `12px`
- Connected by `2px`-wide vertical connectors (completed: `#eba714`, upcoming: `#e8e0d8`)
- Hover tooltip: navy background (`#081f3f`), warm-stone text (`#faf5f0`), positioned to the right with a CSS triangle pointer

### Target Sidebar (Right, Optional)

- Width: `500px`, sticky at `top: 16px`
- White card with `16px` radius, `2px solid #e8e0d8` border, subtle shadow
- Used when learners need a persistent visual reference (e.g., a mockup they're building toward)
- Clicking opens a modal overlay for full-size viewing

---

## Navigation

Sticky at `top: 0` with a warm-stone gradient fade-out below it.

```css
.nav-header {
  position: sticky;
  top: 0;
  background: #faf5f0;
  padding: 8px 0 12px;
  z-index: 10;
}
```

### Buttons

| Button | Background | Color | Border | Flex |
|--------|-----------|-------|--------|------|
| **Back** | white | `#15465b` | `1px solid #e8e0d8` | `flex: 1` |
| **Next / CTA** | `#d97706` | white | none | `flex: 2` |

- Shared: `padding: 14px 20px`, `border-radius: 12px`, `font-size: 15px`, `font-weight: 600`, Inter font
- Hover: `opacity: 0.9`
- Back button is hidden on the first step

---

## Typography (Learning-Specific)

Inherits from the MVP Club brand with these learning-page specifics:

| Element | Font | Size | Weight | Color |
|---------|------|------|--------|-------|
| Step title (h1) | Zilla Slab | 28px | 400 | `#081f3f` |
| Step subtitle | Inter | 16px | 400 | `#15465b` |
| Body paragraph | Inter | 17px, line-height 1.8 | 400 | `#081f3f` |
| Section label | Inter | 11px, uppercase, 1px tracking | 600 | `#15465b` |
| Brand tagline | Inter | 11px, uppercase, 1.5px tracking | 600 | `#d97706` |

Body paragraphs have `margin-bottom: 20–28px` for generous vertical rhythm.

---

## Component Library

### Callouts

Left-bordered boxes for tips, warnings, and context. Shape: `border-radius: 0 12px 12px 0`.

| Variant | Background | Border-left color | Use for |
|---------|-----------|-------------------|---------|
| `callout-purple` | `#fef9f0` | `#081f3f` (navy) | Key concepts, important notes |
| `callout-green` | `#f0fdf4` | `#16a34a` | Success tips, best practices |
| `callout-blue` | `#f0f5f7` | `#15465b` (slate) | Context, background info |
| `callout-amber` | `#fef9f0` | `#d97706` | Warnings, things to watch for |

Inner text: title at `14px/600`, body at `13px/400` in `#15465b`.

### Dark Card

A navy hero block for section introductions or key moments.

```css
.dark-card {
  background: #081f3f;
  border-radius: 16px;
  padding: 28–32px;
  text-align: center;
}
/* Heading: Zilla Slab 22px/400, color #faf5f0 */
/* Body: 14px, color #eba714 (golden) */
```

### Expandable Card (Accordion)

```css
.expand-card {
  border: 1px solid #e8e0d8;
  border-radius: 12px;
  background: white;
  overflow: hidden;
}
```

- Header: `15px/600` in `#081f3f`, arrow rotates 180° on open
- Body: `14px` in `#15465b`, `line-height: 1.7`, hidden by default

### Prompt Block

For displaying prompts learners should copy into Claude.

```css
.prompt-block {
  background: #081f3f;
  color: #faf5f0;
  border-radius: 12px;
  padding: 20px;
  font-size: 14px;
  line-height: 1.7;
  font-family: monospace;
  white-space: pre-wrap;
}
```

Always paired with a full-width copy button below:

```css
.copy-btn {
  background: #d97706;
  color: white;
  border-radius: 8px;
  padding: 10px 20px;
  font-size: 14px;
  font-weight: 600;
}
.copy-btn.copied { background: #059669; }
```

### Folder Tree

An interactive file-tree explorer.

```css
.folder-tree {
  background: white;
  border-radius: 16px;
  border: 1px solid #e8e0d8;
  padding: 16–20px 8–12px;
}
```

- Items: `monospace 14px`, hover highlight `#fef9f0`
- Folder names: `font-weight: 700`
- Hint text: `11px/600`, fades in on hover
- Tooltips: warm-stone background, slate text, shown below the hovered item

### Compare Split

Side-by-side comparison (e.g., "without context" vs "with context").

```css
.compare-split {
  display: flex;
  border-radius: 16px;
  overflow: hidden;
  border: 1px solid #e8e0d8;
}
```

| Side | Background |
|------|-----------|
| Naive / Before | `#f7f3ee` |
| Contextual / After | `#fef9f0` |

Divided by a `2px` solid `#e8e0d8` line with a `28px` circular dot in the center.

Badges: `10px/700`, uppercase, pill-shaped (`border-radius: 20px`).

### Layer Stack

Stacked blocks that visualize a progression or hierarchy.

```css
.layer-block {
  padding: 16px 20px;
  display: flex;
  align-items: center;
  gap: 14px;
  cursor: pointer;
  transition: all 0.2s;
}
.layer-block:hover { transform: translateX(4px); }
```

- First block: `border-radius: 12px 12px 0 0`
- Last block: `border-radius: 0 0 12px 12px`
- Contains: a large number (`20px/600`, low opacity), title + description, and an icon

### Flow Diagram / Vibe Loop

A horizontal process diagram on a dark gradient background.

```css
.flow-diagram {
  background: linear-gradient(135deg, #081f3f, #15465b);
  border-radius: 16px;
  padding: 24–28px;
}
```

- Step icons: `48px` circles with `rgba(255,255,255,0.1)` background
- Labels: `12px/700` white
- Descriptions: `10px` golden (`#eba714`)
- Arrows between steps: `#d97706`
- Footer: `11px` italic golden

### Context Meter / Progress Bar

```css
.meter-bar-track {
  height: 12px;
  background: #f0ebe4;
  border-radius: 6px;
  overflow: hidden;
}
.meter-bar-fill {
  height: 100%;
  border-radius: 6px;
  transition: width 0.6s ease, background 0.6s ease;
}
```

Labels below: `11px/600`, muted `#b8a898`, active label colored `#d97706`.

### Permission Cards

Expandable cards showing tool permissions.

```css
.perm-card {
  border: 1px solid #e8e0d8;
  border-radius: 12px;
}
.perm-card.open { background: #fef9f0; }
```

- Label uses monospace font with `#fef3e2` background pill
- Verdict block: green background (`#ecfdf5`), green text (`#065f46`)

### Iteration Prompt Cards

Quick-copy prompt suggestions.

```css
.iter-card {
  background: #faf5f0;
  border-radius: 12px;
  padding: 14px 18px;
  border: 1px solid #e8e0d8;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

- Copy button: amber-tinted background (`#fef3e2`), amber text (`#b45309`)

### Success Card

Celebration moment when a step or tutorial is completed.

```css
.success-card {
  background: #f0fdf4;
  border-radius: 12px;
  padding: 20–24px;
  border: 1px solid #bbf7d0;
  text-align: center;
}
/* Title: 16px/700, color #15803d */
/* Body: 14px, color #15465b */
```

### Doc Card

For listing document types or resources.

```css
.doc-card {
  background: white;
  border-radius: 12px;
  padding: 18px 20px;
  border: 1px solid #e8e0d8;
}
```

- Header: badge pill + `15px/600` title
- Description: `13px` slate
- Example block: navy background (`#081f3f`), monospace, muted text with `<strong>` in warm-stone

### Input Fields

```css
.input-field {
  width: 100%;
  padding: 10px 14px;
  border-radius: 8px;
  border: 1px solid #d4ccc4;
  font-size: 15px;
}
.input-field:focus {
  border-color: #d97706;
  box-shadow: 0 0 0 3px rgba(217,119,6,0.1);
}
```

Labels: `13px/600` in `#15465b`.

### Framework / Prompt Builder

A structured prompt recipe with color-coded sections.

```css
.framework {
  background: white;
  border-radius: 16px;
  border: 1px solid #e8e0d8;
  padding: 20px 16px;
}
```

- Badge pills: `12px/600`, white text on colored backgrounds
- Question text: `13px` slate
- Footer: warm-stone background (`#faf5f0`), `12px` centered

### Next Steps Grid

```css
.next-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
}
.next-card {
  background: white;
  border-radius: 12px;
  padding: 16px;
  border: 1px solid #e8e0d8;
  text-align: center;
}
```

### Frontend / Backend Split

Two-panel comparison with gradient backgrounds.

| Side | Background |
|------|-----------|
| Frontend | `linear-gradient(180deg, #fef3e2, #fef9f0)` |
| Backend | `linear-gradient(180deg, #f0ebe4, #faf5f0)` |

Active badge: `#d97706` background, white text. Inactive: `#e8e0d8`, slate text.

---

## Icons

All icons use **CSS mask-image** with inline SVG data URIs. This keeps icons purely in CSS, tintable via `color`/`background`, and avoids extra HTTP requests.

```css
.icon {
  display: inline-block;
  width: 1em;
  height: 1em;
  background: currentColor;
  vertical-align: -0.125em;
  -webkit-mask: no-repeat center/contain;
  mask: no-repeat center/contain;
}
```

Icon set derived from Lucide: folder, file, eye, gear, laptop, cloud, globe, package, monitor, edit, save, check, chat, zap, search, refresh, rocket, star, sparkle, target, wrench, grid, chart, briefcase, layers, brain, sliders, book, map, database, user.

Use `font-size` on the icon element to control size. Use `color` to tint.

---

## Interaction Patterns

### Step Navigation

- Steps are `display: none` by default, `.step.active` shows the current one
- Navigation buttons at the top (sticky) advance or retreat through steps
- The section rail updates thumb states (upcoming/current/completed) on each step change
- Back button is hidden on step 0

### Expand / Collapse

- Toggle `.open` class on the card
- Arrow rotates `180deg` when open
- Body toggles between `display: none` and `display: block`

### Copy to Clipboard

- Prompt blocks have a paired copy button
- On click: copy text, swap button text/color to "Copied" state (`#059669`)
- Reset after a short timeout

### Hover Behaviors

- Cards: slight lift or border-color change
- Tree items: warm background highlight (`#fef9f0`)
- Rail thumbs: tooltip appears to the right
- Arrows/icons: opacity transition or translateX nudge

---

## Color Reference (Learning-Specific Usage)

| Token | Hex | Where It Shows Up |
|-------|-----|--------------------|
| Navy | `#081f3f` | Dark cards, prompt blocks, headings, tooltips |
| Slate Blue | `#15465b` | Subtitles, body secondary text, callout-blue border |
| Warm Amber | `#d97706` | CTAs, current rail thumb, active states, borders |
| Golden Yellow | `#eba714` | Dark-card body text, completed rail connectors, flow descriptions |
| Burnt Amber | `#b45309` | Current rail border, completed thumb text, copy-button text |
| Warm Stone | `#faf5f0` | Page background, tooltip text on dark, prompt-block text |
| Parchment | `#fef9f0` | Callout backgrounds, hover highlights, open-state cards |
| Light Warm | `#fef3e2` | Completed rail thumb, permission labels, frontend gradient |
| Muted Warm | `#f0ebe4` | Upcoming rail thumb, meter track, tree separators |
| Border | `#e8e0d8` | Card borders, dividers, inactive connectors |
| Input Border | `#d4ccc4` | Text input default border |
| Muted Text | `#b8a898` | Upcoming rail text, inactive meter labels |
| Success Green | `#16a34a` / `#059669` | Callout-green border, copied state |
| Success Light | `#f0fdf4` | Success card, callout-green background |

---

## Spacing Patterns

| Context | Value |
|---------|-------|
| Between steps (margin-bottom on step content) | `32px` |
| Between paragraphs | `20–28px` |
| Between component blocks | `20–32px` |
| Card padding | `16–32px` (scales with card importance) |
| Button padding | `14px 20px` |
| Rail connector height | `6px` |
| Border-radius: cards | `12–16px` |
| Border-radius: buttons | `8–12px` |
| Border-radius: pills/badges | `20px` |

---

## Fonts to Load

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&family=Zilla+Slab&display=swap" rel="stylesheet">
```

---

## Quick Checklist for New Learning Pages

1. **Three-column layout?** Rail + main + optional sidebar
2. **Sticky nav at top?** Back/Next buttons with gradient fade
3. **Rail thumbs updating?** Upcoming/current/completed states
4. **Warm stone background?** `#faf5f0`, never pure white for the page
5. **Zilla Slab for step titles only?** Regular weight, never bold
6. **Body text at 17px with 1.8 line-height?** Generous, readable
7. **Dark cards for key moments?** Navy with golden text
8. **Callouts for tips and context?** Left-bordered, color-coded
9. **Prompt blocks with copy buttons?** Navy background, monospace
10. **Transitions subtle and purposeful?** 0.15–0.25s, ease/ease-out
