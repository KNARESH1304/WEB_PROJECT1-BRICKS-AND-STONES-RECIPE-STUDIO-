# Bricks and Stones Recipe Studio

CSC 4370/6370 – Web Programming | Track A: Recipe Studio | Extension pack: Story Pack

**Team:** Kothoju Naresh (002923882), Sri Krishna Teja Gangina (002923905), Sattwik Bhattacharjee (002960354)

## Project story
A recipe website for beginner home cooks. Users browse pizza recipes, choose servings, save favorites, order from a menu, and cook along step by step. Everything works with HTML and CSS only (hidden radio buttons/checkboxes + `:checked` selectors). No JavaScript, no AI API.

## How to run
1. Unzip the folder.
2. Open `index.html` in a browser (Chrome, Edge, Firefox, or Safari). No build step or server is needed.
3. Keep `index.html`, `styles.css`, and the `images/` folder together.

## Folder structure
```
index.html      all screens (panels switched with CSS)
styles.css      all styling
images/         16 photos (currently placeholders - replace with real photos, same file names)
docs/           proposal, dev-journal.md, qa-notes.md
links.txt       required links
```

## Bonus features (all six, embedded in the main flow)
All features are HTML/CSS only. They simulate AI ideas with fixed rules; no model, API, or JavaScript is used.

| # | Feature | Where you see it | AI concept it represents |
|---|---|---|---|
| 1 | AI Assistant Panel | "Help" button on every screen | Conversational AI: intent cards map to pre-written response templates |
| 2 | Recommendation Engine UI | Home, Favorites, Cart, Cook-Along ending | Recommender system with explainable AI (confidence meter + "Why this suggestion?") |
| 3 | Predictive Progress Dashboard | Favorites page | Forecasting: milestone cards show estimated time and fill in as you progress |
| 4 | Computer Vision Overlay | Recipe Detail ("Scan ingredients") | Object detection: scan line, then labeled bounding boxes with confidence |
| 5 | AI Ethics & Safety Notices | Recipe steps, Cook-Along, Cart, Menu, About | Responsible AI: Low/Medium/High risk labels with mitigations |
| 6 | Model Comparison Cards | Home (above suggestions) | Model trade-offs: speed, quality, cost; the chosen model changes the confidence meters |

### Full integration
The assistant is on every page. Suggestions react to your saved recipes and cart. Forecast cards react to favorites, cart, order, and cook-along. The scan and risk notes sit inside the recipe pages. The model cards control how the suggestion meters look.

### Innovation evidence
- State-driven suggestion cards using `:has()`, with a "Not helpful" button that hides a card (a feedback loop).
- Choosing a model changes the confidence meters on every suggestion card.
- The scan runs as a CSS-only animation sequence: scan line, then result boxes.
- In Cook-Along, ticking the mitigation checkbox turns the Next button solid (a soft nudge, never a lock).

### How each feature is implemented
Hidden radio buttons and checkboxes hold state; labels act as buttons; `:checked`, `:has()`, and sibling selectors show or hide content. Reusable patterns: `.suggest-card`, `.meter`, `.risk` (low/med/high), `.model-card`, `.fc`, `.bubble`.

### Trade-offs
- Rules and confidence values are fixed examples, so variety is limited.
- CSS-only state resets when the page reloads.
- Scan boxes are pre-placed and will not match every photo exactly; adjust the `--x --y --w --h` values after you add real images.
- `:has()` needs a recent browser (Chrome, Edge, Safari 15.4+, Firefox 121+).
- Too many warnings can cause alert fatigue, so High risk is used only for oven steps.

### Testing evidence
29 automated checks (layout, accessibility, responsive) pass; see `docs/qa-notes.md`.

## AI assistance disclosure
AI (Claude, by Anthropic) helped draft the project proposal and prepare this package (renaming, placeholder images, README draft). Add any other AI help (code, ideas, wording) here.

## Image credits
Add photographer name, source link, and license for each photo in `images/` here.

## Design trade-offs / reflection
(Write after the project is finished.)
