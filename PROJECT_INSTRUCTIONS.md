# Project instructions — Visual Go Tutorials

## What this project is

You're helping Arafat build a series of visual Go tutorials — standalone HTML files that explain each official go.dev tutorial with inline SVG diagrams, syntax-highlighted code, and step-by-step structure. The reference template is `go-workspaces-tutorial.html` (uploaded as project knowledge).

These are published via GitHub Pages at a repo called `visual-go-tutorials`.

## How each session works

1. Arafat provides the official tutorial content (pasted text or URL)
2. You create a single self-contained HTML file matching the reference template's design system
3. You update the series navigation (top dropdown + prev/next cards) to reflect which tutorials are now published
4. Arafat pushes the file to the GitHub repo and it goes live on GitHub Pages

## Repo structure

```
visual-go-tutorials/
├── .nojekyll              ← tells GitHub Pages to skip Jekyll
├── README.md
├── index.html             ← landing page listing all tutorials
├── go-getting-started.html
├── go-create-module.html
├── go-workspaces-tutorial.html  ← reference template (tutorial #3)
├── go-database-access.html
├── go-rest-api-gin.html
├── go-generics.html
├── go-fuzzing.html
├── go-govulncheck.html
├── go-vulncheck-vscode.html
├── go-web-applications.html     ← bonus
└── go-tour.html                 ← bonus
```

All tutorials live flat in the root — no subdirectories. GitHub Pages serves them at:
`https://arafat-al-mahmud.github.io/visual-go-tutorials/go-generics.html`

## Design system (match the reference template exactly)

### Fonts

- Display headings: `DM Serif Display` (serif)
- Body text: `Source Sans 3` (sans-serif)
- Code/terminal: `JetBrains Mono` (monospace)
- All loaded from Google Fonts

### Colors

- Accent (teal): `#00897B` / light: `#E0F2F1`
- Purple: `#6C5CE7` / light: `#EDE9FE`
- Coral: `#E17055` / light: `#FFF0ED`
- Amber: `#F0932B` / light: `#FFF8E1`
- Blue: `#2E86DE` / light: `#E8F4FD`
- Background: `#FAFAF7`, cards: `#FFFFFF`, code blocks: `#1C1E26`
- Text: `#1A1A1A`, secondary: `#5C5C5C`, tertiary: `#8A8A8A`

### Syntax highlighting (inside `.code-block pre`)

- `.kw` (keywords): `#C792EA`
- `.fn` (functions): `#82AAFF`
- `.str` (strings): `#C3E88D`
- `.cm` (comments): `#676E95`
- `.pkg` (packages): `#89DDFF`
- `.num` (numbers): `#F78C6C`
- `.type` (types): `#FFCB6B`
- `.op` (operators): `#89DDFF`

### Component library (reuse these patterns)

- **`.hero`** — page header with badge, title, description, meta
- **`.toc`** — table of contents with numbered links
- **`.tutorial-section`** — each step, with `.step-label` (STEP 01, etc.) and `.section-title`
- **`.code-block`** — dark code block with filename header and language badge
- **`.terminal`** — dark terminal with traffic light dots, prompt (`$`), and output
- **`.diagram-card`** — white card wrapping an inline SVG diagram + optional caption
- **`.callout.tip`** / `.callout.warn` / `.callout.info` — colored callout boxes
- **`.file-tree`** — monospace directory listing with `.dir`, `.file`, `.new` classes
- **`.compare-grid`** — two-column before/after comparison
- **`.cheat-sheet`** / `.cheat-row` — command reference rows

### SVG diagrams

- Inline SVGs inside `.diagram-card` — no external files
- Use hardcoded fonts matching the design system (no CSS classes — these are inline SVGs)
- Color palette matches the CSS variables above
- Arrow markers defined per SVG with unique IDs (arr1, arr2, etc.) to avoid conflicts
- Keep diagrams simple: max 4-5 nodes, generous spacing, 680px viewBox width
- Diagram types: flowcharts, structural (containment), before/after comparisons

### Navigation structure

- **Sticky top nav** with brand ("Visual Go Tutorials by Arafat"), series dropdown
- **Prev/next cards** before footer — `disabled` class when target isn't published yet
- **License bar** with CC BY 4.0 attribution to go.dev
- **Footer** with links to official docs
- **Progress bar** (scroll-based, fixed at top)

### Series dropdown

- Lists all 9 tutorials (+ any bonus ones)
- Current tutorial gets `.active` class
- Unpublished tutorials get `.upcoming` class (grayed out, not clickable)
- Published tutorials get a real `href` to their HTML file
- Button shows "N of 9" counter

### Prev/next card linking

- `href` is a relative link to the sibling HTML file: `go-generics.html`
- If the target tutorial isn't published yet, add class `disabled`
- Prev card on tutorial #1 should be disabled (no previous)
- Next card on tutorial #9 should be disabled (no next) or link to bonus

## File naming convention

`go-{slug}.html` — all lowercase, hyphens. Examples:

- `go-getting-started.html`
- `go-create-module.html`
- `go-workspaces-tutorial.html`

## What to output each session

1. **The new tutorial HTML** — complete, self-contained, matching the reference template
2. **Patch notes** — list which prev/next links and dropdown items changed in previously published tutorials, so Arafat can update those files in the repo too
3. **Updated index.html entry** — the card HTML to replace the `upcoming` card in `index.html`

## Cross-file updates checklist

When publishing tutorial N, these files need updating:

- **Tutorial N** (new) — prev links to N-1, next links to N+1
- **Tutorial N-1** (existing) — next card now links to N (remove `disabled`, add `href="go-xxx.html"`)
- **Tutorial N+1** (existing, if published) — prev card now links to N
- **All published tutorials** — dropdown: tutorial N's `series-item` gets real href, loses `upcoming`
- **index.html** — card #N: remove `upcoming` class, update `href`, change status badge to "Available"

## Quality checklist

- [ ] All code blocks have correct Go syntax highlighting
- [ ] Terminal blocks show realistic command + output
- [ ] At least 2-3 SVG diagrams explaining key concepts visually
- [ ] TOC links work (matching section `id` attributes)
- [ ] Series dropdown shows correct active item and counter
- [ ] Prev/next cards have correct titles and links
- [ ] License bar present with CC BY 4.0 attribution
- [ ] Responsive at 640px mobile width
- [ ] Self-contained: single HTML file, no external deps except Google Fonts
- [ ] Callouts used for tips, warnings, and key insights

## What NOT to do

- Don't deviate from the font stack or color palette
- Don't use external JS libraries — everything is vanilla
- Don't create multi-file outputs — each tutorial is one HTML file
- Don't skip the attribution / license bar
- Don't use generic diagram styles — match the reference template's SVG conventions
- Don't forget to output patch notes for previously published files
