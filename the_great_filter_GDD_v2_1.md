# The Great Filter — Complete Game Design Document v2.1

---

## Vision & Philosophy

A roguelite civilization survival game rooted in the Fermi Paradox. The universe is indifferent. Most civilizations don't make it. Every decision is permanent. Winning feels rare and earned. Losing feels meaningful not cheap.

The filters are never planetary events. They are **civilization-wide crises** that hit your entire civilization simultaneously. The same crisis plays out differently across each planet your civilization spans because each planet has a different profile. You are never managing planets. You are managing one civilization that happens to live on multiple planets.

---

## Epistemological Core — Why Everything Is Invisible

The invisibility in this game is not a design choice for difficulty. It is a **philosophical position.**

We don't know what Mars will actually cost us. We have estimates. We have projections. We have models and simulations. But the moment boots hit regolith the black swans begin — supply chains we didn't anticipate, psychological costs of isolation we underestimated, soil chemistry that surprises us, energy demands that dwarf projections. The player not knowing the exact cost profile of each planet isn't a mechanic. **It's the truth.**

This extends to everything in the game:
- We don't know which filter will kill us — **black swan**
- We don't know what The Great Filter actually tests — **black swan**
- We don't know what an alien world will demand of us — **black swan**
- We don't know if our civilization is balanced enough — **black swan**

The player has exactly what humanity has — the information we've gathered about each place. Everything beyond that they were never supposed to know. The game is saying: **you never had the information. You never will. You make your best decisions with what you can observe and the universe decides the rest.**

The game's thesis: **You are not supposed to know. Neither were we.**

---

## The Information Gradient

The player knows exactly what humanity knows about each planet. No more. No less. This is the natural difficulty curve — not artificial game balancing, but the actual state of human knowledge.

| Planet | What player knows | Uncertainty level |
|--------|------------------|------------------|
| Earth | Everything — lived experience, history, intuition, centuries of data | Minimal |
| Mars | A lot — decades of research, missions, rovers, atmospheric data | Some black swans |
| Europa | Some — observed it, theorized about subsurface ocean, extreme radiation known | Many unknowns |
| Kepler-452b | Very little — distant observations, rough size and orbit estimates only | Mostly unknown |
| Alien worlds | Almost nothing | Pure black swan territory |

**On Earth** the player feels confident. They've lived here. They know food matters, energy matters, society holds things together. They make informed decisions.

**On Mars** the player feels cautious. They know it's cold, atmosphere is thin, soil is toxic. They know Energy and Food will be expensive. But how expensive exactly? They don't know. Black swans lurk.

**On Europa** the player feels genuinely uncertain. Subsurface ocean. Extreme radiation. No solid ground we understand well. They're guessing now. Educated guessing but guessing.

**On alien worlds** they're completely blind. Every investment is a hypothesis.

This is also why losing always feels fair. The player can never say the game didn't tell them. The game told them exactly what humanity knows. Everything beyond that — they were never supposed to know. That's not a game being unfair. That's the universe being the universe.

---

## Visual Style & UI

- Pixel art retro aesthetic throughout
- Main screen is a **solar system view** — planet center screen, stars, ambient space atmosphere
- Planet pulses gently during investment phase
- Space darkens and stars flicker as a filter approaches
- Filter strike = dramatic pixel animation over the planet(s)
- Pass = planet(s) glow bright, relief
- Fail = planet cracks, goes dark, civilization retreats
- Jumping to new solar system = dramatic moment, different star color, different planet aesthetics entirely
- **One UI change only as civilization expands** — a small number in one corner showing how many planets your civilization currently spans (1, 2, 3...)
- No dashboards per planet, no panel switching, no complex multi-screen UI
- Clean, atmospheric, minimal text always
- **No hints ever** — player learns through failure alone
- Planet profiles communicated through visual environmental cues only — atmosphere color, soil texture, terrain type, light quality. Never through numbers or text.

---

## The Four Fields

Civilization-wide resources. Always just these four. Never more. Investment pool is shared across all planets your civilization spans.

| Field | Emoji | Represents |
|-------|-------|------------|
| Food | 🌾 | biological survival, population health |
| Energy | ⚡ | power, industry, infrastructure |
| Science | 🔬 | research, technology, adaptation |
| Society | 🤝 | culture, governance, social cohesion |

**How fields interact with planets:**
- Science → same return regardless of planet, one civilization-wide research pool
- Food → efficient on fertile planets, terrible return on hostile ones (Mars has no soil)
- Energy → consumed faster as more planets added, hostile planets demand disproportionately more
- Society → holds civilization together across all planets, more planets = more passive strain

**The invisible complexity:** Player never sees "Mars is consuming 40% of your Energy." They feel it through draining numbers and have to reason why. They look at the corner number. It says 3. They adjust. Or they don't. And a filter comes.

---

## Resource Economy

- Each field generates its own resource per second passively
- Food → feeds population → influences coin income rate
- Energy → powers infrastructure → accelerates Science gain
- Science → multiplies all field effectiveness over time
- Society → reduces resource drain during filter strikes
- Player spends coins to invest into any field at any time
- **Decisions are irreversible** — once invested, cannot be reallocated
- The player who spammed Food and ignored Science earned their Plague death

---

## Planet Upgrade System

The planet itself can be upgraded as a separate investment — distinct from the four fields. Upgrading represents terraforming, infrastructure development, industrial capacity — making the world physically more capable of sustaining and growing civilization.

**Base income starts at 8 coins/sec on every planet regardless of field levels.** Field investments modify how income compounds and multiplies internally over time, but the raw per/sec only doubles through deliberate planet upgrades. This gives income a spine — it is a conscious decision not a passive drift.

| Stage | Planet looks like | Cost to upgrade | Per/sec |
|-------|------------------|----------------|---------|
| 0 | dim, sparse, barely alive | — | 8/sec |
| 1 | slightly brighter, early infrastructure visible | 150 coins | 16/sec |
| 2 | glowing, complex surface patterns | 400 coins | 32/sec |
| 3 | fully alive, radiant, dense civilization visible | 900 coins | 64/sec |
| 4 | peak — maximum planetary civilization | 2000 coins | 128/sec |

**Rules:**
- Planet upgrade resets to stage 0 on every new planet — you are starting from scratch on a new world with no existing infrastructure regardless of how advanced your previous civilization was
- Upgrade costs are fixed regardless of planet profile — the work of building infrastructure costs the same everywhere. What differs is how much your field costs drain your ability to save for it
- The visual evolution of the planet is the only indicator of upgrade stage — no number shown, player reads the planet
- Upgrade button is always visible alongside the four fields — it competes for the same coin pool

**The strategic tension this creates:**
Upgrade the planet early → better income → stronger field investment → better filter survival, but field levels stay low when early filters arrive. Invest in fields first → survive early filters → but income stays at 8/sec → later filters demand more than weak income can sustain. Neither approach is obviously correct. Both can fail. Both can succeed. The right answer depends on which planet you are on, which filters are coming, and how much surplus you built on the planet before.

**On hostile planets the tension is explicit:** On Mars, 8/sec with expensive Food and Energy costs means every coin is spoken for. Saving 150 coins for a stage 1 upgrade while also needing Science and Energy invested before the Plague arrives is a real civilizational choice that has no clean answer. That pressure is intentional. That is what it would actually feel like.

---

## Planet Cost Profiles

Each planet has natural conditions that make certain fields cheaper or more expensive. This is **never shown as numbers** — communicated purely through visual environmental cues (atmosphere color, soil texture, terrain type). Player reads the environment and adapts or fails.

**Example profiles:**

| Planet | Food | Energy | Science | Society |
|--------|------|--------|---------|---------|
| Earth | cheap | cheap | normal | normal |
| Mars | very expensive | expensive | normal | normal |
| Europa | nearly impossible | expensive | cheap | normal |
| Kepler-452b | cheap | cheap | normal | expensive |
| Alien worlds | unknown | unknown | unknown | unknown |

**Habitable does not mean Earth-like.** Gas giant moons, frozen oceans, thin atmosphere worlds all count as habitable. Dead rocks do not. Habitable means survivable with sufficient investment.

---

## Income & Expenditure Scaling

- Each new planet added doubles civilization-wide coin income per second
- But each planet's cost profile determines how efficiently that income converts
- A hostile planet (Mars) may largely neutralize the income boost
- A friendly planet (Kepler-452b after Earth) may feel like genuine net progress
- More planets = more Society strain passively regardless of profile
- **The ghost of past decisions compounds** — a Society-neglected Earth civilization arrives at Mars fractured, twice as resource-rich but socially unstable, and Mars filters punish that

**Lucky run:** Earth → Kepler-452b → another friendly profile → income doubles feel real, player gets far
**Brutal run:** Earth → Europa → income doubled but Food is nearly impossible on Europa, hostile profile punishes underprepared civilizations

**The surplus principle — this game is not fate:** A brutal run is only truly brutal if the player arrived underprepared. The early game on any planet is not just about surviving its own filters — it is a window to build surplus that becomes leverage on the next planet. A player who builds excess Food, Energy and Science on Earth beyond what the filters demand arrives at Europa with a buffer. The hostile Food profile still bites but surplus cushions it. A sloppy player who scraped through Earth's filters with nothing in reserve arrives at Europa naked and collapses immediately. The difference is not luck. It is strategy. Luck determines which planet comes next. Strategy determines whether you survive it.

---

## The Six Filters

Filters are **civilization-wide crises**, not planetary tests. The same filter hitting a 3-planet civilization is fundamentally harder than hitting a 1-planet civilization because the same resource pool must now satisfy multiple hostile profiles simultaneously.

**Timer rule — each filter doubles arrival time:**

| # | Filter | Arrives after |
|---|--------|--------------|
| 1 | 🦠 The Plague | 10 seconds |
| 2 | ☢️ The War | 20 seconds |
| 3 | 🌡️ Climate Collapse | 40 seconds |
| 4 | 🤖 The Machine God | 80 seconds |
| 5 | 👽 The Signal | 160 seconds |
| 6 | ✨ The Great Filter | no timer — arrives unpredictably |

**Why 10 seconds is correct and not unfair:** No one handed early humans a tutorial on how to survive. No tooltip explained what a plague would do to an underprepared civilization. You figure it out or you don't. Next time you know a little more. The brutal opening is honest, not cruel.

---

## Each Filter's Dynamic Algorithm

No filter is static. Each tests a combination of fields in ways that punish tunnel vision and reward balance. **None of these algorithms are ever shown to the player.** The player learns them only through repeated failure across runs.

**🦠 The Plague**
- High Food + low Science = plague spreads through well-fed but uncured population → death
- High Science + low Energy = cure exists but no power to distribute it → death
- On a multi-planet civilization — Science is shared but Energy and Food effectiveness differs per planet profile. Mars may starve through the plague even if Earth is fine.
- Pure Food investment = guaranteed death regardless of planet count
- Sweet spot: Food + Science + enough Energy, all reasonably balanced

**☢️ The War**
- High Energy + low Society = aggressive militarized civilization that self-destructs
- High Society + low Energy = cannot defend, overwhelmed
- Energy and Society must balance
- Science contributes deterrence
- On multiple planets — Society strain is already higher, War hits harder
- Neglect either Energy or Society = death

**🌡️ Climate Collapse**
- High Energy use damages environment
- High Food overdone = deforestation and soil depletion
- Science provides solutions but slowly
- Society enables policy change, fastest fix but requires prior investment
- All 4 fields must be reasonably invested — any neglected field = death
- On multiple planets — Energy consumption across hostile planets accelerates collapse
- Most punishing of imbalance of all early filters

**🤖 The Machine God**
- High Science + low Society = AI has no ethical framework, goes rogue → death
- High Society + low Science = AI never developed, civilization too primitive to pass threshold → death
- Science and Society must be close to each other in investment level
- Energy required to run AI systems
- Most punishing of the Science/Society gap specifically

**👽 The Signal**
- Aliens judge your civilization's profile as a whole
- High Energy + low Society = perceived as dangerous and militaristic → destroyed
- Low Science = too primitive to be considered → ignored → destroyed
- All fields must be high, Society weighted most heavily in the judgment
- On multiple planets — a fractured multi-world civilization with low Society reads as chaotic and threatening
- Highest explicit threshold of all named filters

**✨ The Great Filter**
- No timer shown — arrives unpredictably after The Signal, player never knows when
- No filter animation — screen goes completely dark first
- Silence
- Your 4 field numbers float on screen
- Single line: **"THE UNIVERSE DECIDES"**
- 3 second pause
- Hidden randomized weights applied to all 4 fields — different every single run
- Nobody knows what The Great Filter actually tests. That is the point.
- Survival chance weighted by investment balance quality:
  - Perfect balance across all 4 fields → 90% survival
  - Slightly imbalanced → 60%
  - Badly imbalanced → 20%
- Never guaranteed. Never purely luck. The universe is harsh but not entirely cruel.
- Win screen is quiet, not celebratory — you are one of the few

---

## Progression Structure

```
Spawn on first habitable planet in procedurally generated solar system
                    ↓
   Invest in 4 fields + upgrade planet to grow income
                    ↓
          Win all 6 filters including The Great Filter
                    ↓
        Another habitable planet in this solar system?
               ↓ yes              ↓ no
        Expand there        Jump to next solar system
        corner now says 2   new star, new aesthetics
                    ↓
     Now managing civilization across 2 planets simultaneously
     Same 4 fields, same UI, same coin pool
     But economics changed — one corner number tells all
                    ↓
         Survive filters again as larger civilization
                    ↓
              Keep expanding...
```

**Expansion stages:**

| Stage | Corner number | Description |
|-------|--------------|-------------|
| Planetary | 1 | Learn the basics, one profile, known territory |
| Interplanetary | 2-4 | Same system, multiple profiles, one pool |
| Interstellar | 5+ | New solar systems, alien profiles, unknown costs |
| Intergalactic | mythical | Almost no one reaches this. Ever. |

---

## Loss System & Irreversibility

**During single planet phase:**
- Fail any filter → full game over, run ends immediately
- No fallback to another planet — the civilization had one world and lost it
- Milestone is recorded — if this was the first planet, no inheritance. Next run starts from scratch.

**During multi-planet phase:**
- Fail any filter → full game over, run ends immediately
- The filter is civilization-wide — failing it means the entire civilization failed, not just one planet
- No retreat to base planet — a civilization that couldn't survive the Plague couldn't survive it anywhere
- Milestone is recorded before run ends — next run inherits the progress reached

**The irreversibility rule:**
- All investment decisions permanent within a run — no reallocation ever
- The player who spammed one field and died to the filter that punished it earned that death
- No second chances on the same planet in the same run
- **Fail any filter at any stage = game over, full stop.** No retreat. No fallback within a run. The filter is civilization-wide — if the civilization failed it, it failed everywhere simultaneously. A civilization that couldn't cure the Plague on Mars also couldn't cure it on Earth. The disease does not respect which planet you colonized first.

---

## Inherited Progress

Civilizations fall. But knowledge doesn't vanish entirely. The next attempt builds on what the last one reached. This is not a second chance — it is inherited progress. That is different. And it is true. Knowledge compounds even when civilizations fall.

**Milestone system — next run starts at the highest stage previously reached:**

| Milestone reached in previous run | Next run starts at |
|----------------------------------|-------------------|
| Never left first planet | Start at Earth, solar system 1, no inheritance |
| Reached interplanetary (2+ planets) | Start with 2 planets already colonized |
| Reached interstellar (new solar system) | Start at solar system 2 |
| Reached intergalactic | Start at solar system 3+ |

**Rules:**
- Milestone is saved permanently — survives across all runs
- Starting further does not mean starting easier — filters still arrive with full force, field levels still start at zero, planet stage still starts at 0
- The inheritance is position only — the next civilization starts where the last one reached, not with what the last one had
- A player who reached interstellar and keeps dying at interstellar still starts at interstellar — they are not pushed back
- Intergalactic milestone is the only one that cannot be inherited further — if you reached it once you start there every run after

**Why this feels right:**
The first run is brutal — total darkness, no knowledge, starting from nothing. Each run the player starts slightly further into the unknown. Long term, players slowly push the frontier run by run. The universe doesn't get easier. The player just begins closer to where it gets hard.

---

## Solar System Generation

- Each run gets a procedurally generated solar system
- Random number of habitable planets per system (sometimes 1, sometimes 4)
- Planet profiles drawn randomly from a pool of known and unknown types
- No two runs visit the same sequence of planets
- Lost planets in current run removed from that run's pool only
- If no habitable planets remain in current solar system → jump to next solar system
- Jumping solar systems only happens when the current system is exhausted of habitable planets

---

## Save System

- Progress persists between sessions completely
- Player can stop at any point and return exactly where they left off
- Current field investment levels saved
- Current solar system layout and remaining habitable planets saved
- Which solar systems have been cleared saved
- Long term progression toward intergalactic saved
- The game does not require completing anything in one sitting

---

## What The Player Feels Across A Run

```
Early — frantic, hopeful, clicking fast, learning
Warning approaches — dread sets in
Filter strikes — chaos, watching numbers
Pass — brief relief, then next timer starts
New planet — same screen, corner says 2, something feels different
Numbers draining faster — why? Oh. Two planets now.
Filter hits civilization-wide — Earth fine, Mars struggling
Lose Mars — retreat, grief, Earth alone again
Build back up — wiser now
The Great Filter arrives with no warning — darkness — silence
"THE UNIVERSE DECIDES"
...
```

---

## Replayability Pillars

- Procedural solar systems mean no two runs are identical
- Planet profiles and the information gradient create different strategic demands each run
- The Great Filter's randomized weights mean even perfect play keeps tension
- Players develop intuition across runs — Europa deaths teach food crisis management
- Lucky runs and brutal runs both feel fair because both reflect real knowledge states
- Community stories emerge naturally — players share their routes and their losses

---

## What This Game Actually Is

Not a fun arcade game. A quiet dread simulator. You watch your civilization breathe across an indifferent universe and hope your decisions were wise enough. The complexity is never shown — it is felt. The same four fields, forever, but the weight behind them grows with every planet.

The game is epistemologically honest. It gives you exactly what humanity has — the knowledge we've gathered, nothing more. The black swans that await on Mars, on Europa, on worlds we've never seen — those aren't game mechanics. They're the truth. Most civilizations don't make it. The ones that do feel it.

---

*Document v2.3 — inherited progress system added, loss system clarified. Complete.
