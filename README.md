\# ERC-20 Token Faucet DApp (Sepolia)



\## Overview

This project is a full-stack ERC-20 Token Faucet decentralized application built on the Sepolia testnet.  

It demonstrates smart contract development, on-chain rate limiting, wallet integration, and containerized deployment.



The faucet enforces:

\- 24-hour cooldown between claims

\- Lifetime maximum claim limit per address

\- Admin-controlled pause mechanism



---



\## Architecture

\- \*\*ERC-20 Token Contract\*\*

&nbsp; - Fixed maximum supply

&nbsp; - Minting restricted to faucet contract

\- \*\*Faucet Contract\*\*

&nbsp; - Enforces cooldown and lifetime limits on-chain

&nbsp; - Emits events for all claims and pause actions

\- \*\*Frontend\*\*

&nbsp; - React + Vite

&nbsp; - MetaMask wallet integration (EIP-1193)

&nbsp; - Real-time balance and eligibility display

\- \*\*DevOps\*\*

&nbsp; - Dockerized frontend

&nbsp; - Health check endpoint for readiness



---



\## Deployed Contracts (Sepolia)



\- \*\*ERC-20 Token\*\*  

&nbsp; https://sepolia.etherscan.io/address/0xFA8a0937d4019647A188296753861abeF5E6E892



\- \*\*Token Faucet\*\*  

&nbsp; https://sepolia.etherscan.io/address/0x08Ee0fd68b52E69c3f3b3a875F475E5e77824b85



Both contracts are verified on Etherscan.



---



\## Faucet Parameters

\- \*\*Tokens per claim\*\*: Fixed amount per request

\- \*\*Cooldown\*\*: 24 hours between claims

\- \*\*Lifetime limit\*\*: Fixed maximum tokens per address



These values are enforced directly on-chain for trustless operation.



---



\## Quick Start (Docker)



```bash

cp .env.example .env

\# Update RPC URL if needed



docker compose up --build



