# degen

## Introduction

DegenToken is an ERC20-compatible token smart contract developed on the Ethereum blockchain. It allows for the creation, transfer, and redemption of tokens, which can be utilized for various purposes including in-game item redemption.

## Functionality

### ERC20 Standard

DegenToken adheres to the ERC20 standard, providing basic functionalities such as:

- Transfer tokens between addresses.
- Approve and transferFrom mechanism.
- Check balance of an address.

### Additional Features

#### Minting

The contract owner can mint new DegenToken tokens, thereby increasing the token supply.

#### Redemption

Users can redeem their DegenToken tokens for in-game items based on predefined redemption thresholds. Two types of packs are available for redemption:

- **Super Pack**: Requires a large amount of tokens for redemption.
- **Normal Pack**: Requires a smaller amount of tokens for redemption.

Redemption is handled by calling the `redeem` function, which deducts the specified amount of tokens from the user's balance and records the redeemed items accordingly.

#### Burning

Users can burn their DegenToken tokens, effectively reducing the token supply.

## Security

### Owner Access Control

Certain critical functions, such as minting new tokens, can only be executed by the contract owner. This access control mechanism ensures that only authorized entities can modify the token supply.

### Input Validation

The contract includes input validation checks to prevent invalid operations, such as transferring negative amounts or redeeming an unsupported quantity of tokens.

## Usage

### Deployment

Deploy the DegenToken contract to the Ethereum blockchain, specifying the initial token supply and other parameters.

### Interacting with the Contract

Users can interact with the DegenToken contract through various Ethereum-compatible interfaces such as web3.js, ethers.js, or directly through Ethereum wallet applications like MetaMask.

#### Minting Tokens

Only the contract owner can mint new tokens. To mint tokens, call the `mint` function with the desired recipient address and the amount of tokens to be minted.

#### Transferring Tokens

Tokens can be transferred between addresses by calling the `transfer` function, providing the recipient's address and the amount of tokens to transfer.

#### Redeeming In-Game Items

Users can redeem in-game items by calling the `redeem` function with the desired amount of tokens. The contract automatically validates the redemption amount and records the redeemed items for the user.

#### Burning Tokens

Users can burn their tokens by calling the `burn` function with the amount of tokens they wish to burn.

### Security Considerations

When interacting with the contract, ensure that you trust the deployed contract and review its source code to understand its functionalities and potential risks.

## License

DegenToken is licensed under the MIT License, which allows for free usage, modification, and distribution of the software.

---

This README provides an overview of the DegenToken contract, its functionalities, and usage instructions. For detailed technical specifications and implementation details, refer to the contract source code and comments.
