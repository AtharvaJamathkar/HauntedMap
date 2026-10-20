# 🕯️ Labyrinth of Oblivion

![Unity](https://img.shields.io/badge/Unity-2022.3%20LTS-black?style=flat&logo=unity)
![AI](https://img.shields.io/badge/AI-Finite%20State%20Machine-red)
![Genre](https://img.shields.io/badge/Genre-Survival%20Horror-8A0303)

> **Trapped. Hunted. Escape.**

**Labyrinth of Oblivion** is a first-person 3D survival horror game where strategic exploration meets psychological tension. Trapped in a dark, complex maze, you must scavenge for tools, solve the layout, and evade a hostile, intelligent entity that listens to your every move.

<img width="1915" height="897" alt="image" src="https://github.com/user-attachments/assets/0b32c4d9-3d53-407f-be5f-1f59536cc796" />
<img width="1919" height="896" alt="image" src="https://github.com/user-attachments/assets/0a7d4b8c-cbdf-47c9-84e3-e11b581d0c60" />
<img width="1913" height="888" alt="image" src="https://github.com/user-attachments/assets/12aa2fe1-0271-41ca-a5af-268f22a3cf63" />
<img width="1919" height="889" alt="image" src="https://github.com/user-attachments/assets/61172c02-4cbd-4718-a4c2-f43c4c8761b5" />

---

## 💀 Gameplay Overview

The goal is simple: **Escape.**
To do so, you must explore the environment and interact with chests to find three critical items:
1.  **The Lantern:** To navigate the crushing darkness.
2.  **The Gun:** A limited-use weapon for last-resort defense.
3.  **The Key:** Randomly hidden in a chest, required to unlock the exit.

**The Catch:** You are not alone. An AI-driven enemy patrols the maze, reacting dynamically to light and sound.

---

## 🧠 AI & Systems Implementation

The core of this project is a modular C# codebase focusing on intelligent enemy behavior and immersive systems.

### 🤖 Enemy AI (FSM + NavMesh)
The enemy utilizes a **Finite State Machine (FSM)** integrated with **Unity NavMesh** to transition between behaviors smoothly:
* **Idle/Patrol:** Roams the maze using a network of waypoints.
* **Chase:** Triggered upon visual confirmation of the player.
* **Attack:** Engages when in close proximity.
* **Detection System:** The AI utilizes **Spatial Sound Triggers**. Running, opening chests, or dropping objects generates "noise" that draws the enemy to your location.

### 🔦 Dynamic Mechanics
* **Interaction System:** Raycast-based interactions for opening chests and collecting items.
* **Lighting:** Real-time lantern mechanics where light is a resource. Lights may flicker or deactivate based on game events to heighten tension.
* **Weapon System:** A "One-Shot" firearm mechanic. It is not an action game; the gun is a tool with a long reload and limited ammo, designed to create moments of vulnerability.

---

## 🛠️ Tech Stack

| Category | Tool/Technology |
| :--- | :--- |
| **Engine** | Unity 2022.3 LTS |
| **Language** | C# (Modular Scripting) |
| **AI** | NavMesh Agent, Finite State Machine (FSM) |
| **Animation** | Unity Animator, Timeline, Adobe Mixamo |
| **Assets** | Blender (3D Modeling of maze/props) |

---

## 🎮 Game Flow

1.  **Awakening:** Player starts in a locked, dark maze environment.
2.  **Scavenging:** Locate chests. RNG determines which chest contains the **Key**.
3.  **Survival:** Avoid the patrolling enemy. Use the **Lantern** wisely—light reveals the path but attracts attention.
4.  **Escape:** Bring the Key to the Exit Door.
5.  **Fail State:** If the enemy catches you, the game transitions to a Death Scene.

---

## 📊 Project Status

**Current Version:** Prototype (Playable)
* ✅ Fully integrated gameplay loop (Start -> Gameplay -> Win/Loss).
* ✅ Functional AI with pathfinding and state switching.
* ✅ Inventory and Item collection systems working.

**Planned Enhancements:**
* [ ] **Procedural Generation:** Move from a static maze to runtime map generation.
* [ ] **Adaptive AI:** Enemy "learns" player patterns (e.g., checking hiding spots).
* [ ] **UI Overhaul:** Diegetic UI for health and inventory management.

---

## ⚙️ Setup & Requirements

* **Unity Version:** 2022.3 LTS or higher.
* **Hardware:** GPU with support for real-time dynamic lighting and shader processing.
* **Input:** Keyboard & Mouse (Standard FPS controls).

---
