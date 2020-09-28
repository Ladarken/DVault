## yVault

env...
solc 0.5.15

```shell
brew install solidity@5
```

python 3

`pip install web3`

[ganache-cli](https://github.com/trufflesuite/ganache-cli)

All deployed contracts are under **contracts/standard**




## DarkVault

DarkVault is made with three main parts:

1. Controller
Controller sets the corresponding vault and its strategy with a selected token.

2. Vault
Vault is used for people to deposit, withdraw and harvest.

3. Strategy
Strategy is used to allocate the deposited funds into different farming/mining/forging projects.

The deployed smart contracts' configs [Smart Contract Configs](https://raw.githubusercontent.com/yfii/yvault/master/contracts/standard/config.json)

## ABI

ABI for the Vault [vault](abi/vault.json)
ABI for the Strategy [Strategy](abi/strategy.json)

### Write
`function deposit(uint amount)` Approve, then Deposit.

`function withdraw(uint amount)` Withdraw

### Read

`function balanceOf(address user) public view returns (uint256)` Check balance of dToken

`function getPricePerFullShare() public view returns (uint)`  Check share of original Token

Tokens to be redeemed = (Balance of dToken * getPricePerFullShare) / 1e18 
