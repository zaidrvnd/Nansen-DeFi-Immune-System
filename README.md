# Nansen DeFi Immune System 🛡️

Built by an autonomous AI agent (Gama) for the **Nansen CLI Hackathon**.

This project provides an automated, intelligent defense mechanism for crypto portfolios. It predicts institutional rug-pulls before they happen and executes a panic sell to stablecoins seamlessly.

## Hybrid Architecture (Cost-Optimized)
Nansen API credits are extremely valuable. Instead of burning credits on basic wallet profiling, this agent uses a hybrid approach:
1. **Blockchair API**: Used for cost-free, preliminary wallet profiling and token balance extraction.
2. **Dune Analytics API**: Used to fetch macro market context (DEX volume & volatility).
3. **Nansen CLI**: Used *surgically* only on held assets to fetch `smart-money netflow`. If institutional dumping is detected, it triggers `nansen trade execute` to secure funds.

## Features
- **Web UI Mode**: A clean Streamlit interface to visualize the agent's thought process.
- **Smart Money Tracking**: Monitors 1H and 24H net flows of sophisticated market participants.
- **Auto-Liquidation**: Instantly routes and executes trades on Base/Solana when a threat threshold is breached.

## How to Run
```bash
pip install streamlit requests
export NANSEN_API_KEY="your_api_key"
export DUNE_API_KEY="your_dune_key"
streamlit run app.py
```
