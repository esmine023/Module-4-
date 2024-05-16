# Module-4
In this last module were gonna do is the challenges we were tasked to do! which is Minting, Transferring, Redeeming, Checking, and Burning Tokens!

# Description
The last module, the very last ETH AVAX. Written in Remix Ethereum, a programming language used for developing Tokens and other NFTs! These are a few codes in that can work perfectly in your favor as OpenZepplin gives you a GitHub that automatically gives you your initial code without even typing it. Just give a little more minting and coding and voila! done very easily.

# Getting Started 
Open Remix: Go to the Remix Ethereum IDE and Click on the "+" icon in the file explorer panel on the left side to create a new file. Paste the contract code into the editor.

## Coding
Switch to the "Solidity Compiler" tab on the left sidebar. Select the version of the Solidity compiler that matches the pragma statement in your contract (^0.8.18 in this case). Then click on the "Compile DegenToken.sol" button to compile the contract.

```
   function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }

    function transfer(address to, uint256 amount) public virtual override returns (bool) {
        _transfer(_msgSender(), to, amount);
        return true;
    }

    function redeem(uint256 amount) public {
        _burn(msg.sender, amount);
        // Perform actions to deliver items to the player
    }

    function balanceOf(address account) public view virtual override returns (uint256) {
        return super.balanceOf(account);
    }

    function burn(uint256 amount) public {
        _burn(msg.sender, amount);
    }
}
```
add functionalities as such; burrn, balance of your token, redeeming, transfer, and mining!

## Running The Code
Once you are all done there you need to do a ctrl + s to see if you have discrepancies in your code, if you don't have then voila! Youre now on your next step! Switch to the "Deploy & run transactions" tab on the left sidebar. Select the "DegenToken" contract from the dropdown list and Click on the "Deploy" button. Confirm the transaction, and after a short while, the contract should be deployed! 

# Authors 
Jay-Ann S. Rafanan/ 3.1BIST/ NTC/ Sakiwaree

# License
This project is licensed under the MIT License - see the LICENSE.md file for details
