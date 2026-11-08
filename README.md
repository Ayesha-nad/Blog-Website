# ✨ Lumen. — Modern Editorial Digital Magazine

> **Student Project:** TSG Web Development — Project 03 (100 Marks)  
> **Topic:** Multi-Page Blog Website  
> **Marks Distribution:** Page Structure (25) • Design Consistency (20) • Visual Design (18) • Responsiveness (15) • File Organisation (12) • Documentation (10)  
> **Live Demo:** [https://ayesha-nad.github.io/Blog-Website/](https://ayesha-nad.github.io/Blog-Website/)  
> **GitHub Repository:** [https://github.com/Ayesha-nad/Blog-Website](https://github.com/Ayesha-nad/Blog-Website)  

---

## 📖 Project Overview

**Lumen.** is a high-end, modern editorial digital magazine designed with the visual sophistication of publications like *Stripe Press*, *Linear*, and *Awwwards* nominees, implemented using strictly **pure HTML5 and CSS3** (zero JavaScript, zero frameworks, zero inline styles).

The aesthetic embraces a calm, confident "Modern Editorial" design language:
- **Warm Ivory Canvas:** `#F7F4EE` warm paper background paired with deep navy-purple ink (`#0F1226`) for optimal reading comfort.
- **Atmospheric Depth:** Multi-layered soft box shadows, 1px hairline dividers (`#E6E1D8`), and an animated drifting aurora glow behind the hero.
- **Editorial Typography:** *Instrument Serif* for expressive headlines paired with an italicized gradient emphasis, grounded by *Plus Jakarta Sans* for clean, legible body text and tracking caps.
- **Pure CSS Interactivity:** CSS-only hamburger menu drawer, infinite gliding typography marquee, floating form labels, and progressive scroll-driven view timeline animations.

---

## 📁 Project Folder Structure

```text
tsg-webdev-p03-yourname/
├── index.html              # Home page: Hero showcase, aurora glow, marquee, feature tiles, latest stories, CTA
├── blog.html               # Blog archive: 4 editorial post cards with featured horizontal desktop layout
├── contact.html            # Contact page: Dark details card & interactive form with pure CSS floating labels
├── css/
│   └── style.css           # ONE shared stylesheet for all 3 pages (11 structured sections)
├── images/
│   ├── favicon.svg         # Modern editorial luminous star brand favicon
│   ├── hero.jpg            # Creative daylight studio workspace photograph (800x600 px)
│   ├── post-1.jpg          # Design & typography moodboard (600x450 px)
│   ├── post-2.jpg          # Clean modern CSS laptop workstation (600x450 px)
│   ├── post-3.jpg          # Kyoto matcha & leather travel journal (600x450 px)
│   └── post-4.jpg          # Mindful workspace & mechanical keyboard (600x450 px)
└── README.md               # Complete documentation, architecture guide & asset credits
```

---

## 📄 Pages Architecture & Content

### 1. Home Page (`index.html`)
* **Shared Site Header**: Translucent frosted-glass sticky bar (`backdrop-filter: blur(16px)`), brand serif logo with gradient dot, desktop nav links with animated underline, subscribe button, and CSS-only hamburger menu toggle.
* **Hero Showcase**:
  * Fluid headline using `clamp(2.8rem, 7vw, 5.5rem)` featuring an italicized gradient keyword (`background-clip: text`).
  * Atmospheric Aurora background: 3 blurred color orbs (indigo, pink, amber) drifting with `@keyframes`.
  * Subtle CSS dotted-grid texture (`radial-gradient`) with zero external image requests.
  * Hero image inside a rounded frame (`border-radius: 24px`) with gentle floating motion (`translateY(0 to -12px)`).
  * Two floating frosted-glass stat cards (`14,000+ Avid Readers` and `4 Curated Longform Essays`) with asynchronous bobbing animations.
* **Infinite Outlined Marquee**: Gliding editorial typography strip (`Design / Slow Travel / Modern Web / Culture / Craftsmanship`) that pauses on `:hover`.
* **Editorial Vision (01 / 02 / 03)**: Three numbered feature cards with hover elevation and border transition.
* **Latest Stories Teaser**: Three compact preview cards with category metadata, publication dates, and reading triggers.
* **Full-Width Call to Action**: Lavender gradient banner encouraging Sunday dispatch newsletter subscription.

### 2. Blog Archive (`blog.html`)
* **Editorial Header Banner**: Centered serif title with italicized gradient emphasis and soft background aurora glow.
* **Four Featured Article Cards** (`<article class="post-card">`):
  1. *Finding Your Creative Rhythm in a Distracted World* (Category: Design & Craft) — **Featured Desktop Layout** with horizontal card orientation.
  2. *Why Modern CSS is Pure Magic in 2026* (Category: Web Craft).
  3. *Slow Travel Notes: Reflections from a Kyoto Cafe* (Category: Slow Travel).
  4. *Building a Low-Noise Digital Sanctuary* (Category: Mindful Living).
* **Flexbox Layout**: Fluid 1-column stack on mobile, expanding to a 2-column editorial grid on tablet and desktop.
* **Hover Micro-Interactions**: Card lift (`-8px`), shadow expansion, subtle image zoom (`scale(1.06)` inside `overflow: hidden`), and category badge lift.

### 3. Contact & Inquiries (`contact.html`)
* **Two-Column Desktop / Fluid Mobile Stack**:
  * **Left Column (Dark Ink Details Card)**: Deep navy gradient background (`--dark-bg`), circular icon chips with hover scaling, direct studio email, telephone, Franklin St address, operating hours, and an animated floating paper plane icon.
  * **Right Column (Interactive Form Card)**:
    * `Name` input with pure CSS floating label.
    * `Email` input (`type="email"`) with floating label and subtle validity border feedback.
    * `Subject` select dropdown with custom SVG arrow indicator.
    * `Message` textarea with floating label.
    * `Send Message` primary gradient pill submit button with hover glow and sliding arrow icon.

---

## ✨ Pure CSS Animations & Technical Highlights

All dynamic effects operate strictly with **zero JavaScript**:

1. **Page-Load Staggered Sequence**: Elements fade and glide up sequentially (`translateY(24px) -> 0`) using classes `.reveal-1` through `.reveal-5` with calculated animation delays (`0.1s` to `0.7s`).
2. **Atmospheric Aurora Drift**: 3 large blurred circles (`filter: blur(80px)`) gently shift positions via `@keyframes auroraDrift1`, `2`, and `3`.
3. **Animated Gradient Typography**: Moving background position loop (`background-clip: text`) gives the hero keyword an organic, luminous feel.
4. **CSS-Only Mobile Menu ("Checkbox Technique")**:
   - Hidden checkbox: `<input type="checkbox" id="nav-toggle" class="nav-toggle">`
   - Label with 3 hamburger bars: `<label for="nav-toggle" class="nav-toggle-label">`
   - Sibling combinator: `.nav-toggle:checked ~ .site-nav { display: flex; }`
   - Hamburger lines rotate into an elegant 'X' via CSS transforms.
5. **Active Page Indicator**:
   - `class="site-nav__link active"` and `aria-current="page"` applied on the active page's link in each HTML file.
   - Styled as a soft lavender pill (`background: var(--tint); color: var(--accent)`).
6. **Pure CSS Floating Labels**:
   - Empty single-space placeholder: `placeholder=" "`
   - Sibling transition: `.form-input:focus ~ .form-label`, `.form-input:not(:placeholder-shown) ~ .form-label` floats the label up and scales it down to `0.8`.
7. **Scroll-Driven Reveal**: Progressive enhancement wrapped in `@supports (animation-timeline: view())` so modern browsers fade cards in smoothly on scroll while unsupported browsers display content normally.
8. **Reduced Motion Accessibility**: Full `@media (prefers-reduced-motion: reduce)` media query deactivates continuous rotations and translates for users with motion sensitivities.

---

## 🎨 Color Palette & Design Tokens

Defined in `:root` in [css/style.css](file:///f:/Internships/The%20Sky%20Gen%20(TSG)%20Web%20Development/Blog%20Website/css/style.css):

| Variable | Value | Purpose |
| :--- | :--- | :--- |
| `--paper` | `#F7F4EE` | Warm ivory page background |
| `--surface` | `#FFFFFF` | Card surfaces & white inputs |
| `--ink` | `#0F1226` | Deep navy headings & body text |
| `--muted` | `#5E6275` | Secondary text & captions |
| `--line` | `#E6E1D8` | 1px hairline dividers & card borders |
| `--accent` | `#5B3DF5` | Primary indigo-violet (buttons, links, active pill) |
| `--accent-2` | `#FF5E8A` | Vibrant pink accent in gradients |
| `--amber` | `#F7B538` | Small highlights & tag accents |
| `--tint` | `#ECE8FF` | Soft lavender background highlights |
| `--dark-bg` | `#0F1226` | Deep navy footer and contact details card |

---

## 🖼️ Royalty-Free Images & Download Guide

To download or replace the images with royalty-free photography from **Unsplash** or **Pexels**, follow these specifications:

| Filename | Search Query (Unsplash / Pexels) | Aspect Ratio & Resolution | Max File Size | Target Mood |
| :--- | :--- | :--- | :--- | :--- |
| `images/hero.jpg` | "creative studio desk laptop plant natural sunlight" | 4:3 (800 x 600 px or 900 x 1000 px) | < 200 KB (JPEG) | Bright natural daylight, clean composition, artistic desk |
| `images/post-1.jpg` | "typography posters graphic design sketchbook markers" | 4:3 or 16:10 (600 x 450 px) | < 180 KB (JPEG) | Design studio moodboard, colorful swatches, pens |
| `images/post-2.jpg` | "developer laptop dark code editor desk plants" | 4:3 or 16:10 (600 x 450 px) | < 180 KB (JPEG) | Clean laptop setup displaying modern code |
| `images/post-3.jpg` | "kyoto cafe wooden table matcha latte journal notebook" | 4:3 or 16:10 (600 x 450 px) | < 180 KB (JPEG) | Warm wooden cafe, ceramic matcha cup, handwritten journal |
| `images/post-4.jpg` | "minimalist workspace mechanical keyboard plant lamp" | 4:3 or 16:10 (600 x 450 px) | < 180 KB (JPEG) | Serene, uncluttered desk, mechanical keyboard, plant |

---

## 📱 Responsive Testing & Breakpoints

* **Mobile (320px – 599px)**: 1-column layout, full-width cards, mobile hamburger toggle, zero horizontal scroll at 320px.
* **Tablet (600px – 899px)**: 2-column post cards, multi-column footer layout.
* **Desktop (900px – 1199px)**: Horizontal nav bar, desktop subscribe button, side-by-side hero and contact layouts, featured 2-column horizontal post card.
* **Large Desktop (1200px+)**: Constrained maximum container width (`1160px`) centered on screen.

---

## 📸 Screenshots (Placeholders)

| Desktop View | Mobile View (375px) |
| :---: | :---: |
| `![Desktop Home](screenshots/desktop-home.png)` | `![Mobile Home](screenshots/mobile-home.png)` |
| `![Desktop Blog](screenshots/desktop-blog.png)` | `![Mobile Blog](screenshots/mobile-blog.png)` |
| `![Desktop Contact](screenshots/desktop-contact.png)` | `![Mobile Contact](screenshots/mobile-contact.png)` |

---

## 🚀 How to Run Locally

You do not need npm, Node.js, or any build tools to view the website.

### Option 1: Direct File Opening
Double-click `index.html` in your file explorer to launch it directly in Chrome, Edge, Safari, or Firefox.

### Option 2: VS Code Live Server
1. Open this project directory in Visual Studio Code.
2. Install the **Live Server** extension.
3. Right-click `index.html` and choose **"Open with Live Server"**.

### Option 3: Command Line
```powershell
# Using Python
python -m http.server 3000

# Or using Node
npx serve -p 3000
```
Then navigate to: `http://localhost:3000/`

---

## 📜 Credits & Third-Party Asset Licenses

* **Typography**:
  * [Instrument Serif](https://fonts.google.com/specimen/Instrument+Serif) by Rodrigo Fuenzalida & Jordan Bell (SIL Open Font License)
  * [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) by Tokotype (SIL Open Font License)
* **Iconography**:
  * [Font Awesome 6 Free](https://fontawesome.com) (CC BY 4.0 / SIL OFL 1.1)
* **Imagery**:
  * High-resolution daylight photography curated for portfolio and educational demonstration.
* **Author**:
  * Handcrafted semantic HTML5 & CSS3 by Senior Front-End Developer.
