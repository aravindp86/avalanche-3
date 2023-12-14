# Token 

## Introduction

This repository contains a Solidity smart contract for a custom ERC-20 token named "Arvind" (with the symbol "AR"). The token contract is implemented using the OpenZeppelin library, leveraging the ERC20, Ownable, and ERC20Burnable standard contracts.

## Smart Contract Overview

### Token Features

1. **Name and Symbol:** The token is named "Arvind" and has the symbol "AR."

2. **Initial Supply:** Upon deployment, the contract mints 300 AR tokens and assigns them to the address specified as the initial owner.

3. **Minting:** Only the owner of the contract can mint additional tokens. The `mintTokens` function allows the owner to mint a specified amount of tokens and assign them to a destination address.

4. **Burning:** Token holders can burn their own tokens using the `burnTokens` function, reducing the total token supply.

5. **Transfer:** The contract includes a standard ERC-20 `transfer` function to facilitate token transfers between addresses.

### Security

The contract inherits from the OpenZeppelin `Ownable` contract, ensuring that only the owner has the authority to mint new tokens. Additionally, the `ERC20Burnable` contract is utilized for secure burning functionality.

## Getting Started

To deploy and interact with the contract, follow these steps:

1. **Install Dependencies:** Make sure you have Node.js and npm installed. Run `npm install` to install the necessary dependencies, including OpenZeppelin contracts.

2. **Deploying the Contract:** Deploy the contract to the Ethereum blockchain using a development environment like Remix, Truffle, or Hardhat. Ensure that you provide an initial owner address during deployment.

3. **Interacting with the Contract:** Use a wallet or a tool like Remix to interact with the deployed contract. The owner can mint tokens, and anyone can burn their own tokens.

## Example Usage

### Minting Tokens

To mint additional tokens, call the `mintTokens` function, providing the destination address and the number of tokens to mint.

```solidity
// Example: Minting 100 tokens to address 0x123...
mintTokens(0x123..., 100);
```

### Burning Tokens

Token holders can burn their own tokens by calling the `burnTokens` function, specifying the number of tokens to burn.

```solidity
// Example: Burning 50 tokens
burnTokens(50);
```

### Transferring Tokens

Use the standard ERC-20 `transfer` function to send tokens from one address to another.

```solidity
// Example: Transferring 20 tokens to address 0x456...
transfer(0x456..., 20);
```
