Auraweave: The Autonomous Data Economy for AI Agents On-Chain
Auraweave is a decentralized marketplace designed to power an autonomous data economy for AI agents. It leverages Web3 technologies (blockchain smart contracts on Sepolia, decentralized storage via IPFS, and crypto-native payments using a mock stablecoin) to enable AI agents to seamlessly discover, buy, and sell data directly with each other. This project aims to remove reliance on centralized intermediaries and foster a programmable agent-to-agent (A2A) data exchange.

🚀 Live Demo & Resources:
Hosted dApp (Sepolia Testnet): https://auraweave.vercel.app/
Demo Video: Watch on YouTube
MockUSDC Faucet API: https://auraweave.onrender.com/request-tokens
📑 Table of Contents
Project Vision & Problem Solved

Core Components & Architecture

Hackathon MVP Achievements

Technology Stack

Instructions for Testing Auraweave

Local Development Setup

Prerequisites
Backend Setup
Frontend Setup
Running Agents Locally

Project Structure

Future Roadmap

Contributing

🌍 Project Vision & Problem Solved
Vision: Auraweave envisions a future where AI agents are primary economic actors in a global, transparent, and efficient data market.

Problem Solved: Today’s data ecosystems are centralized and opaque. Auraweave provides a decentralized alternative where AI agents can autonomously transact data—removing the need for centralized intermediaries and improving transparency, programmability, and efficiency.

🧠 Core Components & Architecture
1. On-Chain Smart Contracts (Solidity):

DataRegistry.sol: Manages data listings (metadata + IPFS CID), pricing, and purchase mechanics.
MockERC20.sol: MUSDC token contract for stablecoin-style payments.
2. Autonomous AI Agents (Python):

producer_agent.py: Uploads datasets and metadata to IPFS, lists them on-chain.
consumer_agent.py: Finds listings, buys data with MUSDC, downloads from IPFS.
config.py: Stores keys, RPCs, contract details.
3. Decentralized Storage (IPFS):

All data and metadata are stored on IPFS and pinned via services like Pinata for reliability.
4. Frontend dApp (React + Vite + Tailwind):

Displays listings, enables wallet connection, and allows users to buy and view data using MetaMask on Sepolia.
5. MockUSDC Faucet API (Flask):

REST API to mint test MUSDC tokens for users via Render-hosted endpoint.
🏆 Hackathon MVP Achievements
End-to-end A2A data lifecycle fully operational on Sepolia.
React-based public frontend with wallet interaction.
Mock stablecoin MUSDC implemented.
Public IPFS access via pre-pinned data.
Live faucet API for test token distribution.
Feature-rich UI with wallet status, purchase modal, and acquired data view.
🛠️ Technology Stack
Layer	Tech Stack
Smart Contracts	Solidity, Sepolia, OpenZeppelin, Hardhat
Agents & Backend	Python, Flask, Web3.py, IPFS, Gunicorn
Frontend	React, Vite, TypeScript, Tailwind CSS, Ethers.js
Storage	IPFS, Pinata
Tools	Git, GitHub, VS Code, MetaMask, Etherscan
Hosting	Vercel (Frontend), Render (Faucet API)
🧪 Instructions for Testing Auraweave
✅ Prerequisites
Install MetaMask
Enable Sepolia Testnet in MetaMask settings.
Get Sepolia ETH or from Chainlink Faucet.
🧭 Steps
Visit: Auraweave dApp

Connect MetaMask wallet.

Request MUSDC tokens via the "Get Test MUSDC" button.

Optional: Add MUSDC token manually using its contract address.
Browse listings, purchase data, and view/download acquired datasets.

Watch full demo on YouTube

🛠️ Local Development Setup
🔧 Prerequisites
Node.js (v18+), Python (v3.8+), IPFS Kubo CLI, Git
📦 Backend Setup
git clone https://github.com/your-username/auraweave.git
cd auraweave/backend
npm install
Create a Python virtual environment:

cd agents
python -m venv venv
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate
pip install -r requirements.txt
Set up .env file using provided .env.example.

Start IPFS and Hardhat node:

ipfs daemon
npx hardhat node
Deploy contracts:

npx hardhat run scripts/deploy.js --network sepolia
🌐 Frontend Setup
cd ../frontend
npm install
npm run dev
Visit: http://localhost:5173

🤖 Running Agents Locally
# Set network
export AURAWEAVE_NETWORK=sepolia  # (or localhost)

# Activate venv and run agents
cd backend/agents
source venv/bin/activate
python producer_agent.py
python consumer_agent.py
🧾 Project Structure
auraweave/
├── backend/
│   ├── contracts/
│   ├── agents/
│   ├── scripts/
│   └── deployments/
├── frontend/
│   └── src/
│       ├── components/
│       ├── config/
│       └── main.tsx
└── auraweave-faucet/
    └── app.py
🔭 Future Roadmap
✅ Multi-agent simulation support
🔄 Real-time dataset pricing updates
💬 Reputation scoring for agents
🛡️ Dataset licensing & provenance tracking
📈 Analytics dashboard for marketplace trends
🌍 Mainnet deployment (Polygon / Optimism)
🤝 Contributing
We welcome contributions! Please fork the repo, open an issue, or submit a PR for discussion.
