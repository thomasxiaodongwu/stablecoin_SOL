# Decentralized Stablecoin on Solana

This project implements a decentralized stablecoin system on the **Solana** blockchain. The stablecoin is backed by collateral, and its value is maintained via an over-collateralized system. This mechanism ensures the stablecoin's price stability through a combination of liquidation mechanisms, price feeds, and a governance protocol.

### Key Features:
- **Over-Collateralized Stablecoin**: Mint stablecoins by locking up collateral, ensuring the stability of the stablecoin’s value.
- **Health Factor & Liquidation**: Positions are continuously monitored for health factor. If collateral falls below the required threshold, liquidations are triggered to maintain stability.
- **Price Feeds**: Real-time price data from **Pyth** (or other trusted Oracle providers) to maintain the accurate value of collateral backing the stablecoin.
- **Governance**: Allows stakeholders to vote on critical parameters like collateralization ratios and liquidation thresholds.

---

## Overview

This decentralized stablecoin operates similarly to MakerDAO, where users can mint stablecoins by providing collateral (e.g., Solana tokens) into a smart contract. The stablecoin's stability is ensured by maintaining a collateralization ratio, with liquidations occurring when collateral value drops too low.

### Components:
- **Minting Stablecoins**: Users can mint stablecoins by collateralizing assets.
- **Collateralization Ratio**: The system ensures that collateral always exceeds the value of the minted stablecoins.
- **Health Factor**: Calculates the health of the collateralized position. If the health factor falls below a certain threshold, the position is eligible for liquidation.
- **Price Feeds**: Price data from **Pyth** (or another oracle) ensures that collateral is correctly valued.
- **Liquidation**: When the health factor falls below the liquidation threshold, the position is liquidated by a trusted actor (e.g., liquidator).
- **Governance**: Community-driven decision-making on system parameters via a decentralized governance mechanism.

