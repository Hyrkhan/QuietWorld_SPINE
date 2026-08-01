# Items, Mobs & Zone Art Direction — *Crown of the Hollow Reign*

Date: 051926
Setting: post-Long-Quiet, Quiet Year 312. Player faction: **the Verge**.
Lore canon: `docs/051726/LORE.md` and `LORE_FOR_KIDS.md`. World layout: `docs/051726/WORLD_MAP_ALPHA.md`.

> Supersedes any earlier item/zone docs that referenced "Hoppers" — that lore branch was wrong and is abandoned.

---

## Design Philosophy

Three rules:

1. **Salvage economy.** Nothing is *made.* Every weapon, every coin, every shred of armor is **recovered** from a ruin, **scavenged** from a corpse, or **forged in Stannar from Heleth alloys nobody fully understands.** Items have history. They are old.
2. **Five-tier faction palette.** Items belong to one of five origin schools — Verge issue, Imperial Vaelthar relics, Heleth artifacts, Silent Ord penitent gear, Brass-House commerce. Each looks visually distinct.
3. **Ragnarok-style biomes.** Each zone has **3–5 mob types at similar tier**. Players orient by ecosystem ("the lake area"), not by mob name.

## Three Style Prefixes for Nano Banana — Bright Cartoon MMO Direction

**Tone clarification:** The lore (`LORE.md`) describes a post-cataclysmic world with grim themes — but the **render is bright cartoon MMO**, not dark/grim. The contrast between "this NPC's family died in the Long Quiet" and "she's drawn as a smiling chibi merchant" is a feature, not a bug. See: Cult of the Lamb, MapleStory, Tree of Savior, Trove, Castle Cats, Cookie Run Kingdom — all combine heavy lore with bright, friendly art.

### A) ITEM ICON PREFIX *(use for everything in Part 1 — weapons, consumables, materials, equipment)*

> *"Vibrant chibi mobile MMO inventory icon. Bright saturated cartoon color palette — full colorful, never muted or dusty. Chunky cute proportions, soft round shapes, no sharp points or thin slender forms. Thin clean outlines in a slightly darker version of the fill color (not pure black, never harsh). Two to four flat colors per item with one bright soft highlight, no complex shading or gradients. Items occupy 60–70 percent of the square frame with breathing room. Cheerful, friendly, approachable cartoon feel — items look fun to hold even if their subject is sad in lore. Transparent background, no border, no card frame, no drop shadow, no inventory cell behind the item. Square 1:1 aspect ratio. Style references: Layer Lab Minimal Game Light icons, Castle Cats UI, Cookie Run Kingdom items, Soul Knight inventory, Pokemon item icons, mobile cartoon RPG inventory art, modern colorful idle game UI."*

**Item negative prompt:**
> *"No muted palette, no dusty earthy colors, no dark grim look, no painterly oil painting, no realistic shading, no realistic proportions, no slender long blades, no detailed engravings, no gradients, no photorealism, no pure black hard outlines, no harsh pixel art, no text, no UI border, no inventory cell behind the item, no drop shadow."*

### B) MOB / CREATURE PREFIX *(use for all 1:1 mob prompts in Part 2)*

> *"Vibrant chibi cartoon creature illustration, bright saturated color palette. Big expressive cute eyes, simple chunky toy-like body proportions, soft round forms with no sharp anatomy. Thin clean outlines in darker fill colors (not pure black). Two to four flat colors per creature with one or two soft highlights, no realistic shading, no painterly brushwork, no muted palette. Friendly, expressive, slightly comic feel — creatures read as adorable miniatures regardless of how scary their lore says they are. The cuteness IS the design — players should want to befriend the monsters before they have to fight them. Plain neutral background, side or 3/4 view, clean cutout. Square 1:1 aspect ratio. Style references: Pokemon (modern), Cookie Run Kingdom characters, Cult of the Lamb followers, Slime Rancher slimes, Castle Cats companions, Layer Lab chibi mob designs."*

### C) ZONE / ENVIRONMENT PREFIX *(use for all 16:9 zone prompts in Part 2)*

> *"Stylized top-down 3/4 isometric environmental view in vibrant cartoon mobile MMO style. Bright saturated color palette — lush emerald greens, bright sky blues, warm sunny yellows, soft creamy stone, vivid colorful foliage. Cheerful and inviting atmosphere even for ruined or dangerous places — ruins are charming and overgrown, not grimdark; dead engines glow with friendly bright magic-blue not sickly cold blue. Soft hand-painted lighting with clear shapes, no harsh shadows, no muted dustiness, no dark grim mood. Cute stylized props: rounded boulders, fluffy painterly trees, glossy water, big readable architecture. No characters, no UI elements, no text. 16:9 aspect ratio. Style references: Ni no Kuni 2 environments, Genshin Impact concept art, Pokemon Sword/Shield route paintings, Cozy Grove, Layer Lab Minimal Game Light backgrounds, modern cozy MMO map art."*

**Mob/Zone negative prompt:**
> *"No muted palette, no dusty earthy colors, no dark grim Berserk style, no Souls-series atmosphere, no painterly oil painting, no realistic textures, no photorealism, no harsh shadows, no UI, no text, no health bars, no watermarks, no signature, no characters in zone shots."*

> **Important:** every per-zone and per-mob content prompt in Part 2 was originally written in a darker melancholy register. **Some content prompts still mention "muted palette" or "cool sickly green" or "twilight" — ignore those palette words.** Render everything in the bright cartoon style from the prefixes. The lore details (Heleth ruins, stillfire glow, broken bell motifs, Silent Ord penitents) all stay — they just look adorable instead of grim.

## Tier Color Reference

Must match `data/itemTiers.ts`.

| Tier | Letter | Color | Drop weight |
|---|---|---|---|
| 0 | F | gray (#AAAAAA) | very common |
| 1 | E | white (#E6E6E6) | common |
| 2 | D | green (#78DC78) | uncommon |
| 3 | C | blue (#78AAF0) | rare |
| 4 | B | purple (#C882F0) | very rare |
| 5 | A | red (#F06E6E) | epic |
| 6 | S | gold (#FFD23C) | legendary (boss-rare) |
| 7 | S+ | pink-magenta (#FF82DC) | mythic / lore-locked |

## Item Origin Schools (visual identity)

| School | Look | Heraldry | Typical tier band |
|---|---|---|---|
| **Verge issue** | Brown leather, dull bronze, simple, well-maintained, modest stamp of a cracked-bell-under-crown | crown over cracked black bell | F – C |
| **Imperial Vaelthar relics** | Ornate bronze, faded gilt, crown-and-bell motifs, often cracked or singed, sometimes dimly humming | crown over a single black bell, mid-toll | B – A |
| **Heleth-forged** | Pale alien geometry, indestructible faceted shards, faintly glowing stillfire-blue seams, no recognizable handle/grip | none — Heleth used no heraldry | S – S+ |
| **Silent Ord penitent** | Heavy raw iron, deliberately crude, black-flame brand, hand-stitched white linen wraps | black flame over white linen | D – A |
| **Brass-House commerce** | Stannar forge-stamp, three-ring mark, more polished than Verge but plainer than Imperial | three iron rings interlinked | E – A |

---

# PART 1 — ITEMS

## 1A. Weapons (1000–1999)

### Verge issue (F – C tier)

| ID | Name | Tier | Lv | In-fiction description | Nano Banana prompt |
|---|---|---|---:|---|---|
| 1001 | **Verge Field Mace** | F | 1 | Standard issue Verge mace. Bronze head over an oak haft. Stamped under the head with a tiny cracked-bell-under-crown. New recruits are issued three of these in their first year because they keep breaking them on Husk-Crab shells. | *A short oak-hafted bronze mace, head modestly engraved with a cracked-bell-under-crown stamp, slightly chipped, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, transparent background.* |
| 1002 | **Verge Shortbow** | F | 1 | Yew shortbow with a single brass nock. Cheap to issue. Cheap to replace. The string is the only part the Verge expects you to maintain. | *A simple unstrung yew shortbow with brass nocks, leather hand-wrap, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 1003 | **Verge Sidearm** | F | 1 | Short straight sword, bronze blade, leather grip. Sergeant Halloway calls it "the convince-em." The Reliquary calls it "the stab-it." | *A short straight sword with bronze blade and leather-bound grip, slightly nicked, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 1004 | **Quieting Hammer** | D | 8 | Square iron head wrapped in copper-wire and sealed with chord-sand. Forged specifically for Verge Quieting specialists — the wire grounds the stillfire shock when striking a Stilled core. | *A square iron hammerhead wrapped tightly in copper wire with faint pale-blue motes leaking out, leather-bound oak haft, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 1005 | **Bell-Knight's Spear** | C | 15 | Long polearm with a leaf-shaped bronze head and a small clapper-bell mounted at the joint. Rings on impact. Bell-Knights say it warns the Stilled that something honest is coming. | *A long ceremonial spear with leaf-shaped bronze head, a small bronze bell mounted at the haft-joint, oak shaft, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, slight bronze gleam.* |
| 1006 | **Tolling Longsword** | C | 18 | Issued to Bell branch operators after their first ruin-recovery. The fuller is engraved with the names of the seven who founded the Bell. | *A one-handed longsword with bronze pommel and crossguard, fuller engraved with tiny illegible names, leather grip, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |

### Imperial Vaelthar relics (B – A tier, looted from ruins)

| ID | Name | Tier | Lv | In-fiction description | Nano Banana prompt |
|---|---|---|---:|---|---|
| 1010 | **Khelior-Pattern Sabre** | B | 18 | A curved cavalry sword from the imperial battle-hound corps. Bronze blade with a gilt fuller and a hound-head pommel. The grip still smells faintly of horse-sweat after three hundred years. | *A curved bronze cavalry sabre with gilt-edged fuller and a small bronze hound-head pommel, slightly verdigrised, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 1011 | **Chord-Warden's Focus-Wand** | A | 22 | A short slender bronze wand topped with a chord-cell. Drawn fully charged from a Wayward Knight's belt. Hums when held by anyone with INT above 30. | *A short ornate bronze wand with a small pale-blue glowing crystal capping the tip, faint geometry runes etched along the shaft, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, soft inner glow.* |
| 1012 | **Sister-Spire Glaive** | A | 25 | Long polearm carried by orbital-station marines before the Long Quiet. Its head is forged from Sister-Spire fragment metal — alloy unobtainable since the spires fell. | *A long polearm with an elegant blade made of pale silvery alien-alloy metal, ornate bronze haft, faint geometric etchings, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, cool light.* |

### Heleth-forged (S+ tier, mythic)

| ID | Name | Tier | Lv | In-fiction description | Nano Banana prompt |
|---|---|---|---:|---|---|
| 1020 | **Held-Note Edge** | S | 30 | A Heleth blade. Translucent. Faceted like a piece of geometry rather than something forged. Cuts what it is named at — and only what it is named at — but the Verge has lost the cant by which to name. | *A translucent crystalline sword that looks more like a geometric construct than a forged weapon, faintly glowing pale-blue seams, hilt formed of woven pale light, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, ethereal.* |
| 1021 | **Resonance Lance** | S | 35 | A two-prong Heleth lance that focuses stillfire into a directed beam. The pitch of the beam shifts depending on what the wielder is thinking about. Bell-Knight Halloway forbids speaking aloud while one is drawn. | *A two-pronged tuning-fork-shaped polearm of polished pale silvery alloy, with visible sonic ripples in the air between the prongs, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, with a small luminous highlight accent.* |
| 1022 | **The Last Tolling** | S+ | — | Mira Velour's blade. Bronze-edged, but the edge is wrapped in a single fiber of stillfire that hums when blood is near. Held by the standing Bell-Warden. **Not obtainable.** Listed here for completeness because some quest text references it. | *A one-handed straight sword of dark bronze, the edge faintly glowing pale-blue with a thread of stillfire, ornate ancient grip, the air around it slightly distorted, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |

### Silent Ord penitent (B – A tier)

| ID | Name | Tier | Lv | In-fiction description | Nano Banana prompt |
|---|---|---|---:|---|---|
| 1030 | **Penitent's Iron Maul** | B | 18 | A two-handed iron maul, deliberately crude, branded with the Silent Ord's black flame. Heavy in a way that suggests it was designed not just to hit, but to be carried as a burden. | *A two-handed iron maul with rough crude finish, a black-flame brand seared into one face, leather strap with white linen wraps on the haft, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 1031 | **Iron-Atonement Greataxe** | A | 25 | Two-handed greataxe taken from a fallen Silent-Brute champion. The head is forged in one piece with the haft — a Silent Ord ritual choice meaning "this weapon has no parts to fail; only the bearer fails." | *A two-handed iron greataxe forged as a single piece with the haft, no joints, black-flame brand on the head, white linen wraps stained with dust, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 1032 | **Black-Flame Censer** | A | 28 | A long-chained iron censer used by the Silent Ord's high priests. Burns confiscated chord-sand. Hated by Stilled. Painful to carry for any operator with INT above 25. | *A long-chained iron censer with a hinged dome, faint black flame visible inside through the latticework, chain ending in a leather-wrapped handle, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, with a tiny soft black-flame glow accent.* |

### Stilled-touched (D – B tier, cursed)

| ID | Name | Tier | Lv | In-fiction description | Nano Banana prompt |
|---|---|---|---:|---|---|
| 1040 | **Coolant Whip** | D | 9 | A length of Engine-Slime jelly drawn and braided into a whip. Holds itself together by some quiet thinking. Strikes leave a numbing residue. | *A whip made of coiled translucent blue-green semi-rigid slime substance, with a leather-wrapped handle, faint inner motes of light, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 1041 | **Wayward Pattern Sword** | B | 17 | Recovered from a Wayward Knight who had been standing at attention for two hundred years. Still in formation guard-position when found. The blade remembers patrol drills and twitches slightly while you sleep. | *A bronze longsword with ornate Imperial Vaelthar crossguard, slight residual pale-blue glow at the edge, bronze pommel shaped like a closed bell, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, slight unease.* |
| 1042 | **Tongue-Lash** | B | 21 | The preserved tongue of a Silent-Brute, oiled and braided onto an iron handle. Strikes faster than expected. Unsettling to swing. Most Verge operators refuse to carry one. | *A long whip with a braided sinewy pale-pink tongue tail, iron-wrapped handle with black wax seal, slightly glossy and unsettling, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |

## 1B. Consumables (2000–2999)

| ID | Name | Tier | Effect | In-fiction description | Nano Banana prompt |
|---|---|---|---|---|---|
| 2001 | **Verge Field Bread** | F | +30 SP | Dense flatbread baked at the Tolling Keep's kitchens. Travels a week in a pack. Tastes like a wet sock by then. | *A round dense flatbread loaf with a slightly burnt crust on a folded cloth, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2002 | **Reliquary Tonic** | F | +50 HP | A small clay flask of herbal water mixed with a pinch of chord-sand. Standard issue. Tastes faintly of iron and damp stone. | *A small clay flask with a cork stopper containing pale-amber liquid with faint sparkles of pale-blue suspended in it, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2003 | **Crab-Chitin Crisp** | F | +40 HP | Husk-Crab shell crisped in oil, salted. Cheap, ubiquitous around the Verge mess hall. The trace chord-residue gives a slight warm feeling in the chest. | *A small wooden plate with several crispy salted golden-brown crab shell pieces, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2010 | **Cell-Powered Restorative** | D | +120 HP over 10s | A flask with a tiny chord-cell soldered into the cork. Twist the cork to discharge the cell into the contents. Single-use; the cell is consumed. | *A glass flask with a brass-collared cork holding a small glowing pale-blue crystal, the liquid inside slightly luminous, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2011 | **Chord-Sand Vial** | D | +60 SP | A small bronze tube of microscopic chord-sand. Snuffed once per use. Reliquary scholars carry several. | *A small bronze tube with a removable cap, holding visible pale-blue glowing dust, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2012 | **Bell-Cantor's Anointing Oil** | C | Full HP | Distilled by Bell-Cantors at the Tolling Keep. The recipe is held by a single living person. The oil smells like the cathedral at twilight. | *An elegant ornate glass bottle with bronze bell-shaped cap holding luminous pale-amber oil with motes of pale-blue light, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, soft glow.* |
| 2020 | **Chord-Sand Smoke Pellet** | E | Blind aoe | A small wax pellet packed with chord-sand. Crush to release a cloud of pale-blue smoke. Stilled flinch from it; Silent Ord penitents are unaffected. | *A small dark waxed pellet with a faint pale-blue inner glow, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2021 | **Resonance Tuner** | D | +10% atk 30s | A small bronze tuning fork etched with a Reliquary glyph. Strike against any solid object to attune your nearby gear. Single use; the etching fades. | *A small bronze tuning fork with a single etched geometric symbol on the prong, slight pale-blue residual light, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2030 | **Quieting Salve** | C | Cures Stilled-touched debuff | Salve of chord-sand and burnt linen, applied to a wound that has touched a Stilled. The Verge issues two per operator per ruin. | *A small clay jar with a wooden lid containing pale-gray salve with pale-blue motes, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2031 | **Sealed Letter of Recall** | C | Warp to last savepoint | A folded letter sealed with old Reliquary wax. Burning it opens a Heleth fold. Bell-Knight Halloway insists the folds are *somewhere* — not just teleport, but a place you pass through. | *A folded yellowed parchment letter sealed with a dark-blue wax stamp showing a closed bell, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2040 | **Silent Ord Penitent Ration** | E | +20% move speed 30s | A dark wafer pressed with a tiny black-flame brand. Silent Ord initiates carry one per knee. Bitter. Filling. Confiscated bundles can be bought illegally in Stannar. | *A small dark dense waxed wafer with a black-flame brand seared into one side, wrapped in white linen, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2041 | **Brass-House Cordial** | D | +50% haggle 5min | A small Stannar-glass bottle of distilled fruit cordial with a Brass-House three-ring stamp. Sold by lord-forgemasters to traveling Verge operators at a markup. | *A small ornate glass bottle with three-ring brass collar, holding amber liquid, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2050 | **Common Chord-Shard** | C | Refine fodder | A milky polished fragment of Heleth glass. Verge alchemists use it as refining catalyst. Common in Reliquary stores. | *A small polished translucent milky-white crystalline fragment, faintly faceted, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 2051 | **Pristine Chord-Shard** | A | Refine fodder, higher success | A fully transparent Heleth-glass shard with a clean geometric facet. Reliquary scholars say it "remembers" the original chord. | *A faceted clear pale-blue gemstone glowing with faint inner light, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, light refraction.* |

## 1C. Materials (3000–3999)

Drop loot. Sells well to Verge artificers + Brass-House factors.

| ID | Name | Tier | Source | Description | Nano Banana prompt |
|---|---|---|---|---|---|
| 3001 | **Husk-Crab Chitin** | F | Husk-Crab | Cream-colored shell with trace chord-residue. Used for low-tier armor scales. | *A curved cream-colored insect/crustacean shell fragment with subtle pink ridges and faint pale-blue chord-residue speckles, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 3002 | **Polish-Roach Brush** | F | Polish-Roach | The brush-bristled underside of a cathedral-floor cleaning drone. Imperial servitor-tech. | *A small flat dark chitinous plate with rows of stiff brass-tipped bristles on the underside, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 3003 | **Lantern-Moth Wing** | F | Lantern-Moth | A papery wing that glows faintly pale-blue when fresh. Briefly. | *A teardrop-shaped translucent moth wing with pale-blue luminescent veins, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, faint glow.* |
| 3010 | **Engine-Slime Core** | E | Engine-Slime | A glassy bead found at the heart of a slain Engine-Slime. Hums faintly. Worth real coin to Reliquary scholars. | *A small spherical glass orb with swirling blue-green energy inside, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 3011 | **Coolant Residue** | E | Coolant-Drip | A small vial of viscous blue-green coolant gel from Heleth engines. | *A small glass vial of viscous translucent blue-green liquid, cork stopper, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 3012 | **Geometry-Beetle Carapace** | E | Geometry-Beetle | A chitinous shell etched with raised Heleth glyphs. The Reliquary buys all you can find. | *A flat oval beetle shell with raised geometric Heleth glyph patterns embossed across its surface, faint pale-blue inner glow, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 3020 | **Iron-Hound Plate-Scale** | D | Iron-Hound | Adaptive armor fragment, black with rust streaks. Brass-Houses pay for whole sets. | *A curved overlapping bronze-black metallic armor scale with rust-orange streaks, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 3021 | **Sentry-Wing Lens** | D | Sentry-Wing | A polished bronze lens from a Heleth aerial sentry. Still focuses light when held to the sun. | *A circular polished bronze lens with engraved iris-pattern around the edge, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, slight light refraction.* |
| 3030 | **Wayward Bell-Shard** | C | Wayward Knight | A fragment of the broken bell every Wayward Knight wears. Some still ring softly when pressed to the ear. | *A jagged bronze bell-fragment shard with verdigris patina, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 3031 | **Reliquary Glyph-Tile** | C | Reliquary Watcher | A square bronze plate inscribed with raised script no living scholar reads. Reliquary buys at standard rate. | *A square bronze plate with raised illegible geometric runes, slightly tarnished, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 3040 | **Penitent Iron Strip** | B | Silent-Brute | Strip of iron from a Silent-Brute's Atonement plating. Brass-Houses melt down for re-forging. The black-flame brand is removed in the process. | *A torn strip of beaten iron with rough black-flame brand on one face, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 3041 | **Black-Linen Scrap** | B | Reed-Stalker | Torn fragment of Silent Ord uniform linen, white but smoke-stained. Useful for stealth-related crafting in the Reliquary. | *A torn scrap of off-white linen cloth, ash-stained at one edge, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 3050 | **Heleth Glyph-Shard** | A | Ruin drops | A piece of indestructible Heleth glass etched with geometry no one understands. Always cool to the touch. | *A jagged shard of translucent pale-blue Heleth-glass with sharp geometric inner facets, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, slight internal sparkle.* |
| 3051 | **Raw Chord-Sand** | A | Boss drops | A small pouch of crystallized stillfire residue. Smells like wet stone and sleep. Reliquary scholars guard their stock jealously. | *A small open leather pouch with a pinch of luminous pale-blue crystalline powder spilling out, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, faint glow.* |
| 3060 | **Sister-Spire Fragment** | A | Eastern Forest (sealed-preview) | A piece of fallen orbital station alloy. Cool, light, indestructible. Forge-master Aimes pays heavily for any sample. | *A small jagged metallic fragment of pale silvery alloy with sharp clean edges, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 3061 | **Cold Moors Frost-Salt** | A | Cold Moors (sealed-preview) | Pale crystalline salt that forms only where chord-engines died cold. Cannot be synthesized. | *A small pile of pale silver-white crystalline salt crystals, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, cool light.* |

## 1D. Equipment (4000–4999)

### Headgear

| ID | Name | Tier | Lv | School | Description | Nano Banana prompt |
|---|---|---|---:|---|---|---|
| 4001 | **Verge Field Cap** | F | 1 | Verge | Brown leather cap stamped with the cracked-bell-under-crown. Issued at the Keep gate. | *A simple brown leather skull-cap with a small bronze emblem on the forehead — a cracked bell beneath a small crown, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4002 | **Reliquary Reading Hood** | E | 5 | Verge | Soft cloth hood worn by Reliquary scribes. Ink-stained inside the brim. | *A simple cloth hood, deep brown, with ink-stained linen lining visible at the brim, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4010 | **Bell-Cantor's Circlet** | C | 15 | Verge | A thin silver circlet hung with three tiny bells. Hums softly. Stilled flinch from it. | *A delicate silver circlet with three small dangling bronze bells, faint inner pale-blue glow, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, soft side-light.* |
| 4020 | **Bell-Knight Vergeguard Helm** | A | 22 | Verge | Full bronze helm with visor and a small clapper-bell mounted at the crown. Tolls when struck. | *A polished bronze knight helm with closed visor and a small bronze bell mounted at the top, slightly battle-scarred, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4030 | **Imperial Crown-Fragment** | S | 30 | Imperial | A bronze crown half — a single arc of Empress Theresia VII's coronation regalia. Looted from Vaelm-Lesser. The other half is unaccounted for. | *A jagged half of an ornate bronze crown, gilt fading, set with a single intact dark-blue stillfire gem, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, with a small luminous highlight accent.* |
| 4040 | **The Hollow Reign** | S+ | 50 | Imperial | The full ceremonial crown of Empress Theresia VII, reconstituted from both halves. Whoever wears it hears the held note again. **Boss-vault reward.** | *An ornate bronze crown set with a single large pale-blue stillfire gem, faint sonic ripples visible in the air around it, the air around the wearer slightly distorted, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, with a small luminous highlight accent.* |

### Body armor

| ID | Name | Tier | Lv | School | Description | Nano Banana prompt |
|---|---|---|---:|---|---|---|
| 4101 | **Vergeguard Tunic** | F | 1 | Verge | Quilted brown cotton tunic. Dyed the same color so the blood doesn't show. | *A quilted brown sleeveless cotton tunic with subtle stitching pattern, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4110 | **Field Ring-Mail** | D | 10 | Verge | Bronze ring-mail riveted to leather. Standard for Verge-Captains. | *A short-sleeved bronze ring-mail shirt with leather backing visible at the collar, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4120 | **Reliquary Robes** | C | 15 | Verge | Long deep-brown robes with chord-cell sockets sewn into the cuffs. Worn by the Reliquary branch's combat operators. | *Long deep-brown ankle-length robes with multiple small bronze-collared cell-sockets sewn into the wide cuffs, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4130 | **Iron Atonement Plate** | B | 18 | Silent Ord (looted) | Heavy iron plate. Taken from a Silent-Brute who didn't survive Atonement. The Ord considers wearing it a desecration. | *A heavy raw-iron chest cuirass with rough black-flame brand on the breast, white linen wraps stained brown, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4140 | **Bell-Knight Cuirass** | A | 25 | Verge | Burnished bronze breastplate engraved with the names of every Bell-Knight who fell sealing the first Falling Age. Reads like a prayer when polished. | *A polished bronze chest cuirass engraved with rows of tiny written names, slight verdigris in the engraved letters, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4150 | **Brass-House Trader's Coat** | D | 12 | Brass-House | A lined coat with three-ring brass clasps. Worn by Stannar merchants visiting Verge outposts. Gives a small haggle bonus. | *A long forest-green lined coat with three round brass clasps down the front, slightly travel-worn, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |

### Footgear

| ID | Name | Tier | Lv | School | Description | Nano Banana prompt |
|---|---|---|---:|---|---|---|
| 4201 | **Verge Cloth Boots** | F | 1 | Verge | Calf-high cloth boots with a leather sole. The Verge makes them in three sizes: too small, too large, and "report it back to the quartermaster." | *A pair of brown cloth calf-high boots with leather soles and simple ties, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4210 | **Marsh-Walker Soles** | E | 6 | Verge | Reed-woven sandals reinforced with leather. Don't sink in Crooked Lake mud. Smell terrible after a week. | *A pair of woven reed sandals with leather reinforcing straps, slightly wet-looking on the soles, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4220 | **Sealed Footgear** | B | 20 | Imperial | Bronze-toed boots taken from a Wayward Knight whose left boot still bears an intact Reliquary seal. The right boot does not. | *A pair of dark leather boots with polished bronze toe-caps, the left boot showing an intact dark wax seal, the right broken open, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |

### Garments (cloaks)

| ID | Name | Tier | Lv | School | Description | Nano Banana prompt |
|---|---|---|---:|---|---|---|
| 4301 | **Verge Field Cloak** | E | 5 | Verge | Brown wool cloak with the cracked-bell-under-crown stitched at the throat. Issued at the Tolling Keep gate to every operator on their first deployment. | *A brown wool hooded cloak with a small silver cracked-bell-and-crown clasp at the throat, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4310 | **Cold Moors Pelt** | A | 25 | Foraged | Pelt of a creature that lived only in the sealed Cold Moors. Smuggled through Iron Reach. Warm enough to sleep in snow. | *A heavy gray-brown fur cloak draped over an invisible figure, frost crystals faintly at the tips, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, cool light.* |

### Accessories

| ID | Name | Tier | Lv | School | Description | Nano Banana prompt |
|---|---|---|---:|---|---|---|
| 4401 | **Chord-Cell Pendant** | D | 8 | Verge | A leather cord with a small bronze-collared chord-cell. Glows pale-blue near a Stilled. The Reliquary issues one to every Quieting-branch operator. | *A small bronze-collared glowing pale-blue crystal pendant on a leather cord, faint inner glow, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4410 | **Bell-Ringer's Pin** | C | 12 | Verge | A small brass pin shaped like a stylized bell, awarded only to operators who have rung the Tolling Keep's chapel bell for a fallen comrade. | *A small ornate brass pin shaped like a stylized hanging bell with a single ring around it, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4420 | **Brass-House Trader's Ring** | B | 18 | Brass-House | A heavy bronze ring set with three smaller iron rings interlinked. Marks the bearer as a registered Stannar trader. Vendors give a small discount on sight. | *A heavy bronze ring set with three small interlinked iron rings on top, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |
| 4430 | **Heleth-Etched Bracer** | A | 25 | Heleth (looted) | A bronze bracer with raised Heleth glyphs that arrange themselves slightly differently each morning. Reliquary scholars are afraid of them. | *A polished bronze bracer with raised pale-blue glowing geometric glyph patterns, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1, soft glow.* |
| 4440 | **Mira's Locket** | S+ | — | Lore-locked | Bell-Warden Velour's personal locket. Contains a single Heleth glyph-shard. Listed for completeness — **not obtainable** in alpha. | *A small ornate silver locket on a fine chain, the cover engraved with a cracked bell, vibrant chibi mobile MMO icon, bright saturated cartoon colors, chunky cute proportions, 1:1.* |

## 1E. Crafting Recipes

The Verge does not *invent* — it **recovers and re-forges.** Every craftable
item in the alpha is built from materials looted in the field (mob drops, ruin
scrap, Heleth fragments) plus a small endrite fee. Crafting is **guaranteed**;
the scarcity lives in the materials, not in dice rolls. Refining (gem-stat
upgrades on equipped gear) is a separate system handled by `RefineSystem.ts`.

### Crafting NPCs

| NPC | Location | Specialty |
|---|---|---|
| **Reliquary Artificer Tenne Wrenwhistle** | E3 East Verge Outpost | All standard Verge / Imperial-salvage crafts |
| **Reliquary Scribe Allard** | C3 West Verge Outpost | Consumables, Heleth scroll-binding (Sealed Letters of Recall) |
| **Whisper-Vendor** | E1 Crooked Lake — hidden, unlocks via questline | Silent Ord taboo crafts (Penitent gear). The Verge tolerates this contact but does not endorse it. |
| **Stannar Forge-Master Bevorin** | (out-of-region, alpha-2) | Imperial-relic restoration. Listed for completeness. |

### What's craftable vs. drop-only

| Origin school | Craftable? | Notes |
|---|---|---|
| Verge issue (F – C) | ✅ Yes | Tenne sells the recipes openly |
| Imperial Vaelthar relics (B – A) | ❌ Drop-only | The Empire is dead; the recipes are lost |
| Heleth-forged (S – S+) | ❌ Drop-only | Cannot be made; they were *made by the Heleth* |
| Silent Ord penitent (B – A) | ⚠️ Yes (taboo) | Only via Whisper-Vendor, after questline |
| Brass-House commerce | ✅ Yes (at outpost) | Trader's Coat etc. |
| Stilled-touched (cursed) | ❌ Drop-only | Cannot be re-forged; the corruption is the *item* |

### Material → recipe summary

Each material has at least one craft use. This is the inverse table: when a
player picks up a drop, they can check what it builds.

| Material | Used in |
|---|---|
| **Husk-Crab Chitin** (3001) | Verge Field Mace, Verge Sidearm, Verge Field Cap, Vergeguard Tunic, Verge Cloth Boots, Verge Field Cloak |
| **Polish-Roach Brush** (3002) | Verge Field Mace, Verge Field Cap, Reliquary Tonic |
| **Lantern-Moth Wing** (3003) | Verge Sidearm, Reliquary Tonic, Verge Field Cloak, Reliquary Reading Hood |
| **Engine-Slime Core** (3010) | Quieting Hammer, Coolant Whip, Cell-Powered Restorative, Chord-Sand Vial, Chord-Cell Pendant |
| **Coolant Residue** (3011) | Coolant Whip, Marsh-Walker Soles, Quieting Hammer |
| **Geometry-Beetle Carapace** (3012) | Coolant Whip, Reliquary Robes |
| **Iron-Hound Plate-Scale** (3020) | Quieting Hammer, Field Ring-Mail, Brass-House Trader's Coat, Bell-Knight's Spear, Tolling Longsword, Reliquary Robes |
| **Sentry-Wing Lens** (3021) | Field Ring-Mail, Brass-House Trader's Coat |
| **Wayward Bell-Shard** (3030) | Bell-Knight's Spear, Tolling Longsword, Bell-Cantor's Circlet, Bell-Cantor's Anointing Oil |
| **Reliquary Glyph-Tile** (3031) | Bell-Knight's Spear, Bell-Cantor's Circlet, Reliquary Robes, Quieting Salve, Sealed Letter of Recall, Bell-Knight Cuirass, Heleth-Etched Bracer |
| **Penitent Iron Strip** (3040) | Penitent's Iron Maul, Iron Atonement Plate, Bell-Knight Cuirass |
| **Black-Linen Scrap** (3041) | Penitent's Iron Maul, Iron Atonement Plate |
| **Heleth Glyph-Shard** (3050) | Bell-Knight Cuirass, Heleth-Etched Bracer |
| **Raw Chord-Sand** (3051) | Bell-Cantor's Anointing Oil (advanced variant) |

### F-tier recipes (Tenne, West/East Outpost)

| Output | ID | Materials | Endrite | Notes |
|---|---:|---|---:|---|
| Verge Field Mace | 1001 | 3× Husk-Crab Chitin + 1× Polish-Roach Brush | 10 | Tutorial-tier weapon |
| Verge Shortbow | 1002 | 2× Lantern-Moth Wing + 1× Husk-Crab Chitin | 10 | |
| Verge Sidearm | 1003 | 4× Husk-Crab Chitin + 2× Lantern-Moth Wing | 15 | |
| Reliquary Tonic | 2002 | 1× Lantern-Moth Wing + 1× Polish-Roach Brush | 5 | Cheap heal staple |
| Crab-Chitin Crisp | 2003 | 2× Husk-Crab Chitin | 3 | Cooking — flavor over function |
| Verge Field Cap | 4001 | 2× Husk-Crab Chitin + 1× Polish-Roach Brush | 10 | |
| Vergeguard Tunic | 4101 | 4× Husk-Crab Chitin | 20 | |
| Verge Cloth Boots | 4201 | 3× Husk-Crab Chitin | 15 | |

### E-tier recipes

| Output | ID | Materials | Endrite |
|---|---:|---|---:|
| Reliquary Reading Hood | 4002 | 2× Lantern-Moth Wing + 1× Husk-Crab Chitin | 30 |
| Verge Field Cloak | 4301 | 2× Husk-Crab Chitin + 1× Lantern-Moth Wing | 40 |
| Marsh-Walker Soles | 4210 | 3× Coolant Residue + 2× Husk-Crab Chitin | 50 |
| Chord-Sand Smoke Pellet | 2020 | 1× Coolant Residue + 1× Common Chord-Shard | 25 |
| Tolling Brew | 2003 | 1× Geometry-Beetle Carapace + 5× Husk-Crab Chitin | 40 |
| Penitent Ration (counterfeit) | 2040 | 2× Black-Linen Scrap + 1× Polish-Roach Brush | 35 | (Tenne sells a non-taboo lookalike) |

### D-tier recipes

| Output | ID | Materials | Endrite |
|---|---:|---|---:|
| Quieting Hammer | 1004 | 5× Iron-Hound Plate-Scale + 2× Engine-Slime Core + 3× Coolant Residue | 200 |
| Coolant Whip | 1040 | 5× Coolant Residue + 1× Engine-Slime Core + 1× Geometry-Beetle Carapace | 150 |
| Cell-Powered Restorative | 2010 | 1× Engine-Slime Core + 1× Common Chord-Shard | 100 |
| Chord-Sand Vial | 2011 | 1× Engine-Slime Core + 1× Common Chord-Shard | 100 |
| Resonance Tuner | 2021 | 2× Engine-Slime Core + 1× Common Chord-Shard | 150 |
| Field Ring-Mail | 4110 | 8× Iron-Hound Plate-Scale + 2× Sentry-Wing Lens | 300 |
| Brass-House Trader's Coat | 4150 | 5× Iron-Hound Plate-Scale + 1× Sentry-Wing Lens | 250 |
| Chord-Cell Pendant | 4401 | 1× Engine-Slime Core + 1× Common Chord-Shard | 150 |

### C-tier recipes

| Output | ID | Materials | Endrite |
|---|---:|---|---:|
| Bell-Knight's Spear | 1005 | 6× Iron-Hound Plate-Scale + 2× Wayward Bell-Shard + 1× Reliquary Glyph-Tile | 600 |
| Tolling Longsword | 1006 | 4× Iron-Hound Plate-Scale + 3× Wayward Bell-Shard | 800 |
| Bell-Cantor's Anointing Oil | 2012 | 3× Wayward Bell-Shard + 1× Pristine Chord-Shard | 1000 |
| Quieting Salve | 2030 | 2× Reliquary Glyph-Tile + 1× Common Chord-Shard | 400 |
| Sealed Letter of Recall | 2031 | 1× Reliquary Glyph-Tile + 1× Pristine Chord-Shard | 800 |
| Reliquary Robes | 4120 | 5× Iron-Hound Plate-Scale + 2× Reliquary Glyph-Tile + 1× Common Chord-Shard | 700 |
| Bell-Cantor's Circlet | 4010 | 3× Wayward Bell-Shard + 1× Reliquary Glyph-Tile + 2× Common Chord-Shard | 900 |

### B-tier taboo recipes (Whisper-Vendor only, post-questline)

The Verge does not approve. Bell-Warden Vossward has publicly warned that
operators buying these will be questioned. Buy at your own risk.

| Output | ID | Materials | Endrite |
|---|---:|---|---:|
| Penitent's Iron Maul | 1030 | 8× Penitent Iron Strip + 2× Black-Linen Scrap | 3000 |
| Iron Atonement Plate | 4130 | 12× Penitent Iron Strip + 4× Black-Linen Scrap | 4000 |

### A-tier recipes (rare — endgame alpha)

| Output | ID | Materials | Endrite |
|---|---:|---|---:|
| Bell-Knight Cuirass | 4140 | 10× Penitent Iron Strip + 5× Reliquary Glyph-Tile + 2× Pristine Chord-Shard + 1× Heleth Glyph-Shard | 10,000 |
| Heleth-Etched Bracer | 4430 | 5× Reliquary Glyph-Tile + 3× Heleth Glyph-Shard + 1× Pristine Chord-Shard | 8,000 |

### Special: Chord-shard production

Both refining stones are simultaneously consumables, materials, AND recipes:

| Output | ID | Materials | Endrite | Notes |
|---|---:|---|---:|---|
| Common Chord-Shard | 2050 | 5× Engine-Slime Core | 100 | Common conversion |
| Pristine Chord-Shard | 2051 | 3× Common Chord-Shard + 1× Heleth Glyph-Shard | 1,500 | Concentration |

This gives players a way to **convert excess low-tier mats into refining
catalyst** late-game.

### Special: The Hollow Reign assembly (S+ endgame)

A unique once-per-player ritual at the Tolling Keep chapel. Not a Tenne craft —
performed at the **Bell-Warden's audience** after defeating Aurelyne.

| Output | ID | Materials | Endrite | Notes |
|---|---:|---|---:|---|
| The Hollow Reign (full crown) | 4040 | 2× Imperial Crown-Fragment + 1× Raw Chord-Sand + 1× Pristine Chord-Shard | — | Both Crown-Fragments must be from defeating Aurelyne and one of her sibling Hush-Magisters (alpha-2 content). Until alpha-2, the assembly recipe shows "missing component" |

### Salvage rules

To make unwanted drops useful, Tenne also offers a **salvage service**:

| Action | Returns |
|---|---|
| Salvage F-tier item | 50% of original mats (rounded down) |
| Salvage E-tier item | 50% of original mats |
| Salvage D-tier item | 40% of original mats |
| Salvage C-tier item | 30% of original mats |
| Salvage B-tier item | 25% of original mats |
| Salvage A-tier item | 20% of original mats — only ever salvage if you can't sell it |

**Cannot salvage:** Imperial relics, Heleth-forged, lore-locked items, currently-equipped items, items with refines (the refine gem is destroyed if you do).

### Crafting UI / message protocol

Add to `MMO-Server-Colyseus/src/types/index.ts`:

```ts
CRAFT_ITEM:      "craft",        // client → server: { recipeId }
CRAFT_RESPONSE:  "craftResp",    // server → client: { ok, itemId, errorReason? }
SALVAGE_ITEM:    "salvage",      // client → server: { inventorySlot }
SALVAGE_RESPONSE:"salvageResp",  // server → client: { ok, materials[], errorReason? }
LIST_RECIPES:    "recipes",      // client → server: { npcId }
RECIPES_RESPONSE:"recipesResp",  // server → client: { npcId, recipes[] }
```

Mirror in `coh/scripts/scr_messages.gml`:

```gml
#macro MSG_CRAFT_ITEM         "craft"
#macro MSG_CRAFT_RESPONSE     "craftResp"
#macro MSG_SALVAGE_ITEM       "salvage"
#macro MSG_SALVAGE_RESPONSE   "salvageResp"
#macro MSG_LIST_RECIPES       "recipes"
#macro MSG_RECIPES_RESPONSE   "recipesResp"
```

Server-side validates:
1. Player has all required materials.
2. Player has enough endrite.
3. Player is within interaction range of the requested NPC (`Tenne` or `Whisper-Vendor`).
4. Recipe is unlocked (Whisper-Vendor recipes require questline flag).

If all pass: deduct materials + endrite, push output item into inventory,
respond `CRAFT_RESPONSE { ok: true, itemId }`. If any fail: respond
`{ ok: false, errorReason: "Not enough Iron-Hound Plate-Scale" }` etc.

### Where the recipe table lives

Server canon: a new file **`MMO-Server-Colyseus/src/data/recipes.ts`** —
single source of truth. Client mirrors only **recipe names + material name
display strings** in `coh/scripts/scr_constants.gml`. The recipe *contents*
(material IDs, counts, output ID, cost) live on the server.

---

# PART 2 — ZONES (3–5 mobs each)

This replaces the "one mob per cell" `ROOM_SPAWNS` in `WORLD_MAP_ALPHA.md`. Each open zone now has an **ecosystem of 3–5 same-tier mobs**.

## D3 — Tolling Vale (safe hub, level 1+ entry)

The valley around the Tolling Keep. Spawn point for all new operators. NPC vendors, the Verge bell-tower, the keep gates.

- **Mobs:** none. Strictly safe.
- **NPCs visible:** Verge sentries, Reliquary scribes, a few off-duty Bell-Knights, a Brass-House trade-tent at the south gate.

**Nano Banana zone prompt (16:9):**
> *Top-down 3/4 isometric view of a Verge monastery courtyard at golden hour, centered on a tall bronze bell-tower with a single great bell visible, cobblestone paths radiating to four arched gateways at the cardinal directions, weathered stone walls with banners showing a cracked black bell beneath a crown, Verge sentries in bronze ring-mail visible at posts, scattered Heleth ruin stones repurposed as benches, lush worn grass between stones, soft warm afternoon light with pale-blue stillfire glow leaking from sealed cracks in the older stones, no UI elements, vibrant cartoon mobile MMO environment, bright saturated colors, lush cheerful palette, 16:9.*

## D4 — Crab-Meadow (Level 1, starter)

Old cathedral plaza, now overgrown. Imperial servitor drones still wander what they used to clean. Friendly until kicked.

| Mob | Lv | Behavior | Drops |
|---|---:|---|---|
| **Husk-Crab** (template 0) | 1 | Passive until hit | Husk-Crab Chitin |
| **Polish-Roach** (new) | 1 | Wanders fixed loops, flees on attack | Polish-Roach Brush, F-tier consumables |
| **Lantern-Moth** (new) | 2 | Slow flight, pale-blue glow draws Stilled | Lantern-Moth Wing |
| **Resonance-Vole** (new) | 2 | Natural rodent drawn to stillfire residue, flees | F-tier weapons (rare) |
| **Dustling** (new) | 3 | Stationary servitor cloud — sweeps an aoe of dust | Polish-Roach Brush, F-tier consumables |

**Zone Nano Banana prompt (16:9):**
> *Top-down 3/4 isometric view of an ancient sunlit cathedral plaza, the cathedral itself reduced to its outer walls and a partial dome on one side, pale grass and orange wildflowers growing through cracked flagstones, scattered low Heleth ruin stones with faintly glowing pale-blue cracks, broken bronze plaques bearing illegible imperial script, sense of "this used to be sacred," warm midday light with pockets of pale-blue stillfire glow, no UI elements, vibrant cartoon mobile MMO environment, bright saturated colors, lush cheerful palette, 16:9.*

**Mob Nano Banana prompts (1:1):**

- **Husk-Crab:** *A small bipedal crab-like servitor drone, cream-colored bronze chitin plating, two oversized brass-tipped claws, small pale-blue stillfire eye-lights, slightly worn polishing brush extending from underside, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Polish-Roach:** *A small flat dark-bronze beetle-shaped cleaning drone, brass-tipped scrubbing bristles on its underside visible through the gap between body and ground, faint pale-blue stillfire glow at joints, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Lantern-Moth:** *A medium fantasy moth the size of a cat with translucent papery pale-blue glowing wings, fed by stillfire residue, hovering slowly, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Resonance-Vole:** *A small mossy gray-brown rodent with oversized ears and large frightened pale-blue eyes, natural creature affected by stillfire exposure, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Dustling:** *A small stationary servitor — a low broom-headed bronze drone, half-collapsed, emitting a slow expanding cloud of pale dust around itself, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*

## C4 / E4 — Southwest & Southeast Meadows (Level 1–3, overflow)

Same mob pool as D4 with different distribution. Use when D4 is crowded.

**C4 variant:** *Same plaza ruin aesthetic but with a partial collapsed colonnade leading west toward sealed Western Cliffs, more sand-blown flagstones.*

**E4 variant:** *Same plaza ruin aesthetic but with a small reed-bordered stream cutting through, leading east toward the forest. A single broken Heleth archway in the middle distance.*

## F3 — Engine-Slime Forest (Level 4–6)

Old Heleth coolant lines burst here three centuries ago. The forest grew up around the leak. Now the gel thinks, and the trees have learned to listen.

| Mob | Lv | Behavior | Drops |
|---|---:|---|---|
| **Engine-Slime** (template 1) | 5 | Aggressive bounce-toward | Engine-Slime Core, E-tier consumables |
| **Coolant-Drip** (new) | 4 | Small, fast, drips from canopy | Coolant Residue |
| **Loom-Fly** (new) | 5 | Cleaned imperial looming machines — now drawn to stillfire | Geometry-Beetle Carapace (rare) |
| **Geometry-Beetle** (new) | 5 | Walks in geometric patterns; ambushes if its line is broken | Geometry-Beetle Carapace |
| **Murmur-Vine** (new) | 6 | Stationary plant, ranged stillfire-laced thorn | Coolant Residue, F-tier weapons |

**Zone Nano Banana prompt (16:9):**
> *Top-down 3/4 isometric view of a dense fantasy forest in late afternoon, the trees old and moss-covered with thick exposed roots, pools of glowing pale-blue stillfire-coolant on the forest floor, oversized mushrooms in turquoise and pale-green, broken Heleth coolant pipes visible jutting from the moss, sense of vibrant decay, cool palette with pockets of warm dappled sun, no UI elements, vibrant cartoon mobile MMO environment, bright saturated colors, lush cheerful palette, 16:9.*

**Mob Nano Banana prompts (1:1):**

- **Engine-Slime:** *A medium translucent blue-green slime creature with a small glassy core glowing inside its body, slight metallic Heleth-pattern sheen on the surface, hints of dissolved bronze gears half-floating within, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Coolant-Drip:** *A small translucent pale-blue slime drop hanging mid-fall, tiny tendrils, faint inner light, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Loom-Fly:** *A medium fantasy moth with translucent gear-like wings of pale-bronze, slightly mechanical body, intricate Heleth weaving patterns on the thorax, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Geometry-Beetle:** *A medium beetle with a flat oval shell etched with raised pale-blue glowing Heleth geometric patterns, calm methodical posture, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Murmur-Vine:** *A stationary plant-creature with a vine-knot torso atop thick mossy roots, several thorn-tipped vines coiled around it, faint pale-blue motes drifting upward, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*

## B3 — Iron Hills (Level 9–11)

Old Khelior-pattern training grounds for the Empire's battle-hound corps. Hounds still patrol the ranges. Natural creatures have moved in around them.

| Mob | Lv | Behavior | Drops |
|---|---:|---|---|
| **Iron-Hound** (template 2) | 10 | Pack hunter, fast lunge | Iron-Hound Plate-Scale, D-tier weapons |
| **Scent-Vole** (new) | 9 | Small auxiliary tracker construct, runs in arcs | Polish-Roach Brush |
| **Sentry-Wing** (new) | 10 | Aerial Heleth recon drone, dives | Sentry-Wing Lens |
| **Iron-Larva** (new) | 10 | Malfunctioning battle-hound puppy that never matured | Iron-Hound Plate-Scale (rare) |
| **Quarry-Mole** (new) | 11 | Natural mole that fed on Heleth scrap iron, now metal-skinned | Iron-Hound Plate-Scale |

**Zone Nano Banana prompt (16:9):**
> *Top-down 3/4 isometric view of a cheerful rugged hill country at sunny afternoon, exposed iron-veined warm-gray rock faces with vibrant moss patches, an abandoned imperial quarry pit visible in the middle distance with broken bronze cutting-machinery half-buried among bright grass, faded Vaelthar Imperial banners still hanging from a collapsed watchtower, warm orange dirt paths winding between low hills, vibrant green hill palette with warm sunny highlights, no UI elements, vibrant cartoon mobile MMO environment, bright saturated colors, lush cheerful palette, 16:9.*

**Mob Nano Banana prompts (1:1):**

- **Iron-Hound:** *A medium quadrupedal Heleth-construct hound with black-metallic adaptive armor plating like overlapping scales, glowing pale-blue eyes set in a featureless metal face, lean muscular build, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Scent-Vole:** *A small four-legged Heleth construct shaped like a rodent, brass plates and exposed gears, single forward-mounted pale-blue eye-lens, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Sentry-Wing:** *A medium aerial construct shaped like a metal owl, brass wings with hinged feathers, single large pale-blue eye-lens in the chest, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Iron-Larva:** *A small malformed battle-hound puppy construct, mismatched armor plates, one eye-lens cracked, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Quarry-Mole:** *A heavy molelike creature with shovel-claws and bronze flecks visible in its dark fur from years of eating Heleth scrap, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*

## D2 — The Wayside (Level 11–13)

The old imperial road connecting the Tolling Vale to Vaelm-Lesser. Patrols still walk it. They don't know who they're patrolling for.

| Mob | Lv | Behavior | Drops |
|---|---:|---|---|
| **Iron-Hound (patrol)** | 12 | Spawns in pairs, faster | Iron-Hound Plate-Scale, D-tier weapons |
| **Road-Wraith** (new) | 11 | Ghost of a fallen patrol-soldier, ranged stillfire dart | C-tier consumables (rare) |
| **Lantern-Hound** (new) | 12 | Iron-Hound with broken built-in stillfire-lamp, lights area | Sentry-Wing Lens, Iron-Hound Plate-Scale |
| **Sundered Auxiliary** (new) | 13 | Small armed Heleth construct that supported patrols, dual short-blades | Reliquary Glyph-Tile |

**Zone Nano Banana prompt (16:9):**
> *Top-down 3/4 isometric view of an old worn stone road cutting through cheerful scrubland under a bright cloudy sky, broken bronze imperial milestones half-fallen with vibrant green grass growing around them, soft bramble bushes with tiny flowers, a cute abandoned guard-tower visible in the distance with faded Vaelthar Imperial banners, charmingly empty, vibrant green and warm beige palette with bright magic-blue stillfire glow sparkling from cracks in milestones, no UI elements, vibrant cartoon mobile MMO environment, bright saturated colors, lush cheerful palette, 16:9.*

**Mob Nano Banana prompts (1:1):**

- **Iron-Hound (patrol variant):** *Same as Iron-Hound but wearing a small brass collar with imperial Vaelthar livery and a tiny bell, more battle-scarred, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Road-Wraith:** *A translucent ghost of a Vaelthar patrol-soldier in faded imperial bronze armor, half-faded, pale-blue stillfire chains around its limbs, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Lantern-Hound:** *An Iron-Hound construct with a small broken lantern-housing mounted on its back, pale-blue light leaking from the cracked housing, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Sundered Auxiliary:** *A small bipedal Heleth construct, lean armored chassis, dual short bronze blades for arms, single eye-lens on a stalked head, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*

## D1 — Vaelm-Lesser Ruin (Level 14–16)

A minor cathedral of the old Empire. The chord-engine here has been silent for 300 years. The garrison hasn't noticed.

| Mob | Lv | Behavior | Drops |
|---|---:|---|---|
| **Wayward Knight** (template 3) | 15 | Slow but high damage, executes formal guard-patterns | Wayward Bell-Shard, C-tier weapons |
| **Reliquary Watcher** (new) | 14 | Stationary Heleth observer, ranged pale-blue beam | Reliquary Glyph-Tile |
| **Bell-Hound** (new) | 15 | Iron-Hound variant with a chapel bell visible in its jaws, rings on aggro | Wayward Bell-Shard |
| **Cathedral-Crawler** (new) | 16 | Six-legged insect nested in chord-engine housings | Reliquary Glyph-Tile (rare) |
| **Bound Spectre** (new) | 16 | Ghost of a chord-engine attendant, phases through walls | Raw Chord-Sand (rare), C-tier consumables |

**Zone Nano Banana prompt (16:9):**
> *Top-down 3/4 isometric view of a moss-overgrown imperial cathedral ruin, broken white-stone columns and toppled archways carved with imperial Vaelthar crown-and-bell motifs, faint pale-blue stillfire light seeping from cracks in the stone floor where the dead chord-engine still lies sealed, ivy curtains across collapsed walls, a single shaft of dust-filled light from a hole in the partial ceiling, sense of held breath, vibrant cheerful palette with warm golden light pockets, no UI elements, vibrant cartoon mobile MMO environment, bright saturated colors, lush cheerful palette, 16:9.*

**Mob Nano Banana prompts (1:1):**

- **Wayward Knight:** *A tall armored figure in tarnished bronze imperial Vaelthar plate, helm closed, holding a long bronze longsword in formal guard position, faint pale-blue stillfire glow leaking from the helm's eye-slits, ornate crown-and-bell motifs on the chest, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Reliquary Watcher:** *A stationary statue-like Heleth construct, humanoid pale-stone figure with a single large glowing pale-blue eye-lens set in its chest, no legs, suspended slightly above the ground, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Bell-Hound:** *Like Iron-Hound but covered in faintly glowing pale-blue runes, a small bronze cathedral bell visible inside its open jaws as if perpetually swallowed, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Cathedral-Crawler:** *A large six-legged insect creature with a chitinous exoskeleton of cracked pale Heleth-stone, faintly glowing seams between plates, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Bound Spectre:** *A translucent ghost of an imperial chord-engine attendant in faded white-and-bronze robes, chains of pale-blue stillfire light wrapped around its wrists, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*

## E1 — Crooked Lake (Level 19–21)

A flooded chord-engine site. Silent Ord penitents come here to die. Some don't manage to.

| Mob | Lv | Behavior | Drops |
|---|---:|---|---|
| **Silent-Brute** (template 4) | 20 | Slow, huge damage, iron-tongue lash | Penitent Iron Strip, B-tier weapons |
| **Reed-Stalker** (new) | 19 | Silent Ord scout, ambushes from reeds | Black-Linen Scrap |
| **Lake-Lurker** (new) | 20 | Submerged Stilled (former servitor drowned in lake) | B-tier consumables, Black-Linen Scrap |
| **Mire-Newt** (new) | 21 | Pack of warped natural newts, stillfire-touched | Penitent Iron Strip (rare) |
| **Penitent-Mother** (new, elite) | 21 | Elder Silent-Brute, leads raid-parties of Reed-Stalkers | Penitent Iron Strip, Sealed Footgear (4220) |

**Zone Nano Banana prompt (16:9):**
> *Top-down 3/4 isometric view of a cheerful fantasy lake at golden hour, bright turquoise-blue water with floating clusters of green reeds, twisted gnarled trees rising from the water glowing with friendly magic-blue stillfire light at the cracks, a half-submerged Heleth ruin on a small islet in the center, scattered lily pads, Silent Ord cute orange-flame brazier visible on a far shore, vibrant green and turquoise palette with warm sunset accents, no UI elements, vibrant cartoon mobile MMO environment, bright saturated colors, lush cheerful palette, 16:9.*

**Mob Nano Banana prompts (1:1):**

- **Silent-Brute:** *A huge bipedal humanoid the size of two men, sewn into rough iron Atonement plating, no visible face behind the iron helm-cage, white linen wraps stained brown, a long iron-edged tongue-whip held in one hand, black-flame brand visible on the chest plate, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Reed-Stalker:** *A lean Silent Ord scout in black-stained white linen wraps, carrying a thin reed-spear, partially obscured by stylized reeds suggesting marsh-camouflage, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Lake-Lurker:** *A long eel-like aquatic creature, body partially mechanical (former Heleth servitor) and partially natural, multiple small glowing pale-blue eye-lenses, wide spitting maw, partially submerged, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Mire-Newt:** *A small dark-green newt with bright pale-blue stillfire glow along its dorsal stripe and webbed feet, alert posture, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Penitent-Mother (elite):** *A larger Silent-Brute variant, female, taller and gaunt, wearing more ceremonial Atonement plating with the black-flame brand etched directly into the iron, a long iron-shod staff in one hand, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*

## C3 — West Verge Outpost

NPC guards. No spawns. Shops + quest-givers (Reliquary scribes, Bell branch quartermaster).

**Nano Banana zone prompt (16:9):**
> *Top-down 3/4 isometric view of a small fortified Verge outpost on the edge of grasslands, a wooden palisade wall with bronze-reinforced gates, two small guard-towers flying the cracked-bell-under-crown banner, a central courtyard with a Reliquary scribe's tent, vendor stalls, and a stone well, Verge guards in bronze ring-mail standing watch, warm afternoon light, no UI elements, vibrant cartoon mobile MMO environment, bright saturated colors, lush cheerful palette, 16:9.*

## E3 — East Verge Outpost

Mirror of C3. Different vendor mix: Brass-House trade-tent, forge tent, fishing supplies.

**Nano Banana zone prompt (16:9):**
> *Same as West Verge Outpost but with a small smithing forge-tent with smoke rising, a Brass-House trade tent showing three-ring banners alongside the Verge banners, and a dock visible to the east with drying nets, slight industrial atmosphere, 16:9.*

## D0 — Boss Vault: The Held Note (Level 50)

The sealed sub-vault beneath Vaelm-Lesser, where one of the four surviving Hush-Magisters has been note-binding herself to a dying chord-shard for 300 years. End-of-alpha. Quest-gated.

| Mob | Lv | Behavior | Drops |
|---|---:|---|---|
| **Bell-Sentry** (new) | 48 | Stationary, ranged tone-beam | Heleth Glyph-Shard |
| **Echo-Wraith** (new) | 49 | Phases through walls, ambushes | Raw Chord-Sand, S-tier consumables |
| **Hush-Magister Aurelyne** (template 9) | 50 | BOSS — phases, tuning-fork strikes, summons Echo-Wraiths, **will speak — do not answer** | Imperial Crown-Fragment (guaranteed), Bell-Knighthood token |

**Zone Nano Banana prompt (16:9):**
> *Top-down 3/4 isometric view of a vast subterranean Heleth vault, polished obsidian floor reflecting cold pale-blue light from suspended Heleth-glass shards floating mid-air, towering pillars carved with imperial Vaelthar bell-script, a central raised platform where a tall silver tuning-fork-shaped figure in pale robes stands beside a cracked chord-engine sphere, dramatic high-contrast lighting, sense of held-breath quiet, no UI elements, painterly post-imperial fantasy boss arena concept art, 16:9.*

**Mob Nano Banana prompts (1:1):**

- **Bell-Sentry:** *A floating Heleth construct shaped like a hollow brass bell suspended in air, single glowing pale-blue eye-slit in its base, faint sound-ripples visible around it, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Echo-Wraith:** *A faintly translucent humanoid figure made of pale-blue sound-waves and faded imperial Vaelthar robes, no clear face, drifting just above the ground, vibrant chibi cartoon creature, big cute eyes, bright saturated colors, plain neutral background, 1:1.*
- **Hush-Magister Aurelyne (BOSS):** *A tall female figure in long pale-silver imperial Vaelthar court robes, holding two tuning-fork-shaped weapons crossed before her, a smooth silver mask with no features over the face, ethereal pale-blue resonance lines visible in the air around her, ornate ceremonial bronze chord-Warden's headdress, intimidating dramatic pose, painterly post-imperial fantasy BOSS concept art, plain neutral background, 1:1.*

---

# PART 3 — Updated `ROOM_SPAWNS`

Replace the existing table in `GameRoom.ts` / `WORLD_MAP_ALPHA.md`:

```ts
// Per-room mob spawns. Multiple templates per room = Ragnarok-style biome.
// Sea / unused indices are absent — server rejects joins to them.
const ROOM_SPAWNS: Record<number, Array<{ templateId: number; count: number }>> = {
    // D0  Boss Vault (lv 48-50)
    3:  [
        { templateId: 9,  count: 1  },  // Hush-Magister Aurelyne (boss)
        { templateId: 10, count: 4  },  // Bell-Sentry
        { templateId: 11, count: 3  },  // Echo-Wraith
    ],
    // D1  Vaelm-Lesser Ruin (lv 14-16)
    10: [
        { templateId: 3,  count: 4 },  // Wayward Knight
        { templateId: 20, count: 3 },  // Reliquary Watcher
        { templateId: 21, count: 3 },  // Bell-Hound
        { templateId: 22, count: 2 },  // Cathedral-Crawler
        { templateId: 23, count: 2 },  // Bound Spectre
    ],
    // E1  Crooked Lake (lv 19-21)
    11: [
        { templateId: 4,  count: 2 },  // Silent-Brute
        { templateId: 30, count: 4 },  // Reed-Stalker
        { templateId: 31, count: 3 },  // Lake-Lurker
        { templateId: 32, count: 5 },  // Mire-Newt
        { templateId: 33, count: 1 },  // Penitent-Mother (elite)
    ],
    // C2  Old Road North — transit overflow
    16: [
        { templateId: 2,  count: 3 },  // Iron-Hound
        { templateId: 40, count: 2 },  // Road-Wraith
    ],
    // D2  The Wayside (lv 11-13)
    17: [
        { templateId: 2,  count: 4 },  // Iron-Hound (patrol)
        { templateId: 40, count: 2 },  // Road-Wraith
        { templateId: 41, count: 2 },  // Lantern-Hound
        { templateId: 42, count: 3 },  // Sundered Auxiliary
    ],
    // B3  Iron Hills (lv 9-11)
    22: [
        { templateId: 2,  count: 4 },  // Iron-Hound
        { templateId: 50, count: 3 },  // Scent-Vole
        { templateId: 51, count: 3 },  // Sentry-Wing
        { templateId: 52, count: 2 },  // Iron-Larva
        { templateId: 53, count: 2 },  // Quarry-Mole
    ],
    23: [],   // C3  West Verge Outpost — safe
    24: [],   // D3  TOLLING VALE — safe hub
    25: [],   // E3  East Verge Outpost — safe
    // F3  Engine-Slime Forest (lv 4-6)
    26: [
        { templateId: 1,  count: 6 },  // Engine-Slime
        { templateId: 60, count: 5 },  // Coolant-Drip
        { templateId: 61, count: 3 },  // Loom-Fly
        { templateId: 62, count: 3 },  // Geometry-Beetle
        { templateId: 63, count: 2 },  // Murmur-Vine
    ],
    // C4  SW Meadow (lv 1-3 overflow)
    30: [
        { templateId: 0,  count: 6 },  // Husk-Crab
        { templateId: 70, count: 4 },  // Polish-Roach
        { templateId: 71, count: 3 },  // Lantern-Moth
    ],
    // D4  Crab-Meadow (lv 1-3 starter)
    31: [
        { templateId: 0,  count: 8 },  // Husk-Crab
        { templateId: 70, count: 5 },  // Polish-Roach
        { templateId: 71, count: 3 },  // Lantern-Moth
        { templateId: 72, count: 3 },  // Resonance-Vole
        { templateId: 73, count: 2 },  // Dustling
    ],
    // E4  SE Meadow (lv 1-3 overflow)
    32: [
        { templateId: 0,  count: 6 },  // Husk-Crab
        { templateId: 71, count: 4 },  // Lantern-Moth
        { templateId: 73, count: 3 },  // Dustling
    ],
};
```

You'll need to register **24 new mob templates** in `MMO-Server-Colyseus/src/data/mobs.ts`:

- 10 Bell-Sentry, 11 Echo-Wraith (D0)
- 20–23 Reliquary Watcher, Bell-Hound, Cathedral-Crawler, Bound Spectre (D1)
- 30–33 Reed-Stalker, Lake-Lurker, Mire-Newt, Penitent-Mother (E1)
- 40–42 Road-Wraith, Lantern-Hound, Sundered Auxiliary (D2)
- 50–53 Scent-Vole, Sentry-Wing, Iron-Larva, Quarry-Mole (B3)
- 60–63 Coolant-Drip, Loom-Fly, Geometry-Beetle, Murmur-Vine (F3)
- 70–73 Polish-Roach, Lantern-Moth, Resonance-Vole, Dustling (D4)

---

# PART 4 — Nano Banana Workflow

1. **First time only:** paste the global style prefix + generate a single reference image ("a Verge outpost at golden hour"). Save it as your benchmark. Use it as a "style reference attachment" for every future generation if Nano Banana supports it.
2. **Batch by zone.** Generate all 5 mobs of one zone in a single session — they share the global style prefix + the zone's lighting. Keeps the ecosystem visually coherent.
3. **Items 1:1, mobs 1:1, zones 16:9.** Aspect ratio matters more than people think.
4. **Negative prompt every time** if quality drifts: *"No text, no UI, no anime, no Ragnarok cute, no photorealism, no Disney style, no children's book."*
5. **Iterate, don't restart.** When close-but-wrong, tell Nano Banana what to change rather than re-prompting: *"Same image but make the bronze more verdigris and the stillfire glow paler."* 2–3 iterations usually finishes the job.
6. **Save the prompts alongside the outputs.** Each generation should be reproducible. Drop the prompt in the image's filename or a sidecar `.txt`.

---

# PART 5 — Open Questions

- **Set bonuses.** "Wear 3 Bell-Knight pieces → +5% resonance" is appealing but adds balance work. Defer to post-alpha.
- **Crafting recipes.** This doc lists materials but not recipes. Define in `crafting.md` once a Norgil-equivalent crafting NPC is wired.
- **Drop probabilities.** Names listed here, weights live in `data/mobs.ts`. Treat this doc as design intent, not source of truth for tuning.
- **Sub-zones.** Tolling Vale interior (the Keep itself) might be a separate Colyseus room later. Out of scope for alpha.
- **Boss cosmetic drop.** Hush-Magister's Imperial Crown-Fragment is guaranteed. Add a low-probability cosmetic (Aurelyne's mask?) for repeat clears in alpha-2.
- **Mira's Locket & The Last Tolling.** Both lore-locked. Should they be obtainable in *any* timeline, even alpha-3+? Probably not — both belong to specific characters. They are listed for completeness only.
