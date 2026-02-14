<img src="docs/screenshots/hero.png" width="100%" alt="Saga — Campaign Management for Dungeon Masters" />

<div align="center">

# Saga

**Campaign Management for Dungeon Masters**

![Next.js](https://img.shields.io/badge/Next.js_15-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript_5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React_19-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS_4-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma_6-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

</div>

Saga replaces the scattered notebooks, spreadsheets, and browser tabs that DMs juggle during a campaign. One interface for characters, sessions, milestones, badges, and a full campaign timeline — with a floating dice roller and initiative tracker always one click away.

---

### Features

- **8-Tab Campaign Interface** — Overview, Roster, Badges, Timeline, Combat, NPCs, Add, and Export tabs give every campaign phase its own workspace
- **Floating Dice Roller** — Persistent FAB accessible from any tab for quick checks without leaving your current view
- **Initiative Tracker** — Add combatants, roll initiative, and step through turn order during live encounters
- **NPC Directory** — Searchable, filterable NPC list linked to your campaign for mid-session reference
- **Badge System** — Four rarity tiers (Common, Uncommon, Rare, Epic) for rewarding memorable player moments
- **Onboarding Wizard** — 4-step guided setup walks new DMs through campaign creation in under a minute
- **PWA-Ready** — Install directly to phone or tablet for a native-app feel at the gaming table

---

### Screenshots

<img src="docs/screenshots/feature-1.png" width="100%" alt="Campaign dashboard with character roster, session timeline, and quick stats" />

*Campaign dashboard with character roster, session timeline, and quick stats*

<img src="docs/screenshots/feature-2.png" width="100%" alt="Landing page with feature highlights and dark fantasy aesthetic" />

*Landing page with feature highlights and dark fantasy aesthetic*

<img src="docs/screenshots/mobile.png" width="50%" alt="Saga mobile view" />

*Mobile-responsive layout for use at the gaming table*

---

### Architecture

- Decomposed component architecture with no file exceeding 250 lines — every tab dynamically imported for code-splitting
- 19 RESTful API endpoints across campaigns, characters, badges, sessions, milestones, dice, encounters, and NPCs
- Shared UI kit ensures visual consistency across all 8 tabs without style duplication
- SQLite via Prisma ORM provides zero-config persistence with type-safe database access

---

### Tech Stack

![Next.js](https://img.shields.io/badge/Next.js_15-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript_5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React_19-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS_4-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma_6-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-0055FF?style=for-the-badge&logo=framer&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=for-the-badge&logo=pwa&logoColor=white)

---

### Design Philosophy

> Saga was designed around the DM's workflow — prep before the session, run during play, review after. Every feature maps to a real moment at the table.

---

### D&D Toolkit Suite

Saga is part of a 7-tool suite built for Dungeon Masters who want focused, offline-first tools instead of bloated platforms.

| Tool | Description |
|------|-------------|
| **Saga** | Campaign management — characters, timelines, badges, session logs |
| **[Loreforge](https://github.com/DarkCandyLord/loreforge)** | Template-driven worldbuilding — structured prompts for rich settings |
| **[Intrigue](https://github.com/DarkCandyLord/intrigue)** | NPC relationship mapper — interactive D3.js force-directed network graph |
| **[Oath](https://github.com/DarkCandyLord/oath)** | Session zero generator — social contracts, safety tools, tone setting |
| **[Outlands](https://github.com/DarkCandyLord/outlands)** | Hex crawl generator — SVG hex maps with terrain painting and encounters |
| **[Favor](https://github.com/DarkCandyLord/favor)** | Faction reputation tracker — character-faction heatmap with tier system |
| **[Voicecraft](https://github.com/DarkCandyLord/voicecraft)** | NPC voice profiles — dialect mixing, coaching prompts, sample dialogue |

---

<div align="center">

*Built for Dungeon Masters, by a Dungeon Master.*

</div>
