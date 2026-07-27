# EVMC — Eastern Visayas Medical Center Landing Page

A responsive, single-page **landing website** for the **Eastern Visayas Medical Center (EVMC)** — a Department of Health (DOH) government tertiary hospital in Tacloban City, Leyte, Philippines. The page presents the hospital's identity, core services, key statistics, news, and contact information in a clean, mobile-friendly layout.

It is a **static, zero-build** site: plain HTML and CSS on top of Bootstrap 5, with no server or build step required.

---

## Table of Contents

- [Overview](#overview)
- [Tech stack](#tech-stack)
- [Project structure](#project-structure)
- [Page sections](#page-sections)
- [Core services featured](#core-services-featured)
- [Running it locally](#running-it-locally)
- [Deploying](#deploying)
- [Customizing](#customizing)
- [Contact information (as shown on the page)](#contact-information-as-shown-on-the-page)
- [Notes](#notes)

---

## Overview

EVMC is presented as a premier **1,500-bed capacity** medical center serving the entire Eastern Visayas region, spanning **16 departments**. The page narrative highlights the hospital's growth from a provincial hospital into a regional referral center, its resilience following Super Typhoon Yolanda, and its commitment to accessible, evidence-based healthcare.

The site's tone is institutional and reassuring, with prominent 24/7 emergency hotlines and clear service information.

Design goals:

- **No build step** — open `index.html` and it runs in any browser.
- **Mobile-first & responsive** — Bootstrap 5 grid with a collapsible navbar.
- **Information-forward** — emergency contacts, services, stats, and news are all above-the-fold or one scroll away.

---

## Tech stack

| Layer | Choice |
|---|---|
| Markup | Semantic HTML5 (single `index.html`) |
| Layout / components | [Bootstrap 5.3](https://getbootstrap.com/) (CSS + JS bundle, via CDN) |
| Icons | [Bootstrap Icons 1.11](https://icons.getbootstrap.com/) (via CDN) |
| Custom styling | `assets/css/styles.css` |
| Interactivity | Bootstrap bundle only (responsive navbar toggle) — no custom JS |

The Bootstrap CSS/JS and icon fonts load from a CDN; everything else (styles, images, logo) is local to the repo.

---

## Project structure

```
EVMC-LandingPage/
├── index.html                  # the entire page
└── assets/
    ├── css/
    │   └── styles.css          # custom EVMC theme on top of Bootstrap
    └── photos/
        ├── logo/               # EVMC logo(s)
        ├── news/               # news/announcement images
        └── *.jpg               # hero / building photos
```

---

## Page sections

1. **Top info bar** — fixed strip with emergency hotlines, email, and a "24/7 Service" note.
2. **Main navbar** — fixed, with EVMC logo/brand and navigation links (Home, About Us, Departments, Contact). Collapses to a hamburger menu on small screens.
3. **Hero** — full-width banner with the hospital name.
4. **Welcome / About** — the hospital's story and mission, with stat boxes highlighting **1,500+** bed capacity and **16** departments.
5. **Our Core Services** — a grid of service cards (see below).
6. **Need Medical Assistance? (CTA)** — call-to-action with phone and appointment prompts.
7. **News & Announcements** — recent updates (e.g., the opening of a state-of-the-art Cardiology Center).
8. **Footer** — address, contact details, quick links, social links, the "EVMC CARES" values (*Compassionate · Accessible · Resilient · Excellent · Sensitive*), and copyright.

---

## Core services featured

Each service is a Bootstrap card with an icon and a short list of highlights:

- 🫀 **24/7 Emergency Department**
- 🩺 **Outpatient Department (OPD)**
- 💧 **Laboratory & Diagnostics**
- ⭐ **Specialty Centers**
- 🌎 **OFW & Seafarer Services**
- 📖 **Teaching & Research**

---

## Running it locally

No server or build required:

1. Open the project folder.
2. Double-click **`index.html`** to open it in any browser.

> Tip: `styles.css` is linked with a root-absolute path (`/assets/css/styles.css`). If custom styles don't appear when opening the file directly, serve the folder with a simple static server so the root path resolves — for example:
> ```bash
> python3 -m http.server 8000
> # then visit http://localhost:8000
> ```

An internet connection is needed to load the Bootstrap and Bootstrap Icons CDN assets.

---

## Deploying

As a static site, it can be hosted anywhere:

- **GitHub Pages** — enable Pages and serve from the repo root.
- **Netlify / Vercel / Cloudflare Pages** — no build command; publish directory is the root.
- **Any web server** — copy the files to the web root (which also makes the `/assets/...` absolute paths resolve correctly).

---

## Customizing

- **Content:** edit `index.html` (much of the styling is inline plus Bootstrap utility classes).
- **Theme / colors / spacing:** edit `assets/css/styles.css` (the EVMC brand blues and section styling live here).
- **Images:** replace files in `assets/photos/` (logo, hero, and news images).

---

## Contact information (as shown on the page)

- **Emergency Hotlines:** (0977) 346-0358 · (0928) 388-7722
- **Email:** evmc@doh.gov.ph
- **Address:** Barangay 93 Bagacay, Tacloban City, Leyte, Philippines
- **Landline:** (053) 832-5309
- **Website:** evrmc.doh.gov.ph
- **Facebook:** facebook.com/EVMC

---

## Notes

- This repository contains a **front-end landing page only** — it is a presentational website, not a hospital management system, and has no backend or data collection.
- All contact details and content above are transcribed from the page markup for reference.
