# R-TANKS 5: Car-Mero Edition

A TRON-inspired wireframe tank combat game built with React, Three.js, and TypeScript. Explore a procedurally generated open world, battle AI opponents across infinite terrain, collect loot, talk to NPCs, call in wingman airstrikes, and build up your home base.

**[Play Now in Your Browser](https://scuffedepoch.com/react-tanks-5/)**

---

## What's New in R-TANKS 5

- **Open World** — Infinite procedurally generated terrain replaces fixed arenas. Valleys are seeded from grid coordinates so the world is consistent across sessions.
- **Valley Types** — Combat, Treasure, Settlement, Boss, Hazard, and Empty zones each with distinct enemy counts, loot tables, and NPC spawns.
- **Biomes** — Grassland, Desert, Tundra, Volcanic, Alien, and Canyon biomes with terrain-aware movement.
- **Loot System** — 6 item types across 5 rarity tiers (Common → Legendary) with deterministic position-based generation.
- **NPC Dialog System** — 4 NPC types (Merchant, Mechanic, Scout, Quest Giver) with branching dialog trees and custom portrait art.
- **Wingman Airstrikes** — 4 selectable AI wingmen (Hawk, Viper, Storm, Nova) each with a unique attack pattern on a 45-second cooldown.
- **Home Base** — Persistent player hub at valley (0,0) with starter structures, editable via the Level Editor.
- **Explosion System** — Multi-tier explosions (Small, Medium, Large) with camera shake, particle effects, and audio.
- **World Map HUD** — Live minimap showing visited valleys, current position, and valley types.
- **Engine Audio** — Procedural SNES-style engine sound with gear shifts, boost effects, and throttle response.
- **Distant Battles** — Muzzle flashes and explosions visible in neighbouring valleys for ambient atmosphere.
- **Auto-Save** — Player position, inventory, and progress saved every 30 seconds.

---

## Gameplay

You command a customizable tank in fast-paced combat across a procedurally generated open world. Explore valleys, defeat enemy tanks, collect loot, interact with NPCs, and expand your home base.

### Controls

| Action | Keys |
|--------|------|
| Move Forward / Back | `W` `S` |
| Strafe Left / Right | `A` `D` |
| Aim | Mouse |
| Fire | Left Mouse Button |
| Boost | `Spacebar` (2.5s burst, 6s cooldown) |
| Drift | `Shift` |
| Switch Weapon | `1` `2` `3` `4` `5` |
| Select Wingman | `6` `7` `8` `9` |
| Call Airstrike | `R` |
| Interact / Talk | `E` |
| Pick Up Loot | `F` |
| Toggle Camera | `V` |
| Orbit Camera | Right-Drag |
| Zoom Camera | Scroll Wheel |
| Reset Camera | `X` |
| Toggle Aim Mode | `Q` (auto / manual) |
| Pause / Save | `Escape` |

### Weapons

All weapons have unlimited ammo — cooldowns and overheat are the limits.

| # | Weapon | Damage | Fire Rate | Range | Special |
|---|--------|--------|-----------|-------|---------|
| 1 | **Precision Cannon** | 25 | 3/sec | Long | 2x critical on rear hits |
| 2 | **Plasma Mortar** | 50 | 1/sec | Mid | Splash damage, destroys cover, area denial |
| 3 | **Rapid Pulse** | 10 | 8/sec | Short-Mid | Slows targets, overheat mechanic |
| 4 | **Scatter Shot** | 12x8 | 1.5/sec | Close | 8 pellets, knockback |
| 5 | **Seeker Missile** | 90 | 0.5/sec | Any | Guaranteed hit, 8s cooldown |

### Wingmen

Call in AI support with `R` when a valid target is ahead. 45-second cooldown between strikes.

| # | Wingman | Type | Description |
|---|---------|------|-------------|
| 6 | **HAWK** | Gatling | Rapid gatling burst |
| 7 | **VIPER** | Beam | Sustained energy beam |
| 8 | **STORM** | Lightning | Chain lightning |
| 9 | **NOVA** | Missile | Homing missile barrage |

### Open World

The world is an infinite grid of 500x500-unit valleys. Each valley is procedurally generated from its grid coordinates and the world seed, so the landscape is always the same.

| Valley Type | Frequency | What to Expect |
|-------------|-----------|----------------|
| **Combat** | 35% | 3-15 enemies, light loot drops |
| **Treasure** | 15% | 3-8 loot items, high rarity chance |
| **Settlement** | 10% | NPCs with dialog, no enemies |
| **Boss** | 5% | 1-3 boss-tier enemies, heavy loot (distance ≥3 from home) |
| **Empty** | 25% | Wilderness, safe traversal |
| **Hazard** | 10% | Environmental threats, sparse enemies |

### Loot & Items

Items drop in valleys and are picked up with `F`. Each item has a rarity tier that scales its effect and value.

| Item | Effect | Base Value |
|------|--------|------------|
| Repair Kit | Restore health | 10-15 SC |
| Shield Cell | Restore shields | 10-15 SC |
| Damage Amplifier | Temporary damage buff | 12-20 SC |
| Turbo Injector | Temporary speed buff | 12-20 SC |
| Armor Plate | Temporary armor increase | 15-25 SC |
| Wingman Charge | Reduce wingman cooldown by 15s | 20-30 SC |

### NPCs

Found in Settlement valleys. Approach and press `E` to talk.

| NPC | Role | Color |
|-----|------|-------|
| **Merchant** | Buy repairs and supplies | Gold |
| **Mechanic** | Hull repair, armor upgrades | Orange |
| **Scout** | Reveal map, enemy intel | Cyan |
| **Quest Giver** | Missions and story | Magenta |

### Secrets

Every valley can contain hidden secrets at easy, medium, and hard difficulty. Discover them by exploring — look for destructible walls, hidden paths, and timed doors. Rewards include health boosts, shield upgrades, damage multipliers, and speed buffs.

### Home Base

Your persistent hub at valley (0,0). Customize your loadout, select your wingman, and deploy into the open world. The Home Base includes starter structures (Garage, Comm Tower, Supply Depot, Defensive Barriers) and can be customized with the Level Editor.

### Level Editor

Build and modify your Home Base layout with the built-in level editor. Place platforms, ramps, cover elements, and landmarks to create your ideal base of operations.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| UI Framework | React 18 |
| Language | TypeScript |
| 3D Rendering | Three.js + @react-three/fiber + drei |
| State Management | Zustand |
| Build Tool | Vite |
| Audio | Procedural Web Audio API (SNES-style synthesis) |
| Persistence | localStorage (settings, loadout, inventory, progress) |


---

## Citation

### Academic Citation

If you use this codebase in your research or project, please cite:

```bibtex
@software{r_tanks_5,
  title = {R-TANKS 5: Car-Mero Edition — TRON-Inspired Open World Tank Combat},
  author = {Drift Johnson},
  year = {2025},
  url = {https://github.com/MushroomFleet/R-TANKS-5},
  version = {5.0.0}
}
```

### Donate:

[![Ko-Fi](https://cdn.ko-fi.com/cdn/kofi3.png?v=3)](https://ko-fi.com/driftjohnson)
