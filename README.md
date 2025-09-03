# Site Design Change Plan

1. Remove all signatures/traces from original author
2. Change background/foreground/shade with matching color palette
3. Change fonts to Arial, Helvetica, sans-serif
4. Change icons to Material UI or simple ready-to-use icons

## Notes & Progress

- [ ] Remove author signatures
- [ ] Update fonts
- [ ] Update colors
- [ ] Replace icons

# ClaireSite01 Design Change Tracker

## 1. Remove all signatures/traces from original author

- **Status:** ☐ Pending / ☐ In Progress / ☐ Done
- **Files affected:** `_includes/footer.html`, `README.md`, `LICENCE`
- **Planned Steps:**
  1. Remove author text from footer.
  2. Remove author references in README.md and LICENSE.
- **Questions / Notes:**
  - [Q] Can I safely remove all footer credits without breaking layout?
  - [A] Yes, footer is a simple HTML partial. Keep container div intact.
- **Local Test Notes:**
  - Check homepage footer after edit.
- **Git Branch / Commit:**
  - Branch: `remove-author-signatures`
  - Commit message: `"Remove original author signatures from footer and docs"`

---

## 2. Change background/foreground/shade with matching color palette

- **Status:** ☐ Pending / ☐ In Progress / ☐ Done
- **Files affected:** `_config.yml`, `style.css`, possibly `_includes/header.html` or `_includes/footer.html`
- **Planned Steps:**
  1. Update `_config.yml` color section:
     ```yaml
     color:
       primary: C6AD94
       primary-rgb: "198, 173, 148"
       secondary: FAB3A9
       secondary-dark: C6AD94
     ```
  2. Override background/text/button colors in `style.css`.
  3. Test one section at a time (navbar, buttons, modals, footer).
- **Questions / Notes:**
  - [Q] How to make sure buttons inherit the new primary color?
  - [A] Update `style.css` classes like `.btn-primary` or `.btn-default`.
- **Local Test Notes:**
  - Preview locally with `bundle exec jekyll serve`.
- **Git Branch / Commit:**
  - Branch: `update-color-palette`
  - Commit message: `"Update site color palette based on primary/secondary colors"`

---

## 3. Change fonts to Arial, Helvetica, sans-serif

- **Status:** ☐ Pending / ☐ In Progress / ☐ Done
- **Files affected:** `_includes/head.html`, `style.css`
- **Planned Steps:**
  1. Remove Google Fonts `<link>` lines from `head.html`.
  2. Add font override in `style.css`:
     ```css
     body {
       font-family: Arial, Helvetica, sans-serif !important;
     }
     ```
- **Questions / Notes:**
  - [Q] Will removing Google Fonts break layout?
  - [A] No, layout will stay intact; only fonts change.
- **Local Test Notes:**
  - Check headings, body text, buttons.
- **Git Branch / Commit:**
  - Branch: `update-fonts`
  - Commit message: `"Switch site fonts to Arial, Helvetica, sans-serif"`

---

## 4. Change icons to Material UI or simple icons

- **Status:** ☐ Pending / ☐ In Progress / ☐ Done
- **Files affected:** `_includes/head.html`, `_includes/modals.html`, `_includes/footer.html`, `_includes/nav.html`
- **Planned Steps:**
  1. Remove Font Awesome `<link>` from `head.html`.
  2. Replace `<i class="fa ...">` tags with Material UI icons or text/SVG.
  3. Test modals, buttons, scroll-top button, footer social icons.
- **Questions / Notes:**
  - [Q] Can I safely replace FA icons with SVGs?
  - [A] Yes, make sure each `<i>` tag is replaced consistently.
- **Local Test Notes:**
  - Click all modals and buttons, verify icons appear.
- **Git Branch / Commit:**
  - Branch: `replace-icons`
  - Commit message: `"Replace Font Awesome icons with Material UI / SVG"`

---

## General Notes / Tips

- Always **create a separate branch for each change**.
- Commit often to save progress.
- Preview locally using:
  ```bash
  bundle exec jekyll serve
  ```

# Freelancer Jekyll theme

Jekyll theme based on [Freelancer bootstrap theme ](http://startbootstrap.com/template-overviews/freelancer/)

## How to use

- Place a image in `/img/portfolio/`
- Replace `your-email@domain.com` in `_config.yml` with your email address. Refer to [formspree](http://formspree.io/) for more information.
- Create posts to display your projects. Use the follow as an example:

```txt
---
layout: default
modal-id: 1
date: 2020-01-18
img: cabin.png
alt: image-alt
project-date: January 2020
client: The Client
category: Web Development
description: The description of the project

---
```

## Demo

View this jekyll theme in action [here](https://jeromelachaud.com/freelancer-theme)

## Screenshot

![screenshot](https://raw.githubusercontent.com/jeromelachaud/freelancer-theme/master/screenshot.png)

---

For more details, read the [documentation](http://jekyllrb.com/)
