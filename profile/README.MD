# PrediX - AI-Powered PvP Prediction Market

## Overview
PrediX is an AI driven, prompt-based PvP prediction market built on the Solana blockchain. The platform enhances reliability through decentralized smart contract logic, real-time oracle data, and AI powered automation for market creation, resolution, and payouts. PrediX enables users to create and participate in prediction markets seamlessly, leveraging Solana's high-speed, low-cost transactions, and now features cross-chain capabilities through Wormhole integration.

---
<p align="center">
  <img src="https://predix-dev.s3.ap-northeast-2.amazonaws.com/Home%5Bconnect-wallet%5D_show-games.png" alt="Home - Show Games" width="45%" />
  <img src="https://predix-dev.s3.ap-northeast-2.amazonaws.com/chatting_.png" alt="Chatting" width="45%" />
</p>

---

## Key Features

### ✅ AI-Powered Prediction Markets
- AI agents automate market creation, answer selection, and resolution.
- Smart contracts ensure fair and transparent outcomes.
- Real-world data is retrieved from trusted API providers (e.g., `api-sports.io` for sports, OKX Wallet API for crypto).

### ✅ On-Chain Betting System on Solana
- Users bet on predefined outcomes in a decentralized environment.
- All transactions are recorded on-chain, ensuring transparency.
- Market resolution is fully automated using AI and on-chain governance.

### ✅ Cross-Chain Support via Wormhole
- Seamlessly move assets across multiple blockchains with Wormhole integration.
- Support for native USDC and other tokens through CCTP & Token Bridge.
- Secure settlement layer and cross-chain queries for reliable verification.
- Bet with tokens from different chains without manual bridging.

### ✅ Solana-Optimized Trading & Wallet System
- Users deposit SOL and other supported tokens into an embedded wallet to place bets.
- Integrated with Jupiter API for seamless swaps between SOL, altcoins, and meme coins.
- Cross-chain asset top-up and cash-out solutions.

### ✅ SocialFi & Community Engagement
- **PnL NFT Cards**: Users can mint and share performance-based NFTs via Metaplex.
- **In-App Chat & Networking**: Social features powered by TalkJS or Sendbird.
- **Blink Integration for X (Twitter) Interaction**: Create and join markets directly from X.

### ✅ Fast, Feeless Transactions
- Users can place bets with minimal transaction fees thanks to Solana's low-cost architecture.
- Optimized for real-time, high-frequency trading.

### ✅ AI-Powered Prompt System
- Users can interact with the platform through natural language commands:
  - _"Create a prediction for the Man City vs Tottenham match next week. Bet 1 SOL on Tottenham."_
  - _"Show me ongoing predictions."_
  - _"Join the second prediction with 2 SOL."_
  - _"Create a BTC price up/down prediction, starting today at 12 PM UTC, resolution in 48 hours. Bet 2 SOL on UP."_
  - _"List ongoing predictions by highest bet."_
  - _"Show my winning predictions and claim all rewards."_

---

## How PrediX Leverages Solana & Wormhole

### 🔹 High-Speed Transactions
- Solana’s high throughput enables real-time market creation and settlement.
- Low-latency transactions ensure instant bet placements and payouts.

### 🔹 Decentralized Smart Contracts
- Built with Anchor, Solana’s Rust-based smart contract framework.
- Fully automated resolution process with immutable on-chain verification.

### 🔹 Tokenized Economy with SPL Tokens
- Users deposit and withdraw funds using Solana’s SPL token standard.
- Rewards and payouts are distributed instantly without intermediaries.

### 🔹 Secure & Efficient Betting Mechanism
- Embedded wallets allow seamless onboarding for non-crypto users.
- Market outcomes are determined on-chain, ensuring fairness and transparency.

---

## Key Technologies
- **Programming Language**: Rust
- **Blockchain**: Solana
- **Smart Contract Framework**: [Anchor](https://project-serum.github.io/anchor/)
- **Oracles & APIs**:
  - [api-sports.io](https://api-sports.io/) (sports data)
  - [OKX Wallet API](https://www.okx.com/wallet-api) (crypto data)
- **Token Standards**:
  - SPL Tokens (`Token2022`)
  - `Associated Token Accounts`

---

## Environment Setup
Ensure the following environment variables are configured:
```env
RPC_URL=<your_sol_rpc_url>
PREDIX_PROGRAM_ID=<your_predix_smart_contract_address>
```

---

## Installation

### Clone the Repository
```bash
git clone <repository-url>
cd <repository-directory>
```

### Install Dependencies
```bash
anchor build
```

### Deploy Smart Contracts
```bash
anchor deploy
```

---

## Usage

### 📌 Placing a Prediction Bet
```rust
let result = bet(ctx, answer_key, amount);
```

### 📌 Creating a Prediction Market
```rust
let result = create_market(ctx, market_key, answer_keys);
```

### 📌 Claiming Rewards
```rust
let result = claim_token(ctx);
```

---

## Governance & Security
### 🔹 Fair Play & Anti-Manipulation Measures
- AI verification for prediction integrity.
- Strict security policies to prevent market manipulation.

### 🔹 User Protection & Compliance
- Embedded wallet security mechanisms.
- Adheres to DeFi best practices for transparent financial operations.

### 🔹 Policy Updates & Community Governance
- Regular policy reviews based on user feedback.
- Transparent governance with community-driven updates.

---

## Wormhole SDK
🔹 Cross-Chain Token Transfers with Token Bridge & CCTP
Integrated Wormhole Token Bridge and CCTP (Circle Cross-Chain Transfer Protocol) to support native USDC and other wrapped assets across supported chains.

Users can deposit and wager using tokens from chains like Ethereum, Base, BNB, Arbitrum, Optimism, and more.

Transfers are initiated via the PrediX Agent and relayed to Solana using VAA (Verified Action Approval) messages handled by Wormhole’s core infrastructure.

🔹 Cross-Chain Settlement Layer & Queries
Utilizes Wormhole's Query and Settlement Layer to validate and verify transactions from source chains in real time.

Enables automated resolution of PvP markets where the wagered token originates from a different chain.

Provides proof-of-origin and finality checks to ensure trustless cross-chain settlement.

🔹 Wormhole SDK via PrediX Agent (AI Control Layer)
Wormhole SDK functions are abstracted through the PrediX AI Agent, allowing users to interact with cross-chain features using natural language prompts.

“Bridge 20 USDC from Base to Solana and place a bet.”

“Withdraw winnings to my Ethereum wallet.”

Wormhole’s cross-chain functions are exposed as AI-callable operations using an internal wrapper around Wormhole SDK APIs.

🔹 Upcoming: Chain-vs-Chain Wagering
Infrastructure is being expanded to support Chain-vs-Chain PvP prediction matches:

e.g., Solana users vs Base users betting on major events using native assets.

Wormhole SDK ensures trustless interaction and resolution across different L1/L2 ecosystems.

🔹 Security and Monitoring
VAAs and cross-chain events are tracked using Wormhole SDK event listeners and verified using the Guardians network.

Ensures tamper-proof cross-chain operations for all token flows and settlement processes.

- txHash : https://wormholescan.io/#/tx/0x6bcd4e8e89a8b89427aa1ec083e724a2f7ed6eddcc3e6cdf648699390a5ffde6?network=Testnet

---

## Business Model
PrediX operates on a sustainable revenue model through transaction-based fees and SocialFi partnerships:

### 🔹 Market Resolution Fee
- A **3% fee** is deducted from the total payout of completed predictions to sustain platform operations.

### 🔹 SocialFi Engagement & Ads
- Sponsored prediction markets.
- In-app chat monetization through integrated promotions.

---

## Contribution
Contributions are welcome! Feel free to open issues and submit pull requests.

---

## License
This project is licensed under the MIT License.
