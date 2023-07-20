# GAMMA TOKEN

This Solidity program defines a smart contract called "MyToken" that represents a basic cryptocurrency token. Solidity is a programming language specifically designed for writing smart contracts on the Ethereum blockchain.

## Description

The provided Solidity code represents a simple token contract called "MyToken". This contract can be used to create and manage a basic cryptocurrency token on the Ethereum blockchain. 

The contract includes the following features:

- `name` and `abbrv`: These variables represent the name and abbreviation of the token, respectively. In this example, the token is named "GAMMA" with the abbreviation "GAMM". These values are stored as strings and can be accessed publicly.

- `totalSupply`: This variable keeps track of the total supply of the token. It is initialized to 0 but can be increased through the `mint` function and decreased through the `burn` function.

- `balances`: This mapping associates token balances with specific addresses. Each address corresponds to a specific token holder, and their respective token balances are stored as unsigned integers (`uint`). The `balances` mapping is publicly accessible.

- `mint` function: This function allows for the creation of new tokens. It takes an address `_address` and a value `_values` as inputs. The `totalSupply` is increased by the specified `_values`, and the token balance of the `_address` is incremented by the same amount.

- `burn` function: This function enables the destruction of tokens. It takes an address `_address` and a value `_values` as inputs. If the token balance of the `_address` is greater than or equal to the specified `_values`, the `totalSupply` is decreased by `_values`, and the token balance of the `_address` is reduced by the same amount.

By deploying and interacting with this contract on the Ethereum blockchain, you can create instances of the "GAMMA" token, mint new tokens for specific addresses, and burn existing tokens. This contract serves as a foundation for managing a basic cryptocurrency token within your programs or decentralized applications (DApps).
## Getting Started

### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., [ANY NAME].sol). Copy and paste the following code into the file:
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

    contract GAMMA {
        string public name = "GAMMA";
        string public abbrv = "GAM";
        uint TotalSupply = 0;

        mapping(address => uint) public balances;

    function mint(address _address, uint _values) public{
        TotalSupply += _values;
        balances[_address] += _values;
        }

    function burn(address _address, uint _values) public{
        if (balances[_address] >= _values)
        TotalSupply -= _values;
        balances[_address] -= _values;
    }
}   
```
### How to Us
- Compile the contract: First is tick the box of Auto Compiler then Click the Complie Button.
- Deploy the contract: below the Contract press Deploy then check for "Deployed Contracts" below the "Transactions Recorded" then press Greater Than Icon( > )
- Interact with the contract: Copy and Paste the Account(Below the Environment) to the Address on mint(add) or burn button(subtract) values of your balances after doing that you can check it out by pressing the balances button.

P.S All of this function is located to the left side of the screen
## Authors

@Mark Angelo Evangelista
