# Supply chain & data auditing

This repository containts an Ethereum DApp that demonstrates a Supply Chain flow between a Seller and Buyer. The user story is similar to any commonly used supply chain process. A Seller can add items to the inventory system stored in the blockchain. A Buyer can purchase such items from the inventory system. Additionally a Seller can mark an item as Shipped, and similarly a Buyer can mark an item as Received.

The DApp User Interface when running should look like...

![truffle test](images/ftc_product_overview.png)

![truffle test](images/ftc_farm_details.png)

![truffle test](images/ftc_product_details.png)

![truffle test](images/ftc_transaction_history.png)


## Library used
```
Truffle v5.7.0 (core: 5.7.0)
Ganache v7.5.0
Solidity v0.5.16 (solc-js)
Node v16.17.0
Web3.js v1.7.4
@truffle/hdwallet-provider v2.1.2
```

## Contract Address

The smart contract is deployed in the `goerli`-Network with following addresses:

### FarmerRole
[link](https://goerli.etherscan.io/address/0x88cb33f44929cb429d8f34999eb2bf8007a6ee58)
```
transaction hash:    0x30309beb39081fd6b0d88999b63585015a7c32f878f9ae1acb864c29d32e0c29
contract address:    0x88Cb33F44929cB429D8F34999eb2bf8007a6EE58
```
### DistributorRole
[link](https://goerli.etherscan.io/address/0x00c1092deeb7a4e33bd4904f9fa334528e1f496f)

```
transaction hash:    0x572afaf22cb199709702273de2609a68c9b4f7a9707f08134e438a7c30b286f6
contract address:    0x00C1092DEEb7A4E33BD4904f9fA334528e1f496F
```
### RetailerRole
[link](https://goerli.etherscan.io/address/0x1fc05d3ebc788dcde8f054a62f6e7b98b547db63)

```
transaction hash:    0xa3f95fc6abeab6f251ca1a55b11109ac7a893ccf9c45a4f5e17bd939224257d7
contract address:    0x1Fc05d3Ebc788Dcde8F054a62f6E7B98b547Db63
```
### ConsumerRole
[link](https://goerli.etherscan.io/address/0x406453e690a6ce3a5f9f65bf7faea166c32dedc6)

```
transaction hash:    0xf7305e937a01789378a5813a13924d2de091d38086acbce2f9826a3a02089432
contract address:    0x406453E690a6CE3a5f9F65BF7FAea166c32dEdc6
```

### SupplyChain
[link](https://goerli.etherscan.io/address/0xaa57cc93f5e9e558a77c84fb0edb58d435675224)

```
transaction hash:    0x01715ad82c68e6ea1b7aa2f1d851fb91b35ba3dcd6e45a7b9d460285d0f8e69e
contract address:    0xaA57cC93f5e9E558A77C84fB0eDB58D435675224    
```



## UML Diagram
The draw.io are used and the project located in [udacity_coffee_supply_chain.drawio](images%2Fudacity_coffee_supply_chain.drawio) .
### Activity Diagram
![udacity_coffee_supply_chain-activity.jpg](images%2Fudacity_coffee_supply_chain-activity.jpg)

### Sequence Diagram
![udacity_coffee_supply_chain-sequence.jpg](images%2Fudacity_coffee_supply_chain-sequence.jpg)

## State Diagram
![udacity_coffee_supply_chain-state.jpg](images%2Fudacity_coffee_supply_chain-state.jpg)

## UML Diagram
For this part, the library called [sol2uml](https://github.com/naddison36/sol2uml) will be used.  
```
cd project-6

# install sol2uml globally
npm link sol2uml --only=production 

# generate class diagram as svg
sol2uml class contracts -o ../images/udacity_coffee_supply_chain-class.svg
```
![udacity_coffee_supply_chain-class.svg](images%2Fudacity_coffee_supply_chain-class.svg)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Please make sure you've already installed ganache, Truffle and enabled MetaMask extension in your browser.

### Installing

Clone this repository:

```
git clone https://github.com/veectro/bdnd_project_3.git
```

Change directory to ```project-6``` folder and install all requisite npm packages (as listed in ```package.json```):

```
cd project-6
npm install
```

Launch Ganache:

```
ganache -m "spirit supply whale amount human item harsh scare congress discover talent hamster"
```

Your terminal should look something like this:

![truffle test](images/ganache-cli.png)

In a separate terminal window, Compile smart contracts:

```
truffle compile
```

Your terminal should look something like this:

![truffle test](images/truffle_compile.png)

This will create the smart contract artifacts in folder ```build\contracts```.

Migrate smart contracts to the locally running blockchain, ganache-cli:

```
truffle migrate
```

Your terminal should look something like this:

![truffle test](images/truffle_migrate.png)

Test smart contracts:

```
truffle test
```

All 10 tests should pass.

![truffle test](images/truffle_test.png)

In a separate terminal window, launch the DApp:

```
npm run dev
```

## Built With

* [Ethereum](https://www.ethereum.org/) - Ethereum is a decentralized platform that runs smart contracts
* [Truffle Framework](http://truffleframework.com/) - Truffle is the most popular development framework for Ethereum with a mission to make your life a whole lot easier.


## Acknowledgments

* Solidity
* Ganache
* Truffle
