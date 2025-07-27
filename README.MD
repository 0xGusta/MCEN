# MonChat

MonChat is a real-time, decentralized chat application built on the Monad blockchain. It allows users to connect their Web3 wallets, create a profile, and communicate with others in a public chatroom. All messages are stored on-chain, providing a transparent and persistent communication platform.

## Features

* **Real-Time Messaging:** Send and receive messages instantly.
* **Multimedia Support:** Share text messages, images (via IPFS/Pinata), and GIFs (via Tenor API).
* **Web3 Integration:** Connect securely with your favorite wallet using Wagmi and Reown AppKit.
* **User Profiles:** Register a unique username and set a profile picture.
* **Message Interactions:** Reply to, edit, and delete your messages.
* **User Presence:** See who is online and when they are typing, powered by Multisynq's `react-together` hook.
* **Token Transfers:** Send MON tokens directly to other users within the chat.
* **Game Challenges:** Challenge other online users to a game of Tic-Tac-Toe or Tetris.
* **Moderation:** Owner and moderator roles with the ability to ban/unban users and manage moderator lists.
* **On-Chain Data:** All messages and user profiles are stored publicly on the Monad Testnet blockchain.

## Tech Stack

* **Frontend:** React, Vite, Tailwind CSS
* **Blockchain Interaction:** Ethers.js, Wagmi, Viem
* **Wallet Connection:** Reown AppKit
* **Real-time State:** React Together (using Multisynq)
* **Decentralized Storage:** IPFS via Pinata for image uploads
* **APIs:** Tenor for GIFs, TimeZoneDB for presence time synchronization

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

* Node.js (v18 or higher recommended)
* pnpm package manager

### Installation

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/0xGusta/mcen.git](https://github.com/0xGusta/mcen.git)
    cd mcen
    ```

2.  **Install dependencies:**
    ```sh
    pnpm install
    ```

3.  **Set up environment variables:**
    Create a `.env` file in the root of the project by copying the example file:
    ```sh
    cp .env.example .env
    ```
    You will need to add your own API keys and project IDs to the `.env` file. See the [Environment Variables](#environment-variables) section below for more details.

4.  **Run the development server:**
    ```sh
    pnpm dev
    ```
    The application will be available at `http://localhost:5173` (or another port if 5173 is in use).

## Environment Variables

To run this project, you will need to add the following environment variables to your `.env` file. These are sourced from various services required for the app's functionality:

* `VITE_MULTISYNQ_APP_ID`: Your application ID from [Multisynq](https://multisynq.io/) for real-time presence and gaming features.
* `VITE_PROJECT_ID`: Your project ID from [Reown AppKit](https://dashboard.reown.com/) for wallet connectivity.
* `VITE_PINATA_API_KEY`: Your API key from [Pinata](https://app.pinata.cloud/) for pinning images to IPFS.
* `VITE_PINATA_SECRET_KEY`: Your secret API key from Pinata.
* `VITE_TENOR_API_KEY`: Your API key from [Google Tenor](https://developers.google.com/tenor/guides/quickstart) for GIF integration.
* `VITE_TIMEZONEDB_API_KEY`: Your API key from [TimeZoneDB](https://timezonedb.com/api) for accurate user presence timestamps.

## About The Project

This is an open-source project developed by [0xGus](https://x.com/0xGustavo). It is an independent project and is not officially affiliated with the Monad team.

* The smart contract is deployed on the Monad Testnet and can be viewed on the [MonVision](https://testnet.monadexplorer.com/address/0xA625578F0C4E3c1d367D87e17157b5c7dD056e9F?tab=Contract) or in [GitHub](https://github.com/0xGusta/MCContract)

Please be aware that all messages are public and permanently recorded on the blockchain. Do not share sensitive information.