# Alpha World Map — *The Isle of Vaelmir*

> **Scope:** the playable island in the current alpha build.
> **Room size:** **2000 × 2000 px per Colyseus room.** Each room = one map cell.
> **World size:** 7 cells × 7 cells = **14,000 × 14,000 px** in world-space if you flattened it; in practice only the **29 land cells** of the island shape are real rooms. Everything else is sea.
> **Setting:** the island of **Vaelmir**, the seat of the Verge in the central Shardlands of Vaelthar.
> **Lore reference:** see [`LORE.md`](./LORE.md).

---

## Design intent

- **Island shape, not rectangle.** The world has a coastline. You cannot walk past the edge cells — the sea is a hard wall, but visible (creates atmosphere, defines geography).
- **Each room is one cell.** 2000×2000 px is the sweet spot for GM performance and Colyseus broadcast load.
- **Center is safe.** The Tolling Vale (cell `D3`) is the player spawn and the social hub. All other zones radiate outward.
- **Outer cells locked for staged release.** The alpha plays ~10 rooms. The other ~19 are sealed (visible on the map with a "🔒 sealed" tag) and unlock in later content patches.
- **One mob template per cell.** Each room has a clear identity: "this is the lake," "this is the ruin." Players orient by zone, not coordinates.

---

## The island

```
            COL A     COL B     COL C     COL D     COL E     COL F     COL G
           x=0-2k   x=2-4k   x=4-6k   x=6-8k   x=8-10k  x=10-12k x=12-14k
        ┌─────────┬─────────┬─────────┬─────────┬─────────┬─────────┬─────────┐
ROW 0   │   ≈≈    │   ≈≈    │  🔒🔒🔒  │  ★★★★★  │   ≈≈    │   ≈≈    │   ≈≈    │
y=0-2k  │   sea   │   sea   │  Pale   │  Boss   │   sea   │   sea   │   sea   │
        │         │         │ Cliffs  │ Vault   │         │         │         │
        ├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
ROW 1   │   ≈≈    │  🔒🔒🔒  │  ▒▒▒▒▒  │  RRRRR  │  ~~~~~  │  🔒🔒🔒  │   ≈≈    │
y=2-4k  │   sea   │ Cold    │ Seven-  │ Vaelm-  │ Crooked │ Iron    │   sea   │
        │         │ Moors   │ fold N  │ Lesser  │ Lake    │ Reach   │         │
        ├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
ROW 2   │   ≈≈    │  ▒▒▒▒▒  │  ░░░░░  │  ░░░░░  │  FFFFF  │  FFFFF  │  🔒🔒🔒  │
y=4-6k  │   sea   │ Wolf    │ Old     │ The     │ Engine- │ Eastern │ Coast   │
        │         │ Hills   │ Road N  │ Wayside │ Slime   │ Forest  │ Bluff   │
        ├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
ROW 3   │  🔒🔒🔒  │  HHHHH  │  VVVVV  │ ⭐⭐⭐⭐⭐ │  VVVVV  │  FFFFF  │  ░░░░░  │
y=6-8k  │ Western │ Iron    │ West    │ TOLLING │ East    │ Engine- │ Eastern │
        │ Cliffs  │ Hills   │ Verge   │ VALE    │ Verge   │ Slime   │ Coast   │
        │ 🔒      │         │ outpost │ SAFE    │ outpost │ Forest  │         │
        ├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
ROW 4   │   ≈≈    │  HHHHH  │  ▒▒▒▒▒  │  ▒▒▒▒▒  │  ▒▒▒▒▒  │  ░░░░░  │   ≈≈    │
y=8-10k │   sea   │ Iron    │ SW      │ CRAB-   │ SE      │ Coast   │   sea   │
        │         │ Quarry  │ Meadow  │ MEADOW  │ Meadow  │ Path    │         │
        ├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
ROW 5   │   ≈≈    │   ≈≈    │  ░░░░░  │  ░░░░░  │  ░░░░░  │   ≈≈    │   ≈≈    │
y=10-12k│   sea   │   sea   │ Fisher  │ South   │ Coastal │   sea   │   sea   │
        │         │         │ Cove    │ Beach   │ Path    │         │         │
        ├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┤
ROW 6   │   ≈≈    │   ≈≈    │   ≈≈    │  ⛵⛵⛵  │   ≈≈    │   ≈≈    │   ≈≈    │
y=12-14k│   sea   │   sea   │   sea   │ Port    │   sea   │   sea   │   sea   │
        │         │         │         │ Stilling│         │         │         │
        └─────────┴─────────┴─────────┴─────────┴─────────┴─────────┴─────────┘
```

### Tile legend

| Symbol | Meaning |
|---|---|
| `≈≈` | **Sea.** Not a room. The island's edge. |
| `⭐` | Tolling Vale — **safe hub + spawn point**. |
| `★★` | Boss vault — alpha endgame, gated. |
| `⛵` | Port — south-coast village, alpha social/economy hub. |
| `RR` | Ruin |
| `~~` | Swamp / lake |
| `▒▒` | Meadow / open grass |
| `HH` | Hills |
| `FF` | Forest |
| `VV` | Village / outpost |
| `░░` | Road / coastal path (low-mob traversal) |
| `🔒` | **Sealed in alpha.** Visible on the map, returns "the gate is closed" if entered. Future patch content. |

---

## Room directory (29 land cells)

| Cell | Room name | Mob | Level | Status |
|---|---|---|---|---|
| **C0** | Pale Cliffs | — | — | 🔒 sealed |
| **D0** | **Boss Vault — The Held Note** | Hush-Magister | 50 | 🔓 gated by quest |
| **B1** | Cold Moors | — | — | 🔒 sealed |
| **C1** | Sevenfold Wood North | Engine-Slime (elite) | 18 | 🔒 sealed |
| **D1** | **Vaelm-Lesser Ruin** | Wayward Knight | 15 | 🔓 open |
| **E1** | **Crooked Lake** | Silent-Brute | 20 | 🔓 open |
| **F1** | Iron Reach | — | — | 🔒 sealed |
| **B2** | Wolf Hills | — | — | 🔒 sealed |
| **C2** | Old Road North | road only | — | 🔓 transit |
| **D2** | **The Wayside** | Iron-Hound (patrol) | 12 | 🔓 open |
| **E2** | Engine-Slime Bog (north) | — | — | 🔒 sealed |
| **F2** | Eastern Forest | — | — | 🔒 sealed |
| **G2** | Coast Bluff | — | — | 🔒 sealed |
| **A3** | Western Cliffs | — | — | 🔒 sealed |
| **B3** | **Iron Hills** | Iron-Hound | 10 | 🔓 open |
| **C3** | **West Verge Outpost** | — | — | 🔓 safe-ish (NPC guards) |
| **D3** | ⭐ **THE TOLLING VALE** | — | — | 🔓 **SAFE HUB / SPAWN** |
| **E3** | **East Verge Outpost** | — | — | 🔓 safe-ish (NPC guards) |
| **F3** | **Engine-Slime Forest** | Engine-Slime | 5 | 🔓 open |
| **G3** | Eastern Coast | — | — | 🔒 sealed |
| **B4** | Iron Quarry | — | — | 🔒 sealed |
| **C4** | Southwest Meadow | Husk-Crab | 1 | 🔓 open (overflow) |
| **D4** | **Crab-Meadow** | Husk-Crab | 1 | 🔓 **starter zone** |
| **E4** | Southeast Meadow | Husk-Crab | 1 | 🔓 open (overflow) |
| **F4** | Coast Path | — | — | 🔒 sealed |
| **C5** | Fisher Cove | — | — | 🔒 sealed |
| **D5** | South Beach | — | — | 🔒 sealed |
| **E5** | Coastal Path | — | — | 🔒 sealed |
| **D6** | ⛵ **Port Stilling** | — | — | 🔒 sealed (alpha-2 hub) |

**Open in alpha (10 rooms):** D3 (hub), C3, E3, B3, D2, D1, E1, D0, C4, D4, E4.
**Sealed (19 rooms):** the rest. Visible on the map. Each shows a "🔒 The way is closed" message when bumped.

---

## The alpha play loop

```
                     [ D0  Boss Vault ]  ← alpha endgame
                            ↑ gated by quest chain
                     [ D1  Vaelm-Lesser Ruin ] ← lv 15 mid-game
                            ↑
                     [ D2  The Wayside ] ← lv 12 transit
                            ↑                    [ E1  Crooked Lake ]  lv 20 (east branch)
                            │                            ↑
   [ B3  Iron Hills ] ←  [ D3  TOLLING VALE  ⭐ ] → [ F3  E.Slime Forest ]
        lv 10                  safe hub                    lv 5
                            │
                     [ D4  Crab-Meadow ] ← lv 1 tutorial
```

**Recommended progression:**
1. Spawn in D3 (Tolling Vale).
2. Walk south through Verge-Hold gates to **D4 Crab-Meadow** (lv 1 tutorial mobs, friendly).
3. Try **F3 Engine-Slime Forest** to the east (lv 5, your first aggressive encounters).
4. Try **B3 Iron Hills** to the west (lv 10).
5. Go north through the gate into **D2 The Wayside** (lv 12, patrolling Iron-Hounds).
6. Tackle **D1 Vaelm-Lesser Ruin** (lv 15, Wayward Knights). Collect Reliquary Key shards.
7. Branch east to **E1 Crooked Lake** (lv 20, Silent-Brutes). Loot Sealed Footgear.
8. Return to D1, assemble the key.
9. Open **D0 Boss Vault**, fight the Hush-Magister. Earn a Bell-Knighthood.

That's the alpha endgame.

---

## Server config (Colyseus)

### Room index mapping

Convert `(col, row)` to a flat Colyseus `roomIndex` so each grid cell is its own room:

```ts
// 7 wide × 7 tall = 49 indices. Most are sea/unused but the index map is stable.
function cellToRoomIndex(col: number, row: number): number {
    return row * 7 + col;       // A=0..G=6, row 0..6 → roomIndex 0..48
}
// Examples:
//   D3 (tolling vale) = 3*7 + 3 = 24
//   D4 (crab-meadow)  = 4*7 + 3 = 31
//   D0 (boss vault)   = 0*7 + 3 = 3
```

### Spawn config table

Replace the current `roomMobConfigs` in `GameRoom.ts` with the per-cell table below. Sea cells have no entry — the server should refuse `joinOrCreate` for them.

```ts
// Per-room mob spawns. Key = Colyseus roomIndex = row*7 + col.
// Sea / unused indices are absent — server rejects joins to them.
const ROOM_SPAWNS: Record<number, Array<{ templateId: number; count: number }>> = {
    3:  [{ templateId: 9, count: 1 }],     // D0  boss
    10: [{ templateId: 3, count: 5 }],     // D1  ruin (lv 15)
    11: [{ templateId: 4, count: 3 }],     // E1  swamp (lv 20)
    16: [{ templateId: 2, count: 4 }],     // C2  transit (overflow patrol)
    17: [{ templateId: 2, count: 6 }],     // D2  wayside (lv 12)
    22: [{ templateId: 2, count: 6 }],     // B3  hills (lv 10)
    23: [],                                // C3  west outpost (safe)
    24: [],                                // D3  TOLLING VALE (safe hub)
    25: [],                                // E3  east outpost (safe)
    26: [{ templateId: 1, count: 10 }],    // F3  forest (lv 5)
    30: [{ templateId: 0, count: 12 }],    // C4  SW meadow (lv 1 overflow)
    31: [{ templateId: 0, count: 18 }],    // D4  CRAB-MEADOW (lv 1 starter)
    32: [{ templateId: 0, count: 12 }],    // E4  SE meadow (lv 1 overflow)
};
```

The remaining indices in `ROOM_SPAWNS` are sealed/sea — `joinOrCreate(roomIndex)` should return an error if the index isn't in this table.

---

## Edge-portal transitions

Each 2000×2000 room has up to 4 neighbours. The client checks the player's local-room position each step:

```gml
// obj_Player Step — when the player crosses a room edge.
var _BORDER = 32;    // px from edge before transition fires
var _W = 2000;
var _H = 2000;
if (x < _BORDER         && room_has_neighbor("west"))  request_zone_transition("west");
if (x > _W - _BORDER    && room_has_neighbor("east"))  request_zone_transition("east");
if (y < _BORDER         && room_has_neighbor("north")) request_zone_transition("north");
if (y > _H - _BORDER    && room_has_neighbor("south")) request_zone_transition("south");
```

The server validates the transition (must be to an open room, must be adjacent in the grid), drops the player from the current Colyseus room, and joins them to the target. Player respawns on the opposite edge of the new room (entered from south = appears at north edge of the new zone).

Bumping into a sealed edge shows: `"🔒 The way is closed. Return when the world remembers it."`

Bumping into a sea edge shows nothing — the cliffs/coast are visually impassable.

---

## Why this is the right shape

- **Island ≠ infinite world.** Players see edges. The map feels *real* because it has shape.
- **2000×2000 rooms** are CPU- and bandwidth-cheap. Each room hosts ~5–20 entities max.
- **Locked cells = future content.** When alpha-2 ships, we unseal Pale Cliffs / Port Stilling / Eastern Forest. Existing players already know the map shape — they just see new icons turn green.
- **One Colyseus room per cell** scales linearly. Want to add an island? Add another grid + index range. Want to add a continent? Multiple islands, each its own grid.
- **Lore-consistent.** The island is the Verge's home turf. Beyond it lie Stannar, the Silent Citadel, Os-Karn — future continents.

---

## Open design questions

- **Sealed-cell visual treatment** — do we draw a fog-of-war texture, or a literal stone wall? Recommendation: stone wall with a banner saying which faction sealed it.
- **Boss vault gating** — quest chain through ruin + lake, or single key drop? Quest chain feels more MMO.
- **Tolling Vale interior** — single open room, or two sub-areas (Verge-Hold village + the Keep)? Single keeps it cheap.
- **PvP** — recommend keeping all of alpha PvE. Open PvP can come in alpha-3 with the addition of "contested" zones (those near Stannar / the Silent Citadel).
