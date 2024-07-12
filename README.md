# NFT-project

This project involves creating a 5-item NFT collection using DALLE 2 or Midjourney, storing these items on IPFS using pinata.cloud, deploying an ERC721 or ERC1155 contract to the Goerli Ethereum Testnet, and transferring them to Polygon Mumbai using the FxPortal Bridge.

## Steps to Set Up and Deploy:

### 1. Generate NFT Collection

Use DALLE 2 or Midjourney to generate a unique 5-item NFT collection.

### 2. Store Items on IPFS

Upload generated NFT items to IPFS for decentralized storage using [pinata.cloud](https://pinata.cloud).

### 3. Deploy Contract on Goerli Ethereum Testnet

Deploy an ERC721 or ERC1155 contract to the Goerli Ethereum Testnet. This contract will manage the minting and transfer of your NFTs.

### 4. Implement `promptDescription` Function

Ensure your contract includes a `promptDescription` function that returns the prompt used to generate the images for transparency and authenticity.

### 5. Map NFT Collection Using Polygon Network

(Optional) Map your NFT collection using the Polygon network token mapper for easier visualization and management.

### 6. Hardhat Scripts

#### Batch Minting (ERC721A)

Write a Hardhat script (`batchMint.js`) to batch mint all NFTs. This script will facilitate efficient minting of your entire collection.

#### Batch Transfer to Polygon Mumbai

Write another Hardhat script (`batchTransfer.js`) to batch transfer all NFTs from Ethereum to Polygon Mumbai using the FxPortal Bridge. Steps include:
- Approving NFTs for transfer.
- Depositing NFTs to the FxPortal Bridge for cross-chain transfer.

### 7. Testing

Test the functionality by:
- Using `balanceOf` on the Polygon Mumbai network to verify NFT balances post-transfer.

## Project Structure

- **contracts/**: Contains Solidity smart contracts.
- **scripts/**: Holds Hardhat scripts for minting and transferring NFTs.
- **tests/**: Includes test scripts to verify contract functionality.

## Dependencies

Ensure you have Node.js and Hardhat installed globally. Install additional dependencies using:

```bash
npm install
```

## Usage

1. **Compile Contracts**: Compile Solidity contracts using Hardhat.
   
   ```bash
   npx hardhat compile
   ```

2. **Run Hardhat Scripts**: Execute Hardhat scripts for minting and transferring NFTs.

   ```bash
   npx hardhat run scripts/batchMint.js --network goerli
   npx hardhat run scripts/batchTransfer.js --network mumbai
   ```

3. **Test**: Run tests to ensure proper functionality.

   ```bash
   npx hardhat test
   ```

## Additional Notes

- Ensure proper configuration of `.env` files for network variables and API keys.
- Customize scripts and contract functionality as needed for specific project requirements.

---
