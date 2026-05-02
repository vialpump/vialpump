<div align="center">
  <h1>VIALPUMP</h1>
  <p><strong>Hold harder, rarer drops.</strong></p>
  <p>Automated Pixel Vial cNFT minting engine driven by Solana token trades.</p>
  
  ![License](https://img.shields.io/badge/License-MIT-blue.svg)
  ![Solana](https://img.shields.io/badge/Chain-Solana-green.svg)
  ![Status](https://img.shields.io/badge/Status-Mainnet-brightgreen.svg)
</div>

## What is Vialpump?

Memecoins on Pump.fun are flat. Holding feels passive. Vialpump fixes this by turning the token trade into the mint event. Every 50,000 `$VIALPUMP` threshold crossed auto-mints a unique deterministic Pixel Vial cNFT. Sell 50,000, and your most recent vial burns via LIFO. 

## Core Mechanics

| Mechanic | Description | Impact |
|----------|-------------|--------|
| **Auto-Mint** | 1 cNFT minted per 50k tokens held | Turns holding into a collectible game |
| **LIFO Burn** | Selling burns the newest vials first | Protects rare early mints, punishes flips |
| **Hard Cap** | Exactly 10,000 vials max supply | Immutable scarcity separate from token |
| **Deterministic Art** | `sha256(wallet + edition)` | Eliminates IPFS reliance, guarantees uniqueness |

## How It Works

```text
 ┌────────────────┐       ┌─────────────────┐       ┌─────────────────┐
 │ Pump.fun Buy   │ ────▶ │ Helius Webhook  │ ────▶ │ Listener Engine │
 └────────────────┘       └─────────────────┘       └─────────────────┘
                                                             │
                                                             ▼
 ┌────────────────┐       ┌─────────────────┐       ┌─────────────────┐
 │ cNFT in Wallet │ ◀──── │ Bubblegum Mint  │ ◀──── │ State Database  │
 └────────────────┘       └─────────────────┘       └─────────────────┘
```

## Technology Stack

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Chain** | Solana | High throughput, low cost |
| **NFT Standard** | Metaplex Bubblegum | Compressed NFTs (~$0.0008 per mint) |
| **Indexing** | Helius | Real-time transfer webhooks |
| **State Layer** | Realtime PostgreSQL | Wallet state caching & live feeds |
| **Renderer** | Node.js (Sharp) | Deterministic layered image generation |

## Phased Roadmap

| Phase | Description | Status |
|-------|-------------|--------|
| **Phase 0** | Listener deployment, Pump.fun launch | Active |
| **Phase 1** | Pharmacy P2P marketplace, Dashboard | Next |
| **Phase 2** | Vial Staking, Trait Fusion | Planned |
| **Phase 3** | Apothecary Governance, Collabs | Vision |

## Reference Links

| Resource | Link |
|----------|------|
| Website | [vialpump.fun](https://vialpump.fun) |
| X / Twitter | [@vialpump](https://x.com/vialpump) |
| Docs | [vialpump-docs](../vialpump-docs) |

<br>
<div align="center">
  <sub>Vialpump is experimental software. Use at your own risk. Not financial advice.</sub>
</div>
