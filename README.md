# ❄️ Frostward: Infinite Survival Map Engine

**Made by Satoru Suzuki**

A high-performance, single-file procedural world engine designed for glacial apocalypse and 4X survival games. This engine simulates an infinite frozen wasteland where every tile represents a **1x1 km area**, governed by complex thermal and atmospheric noise layers.

Inspired by survival strategy titles like *Whiteout Survival*, this tool provides a foundation for building infinite exploration games without the overhead of heavy game engines.

---

## 🛠 The Survival Logic

Unlike standard random generators, Frostward uses **Triple-Layer Noise Abstraction** to determine the environment:

1.  **Elevation ($e$):** Determines the physical landscape, from frozen oceanic abysses to towering glacial spires.
2.  **Blizzard Severity ($s$):** A moisture-equivalent layer that dictates snow density and "Whiteout" visibility zones.
3.  **Cold Intensity ($c$):** Represents temperature flux. Low $c$ values indicate **Geothermal Vents** or **Furnace Cities**, while high $c$ values create lethal "Deep Freeze" zones.

---

## ✨ Key Features 

* **🌐Infinite Procedural Exploration:** Uses Fractal Brownian Motion (FBM) with 4 octaves to ensure natural terrain across infinite coordinates.
* **🏘️Heat-Sync Settlements:** Features an intelligent spawning system for **Furnace Cities**, **Coal Mines**, and **Survivor Camps** based on local thermal data.
* **⚓Contextual Coastal Logic:** Port cities and Icebreaker Docks only spawn on "Ice Shelf" tiles that are adjacent to "Frozen Ocean".
* **📋The Survivor's Log:** A built-in coordinate-based ledger that allows players to "tag" locations with notes on resources, threats, or supply caches.
* **💾 Persistent Save System:** Integrated `localStorage` support. Your coordinates ($X, Y$), current world seed, and all ledger notes are automatically saved and reloaded upon return.
* **📋 Survivor Log Reviewer:** A new centralized log interface allows you to view all notes made across the infinite map in one chronological list, making it easier to track discovered resources.
* **🔑 Custom Seed Injection:** Players can now manually input and "Load" specific world seeds, allowing for shared world exploration and speed-running.
* **⚙️ Unified System Menu:** A clean modal-based UI replaces the old action bar, housing world-reset, trekking, and log-management tools.
* **💯Zero-Dependency Architecture:** A "Digital Talisman"—one single HTML file containing all Logic (JS), Styling (CSS), and Structure (HTML).

---

## 🎮 Controls

* **Navigation:** Use `WASD` or `Arrow Keys` to move your lantern through the frost.
* **🔦 Scout (Lantern):** Click your current tile to read detailed thermal data and leave a note in the **Survivor's Log**.
* **⚙️ System Menu:** Access the settings icon to save your progress, jump to new coordinates, or view your logs.
* **❄️ Blizzard Trek:** A "Void Drift" protocol that allows you to jump thousands of kilometers to a new random coordinate.
* **☢️ New Expedition:** Permanently wipe current progress and generate a completely new world seed.

---

## 🗺 Frozen Biome Reference

| Icon | Name | Description | Logic Condition |
| :--- | :--- | :--- | :--- |
| 🏭 | **Furnace City** | Human bastion with a heat core. | Low Cold + Mid Elevation |
| 🌋 | **Active Core** | Rare geothermal heat vents. | High Elevation + Low Cold |
| 🏙️ | **Ruined Metropolis** | Buried skyscrapers of the old world. | Rare Spawn (High Loot) |
| 🪵 | **Deadwood Forest** | Frozen trees used for lumber. | High Moisture + High Cold |
| 🧊 | **Deep Freeze** | Treacherous, thin abyssal ice. | Minimum Elevation ($e < 0.22$) |
| ⛺ | **Survivor Camp** | Common clusters of tents. | Frequent Spawn ($h > 0.88$) |

---

## 🚀 Deployment

1.  Download or clone the repository.
2.  Open `frostward-map1.html` in any modern web browser.
3.  No server, build-tools, or installation required. 

---

> "The frost does not judge; it only tests the strength of the flame within."
