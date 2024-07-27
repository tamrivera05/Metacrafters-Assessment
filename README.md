# Project: Create a Token 
The MyToken contract is a simple implementation of an ERC20-like token on the Ethereum blockchain. It allows users to mint and burn tokens, managing their own token balances and the total supply of the token.

## Description
The MyToken contract is designed to handle basic token functionality with public variables for the token's name, abbreviation, and total supply. It includes a mapping to keep track of each address's balance. The contract provides two primary functions: `mint` and `burn`. The `mint` function increases the total supply and an address's balance by a specified amount, while the `burn` function decreases both the total supply and an address's balance. The `burn` function also includes a check to ensure that the sender has sufficient balance to burn the requested amount.

## Getting Started
I used the Remix-Ethereum IDE so all you need to do is clone my repository

##Interacting with the Contract
Use the "Deploy & Run Transactions" section in Remix to interact with the contract

### Modifications
- Token Details: Change the `tokenName` and `tokenAbbrv` variables to set your token's name and abbreviation.
- Initial Supply: Adjust the `totalSupply` if needed.

## Authors
Tamara Angela Rivera 
[@tamrivera05](https://github.com/tamrivera05)
