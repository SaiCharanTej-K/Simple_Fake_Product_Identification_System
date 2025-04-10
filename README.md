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
- ![image](https://github.com/user-attachments/assets/40d59427-21c2-4f41-863c-19a1ebdd65dc)

- Compile the contract.
- Go to the **"Deploy & Run Transactions"** tab:
  - Set the **Environment** to `Injected Web3`.
  - Choose the Ganache-imported admin account from MetaMask.
  - Before Deploying at address mention the imported account -admin account to deploy
![image](https://github.com/user-attachments/assets/6716a3f9-ac70-4ae3-838f-b17fa24bdf5e)

  - Click **Deploy**.

---

## 📥 Integrate with Frontend (Important)

After successful deployment in Remix:

### 🔹 Copy ABI

![image](https://github.com/user-attachments/assets/1a2df435-be3b-456b-bdbf-68287506cac0)

1. Go to the **"Compilation" tab**.
2. Scroll down the compiling tab left side and on the bottom we can find abi code
![image](https://github.com/user-attachments/assets/d2f6e851-b776-41f3-80e3-e02bf3f200fb)


3. Click on the **"ABI" copy icon**.
4. Paste this into the `script.js` like this:
   ```js
   const contractABI = [PASTE_HERE];

5. And in Deployment Tab we can find  contract address copy the  address and paste in script.js


   ![image](https://github.com/user-attachments/assets/42254f4f-f2e5-4d44-9134-b09f07e1f132)

   ![image](https://github.com/user-attachments/assets/f82e1922-1c52-482b-bb8c-e0d519e66c7e)

6. And finally run it using open with Live Server in VS Code.

![image](https://github.com/user-attachments/assets/8b0a7e29-58e1-4b59-a13e-45a4fb9a787e)

