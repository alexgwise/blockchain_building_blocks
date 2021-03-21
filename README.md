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

- Network Name: zbank3 
- Network ID: 111
- Node 1 public address: 0xEBB3e5abF1A8c386C3d1C059F34aF8368ac6D720
- Node 1 password: 111
- Node 1 P2P Enode: enode://ad016c2d9bba778d9253c55c12f2fe7a9ca03dd4586361fb5a6d307c330c7a8dc0c4f93894e002e0ce1c4ab5977661aea9d4c9a097a5bf5ff1fc4763517481d7@127.0.0.1:30303
- Node 2 public address: 0x8976242C6C0e4De2509e084f34776B841788cF75 
- Node 2 password: 111

***To Get Started***

Prior to using this test network, make sure you have the following applications installed: 

***MyCrypto***

[MyCrypto](https://www.mycrypto.com/)

***Ethereum Blockchain Tools***

[Go Ethereum](https://geth.ethereum.org/)

You will also need the Node1 and Node2 folders contained in this GitHub repository. 

To activate the two nodes on this blockchain network, run the following commands in Git Bash. Make sure you have navigated to the folder where your Geth tools are located.

**./geth --datadir node1 --unlock "0xEBB3e5abF1A8c386C3d1C059F34aF8368ac6D720" --mine --minerthreads 1

**./geth --datadir node2 --unlock "0x8976242C6C0e4De2509e084f34776B841788cF75" --port 30304 --rpc --bootnodes "enode://ad016c2d9bba778d9253c55c12f2fe7a9ca03dd4586361fb5a6d307c330c7a8dc0c4f93894e002e0ce1c4ab5977661aea9d4c9a097a5bf5ff1fc4763517481d7@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock 


## How the Network was Created

With Puppeth, a new genesis was configured from scratch. Please note: Due to a bug unable to be resolved in class, this network relies on a proof of work rather than proof of authority consensus algorithm. Each account was prefunding, and the resulting .json file was exported. 

![Genesis](https://github.com/alexgwise/blockchain_building_blocks/blob/main/screenshots/zbank3%20configuration.PNG)

Next, each of the two nodes were created. The following command was used for node1, and repeated for node2: ./geth account new --datadir node1
The resulting public and secret keys were copied and pasted into the network info .txt file. 

![Node1](https://github.com/alexgwise/blockchain_building_blocks/blob/main/screenshots/Node%201%20Creation.PNG)

![Node2](https://github.com/alexgwise/blockchain_building_blocks/blob/main/screenshots/Node%202%20Creation.PNG)

Next, each node was initialized using the .json saved from our initial network configuration

![Initialized](https://github.com/alexgwise/blockchain_building_blocks/blob/main/screenshots/Node%201%20initialized.PNG)

![Initialized](https://github.com/alexgwise/blockchain_building_blocks/blob/main/screenshots/Node%202%20initialized.PNG)

I was then able to start up the mining process on node1 with the following command:
**./geth --datadir node1 --mine --miner.threads 1**
The resulting P2P enode was copied and saved for later use with node2

![Initialized](https://github.com/alexgwise/blockchain_building_blocks/blob/main/screenshots/node%201%20mining%20enabled.PNG)

![Initialized](https://github.com/alexgwise/blockchain_building_blocks/blob/main/screenshots/successful%20mining.PNG)

A 2nd port for node2 was then established

![2nd port](https://github.com/alexgwise/blockchain_building_blocks/blob/main/screenshots/node%202%20new%20port%20created.PNG)

***Now that both nodes are successfully up and running, a test transaction can be performed in MyCrypto.***

In My Crypto, I created a custom node using the network info below. I then sent a test transaction from node 1 to node 2 of 25 ETH after logging in with my private key. 

The first screenshot below show node2 receiving this test transaction. The second screenshot shows MyCrypto acknowledging the successful transaction. 

![node2 receipt](https://github.com/alexgwise/blockchain_building_blocks/blob/main/screenshots/node%202%20receipt%20of%20transaction.PNG)

![success](https://github.com/alexgwise/blockchain_building_blocks/blob/main/screenshots/Successful%20transaction.PNG)


### Thanks for taking the time to check out my test network ###

