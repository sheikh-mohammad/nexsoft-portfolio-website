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

## Sections to Build

- **Navbar** — Responsive, collapsible on mobile
- **Hero** — Name, title, tagline, CTA buttons
- **About** — Bio summary from profile
- **Skills** — Tech stack grid: HTML, CSS, JS, Bootstrap, Tailwind, React, Next.js, TypeScript, Node.js, Python, Firebase, Supabase, OpenAI Agents SDK, Claude Code, n8n, Git, Figma, Vercel, Netlify
- **Experience** — Timeline of roles (Aplinode, Nexsoft, Turbo Services, Markaaf Studio)
- **Projects** — Hackathons (Helplytics AI, Maintain-IQ, Roberto-Web), Company websites (Aplinode, Markaaf Studio, Turbo Services), Client works (Sai Sapata, Hamida Khokhar, Al Suffah Academy, Lodhi Academy, Molana Qari Abad, Trendz Automotives)
- **Contact** — Social links (GitHub, LinkedIn, X/Twitter, Facebook, Email) + resume download
- **Footer** — Copyright, quick links
- **Theme toggle** — Dark/Light mode switcher

## Development

Static site — no build step required:

```bash
# Local server (pick one)
npx serve .
python -m http.server 8000
```

## Project Structure (Expected)

```
/
├── index.html          # Single-page portfolio
├── css/
│   └── style.css       # Main styles + dark/light theme variables
├── js/
│   └── main.js         # Theme toggle, smooth scroll, interactivity
├── assets/
│   ├── images/         # Profile photo, project screenshots, icons
│   └── resume.pdf      # Downloadable resume
└── docs/               # Requirements, profile, references
```

## Design Decisions

- **Vanilla only** — No frameworks, no bundlers, no npm. Keep dependency-free.
- **CSS custom properties** for theming (dark/light toggle)
- **Flexbox/Grid** for responsive layout
- **Mobile-first** responsive approach
- Font Awesome or plain SVG icons for social links

## Deployment

Vercel or Netlify. Both auto-detect static sites — connect repo, it just works.
