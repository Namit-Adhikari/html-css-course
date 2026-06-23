# Static YouTube Clone

![GitHub License](https://img.shields.io/github/license/Namit-Adhikari/html-css-course)
![HTML5](https://img.shields.io/badge/HTML5-orange?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-blue?logo=css3&logoColor=white)

A static YouTube clone website built with HTML and vanilla CSS. Simple, yet mimics the basic functionalities of YouTube.

## Table of Contents

- [Overview](#overview)
- [Demo](#demo)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running Locally](#running-locally)
- [Architecture](#architecture)
- [Project Structure](#project-structure)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Overview

This repository contains a static YouTube clone built using only HTML and vanilla CSS. It includes responsive layout, tooltip popup on hover, and basic redirecting functionality, following production-grade documentation standards and clean code practices.

## Demo

- Live demo: `https://namit-adhikari.github.io/html-css-course/`

## Key Features

- Redirect to YouTube when clicking as usual
- Responsive web design using `media` query
- Tooltip popup on hovering
- Header and sidebar fixed on window

## Tech Stack

- HTML5
- CSS3

## Getting Started

Follow these steps to run the site locally.

### Prerequisites

- Modern web browser

### Installation

1. Clone the repository

```bash
git clone https://github.com/Namit-Adhikari/html-css-course.git
```

1. Navigate to the project directory

```bash
cd html-css-course
```

### Running Locally

Open `index.html` directly in the browser

## Architecture

The application is structured in a simple, maintainable way:

- `index.html` - page structure
- `/styles` - stylesheet directory

## Project Structure

```text
html-css-course/
  html-css-course/
    channel-pictures/
    icons/
    styles/
      general.css
      header.css
      sidebar.css
      video.css
    thumbnails/
  index.html
  LICENSE
  README.md
```

## Testing

This sample project is simple and uses manual verification:

1. Open the site in a browser
2. Click on thumbnails, titles, channel pictures or channel names to confirm if it redirects to YouTube
3. Confirm channel names, channel pictures, video thumbnails or video titles are correct
4. Validate responsive behavior when window size of the browser is changed

## Design Decisions & Tradeoffs

### HTML & CSS Only (No JavaScript)

**Decision:** The site was built without any CSS frameworks or JavaScript codes for learning foundational web design.  
**Pros:** Simple to develop, faster rendering, no JS dependency, better for learning.  
**Cons:** No interactivity because of no JS, slow development time due to not using any frameworks.

### CSS Grid vs Flexbox for Video Layout

**Decision:** For video thumbnails in home feed, `display: grid` was chosen over flexbox.  
**Pros:** Better for 2D layouts.  
**Cons:** Less browser support in older devices.

### Fixed Header & Sidebar Layout

**Decision:** Used `position: fixed` for persistent navigation.  
**Pros:** Mimics YouTube UX, familiar to users.  
**Cons:** Reduces screen real estate for video thumbnails.

## Technical Challenges & Solutions

| Challenge                                                                                          | Solution                                                                                                     |
| -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| While scrolling the page, inconsistency of elements getting laid over/under relative to the header | Used suitable `z-index` values to lay all of the elements under the header                                   |
| Misalignment of position of channel tooltips                                                       | Used `position: absolute` for tooltip div and `top: 55px` for alignment                                      |
| Video thumbnails became too small when zoomed in                                                   | Used `@media` query to position 2, 3 or 4 video thumnails per row depending on the zoom level or window size |

## Future Improvements & Scalability

If this project scaled to production:

1. **Add JavaScript** for dynamic video feeds, search, and filtering
2. **Implement backend API** to replace hardcoded data
3. **Performance optimization** (lazy loading images, code splitting)
4. **Testing framework** (unit + integration tests)
5. **Build tooling** (bundler, minification, asset optimization)

## Deployment

To deploy your fork or clone:

1. Enable GitHub Pages in your repository settings
2. Set the source branch to `main` (or your default branch)
3. Your site will be live at `https://<your-username>.github.io/<repo-name>/`

Alternatively, use:

- Netlify
- Vercel
- Any static hosting provider

## Contributing

1. Fork the repository
2. Create a feature branch
3. Add and test your changes
4. Submit a pull request with a clear summary

## License

This project is licensed under the [MIT License](LICENSE).
