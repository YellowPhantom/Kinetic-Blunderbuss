# Kinetic Blunderbuss: Ascension

[cite_start]**Kinetic Blunderbuss: Ascension** is a high-precision, physics-driven 2D platformer where your weapon is your primary engine of movement[cite: 1]. [cite_start]Navigating through 13 challenging levels, players must master the art of recoil propulsion to overcome environmental hazards and ascend the void [cite: 39-41, 211-237].

## 🎮 Gameplay Overview

In the void, standard movement is often not enough. [cite_start]Players are equipped with the **Kinetic Blunderbuss**, a powerful tool that provides massive instantaneous impulse, allowing for mid-air dashes, vertical climbs, and momentum-based puzzles [cite: 101-114].

### Core Mechanics
* [cite_start]**Recoil Propulsion**: Every shot fired generates a force exactly opposite to the aim angle, overriding current velocity for a snappy, responsive feel [cite: 111-113].
* **Fixed Ordnance**: Ammo is fixed per level. [cite_start]Players must manage their shells wisely, as they do not recharge mid-stage [cite: 40, 103-109].
* [cite_start]**The Cooldown Rhythm**: The blunderbuss has a 1-second firing delay[cite: 105, 109]. [cite_start]A dynamic cooldown bar is rendered directly above the player's head for "eyes-on-target" feedback [cite: 177-184].
* [cite_start]**Level Selection & Progression**: A robust menu system tracks your "Ascension" [cite: 52, 67-87]. [cite_start]Levels are unlocked sequentially, with a detailed hover-info panel providing shell counts and mechanic descriptions [cite: 44-47, 81-84].

## 🛠 Technical Features

[cite_start]The game is built using a single-file vanilla JavaScript and HTML5 Canvas architecture [cite: 1-267].

* [cite_start]**Robust Physics Engine**: Implements a stable **2-Pass AABB Collision Resolution** system, handling Y-axis and X-axis collisions separately to prevent clipping [cite: 137-145].
* [cite_start]**Procedural Animation**: Character visuals are rendered procedurally using a 16x16 "Terraria-style" aesthetic, including a 4-frame walking cycle and dynamic weapon rotation [cite: 153-176].
* **Environmental Diversity**:
    * [cite_start]**Ice Tiles**: Friction is significantly reduced, causing players to retain speed [cite: 50, 122, 194-196].
    * [cite_start]**Zero-G Bubbles**: Spherical zones where gravity is reduced by 90% [cite: 49, 116-121, 185-187].
    * [cite_start]**Crumbling Platforms**: Fragile blocks that dissolve shortly after contact [cite: 133-135, 142-143, 197-203].
    * [cite_start]**Moving Platforms**: Industrial lifts that require precise timing to mount and dismount [cite: 131-133, 136-137, 192-194].

## ⌨️ Controls

| Action | Input |
| :--- | :--- |
| **Move** | [cite_start]`A` / `D` or `Left` / `Right` [cite: 39, 60-63] |
| **Jump** | [cite_start]`W`, `Space`, or `Up` [cite: 40, 61-63] |
| **Aim** | [cite_start]Mouse Movement [cite: 39, 64] |
| **Fire** | [cite_start]Left Mouse Click [cite: 39, 65] |
| **Restart Level** | [cite_start]`R` [cite: 41, 60] |
| **Level Menu** | [cite_start]`ESC` [cite: 41, 59] |

## 🚀 Levels

[cite_start]The gauntlet consists of 13 hand-crafted stages [cite: 53-56]:
1.  [cite_start]**Levels 1-3**: Basic training in dashing and climbing [cite: 211-216].
2.  [cite_start]**Levels 4-6**: Introduction to crumbling paths and moving ferries [cite: 217-223].
3.  [cite_start]**Levels 7-9**: Advanced physics including Ice and Zero-G "Archipelagos" [cite: 224-228].
4.  [cite_start]**Levels 10-13**: Hardcore precision puzzles requiring perfect ammo conservation [cite: 229-237].

## ⚠️ Known Issues

* [cite_start]**Moving Platform Inertia Desync**: Players may occasionally experience a coordinate "snap" or teleport effect when jumping from vertical lifts, as the player's position is updated by the platform's velocity [cite: 136-137, 245].
* [cite_start]**Input Buffering**: The engine does not support input buffering; actions like jumping or blasting will only trigger if the key is pressed while the player is grounded or after the cooldown has depleted [cite: 109, 127-128].
* [cite_start]**Extreme Precision Requirement**: Level 11 ("ONE SHOT") is balanced with a strict limit of 3 shells, requiring a near-perfect run[cite: 231].
* [cite_start]**Frame-Rate Bound Physics**: Movement and gravity are calculated within a standard requestAnimationFrame loop, tying physics speed to the browser's refresh rate[cite: 247, 267].
* [cite_start]**Crumbling Platform Timing**: Platforms are set to dissolve exactly 40 frames after contact, creating tight timing windows [cite: 142-143].

## 📜 License

This project is licensed under the **PolyForm Noncommercial License 1.0.0**. 

* **Permitted**: Personal study, private entertainment, and non-commercial hobby projects.
* **Prohibited**: Any use primarily intended for commercial advantage or monetary compensation.
