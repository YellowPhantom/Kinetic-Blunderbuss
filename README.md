# Kinetic Blunderbuss: Ascension

**Kinetic Blunderbuss: Ascension** is a high-precision, physics-driven 2D platformer where your weapon is your primary engine of movement. Navigating through 13 challenging levels, players must master the art of recoil propulsion to overcome environmental hazards and ascend the void.

## 🎮 Gameplay Overview

In the void, standard movement is often not enough. Players are equipped with the **Kinetic Blunderbuss**, a powerful tool that provides massive instantaneous impulse, allowing for mid-air dashes, vertical climbs, and momentum-based puzzles.

### Core Mechanics
* **Recoil Propulsion**: Every shot fired generates a force exactly opposite to the aim angle, overriding current velocity for a snappy, responsive feel.
* **Fixed Ordnance**: Ammo is fixed per level. Players must manage their shells wisely, as they do not recharge mid-stage.
* **The Cooldown Rhythm**: The blunderbuss has a 1-second firing delay. A dynamic cooldown bar is rendered directly above the player's head for "eyes-on-target" feedback.
* **Level Selection & Progression**: A robust menu system tracks your "Ascension." Levels are unlocked sequentially, with a detailed hover-info panel providing shell counts and mechanic descriptions.

## 🛠 Technical Features

The game is built using a single-file vanilla JavaScript and HTML5 Canvas architecture.

* **Robust Physics Engine**: Implements a stable **2-Pass AABB Collision Resolution** system, handling Y-axis and X-axis collisions separately to prevent clipping.
* **Procedural Animation**: Character visuals are rendered procedurally using a 16x16 "Terraria-style" aesthetic, including a 4-frame walking cycle and dynamic weapon rotation.
* **Environmental Diversity**:
    * **Ice Tiles**: Friction is significantly reduced, causing players to retain speed.
    * **Zero-G Bubbles**: Spherical zones where gravity is reduced by 90%.
    * **Crumbling Platforms**: Fragile blocks that dissolve shortly after contact.
    * **Moving Platforms**: Industrial lifts that require precise timing to mount and dismount.

## ⌨️ Controls

| Action | Input |
| :--- | :--- |
| **Move** | `A` / `D` or `Left` / `Right` |
| **Jump** | `W`, `Space`, or `Up` |
| **Aim** | Mouse Movement |
| **Fire** | Left Mouse Click |
| **Restart Level** | `R` |
| **Level Menu** | `ESC` |

## 🚀 Levels

The gauntlet consists of 13 hand-crafted stages:
1.  **Levels 1-3**: Basic training in dashing and climbing.
2.  **Levels 4-6**: Introduction to crumbling paths and moving ferries.
3.  **Levels 7-9**: Advanced physics including Ice and Zero-G "Archipelagos".
4.  **Levels 10-13**: Hardcore precision puzzles requiring perfect ammo conservation.

## ⚠️ Known Issues

* **Moving Platform Inertia Desync**: Players may occasionally experience a coordinate "snap" or teleport effect when jumping from vertical lifts, as the player's position is updated by the platform's velocity.
* **Input Buffering**: The engine does not support input buffering; actions like jumping or blasting will only trigger if the key is pressed while the player is grounded or after the cooldown has depleted.
* **Frame-Rate Bound Physics**: Movement and gravity are calculated within a standard requestAnimationFrame loop, tying physics speed to the browser's refresh rate.

## 📜 License

This project is licensed under the **PolyForm Noncommercial License 1.0.0**. 

* **Permitted**: Personal study, private entertainment, and non-commercial hobby projects.
* **Prohibited**: Any use primarily intended for commercial advantage or monetary compensation.
