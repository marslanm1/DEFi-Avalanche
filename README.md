# DeFi Empire: A Simple DeFi Kingdom Clone

This project demonstrates the process of creating a simple DeFi Kingdom clone on the Avalanche blockchain using custom EVM subnets. The project involves the creation of an ERC20 token contract, a Vault contract, and integration with MetaMask.

## Overview

- **Blockchain**: Avalanche (EVM Subnet)
- **Smart Contracts**: ERC20 Token, Vault
- **Tooling**: Avalanche CLI, Remix IDE, MetaMask
- **Project Objective**: To create a decentralized gaming environment, where users can mint, transfer, deposit, and withdraw tokens.

## Table of Contents

1. [Installation](#installation)
2. [Creating a Subnet](#creating-a-subnet)
3. [Connecting to MetaMask](#connecting-to-metamask)
4. [Smart Contracts](#smart-contracts)
5. [Deployment](#deployment)
6. [Usage](#usage)
7. [Contributing](#contributing)
8. [License](#license)

## Installation

To begin, install the Avalanche CLI on your system:

```bash
curl -s https://install.avalanche.network | sudo bash
```

Check if the installation is successful:

```bash
avalanche --version
```

This command should display the installed version of the Avalanche CLI.

## Creating a Subnet

Create a custom subnet named `DEFII` for this project. Run the following command:

```bash
avalanche subnet create DEFII
```

- **Chain Type**: EVM
- **Native Currency**: Specify the name of the custom native currency.

The configuration details for the subnet will be generated by the Avalanche CLI.

## Connecting to MetaMask

To interact with the new subnet, it must be added to MetaMask:

1. Open MetaMask, click on **Add Network**.
2. Enter the following details:
   - **Network Name**: DEFII
   - **RPC URL**: Provided by Avalanche CLI.
   - **Chain ID**: The unique ID of the created subnet.
   - **Currency Symbol**: The native currency of the subnet.

Click **Save** to add the network to MetaMask. Ensure the MetaMask is switched to the DEFII subnet.

## Smart Contracts

### 1. ERC20 Token Contract

This contract implements a custom ERC20 token. Key functions include:

- **Mint**: Create new tokens.
- **Burn**: Destroy tokens.
- **Transfer**: Transfer tokens between users.
- **Approve & TransferFrom**: Allow spending on behalf of users.

### 2. Vault Contract

The Vault contract allows users to deposit ERC20 tokens and receive shares representing their stake in the Vault. Key functions include:

- **Deposit**: Users can deposit tokens and receive shares.
- **Withdraw**: Users can burn shares to get back tokens.

## Deployment

The contracts are deployed using Remix IDE:

1. Compile both **ERC20** and **Vault** contracts using Remix.
2. Connect to MetaMask by selecting **Injected Web3** in Remix.
3. Deploy the **ERC20** token contract first.
4. Use the token’s address to deploy the **Vault** contract.

## Usage

After deploying the contracts, you can interact with them:

### Minting and Transferring Tokens

1. **Mint Tokens**: Use the `mint` function to create tokens.
2. **Transfer Tokens**: Use the `transfer` function to send tokens to another address.

### Depositing and Withdrawing from Vault

1. **Deposit Tokens**: Use the `deposit` function of the Vault contract to deposit tokens and receive shares.
2. **Withdraw Tokens**: Use the `withdraw` function to burn shares and get back an equivalent amount of tokens.

## Contributing

If you would like to contribute to this project, please open an issue or submit a pull request with your suggestions and improvements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
