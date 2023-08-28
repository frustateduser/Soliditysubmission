# Soliditysubmission
submission for solidity project for metacrafter. This is a contract which adds value to address and detect's it 
it also stop detecting balance if detecting amount is more than balance
# DESCRIPTION
This program is written in solidity a programming language which is used to write smart contract in Ethereum a leading
in blockchain technology, this contract is a simple set of code which is used to add ether to your account and detect it
and if the detuction amount is more than avilable it does not detect the amount, other than this it shows the avilable 
amount in our address.

### Running the code
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at <a heref="https://remix.ethereum.org/">https://remix.ethereum.org/</a>

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar.
Save the file with a .sol extension. 
Copy and paste the following code into the file:
```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8;

contract MyToken {

    // public variables here
    string public tokenName="META";
    string public tokenAbbr ="MTA";
    uint public totalSupply =0;
    // mapping variable here
    mapping (address => uint) public balances;
    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }
    // burn function
    function burn (address _address,uint _value) public {
        if(balances[_address]>= _value){
        totalSupply -= _value;
        balances[_address] -= _value;
        }
    }

}

```

save the code to compile and deploy it using remix.
{for more detail refer the code}
