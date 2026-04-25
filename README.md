# The DAOVerse

[![License: MPL 2.0](https://img.shields.io/badge/License-MPL%202.0-brightgreen.svg)](https://opensource.org/licenses/MPL-2.0)
[![ETHAmsterdam](https://img.shields.io/badge/ETHAmsterdam-Hackathon%20Winner-blueviolet)](https://ethglobal.com)
[![Polygon](https://img.shields.io/badge/Network-Polygon-8247e5)](https://polygon.technology)
[![IPFS](https://img.shields.io/badge/Storage-IPFS-65c2cb)](https://ipfs.io)

> A 3D Web & VR-enabled metaverse platform facilitating community onboarding & engagement for DAOs, NFT projects, and Web3 communities.

---

## Overview

The DAOVerse is a decentralized application (dApp) that enables Web3 communities — DAOs, NFT creators, and beyond — to **gamify and personalize the process** by which they onboard and incentivize new and existing community members. Built on top of Mozilla Hubs and A-Frame, it delivers an immersive 3D/VR environment accessible from any web browser, mobile device, or compatible VR headset.

Web3 communities today face fragmented onboarding: members are scattered across Telegram, Discord, Twitter, and other platforms with no clear engagement flow. The DAOVerse solves this by creating a single, tailored, gamified metaverse space where community culture, learning, bounties, and social connection all live together.

---

## Awards

Built at **ETHAmsterdam Hackathon**:

| Award | Sponsor |
|---|---|
| 💪 UX Prize | Web3Auth |
| 🥇 Best Use | Coinbase Wallet |
| 🥈 Best Use | Polygon |
| 📈 Projects with Huge Potential | Tatum |
| 🏊 IPFS/Filecoin Pool Prize | Protocol Labs |

---

## Features

### Gamified Onboarding
- Connect a wallet and select an avatar to enter the onboarding level
- Complete community-defined quests and missions to earn **POAP badges** (LEARN, EARN, PLAY)
- Automatically receive NFT rewards upon completing badge requirements
- Gate access to the full DAOVerse until minimum onboarding requirements are met

### Full DAOVerse Experience
- **Bounty Chest** — Community contributors post initiatives with DAO token rewards; members bid to earn
- **Community Area** — Wander with your avatar and meet fellow members and potential collaborators
- **Resources Area** — Share and discover links, media, and tools curated by the community
- **Event Area** — Attend live-streamed workshops and community events

### Wallet Integration
- **MetaMask** (Injected Connector)
- **WalletConnect** — Mobile wallet bridge
- **Coinbase Wallet** — WalletLink connector
- **Web3Auth** — Social login and email-based onboarding for users new to crypto

### 3D / VR Environment
- Full 3D and WebVR support via A-Frame and Mozilla Hubs
- Works in-browser, on mobile, and with compatible VR headsets (no download required)
- Real-time multiplayer via Networked A-Frame and Janus WebRTC

### NFT & Blockchain
- NFT badge minting powered by the **Tatum API** on **Polygon**
- Metaverse assets hosted on **IPFS** via Protocol Labs
- Wallet message signing and verification for authentication

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend Framework | React 16, React Router 5 |
| 3D / VR | A-Frame, Three.js, Mozilla Hubs (custom fork) |
| Multiplayer | Networked A-Frame, Janus WebRTC, Phoenix Channels |
| Wallet / Web3 | ethers.js, web3.js, @web3-react/core |
| Wallet Connectors | InjectedConnector, WalletConnect, WalletLink (Coinbase) |
| Auth | Web3Auth |
| NFT Minting | Tatum API |
| Blockchain | Polygon (MATIC) |
| Decentralized Storage | IPFS / Filecoin |
| UI Components | Chakra UI, Emotion, Sass |
| Build Tools | Webpack 4, Babel |
| Backend | Reticulum (Phoenix/Elixir) |

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org) v12 or higher
- An [Infura](https://infura.io) API key for RPC endpoints
- A [Tatum](https://tatum.io) API key for NFT minting

### Installation

```bash
git clone https://github.com/your-org/DAOVerse.git
cd DAOVerse
npm ci
```

### Configuration

Copy `.defaults.env` and fill in your values:

```bash
cp .defaults.env .env
```

Key environment variables:

| Variable | Description |
|---|---|
| `INFURA_KEY` | Infura project ID for Ethereum RPC |
| `RETICULUM_SERVER` | Backend server URL (default: `dev.reticulum.io`) |
| `CORS_PROXY_SERVER` | CORS proxy service URL |
| `THUMBNAIL_SERVER` | Media thumbnail service URL |
| `ASSET_BUNDLE_SERVER` | Asset hosting URL |
| `DEFAULT_SCENE_SID` | Default VR scene identifier |
| `BASE_ASSETS_PATH` | Path for static asset serving |

### Running Locally

```bash
# Development server (all features)
npm run dev

# Development against a Hubs Cloud instance
npm run start

# Local-only development
npm run local
```

### Building for Production

```bash
npm run build
```

### Other Commands

```bash
npm run lint      # Run ESLint
npm run test      # Run test suite
```

---

## How It Works

1. **Connect** — A user lands on the DAOVerse and connects their wallet via MetaMask, WalletConnect, Coinbase Wallet, or Web3Auth.
2. **Onboard** — They select an avatar and enter the onboarding level, where they find community-defined quests.
3. **Earn Badges** — Completing quests (e.g., reading about the DAO, following social handles, connecting a wallet) earns POAP-style NFT badges minted on Polygon via Tatum.
4. **Unlock Access** — Once all required badges are collected, the user is minted an NFT entrance pass and gains access to the full DAOVerse environment.
5. **Engage** — Inside the full experience, members attend events, claim bounties, find collaborators, and contribute to the community — all within a shared 3D world.

---

## Beta Pilot

The initial pilot demonstrates a full community onboarding flow. New members must collect three badges:

| Badge | Requirement |
|---|---|
| **EARN** | Connect your wallet |
| **LEARN** | Read about the DAO, watch a video, and pass a quiz |
| **PLAY** | Follow 2 of 4 community social media handles |

Upon earning all three, members receive an NFT entrance pass to the full DAOVerse with Bounty Chest, Community Area, Resources Area, and Event Area.

---

## Hubs Cloud Deployment

The DAOVerse client can be deployed to any [Hubs Cloud](https://hubs.mozilla.com/docs/hubs-cloud-intro.html) instance. Refer to the [custom client deployment guide](https://hubs.mozilla.com/docs/hubs-cloud-custom-clients.html) for details on connecting to your own Reticulum backend.

---

## Contributing

Contributions are welcome. Please open an issue or pull request describing your proposed change. For significant changes, open an issue first to discuss.

See [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed guidelines.

---

## License

This project is licensed under the [Mozilla Public License 2.0](https://opensource.org/licenses/MPL-2.0). See [LICENSE](./LICENSE) for details.

---

## Acknowledgements

- [Mozilla Hubs](https://hubs.mozilla.com/) — Open-source 3D collaboration platform (base framework)
- [A-Frame](https://aframe.io/) — Web framework for building VR experiences
- [Web3Auth](https://web3auth.io/) — Wallet authentication and social login
- [Tatum](https://tatum.io/) — NFT minting API
- [Protocol Labs](https://protocol.ai/) — IPFS / Filecoin decentralized storage
- [Polygon](https://polygon.technology/) — Layer 2 blockchain for NFT rewards
