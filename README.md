# Crypto Exchange

Crypto Exchange is a decentralized exchange (DEX) built on top of Uniswap V3 protocol. It allows users to swap tokens, add liquidity to pools, and deploy new pools. The project utilizes a combination of Solidity for smart contracts, Foundry for development and deployment, and Next.js for the frontend.

## Features

- **Token Swapping**: Users can swap tokens using the Uniswap V3 protocol.
- **Liquidity Management**: Users can add or remove liquidity from existing pools.
- **Pool Deployment**: Users with the necessary permissions can deploy new pools.
- **Price Oracle**: The DEX integrates with Uniswap V3's price oracle to fetch accurate token prices.
- **Token Information**: Users can view detailed information about available tokens, including balances, symbols, and names.
- **Liquidity Data**: The DEX provides comprehensive liquidity data for all user-created pools.
- **Top Tokens**: The DEX displays a list of the top 10 tokens by trading volume.

## Architecture

The project consists of two main components:

### Backend (Solidity Contracts and Deployment Scripts)

- Contract Deployment: Deploys core Uniswap V3 contracts (Factory, SwapRouter, NFTDescriptor, etc.) and links libraries.
- Token Deployment: Deploys sample ERC20 tokens and mints initial supply.
- Pool Deployment: Creates Uniswap V3 pools and adds initial liquidity.
- Liquidity Checking: Fetches and displays the current state of deployed pools.

### Frontend (Next.js Components)

- Liquidity Management: Handles adding liquidity to Uniswap V3 pools using Web3Modal for wallet connection.
- App Features: Provides utility functions for wallet connection and contract interactions.
- Liquidity Checking: Fetches and processes liquidity data from Uniswap V3 pools.
- Pool Deployment: Handles the deployment of new Uniswap V3 pools.
- Price Fetching: Fetches price data from Uniswap V3 pools using the Quoter contract.

## Prerequisites

- Node.js (v14+ recommended)
- npm or yarn
- MetaMask browser extension





## Deploying the Project Locally

1. Ensure you have [Foundry](https://github.com/foundry-rs/foundry) installed.
1. Install the dependencies:
    ```shell
    $ forge install
    $ cd ui && yarn
    ```
1. Run Anvil:
    ```shell
    $ make anvil
    ```
1. Set environment variables and deploy contracts:
    ```shell
    $ source .envrc
    $ make deploy
    ```
1. Start the UI:
    ```shell
    $ cd ui && yarn start
    ```
1. In Metamask, import this private key and connect to `localhost:8545`:
    ```
    0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80
    ```
