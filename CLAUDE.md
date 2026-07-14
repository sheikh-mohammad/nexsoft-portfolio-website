# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio website for **Sheikh Mohammad Ahmed** — a Nexsoft Solutions internship task. Vanilla static site (HTML/CSS/JS), no build tools or frameworks.

**Site:** Single-page responsive portfolio  
**Deploy target:** Vercel or Netlify (zero-config static hosting)  
**Theme:** Dark/Light toggle

## Content Source

All profile content is documented in detail:

- **`docs/user-profile.md`** — Full profile: experience, projects, skills, education, socials, client work
- **Permanent memory** (auto-loaded for Claude) — `user-profile` and `portfolio-website` memories under `.claude/memory/`

Key facts: Sheikh Mohammad Ahmed — Web Developer & AI Builder | Co-Founder @ Aplinode | Full Stack Developer Intern @ Nexsoft | Former Co-Founder & CEO @ Markaaf Studio, Former Co-Founder & CTO @ Turbo Services | Hackathon Winner (1200+ participants)

## Development

Static site — no build step required:

```bash
# Local server (pick one)
npx serve .
python -m http.server 8000
```

## Project Structure

```
/
├── index.html          # Single-page portfolio (all sections)
├── css/
│   └── style.css       # 1000+ lines — dark/light themes via CSS custom properties,
│                       #   glassmorphism, gradients, responsive breakpoints, animations
├── js/
│   └── main.js         # Theme toggle, mobile nav, cursor effects, scroll animations,
│                       #   project filtering, contact form, back-to-top, parallax
├── docs/               # Requirements, profile doc, resume PDFs
└── README.md
```

**No `assets/` directory** — profile image is loaded directly from GitHub avatars CDN. No local images or icons needed (Font Awesome CDN for icons).

## Design System

- **CSS Custom Properties** for theming — `:root` vars switched via `[data-theme="dark"]` / `[data-theme="light"]`
- **Gradients:** Inspired by profile photo (warm earth tones). Primary: `#D4A373 → #9D4E4E` (gold → burgundy), Accent: `#E8C4A0 → #C4845D` (cream → terracotta)
- **Fonts:** Source Serif 4 (headings — Adobe's premium serif, reliable & unique) + Quicksand (body — fully rounded, no sharp edges).
  - These are chosen to avoid overused AI-slob fonts (no Inter, Poppins, Space Grotesk, etc.)
- **Glassmorphism:** `backdrop-filter: blur()` on navbar, status card, project overlays
- **Animations:** `fade-in` class for scroll-triggered reveals (IntersectionObserver), floating orbs, pulse glow
- **Custom cursor** on desktop (dot + trailing ring)
- **Responsive:** Mobile-first breakpoints at 1024px, 768px, 480px

## Key Features

- **Theme toggle** — Dark/Light with localStorage persistence
- **Project filter** — Tab-based filtering (All / Hackathons / Companies / Clients)
- **Scroll animations** — Elements fade up on scroll via IntersectionObserver
- **Active nav tracking** — Highlights current section in navbar on scroll
- **Navbar auto-hide** — Hides on scroll down, shows on scroll up
- **Parallax** — Subtle parallax on hero background grid and orb

## Deployment

Vercel or Netlify — zero-config static hosting. Just connect the repo.
