# Project Title

A simple smart contract for creating and managing a token named "Newton" with the abbreviation "N".

## Description

The `MyToken` contract allows users to mint new tokens, burn existing tokens, and keep track of token balances associated with different addresses. The contract demonstrates basic token management on the Ethereum blockchain.

## Getting Started

### Executing program

Follow these steps to set up and deploy the contract using Remix IDE:

1. **Open Remix IDE:**
   Go to [Remix IDE](https://remix.ethereum.org).

2. **Create a New File:**
   - In the left sidebar, click on the "+" icon to create a new file.
   - Name your file `MyToken.sol`.

3. **Paste the Solidity Code:**
   ```solidity
   // SPDX-License-Identifier: MIT
   pragma solidity 0.8.18;

   contract MyToken {

       // public variables here
       string public TOken_Name = "Newton";
       string public Token_Abbrv = "N";
       uint public Total_Supply = 0;
       
       // mapping variable here
       mapping(address => uint) public Balanace;

       // mint function
       function mint (address _Addre, uint _val) public {
           Total_Supply += _val;
           Balanace[_Addre] += _val;
       }

       // burn function
       function burn (address _Addre, uint _val) public {
           if(Total_Supply >= _val) {
               Total_Supply -= _val;
               Balanace[_Addre] -= _val;
           }
       }
   }

## Help

For common issues or problems, you can refer to the Remix IDE documentation or check the console for error messages.

command to run if program contains helper info
```

## Authors

Contributors names and contact info:

Rahul Prasad
@RahulPrasad-78

