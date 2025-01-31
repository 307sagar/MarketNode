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
- Select Environment - 'walletConnect'
- Verify the connect wallet address
- Under DEPLOY section -
- Add Name,symbol as UPPERCASE.(no breaks allowed in name)
- Add CAP,INITIALSUPPLY - Based on gas supported by the wallet connected, add these values.Start with low values (E.g CAP - 5000000000000000000 , INITIALSUPPLY - 4000000000000000000 as gwei)
- Click transact
- At the bottom section, go to Deployed/Unpinned contracts - Copy the deployed contract address
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
- Connect metamask wallet
- It should display all the Token parameters
- The transfer, mint functions should be working in sync with metamask wallet as well.
- Added functionalities like blacklist address, owner display, pause/unpause contracts should be working expectedly.


## NOTE
- Testing framework to be implemented - CHAI preferably
- Blockchain development infrastructure to be implemented - upgraded to HARDHAT preferably
