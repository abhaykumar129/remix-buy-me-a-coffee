
# remix-buy-me-a-coffee

☕ Buy Me A Coffee - Vyper Smart Contract

📌 Overview

This is a decentralized "Buy Me A Coffee" funding contract built with Vyper.
It allows anyone to send ETH to support the contract owner, but only if the funding amount meets a minimum USD value (using a Chainlink price feed).

**** Language: Vyper ^0.4.1

**** Network: Ethereum / Sepolia Testnet

**** Use Case: Crowdfunding / Tips


🔹 Features

1.Users can fund the contract with ETH.

2.ETH amount is converted to USD using Chainlink Price Feed.

3.Minimum funding amount: $5 USD.

4.Owner can withdraw all funds at any time.

5.Tracks funders and their contributions.


📦 Contract Details

Constants & Immutables

**** MINIMUM_USD = 5 ETH (in Wei) – Minimum funding in USD.

**** OWNER – Contract deployer (immutable).

**** PRICE_FEED – Chainlink ETH/USD Aggregator (immutable).

**** PRECISION = 1e18 – Used for USD calculation.

Storage Variables
**** funders – List of all funder addresses.

**** funder_to_amount_funded – Mapping of address → funded ETH.


🔹 How It Works


1.User sends ETH via fund() or by sending ETH directly to the contract.

2.Contract fetches ETH/USD price from Chainlink Aggregator.

3.ETH amount is converted to USD.

4.If >= $5, the funding is accepted; otherwise, the transaction reverts.

5.Owner can withdraw all collected funds with withdraw().




   
