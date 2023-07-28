# MyToken

A simple implementation of a token on the blockchain. It allows users to mint and burn tokens.

## Description

This contract provides a basic structure for creating and managing tokens on blockchain with the functions: Mind and Burn. It allows the users to track the gas fees and check whether the balances are working as intended before using on future projects.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Solidity.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.18;

contract MyToken {

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
```

To compile the code, click on the "MyToken Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the sayMyToken function. Click on the "MyToken" contract in the left-hand sidebar, and then click on the "sayMyToken" function. Finally, click on the "transact" button to execute the function and retrieve the "MyToken" message.

## Authors

Metacrafter kennethdelosreyes
[@metacraftersio]


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
