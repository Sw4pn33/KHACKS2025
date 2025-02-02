Here is the complete `README.md` file in proper format for you to copy and paste directly into your GitHub repository:

```markdown
<h1 align="center">
  <br>
  <a><img src="https://github.com/rishav4101/eth-supplychain-dapp/blob/main/images/logo.png" width="200"></a>
  <br>  
  Blockchain-Based Supply Chain Verification System
  <br>
</h1>

<p align="center">
  <a href="https://github.com/trufflesuite/ganache-cli">
    <img src="https://github.com/rishav4101/eth-supplychain-dapp/blob/main/images/ganachetrans.png" width="90">
  </a>
  <a href="https://soliditylang.org/">
    <img src="https://github.com/rishav4101/eth-supplychain-dapp/blob/main/images/Solidity.svg" width="80">       
  </a>
  <a href="https://reactjs.org/"><img src="https://github.com/rishav4101/eth-supplychain-dapp/blob/main/images/react.png" width="80"></a>
  
  <a href="https://www.trufflesuite.com/">
    <img src="https://github.com/rishav4101/eth-supplychain-dapp/blob/main/images/trufflenew.png" width="50">
  </a>
   &nbsp;&nbsp;&nbsp;
  <a href="https://www.npmjs.com/package/web3">
    <img src="https://github.com/rishav4101/eth-supplychain-dapp/blob/main/images/web3.jpg" width="60">
  </a>
  
  <a href="https://material-ui.com/">
    <img src="https://github.com/rishav4101/eth-supplychain-dapp/blob/main/images/mat.png" width="60">       
  </a>
  &nbsp;&nbsp;&nbsp;
  <a href="https://expressjs.com/"><img src="https://github.com/rishav4101/eth-supplychain-dapp/blob/main/images/express.svg" width="50"></a>
  &nbsp;&nbsp;
  <a href="https://www.nginx.com/">
    <img src="https://github.com/rishav4101/eth-supplychain-dapp/blob/main/images/nginx.png" width="80">
  </a>
</p>

<h4 align="center">A blockchain-based system for transparent and secure supply chain verification using <a href="https://docs.soliditylang.org/en/v0.8.4/" target="_blank">Solidity</a>.</h4>

<p align="center">
  <a >
    <img src="https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen.svg">
       
  </a>
  <a href="https://github.com/rishav4101/eth-supplychain-dapp/issues"><img src="https://img.shields.io/github/issues/rishav4101/eth-supplychain-dapp.svg"></a>
  
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/license-MIT-green.svg">
  </a>
</p>

<p align="center">
  <a href="#description">Description</a> •
  <a href="#features">Features</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#flow">Flow</a> •
  <a href="#installation-and-setup">Installation and Setup</a> •
  <a href="#license">License</a>
</p>

## Description
Traditional supply chain systems often lack transparent verification mechanisms, leading to issues like counterfeiting and security breaches, especially in critical industries such as pharmaceuticals and electronics. This project aims to develop a blockchain-based verification system that tracks and authenticates products throughout the supply chain. The system uses QR codes or NFC tags to enable real-time tracking and verification, ensuring product authenticity and preventing counterfeiting.

## Features
- **Smart Contract Implementation**: Automated verification using smart contracts.
- **Real-Time Product Tracking Dashboard**: A dashboard for real-time tracking of products.
- **Mobile App**: QR/NFC scanning and verification through a mobile app.
- **Incident Reporting and Alert System**: A system for reporting incidents and sending alerts.

## Architecture
The system is built using Solidity for smart contracts, which are compiled, migrated, and deployed using Truffle.js on a local blockchain network created with Ganache-cli. The frontend, developed using React.js, communicates with the smart contract and the local blockchain network via Web3.js. Nginx is used as a load balancer, and Express.js handles dynamic routing.

<p align="centre">  
    <img src="https://github.com/rishav4101/eth-supplychain-dapp/blob/main/images/architecturefinal.png?raw=true" >  
</p>

## Flow
<p align="centre">  
    <img src="https://github.com/rishav4101/eth-supplychain-dapp/blob/main/images/flow.png" width="300">  
</p>

## Installation and Setup
Prerequisites : `npm, git, docker(optional)`

Clone the repository 
```Bash
git clone https://github.com/rishav4101/eth-supplychain-dapp.git && cd eth-supplychain-dapp
```
Install dependencies
```Bash
npm i
```
Install ganache-cli
```Bash
npm i -g ganache-cli
```
Configure ganache-cli for 10 accounts and extend gasLimit to 6721975000 and beyond, so as to have enough gas for migrating the smart contracts and a data flow for the prototype.  
```Bash
ganache-cli --accounts 10 --gasLimit 6721975000
```
If you want to run the ganache-cli on docker then use the following command
```Bash
sudo docker run -d -p 8545:8545 trufflesuite/ganache-cli:latest -h 0.0.0.0 --accounts 10 --gasLimit 6721975000
```
Migrate the contracts
```Bash
truffle migrate --network=develop --reset
```
Open a second terminal and enter the client folder
```Bash
cd client
```
Install all packages in the package.json file
```Bash
npm i
```
Setup an .env file using the `nano .env` command and enter the google maps api key and set the react rpc port to 8545 since the ganache-cli runs on the same port by default.
The final .env file must look like this
```Bash
REACT_APP_GOOGLE_MAP_API_KEY=*************************
REACT_APP_RPC=http://127.0.0.1:8545/

```
Run the app
```Bash
npm start
```
The app gets hosted by default at port 3000.

## License
This project uses an [MIT](https://opensource.org/licenses/MIT) license.
## Documentation to help with Solidity
https://docs.soliditylang.org/en/v0.8.4/
## Documentation to help with React
https://reactjs.org/docs/getting-started.html
## Documentation to help with Truffle
https://www.trufflesuite.com/docs/truffle/reference/configuration
## Documentation to help with Ganache-cli
https://www.trufflesuite.com/docs/ganache/overview
```

You can now copy and paste this content directly into your `README.md` file on GitHub.
