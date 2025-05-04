# 📈 Ethereum Price Tracker Chainlink dApp

A fully decentralized application (dApp) that allows users to fetch and store the current price of Ethereum (ETH) using the **Chainlink ETH/USD Data Feed**. Built using Solidity smart contracts, deployed to the Sepolia testnet, and connected to a React frontend via Ethers.js.

## 🚀 Features

- ✅ Retrieve real-time Ethereum price from Chainlink oracles.
- ✅ Store the latest ETH/USD price on-chain.
- ✅ Interact with the contract via a user-friendly React interface.
- ✅ MetaMask wallet integration for secure transaction signing.

---

## 🧱 Architecture Overview

- **Smart Contract (Solidity)**  
  Stores the latest ETH/USD price retrieved from the Chainlink data feed.

- **Frontend (React + Ethers.js)**  
  Connects to the deployed contract, fetches the price, and allows users to trigger on-chain storage.

- **Deployment**  
  - Smart contracts deployed using [Foundry](https://book.getfoundry.sh/).
  - Frontend bootstrapped using `create-react-app`.

---

## 🛠️ Tech Stack

| Layer          | Technology                          |
|----------------|--------------------------------------|
| Blockchain     | Ethereum Sepolia Testnet            |
| Oracle         | Chainlink ETH/USD Data Feed         |
| Smart Contract | Solidity                            |
| Deployment     | Foundry (Rust-based)                |
| Frontend       | React.js                            |
| Wallet         | MetaMask                            |
| Web3 Library   | Ethers.js v5.7.2                    |
| Styling        | Bootstrap                           |

---

## 📂 Project Structure

```

chainlink-dapp-example/
├── backend/
│   ├── src/
│   │   └── PriceConsumerV3.sol
│   ├── script/
│   │   └── DeployPriceConsumer.s.sol
│   ├── .env
│   └── foundry.toml
└── frontend/
├── src/
│   └── App.js
└── public/

````

---

## ⚙️ Setup Instructions

### Prerequisites
- Node.js
- Rust (for Foundry)
- MetaMask extension
- Fuji RPC URL

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ethereum-price-tracker-dapp.git
cd ethereum-price-tracker-dapp
````

### 2. Backend (Smart Contracts)

```bash
cd backend
forge install smartcontractkit/chainlink-brownie-contracts
forge init
```

Update `.env` with:

```
PRIVATE_KEY=your_private_key
FUJI_RPC_URL=https://sepolia.infura.io/v3/YOUR_INFURA_KEY
```

Compile and deploy:

```bash
forge compile
forge script script/DeployPriceConsumer.s.sol --broadcast
```

Note the deployed contract address.

### 3. Frontend

```bash
cd ../frontend
npm install bootstrap ethers@5.7.2
```

Update `App.js` with the deployed contract address and ABI.

Start the app:

```bash
npm start
```

---

## 💡 Learnings

Through this project, I learned about:

* Building and deploying smart contracts with Foundry.
* Consuming Chainlink oracles.
* Web3 frontend integration with Ethers.js.
* Managing testnet transactions with MetaMask.

---

## 🧪 Test Network

* **Network**: Sepolia Testnet
* **Contract Address**: `0xYourDeployedAddress` *(replace this with your actual address)*

---

