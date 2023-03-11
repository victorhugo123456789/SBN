# Initial Setup
.. most operations are inside the "mainContracts" directory.
## INSTALLATION
First run the command below to get `foundryup`, the Foundry toolchain installer:

```sh
curl -L https://foundry.paradigm.xyz | bash
```
#### then install 
```sh
forge init --force --no-commit
forge install Openzeppelin/openzeppelin-contracts --no-commit
forge install Openzeppelin/openzeppelin-contracts-upgradeable --no-commit
forge install smartcontractkit/chainlink-brownie-contracts --no-commit
forge install transmission11/solmate --no-commit
```
#### then build
```sh
forge build --via-ir
forge clean
forge inspect
```

#### then test ( use fuzzing, cheats and more!!)
```sh
forge test
```
#### then Deploy 
```sh
forge create
forge verify-contract
forge verify-check
forge flatten
```
### deploy example
```sh
forge create src/Contract.sol:ContractWithNoConstructor
## or with arguments
forge create src/Contract.sol:MyToken --constructor-args "My Token" "MT"
## verify
forge verify-contract <address> SomeContract --watch
## flatten to Contract.flattened.sol
forge flatten --output src/Contract.flattened.sol src/Contract.sol
```

# FinanceSBN Contracts v2

### Please use only the V2 contracts V1 depreciated.


## FinanceSBN Token
Runs on Polygon Edge (previously SDK) is 

## FinanceSBN (FSBN)
- creates new SBN contract for registration process for a Token team looking for Advance on Tokens
- 

### Factory contract for creating new contracts that emit data.
each contract will be generated and registered on the teams token to allow minting for both NFT and main Token Contract
* * the contract will be deployed to the blockchain and the address will be stored

## Default SBN Contract

### Default Contract used after initial setup and focused on NFT Advance relationships/actions
- based on any given NFT token ID payment information stored and used
- Initial purchase of NFT and payment plans to buy back said NFT 
- Payments made during the advance are made to the "owner" of any given NFT ID.
- Final payment will only be allowed to be completed through a manual process.


## Swap External


## Swap Internal - NOT REQUIRED

