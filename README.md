# blockchain_building_blocks

## ZBank3 Blockchain Test Network ##

Welcome to my test blockchain network. This README file will walk you through the steps I took to create the network and successfully transmit a test transaction, including:

- Configuring the network and creating a genesis block
- Node 1 & 2 creation
- Node 1 & 2 initialization
- Enabling Node 1 mining
- Creating a 2nd port for Node 2
- Successful transmission of a test transaction

### Some Key Info About the Network ###

* Network Name: zbank3 
* Network ID: 111
* Node 1 public address: 0xEBB3e5abF1A8c386C3d1C059F34aF8368ac6D720
* Node 1 password: 111
* Node 1 P2P Enode: enode://ad016c2d9bba778d9253c55c12f2fe7a9ca03dd4586361fb5a6d307c330c7a8dc0c4f93894e002e0ce1c4ab5977661aea9d4c9a097a5bf5ff1fc4763517481d7@127.0.0.1:30303
* Node 2 public address: 0x8976242C6C0e4De2509e084f34776B841788cF75 
* Node 2 password: 111

* To Get Started

Prior to using this test network, make sure you have the following applications installed: 

* MyCrypto

[MyCrypto](https://www.mycrypto.com/)

* Ethereum blockchain tools

[Go Ethereum](https://geth.ethereum.org/)

You will also need the Node1 and Node2 folders contained in this GitHub repository. 

To activate the two nodes on this blockchain network, run the following commands in Git Bash. Make sure you have navigated to the folder where your Geth tools are located.

./geth --datadir node1 --unlock "0xEBB3e5abF1A8c386C3d1C059F34aF8368ac6D720" --mine --minerthreads 1

./geth --datadir node2 --unlock "0x8976242C6C0e4De2509e084f34776B841788cF75" --port 30304 --rpc --bootnodes "enode://ad016c2d9bba778d9253c55c12f2fe7a9ca03dd4586361fb5a6d307c330c7a8dc0c4f93894e002e0ce1c4ab5977661aea9d4c9a097a5bf5ff1fc4763517481d7@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock 


## How the Network was Created

![catalina-allow-unidentified-app](Images/catalina-allow-unidentified-app.jpg)

note: due to bugs unabled to be resolved in class, this network relies on a proof of work rather than proof of authority consensus algorithm 