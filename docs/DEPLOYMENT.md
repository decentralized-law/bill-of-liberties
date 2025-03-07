# Deployment Guide

This document provides step-by-step instructions for deploying the Decentralized Bill of Liberties smart contract to the Ethereum blockchain.

## Prerequisites

Before deployment, ensure you have:

- MetaMask or another Ethereum wallet with sufficient ETH for gas fees
- Basic understanding of Ethereum transactions
- Familiarity with Remix IDE or another Solidity development environment

## Optional: Customizing the Contract Text

If you want to deploy your own custom text instead of the Decentralized Bill of Liberties:

1. **Open the contract file** `DecentralizedBillOfLiberties.sol`
2. **Modify the constructor function** to set your own title and text:
```solidity
constructor() {
    title = "Your Custom Title";
    text = "Your custom text goes here.\n\nUse \\n for line breaks.\n\nMake sure to keep proper formatting.";
}
```
### Text Formatting Tips
- Use `\n` for line breaks
- Keep the text well-structured
- The text is stored permanently, so review carefully before deployment

## Deployment Options

### Option 1: Deploy to Sepolia Testnet (For Testing)
Before deploying to Mainnet, you may want to test on Sepolia:

1. **Get Sepolia ETH**
   - Use a Sepolia faucet to obtain Sepolia
   - Request test ETH to your wallet address

2. **Configure MetaMask for Sepolia**
   - In MetaMask, click on the network dropdown
   - Select "Sepolia Test Network"

3. **Follow the Remix steps below**
   - Make sure your wallet is connected to Sepolia
   - Deploy following the same steps as Option 2

4. **Test the Contract**
   - Use the Remix interface to call the `title()` and `text()` functions
   - Verify that the correct text is returned

### Option 2: Deploy using Remix IDE (Beginner-Friendly)
1. **Access Remix IDE**
   - Go to Remix IDE

2. **Create a New File**
   - Click the "+" icon in the file explorer
   - Name it `DecentralizedBillOfLiberties.sol`
   - Copy and paste the contract code from this repository

3. **Compile the Contract**
   - Select the "Solidity Compiler" tab from the left sidebar
   - Choose compiler version 0.8.20
   - Click "Compile DecentralizedBillOfLiberties.sol"

4. **Deploy the Contract**
   - Select the "Deploy & Run Transactions" tab
   - Set the environment to "Injected Provider - MetaMask" (connects to your wallet)
   - Click "Deploy"
   - Confirm the transaction in your wallet

5. **Verify Contract**
   - After deployment, note the contract address
   - You can verify your contract on Etherscan for public transparency

## After Deployment
1. **Record the Contract Address**
  - This is crucial for frontend integration
  - Update the address in your frontend code

2. **Verify on Etherscan** *(Recommended)*
  - This allows anyone to view and interact with your contract
  - Makes the code transparent to all users

3. **Test the Frontend Integration**
  - Try the frontend code with your new contract address
  - Ensure it successfully retrieves and displays the text

**Note**: The contract is read-only after deployment, so no ongoing costs are associated.


