# SOLIDITY TOKEN

This is simple a creation of "SOLIDITY TOKEN". This program is indicated for you to create a token using the functionality of the Solidity programming language.

## Description

This program is a simple smart contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a mint and burn function that creates the token. This program serves as a simple and straightforward introduction to Solidity programming and for creating a token, and can be used as a stepping stone for more complex projects in the future (e.g., ERC-721 NFT Token).

## Getting Started

### Installing

You can download my file here in Github (https://github.com/c-bugarin/Solidity-Assessment/tree/main)

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new workspace, after that create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity >=0.8.18;

contract myToken {

    // public variables here
    string public tokenName = "META";
    string public tokenAbbrv = "MTA";
    uint public totalSupply = 0;

    // mapping variable here
     mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
   }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
      }
   }
}

## Authors

Contributors names and contact info

Bugarin, Catherine  

## License

This project is licensed under Bugarin, Catherine. License - see the LICENSE.md file for details
