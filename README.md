# HyperLedger-Fabric
BlockEstate is a revolutionary real estate transaction platform built on the Hyperledger blockchain framework. It leverages blockchain technology to enhance the efficiency, security, and transparency of property transactions. The platform employs a unique chaincode for property ownership management and a novel pay order mechanism.

## Key Features
The smart contract (in folder `chaincode-go`) implements the following functions to support the application:

- CreateAsset
- ChangePublicDescription
- AgreeToSell
- AgreeToBuy
- VerifyAssetProperties
- TransferAsset
- ReadAsset
- GetAssetPrivateProperties
- GetAssetSalesPrice
- GetAssetBidPrice
- GetAssetHashId
- QueryAssetSaleAgreements
- QueryAssetBuyAgreements
- QueryAssetHistory

### Usage
To deploy the chaincode on a Hyperledger network, follow the specific instructions provided in the deployment directory.
Use the provided APIs to interact with the blockchain for property transactions.

### Contributing
Contributions to BlockEstate are welcome. Please follow these steps to contribute:
- Fork the repository.
- Create a new branch (git checkout -b feature-branch).
- Make your changes and commit them (git commit -am 'Add new feature').
- Push to the branch (git push origin feature-branch).
- Create a new Pull Request.

### License
BlockEstate is licensed under the MIT License.

# Getting Started
To get started with BlockEstate, follow these steps:

### Prerequisites
- Install Hyperledger Fabric
- Install a supported programming language (Go, JavaScript)
- Install Docker & Docker-Compose
- Enable WSL (Windows Sub System for Linux) and Install Ubuntu (Skip if using Linux environment)
- Install Curl, Python 2.7, OpenSSL, Go, Node and npm

### Installation
Clone the repository:
   ```bash
   git clone [[repository-url]](https://github.com/LavizaFalakNaz/HyperLedger-Fabric.git)
   ```
   ``` bash
   cd Project/test-network
   ```
   ``` bash
   ./network.sh down
   ```
   ``` bash
   ./network.sh up createChannel -c mychannel -ca
   ```
   ``` bash
   ./network.sh deployCC -ccn secured -ccp ../asset-transfer-secured-agreement/chaincode-go/ -ccl go -ccep "OR('Org1MSP.peer','Org2MSP.peer')"
   ```
   ``` bash
   cd ../asset-transfer-secured-agreement/application-javascript
   ```
   ``` bash
   node app.js
   ```
