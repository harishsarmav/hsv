# Design QA

## Comparison target

- Source visual truth: selected dark automation-library concept generated in this conversation.
- Implementation: `index.html`, rendered through `_layouts/default.html` on GitHub Pages.
- Intended viewport: desktop, 1440px wide.
- Intended state: initial homepage.

## Browser evidence

The temporary local static server successfully exposed the semantic page structure and anchor navigation, but it does not process Jekyll front matter, layouts, or Liquid `relative_url` paths. Its output is therefore not valid evidence for visual fidelity: it showed raw front matter and did not apply the layout stylesheet.

## Primary interactions checked

- Primary navigation anchors target their matching `#shortcuts`, `#about`, and `#notes` sections.
- The primary shortcut and the three supporting shortcut cards use the existing iCloud Shortcut URLs.
- GitHub, discussions, X, and LinkedIn links are present.

## Required fidelity surfaces

- Fonts and typography: specified in `assets/css/site.css`; browser rendering after Jekyll processing is still required.
- Spacing and layout rhythm: specified as a two-column desktop hero, featured shortcut, three-card grid, and responsive single-column mobile layout; final visual render is still required.
- Colors and visual tokens: defined in CSS custom properties for charcoal, graphite, mint, and violet.
- Image quality and asset fidelity: custom `assets/img/automation-flow.png` is present and referenced as the hero illustration.
- Copy and content: concise shortcut-led messaging replaces the prior long accordion-led homepage.

## Findings

- [P1] Final GitHub Pages/Jekyll render has not been captured.
  - Evidence: Ruby/Jekyll is not installed in the local environment. A raw static server cannot resolve the Jekyll layout or Liquid paths.
  - Impact: typography, asset paths, and responsive rendering cannot be visually confirmed before publishing.
  - Fix: run the site through GitHub Pages or a local Jekyll environment, then capture the resulting `/hsv/` page at a 1440px viewport.

## Final result

final result: blocked
