<div align="center">

# :crossed_swords: Saga

### Campaign Management for Any Roleplaying Player

![Saga — Campaign Management](docs/screenshots/hero.png)

Track characters, milestones, badges, sessions, and campaign timelines.
Built for DMs who want a digital companion for their tabletop adventures.

![Next.js](https://img.shields.io/badge/Next.js-15-black?style=flat-square&logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react&logoColor=black)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-6-2D3748?style=flat-square&logo=prisma)
![SQLite](https://img.shields.io/badge/SQLite-3-003B57?style=flat-square&logo=sqlite&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-Ready-5A0FC8?style=flat-square)

</div>

---

## Overview

Saga is a full-featured campaign management tool built for Roleplaying Player or Dungeon Masters who run tabletop RPG sessions. It replaces scattered notebooks, spreadsheets, and browser tabs with a single, purpose-built interface that supports every phase of the game -- prep before the session, play at the table, and review afterward.

The application ships with a seed campaign (*The Hollow Stars*), four characters, twelve badges, five sessions, and over fifteen milestones so you can explore every feature immediately.

---

## Key Features

### 8-Tab Campaign Interface

| Tab | Purpose |
|-----|---------|
| **Overview** | Campaign summary, recent activity, quick stats |
| **Roster** | Character cards with stats, portraits, and backstory tracking |
| **Badges** | Achievement gallery with 4 rarity tiers (Common, Uncommon, Rare, Epic) |
| **Timeline** | Session history with 15+ milestone markers |
| **Combat** | Initiative tracker for live encounter management |
| **NPCs** | Searchable NPC directory for quick reference mid-session |
| **Add** | Create new characters, sessions, badges, and milestones |
| **Export** | Download campaigns as Markdown or JSON |

### DM Tools

- **Floating Dice Roller** -- A persistent FAB (floating action button) accessible from any tab. Roll any standard polyhedral dice without leaving your current view.
- **Initiative Tracker** -- Add combatants, roll initiative, and step through turn order during encounters.
- **NPC Directory** -- Searchable, filterable list of NPCs linked to your campaign.

### Onboarding Wizard

A 4-step guided setup flow walks new users through campaign creation:

1. **Campaign** -- Name, description, and tone
2. **Character** -- Create your first party member
3. **Tour** -- Quick walkthrough of the interface
4. **Ready** -- Jump into your campaign

### Progressive Web App

Saga is PWA-ready with a web manifest and mobile-optimized layouts. Install it directly to your phone or tablet for a native-app feel at the table -- no app store required.

---

## Architecture

```
saga-app/
  app/
    api/           # 19 RESTful API endpoints
    (routes)/      # Next.js App Router pages
  components/
    tabs/          # Tab-level components (dynamically imported)
    ui/            # Shared UI kit (buttons, cards, modals, badges)
  lib/
    prisma.ts      # Database client singleton
  prisma/
    schema.prisma  # Campaign, Character, Badge, Session, Milestone models
    dev.db         # SQLite database (zero-config)
```

### Design Decisions

| Decision | Rationale |
|----------|-----------|
| **Decomposed components (<250 LOC)** | Maintainability and testability over monolithic files |
| **Dynamic imports for tab content** | Code-splitting keeps initial bundle small; heavy tabs load on demand |
| **Shared UI kit** | Consistent styling across all 8 tabs without duplication |
| **19 RESTful endpoints** | Clean separation between data and presentation layers |
| **SQLite via Prisma ORM** | Zero-config persistence; no database server to manage |
| **Framer Motion** | Polished micro-interactions without a heavy animation library |
| **Sonner for toasts** | Lightweight, accessible notification system |

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Framework | Next.js 15 (App Router) |
| UI | React 19, Tailwind CSS, Framer Motion |
| Language | TypeScript (strict mode) |
| Database | SQLite via Prisma 6 |
| Notifications | Sonner |
| Deployment | PWA-ready, self-hosted |

---

## Design Philosophy

> *Saga was designed around the DM's workflow -- prep before the session, run during play, review after. Every feature maps to a real moment at the table.*

**Prep**: Build your roster, define badges, outline session plans, and populate your NPC directory before game night.

**Play**: Use the floating dice roller for quick checks, the initiative tracker for combat, and the NPC directory for on-the-fly reference -- all without switching apps.

**Review**: Walk through the timeline, award badges for memorable moments, and log milestones that track the campaign's arc over time.

---

## Screenshots

<details>
<summary><strong>Campaign Timeline</strong></summary>

![Timeline View](docs/screenshots/timeline.png)

Session history with milestone markers, narrative summaries, and chronological navigation.

</details>

<details>
<summary><strong>Character Roster</strong></summary>

![Character Roster](docs/screenshots/roster.png)

Party overview with stat blocks, portraits, backstory tracking, and quick-edit actions.

</details>

<details>
<summary><strong>Badge Gallery</strong></summary>

![Badge Gallery](docs/screenshots/badges.png)

Achievement system with four rarity tiers: Common, Uncommon, Rare, and Epic.

</details>

<details>
<summary><strong>Mobile View</strong></summary>

![Mobile View](docs/screenshots/mobile.png)

Fully responsive layout optimized for phones and tablets at the game table.

</details>

---

## Getting Started

```bash
# Clone the repository
git clone https://github.com/Jarredkern/saga.git
cd saga

# Install dependencies
npm install

# Set up the database
npx prisma generate
npx prisma db push

# Seed with sample data (optional)
npx prisma db seed

# Start the dev server
npm run dev
```

Open [http://localhost:3005](http://localhost:3005) in your browser.

---

## API Reference

Saga exposes 19 RESTful endpoints across five resource types:

| Resource | Endpoints | Operations |
|----------|-----------|------------|
| Campaigns | `/api/campaigns` | CRUD, export (Markdown/JSON) |
| Characters | `/api/characters` | CRUD, roster queries |
| Badges | `/api/badges` | CRUD, rarity filtering |
| Sessions | `/api/sessions` | CRUD, timeline queries |
| Milestones | `/api/milestones` | CRUD, session linking |
| DM Tools | `/api/dice`, `/api/encounters`, `/api/npcs` | Dice rolls, initiative, NPC directory |

---

## D&D Toolkit Suite

Saga is one of seven purpose-built tools for Dungeon Masters. Each tool solves a specific DM pain point and works as a standalone application.

| Tool | Description |
|------|-------------|
| **[Saga](https://github.com/Jarredkern/saga)** | Campaign management for Dungeon Masters |
| **[Loreforge](https://github.com/Jarredkern/loreforge)** | Template-driven worldbuilding for TTRPGs |
| **[Intrigue](https://github.com/Jarredkern/intrigue)** | Interactive NPC relationship network mapper |
| **[Oath](https://github.com/Jarredkern/oath)** | Session zero social contract generator |
| **[Outlands](https://github.com/Jarredkern/outlands)** | Hex crawl map generator and terrain editor |
| **[Favor](https://github.com/Jarredkern/favor)** | Faction reputation tracker with heatmap matrix |
| **[Voicecraft](https://github.com/Jarredkern/voicecraft)** | NPC voice profile generator with coaching prompts |

---

<div align="center">

**Built for Dungeon Masters, by a Dungeon Master.**

*May your campaigns be long, your crits be natural, and your players never split the party.*

</div>
