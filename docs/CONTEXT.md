# ChainPay NG

A blockchain-based bill payment platform enabling Nigerians to pay for utilities and services using stablecoins and cryptocurrencies on a low-fee, scalable blockchain network.

---

## Table of Contents

1. [Overview](#overview)
2. [Technical Architecture](#technical-architecture)
   - [Blockchain Layer](#blockchain-layer)
   - [Frontend Architecture](#frontend-architecture)
   - [Application Stack](#application-stack)
3. [Core Features](#core-features)
   - [Wallet Integration](#wallet-integration)
   - [Bill Payment Services](#bill-payment-services)
   - [Smart Contract System](#smart-contract-system)
4. [Payment Flow](#payment-flow)
5. [API Integrations](#api-integrations)
6. [Development Roadmap](#development-roadmap)
7. [Future Plans](#future-plans)
8. [Security](#security)
9. [Contributing](#contributing)
10. [License](#license)
11. [Project Structure](#project-structure)

---

## Overview

ChainPay NG bridges traditional bill payments with blockchain technology, offering:

- **Fast, low-fee transactions**: Designed for microtransactions, enabling payments as low as 10 cents.
- **Wallet-based payments**: No need for bank accounts; users can pay directly from their crypto wallets.
- **Smart contract security**: Transparent and tamper-proof transactions powered by blockchain.
- **Multi-service support**: Pay for utilities, airtime, data bundles, and more.

The platform is currently built on **Base (EVM)** for its low transaction fees and scalability, making it ideal for microtransactions. Future updates will expand support to additional blockchain networks and tokens.

---

## Technical Architecture

### Blockchain Layer

- **Network**: Base (EVM) - Chosen for its low transaction fees, scalability, and developer-friendly ecosystem.
- **Tokens**: USDC (primary stablecoin), with plans to support additional tokens like Base_ETH, USDT, pNGN (Chain Pay Naira), and others in future updates.
- **Smart Contracts**: Written in Solidity for secure and efficient payment processing.
- **Supported Wallets**:
  - MetaMask
  - OKX Wallet
  - Trust Wallet
  - Other Web3 wallets (via WalletConnect or injected connectors)

### Frontend Architecture

- **Framework**: Next.js for server-side rendering and optimized performance.
- **Styling**: TailwindCSS for utility-first, responsive design.
- **State Management**: Redux Toolkit for global state management.
- **Web3 Integration**: Wagmi for seamless wallet connections and interactions.
- **Theme System**: CSS Variables + React Context for dynamic theming.

### Application Stack

- **Backend**:
  - Node.js with NestJS for a scalable and modular backend.
  - Supabase for database and authentication.
  - Payment API integrations with Flutterwave, Paystack, and Monnify.
- **Frontend**:
  - React.js/Next.js for a dynamic and responsive user interface.
  - TailwindCSS/Chakra UI for component-based styling.
  - Web3.js/Ethers.js for blockchain interactions.
  - Wagmi for simplified Web3 integration.

---

## Core Features

### 1. Wallet Integration

- Seamless wallet connections via MetaMask, Trust Wallet, and WalletConnect.
- Real-time balance checking and management.
- Transaction history tracking for all payments.

### 2. Bill Payment Services

- **Airtime Purchase**: Top up any Nigerian mobile network.
- **Data Bundles**: Buy data plans for all major providers.
- **Electricity Bills**: Pay for electricity directly from your wallet.
- **Other Utilities**: Expandable to include water, cable TV, and more.

### 3. Smart Contract System

The smart contract system is designed for flexibility, allowing future upgrades to support multiple tokens and networks.

```solidity
interface IChainPayNG {
    function depositFunds(address user, uint256 _amount) external;
    function payBill(address provider, uint256 _amount) external;
    function getBalance(address user) external view returns (uint256);
    function withdrawFunds(address user, uint256 _amount) external;
}
```

---

## Payment Flow

1. **Connect**: User connects their wallet to the platform.
2. **Select**: User selects the service (e.g., airtime, data, electricity) and enters the required details.
3. **Confirm**: User approves the transaction in their wallet.
4. **Process**: The smart contract executes the payment on the blockchain.
5. **Deliver**: The service provider fulfills the request (e.g., airtime is credited).
6. **Verify**: User receives a confirmation of the successful transaction.

---

## API Integrations

### Payment Processors

- **Flutterwave**: For airtime and bill payments.
- **Paystack**: For utility and mobile payments.
- **Monnify**: For fiat on/off-ramp services, enabling users to convert between fiat and crypto.

---

## Future Plans

- **Multi-Chain Support**: Expand support to additional blockchain networks like Polygon, Arbitrum, and Binance Smart Chain.
- **Multi-Token Support**: Add support for USDT, BUSD, and other stablecoins.
- **Recurring Payments**: Enable automated recurring payments for utilities.
- **Pan-African Expansion**: Extend services to other African countries.
- **Mobile Application**: Develop a mobile app for iOS and Android.
- **Additional Services**: Integrate more utility providers and services.

---

## Security

- **Smart Contract Audits**: Regular audits by reputable firms to ensure security.
- **Multi-Signature Controls**: Enhanced security for fund management.
- **Rate Limiting**: Protection against DDoS attacks and abuse.
- **Regular Security Assessments**: Continuous monitoring and updates to address vulnerabilities.

---

## Contributing

We welcome contributions from the community! Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines on:

- Code standards and best practices.
- Pull request process and code reviews.
- Development setup and environment configuration.
- Testing requirements and quality assurance.

---

## License

This project is licensed under the MIT License - see [LICENSE](./LICENSE) for details.

---
