# PumpFun Bundler

A powerful Solana token launch and distribution tool that creates tokens on PumpFun and distributes them across 20 wallets and distribute to 200 wallets without triggering flags on popular tracking platforms like Photon, GMGN.ai, and Bullx Neo.

## 📩 Contact Me on Telegram

For inquiries, collaborations, or support, feel free to reach out:

[![Telegram Contact](https://img.shields.io/badge/Telegram-Contact%20Me-blue?logo=telegram&style=for-the-badge)](https://t.me/cashblaze127)
## These are related images
![create](https://github.com/user-attachments/assets/eca3c3d7-ab0b-4c6f-9579-2cd9510de4fb)
![buy](https://github.com/user-attachments/assets/49eda38f-ae1c-423b-abcb-364ed568badc)
![gmgn](https://github.com/user-attachments/assets/f8b25fd9-e29e-4f28-9fbb-7186765f7bb7)
![bullx neo](https://github.com/user-attachments/assets/04de42fc-1aff-400d-bd47-f472a2c2ee40)



## What This Tool Does

This bundler automates the entire token launch process on PumpFun:

1. **Token Creation**: Creates a new token on the PumpFun platform with your custom metadata
2. **Smart Distribution**: Distributes SOL across multiple wallets (20-200 wallets)
3. **Coordinated Buying**: Executes simultaneous token purchases across all wallets
4. **Natural Trading Pattern**: Uses randomized amounts and timing to appear organic
5. **Token Redistribution**: Further distributes tokens to create more realistic holder patterns

## Key Features

- **Stealth Mode**: Designed to avoid detection by popular Solana tracking tools
- **Jito Integration**: Uses Jito bundling for faster, more efficient transactions
- **Lookup Tables**: Optimizes transaction costs through address lookup tables
- **Randomized Patterns**: Implements random variations in amounts and timing
- **Multiple Wallet Management**: Handles hundreds of wallets seamlessly

## Prerequisites

Before you start, make sure you have:

- **Node.js** (v20.18.0 or higher)
- **Sufficient SOL** in your main wallet (typically 57 SOL depending on scale)
- **RPC Endpoint** (Helius, QuickNode, or similar with high rate limits)
- **Basic understanding** of Solana and token launches

## Installation

1. Clone this repository:
```bash
git clone https://github.com/cashblaze127/pumpfun-bundler.git
cd pumpfun-bundler
```

2. Install dependencies:
```bash
npm install
```

3. Create your configuration file (see Configuration section below)

## Configuration

Create a `constants.ts` file with your settings:

```typescript
// Your main wallet private key (base58 encoded)
export const PRIVATE_KEY = "your_private_key_here"

// Number of wallets to distribute tokens to (20-200)
export const DISTRIBUTION_WALLETNUM = 50

// Token information
export const TOKEN_NAME = "Your Token Name"
export const TOKEN_SYMBOL = "SYMBOL"
export const TOKEN_SHOW_NAME = "Display Name"
export const DESCRIPTION = "Your token description here"

// Social links (optional)
export const TWITTER = "https://twitter.com/your_handle"
export const TELEGRAM = "https://t.me/your_channel"
export const WEBSITE = "https://your-website.com"

// Token image file path
export const FILE = "./path/to/your/token/image.png"

// RPC Configuration
export const RPC_ENDPOINT = "https://your-rpc-endpoint.com"
export const RPC_WEBSOCKET_ENDPOINT = "wss://your-ws-endpoint.com"

// Trading amounts
export const SWAP_AMOUNT = 0.1 // SOL amount per wallet
export const SWAP_AMOUNT_TOKEN = 1000000 // Token amount (adjust based on your needs)

// Jito tip amount (in SOL)
export const JITO_FEE = 0.01
```

## How to Use

### Step 1: Prepare Your Wallet
Make sure your main wallet has enough SOL. The tool will calculate the exact amount needed based on your settings, but typically you'll need:
- 50-100 SOL for 20-50 wallets
- 100-200 SOL for 50-200 wallets

### Step 2: Set Up Token Assets
1. Prepare your token image (PNG/JPG format)
2. Update the `FILE` path in your constants
3. Fill in all token metadata (name, symbol, description, social links)

### Step 3: Run the Bundler
```bash
npm start
```

The tool will:
1. Create your token on PumpFun
2. Generate and fund multiple wallets
3. Create a lookup table for efficiency
4. Execute coordinated token purchases
5. Redistribute tokens for natural distribution

### Step 4: Monitor Progress
The tool provides detailed console output showing:
- Wallet generation and funding
- Token creation transaction
- Purchase transactions across all wallets
- Distribution transactions

## Understanding the Process

### Phase 1: Token Creation
- Generates a new mint keypair
- Creates token metadata and uploads to IPFS
- Submits token creation transaction to PumpFun

### Phase 2: Wallet Setup
- Generates specified number of wallets
- Calculates required SOL for each wallet
- Distributes SOL from main wallet to generated wallets

### Phase 3: Coordinated Buying
- Creates lookup table for transaction efficiency
- Prepares buy instructions for all wallets
- Bundles transactions using Jito for simultaneous execution

### Phase 4: Token Distribution
- Further distributes tokens among additional wallets
- Uses random variations to create natural holder patterns
- Keeps some tokens in original wallets for realistic distribution

## Important Notes

### Security Considerations
- **Never share your private keys**
- **Use a dedicated wallet** for bundling operations
- **Test with small amounts first**
- **Keep backups** of all generated wallet files

### Cost Estimation
- Typical cost: 0.1-0.3 SOL per wallet (including Jito fees)
- Additional costs: Token creation (~0.02 SOL) and network fees
- Always have 20% extra SOL as buffer for price fluctuations

### Best Practices
- **Start small**: Test with 20-30 wallets first
- **Monitor transactions**: Check Solscan links provided in console
- **Timing matters**: Avoid peak network congestion hours
- **Stay updated**: PumpFun may change their contract, update accordingly

## Troubleshooting

### Common Issues

**"Buyer wallet balance is not enough"**
- Solution: Add more SOL to your main wallet

**"Lookup table not ready"**
- Solution: Wait longer between LUT creation and usage

**"Transaction failed" errors**
- Solution: Check RPC endpoint health and rate limits

**Token creation fails**
- Solution: Verify all metadata is correct and image file exists

### Getting Help

If you encounter issues:
1. Check the console output for specific error messages
2. Verify your RPC endpoint is working properly
3. Ensure all configuration values are correct
4. Make sure you have sufficient SOL in your main wallet

## Disclaimer

This tool is for educational and legitimate business purposes only. Users are responsible for:
- Complying with all applicable laws and regulations
- Understanding the risks involved in token launches
- Using the tool ethically and responsibly
- Ensuring proper disclosure of token ownership distribution

**Use at your own risk.** Token launches involve significant financial risk, and past performance doesn't guarantee future results.

## Files Generated

The tool creates several files during operation:
- `data.json`: Contains generated wallet private keys
- `mint.json`: Contains token mint private key
- `lut.json`: Contains lookup table address
- `distribute.json`: Contains distribution wallet keys

**Keep these files secure and backed up!**

## Contributing

Feel free to submit issues and enhancement requests. This project is continuously being improved based on user feedback and platform changes.

---

*Remember: Successful token launches require more than just technical distribution. Focus on building a strong community, clear value proposition, and sustainable tokenomics.*
