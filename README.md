📌 Overview
AI Maze Solver PRO is a Python desktop application that brings two foundational AI search algorithms to life through real-time step-by-step animation. Draw your own maze, watch BFS and DFS compete, and then route between real cities on an interactive map — all without spending a rupee on APIs.
Built as a university AI course project by students of BS Computer Science, NTU (Session 2024–2028).

✨ Features

🎨 Interactive 20×20 Grid — Draw walls, set start/end points, or generate a random maze with one click
🔵 BFS Visualization — Watch the shortest path emerge as BFS expands outward in waves
🟣 DFS Visualization — See DFS dive deep and backtrack, illustrating why it doesn't guarantee the shortest path
📊 Live Statistics — Real-time display of cells visited, path length, and execution time
🗺️ Real Map Routing — Enter any two city names and get actual road distance, drive time, and straight-line distance
🌍 Interactive HTML Map — Animated multi-route Folium map rendered in your browser with custom JavaScript
⚡ Adjustable Speed — Slider control from slow-motion to rapid visualization
🧵 Multi-threaded — UI stays fully responsive during algorithm execution and API calls
🌑 Dark Mode UI — GitHub-inspired dark color palette




🚀 Getting Started
Prerequisites

Python 3.8 or higher
pip

Installation
bash# Clone the repository
git clone https://github.com/AliCodes-p/ai-maze-solver-pro.git
cd ai-maze-solver-pro

# Install dependencies
pip install requests numpy folium

Note: tkinter comes bundled with Python. No API keys are needed — ever.

Run
bashpython projectAI.py

🎮 How to Use
Maze Solver

Select a Drawing Mode from the left panel (Wall, Erase, Start Point, End Point)
Click and drag on the grid to build your maze
Or click Random Maze to auto-generate one
Choose BFS or DFS and adjust the speed slider
Hit ▶ SOLVE and watch the algorithm work

Real Map Routing

Enter two city names in the right panel (e.g., Lahore, Pakistan → Karachi, Pakistan)
Click 🗺 Find Route + Map to get road distance and drive time
Click 🌍 Open Interactive Map to launch an animated Folium map in your browser


🛠️ Tech Stack
ComponentTechnologyLanguagePython 3.8+GUItkinter / ttkGrid DataNumPyGeocodingNominatim (OpenStreetMap)Road RoutingOSRM (Open Source Routing Machine)Map RenderingFolium + Leaflet.jsThreadingPython threading moduleDistanceHaversine formula
All external APIs are 100% free — no API key required.

📐 Algorithm Details
BFS — Breadth-First Search

Uses a collections.deque as a FIFO queue
Explores all nodes at distance N before advancing to N+1
Guarantees the shortest path
Better for finding optimal routes

DFS — Depth-First Search

Uses a Python list as a LIFO stack
Dives as deep as possible before backtracking
Does not guarantee the shortest path
Typically visits fewer cells but produces longer paths

Test Results (20×20 grid)
ScenarioBFS VisitedDFS VisitedBFS PathDFS PathEmpty grid220 cells47 cells39 steps71 stepsLight maze (15% walls)185 cells62 cells39 steps89 stepsMedium maze (28% walls)143 cells58 cells42 steps97 stepsDense maze (40% walls)89 cells34 cells48 stepsNot found

📁 Project Structure
ai-maze-solver-pro/
│
├── projectAI.py          # Main application (single-file architecture)
├── route_map.html        # Generated interactive map (auto-created on use)
└── README.md

🔮 Future Enhancements

 A* algorithm with Manhattan/Euclidean heuristics
 Dijkstra's algorithm for weighted grids
 Larger grid sizes (40×40, 100×100)
 Proper maze generation (Recursive Backtracker, Prim's, Kruskal's)
 Side-by-side BFS vs DFS split-screen comparison
 Traffic-aware routing via live API
 Mobile port using Kivy


👨‍💻 Authors
NameRoll NumberM Nouman Sajid24-NTU-CS-FL-1077M Ali24-NTU-CS-FL-1057M Hassan24-NTU-CS-FL-1067
Course: Artificial Intelligence — BS Computer Science, NTU (2024–2028)

📚 References

Russell, S. & Norvig, P. (2020). Artificial Intelligence: A Modern Approach (4th ed.) — Chapter 3
Nominatim API Documentation
OSRM HTTP API Documentation
Python tkinter Documentation
