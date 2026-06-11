# andrewspringman.com — Website Specification

## Purpose

A personal hub for Andrew Springman — composer, visual artist, educator, and technologist. The site exists to connect people with Andrew's two core offerings:

1. **Teaching** — mathematical art, composition & songwriting, mathematics, programming, and AI
2. **Commission** — music, artwork, and software built for good causes

The site is not a software product page. It is the front door to a person.

---

## Audience

- People curious about mathematical or generative art (potential collectors, students)
- Musicians and composers looking for education or collaboration
- Organizations with good-cause software or creative needs
- Educators interested in math-through-art approaches

---

## Tech Stack

- **Pure HTML / CSS / JavaScript** — no build step, no framework
- **GitHub Pages** — hosted directly from the `main` branch, served from `/docs` or root
- **Google Fonts** — Space Grotesk (headings), Inter (body), JetBrains Mono (code/math accents)
- No backend. Contact via mailto link or embedded form service (Formspree).

---

## Design System

### Colors

| Token | Value | Usage |
|---|---|---|
| `--bg` | `#09090f` | Page background |
| `--surface` | `#13131f` | Cards, panels |
| `--surface-raised` | `#1c1c2e` | Hover states, raised cards |
| `--accent-blue` | `#4da6ff` | Primary CTA, links, highlights |
| `--accent-gold` | `#f0b429` | Secondary accent, teaching section |
| `--accent-orange` | `#e8622a` | Commission section accent |
| `--text` | `#e8e8f2` | Body text |
| `--text-muted` | `#8888aa` | Labels, captions, secondary text |
| `--border` | `#2a2a3e` | Dividers, card borders |

### Typography

```css
--font-heading: 'Space Grotesk', sans-serif;
--font-body:    'Inter', sans-serif;
--font-mono:    'JetBrains Mono', monospace;
```

- Headings: Space Grotesk, weight 600–700
- Body: Inter, 16px base, 1.6 line-height
- Math/code labels: JetBrains Mono, used sparingly as accent

### Spacing

8px base unit. Section padding: 80px vertical on desktop, 48px on mobile.

### Motion

Subtle only. Fade-in on scroll for cards. No autoplay video. No parallax.

---

## Site Structure

```
/                  Home
/teach             Teaching
/commission        Commission
/gallery           Gallery (art + music)
/about             About & Contact
```

---

## Pages

### Home (`/`)

**Hero:**
- Full-viewport dark section
- Background: a high-quality fractal image from ITGrapher (subtle, not overwhelming — consider low opacity or a cropped detail)
- Headline: `"Where math, music, and art become tools for learning."`
- Subhead: `"I'm Andrew Springman — educator, composer, and generative artist. Here's how I can help you."`
- Two CTAs side by side: `"I want to learn something"` → /teach | `"I need something created"` → /commission

**Three pillars strip** (below hero):
- Icon + label cards for: Teaching · Art · Music
- Brief one-line description each
- Links to relevant deeper pages

**Featured work strip:**
- 3 fractal art images, horizontally scrollable on mobile
- Caption: "Generated with ITGrapher, Andrew's custom Metal renderer"

**Social bar** (footer of home):
- Icons linking to: YouTube, SoundCloud, Instagram, Facebook, X, LinkedIn

---

### Teach (`/teach`)

**Intro:**
- Heading: `"Learn something you didn't think you could."`
- Body: 2–3 sentences. Andrew teaches sophisticated ideas in ways that make them feel inevitable. Whether it's the math behind generative art or the harmony theory behind a jazz standard — the goal is always the same: you leave understanding something beautiful.

**Teaching areas** (card grid, 2-up on desktop):

| Area | Accent | Description |
|---|---|---|
| Mathematical Art | blue | Iterative transformation graphing — how repeated math functions create fractal images. Hands-on with ITGrapher. |
| Composition & Songwriting | gold | Music theory applied to real writing. Harmony, voice leading, form. From fundamentals to advanced techniques. |
| Mathematics | gold | Abstract concepts made concrete. Number theory, geometry, and the mathematics that shows up in the real world. |
| Programming | blue | Languages, logic, and problem-solving. Taught from first principles regardless of experience level. |
| Use of AI | orange | Practical AI literacy. Prompting, agents, automation — for creatives, educators, and professionals. |

Each card: title, 2-sentence description, "Get in touch" CTA.

---

### Commission (`/commission`)

**Intro:**
- Heading: `"Let's build something that matters."`
- Body: Andrew takes on commissioned work selectively — for people and organizations pursuing something genuinely good. If that's you, reach out.

**Three service cards:**

| Service | Description |
|---|---|
| Music | Original compositions, arrangements, production. Sacred, cinematic, educational, and jazz-adjacent work. |
| Artwork | Generative and mathematical art — prints, digital originals, site-specific pieces. |
| Software | Custom tools built for good causes. Preference for nonprofits, educators, and faith communities. |

Each card links to the contact section with a subject pre-filled.

---

### Gallery (`/gallery`)

**Two tabs: Art / Music**

**Art tab:**
- Masonry or uniform grid of fractal art images
- Each image: title, algorithm used (optional), purchase/inquiry CTA
- Note: "All works generated with ITGrapher, a custom Metal renderer built by Andrew"

**Music tab:**
- SoundCloud embeds for available tracks
- YouTube embed for any music videos
- Links to YouTube channel

---

### About & Contact (`/about`)

**Bio section:**
- Heading: `"The through-line is helping people understand beautiful things."`
- Photo placeholder (swap in when available)
- 3–4 paragraph bio covering: who Andrew is, the breadth of what he does, the BGEA work as context (optional — his call), the creative mission
- Skills/roles listed simply: Composer · Educator · Visual Artist · Programmer · AI practitioner

**Contact section:**
- Heading: `"Get in touch"`
- Simple form: Name, Email, Subject (dropdown: Teaching inquiry / Commission / Something else), Message
- Formspree or mailto fallback
- Note: "Andrew reads every message."

---

## Global Elements

### Navigation

Desktop: horizontal nav bar — Logo/name left, links right: Teach · Commission · Gallery · About
Mobile: hamburger menu, full-screen overlay

### Footer

- Copyright line
- Social icons: YouTube, SoundCloud, Instagram, Facebook, X, LinkedIn
- "Built with ITGrapher fractal art"

---

## Content Placeholders

The following need real content from Andrew before launch:

- [ ] High-resolution fractal art images (export from ITGrapher)
- [ ] Bio text and photo
- [ ] Music tracks (SoundCloud links)
- [ ] YouTube channel URL
- [ ] Contact form destination email
- [ ] Any specific artwork titles or descriptions

---

## Deployment

1. Enable GitHub Pages on the `andrewspringman/andrewspringman.com` repo (Settings → Pages → main branch)
2. Point `andrewspringman.com` DNS to GitHub Pages once domain is registered
3. Add `CNAME` file to repo root containing `andrewspringman.com`

---

## Out of Scope (for now)

- CMS / content management
- E-commerce / payment processing (art sales via inquiry only at launch)
- Blog
- Authentication
