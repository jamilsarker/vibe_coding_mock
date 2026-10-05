# Smart Escape - Interactive Evacuation Route Simulator

**AI DevFest Mock Test Solution**

[![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen?style=for-the-badge&logo=github)](https://jamilsarker.github.io/vibe_coding_mock/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)
[![Made with](https://img.shields.io/badge/Made%20with-JavaScript-yellow?style=for-the-badge&logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

---

## 🚀 Live Demo

### 🌐 **[Click Here to Open Live Demo](https://jamilsarker.github.io/vibe_coding_mock/)**

> **✅ Live Site:** The application is deployed and ready to use!

### 💻 Local Testing:
If you want to run locally, simply open `index.html` in your browser (Chrome recommended).

**Quick Start:**
1. Open the live demo link above (or local file)
2. Click "Import Building Data" button
3. Select the `building.json` file
4. Select R1 as starting point
5. Try blocking C2 to see route recalculation! ✨

---

## 👤 Developer Information

- **Name**: Jamil Sarker
- **Registration Number**: [Your Registration Number]
- **GitHub Repository**: https://github.com/jamilsarker/vibe_coding_mock
- **Live Website**: https://jamilsarker.github.io/vibe_coding_mock/
- **Final Commit ID**: [Run `git rev-parse --short HEAD` before final submission]

> **✏️ Note:** Update your registration number and final commit ID before submission.
---

## 📖 Project Description

Smart Escape is an interactive browser-based evacuation route simulator that visualizes building layouts and computes optimal escape routes. The application dynamically recalculates paths when hazards (blocked rooms, corridors, or closed exits) change in real-time.

### Key Features:
- **Interactive Map Visualization**: Displays nodes (rooms, junctions, exits) and weighted corridors
- **Shortest Path Algorithm**: Dijkstra's algorithm implementation for optimal route finding
- **Dynamic Hazard Management**: Real-time route recalculation when conditions change
- **Bilingual Interface**: Full support for English and Bangla (বাংলা)
- **Smooth Animations**: Visual feedback for selections, route updates, and hazard toggles
- **Responsive Design**: Works on desktop and mobile devices

---

## 🛠️ How to Run

### Option 1: Direct Browser
1. Download or clone this repository
2. Open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari)
3. Click "Import Building Data" and select `building.json`
4. Start exploring routes!

### Option 2: Local Server
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx http-server

# Then open http://localhost:8000
```

---

## 📋 Implemented Features

### ✅ Mandatory Requirements
- [x] JSON import with comprehensive validation
- [x] Interactive map with node/edge visualization
- [x] Distinct visual styles for room/junction/exit types
- [x] Visible corridor costs on edges
- [x] Starting point selection (unblocked rooms/junctions only)
- [x] Shortest path calculation using Dijkstra's algorithm
- [x] Route display with path sequence, exit, and total cost
- [x] Block/unblock rooms and junctions
- [x] Block/unblock corridors
- [x] Close/reopen exits
- [x] Visual distinction for all hazard states
- [x] Immediate recalculation on any change
- [x] Reset to initial state functionality
- [x] "No route available" error handling
- [x] "Starting location blocked" warning
- [x] Full bilingual support (English + Bangla)

### ✅ Routing Rules Compliance
- [x] Cost calculated as sum of edge costs (not coordinates or corridor count)
- [x] Exclusion of blocked nodes and incident edges
- [x] Exclusion of blocked edges
- [x] Exclusion of closed exits (including as intermediate nodes)
- [x] Minimum cost exit selection
- [x] Lexicographic tie-breaking for equal cost exits
- [x] Lexicographic tie-breaking for equal cost paths

### ✅ Visual & UX Features
- [x] Subtle animations for selections and updates
- [x] Smooth transitions without delays
- [x] High-contrast, modern UI design
- [x] Gradient backgrounds and shadows
- [x] Hover effects and visual feedback
- [x] Scrollable lists for large datasets
- [x] Canvas-based graph rendering
- [x] Legend for node/edge types

### 🎯 Bonus Features
- [x] Dark theme with modern aesthetics
- [x] Click-to-select nodes on canvas
- [x] Categorized hazard controls
- [x] Real-time visual feedback
- [x] Smooth color-coded route highlighting
- [x] Custom scrollbar styling
- [x] Responsive grid layout
- [x] Professional typography

---

## 🧪 Test Cases

All test cases from the problem statement pass successfully:

| Scenario | Action | Expected Result | Status |
|----------|--------|-----------------|--------|
| Baseline | Select R1 | R1 - C1 - C2 - E1; cost 7 | ✅ Pass |
| Blocked junction | Select R1; block C2 | R1 - C1 - C3 - C4 - E2; cost 11 | ✅ Pass |
| Exits closed | Select R1; close E1 and E2 | No route available | ✅ Pass |
| Different start | Select R2 | R2 - C3 - C4 - E2; cost 7 | ✅ Pass |
| Blocked start | Select R1; then block R1 | Starting location blocked | ✅ Pass |

---

## 🤖 AI Tools Used

### Primary AI Assistant: **Claude (Anthropic)**

**Most Useful Prompts:**
1. *"Implement Dijkstra's algorithm with lexicographic tie-breaking for equal cost paths in JavaScript"* - Generated the core pathfinding logic with proper tie-breaking rules
2. *"Create a bilingual UI toggle system for English and Bangla with all labels and messages"* - Set up the complete translation system
3. *"Design a modern dark theme UI with gradients, animations, and smooth transitions using vanilla CSS"* - Produced the visual styling and animations
4. *"Add canvas click handling to select nodes visually on the map"* - Implemented interactive node selection

---

## 🐛 Known Issues

- None currently identified
- Tested with sample data and various edge cases

---

## 📁 File Structure

```
.
├── index.html          # Main application (HTML + CSS + JavaScript)
├── building.json       # Sample building data
├── README.md          # This file
├── LICENSE            # MIT License
└── screenshots/
    ├── baseline.png   # Baseline route screenshot
    └── rerouting.png  # Rerouted after blocking C2
```

---

## 📸 Screenshots

### Baseline Route (R1 → E1, Cost: 7)
![Baseline](screenshots/baseline.png)

### Rerouting After Blocking C2 (R1 → E2, Cost: 11)
![Rerouting](screenshots/rerouting.png)

---

## 📜 License

MIT License - See [LICENSE](LICENSE) file for details

---

## 🙏 Acknowledgments

- AI DevFest organizers for the challenge
- Problem statement and sample data provided
- Built using vanilla HTML, CSS, and JavaScript (no external libraries)

---

## 📞 Contact

For questions or feedback, please reach out through the official submission form.
