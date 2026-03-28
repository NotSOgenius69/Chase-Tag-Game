# 🤖 AI Chase Tag Game

An interactive web-based game where two AI agents compete in a pursuit-evasion scenario. Watch as the chaser uses A* pathfinding to hunt down the evader, while the evader employs sophisticated behavioral AI to escape and survive.

<img width="1216" height="780" alt="Screenshot 2026-03-28 at 11 42 27 AM" src="https://github.com/user-attachments/assets/be1fb3d1-8a33-4521-bc65-5a4cd324c4ee" />

## 🎮 Live Demo

https://notsogenius69.github.io/Chase-Tag-Game/

## 📖 Overview

This project explores the fascinating world of adversarial AI in game development. Two AI agents take turns being the chaser and evader in 20-second rounds, demonstrating different algorithmic approaches to pursuit and evasion.

### Key Features

- **Intelligent Chaser AI**: Uses A* pathfinding algorithm for optimal pursuit
- **Strategic Evader AI**: Employs behavioral AI with:
  - Real-time threat assessment
  - Dead-end and corner detection
  - Escape route analysis
  - Strategic positioning
  - Wall-following behavior
- **Dynamic Gameplay**: Automatic role switching after each round
- **Obstacle Navigation**: Both agents navigate around walls and obstacles
- **Score Tracking**: Keeps track of wins for both players
- **Pure Vanilla JS**: No frameworks or dependencies required

## 🎯 How It Works

### Chaser Strategy (A* Pathfinding)
The chaser uses the A* algorithm to find the optimal path to the evader:
- Calculates shortest path considering obstacles
- Updates path in real-time as evader moves
- Efficient grid-based pathfinding

### Evader Strategy (Behavioral AI)
The evader uses a sophisticated multi-layered behavioral system:

1. **Situation Analysis**: Evaluates current danger level and available escape routes
2. **Position Safety Evaluation**: Checks for dead ends, corners, and open space
3. **Behavioral Selection**:
   - **Emergency Dodge**: When chaser is very close (< 60px)
   - **Dead End Escape**: When trapped with ≤2 escape routes
   - **Strategic Positioning**: When safe, moves to positions with maximum escape options
   - **Smart Evasion**: Normal mode with predictive movement

4. **Scoring System**: Evaluates potential moves based on:
   - Number of escape routes
   - Distance from boundaries
   - Open space availability
   - Distance from chaser
   - Trap avoidance

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- No additional dependencies required!

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/ai-chase-tag-game.git
```

2. Navigate to the project directory:
```bash
cd ai-chase-tag-game
```

3. Open `index.html` in your web browser:
```bash
# On macOS
open index.html

# On Linux
xdg-open index.html

# On Windows
start index.html
```

Or simply drag and drop `index.html` into your browser.

## 🎲 Game Rules

1. **Objective**: 
   - **Chaser**: Tag the evader before time runs out
   - **Evader**: Avoid being tagged for 20 seconds

2. **Scoring**:
   - Chaser wins if they tag the evader
   - Evader wins if they survive 20 seconds

3. **Role Switching**: After each round, players switch roles automatically

4. **Victory**: First to 5 wins (game ends automatically)

## 🛠️ Technical Implementation

### Technologies Used

- **HTML5 Canvas**: For rendering the game
- **Vanilla JavaScript**: Game logic and AI algorithms
- **CSS3**: Styling and UI design

### Core Algorithms

#### A* Pathfinding (Chaser)
```javascript
// Simplified A* implementation
f(n) = g(n) + h(n)
- g(n): Cost from start to node n
- h(n): Heuristic (Euclidean distance to goal)
```

#### Behavioral AI (Evader)
```javascript
// Multi-layered decision system
1. Analyze current situation
2. Evaluate position safety
3. Generate movement candidates
4. Score each candidate
5. Execute best move
```

### Project Structure
```
ai-chase-tag-game/
│
├── index.html          # Main HTML file with embedded CSS and JavaScript
├── README.md           # This file
├── screenshot.png      # Game screenshot (add your own)
└── LICENSE             # License file (optional)
```

## 📊 AI Learning Journey

### Initial Approach (Failed ❌)
- Used A* for both chaser and evader
- **Problem**: Evader kept getting trapped in corners
- **Why**: A* is designed for single-agent shortest path, not adversarial scenarios

### Solution (Success ✅)
- Kept A* for chaser (works great for pursuit)
- Implemented behavioral AI for evader with:
  - Spatial awareness
  - Trap detection
  - Strategic decision making
  - Real-time adaptation

### Key Insight
> "A* finds the shortest path to a goal. But in adversarial games, the 'goal' is dynamic and the opponent is actively trying to counter you. Single-agent algorithms don't translate directly to multi-agent scenarios."

⭐ If you found this project interesting, please consider giving it a star!
