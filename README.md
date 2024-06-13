## Creating New Token 

This Solidity program is just creating our own Token on remix . The purpose of this program is to create our own token in Solidity and want to get a feel for how it works.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has two functions :Mint function (It will increase the total supply and the balance of the “sender” with the Value) . Burn function (It will deduct the value from the total supply and from the balance of the “sender”.) 

This is link to my source code https://gist.github.com/Ankit176y/1e81c7522f3301b1d5a16f56327e8e55

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:


    pragma solidity 0.8.18;
    contract MyToken {

        string public Token_Name ="Tether";
        string public Token_Abbrev = "USDT";
        uint public Total_supply = 0;

        mapping(address => uint) public Balances;

        function mint (address _Address,uint _Value) public {
            Total_supply += _Value;
            Balances[_Address]+= _Value;
        }
        function Burn (address _Address,uint _Value) public {
            if(Balances[_Address] >= _Value){
            Total_supply -= _Value;
            Balances[_Address]-= _Value;
            }
    }
    }
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "HelloWorld" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the sayHello function. Click on the "HelloWorld" contract in the left-hand sidebar, and then click on the "sayHello" function. Finally, click on the "transact" button to execute the function and retrieve the "Hello World!" message.

## Authors

Metacrafter Chris  
[@metacraftersio](https://twitter.com/metacraftersio)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
