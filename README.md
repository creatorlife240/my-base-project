# my-base-project

This project is a simple decentralized guestbook application built on the **Base** network. It allows anyone to submit their name and a message to be stored permanently on the blockchain.

## 🚀 Features
* **Sign Messages:** Users can publish their names and messages to the blockchain.
* **View Messages:** Easily retrieve and display all entries (name, message, timestamp, and sender's address).
* **Blockchain-based:** Every entry is stored on-chain via a smart contract.

## 🛠 Technologies
* **Smart Contract:** Solidity (^0.8.20)
* **Blockchain:** Base (L2)
* **IDE:** Remix IDE

## 📜 Smart Contract Structure
The contract uses an `Entry` struct to store the following data:
- `address sender`: The wallet address of the person who sent the message.
- `string name`: The user's name.
- `string message`: The content of the message.
- `uint256 timestamp`: The time when the message was sent.

## ⚙️ How to Use (Remix IDE)
1. Open **[Remix IDE](https://remix.ethereum.org/)**.
2. Compile your `Guestbook.sol` file.
3. Go to the "Deploy & Run Transactions" tab.
4. Select **Injected Provider - MetaMask** as the Environment.
5. Deploy the contract to the **Base** network.
6. Once deployed, use the `signGuestbook` function to send a message and `getAllEntries` to verify it.

## 👤 Developer
Created by **creatorlife240**.
