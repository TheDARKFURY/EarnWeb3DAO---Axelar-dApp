# Introduction

Cross-chain communication is an essential part of the Web3 ecosystem, enabling different blockchain networks to interoperate and exchange data and value. By facilitating the seamless transfer of information and assets between different blockchains, cross-chain communication allows for the creation of a more open, connected, and inclusive decentralized world. With the ability to bridge the gap between different blockchains, cross-chain communication is a powerful tool for driving innovation and adoption in the world of decentralized technologies.

---

## What is Cross-chain Interoperability?

Cross-chain communication refers to the ability of different blockchain networks to communicate and exchange information with each other. This is important because it allows for the transfer of value and data between different blockchains, which can help to increase the overall interoperability and effectiveness of the broader blockchain ecosystem.

For example, if two different blockchain networks are able to communicate with each other, it would be possible for a user on one network to send a transaction to another user on the other network, even though the two users are on separate blockchains. This can help to improve the overall usability and utility of blockchain technology.

---

## What is Axelar

Axelar provides Web3 with secure cross-chain communication. Axelar is built on proof-of-stake, the battle-tested method utilised by Ethereum, Cosmos, Avalanche, and others.

Axelar-based cross-chain apps are really permissionless, which means that their transactions cannot be restricted by any oracle, relayer, or validator. Axelar's security model is similar to that of many of the chains it connects.

### Fundamental functionality

Here are two basic cross-chain functions that Axelar can add to a dApp.

1. **_Token transfers_**: Securely send and receive fungible tokens from one chain to another, including Cosmos-to-EVM and other complex transfers.
2. **_General Message Transmission_**: Call any EVM chain function from within a dApp; construct DeFi functions; move NFTs cross-chain; execute cross-chain calls of any kind that securely sync state between dApps on different ecosystems.

---

## What we're building

Today, we will create a smart contract in which a user can send a token (say, USDC) from one chain to an account on another chain with "payment information." Payment information can include an invoice/description of payment/reason and note to a buddy, among other things.

---

## Setting Up Dev Environment

To begin, we must clone the examples GitHub repository so that we may work on the pre-built example to send tokens from the source chain to an account in the destination chain.

```bash
git clone https://github.com/axelarnetwork/axelar-local-gmp-examples
```

Next, we must perform a clean installation of the essential npm packages for this run.

```bash
npm ci
```

Next, we'll need our Ethereum wallet private key to deploy contracts to the testnet. Rename `.env.example` to `.env` then insert your private key into the `.env` file.

```bash
cp .env.example .env
```

---
## To make Transaction on Local Node

To Start a Local Node

```bash
node scripts/deploy.js examples/call-contract-with-token local
```

Now, Let's Test our contract. We will transfer 10 aUSDC tokens from Moonbeam to Avalanche chain.

```bash
node scripts/test examples/call-contract-with-token local "Moonbeam" "Avalanche" 10 [address1],[address2] "Message"
```

## Transactions on Axelar    

https://testnet.axelarscan.io/transfer/A7D7207B0C84B132F951AD6C644836B145998118FA03116F6FC5BE47C686771A

https://testnet.axelarscan.io/address/0xE8D0A25E5Bf18870Ad5B0D2164144982BE2441Da

Moonbeam -> Avalanche
https://testnet.axelarscan.io/gmp/0xe8b51fb24161a050b5ed64c333c715c606cf253248a0a4a4f98f502ad1025df5    

Avalanche -> Moonbeam
https://testnet.axelarscan.io/gmp/0x365205d20220977cdd14e25f4146cb46fa9251a482a34cf04bf5bd1979cb480b