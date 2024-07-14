# Market_Node

This project is a comprehensive example of a blockchain application using Ethereum smart contracts for creating an ERC20 token. It consists of two main parts: the backend, which includes the smart contract development and deployment, and the frontend, a React application that interacts with the smart contract.

## Getting Started

To get started with this project, clone the repository to your local machine.

### Prerequisites

- Node.js and npm installed
- MetaMask browser extension for interacting with the Sepolia Ethereum network

### Backend Setup

1. Navigate to the `backend` directory.
2. Install dependencies with `npm install`.
3. Use Remix as the development and deployment environment. 
    3.1 Deploy the 'EnhanedToken.sol' - If issues arise 
     - Navigate to .deps/npm/@openzeppelin/contracts/token/ERC20/ERC20.sol - modify 'internal virtual'.
4. Launch Metamask or other wallets for launching environment.     
5. Connection to wallet
    5.1 Select Environment - 'walletConnect'
    5.2 Verify the connect wallet address
    5.3 Under DEPLOY section -
        5.3.1 Add Name,symbol as UPPERCASE.(no breaks allowed in name)
        5.3.2 Add CAP,INITIALSUPPLY - Based on gas supported by the wallet connected, add these values.Start with low values (E.g CAP - 5000000000000000000 , INITIALSUPPLY - 4000000000000000000 as gwei)
    5.4 Click transact
    5.5 At the bottom section, go to Deployed/Unpinned contracts - Copy the deployed contract address
6. Use the copied address to paste in 'server.js' file. (Example - const contractAddress = "copied address";)
7. Run 'npm start' in backend directory/path.          


### Frontend Setup

1. Navigate to the `frontend` directory.
2. Install dependencies with `npm install`.
3. Use the copied address in backend-setup #6, to add in 'app.js' file.(Example - const contractAddress = "copied address";)
4. Start the development server with `npm start`. This will launch the React app in your default browser.

## Usage

The frontend application allows users to interact with the ERC20 token smart contract. Users can transfer tokens, view their current token balance, and monitor token transfer events.


1. Once the front end is running
 1.1 Connect metamask wallet
 1.2 It should display all the Token parameters
 1.3 The transfer, mint functions should be working in sync with metamask wallet as well.
 1.4 added functionalities like blacklist address, owner display, paus/unpause contracts should be working expectedly.
