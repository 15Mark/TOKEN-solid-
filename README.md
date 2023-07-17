# GAMMA TOKEN

This Solidity program is a "GAMMA TOKENS" program that demonstrates the basic syntax and functionality of the Solidity programming language. 

## Description

An in-depth paragraph about your project and overview of use.

## Getting Started

### Installing

* How/where to download your program
* Any modifications needed to be made to files/folders

### Executing program

* How to run the program
* Step-by-step bullets
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

    contract MyToken {
        
        string public name = "GAMMA";
        string public abbrv = "GAMM";
        uint totalSupply = 0;

        mapping(address => uint) public balances;

        function mint(address _address, uint _values) public{
        totalSupply += _values;
        balances[_address] += _values;
        }
        
        function burn(address _address, uint _values)public{
            if (balances[_address] >= _values){
            totalSupply -= _values;
            balances[_address] -= _values;
            }
        }
}
```

## Authors

Mark Angelo Evangelista

https://www.facebook.com/markangelo.evangelista.507


## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details
