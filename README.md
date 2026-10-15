# A travel guide to Bali

A responsive, single-page travel guide to Bali, built with plain HTML and CSS. It started as a project for the [SheCodes Responsive](https://www.shecodes.io/) course and was then extended with my own improvements to layout, accessibility and code structure.

## What it shows

- A hero section with a call to action that scrolls to the intro.
- A "Why Bali?" section with text and an image.
- A "best beaches" section with three cards, each with a photo, description, address, embedded Google Map and a link to learn more.
- A photo gallery section built as social-media-style post cards.
- A footer with useful links and information about the project.

## Skills demonstrated

- **Semantic HTML:** `header`, `main`, `section` and `footer` landmarks, and a consistent heading hierarchy (`h1` > `h2` > `h3` > `h4`).
- **Responsive layout:** CSS Grid and Flexbox, with a mobile breakpoint at 992px. Columns in a row share the same height, and the card buttons are pinned to the bottom.
- **Modern CSS:** custom properties (variables) for colours, typography, spacing and opacity, plus native CSS nesting to keep the stylesheet short and readable.
- **Accessibility:**
  - descriptive `alt` text, and `title` attributes on the map iframes
  - `aria-label`s on repeated "Learn more" links
  - emojis hidden from screen readers
  - text contrast raised for readability, and left-aligned text instead of justified
  - visible keyboard focus styles
  - safe external links with `rel="noopener noreferrer"`
- **Problem solving:** I replaced third-party Instagram embeds with my own post cards, because the embeds' heights could not be controlled with CSS. The cards use a fixed image aspect ratio, so they stay the same height at every screen size.

## Tech stack

- HTML5
- CSS3 (Grid, Flexbox, custom properties, nesting, media queries)
- Google Fonts (Poppins)
- Google Maps embeds

There is no build step and there are no dependencies.

## Project structure

```
.
├── index.html      # Page markup
├── src/
│   └── style.css   # All styles
└── images/         # Photos, avatars and icons
```

## Running locally

Because the page uses root-relative paths (such as `/images/...`), serve the folder with a local web server instead of opening the file directly:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Notes

- The usernames, locations and likes counts in the gallery are placeholders, and the "View more on Instagram" links go to the Instagram home page.
- CSS nesting requires a current browser (Chrome 120+, Safari 17.2+, Firefox 117+).

## Author

Silvia Cremascoli
