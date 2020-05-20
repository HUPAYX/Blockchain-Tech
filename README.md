# 1. Blockchain
## •  Overview
The most important elements in a blockchain-based payment platform is performance, completeness and stability of the transaction. Existing PoW-based chains cannot be used in the real everyday payments because of the relatively long block time. Considering these points, as a result of comparative analysis of multiple blockchains, HUPAYX's Blockchain MainNet was built on Cosmos Chain.

Cosmos Blockchain is a revolutionary type of "internet of blockchains", which utilizes dPOS (delegated proof-of-stake) through Tendermin (It's a class of protocols which solve consensus under partially synchronous communication) consensus algorithm and solves problems associated with Scalability and Interoperability of blockchain related solutions.

Blockchain technology faces many challenges before it can become a foundational technology for everyday life. One of these is "interoperability". This refers to the inability of different blockchains to communicate with each other and share information. This is why Bitcoin cannot be exchanged for Ethereum without using a third-party exchange or application.
The nature of the design of blockchains means they can only communicate with themselves and not with other blockchains. They are not inherently interoperable. They start out isolated from one another. No information can be directly transferred between them.
However, Cosmos is a network of many independent blockchains called Zones, and Hubs are 'multi-asset proof-of-stake cryptocurrency' that allow the network to adapt and upgrade through a simple governance mechanism. Hubs and Zones of the Cosmos network communicate with each other through the Inter-blockchain communication (IBC) protocol. Tokens can be securely and quickly transferred from one zone to another through a hub without the exchange liquidity between the zones. Cosmos Hub tracks the total amount of tokens held by each zone, and anyone can connect a new zone to Cosmos Hub, making it compatible with the new blockchain. In this private MainNet release, HUPAYX has successfully developed and integrated those Zones to its MainNet.

HUPAYX's payment system has the same characteristics as above, which ensures the speed and completeness of payment settlement, as well as blockchain stability and infinite scalability.

## •  Tendermint Consensus Protocol

Tendermint is a partial Synchronous Byzantine Fault Tolerant (BFT) consensus protocol derived from the DLS consensus algorithm. Tendermint is a consensus algorithm that blends the Delegated Proof-of-Stake (DPoS) concept with the PBFT concept. Many validators who maintain a stable network and participate in governance will be paid for the block generation, and the holders of 'HPX' (Staking Token, formerly HUP) can be delegated to any validators and rewarded in HPX.

## •  Features

① Public or Private Blockchain Support:
Tendermint is a blockchain engine that deals only with the networking and consensus layers of the blockchain. In other words, Tendermint engine handles the process by which nodes propagate transactions and the validators agree to add a set of identical transactions to the blockchain. Laws and regulations, such as how a validator is elected, are determined at the application layer. Therefore, developers can create both public and private chains based on Tendermint. If the application layer selects the validator's selection criteria as 'how many coins are bundled', the blockchain becomes a POS (Proof-Of-Stake) blockchain. However, if the verifier in the application layer specifies that only limited subjects can be verified, the blockchain becomes a private blockchain based on proof-of-authority (POA). Developers are free to set the criteria for selecting the validator of their blockchain.
![Image description](https://drive.google.com/file/d/1opxsaKyTIg3U6nUXnUwOLIkeNSmsrsGs/view?usp=sharing)

② High Performance:
Tendermint cores have a block time of about 1 second and process thousands of transactions per second.

③ Instant Finality:
The Tendermint consensus algorithm is characterized by immediate completeness. This means that forks will never occur unless more than ⅓ of validators engage in Byzantine behaviour. Users can be assured that their transaction is complete as soon as the block is created.

④ Security
Tendermint consensus has accountability as well as Byzantine Fault Tolerance. If a fork occurs in the blockchain, it is possible to determine which validator is responsible for the fork.

⑤ Inter-Blockchain Communication (IBC)
Tokens can be held by an individual user or by the zone itself, and can be transferred from one zone to another through special IBC packets called "coin packets." The IBC protocol can be defined in two variants: the IBCBlockCommitTx variant, where the blockchain proves the latest block hash to any observer, and the blockchain sends the packet to the recent block hash by the sender's application through Merkle authentication. There is an IBCPacketTx variant that proves it did. By dividing the IBC driving scheme into the above two, the recipient chain's internal fee market mechanism can determine which packets will be committed and freely determine how many outbound packets the transmission chain will allow.

## •  Blockchain Structure
![Image description](https://cdn-images-1.medium.com/max/800/1*QbG0lfYhKcb1ZAxFRnbWCA.png)
① Tendermint Core (Consensus Algorithm)
②ABCI
Blockchain can be functionally divided into three layers. It's the networking, consensus, and application layers. Prior to Tendermint, all three layers had to be developed from scratch to develop blockchain. This requires a lot of time and effort. In this reality, Tendermint's goal is to make blockchain development easier by providing a standard engine that is responsible for the networking and consensus layers. The only thing developers need to care about is the application layer. The interface that connects the application layer, or state machine, to the consensus engine, is a socket protocol called Tendermint ABCI. You can create application layers using various development languages and then connect to Tendermint through ABCI.

③ Cosmos SDK
The Cosmos SDK is a generalized framework that simplifies the process of building secure blockchain applications on the Tendermint core. It is based on two main principles:

•  Modularity: The Cosmos SDK, like all Cosmos tools, is designed to be modular. The goal of the Cosmos SDK is to create a modular ecosystem that allows developers to easily launch application-specific blockchains without having to code each feature of the application from scratch. Anyone can create a module for the Cosmos SDK, and using a module prepared on the blockchain is as simple as importing the module into your application. For example, the Tendermint team is building a basic set of modules for the Cosmos Hub. These modules can be used by developers to build their own applications. Developers can also create new modules to customize their applications. As the Cosmos Network evolves, the SDK module ecosystem will expand to make it easier to develop complex blockchain applications.
•  Feature-based security: Features limit the security boundaries between modules, allowing developers to reason more about the module's configurability and limit the range of malicious or unexpected interactions. Cosmos SDK also comes with useful development tools for building command line interfaces (CLI), REST servers, and many other commonly used utility libraries.

Due to the above layered structure, it is possible to develop various dAPPs by providing developers with more flexible scalability than virtual machine-based blockchain platforms such as Ethereum, and the development speed is also faster.

# 2. Block Tracker
HUPAYX-HUB - a tool for monitoring status, blocks and transactions tracking

① Main Screen

• Status dashboard

• Search function

• Block lookup

• Transaction lookup

• Validator Data

• Governance Voting

![Image description](https://cdn-images-1.medium.com/max/2560/1*sBBKCeYhTFmZ-NAAyZhXbw.png) Example of the HUPAYX Explorer (HUPAYX-HUB)
![Image description](https://cdn-images-1.medium.com/max/2560/1*fEdOZRnIF9_NBxSRhxvRcA.png) 

② Block Search Screen

• Block List

• Block Detail Lookup

![Image description](https://cdn-images-1.medium.com/max/2560/1*MdlQmnb7pMelu0Wh6DO5xw.png)

③ Transaction Inquiry screen

• Transaction List

• Query Transaction Details

![Image description](https://cdn-images-1.medium.com/max/2560/1*chvU7FK55lH0DByMmeH8-g.png)

④ Validator inquiry screen

• Validator List

• Validator Rankings (Voting Power Order)

• Inquiry of Validator information such as commission
![Image description](https://cdn-images-1.medium.com/max/2560/1*mVOLI0mfvwf3q-Dy4dy2dA.png)



