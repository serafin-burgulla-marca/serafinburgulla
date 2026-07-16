
# Serafin Burgulla — Portfolio Website

Personal portfolio for **Serafin Burgulla**, a Political Economy student at Georgetown University. Migrated from Webflow to a self-hosted static site for GitHub Pages.

---

## Migration Summary

### What happened

This site was originally built and hosted on **Webflow** at `serafinburgulla.dev`. The goal was to migrate it to a clean, self-contained HTML/CSS site that can be deployed on **GitHub Pages** — no build tools, no CMS dependencies, no JavaScript frameworks.

### Migration process

1. **Extracted the Webflow HTML** — copied the rendered `<head>` and `<body>` from the live Webflow site.
2. **Stripped Webflow dependencies** — removed all Webflow JS bundles (jQuery, webflow runtime chunks), the Webflow-generated CSS stylesheet, the Village analytics widget, and browser extension scripts.
3. **Rewrote the CSS from scratch** — matched the original Webflow design using the site's actual computed CSS values (section layouts, colors, spacing, responsive breakpoints). Preserved all original Webflow class names so the HTML structure stayed familiar.
4. **Updated content** — changed the major from Computer Science & Mathematics to Political Economy, rewrote bio sections, reordered page sections to reflect career priorities, and updated the academic coursework.
5. **Separated concerns** — split into `index.html` (markup) and `style.css` (styling) for easier editing in any IDE.

---

## What Changed (Original → Current)

### Content changes

| Section | Original | Current |
|---|---|---|
| **Hero tagline** | "Creating and shipping work that solves real problems. Using data to measure and create impact on people's lives." | "Political Economy at Georgetown University. Former unit in the Bolivian Armed Forces. Indigenous. First-generation, low-income student." |
| **About Me bio** | "I'm a sophomore at Georgetown University studying Computer Science and Mathematics. I'm driven by my endless curiosity, love for learning, and passion for building. In my free time, I make apps for my friends and family to use." | "I'm a rising junior at Georgetown University. With experience across Bolivia, Peru, Germany, and the United States, I have built organizations, managed financial operations, consulted on workforce development for displaced communities, and created scholarship pipelines for students from backgrounds like mine. I speak Quechua, Spanish, and English." |
| **Academics — Column 1** | Computer Science (CS I, CS II, Math Methods for CS, Web Dev) | Economics & Mathematics (Microeconomics I, Macroeconomics I, Calculus I, Calculus II, Statistics & Probability) |
| **Academics — Column 2** | Mathematics (Calc I, Calc II, Combinatorics, Stats, Linear Algebra) | Political Science (International Relations, Elements of Political Theory, History of Latin America, Ethics & Society, Public Speaking) |
| **Academics — Column 3** | Other Courses (Entrepreneurship, Ethics & Society, Public Speaking, Writing and Culture, How Languages are Learned) | Other Courses (Writing and Culture, How Languages are Learned, Intro to Theology, Entrepreneurship) |

### Layout changes (section order)

| Original order | Current order |
|---|---|
| 1. Hero | 1. Hero |
| 2. About Me | 2. About Me |
| 3. Featured Projects (I & II) | 3. **Consulting & Data** *(moved up)* |
| 4. Certifications | 4. Certifications |
| 5. Consulting & Data | 5. **My Academic Journey** *(moved up)* |
| 6. My Academic Journey | 6. **Featured Projects (I & II)** *(moved down)* |
| 7. Footer | 7. Footer |

### Navigation updated to match

Navbar and footer links were reordered: About me → Consulting → Academics → Projects → Certifications.

---

## File Structure

```
/
├── index.html          # Main page markup
├── style.css           # All styles (separated from HTML)
├── images/             # Local image assets (see migration guide below)
│   ├── nav-bar-logo.png
│   ├── logo-github.png
│   ├── logo-linkedin.png
│   ├── logo-mail.png
│   ├── hero-portrait.png
│   ├── about-georgetown.png
│   ├── ...
│   └── favicon.png
└── README.md           # This file
```

---

## Image Migration Guide

All 38 images have been downloaded to the local `images/` folder and `index.html` now references them directly — no more dependency on Webflow's CDN (`cdn.prod.website-files.com`).

### Complete image inventory (38 files)

#### Navbar
| # | Current filename on CDN | What it is | Suggested local name |
|---|---|---|---|
| 1 | `NAV-BAR-LOGO.png` | Site logo in navbar | `nav-bar-logo.png` |

#### Hero Section
| # | Current filename on CDN | What it is | Suggested local name |
|---|---|---|---|
| 2 | `LOGO-GITHUB.png` | GitHub icon | `logo-github.png` |
| 3 | `LOGO-LINKEDIN-BLACK.png` | LinkedIn icon | `logo-linkedin.png` |
| 4 | `LOGO-MAIL.png` | Email icon | `logo-mail.png` |
| 5 | `OFFICIAL (2).png` | Hero portrait photo | `hero-portrait.png` |

#### About Me Section
| # | Current filename on CDN | What it is | Suggested local name |
|---|---|---|---|
| 6 | `HERO-SECTION-PICTURE.png` | Georgetown / about image | `about-georgetown.png` |

#### Featured Projects (card thumbnails)
| # | Current filename on CDN | What it is | Suggested local name |
|---|---|---|---|
| 7 | `8.png` | G.U. Federal Credit Union screenshot | `project-guasfcu.png` |
| 8 | `10.png` | L'Oréal Routine Builder screenshot | `project-loreal.png` |
| 9 | `11.png` | NASA Space Explorer screenshot | `project-nasa.png` |
| 10 | `9.png` | Water Drop Rescue screenshot | `project-waterdrop.png` |

#### Tech & Tool Logos (shared across cards)
| # | Current filename on CDN | What it is | Suggested local name |
|---|---|---|---|
| 11 | `20.png` | JavaScript logo | `tech-javascript.png` |
| 12 | `21.png` | HTML logo | `tech-html.png` |
| 13 | `22.png` | CSS logo | `tech-css.png` |
| 14 | `23.png` | React logo | `tech-react.png` |
| 15 | `24.png` | Figma logo | `tech-figma.png` |
| 16 | `25.png` | Google Analytics logo | `tech-analytics.png` |
| 17 | `26.png` | OpenAI API logo | `tech-openai.png` |
| 18 | `27.png` | Cloudflare Workers logo | `tech-cloudflare.png` |
| 19 | `28.png` | Bootstrap logo | `tech-bootstrap.png` |
| 20 | `29.png` | PowerPoint logo | `tech-powerpoint.png` |
| 21 | `30.png` | Inkscape logo | `tech-inkscape.png` |
| 22 | `31.png` | Python logo | `tech-python.png` |
| 23 | `32.png` | Google Colab logo | `tech-colab.png` |
| 24 | `33.png` | Scikit-learn logo | `tech-sklearn.png` |
| 25 | `34.png` | Pandas logo | `tech-pandas.png` |
| 26 | `35.png` | Matplotlib logo | `tech-matplotlib.png` |
| 27 | `38.png` | Git logo | `tech-git.png` |

#### Certifications (card thumbnails)
| # | Current filename on CDN | What it is | Suggested local name |
|---|---|---|---|
| 28 | `LOGO.png` (Code in Place) | Stanford / Code in Place logo | `cert-stanford.png` |
| 29 | `16.png` | Google PM course image | `cert-google-pm.png` |
| 30 | `LOGO.png` (Hoyalytics) | Hoyalytics logo | `cert-hoyalytics.png` |
| 31 | `17.png` | Hoya Developers image | `cert-hoyadev.png` |
| 32 | `GEORGETOWN (6).png` | Education Policy capstone | `cert-policy-capstone.png` |

#### Consulting Section
| # | Current filename on CDN | What it is | Suggested local name |
|---|---|---|---|
| 33 | `LOGO (2).png` | Hoyalytics consulting logo | `consulting-hoyalytics-logo.png` |
| 34 | `FINAL (2).png` | Miro logo | `tech-miro.png` |
| 35 | `FINAL (1).png` | Excel logo | `tech-excel.png` |
| 36 | `FINAL.png` | Grameen Creative Lab image | `consulting-grameen.png` |

#### Footer
Reuses icons #2 (GitHub), #3 (LinkedIn), #4 (Email) — no new files needed.

#### Favicon & Apple Touch Icon
| # | Current filename on CDN | What it is | Suggested local name |
|---|---|---|---|
| 37 | `FAVICON.png` | Browser tab icon | `favicon.png` |
| 38 | `MAIN LOGO.png` | Apple touch icon | `apple-touch-icon.png` |

### How to replace

Once all 38 images are in your `images/` folder, do a global find-and-replace in `index.html`:

1. Replace all Webflow CDN base URLs with your local path:
   - Find: `https://cdn.prod.website-files.com/69180aff297b32f670982b0d/` followed by the CDN filename
   - Replace with: `images/` followed by your chosen local filename

2. Example — the hero portrait:
   - **Before:** `src="https://cdn.prod.website-files.com/69180aff297b32f670982b0d/691b028d3216cff5d75b6713_OFFICIAL%20(2)-p-800.png"`
   - **After:** `src="images/hero-portrait.png"`

3. Also update the two references in the `<head>` (favicon and apple-touch-icon).

---

## Tech Stack

| Layer | Technology |
|---|---|
| Markup | Semantic HTML5 |
| Styling | Vanilla CSS (no preprocessor) |
| Fonts | Google Fonts — Open Sans (body) + Inter (headings) |
| Hosting | GitHub Pages (static) |
| Build tools | None — no bundler, no framework |

---

## Deployment (GitHub Pages)

1. Create a repository (e.g., `fin-burgulla.github.io` for a user site, or any repo name for a project site).
2. Place `index.html`, `style.css`, and the `images/` folder at the repository root.
3. Go to **Settings → Pages → Source** and select the `main` branch.
4. The site will be live at `https://fin-burgulla.github.io` (user site) or `https://fin-burgulla.github.io/repo-name/` (project site).

---

## Design Details

| Property | Value |
|---|---|
| Primary color (buttons, accents) | `#3a73da` / `rgb(58, 115, 218)` |
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
| Desktop breakpoint | `> 991px` |
| Tablet breakpoint | `≤ 991px` |
| Mobile breakpoint | `≤ 767px` |
| Small mobile breakpoint | `≤ 479px` |

---

## License

© 2026 Serafin Burgulla. All rights reserved.
