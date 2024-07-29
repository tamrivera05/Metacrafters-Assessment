# Project: Create a Token 
The MyToken contract is a simple implementation of an ERC20-like token on the Ethereum blockchain. It allows users to mint and burn tokens, managing their own token balances and the total supply of the token.

## Description
The MyToken contract is designed to handle basic token functionality with public variables for the token's name, abbreviation, and total supply. It includes a mapping to keep track of each address's balance. The contract provides two primary functions: `mint` and `burn`. The `mint` function increases the total supply and an address's balance by a specified amount, while the `burn` function decreases both the total supply and an address's balance. The `burn` function also includes a check to ensure that the sender has sufficient balance to burn the requested amount.

## Getting Started

### Executing the Program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at [Remix](https://remix.ethereum.org/).

#### Create a New File:
- Click on the "+" icon in the left-hand sidebar.
- Save the file with a `.sol` extension (e.g., `MyToken.sol`).
- Copy and paste the following code into the file:

    ```solidity
    // SPDX-License-Identifier: MIT
    pragma solidity 0.8.26;

    contract MyToken {
        // public variables here
        string public tokenName = "TOKEN";
        string public tokenAbbrv = "TKN";
        uint256 public totalSupply = 0;

        // mapping variable here
        mapping(address => uint256) public balances;

        // mint function
        function mint(address _address, uint256 _value) public {
            totalSupply += _value;
            balances[_address] += _value;
        }

        // burn function
        function burn(address _address, uint256 _value) public {
            if (balances[_address] >= _value) {
                totalSupply -= _value;
                balances[_address] -= _value;
            }
        }
    }
    ```

#### Compile the Code:
- Click on the "Solidity Compiler" tab in the left-hand sidebar.
- Make sure the "Compiler" option is set to `0.8.26` (or another compatible version).
- Click on the "Compile MyToken.sol" button.

#### Deploy the Contract:
- Click on the "Deploy & Run Transactions" tab in the left-hand sidebar.
- Select the "MyToken" contract from the dropdown menu.
- Click on the "Deploy" button.

#### Interact with the Contract:
- Once the contract is deployed, you can interact with it by calling the `mint` and `burn` functions.
- To mint tokens, enter the address and the number of tokens to mint, then click on the "mint" button.
- To burn tokens, enter the address and the number of tokens to burn, then click on the "burn" button.

#### Modifications
- Token Details: Change the `tokenName` and `tokenAbbrv` variables to set your token's name and abbreviation.
- Initial Supply: Adjust the `totalSupply` if needed.

## Authors
Tamara Angela Rivera 
[@tamrivera05](https://github.com/tamrivera05)
