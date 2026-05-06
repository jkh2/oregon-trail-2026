# 🐂 The Oregon Trail — 2026 Edition

> *A living simulation. Not a scripted game.*

### 🎮 [Play Now → jkh2.github.io/oregon-trail-2026](https://jkh2.github.io/oregon-trail-2026)

A modern reimagining of the classic Oregon Trail powered by AI. Built as a single HTML file — no framework, no build step, no backend. Every playthrough is unique. Every decision has real consequences.

---

## What It Is

The Oregon Trail (2026) places you in 1848, leading a wagon party from Independence, Missouri to Oregon City — 2,000 miles of American frontier. The game is driven by a real AI that narrates every scene, voices your party, and evaluates every decision you make against what was actually happening on the trail.

What makes it different from the original:

- **Living narrative** — No scripted events. The AI writes every scene in real time. No two playthroughs read the same.
- **Zone-aware event system** — 47 historically grounded events across 6 trail zones. The threats on the Platte River are different from the threats in the Blue Mountains.
- **The trail drives the story** — Every turn presents a concrete situation you must react to, with AI-generated choices to guide you. The trail never rests.
- **Pace and rations strategy** — Set your travel pace and food rations independently. Push hard and starve. Rest and fall behind schedule. Every setting has a real cost.
- **Player-initiated actions** — Hunt for food, make camp, trade at forts. You decide when and how to act between events.
- **Natural language decisions** — Type what you do, or pick from AI-generated choices. Or both.
- **Hidden intelligence** — Native encounters have a disposition the player cannot see. Reading Samuel and Mary's reactions is the skill.
- **Persistent memory** — The trail remembers. The AI references a lost ox from three weeks ago.

---

## The Threats Are Real

Every threat is drawn from documented historical accounts of the Oregon Trail, 1843–1855.

**Disease** — Cholera spread through contaminated river water and could kill a healthy adult between breakfast and supper. Dysentery was chronic and draining. Typhoid came from bad water. Scurvy appeared late in long journeys.

**Wildlife** — Rattlesnakes struck from brush, packs, and bedrolls. Scorpions required shaking out boots every morning. Grizzly bears raided mountain camps. Wolves followed the trains for livestock. Mountain lions moved silently. Buffalo stampedes destroyed everything in their path.

**River Crossings** — The Kansas River, the South Platte, the Green River, the Snake, the Columbia — each a genuine risk of drowning, capsized wagons, lost cargo, and dead oxen.

**Native American Encounters** — The reality was layered and the game reflects it honestly. The Shoshone near South Pass were consistently helpful. Sioux trading parties offered buffalo meat and information. Native ferrymen ran legitimate operations. The Pawnee demanded tribute. The Bannock raided livestock. The Cayuse after 1847 made the Blue Mountains dangerous. The player cannot always tell which kind of encounter is coming.

**Human Threats** — Lone riders, fake cutoff salesmen, deserters, desperate emigrants who may be exactly what they claim or something worse.

**Mechanical Failures** — Wheels split in desert heat. Axles cracked on rocks. Without oxen, the wagon stopped — and so did everything else.

---

## Gameplay

```
Event unfolds → AI presents choices → Player decides (or types freely) → AI resolves → Repeat
```

**The game drives. You steer.**

### Pace — set in the status panel

| Pace | Miles/Day | Health Effect |
|------|-----------|---------------|
| Grueling | 22–30 | −5/day |
| Strenuous | 16–23 | −2/day |
| Steady | 12–18 | None |
| Easy | 7–12 | +2/day |
| Resting | 0–3 | +6/day |

### Rations — set in the status panel

| Rations | Food Use | Health Effect |
|---------|----------|---------------|
| Filling | High | +2/day |
| Meager | Normal | None |
| Bare Bones | Very Low | −4/day |

### Action Bar — one click, always ready

- 🏕️ **Continue** — Press on at current pace and rations
- 🦌 **Hunt** — Zone and weather-aware outcomes. Buffalo on the plains, deer in the mountains, almost nothing in the desert.
- 🛌 **Rest** — Make camp. Health recovers. Distance stops.
- 🏪 **Trade at Fort** — Appears within 40 miles of Fort Kearney, Fort Laramie, or Fort Hall.

### AI-Generated Choices

After every narration the AI presents 3–4 concrete options — safe, bold, and creative — plus "Something else..." to type freely.

---

## Event System

| Zone | Miles | Primary Threats |
|------|-------|----------------|
| Early Plains | 0–316 | Cholera, Kansas River, Pawnee tribute, scorpions, mud |
| Plains | 316–640 | Buffalo stampede, Platte crossings, Sioux encounters, alkali water, rattlesnakes |
| Rockies | 640–1,000 | Grizzly raids, mountain grades, Shoshone guides, Sublette Cutoff, wolves |
| Desert | 1,000–1,288 | Water crisis, heat collapse, Bannock raids, Paiute ambush, fake cutoffs |
| Cascades | 1,288–2,000 | Columbia crossing, Cayuse territory, mountain lions, early snow, starvation |
| Global | Any | Illness, lame ox, broken axle, strangers, food spoilage, storms |

Events never repeat back-to-back. Twelve percent of days are quiet.

---

## Features

- 🎭 **47 historically grounded events** across 6 trail zones
- ⚡ **Pace system** — 5 settings from Grueling to Resting with real health tradeoffs
- 🍞 **Rations system** — Filling / Meager / Bare Bones affecting food and health daily
- 🎯 **Action bar** — Hunt, Rest, Continue, Trade at Fort (when in range)
- 🦌 **Hunting** — Zone and weather-aware, narrated vividly win or lose
- 🏪 **Fort trading** — Fort Kearney, Fort Laramie, Fort Hall
- 🏹 **Native encounter system** — hidden disposition, friendly to hostile
- 🃏 **AI-generated choices** — 3–4 options per turn plus free-text input
- 🎨 **AI scene illustrations** — unique frontier image every turn via Pollinations.AI (free, no key)
- 🎬 **Ken Burns effect** — 4 randomized pan/zoom animations per image
- 💾 **localStorage save** — auto-saves every turn, Continue Journey on return
- 📓 **Trail Journal** — writes a `.md` journal to your device; AI reads it as long-term memory (Chrome/Edge)
- 🏕️ Three professions — Farmer, Carpenter, Banker
- 📍 11 historical landmarks from Alcove Spring to Oregon City
- ☀️ Dynamic weather affecting travel and consumption
- 🐂 Oxen management — lose them all and you are stranded
- ⌨️ Typewriter narration effect
- ✝️ Death screen with tombstone and player-written epitaph
- 🌲 Win screen with final trail statistics

---

## Getting Started

This game runs on **Groq's free AI API** — no cost, no credit card required.

1. Go to [console.groq.com](https://console.groq.com) and create a free account
2. Navigate to **API Keys → Create Key** and copy your key (starts with `gsk_`)
3. Open the game, paste your key on the first screen, and begin

Your key stays in your browser only — never transmitted anywhere except directly to Groq.

**Optional — Trail Journal (Chrome/Edge only)**
Click "Connect Trail Journal" before starting and choose a folder. The game creates `oregon-trail-journal.md` there and writes every scene as readable markdown. On long games the AI reads the full journal back as long-term memory.

---

## Deploy to GitHub Pages

1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set source to `main` branch, root folder
4. Done — live at `https://yourusername.github.io/oregon-trail-2026`

No npm. No build step. One file.

---

## How It Works (Technical)

**Game Engine** handles resource math, pace/rations calculations, zone detection, event rolling, fort proximity, location tracking, and win/death conditions. The AI never touches these calculations.

**Strategic Systems** — Pace and rations are set by the player and applied every turn in `dailyTick()`. Pace bounds the AI's `distance_change`. Rations multiply food consumption. Health drifts based on both simultaneously, creating compound pressure on long hard stretches.

**Event System** — `rollEvent()` selects a zone-weighted, repeat-filtered event with 12% quiet-day probability. Events inject historical stakes and, for Native encounters, a hidden disposition the AI evaluates the player's response against.

**Action System** — Hunt, Rest, Continue, and Trade inject specific context into the prompt. The AI knows the difference and responds accordingly — different narration, outcomes, and dialogue for each.

**AI Layer (Groq — Llama 3.3 70B)** — One call per turn. Full game state, pace, rations, active event, action type, and journal context all injected. Returns strict JSON with narration, dialogue, choices, state effects, weather, and image prompt.

**Memory** — Three layers: last 16 conversation turns (short-term), last 8 event summaries (mid-term), full Trail Journal from filesystem up to 4,000 chars (long-term, optional).

**Images (Pollinations.AI — Flux)** — AI crafts an image prompt, engine appends frontier style guidance and a random seed, fetches asynchronously behind a shimmer skeleton. Four randomized Ken Burns animations applied on load.

**Trail Journal (File System Access API)** — One-time folder permission via `showDirectoryPicker()`. Appends a formatted markdown entry after every turn. Read back at session start and injected into the system prompt as long-term memory.

---

## Stack

| Layer | Choice | Why |
|-------|--------|-----|
| Frontend | Vanilla HTML/CSS/JS | Single file, zero dependencies, instant deploy |
| AI Narrative | Groq API (Llama 3.3 70B) | Free tier, fast, strong narrative quality |
| AI Images | Pollinations.AI (Flux) | Completely free, no key required |
| Persistence | localStorage + File System Access API | Save/resume + long-term journal memory |
| Fonts | Playfair Display, Courier Prime, IM Fell English | Period-appropriate, readable |
| Hosting | GitHub Pages | Free, fast, permanent |

---

## Roadmap

- [ ] Individual party member health and death tracking
- [ ] Multiple named save slots
- [ ] Persistent leaderboard via Supabase
- [ ] Mobile layout optimization
- [ ] Ambient frontier audio (wind, fire, oxen, rain)
- [ ] AI video scenes when free video generation matures

---

## Built By

**Sentinel AI Systems** — James Keith Harwood II
Antonito, Colorado · San Luis Valley

Built in collaboration with Claude Sentinel (Anthropic).

*"A small, complete, alive experience."*

---

## License

MIT — fork it, extend it, take it west.
