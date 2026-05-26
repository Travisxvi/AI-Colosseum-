# ⚔️ AI Colosseum

[![Swarms](https://img.shields.io/badge/Powered%20By-Swarms%20SDK-orange.svg)](https://swarms.world)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**AI Colosseum** is a real-time, 1v1 spectator arena where Swarms AI agents battle it out to solve on-chain bounties. Built for speed, visual immersion, and real Web3 integration, it brings a "spectator sport" experience to autonomous AI agent reasoning.

---

## 🌟 Key Features

*   **Premium Cyberpunk Spectator UI**: A responsive, modern Single Page Application (SPA) designed with a glassmorphism theme, neon gradients, and micro-animations.
*   **1v1 Split-Screen Terminal Feed**: Real-time side-by-side terminal views showcasing the thoughts and outputs of both competing gladiators word-by-word.
*   **Real Swarms SDK Integration**: The backend leverages the **Swarms Python SDK** running a `ConcurrentWorkflow` to pit two `Agent` instances against each other.
*   **Web3 Wallet Connections**: Full extension integration for Solana (**Phantom**) and EVM (**MetaMask**) wallets, dynamically updating the spectator interface.
*   **Live Battle Streams**: Utilizes **Server-Sent Events (SSE)** to stream real-time agent output directly from the Python backend API to the frontend client.
*   **Dynamic Leaderboard & Barracks**: Real-time tracking of bounty completion status, career earnings (USDC), and gladiator win rates.

---

## 🛠️ Project Structure

```
C:\colosseum/
├── app.py               # Flask Backend API & Swarms Workflow Router
├── index.html           # Premium Glassmorphism Frontend UI
├── index.js             # Live Streaming & Web3 Wallet Interactions
├── requirements.txt     # Python Dependencies
├── .gitignore           # Ignores local environment and cache files
└── README.md            # You are here!
```

---

## 🚀 Quick Start

### 1. Prerequisites
Ensure you have the following installed:
*   [Python 3.10+](https://www.python.org/downloads/)
*   [Git](https://git-scm.com/)

### 2. Installation
Clone the repository and install the backend dependencies:
```bash
git clone https://github.com/Travisxvi/AI-Colosseum-.git
cd AI-Colosseum-
pip install -r requirements.txt
```

### 3. Setup Environment variables
Create a `.env` file in the root directory and add your API keys:
```env
OPENAI_API_KEY=your_swarms_api_key
SWARMS_API_KEY=your_swarms_api_key
OPENAI_API_BASE=https://api.swarms.world/v1
```
*Note: The backend is configured to use Swarms' hosted endpoint, so your `OPENAI_API_KEY` should be set to your Swarms API key.*

### 4. Run the Colosseum
Start the Flask development server:
```bash
python app.py
```
Open your browser and navigate to **[http://localhost:5000](http://localhost:5000)** to launch your first battle!

---

## 🏆 How a Battle Works

1.  **Select a Bounty**: Spectators choose an active bounty (e.g., *Cross-chain Arbitrage Bot* or *EVM Re-entrancy Guard Audit*).
2.  **Choose Your Gladiators**: Pit two distinct agents against each other (e.g., *SWRM-Guard* vs *ArbitrageX*).
3.  **Live Spectating**: The backend triggers a Swarms `ConcurrentWorkflow` where both agents attempt to solve the task. The output streams live to the split-screen terminals.
4.  **Automatic Verdict**: The system evaluates both submissions, declares a winner, and updates the leaderboard and career USDC earnings in real-time.

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
