# 🛡️ Fake Product Identification System

A decentralized web application (dApp) that allows users to verify the authenticity of products using Ethereum blockchain and smart contracts. This system prevents counterfeit products by storing original product records immutably on the blockchain.

---

## 📌 Features

- Admin (deployer) can add genuine products to the system.
- Users can verify if a product is authentic by entering the Product ID.
- All product data is stored immutably on the blockchain.
- Only the admin (the deployer address) can add new products.

---

## 🚀 Getting Started

### ✅ Prerequisites

- [MetaMask](https://metamask.io/) browser extension
- [Remix IDE](https://remix.ethereum.org/) for writing and deploying smart contracts
- [Ganache](https://trufflesuite.com/ganache/) to simulate a local Ethereum blockchain
- Web3.js already included in your HTML (via CDN)

---

## 🛠️ Deployment Steps

### 1. Start Ganache

- Launch Ganache and start a new workspace.
- Copy the **private key** of one account (this will be the **admin**).
- Note the **RPC URL** (e.g., `http://127.0.0.1:7545`).

### 2. Setup MetaMask

- Open MetaMask.
- Import the **admin** account using the private key from Ganache.
- Add a custom network in MetaMask with Ganache's RPC URL.
- Select this account in MetaMask to use for deploying.

### 3. Compile & Deploy `ProductVerification.sol`

- Open [Remix IDE](https://remix.ethereum.org/).
- Paste the `ProductVerification.sol` smart contract in a new file.
- Set the compiler version to **0.8.14**.
- Compile the contract.
- Go to the **"Deploy & Run Transactions"** tab:
  - Set the **Environment** to `Injected Web3`.
  - Choose the Ganache-imported admin account from MetaMask.
  - Click **Deploy**.

---

## 📥 Integrate with Frontend (Important)

After successful deployment in Remix:

### 🔹 Copy ABI

1. Go to the **"Compilation" tab**.
2. Expand the contract dropdown.
3. Click on the **"ABI" copy icon**.
4. Paste this into the `script.js` like this:
   ```js
   const contractABI = [PASTE_HERE];
