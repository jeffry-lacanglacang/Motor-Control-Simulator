# Motor Control Simulator

**Electromechanical & Ladder Logic CAD Simulator** — A browser-based interactive schematic editor and real-time electrical circuit simulator designed around **IEC 60617** industrial control standards.

🔗 **Live Demo:** [https://jeffry-lacanglacang.github.io/Motor-Control-Simulator/](https://jeffry-lacanglacang.github.io/Motor-Control-Simulator/)

---

## ✨ Features

### ⚡ Interactive CAD Schematic Editor
* **IEC 60617 Symbol Library:** Searchable component palette organized into 7 categories:
  * **Sources:** 3-Phase + N + PE Supply (`L1/L2/L3/N/PE`), 1-Phase Supply (`L1/N`), DC Power Supply (`+24V/0V`), and Protective Earth (`PE`).
  * **Protections:** 1-Pole, 2-Pole, and 3-Pole Circuit Breakers (`MCB`), Fuse Links, and Thermal Overload Relays (`95-96 / 97-98`).
  * **Switches & Buttons:** Momentary Start (`NO`) and Stop (`NC`) Push Buttons, Dual `NO+NC` Buttons, Mushroom Emergency Stop (`E-Stop`), Maintained Selector Switches, and Limit/Roller Switches.
  * **Contactors:** 3-Pole & 4-Pole Power Contactors, Contactor Coils (`A1-A2`), and Auxiliary Contacts (`NO`, `NC`, `CO`).
  * **Coils & Timers:** Standard Coils, On-Delay Timer Coils (`TON`), Off-Delay Timer Coils (`TOF`), Flasher/Pulse Relays, and Impulse Latching Relays.
  * **Auxiliary & Timer Contacts:** Standard Relay Contacts (`NO`, `NC`, `SPDT CO`) and Delay-On Timer Contacts.
  * **Motors & Signaling:** 3-Phase Induction Motors, 3-Phase Star-Delta Motors (6-Pin), 1-Phase AC Motors, DC Permanent Magnet Motors, Pilot Indicator Lamps (customizable colors), Acoustic Buzzers/Horns, Freewheeling Diodes, and Text Annotations.
* **Smart Orthogonal Wiring:** Color-coded conductor potentials (`L1`, `L2`, `L3`, `N`, `PE`, `C1`, `DC+`, `DC-`) with automatic junction dots, vertex/segment dragging, and terminal attachment tracking when rotating or moving components.
* **Properties Inspector:** Customize device tags (linking coils to contacts/poles automatically), timer delays, indicator lamp colors, terminal pin markings, rotation angles (`0°`, `90°`, `180°`, `270°`), and labels.
* **Project Persistence:** Export and import complete schematics as JSON files, with full Undo/Redo history support.

### 🎛️ Real-Time Electrical Simulation Engine
* **Live Circuit Solving:** Graph-based electrical potential propagation with real-time wire energization highlighting.
* **Motor Direction & Configuration Detection:**
  * Detects **CW / CCW** phase rotation (`L1-L2-L3` vs. reversed phase sequence) on 3-phase motors.
  * Supports **Star (`Y`)** and **Delta (`Δ`)** winding configurations on 6-pin 3-phase motors.
  * Simulates DC motor polarity reversal (`CW` / `CCW`).
* **Short-Circuit Protection & Alerts:** Automatically detects and halts simulation on Phase-to-Phase (`L1 ↔ L2`), Phase-to-Neutral/Earth, or DC `+24V` to `0V/PE` short circuits.
* **Interactive Controls & Audio Feedback:** Operate push buttons (momentary press-and-hold), toggle breakers, or trip thermal overloads live during simulation, complete with synthesized mechanical click and buzzer audio effects via Tone.js.

### 📱 Responsive & Touch-Friendly Design
* Built with **HTML5 Canvas**, **Tailwind CSS**, and **Vanilla JavaScript** with zero build steps required.
* Supports desktop mouse/keyboard workflows as well as mobile/tablet touch gestures (pinch-to-zoom, two-finger/background panning, and bottom-sheet property inspection).
* Includes Dark Mode and Light Mode themes.

---

## 🚀 Getting Started

### Running Online
Visit the hosted web application directly at:
**[https://jeffry-lacanglacang.github.io/Motor-Control-Simulator/](https://jeffry-lacanglacang.github.io/Motor-Control-Simulator/)**

### Running Locally
Because the simulator is self-contained in a single `index.html` file:
1. Clone the repository:
   ```bash
   git clone https://github.com/jeffry-lacanglacang/Motor-Control-Simulator.git
   ```
2. Open `index.html` in any modern web browser (Chrome, Edge, Firefox, Safari).

---

## 🛠️ Usage Guide

1. **Place Components:** Open the **Resources Palette** (top-left menu icon) and click/tap any IEC symbol to place it onto the grid.
2. **Assign Device Tags:** Select a component and open the **Inspector** (top-right). Assign matching tags (e.g., `KM1`) to link a contactor coil with its main power poles and auxiliary contacts.
3. **Draw Wires:** Switch to the **Wire Tool (`W`)** or click directly on any component terminal pin. Select the desired wire potential (`L1`, `L2`, `L3`, `N`, `C1`, etc.) from the top toolbar and click another terminal or double-click to finish a conductor run.
4. **Simulate:** Click **Simulate** in the top toolbar to energize the circuit. Click or hold switches, push buttons, breakers, and overload relays on the canvas to test your control logic.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| `V` | Switch to Select & Move tool |
| `W` | Switch to Draw Wire tool |
| `R` | Rotate selected component `90°` |
| `Ctrl + D` / `Cmd + D` | Duplicate selected component |
| `Delete` / `Backspace` | Delete selected component or wire |
| `Ctrl + Z` / `Cmd + Z` | Undo last action |
| `Ctrl + Y` / `Cmd + Y` | Redo action |
| `Space + Drag` | Pan across the canvas |
| `Mouse Wheel` | Zoom in / out |
| `Esc` / `Right-Click` | Cancel active wire drawing or clear selection |

---

## 📄 License

[LICENSE](LICENSE)

---

## 📬 Contact

**Developer:** Jeffry Lacanglacang  
**Email:** [jeffrylacanglacang@gmail.com](mailto:jeffrylacanglacang@gmail.com)  
**Project Page:** [https://jeffry-lacanglacang.github.io/Motor-Control-Simulator/](https://jeffry-lacanglacang.github.io/Motor-Control-Simulator/)