# 🐂 The Oregon Trail — 2026 Edition

> *A living simulation. Not a scripted game.*

### 🎮 [Play Now → jkh2.github.io/oregon-trail-2026](https://jkh2.github.io/oregon-trail-2026)

A modern reimagining of the classic Oregon Trail powered by AI. Built as a single HTML file — no framework, no build step, no backend. Every playthrough is unique. Every decision has real consequences.

---

## What It Is

The Oregon Trail (2026) places you in 1848, leading a wagon party from Independence, Missouri to Oregon City — 2,000 miles of American frontier. The game is driven by a real AI that narrates every scene, voices your party, and evaluates every decision you make against what was actually happening on the trail.

What makes it different from the original:

- **Living narrative** — No scripted events. The AI writes every scene in real time. No two playthroughs read the same.
- **Zone-aware event system** — 47 historically grounded events distributed across 6 trail zones. The threats on the Platte River are different from the threats in the Blue Mountains.
- **The trail drives the story** — You are never asked "what do you do?" into a void. Every turn presents a concrete situation you must react to. The trail never rests.
- **Natural language decisions** — No menus. Type what you do. The AI interprets intent and resolves outcome.
- **Hidden intelligence** — Native encounters have a disposition the player cannot see. A hostile response to a friendly Shoshone trading party is a catastrophic mistake. A passive response to a Bannock night raid loses animals. Reading the situation correctly is survival.
- **Character clue system** — Samuel the Skeptic warns when something feels wrong. Mary the Optimist urges openness toward strangers. Their instincts reflect the hidden reality. Learn to read them.
- **Persistent memory** — The trail remembers what happened. The AI references a lost ox from three weeks ago. Past decisions carry future weight.

---

## The Threats Are Real

Every threat in this game is drawn from documented historical accounts of the Oregon Trail, 1843–1855.

**Disease**
Cholera was the deadliest killer — spread through contaminated river water, capable of killing a healthy adult between breakfast and supper. Dysentery was chronic and draining. Typhoid came from bad water and fouled food. Scurvy appeared late in long journeys when food reduced to flour and dried meat.

**Wildlife**
Rattlesnakes struck from trail-side brush, from packs left on the ground, from bedrolls. Children were at greater risk. Desert rattlesnakes carried more venom. Scorpions required shaking out boots and bedrolls every morning. Grizzly bears raided mountain camps. Wolves followed the wagon trains for refuse and livestock. Mountain lions moved silently and took animals. Buffalo stampedes shook the ground and destroyed everything in their path.

**River Crossings**
The most dangerous single decision on the trail. The Kansas River, the South Platte, the Green River, the Snake, the Columbia — each one a genuine risk of drowning, capsized wagons, lost cargo, and dead oxen. Ford, float, hire a ferryman, or wait — every choice has a cost.

**Native American Encounters**
The reality was layered and the game reflects it honestly. The Shoshone near South Pass were consistently documented as helpful — providing horses, fish, and mountain knowledge. Sioux trading parties in early trail years offered buffalo meat and information. Native ferrymen ran legitimate operations at fair prices. The Pawnee demanded tribute on the early plains. The Bannock and Northern Paiute in the Snake River region conducted documented livestock raids. The Cayuse after the 1847 Whitman Massacre made the Blue Mountains genuinely dangerous. The player cannot always tell which kind of encounter is coming. Reading the situation — and Samuel and Mary — is the skill.

**Human Threats**
Lone riders asking to join the party. Men at trail junctions directing wagons toward dangerous cutoffs for a fee. Hard-looking strangers with good horses and no papers. Desperate emigrants who may be exactly what they claim or something worse.

**Mechanical Failures**
Wagon wheels split in dry desert heat. Axles cracked on hidden rocks. Oxen went lame from cracked hooves or overwork. Without oxen, the wagon stopped — and so did everything else.

---

## Event System

The game engine rolls a zone-appropriate event every turn and injects it into the AI's context. The AI weaves it into the scene and closes with it as the next decision bearing down on the party.

| Zone | Miles | Primary Threats |
|------|-------|----------------|
| Early Plains | 0–316 | Cholera, Kansas River crossing, Pawnee tribute, scorpions, mud bogs |
| Plains | 316–640 | Buffalo stampede, Platte crossings, Sioux encounters, alkali water, rattlesnakes, outlaws |
| Rockies | 640–1,000 | Grizzly raids, mountain grades, Shoshone guides, Sublette Cutoff, wolves, deserters |
| Desert | 1,000–1,288 | Water crisis, heat collapse, Bannock raids, Paiute ambush, fake cutoffs, sidewinders |
| Cascades | 1,288–2,000 | Columbia crossing, Cayuse territory, mountain lions, early snow, starvation |
| Global | Any | Illness onset, lame ox, broken axle, wagon wheel failure, strangers, food spoilage, storms |

Events never repeat back-to-back. Twelve percent of days are quiet — which makes the silence feel earned.

---

## Features

- 🎭 **47 historically grounded events** across 6 trail zones, each with real documented stakes
- 🏹 **Native encounter system** with hidden disposition — friendly, neutral, demanding, watchful, or hostile
- 🐻 **Wildlife threats** — rattlesnakes, scorpions, grizzlies, wolves, mountain lions, buffalo stampede
- 👤 **Human threats** — outlaws, deserters, fake cutoff salesmen, desperate strangers
- 🎨 **AI scene illustrations** — every turn generates a unique frontier image via Pollinations.AI (free, no key)
- 🎬 **Ken Burns effect** — four randomized pan/zoom animations with varied durations bring images to life
- 💾 **localStorage save system** — auto-saves every turn, "Continue Journey" on return with day and location shown
- 📓 **Trail Journal** — optional File System Access API feature writes a readable `.md` journal to your device; AI reads it back as long-term memory on extended playthroughs (Chrome/Edge)
- 🏕️ Three professions with real starting resource effects (Farmer, Carpenter, Banker)
- 📍 11 historical landmarks from Alcove Spring to Oregon City
- ☀️ Dynamic weather system affecting travel speed and daily consumption
- 🐂 Oxen management — lose them all and you are stranded
- ⌨️ Typewriter narration effect on every scene
- ✝️ Death screen with tombstone and player-written epitaph
- 🌲 Win screen with final trail statistics

---

## Getting Started

This game runs on **Groq's free AI API** — no cost, no credit card required.

1. Go to [console.groq.com](https://console.groq.com) and create a free account
2. Navigate to **API Keys → Create Key** and copy your key (starts with `gsk_`)
3. Open the game, paste your key on the first screen, and begin

Your key stays in your browser only. It is never transmitted anywhere except directly to Groq's API.

**Optional — Trail Journal (Chrome/Edge only)**
Before starting, click "Connect Trail Journal" and choose a folder on your device. The game creates `oregon-trail-journal.md` there and writes every scene as readable markdown. On long games the AI reads the full journal back as long-term memory — it remembers Day 3 events on Day 40.

---

## Deploy to GitHub Pages

1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set source to `main` branch, root folder
4. Done — live at `https://yourusername.github.io/oregon-trail-2026`

No npm. No build step. One file.

---

## How It Works (Technical)

**Game Engine (JavaScript)**
Handles resource math, daily consumption, zone detection, event rolling, location tracking across 11 landmarks, and win/death conditions. Pure deterministic code — the AI never touches these calculations.

**Event System**
Each turn, `rollEvent()` selects a zone-weighted, repeat-filtered event with a 12% quiet-day probability. The event is injected into the AI context with its historical stakes and, for Native encounters, a hidden disposition the player cannot see. The AI evaluates the player's response against the actual situation and applies consequences accordingly.

**AI Layer (Groq API — Llama 3.3 70B)**
One API call per turn. Full game state, recent event history, active event, and journal context are all injected. The model returns strict JSON:

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
  "weather_update": "Clear",
  "image_prompt": "scene description for image generation"
}
```

JSON enforcement keeps the game stable. The AI returns data — the engine renders it.

**Memory System**
Three layers working together: the last 16 conversation turns (short-term), the last 8 event summaries injected into every prompt (mid-term), and the full Trail Journal read back from the filesystem (long-term, optional). The AI has genuine continuity across a full playthrough.

**Image Layer (Pollinations.AI — Flux)**
The AI crafts an `image_prompt` from the scene. The engine appends frontier style guidance, builds a Pollinations URL with a random seed, and sets it as an image src. Images load asynchronously behind a shimmer skeleton. Four randomized Ken Burns animations are applied on load with varied durations — no two images drift identically. Silent failure on timeout keeps the game running regardless.

**Trail Journal (File System Access API)**
On connection, `showDirectoryPicker()` grants one-time folder access. The engine creates `oregon-trail-journal.md` and appends a formatted entry after every turn. On the next session, the game reads the full journal and injects up to 4,000 characters of history into the system prompt as long-term memory.

---

## Stack

| Layer | Choice | Why |
|-------|--------|-----|
| Frontend | Vanilla HTML/CSS/JS | Single file, zero dependencies, instant deploy |
| AI Narrative | Groq API (Llama 3.3 70B) | Free tier, fast inference, strong narrative quality |
| AI Images | Pollinations.AI (Flux) | Completely free, no key, no account required |
| Persistence | localStorage + File System Access API | Auto-save/resume + long-term journal memory |
| Fonts | Playfair Display, Courier Prime, IM Fell English | Period-appropriate, readable |
| Hosting | GitHub Pages | Free, fast, permanent |

---

## Roadmap

- [ ] Hunting mini-game with probability-based outcomes
- [ ] Fort trading encounters (Fort Kearney, Fort Laramie, Fort Hall)
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
