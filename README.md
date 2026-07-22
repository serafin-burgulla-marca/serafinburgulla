
# Serafin Burgulla - Portfolio Website

Personal portfolio for **Serafin Burgulla**, a Political Economy student at Georgetown University. Originally built on Webflow, then migrated to a self-hosted static site for GitHub Pages.

Live at: `https://www.serafinburgulla.com`

---

## Overview

This repository contains a two-page static website with a shared navbar, footer, and stylesheet:

| Page | File | Purpose |
|---|---|---|
| Home | `index.html` | Main portfolio: hero, about me, experience, courses/certifications, academics, and featured projects |
| My Story | `my-story.html` | A three-generation family history page about military service and legacy in Bolivia |

Both pages share one stylesheet (`style.css`) and the same navbar/footer markup, so styling changes should be made once in `style.css` and content changes made per page.

---

## File Structure

```
/
├── index.html    Main portfolio page
├── my-story.html My Story page
├── style.css     All styles, shared by both pages
├── CNAME         Custom domain config for GitHub Pages (www.serafinburgulla.com)
├── images/       All local image assets (photos, logos, icons, tech badges)
└── README.md     This file
```

---

## Home Page (`index.html`) Structure

Sections appear in this order:

1. **Navbar**
   Logo, links to About me, Consulting, Academics, Projects, Certifications, and My Story, plus external LinkedIn and Resume links. Includes a mobile hamburger menu.

2. **Hero**
   Name, one-line identity statement ("Political Economy at Georgetown University. Former unit in the Bolivian Armed Forces. Indigenous. First-generation, low-income student."), an "About me" button, GitHub/LinkedIn/Email icons, and a portrait photo.

3. **About Me** (`#about-me`)
   Three paragraphs of biography covering his background across Bolivia, Peru, Germany, and the United States, the languages he speaks (Quechua, Spanish, English), and the personal and family history that led him to study political economy. Includes a Georgetown University logo/link.

4. **Experience** (`#consulting`)
   A section heading followed by four project write-ups, each with a logo/image, role and title, description, tool logos, and action buttons:
   - **Red UNITAS** - internship in knowledge management for civil society (Bolivia).
   - **AEBEX** (Asociación de Estudiantes Bolivianos en el Extranjero) - president role in educational access, community building, and fundraising.
   - **The Grameen Creative Lab** - pro bono consulting on refugee integration strategy across Germany, France, and Luxembourg.
   - **Hoyalytics Consulting** - capstone data analytics engagement for a regional cafe chain.

5. **Courses, Research, and Certifications** (`#courses`)
   Five certification cards, each with an image, title, issuing organization, description, and topic tags:
   - Code in Place (Stanford University)
   - Foundations of Project Management (Google Career Certificates)
   - Analyst Training Program (Hoyalytics)
   - Full-Stack Development Training (Hoya Developers)
   - Education Policy Capstone Project (Youth In Policy Institute)

6. **My Academic Journey** (`#academics`)
   Three columns of coursework:
   - Economics & Mathematics: Microeconomics I, Macroeconomics I, Calculus I, Calculus II, Statistics & Probability
   - Political Science: International Relations, Elements of Political Theory, History of Latin America, Ethics & Society, Public Speaking
   - Other Courses: Writing and Culture, How Languages are Learned, Intro to Theology, Entrepreneurship

7. **Featured Projects** (`#featured`), split across two sections:
   - **G.U. Federal Credit Union** - paid redesign of a banking web platform for Georgetown's student-run credit union.
   - **L'Oreal Routine Builder** - personal AI-powered skincare/haircare product advisor.
   - **NASA Space Explorer** - personal web app browsing NASA's Astronomy Picture of the Day.
   - **Water Drop Rescue** - personal browser game demonstrating UI/UX, animation, and DOM manipulation.

8. **Footer**
   Repeats the navbar links, social icons (LinkedIn, GitHub, Email), copyright notice, and a "Send an Email" link.

---

## My Story Page (`my-story.html`) Structure

1. **Navbar** (same as home page, links point back to `/#section` anchors on the home page)
2. **Hero** (same content and image as the home page)
3. **My Story** (`#my-story`) - three generations of military service in the Burgulla family:
   - **Serafin I** - grandfather, corporal in the Viacha Motorized Regiment, served in the Nancahuazu War, later became a minibus driver.
   - **Serafin II** - father, served in the Artillery Regiment of the 7th Division of the Bolivian Army, guarded a military factory during a period of terrorism threats.
   - **Serafin III** - Serafin's own service in the Infantry Regiment of the 7th Division, specialized as a unit marksman, connects his service to his great-grandfather's role in the 1952 Bolivian Revolution.
4. **Footer** (same as home page)

---

## Images

All images are stored locally in `images/` and referenced with relative paths (no external CDN dependency). Categories include:

- **Branding/nav**: `nav-bar-logo.png`, `favicon.png`, `apple-touch-icon.png`
- **Icons**: `logo-github.png`, `logo-linkedin.png`, `logo-mail.png`
- **Portraits**: `hero-portrait.png`, `grandfather.jpg`, `father.jpg`, `son.jpg`
- **Institution/org logos**: `new-logo-georgetown.png`, `about-georgetown.png`, `logo-red-unitas.png`, `new-logo-aebex.png`, `consulting-grameen.png`, `consulting-hoyalytics-logo.png`
- **Project thumbnails**: `project-guasfcu.png`, `project-loreal.png`, `project-nasa.png`, `project-waterdrop.png`
- **Certification thumbnails**: `cert-stanford.png`, `cert-google-pm.png`, `cert-hoyalytics.png`, `cert-hoyadev.png`, `cert-policy-capstone.png`
- **Tech/tool logos**: `tech-javascript.png`, `tech-html.png`, `tech-css.png`, `tech-react.png`, `tech-figma.png`, `tech-analytics.png`, `tech-openai.png`, `tech-cloudflare.png`, `tech-bootstrap.png`, `tech-powerpoint.png`, `tech-inkscape.png`, `tech-python.png`, `tech-colab.png`, `tech-sklearn.png`, `tech-pandas.png`, `tech-matplotlib.png`, `tech-git.png`, `tech-miro.png`, `tech-excel.png`

---

## Tech Stack

| Layer | Technology |
|---|---|
| Markup | Semantic HTML5 |
| Styling | Vanilla CSS (no preprocessor, no framework) |
| Fonts | Google Fonts, Open Sans (body) plus Inter (headings) |
| Interactivity | A small inline script toggles the mobile nav menu; no other JavaScript |
| Hosting | GitHub Pages (static), custom domain via `CNAME` |
| Build tools | None, no bundler and no framework |

---

## Deployment (GitHub Pages)

1. Push `index.html`, `my-story.html`, `style.css`, `images/`, and `CNAME` to the repository root on the `main` branch.
2. In the repository, go to **Settings, then Pages, then Source**, and select the `main` branch.
3. The `CNAME` file points the site at the custom domain `www.serafinburgulla.com`. DNS for that domain must have a CNAME record pointing to the GitHub Pages host.
4. Without the custom domain, the site would otherwise be served at the repository's default `github.io` URL.

---

## Design Details

| Property | Value |
|---|---|
| Primary color (buttons, accents) | `#3a73da` |
| Primary hover | `#2d5cb8` |
| Dark section background | `rgb(58, 115, 218)` |
| Body text color | `#333` |
| Muted text color | `#555` |
| Label text color | `#888` |
| Card border | `#e8e8e8` |
| Footer background | `#f5f5f5` |
| Container max-width | `940px` |
| Navbar max-width | `1140px` |
| Card border-radius | `10px` |
| Desktop breakpoint | above `991px` |
| Tablet breakpoint | up to `991px` |
| Mobile breakpoint | up to `767px` |
| Small mobile breakpoint | up to `479px` |

---

## History: Migration from Webflow

This site was originally built and hosted on Webflow. It was migrated to a self-contained HTML/CSS site with no build tools, no CMS dependencies, and no JavaScript frameworks, so it could run on GitHub Pages.

Migration steps taken:

1. Extracted the rendered `<head>` and `<body>` markup from the live Webflow site.
2. Stripped Webflow dependencies: removed the Webflow JS bundles (jQuery, Webflow runtime chunks), the Webflow-generated stylesheet, an analytics widget, and browser extension scripts.
3. Rewrote the CSS from scratch to match the original design's computed values (layouts, colors, spacing, responsive breakpoints), while keeping the original class names so the HTML structure stayed familiar.
4. Updated content: changed the listed major from Computer Science and Mathematics to Political Economy, rewrote the bio, reordered sections to reflect career priorities, and updated coursework.
5. Downloaded all images referenced from Webflow's CDN into the local `images/` folder and repointed every `src` attribute to the local path.
6. Split the page into `index.html` (markup) and `style.css` (styling) for easier editing outside of Webflow.
7. Later added the `my-story.html` page and the Experience section (renamed from an earlier "Consulting and Data" section) directly as new HTML, reusing the shared stylesheet and navbar/footer.

---

## License

Copyright 2026 Serafin Burgulla. All rights reserved.
