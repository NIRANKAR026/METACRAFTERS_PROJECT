# METACRAFTERS_PROJECT
Final project for the course ETH PROOF: Beginner EVM Course
## TOKEN

Creating a Token 

## Description

This program is written in Solidity,used in Ethereum Blockchain.This program demostrate the creation of a Token along with basic feature of token.

## Getting Started


### Executing program

* To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

* This token project demonstrate several key function of  Token like mapping,mint,and burn function. 

```
contract MyToken {

    // public variables here
    string public Token_Name="Alice";
    string public Token_Abbrv="ALI";
    uint public Total_Supply=0;
    
    // Mapping
    mapping (address=>uint) public balance;

    // mint function(This function contain two parameter one is adress and other is the value assinged to the adresss as balance)
    
    function mint(address _address,uint value) public
    {
        balance[_address]+=value;
        Total_Supply+=value;
    }
    
    //Burn function(Burn function is mechanism used to destroy the token taking into account that the balance availabel in adress is greater than the number of token to be burnt.)

    function burn (address _address,uint value) public 
    {
        if (balance[_address]>=value)
        {
            Total_Supply-=value;
            balance[_address]-=value;
        }
    }
}
```
