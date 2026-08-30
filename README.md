# Brick Survivors

A fast-paced roguelike shooter with Breakout-inspired mechanics. Survive waves of brick enemies, level up, and choose powerful upgrades.

## Play

Open `game.html` in any modern browser. Works offline after first load (PWA).

## Controls

| Key | Action |
|-----|--------|
| WASD / Arrow Keys | Move |
| Mouse | Aim direction |
| Auto | Shoot (always on) |
| 1-4 | Switch weapon |
| ESC | Pause |

## Weapons

| # | Weapon | Ammo | Description |
|---|--------|------|-------------|
| 1 | Pistol | Infinite | Reliable semi-auto |
| 2 | Shotgun | 30 | 5-pellet spread |
| 3 | Laser | 15 | Fast, pierces 5 enemies |
| 4 | Bomb | 5 | Explosive area damage |

## Power-ups

| Icon | Name | Effect |
|------|------|--------|
| + | Heal | Restore 30 HP |
| M | Magnet | Pull all nearby XP |
| S | Shield | +1 damage block |
| ! | Nuke | Damage all enemies |
| > | Speed | +30% speed for 5s |
| D | Damage | +50% damage for 8s |
| A | Ammo | +15 ammo all weapons |

## Upgrades (Level Up)

### Offense
- **Multi-Shot** - +1 projectile
- **Pierce** - +1 enemy pierce
- **Rapid Fire** - +25% fire rate
- **Power Shot** - +30% damage
- **Critical** - +12% crit chance
- **Chain Lightning** - Zap nearby enemies on hit
- **Explosive** - Projectiles explode

### Defense
- **Vitality** - +30 max HP
- **Regen** - Heal 2 HP every 3s
- **Thorns** - Reflect 10 damage
- **Shield** - +1 damage block
- **Armor** - -2 damage taken

### Utility
- **Haste** - +18% move speed
- **Magnet** - +60% pickup range
- **Scholar** - +30% XP gain
- **Velocity** - +35% bullet speed
- **Ricochet** - +2 wall bounces
- **Big Bullets** - +40% projectile size
- **Resupply** - +10 ammo

## Enemy Types

| Type | Shape | Behavior |
|------|-------|----------|
| Gray | Circle | Chase |
| Light Gray | Circle | Strafe |
| Dark Gray | Square | Tank (zigzag) |
| White | Triangle | Rush (charge) |
| Pure White | Triangle | Dodge projectiles |
| Elite | Diamond | Charge + shoot |
| Boss | Square | Orbit + ring attack + summon |

## Stages

Infinite procedurally generated stages. Every 3 stages, harder enemy tiers unlock. Difficulty scales per stage:
- Enemy HP +15%
- Enemy Speed +5%
- Spawn rate increases
- Boss frequency increases

## Combo System

Kill enemies quickly to build up a combo multiplier:

| Combo | Multiplier | Color |
|-------|------------|-------|
| 5 | 1.5x | Blue |
| 10 | 2.0x | Green |
| 15 | 2.5x | Orange |
| 20 | 3.0x | Pink |
| 30 | 4.0x | Red |
| 40 | 5.0x | Yellow |
| 50 | 6.0x | Cyan |
| 75 | 8.0x | Orange |
| 100 | 10x | White |

- Combo decays after 3 seconds without a kill
- Higher combos show bigger floating numbers
- Combo timer bar visible on screen
- Max combo saved to high scores

## Shop System

Earn coins by killing enemies and spend them in the shop between stages:

| Item | Cost | Effect | Max Level |
|------|------|--------|-----------|
| Attack | $50 | +20% damage | 10 |
| Health | $40 | +20 max HP | 10 |
| Speed | $30 | +10% move speed | 10 |
| Fire Rate | $60 | +15% fire rate | 8 |
| Critical | $45 | +5% crit chance | 10 |
| Regen | $35 | +1 HP/3s | 5 |
| Magnet | $25 | +30% pickup range | 8 |
| Armor | $55 | -1 damage taken | 5 |

- Shop upgrades persist across runs
- Coins earned from kills (1-3 per enemy, 8-15 for elites/bosses)
- Shop opens after completing each stage

## Level Tree

- Unlock stages by completing previous ones
- Level select screen to replay any unlocked stage
- Resume button to continue your last run
- All progress saved automatically

## Progress & High Scores

**Auto-saved to browser (localStorage):**
- Top 10 high scores with name, score, stage, time, max combo
- Lifetime stats: games played, total kills, best stage, best level
- Shop upgrades and coins
- Unlocked and completed stages
- Current run (for resume)
- Settings: auto-shoot, sound effects

Data persists across sessions. Clear browser data to reset.

## Tech Stack

- Vanilla JavaScript (no dependencies)
- HTML5 Canvas
- Web Audio API (synthesized sounds)
- PWA (offline support)
- localStorage (save system)

## Install as App

1. Open in Chrome/Edge
2. Click install icon in address bar (or menu > Install)
3. Play offline anytime

## License

Free to use and modify.
