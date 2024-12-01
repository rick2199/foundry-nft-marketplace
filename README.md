# Foundry Ethereum Development Toolkit

**Foundry** is a blazing fast, portable, and modular toolkit for Ethereum application development written in Rust. It provides a comprehensive suite of tools to streamline the development, testing, and deployment of Ethereum smart contracts.

## Overview

Foundry consists of several key components:

- **Forge**: An Ethereum testing framework similar to Truffle, Hardhat, and DappTools. It allows developers to write and execute tests for their smart contracts efficiently.
- **Cast**: A versatile tool for interacting with EVM smart contracts, sending transactions, and retrieving chain data.
- **Anvil**: A local Ethereum node that functions similarly to Ganache and Hardhat Network, providing a sandbox environment for testing and development.
- **Chisel**: A fast, utilitarian, and verbose Solidity REPL (Read-Eval-Print Loop) for interactive contract development.

## Key Features

### Marketplace Contract

The Marketplace contract is a core component of this toolkit, enabling users to list, purchase, and auction NFTs. It includes features such as:

- **Listing and Purchasing**: Users can list their NFTs for sale and purchase listed NFTs. The contract handles the transfer of ownership and payment processing, including marketplace fees.
- **Auctioning**: The contract supports auctions, allowing users to start auctions for their NFTs, place bids, and end auctions. It uses a min-heap data structure to efficiently manage ongoing auctions.
- **Offers**: Users can make offers on listed NFTs, and sellers can accept or reject these offers.

### NFT Contract

The NFT contract provides a simple implementation of an ERC721 token, allowing users to mint and manage NFTs. It includes:

- **Minting**: Users can mint new NFTs with specified metadata URIs.
- **Token Management**: The contract tracks ownership and metadata of each token.

### Testing

The project includes a comprehensive suite of unit and fuzz tests to ensure the reliability and security of the contracts. Tests cover various scenarios, including:

- Listing and purchasing NFTs
- Auction lifecycle management
- Offer creation and acceptance
- NFT minting and metadata management

## Documentation

For detailed documentation, visit [Foundry's Book](https://book.getfoundry.sh/).

## Usage

### Build

To build the project, run:

```shell

forge build

```

### Test

To execute tests, run:

```shell

forge test

```

### Format

To format the code, run:

```shell

forge fmt

```

### Anvil

To start a local Ethereum node, run:

```shell

anvil

```

### Deploy

To deploy a contract, use the following command:

```shell

forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --account <your_account> --sender <your_sender>

```

### Cast

To interact with smart contracts, use:

```shell

cast <subcommand>

```

### Help

For help with any command, use:

```shell

forge --help

anvil --help

cast --help

```