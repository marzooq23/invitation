# Development

When starting the dev server, use background mode:

```
astro dev --background
```

Manage the background server with `astro dev stop`, `astro dev status`, and `astro dev logs`.

# Documentation

Full documentation: https://docs.astro.build

Consult these guides before working on related tasks:

- [Adding pages, dynamic routes, or middleware](https://docs.astro.build/en/guides/routing/)
- [Working with Astro components](https://docs.astro.build/en/basics/astro-components/)
- [Using React, Vue, Svelte, or other framework components](https://docs.astro.build/en/guides/framework-components/)
- [Adding or managing content](https://docs.astro.build/en/guides/content-collections/)
- [Adding styles or using Tailwind](https://docs.astro.build/en/guides/styling/)
- [Supporting multiple languages](https://docs.astro.build/en/guides/internationalization/)

# Project Context

## Project Overview

This project is a **read-only, single-page wedding invitation website** intended for static hosting on AWS.

The goal is to create a polished, mobile-first digital wedding invitation that guests can open easily from links shared through WhatsApp or similar channels.

The site should be lightweight, fast, responsive, accessible, and easy to maintain.

## Technology Stack

- **Framework:** Astro
- **Language:** TypeScript
- **Styling:** Tailwind CSS
- **Rendering:** Static site generation
- **Hosting target:** Amazon S3 + CloudFront
- **Source control:** Git + GitHub
- **GitHub repository:** `marzooq23/invitation`
- **Deployment direction:** GitHub Actions → Astro build → S3 → CloudFront

### Technology Principles

- Keep the architecture simple.
- No backend is required.
- No database is required.
- No authentication is required.
- No API layer is required unless a future requirement explicitly introduces one.
- Avoid adding dependencies unless they solve a real design or functional need.
- Prefer native Astro capabilities and CSS/Tailwind for interactions and animation before introducing additional client-side libraries.
- Keep client-side JavaScript to a minimum.

## Site Architecture

The website is conceptually a **single SPA-style continuous invitation experience**, not a collection of separate pages.

The information architecture is:

```text
01  LANDING
02  nikkah
03  EVENTS
04  VENUE
05  THINGS TO KNOW
06  DUAS & THANKS
```

These are sections within the primary page, with navigation and/or scrolling between sections as appropriate.

## Site Sections

Each section has a dedicated spec file under `docs/`:

- [01 — LANDING](docs/01-landing.md)
- [02 — Nikkah English](docs/02-nikkah-english.md)
- [02 — Nikkah Tamil](docs/02-nikkah-tamil.md)
- [03 — EVENTS](docs/03-events.md)
- [04 — VENUE](docs/04-venue.md)
- [05 — THINGS TO KNOW](docs/05-things-to-know.md)
- [06 — DUAS & THANKS](docs/06-duas-and-thanks.md)

## Overall User Journey

The complete invitation should follow this narrative:

```text
01 — LANDING: Who are they? When are they getting married?
02 — nikkah: What is the sacred occasion?
03 — EVENTS: What is happening and when?
04 — VENUE: Where is it?
05 — THINGS TO KNOW: What does the guest need to know?
06 — DUAS & THANKS: A warm closing and request for duas.
```

## Content Hierarchy

The website should prioritize information in this order:

1. Couple names
2. Wedding date
3. nikkah details
4. Event dates and times
5. Venue and directions
6. Guest information
7. Closing message

Important logistical information should always be easy to find without requiring excessive scrolling.

## Navigation

Navigation should provide quick access to all six sections:

- LANDING
- nikkah
- EVENTS
- VENUE
- THINGS TO KNOW
- DUAS & THANKS

On mobile, navigation should remain compact.

The navigation may use either:

- A minimal fixed header
- A compact menu
- A floating navigation control
- Section-based anchor navigation

The final navigation design will be decided later.