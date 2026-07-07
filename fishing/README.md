# Fishing — community mechanics wishlist

Everything the community has proposed about the **fishing** feature, gathered from two places:

- **Bilibili** — the video *"Chinese players wanted fishing, so we made fishing"* ([BV19NTc6VEfg](https://www.bilibili.com/video/BV19NTc6VEfg/)), where players were explicitly asked how they picture the fishing mechanic. Read in full: 103 top-level comments **and all 179 reply-thread messages** — the most detailed design writeups are in the reply threads.
- **QQ groups** — the official Homespace community groups, messages up to 2026-07-07.

Compiled 2026-07-07. Source is tagged on each point: `[B]` = Bilibili, `[QQ]` = QQ.

> **The single loudest signal:** almost everyone benchmarks against **Russian Fishing 4 (RF4)** — they want its *physical feel* but explicitly **without** its punishing hardcore design (endless no-bite sessions, brutal rare-fish grind). "Beat RF4" is repeated dozens of times. `[B][QQ]`

---

## ⭐ Standout detailed writeups (read these in full on Bilibili)

The players below wrote near-complete design proposals. Handles are given so you can find them under the video (most are in the **reply threads**, not the top comments).

1. **孤寡老徐** *(reply thread)* — **the most actionable one.** What players actually love in RF4 is the *reeling feel*, not the gear. Nail just three sensations — a hooking response with a sense of participation, an operational feel while reeling, and a near-real feel when landing — then **simplify all tackle/rigs down to 3-4 branch options + a line-tension parameter.** RF4 is "worthless besides its data and feel, and its operation is user-hostile."
2. **tu2471** *(top comment + long follow-up)* — anti-grind design philosophy. Argues RF4 barely has *new* players; veterans keep making alt accounts to re-feel the early joy, because the game gates fun behind a grind ("delay pleasure to stretch the product cycle — the dumbest method"). Michelin analogy: a restaurant that takes 5 hours to serve isn't good just because it's long.
3. **干辣椒** *(two top comments)* — the full casting/tackle/aquarium spec (see Sections A, C, F).
4. **江尚寒 / "I want a mulberry fish-pond"** *(reply thread)* — a whole life-loop design doc (pond-fishing + farming + cooking + trade). Homespace replied: "this isn't feedback, you've written us half a design doc."
5. **月華玖璃** *(top comment)* — Chinese-style fishing + trophies (Sections C, F).
6. **影丶窗丶雾** *(reply thread)* — an honest map of how *complex* a real fishing system is (Section C).
7. **莽莽纪** *(top comment + reply)* — realism details: line gauge, rod action, rod snapping (Sections A, C).
8. **是啊康啊** & **1爱做的欢喜少年** *(reply threads)* — concrete horror stories about RF4's rare-fish grind and cheating (Section G).
9. **迈耶诚不欺我** *(reply thread)* — "getting skunked is fun too": random encounter events (Section B).

---

## A. Core catching feel

- **The core thesis (孤寡老徐):** players don't love RF4's gear depth — they love the **fight**. Deliver three sensations well and you win: (1) a **hooking response** that feels like you're part of it, (2) an **operational feel while reeling** the fish in, (3) a **near-real feel on landing**. Then keep the rest simple. `[B]`
- **Match RF4's feel, drop the hardcore.** RF4 is named the current market leader for simulation feel, but hated for too few bites and hours with nothing. Aim for that feel, made easier. `[B]`
- **Casting & fighting loop (干辣椒's detailed proposal):** left mouse to cast; charge/hold time = cast distance; farther from shore = deeper water = faster bite; the bobber sinking = a bite; move the mouse left/right to tire and land the fish. `[B]`
- **Fight big fish physically.** Hooking a giant should be a pull/tug struggle; if the character's stats are too low, the fish drags them into the water. A "tug-of-war with an unknown entity" has a fun **gambling feel** to it (you don't know what you hooked). `[B]`
- **Rod elasticity.** Feedback on the current build: the rod is stiff — real rods flex. Add rod flex/elasticity. The bite → reel → out-of-water steps aren't in yet. `[QQ]`
- **Rod & tackle choice:** soft rod vs hard rod; a line-gauge/line-number selection; buy virtual rods modeled on real makers (via in-game currency + skill level); allow the rod to **snap** — e.g. line gauge too high + big fish → line holds but rod breaks; plus occasional accident events that wear out the rod. `[B]`
- **Controller support + haptic vibration** on the strike/catch. `[B]`
- **Keep progression OPTIONAL and light — the skill tree is contested.** One camp wants a tree (faster bite, auto-lift small fish, fish harder to shake off, highlighted/enlarged bobber, shorter fight time, easier at higher level). Another camp says **no skill tree** — trees deter new players and limit fun, exactly RF4's over-restriction. Simplify, don't gate. `[B]`

## B. Getting skunked — the "empty-handed" culture

- Going home with nothing is a beloved part of Chinese fishing culture (they jokingly call it "joining the air force"). Players *want* a realistic chance of catching nothing, but **not frustratingly high**. Make the skunk rate tunable; let skill matter ("bad technique → get skunked hard"). `[B][QQ]`
- **"Getting skunked is fun too" — lean into random events (迈耶诚不欺我).** Anglers run into weird things: a passer-by falls in the water; you fish up junk, or even a high-end PC or a car; you hook a protected wild animal (in China these are legally protected — harming them means big fines) and scramble to free it from the hook. These little events turn a no-catch session into a story. `[B]`
- At minimum, give a splash / near-miss so a skunked player still sees something happen. `[B]`

## C. Chinese-style fishing (localize the fantasy)

- **Prefer hand-rod / traditional still-fishing (Chinese "platform fishing") over lure fishing** — lure fishing arrived in China later; platform fishing is both more familiar *and* easier to implement. `[B]`
- **Depth of the still-fishing system players want:** float/bobber tuning (there's a saying: "one year to learn the bait, three years to tune the float"), line-rig matching, hook-type selection, bait flavor/scent selection, setting the fishing depth, and choosing bottom vs mid-water fishing. Match line / float / hook so the target fish can take the bait cleanly. `[B]`
- **Chumming a spot** (throwing in groundbait before casting); casting frequency. `[B][QQ]`
- **Reality check on scope — a real fishing system is deceptively complex (影丶窗丶雾).** Just the *methods* already fork into: suspended-sinker, bottom, lure, sea, and fly fishing. On top of that: float or no float; reel or no reel; the feel of different reel gear ratios; rod action/tonality; each bait's cast trajectory; water-flow effects; a lure's swimming posture; and a per-fish "force bar" as it swims. All of it is real programming work — a reason to pick a focused subset and do it well rather than everything shallowly. `[B]`

## D. Environment & simulation depth

- **Multiple maps/regions**, each country/region with its own signature "legendary" fish — make them look beautiful. `[B]`
- **Boats → sea fishing.** `[B]`
- **Time of day** changes which fish appear (day/night fishing). `[B]`
- **Weather + four seasons** affect fishing (and farming): ice fishing / rain fishing / night fishing bonuses; different water bodies and terrain → different fish. Multiple QQ users ask directly, "will weather affect fishing and farming?" `[B][QQ]`
- **Remove the water/land "invisible wall"** other fishing games use (where you can only cross by boat) — allow natural interaction at the shoreline. `[B]`
- **Living ecosystem:** fish schooling (a shoal swimming together looks great); predator–prey behavior (carnivores chase omnivores, big fish chase small). `[B]`

## E. The fish themselves

- **Fish catalog / picture-book** like Animal Crossing or Zelda: each fish with size, weight, and encyclopedia info. `[B]`
- **Size/weight variation within a species**, reflected in the model (heavier = bigger, or small/medium/large tiers). `[B]`
- **Rare variants at low probability:** mutations, giant size, albino, colored scales (like theHunter: Call of the Wild). **But see Section G** — rare fish must never become an unwinnable grind. `[B]`
- **Species variety:** ornamental fish, tropical fish, pufferfish; distinguish ornamental vs edible fish. `[B]`
- **Baits & tackle system:** craftable baits, feed types, a dedicated bait for a specific target fish; rod tiers; different tackle catches different fish. `[B]`
- **Fish farming / breeding**; close the loop **catch → raise → eat** as one connected system. `[B][QQ]`
- (co-op flavor) **poisonous fish** that knock you down when landed — funny in multiplayer. Catching mermaids (joke). `[B][QQ]`

## F. Aquariums & display — the biggest recurring theme (ties fishing to the house, the game's core)

- **Keep caught fish in a tank AND a pond;** tanks as live-creature objects. `[B][QQ]`
- **Aquascaping (干辣椒):** tanks of various sizes; décor of water plants, shells, driftwood, shipwreck & treasure; tank lighting; a wave-maker/pump; also shrimp and turtles; categorize them; add a catalog. Reference **Behind Glass** for custom aquariums. `[B]`
- **Fish tank as architecture (strongly upvoted, ties straight into building):**
  - a tank that becomes / embeds into a **wall** (players already wedge tanks into walls to fake this); `[B][QQ]`
  - **glass floor** with fish swimming below + lighting; `[B][QQ]`
  - **glass pillars** with fish inside; `[B][QQ]`
  - **transparent glass ceiling** with fish overhead. `[B][QQ]`
- **Trophy display:** mount catches as trophies in the house — a taxidermy/specimen wall, or hang the fish to show off (one game lets you hang a fish off the back of your car). Named as a big playtime driver. `[B][QQ]`
- **Lake-view house:** fish directly from your bed / balcony ("a lake-view room, a bed on the roof, fishing straight from bed"). `[QQ]`

## G. Reward design (from the sharpest critiques — RF4 postmortems)

- A game's core is to **create and sustain pleasure** and satisfy needs unmet in real life; an "impossible, self-labeled hardcore" difficulty is just bad design. `[B]`
- **The alt-account tell (tu2471):** RF4 doesn't really pull *new* players — veterans keep rolling alt accounts to re-experience the early joy, because the game caps fun and only offers "start over" as a way to feel it again. The lesson: don't stretch playtime by delaying fun; deliver the fun up front and keep it coming. `[B]`
- **RF4 flaw 1 — server-wide trophy drops:** trophies spawn for all online players at once, so some get repeats and others never get one. Better: **guarantee a trophy once a player has caught enough** — effort should always pay off. `[B]`
- **RF4 flaw 2 — session decay:** the catch rate drops the longer you play in one session, as if the fish "clock off." Fish are NPCs / a boss loot table — don't make them go off-shift. `[B]`
- **The rare-fish horror story (是啊康啊):** a player spent **1,800 real hours** chasing an adult koi in RF4 and never landed one — always "just short of adult weight." Combined with rampant cheaters (multiples of a normal player's playtime), this is the exact anti-pattern to avoid: rare/colored fish (albino, koi) should be a reachable goal, not a slot machine. `[B]`
- **Trading limits (1爱做的欢喜少年):** if you add equipment/fish trading, cap it — especially high-tier gear — or newbies who can't clear the early game just quit. `[B]`

## H. Scope cautions (meta-feedback — take seriously)

- **Don't try to do everything at once.** Strong, repeated worry that chasing every suggestion yields many shallow, rough systems — "a hodgepodge game can't attract players; with limited resources, too many elements makes each one mediocre." Nail the core (building) and polish fishing into ONE solid pillar; ship extra ideas later. `[B][QQ]`
- **Push non-core content to the Steam Workshop / mods** — let the community grow content itself. Matches Artem's own stated plan: fishing is added as a NEW hook to attract players; extras and fish variety go to the Workshop. `[B][QQ]`
- **Fishing is a *relaxing* mini-activity, not a separate DLC (Homespace's own stance in-thread):** "you built your house, now walk over and fish for a bit, watching the sunset over your home." It shouldn't overshadow the core — it should make the world feel more alive. `[B]`
- Open questions players keep asking: is fishing weather-dependent? single-player or multiplayer/co-op? Add a **hunger/satiety system** so cooked fish is eaten because you're hungry (not just for stamina or trade). `[B]`

## I. Adjacent life-loop the pond ties into (江尚寒's mini design doc)

Not strictly fishing, but the community pictures the pond as one node in a whole cozy life-loop, so it's worth recording here:

- Don't only grow edible crops — also plant **flowers** around the house (wildflowers that need little upkeep); collect and arrange them into **bouquets** for the home. `[B]`
- Make cooking indirect: place a **well / pond / waterfall / spring** to gather water and salt for recipes. `[B]`
- The **pond** is for fishing; beside it you can plant trees or raise **silkworms** (a mulberry-dyke fish-pond). `[B]`
- **Fireflies** in the vegetable field at night. `[B]`
- Advanced cooking = combining multiple plants into **spices** (e.g. curry), so farming isn't monotonous. `[B]`
- A light **player trade system** with fixed, system-set prices (submit an order to buy from others) for items you can't get yet. `[B]`

---

## Reference games the community told us to study

| Game | Why it was named |
|---|---|
| **Russian Fishing 4** | Benchmark for feel — copy the physics & reeling feel, fix the hardcore grind, server-wide drops and session decay |
| **theHunter: Call of the Wild** | Quality bar; rare variants (albino / colored) |
| **Red Dead Redemption 2** | Fishing feel to match |
| **Zelda: Ocarina of Time** | Fishing minigame with real operation & feel |
| **Animal Crossing** | Fish catalog / picture-book |
| **Ys series** | Fishing done well as a light side-minigame |
| **Once Human** | Fishing + specimen wall; also structural load/collapse mechanic |
| **Yihuan (Chinese open-world game)** | Hang your catch as a visible trophy |
| **Behind Glass** | Custom aquarium / aquascaping |
| **Fishing Planet-style sims** | Compared against as a bar to beat |

---

*Sources: Bilibili video BV19NTc6VEfg (103 top comments + 179 replies) + Homespace QQ groups. Compiled for the dev team, 2026-07-07.*
