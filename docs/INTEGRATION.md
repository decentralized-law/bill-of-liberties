# Website Integration Guide

This guide explains how to add the Decentralized Bill of Liberties to your website.

## Basic Implementation

1. **Download the file**
   - Download the `BillOfLibertiesFrontEnd.html` file from this repository

2. **Add to your website**
   - Copy the HTML code from the file
   - Paste it into any page on your website where you want to display the Bill of Liberties
   - **Important:** Many standard content management systems, such as Wordpress, require a specific 

3. **Key customization points**
   - Contract address: Change the `contractAddress` variable to point to your deployed contract
   - RPC URL: Modify the `rpcUrl` variable to use your preferred Ethereum node provider (you can leave this as is)
   - Styling: Adjust the `titleStyle` and `textStyle` variables to match your website's design

### Website Builder Implementation

When using website builders such as WordPress, Wix, Squarespace, or Shopify, you might need to use their specific HTML embedding features to add this code to your site. Look for options like "Custom HTML," "HTML Embed," "Code Block," or similar functionality in your website builder's interface. Make sure you're pasting the code in HTML mode rather than visual/text mode for proper functionality.

## Configuration Options

### Contract Address

```javascript
// Change this to your deployed contract address
const contractAddress = "0xdD7150425FE924f1e5D4d650AEBaA6365b1CB7dA";
```

### Ethereum Network URL

These are the default node settings for both Ethereum mainnet, and the Sepolia testnet. Feel free to pick any node (including your own).

```javascript
// Ethereum Mainnet (production)
const rpcUrl = "https://ethereum.publicnode.com";

// OR for Sepolia Testnet (testing)
// const rpcUrl = "https://ethereum-sepolia.publicnode.com";
```

## That's it!

The HTML file is self-contained with all necessary code to fetch and display the Bill of Liberties. No additional files or dependencies need to be installed on your server.
