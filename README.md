# project_2
Below is the Markdown file (`README.md`) for your Solidity contract, formatted for uploading to GitHub:

```markdown
# MyToken Solidity Contract

This repository contains the Solidity code for the `MyToken` smart contract. This contract implements a basic ERC20-like token with minting and burning functionality.

## SPDX License Identifier

```solidity
// SPDX-License-Identifier: MIT
```

## Solidity Version

```solidity
pragma solidity ^0.8.0;
```

## Contract: MyToken

### Public Variables

- `Name`: The name of the token, set to "Ether".
- `Abbreviation`: The abbreviation of the token, set to "ETH".
- `Supply`: The total supply of the token, initialized to 0.

### Mapping

- `balances`: Maps an address to its balance of tokens.

### Functions

#### `mint`

```solidity
function mint(address account, uint amount) public {
    Supply += amount;
    balances[account] += amount;
}
```

- Increases the total supply by the specified amount.
- Increases the balance of the specified account by the specified amount.

#### `burn`

```solidity
function burn(address account, uint amount) public {
    if(balances[account] >= amount){
        Supply -= amount;
        balances[account] -= amount;
    }
}
```

- Decreases the total supply by the specified amount if the account has enough balance.
- Decreases the balance of the specified account by the specified amount if the account has enough balance.

## Full Contract Code

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract MyToken {

    // public variables here
    string public Name = "Ether";
    string public Abbreviation = "ETH";
    uint public Supply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address account, uint amount) public {
        Supply += amount;
        balances[account] += amount;
    }

    // burn function
    function burn(address account, uint amount) public {
        if(balances[account] >= amount){
            Supply -= amount;
            balances[account] -= amount;
        }
    }
}
```

## License

This project is licensed under the MIT License.
```

You can create a `README.md` file in your GitHub repository and copy the above content into it. This will provide a clear and detailed description of your Solidity contract, including the purpose of each function and variable.
