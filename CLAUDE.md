# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A personal portfolio website for the Nexsoft Solutions internship program. This is a static site (HTML/CSS/JS) — no build tooling or framework yet. The project is in its initial state with only a README and requirements document.

## Requirements (from docs/requirements.md)

- Responsive homepage design
- About, Skills, Projects, and Contact sections
- Responsive navbar and footer
- Social media links and resume download button
- Deploy on Vercel or Netlify

## Architecture

As this is a greenfield project with no existing code, expect the following structure once built:

- **index.html** — Single-page portfolio with all sections
- **css/** — Stylesheets (main styles, responsive breakpoints)
- **js/** — Client-side interactivity (smooth scroll, form handling, animations)
- **assets/** — Images, icons, resume PDF
- **docs/** — Project documentation and requirements

No framework or bundler is currently configured. Keep the site lightweight and dependency-free unless a specific need (like a static site generator) arises. Vanilla HTML/CSS/JS is the expectation.

## Development

Since this is a static site with no build step:

- Open `index.html` directly in a browser for local development
- Use a simple HTTP server for testing (e.g., `python -m http.server 8000` or `npx serve .`)

## Deployment

The requirements specify deployment to Vercel or Netlify. Both support static sites with zero configuration — just point at the git repository.

## Key Decisions to Track

- **No framework chosen yet** — the project currently has zero dependencies. If a framework is added, update this file with the build commands.
