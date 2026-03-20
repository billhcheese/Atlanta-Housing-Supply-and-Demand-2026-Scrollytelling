# Housing Income Metro Atl Scrollama

A single-page scrollytelling layout that swaps a Flourish story embed based on scroll position using Scrollama + D3.

This is inspired and edited from Kontinentalist's template for this.

## Files

- `index.html`
  - Page structure and all scrolly “steps” (`.step` elements).
  - Loads external libraries (Bootstrap, jQuery, D3, Scrollama, Flourish embed).
- `styles.css`
  - Typography and layout styling for the scrolly section (`#scrolly__section`, `.step`, `.scrolly__content`).
  - Any special-case spacing tweaks (e.g. `.br-tight`).
- `main.js`
  - Scrollama setup and the `handleStepEnter` handler that updates the Flourish iframe `src` for the active step.

## How it works

Scrollama watches the `.step` elements. When a step becomes active, `handleStepEnter` updates the Flourish embed iframe to the matching slide index.

## Customization

- Update the Flourish story:
  - In `main.js`, change the `linkHead` constant:
    - `https://flo.uri.sh/story/<STORY_ID>/embed#slide-`
- Edit the step content:
  - In `index.html`, change the HTML inside each `.step` container.
- Tighten a specific line break spacing:
  - Add `class="br-tight"` to a `<br>` and keep `.br-tight` in `styles.css`.

## Dependencies (CDN)

This project loads:

- Bootstrap 4.6
- jQuery (slim)
- D3 v5
- IntersectionObserver polyfill
- Scrollama
- Flourish embed script

## Running it locally

This is a static page. You can typically open `index.html` directly in a browser.

