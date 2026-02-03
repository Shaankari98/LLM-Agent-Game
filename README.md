
# 🕹️ LLM‑Agent‑Game (Blockchain Full‑Stack Edition)

![Project Banner](https://img.shields.io/badge/Status‑Active‑brightgreen) ![Python 3.10+](https://img.shields.io/badge/Python‑3.10%2B‑blue) ![License‑MIT](https://img.shields.io/badge/License‑MIT‑yellow)

**LLM‑Agent‑Game** is a full‑stack, blockchain‑enabled game where **AI agents powered by Large Language Models (LLMs)** compete in a turn‑based environment and all moves/results are **recorded on‑chain** for transparency and verifiability.  

Each agent makes game decisions using LLM reasoning, the backend handles game state and API calls, the frontend shows real‑time progress and blockchain results, and smart contracts store final outcomes.

---

## 🚀 Features

- 🤖 **LLM‑Driven Agents** — Agents use natural language reasoning to decide actions.  
- 🕹️ **Turn‑Based Gameplay** — Simple interactive loop for agent actions.  
- ⛓️ **Blockchain Recording** — All game results saved on a testnet (e.g., Goerli / Polygon Mumbai).  
- 💻 **Full Stack** — React frontend + Node backend + Python AI + Solidity smart contracts.  
- 📊 **Leaderboard & Stats** — On‑chain history + frontend display.  
- 🧠 **Easy to Extend** — Add new strategies, UI pages, or AI models.

---

## 🛠️ Tech Stack

| Layer | Tech |
|-------|------|
| Frontend | React.js, Tailwind CSS, Ethers.js/Web3.js |
| Backend | Node.js, Express.js |
| Smart Contracts | Solidity + Hardhat |
| AI Agents | Python 3 + OpenAI GPT / any LLM API |
| Database (optional) | MongoDB / PostgreSQL |
| Deployment | Vercel/Netlify (frontend), Railway/Heroku (backend) |

## 🧠 Setup Smart Contracts
cd blockchain

# Install dependencies
npm install

# Compile contracts
npx hardhat compile

# Deploy to testnet
npx hardhat run scripts/deploy.js --network <your_network>


Save the deployed contract address in the .env for backend & frontend.

## 🌀 Backend Setup
cd backend
npm install


Create .env:

PORT=5000
CONTRACT_ADDRESS=your_contract_address
RPC_URL=https://<your_testnet_rpc>
PRIVATE_KEY=your_wallet_private_key


Start backend API:

npm run dev

⚛️ Frontend Setup
cd frontend
npm install


Update .env:

REACT_APP_RPC_URL=https://<your_testnet_rpc>
REACT_APP_CONTRACT_ADDRESS=your_contract_address


Run the frontend:

npm start

## 🐍 Python AI Agents

Install Python dependencies:

cd agents
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt


Add your LLM API key to .env:

OPENAI_API_KEY=your_api_key_here


Run agent simulation:

python run_game.py

## 🎮 How It Works

Frontend requests a new game session.

Backend initializes game & calls Python agent scripts.

Agents decide actions via LLM API.

Moves are returned to backend & verified.

Backend sends final results to smart contracts.

Frontend displays on‑chain results & leaderboard.

## 📊 Example Game Output
Turn 1: AgentAlpha moves to (2,3)
Turn 2: AgentBeta attacks AgentGamma
Scores → Alpha: 12 | Beta: 8 | Gamma: 3
Game Ended: Winner is AgentAlpha 🏆
TX Hash: 0xabc123...789def

## 📜 License

This project is licensed under the MIT License — see the LICENSE file for details.







