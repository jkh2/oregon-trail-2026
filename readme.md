# 🐂 The Oregon Trail — 2026 Edition

> *A living simulation. Not a scripted game.*

A modern reimagining of the classic Oregon Trail powered by a single AI system. Built as a single HTML file — no framework, no build step, no backend. Deploy anywhere in seconds.

---

## What It Is

The Oregon Trail (2026) is a narrative-driven frontier survival game where you lead a wagon party from Independence, Missouri to Oregon City — 2,000 miles of American frontier, circa 1848.

What makes it different from the original:

- **Living narrative** — Every event is written in real time by Claude AI. No two playthroughs read the same.
- **Distinct characters** — Your party members (Samuel the Skeptic, Mary the Optimist) have genuine personalities. They react differently to every decision you make.
- **Natural language input** — No menus. You type what you do. The AI interprets your intent and resolves the outcome.
- **Memory-aware** — The trail remembers. Lose an ox on Day 12 and the AI references it on Day 20.
- **Real consequences** — Dysentery is real. River crossings kill. Starvation is slow. The tombstone screen is there for a reason.

---

## Gameplay

```
Present situation → Player types decision → AI resolves outcome → Narration + dialogue → Repeat
```

The game engine handles all deterministic systems in code:

- Daily food consumption (scales with party size and weather)
- Resource bars (food, health, morale, oxen)
- Trail progress across 11 real landmarks
- Win/death condition checks

The AI handles everything human:

- Narrating what actually happens
- Writing Samuel and Mary's dialogue
- Calculating realistic resource effects
- Injecting random trail events (illness, storms, buffalo herds, river crossings, fort encounters)

---

## Features

- 🏕️ Three professions with real starting bonuses (Farmer, Carpenter, Banker)
- 📍 11 historical landmarks from Alcove Spring to Oregon City
- ☀️ Dynamic weather system (Clear, Cloudy, Rain, Storm, Snow, Hot)
- 🐂 Oxen management — lose them all and you're stranded
- ✝️ Death screen with tombstone and player-written epitaph
- 🌲 Win screen with final stats
- ⌨️ Typewriter text effect on all narration
- 📜 Animated resource bars with danger/warning states
- 🧠 Rolling event memory fed into every AI prompt

---

## Deploy to GitHub Pages

1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set source to `main` branch, root folder
4. Done — your game is live at `https://yourusername.github.io/oregon-trail-2026`

No npm. No build step. One file.

---

## How It Works (Technical)

The game is a single HTML file with three layers:

**Game Engine (JavaScript)**
Handles resource math, daily consumption, location tracking, landmark detection, and win/death conditions. Pure deterministic code — no AI involved in these calculations.

**AI Layer (Anthropic Claude API)**
One API call per turn. The system prompt injects the full game state (day, location, resources, weather, party status, recent events) and instructs Claude to return strict JSON:

```json
{
  "narration": "string",
  "dialogue": [{ "character": "name", "line": "string" }],
  "state_effects": {
    "food_change": 0,
    "health_change": 0,
    "morale_change": 0,
    "oxen_change": 0,
    "distance_change": 15
  },
  "event_summary": "five word summary",
  "weather_update": "Clear"
}
```

JSON enforcement is what keeps the game stable. The AI never touches the UI — it returns data, the engine renders it.

**Memory System**
The last 16 conversation turns and last 8 event summaries are injected into every prompt. The AI knows your trail history without needing a database.

---

## Stack

| Layer | Choice | Why |
|-------|--------|-----|
| Frontend | Vanilla HTML/CSS/JS | Single file, zero dependencies, instant deploy |
| AI | Claude Sonnet (Anthropic API) | Narrative quality, JSON reliability |
| Fonts | Playfair Display, Courier Prime, IM Fell English | Period-appropriate, readable |
| Hosting | GitHub Pages | Free, fast, permanent |

---

## Roadmap

- [ ] Hunting mini-game (probability-based outcome)
- [ ] Fort trading encounters
- [ ] Party member individual health tracking
- [ ] Multiple save slots (localStorage)
- [ ] Persistent leaderboard (Supabase)
- [ ] Mobile layout optimization
- [ ] Sound design (ambient frontier audio)

---

## Built By

**Sentinel AI Systems** — James Keith Harwood II  
Antonito, Colorado · San Luis Valley

Built in collaboration with Claude Sentinel (Anthropic).

*"A small, complete, alive experience."*

---

## License

MIT — fork it, extend it, take it west.
