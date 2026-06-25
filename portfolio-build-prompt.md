# Portfolio Website — Full Build Prompt

## Overview
Build a single-page personal portfolio website for Hammad Tayyab, a Software Engineering student at GIKI (Batch 2025) and ML Intern at FlyRank AI. The design style is **Glassmorphism + Dark Brutalism hybrid** — frosted glass components combined with bold brutalist typography and raw layout energy. It should feel futuristic, alive, and unlike any standard portfolio.

---

## Design System

**Color Palette:**
- Base: Deep navy / near-black (`#0D1B2A` or similar)
- Glass: Semi-transparent white/blue with backdrop blur
- Accent: Amber (`#F4A933`) OR electric cyan — pick whichever complements the dark base better
- Text: Off-white for body, pure white for headings
- Borders: Thin glowing lines in accent color

**Typography:**
- Display / Headings: Bold, oversized, brutalist — something like `Space Grotesk`, `Syne`, or `Bebas Neue`
- Body / Code: Monospace — `JetBrains Mono` or `Fira Code`
- Mix large and small type intentionally — brutalist contrast

**Global Effects:**
- Custom cursor: small glowing dot that trails slightly behind mouse movement
- Scroll-triggered fade-ins for every section
- Smooth single-page scroll, no reloads
- Subtle animated background: slow-drifting particle mesh or very low opacity floating code fragments
- All transitions should feel fluid, not janky

---

## Sections & Layout

### 1. Hero
- On page load: screen flickers once (like a CRT boot), then your name types out character by character in a terminal style
- After name finishes typing, cursor blinks for 1 second, then a rotating subtitle cycles through:
  - `ML Intern @ FlyRank AI`
  - `Hackathon Builder`
  - `GIKI Software Engineering '25`
  - loops infinitely with a smooth fade or typewriter swap
- Background: animated particle mesh, very subtle, dark
- One CTA button below — `View My Work` — that pulses gently and scrolls to Projects
- Layout: full viewport height, centered or left-aligned with brutalist offset

---

### 2. About
- Short, 2-3 lines only — no walls of text
- Fades in on scroll
- Small animated status badge: `@ FlyRank AI — ML Intern` with a blinking green dot (signals "currently active")
- Brutalist touch: large decorative text in background (like `<DEV/>` or `01`) at low opacity behind the content

---

### 3. Skills
- Not a list — skills rendered as glowing pill/tag components
- Tags animate in on scroll (stagger float-in effect)
- Hover on a tag: it lights up brighter and ripples outward
- Grouped loosely by category but displayed in a flowing wrap layout, not a table

**Categories & Skills:**
- Languages: Python, C++, C, SQL, HTML, CSS
- AI / ML: LLMs, Agentic AI, Agents, Supervised Learning, NLP, Data Analysis, Pandas, NumPy, Seaborn
- Web: React, Tailwind CSS, Supabase
- Tools: Git, GitHub, Linux, API Integration, Printify

---

### 4. Projects
- 3 glassmorphism cards — frosted blur background, semi-transparent
- Each card has an animated gradient border that slowly rotates (conic gradient animation)
- Default state: project name, one-line description, tech stack tags visible
- Hover state: card lifts (transform: translateY), full description slides up from the bottom of the card like a drawer, Live and GitHub buttons appear
- Cards laid out in a row on desktop, stacked on mobile

**Project Data:**

**Harold**
- One-liner: Autonomous AI trading agent that reads live market data and executes ETH/USD trades on Kraken
- Full: Perceives live OHLCV data from Kraken, computes RSI/EMA indicators, passes signals to an LLM for buy/sell/hold decisions, executes with hard risk controls — 5% max position size, 10% daily loss limit. Built for lablab.ai AI Trading Agents Hackathon (Mar–Apr 2026).
- Tech: Python, Kraken CLI, Groq/LLaMA, pandas-ta
- GitHub: https://github.com/hammad-tayyab/Trading-agent-harold-of-hackathon-
- Live: none

**Nighabaan (نگہبان)**
- One-liner: Micro-escrow platform protecting Pakistan's informal labor market — lock pay, do the work, release funds
- Full: Locks payment between homeowners and skilled workers, releasing only on job completion. Simple Lock → Work → Release flow targeting Pakistan's PKR 50B+ informal labor sector. Built at GIKI Hackathon under team Malum Afraad.
- Tech: React 18, Vite, Tailwind CSS, Node.js, Express, SQLite, JWT
- GitHub: https://github.com/hammad-tayyab/micathon
- Live: https://nighaban-micro-escrow-platform.vercel.app/

**SkillForge (MalumAI)**
- One-liner: Agentic AI system that turns your skills into a personalized roadmap, GitHub repos, and Google Calendar schedule
- Full: Analyzes a user's skills, interests, and goals, then generates personalized project roadmaps, auto-creates GitHub repositories with starter code, and schedules milestones directly on Google Calendar. Formerly MalumAI, rebuilt with professional modular architecture.
- Tech: Python, Groq API, Google Calendar API, GitHub API, OAuth2, SQLite
- GitHub: https://github.com/hammad-tayyab/AI-agents
- Live: none

---

### 5. Experience
- Minimal, clean timeline
- Single vertical line with one glowing dot for FlyRank AI
- Dot pulses like a heartbeat (CSS animation)
- Entry: `ML Intern — FlyRank AI` with year `2026`
- Brutalist touch: large faded label `EXPERIENCE` rotated 90° beside the timeline

---

### 6. Contact
- Minimal section, no form
- Three icon links: GitHub, LinkedIn, Email
- Hover: icon glows in accent color, label slides in from the side
- Copy email on click with a small toast notification: `Copied!`

**Links:**
- GitHub: https://github.com/hammad-tayyab
- LinkedIn: https://linkedin.com/in/hammad-tayyab-developer
- Email: hammadtayyab.work@gmail.com

---

### 7. Mini-Game — Bug Squasher
- A floating 🐛 bug icon fixed in the bottom-right corner of the screen at all times
- It wiggles subtly on a loop to catch the visitor's eye
- Clicking it opens a fullscreen dark overlay/modal
- Inside the overlay, cartoon bugs spawn randomly and crawl around the screen in various directions and speeds
- Visitor clicks/taps bugs to squash them — each squash triggers a satisfying splat animation (bug squishes, maybe a little burst effect) and the bug disappears
- No score, no timer, no pressure — purely fun and tactile
- Close button (or press Escape) to exit the overlay and return to the portfolio
- Bug and splat visuals should match the dark brutalist aesthetic — keep it stylized, not cutesy

---

### 8. Footer
- Minimal, centered
- Single line: **Copyright @2026**
- No other clutter

---

## Technical Requirements
- Single HTML file preferred (HTML + CSS + JS all in one) OR a React single-page app
- No frameworks required beyond what's needed — keep it lean
- Fully responsive — mobile, tablet, desktop
- All animations must be performant (CSS preferred over JS where possible)
- Fonts loaded from Google Fonts
- No placeholder content — use only the data provided above
