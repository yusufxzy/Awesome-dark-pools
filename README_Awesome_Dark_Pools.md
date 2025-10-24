# 🕳️ Awesome Dark Pools
*A comprehensive reading list for understanding traditional and blockchain-based dark pools.*

Dark pools have been a critical component of financial markets since the early 1990s, allowing large institutional traders to execute orders without revealing intent to the broader market. While they reduce market impact and information leakage, traditional dark pools are often opaque and susceptible to abuse.  

Blockchain-based dark pools reimagine this architecture through **privacy-preserving cryptography** — building trustless, verifiable, and censorship-resistant mechanisms for private trading.

---

## 📘 Overview

This repository curates academic papers, whitepapers, and technical designs covering:
- Traditional dark pools in finance and market microstructure
- Blockchain-based dark pool architectures using ZKPs, MPC, FHE, and TEEs
- Mempool privacy and pre-execution privacy research
- Design documents of live and upcoming crypto-native private exchanges

---

## 🧱 Traditional Finance & Market Microstructure

| Title | Author(s) | Year | Summary / Focus |
|-------|------------|------|----------------|
| **Dark Pools: The Rise of the Machine Traders** | Scott Patterson | 2012 | Foundational account of the rise of dark pools and algorithmic trading. |
| **Sharks in the Dark: Quantifying HFT Dark Pool Latency Arbitrage** | Matteo Aquilina et al. | 2024 | Quantifies stale reference pricing and latency arbitrage in dark pools using UK regulatory data. Finds HFTs exploit stale quotes 96–99% of the time. |
| **The Muted Seven – 7 Things You Should Consider re: Confidential Compute** | Bryan Ji, Greenfield | 2024 | Explains distinctions between ZKP, MPC, FHE, and TEE in privacy systems — useful when comparing PET primitives in finance. |
| **Regulatory Actions & History** | SEC filings | 1990s–2020s | Multiple cases where dark pool operators (Barclays, Credit Suisse, Deutsche Bank, etc.) were fined for misuse and front-running. |

---

## 🔒 Blockchain-Based Dark Pools

| Title | Source | Year | Summary |
|-------|---------|------|----------|
| **Renegade Whitepaper** | Renegade Labs | 2024 | MPC-based private dark pool on-chain. Orders matched privately via multi-party computation; combines on-chain settlement with off-chain encrypted matching. |
| **Darklake Docs** | Darklake (Solana) | 2025 | zkAMM design encrypting trade direction, size, and slippage. Introduces *Blind Slippage Pools* and *Atomic Pools* (ZK proofs verifying post-trade outcomes). |
| **Silhouette: The Shield Exchange** | Stenton Mayne | 2025 | TEE-based shielded exchange on Hyperliquid. Uses Trusted Execution Environments + ZK verification for “shielded” order matching and settlement. |
| **Indifferential Privacy: A New Paradigm for Optimal Matching in Dark Pool Auctions** | Polychroniadou et al. (J.P. Morgan AI Research) | 2025 | Introduces *indifferential privacy* — hybrid of differential privacy and encryption for efficient dark pool matching without FHE/MPC overhead. |
| **Diving Into Dark Pools** | Muhammad Yusuf | 2024 | Overview of dark pool evolution, MEV implications, and transition from centralized to cryptographic privacy mechanisms. |
| **Dark Pools by Lev** | Lev | — | Descriptive overview of dark pool typologies and ethical issues. |

---

## 🌐 Mempool Privacy & Pre-Execution Privacy (Flashbots / Cryptography)

| Title | Source | Summary |
|-------|---------|----------|
| **FRP-18: Cryptographic Approaches to Complete Mempool Privacy** | Flashbots | Outlines MPC, VDF, threshold cryptography, and delay encryption for full mempool privacy. Foundational for pre-trade confidentiality and anti-MEV architecture. |
| **Mempool Privacy: An Economic Perspective** | Rondelet & Kilbourn | 2023 | Analyzes economic and incentive effects of private mempools. Bridges traditional dark pool economics with blockchain mempool design. |
| **Pre-Execution Privacy in PBS** | Flashbots | 2023 | Discusses privacy challenges in Proposer-Builder Separation (PBS) and pre-execution commitment schemes for Ethereum and rollups. |

---

## 🧠 Key Themes & Research Directions

- **Pre-trade privacy:** Preventing order leakage before execution  
- **Matching confidentiality:** Using MPC, FHE, or TEEs for private order books  
- **Post-trade privacy:** Ensuring settlement and counterparties remain hidden  
- **Economic fairness:** Studying the trade-offs between privacy, liquidity, and efficiency  
- **Cryptographic mechanisms:** Exploring hybrid PETs (ZK + DP + TEEs) for scalable performance  
- **MEV minimization:** Bridging mempool privacy and fair ordering  

---

## 🖼️ Repo Visuals

To include a banner image at the top of your GitHub repo:

```markdown
![Dark Pools Banner](assets/darkpools-banner.jpg)
```

---

## 📂 Suggested Folder Structure

```
awesome-darkpools/
│
├── README.md                # Main document (this file)
├── traditional/
│   ├── darkpools_Lev.pdf
│   ├── Sharks_in_the_dark.pdf
│
├── blockchain/
│   ├── Renegade_Whitepaper.pdf
│   ├── Darklake_docs.pdf
│   ├── Silhouette_Design.pdf
│
├── mempool_privacy/
│   ├── FRP-18.pdf
│   ├── Mempool_Privacy.pdf
│   ├── Pre-Execution_Privacy.pdf
│
└── assets/
    └── darkpools-banner.jpg
```

---

> **Contributions Welcome:**  
> If you have additional papers, designs, or protocols on dark pools or pre-trade privacy — feel free to open a PR or issue.
