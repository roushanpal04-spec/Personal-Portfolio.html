# Personal Portfolio — Raushan Kumar Pal

A clean, responsive personal portfolio website built with plain HTML, CSS and a bit of JavaScript. It showcases a short bio, university details, projects, skills and contact information.

Live demo: (Add your GitHub Pages URL or hosting link here)

---

## Table of contents

- [About](#about)
- [Features](#features)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Known issues & fixes suggested](#known-issues--fixes-suggested)
- [Improvements & To-do](#improvements--to-do)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## About

This repository contains a single-page portfolio (Index.html) designed to present personal information, university details, skills, projects and contact methods. It's lightweight and easy to customize for anyone who wants a simple static portfolio.

---

## Features

- Responsive layout (desktop + mobile)
- Smooth scroll and section animations
- Sticky header with active link highlighting
- Dark mode toggle with localStorage persistence
- Back-to-top button
- Simple, modern styles built with CSS (no frameworks)

---

## Getting Started

To view this portfolio locally:

1. Clone the repository:
   ```
   git clone https://github.com/roushanpal04-spec/Personal-Portfolio.html.git
   ```
2. Open `Index.html` in your browser:
   - Double-click the file, or
   - Serve with a static server (recommended for some browsers' CORS rules), e.g.:
     ```
     npx http-server .
     ```
     then open the provided local URL.

3. Edit content:
   - Replace images in the `photo/` folder.
   - Update contact links and copy in `Index.html`.

---

## Project structure

- `Index.html` — main site file (HTML, embedded CSS and JS).
- `photo/` — image assets used on the site (profile and college images).
- (Optional) add `README.md` (this file), `LICENSE`, and further assets in future.

---

## Known issues & fixes suggested

When reviewing `Index.html`, the following items were found and recommendations made:

- Favicon data URL: the original SVG string had malformed percent-encoding; use a properly encoded data URL (or host a `favicon.ico`).
- `tel:` link contained a space (`tel:+91 7061535521`) which can break dialing on some devices — remove spaces (`tel:+917061535521`).
- External links that open in a new tab should include `rel="noopener noreferrer"` for security.
- There was duplicated/unstructured text in the University section (stray text and repeated "Hostel & Canteen"). Cleaned by moving content into proper paragraphs/lists.
- Two different scroll handlers were used: consolidate into a single scroll listener to avoid conflicts and improve performance. Prefer `window.addEventListener('scroll', handler, { passive: true })`.
- Use `window.scrollY` explicitly instead of relying on implicit globals like `scrollY`.
- Accessibility improvements: add ARIA attributes to toggles (nav and theme), ensure interactive elements have role/labels.
- Consider optimizing images (resize/compress) and using proper alt text for better accessibility and loading performance.

---

## Improvements & To-do

Suggestions to make the site more robust and modern:

- Extract CSS into a separate `styles.css` and JavaScript to `main.js` for maintainability.
- Optimize images (use webp and responsive srcset).
- Add meta tags for better SEO and social sharing (Open Graph, Twitter Cards).
- Preconnect to Google Fonts to reduce font load time:
  ```html
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  ```
- Consider bundling or self-hosting Font Awesome icons to reduce external requests.
- Add an HTML validator/linter step to CI (GitHub Actions).
- Add unit/visual tests or Lighthouse checks in CI for performance auditing.
- Create a `404` or fallback page if deploying to GitHub Pages.

---

## Contributing

Contributions are welcome. Typical workflow:

1. Fork the repo.
2. Create a branch for your feature/fix: `git checkout -b feature-name`.
3. Commit changes and push: `git push origin feature-name`.
4. Open a Pull Request describing your changes.

If you prefer, file issues for bugs or feature requests and I'll review them.

---

## License

This project can be released under the MIT License. Add a `LICENSE` file if you want to apply it.

---

## Contact

Raushan Kumar Pal  
- Email: raushanpal04@gmail.com  
- Instagram: @_roushannnn_  
- Website / Hosting: (Add your deployed link here)

---
