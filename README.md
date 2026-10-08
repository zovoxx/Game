# Sevenfold

A fast, side-view action roguelike for iPad, iPhone and desktop browsers. Seven chapters, seven bosses, one life, and an endless loop.

Everything is in a single self-contained `index.html`: plain HTML, JavaScript and Canvas 2D. All art is drawn in code and all sound is generated with the Web Audio API. There are no image, sound or font files, no libraries and no build step.

## Play

- **Locally:** open `index.html` in a browser.
- **GitHub Pages:** in the repository settings, go to *Pages*, choose *Deploy from a branch*, pick the branch and `/ (root)`, and open the URL it gives you.
- **iPad:** use the *Fullscreen* button on the title screen or in the pause menu.
- **iPhone:** Safari has no fullscreen API, so tap *Share › Add to Home Screen*. The Home Screen version opens without browser bars.

Audio starts after the first tap or key press, which iOS requires. The sound on/off setting is the only thing the game saves.

## Controls

| Action | Touch | Keyboard |
| --- | --- | --- |
| Move | Floating stick (left thumb, anywhere on the left side) | A / D or arrows |
| Aim up / down | Stick up / down | W / S or arrows |
| Jump (double jump in the air) | Jump button | Space |
| Drop through a platform | Stick down + Jump | S + Space |
| Dash (invincible, costs stamina) | Dash button | Shift |
| Weapon 1 / Weapon 2 | Big buttons. Tap for the combo, hold about 0.35 s and release for a charged attack | J / K |
| Up attack / plunge | Stick up + attack / stick down + attack in the air | W + attack / S + attack in the air |
| Skill 1 / Skill 2 | Small buttons (with cooldown sweeps) | U / I |
| Power | Ring button (greyed out until you own a Power) | O |
| Inspect an item | Tap its label, or tap an icon in the build bar | E, or hover / click with the mouse |
| Pause | Top-right button | Esc |

## Debug mode

Add `?debug=1` to the URL, for example `index.html?debug=1`. The **DBG** button (or the backtick key) opens a panel where you can:

- jump to any chapter and loop, or straight to its boss, and force a fork
- grant any weapon (optionally Legendary), skill, power or curse, and fuse powers
- turn on god mode or show hitboxes
- kill all enemies, heal, forge, and spawn any enemy (optionally as an elite)

An FPS counter is also shown. Normal players never see any of this.

## Tuning

Balance values live in data tables near the top of the script:

- `BAL`: global numbers such as HP, stamina, scaling per chapter and per loop, and crit
- `WTYPES` / `WEAPONS`: weapon move sets and the 25 weapons
- `SKILLS`, `POWERS`, `FUSIONS`, `CURSES`
- `EN`: enemy and boss stats
- `CHAPTERS`: palettes, enemy pools and hazards
- `CHUNKS`: the hand-designed ASCII level chunks, with a legend in the comment above them
