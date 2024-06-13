# project_2

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

Refer to the code uploaded in same repository.

## License

This project is licensed under the MIT License.
```

