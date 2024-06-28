# Creating a Token

This project demonstrates how to create a custom token on the Ethereum blockchain using Solidity, the primary programming language for smart contracts on Ethereum. The repository includes the Solidity source code, deployment scripts, and comprehensive instructions on how to set up and deploy your own token.

## Description

This project is an in-depth guide to creating a custom token on the Ethereum blockchain using Solidity. It covers the entire process from writing the Solidity code to deploying the token on the Ethereum network. The project aims to provide a clear understanding of the fundamental concepts of smart contracts and token creation, making it easier for developers to create their own tokens for various applications such as Initial Coin Offerings (ICOs), decentralized applications (dApps), and other blockchain-based projects.

### Key Features:
- **Token Creation**: Step-by-step instructions on writing and understanding the Solidity code necessary for token creation.
- **Deployment**: Detailed deployment scripts and methods to deploy the token on the Ethereum network.
- **Minting and Burning**: Explanation and implementation of minting (creating new tokens) and burning (destroying tokens) functionalities.
- **Comprehensive Guide**: Covers both basic and advanced concepts, suitable for beginners and experienced developers.

## Getting Started

To get started with this project, you'll need to have some basic knowledge of the Ethereum blockchain, Solidity programming, and how smart contracts work. The following sections provide instructions on how to set up your development environment, write the token contract, and deploy it on the Ethereum network.

### Prerequisites
- **Solidity**: Familiarity with Solidity programming language.
- **Remix IDE**: We will use Remix, an online Solidity IDE, to write and deploy our smart contract.

### Installing

1. **Remix IDE**: Visit [Remix IDE](https://remix.ethereum.org/).


### Executing Program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at [Remix IDE](https://remix.ethereum.org/).

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a `.sol` extension (e.g., `MyToken.sol`). Copy and paste the following code into the file:

```solidity
contract MyToken {

    // public variables here
    string public tokenName = "One_piece";
    string public tokenAbbrv = "Op";
    uint256 public totalSupply = 0;

    // mapping variable here
    mapping(address => uint256) public remainingBalance;

    // mint function
    function mintTokens(address recipient, uint256 quantity) public {
        totalSupply += quantity;
        remainingBalance[recipient] += quantity;
    }

    // burn function
    function burnMyTokens(address recipient, uint256 quantity) public {
        if (remainingBalance[recipient] >= quantity) {
            totalSupply -= quantity;
            remainingBalance[recipient] -= quantity;
        }
    }
}

```

### Compiling the Code

1. **Solidity Compiler**: Click on the "Solidity Compiler" tab in the left-hand sidebar.
2. **Compiler Version**: Set the "Compiler" option to "0.8.4" (or another compatible version).
3. **Compile**: Click on the "Compile MyToken.sol" button to compile the code.

### Deploying the Contract

1. **Deploy & Run Transactions**: Click on the "Deploy & Run Transactions" tab in the left-hand sidebar.
2. **Select Contract**: Select the "MyToken" contract from the dropdown menu.
3. **Deploy**: Click on the "Deploy" button to deploy the contract.

Once the contract is deployed, you can use the deployed contract interface in Remix to call functions like `mintTokens`, `burnMyTokens`, and view token balances.

## Authors

Sakshi  
[@Sakshi](https://pandeysakshi30899@gmail.com)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
