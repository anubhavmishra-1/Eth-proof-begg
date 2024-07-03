# Creating a Token.

An Ethereum blockchain token smart contract is implemented by the ImprovedToken contract. It provides the essential functions for tracking token holders' balances and minting and burning tokens.

##  Details
Token Name: "Available Tokens" 

Token Abbreviation: "AT."

initially the available tokens is taken as zero, and all variables are public.

## Applications
### Create Tokens
Tokens can be generated and linked to addresses in a smart contract using the mint function. When the mint function is called, new tokens are generated and assigned to specific blockchain addresses (wallets). This process increases the total number of available tokens by adding newly minted tokens to the existing pool.




### Mint Tokens
Tokens can be added to the current token balance once they have been produced.



### Burn Tokens
If required, we can reduce the total amount of tokens accessible by using the burn function. As a result, tokens are taken from certain addresses, reducing their supply.




## Functions used.


### Mint function

```
 function mint(address _to, uint256 _value) public {
        TotalSupply += _value;
        balanceOf[_to] += _value;
    }
```
### Burn function
```
 function burn(address _from, uint256 _value) public {
        if(balanceOf[_from] >= _value) {
        TotalSupply -= _value;
        balanceOf[_from] -= _value;
    }
```
## Code 
```
contract MyToken {

    string public name = "University";
    string public symbol = "Branch";
    uint256 public TotalSupply = 20;

    mapping(address => uint256) public balanceOf;

  
    function mint(address _to, uint256 _value) public {
        TotalSupply += _value;
        balanceOf[_to] += _value;
    }

    function burn(address _from, uint256 _value) public {
        if(balanceOf[_from] >= _value) {
        TotalSupply -= _value;
        balanceOf[_from] -= _value;
    }
}
}
```
## Where to execute this code?

By working with this code on "https://remix.ethereum.org/," an easy-to-use web platform designed specifically for developing and testing Ethereum smart contracts, we may efficiently compile, deploy, and administer the ImprovedToken contract.


Moreover for detailed explantion, here's an explanatory video regarding the code, "link"
kindly refer to the following link for the detailed explantion. 
## THANK YOU!
