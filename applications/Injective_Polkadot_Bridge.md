# Open Grant Proposal
* **Project Name:** Injective_Polkadot_bridge
* **Team Name:** Injective Protocol
* **Payment Address:** 0xc104B47ea3D9B854CE0F3628f3A4a0A1bCD482dD

## Project Overview :page_facing_up: 
### Brief Injective Protocol Overview
#### Decentralization
The Injective Chain is a fully-decentralized sidechain relayer network which serves as a layer- 2 derivatives platform,trade execution coordinator(TEC), and decentralized orderbook.The core consensus is Tendermint- based.

#### Speed
The Injective Chain provides a two-way Ethereum peg-zone for Ether and ERC-20 tokens to be transferred to the Injective Chain as well as an EVM-compatible execution environment for DeFi applications. The peg-zone is based off Peggy and the EVM execution is based off Ethermint.

#### Orderbook Model
Injective's Orderbook is a fully decentralized 0x-based orderbook enabling sidechain order relay with on - chain settlement - a decentralized implementation of the traditionally centralized off-chain order relay used by nearly all central limit order book decentralized exchanges.

#### Markets
Market creation is entirely open and permissionless. This enables anyone to create a market using only a price feed and deploy it to the larger Injective ecosystem.

#### Gas fees
Given the unique layer-2 structure, Injective is able to avoid both network congestion and the associated high gas fees.This zero gas fee structure can enable anyone to trade freely without having to worry about high gas fees or network latencies.

### Overview
#### The problems
Decentralized finance ecosystem and generally cryptocurrencies are getting more and more attention as years go by.
This big expose is digging up some of the big weaknesses of the ecosystem though.
The most important issues arised are:
 * Scalability
 * Fees
 * Connectivity
 
The first two issues are visible to the most popular cryptocurrencies, like Bitcoin and Ethereum. Especially on big market moves, blockchains like the previously mentioned ones, which are not designed to process a lot of transactions per second struggle to serve on market needs, which results in pending transactions forever if fees paid are not big enough.

A lot of cryptocurrencies' blockchains have been designed to solve those problems, without any of those establishing itself in the ecosystem. And that happens because the third issue exists, which is connectivity.

It is not overstatement to say that Ethereum is holding the decentralized finance's keys. Almost all assets and DEFI applications are part of its ecosystem and it is hard for them to move to other blockchains.

#### The solution
Thus the biggest challenge nowadays is to bridge assets (which also means decentralized applications) between different blockchains.

Polkadot ecosystem is creating big expectations for that reason. An ecosystem that is consisting of different parachains, which are easily communicating with each other. Polkadot will also be able to communicate with Ethereum Blockchain, while it will offer much lower fees and much more transactions per second.

For all those reasons, Polkadot is becoming more and more popular among cryptocurrencies and a huge variety of projects are trying to become part of its ecosystem.

#### The application
Injective Protocol is not in a different situation. A bridge for assets between Injective Chain and Moonbeam parachain, which is part of Polkadot ecosystem will benefit both ecosystems.

Injective Protocol is offering unlimited trading for assets inside the cryptocurrencies' ecosystem, but also for forex and stocks.

With this bridge, Polkadot users will be able to easily transfer their assets and enjoy trading on Injective exchange and then move their earnings back to Polkadot and benefit from all decentralized applications there.

To conclude with, this application could result in a very interesting win-win situation between Injective Protocol and Polkadot.

### Project Details
Generally, the bridge will allow assets to be transfered both ways. That means that tokens will be able to be transferred from their native chain to the other chain as wrapped tokens, but then also those wrapped assets can be transferred back to the native chain.  
  
The procedure will be exactly the same for both chains (same smart contracts, same relayer handling).  
  
The bridge will be consisted of three main parts:  
1) Smart Contracts  
2) Relayer Software  
3) UI  
  
#### Smart Contracts  
All smart contracts will be written in Solidity, as both Moonbeam and Injective support EVM based smart contract development.  
 
There will be created three smart contracts for the bridge's purpose:  
a) Depositor smart contract  
Depositor smart contract will be responsible to accept the deposits of the assets that users would like to bridge.  
Once the assets are deposited in this smart contract there will be locked, till an order from Multisig smart contract to unlock is given.  
 
b) Handler smart contract  
Handler smart contract will be actually the opposite of the depositor smart contract. When a deposit of an asset (native or wrapped) is happening on one chain, handler will be responsible for minting the same asset (wrapped or native) on the destination chain.  
 
c) Multisig smart contract  
Multisig smart contract will actually act as a voting contracts for the validators and as the owner of the handler. Validators, the number of which is yet to be determined, but it will be at least three, will need to reach consensus about the validity of a deposit, so as multisig smart contracts to provide permission for handler smart contract to mint.  
  
#### Relayer Software
Relayer software will be responsible for the smooth functioning of the whole bridge, as it will handle event listening and permission providing. 
 
The main relayers will actually be responsible to listen on the Deposit event of the entry chain and pass the data on the Multisig of the destination chain. 
There will be two main relayers one for each chain. 
 
There will be other relayers, called validators which will listen to the OpenVote event of Multisig. When such an event occurs means that validators will need to vote about the validity of the deposit. Validators will then need to sign their vote with their private keys and pass it to the Multisig. 
The last validator to reach the Multisig, will also trigger the vote result. 
 
If there is no consensus, VoteFailed event is triggered and the main relayer of the respective chain unlocks the deposit, so as user to be able to withdraw them back. 
 
If there is consensus assets are appearing to the destination chain on the wallet that depositor passed as input on the deposit function.

There will be also other features added, like cancellation of a deposit in case a transaction is taking too long to execute (because of low gas fee etc). 
Those features will be certainly provided alongside the Relayer Software milestone, because it is widely known that some edge cases cannot be considered before the real development starts. 

#### UI
Through the UI users will be able to interact with the bridge. It will contain web3 connection to both chains and the essential deposit tab.

### Ecosystem Fit 
As described above, bridging Polkadot assets with Injective, which is a limitless decentralized exchange will be a great utility for the ecosystem growth.

## Team :busts_in_silhouette:

### Team members
* Eric Chen (CEO)
* Albert Chon (CTO)
* Mirza Uddin (Head of Business Development)
* Maxim Kupriianov (Principal Engineer)
* Michael Siedlecki (Software Engineer)
* Markus Waas (Blockchain Engineer)
* Bojan Angjelkoski (Front-end Engineer)
* Alexandros Athanasopoulos (Blockchain Engineer)

### Contact
* **Contact Name:** Mirza Uddin
* **Contact Email:** mirza@injectiveprotocol.com
* https://injectiveprotocol.com/

### Legal Structure 
* **Registered Address:** P.O. Box 1350
Clifton House
75 Fort Street
Grand Cayman KY1-1008
Cayman Islands
* **Registered Legal Entity:** Injective Network Ltd.

### Team's experience
Eric Chen (CEO)-  Eric previously attended NYU Stern where he studied finance and computer science. Before founding Injective, he worked as a cryptography researcher and trader at Innovating Capital where he led innovative market neutral trading efforts in the blockchain space as well as investments into prominent companies such as 0x, ChainLink and Cosmos. Eric has extensive knowledge about blockchain protocols and traditional finance along with a native understanding of both eastern and western blockchain based protocols and communities. 

Albert Chon (CTO) - Albert previously attended Stanford University where he studied computer science and was involved in applied cryptography research advised under Dan Boneh (prominent Stanford cryptography Professor). Before founding Injective, he worked at Amazon as a software developer as well as Open Zeppelin. Albert invented the ERC-1178 token standard which was adopted by Loom Network for NFTs. Having lived in South Korea, Albert also has a keen understanding of the retail trading community in South Korea as well as relationships with key strategic partners in the region.

Mirza Uddin (Head of Business Development) - Mirza was previously on the investment team at Two Sigma (one of the largest hedge funds in the world), where he focused on investments into blockchain based technologies. He also was part of the investment team at Index Ventures. Prior to his work in VC and startups, Mirza held roles in management consulting at BCG and in investment banking. Mirza graduated with a BA from Harvard.

Maxim Kupriianov (Principal Engineer) - Maxim has 11 years of programming experience and has a diverse set of experience building back-end infrastructure at numerous startups. Prior to joining Injective, he was the lead blockchain engineer at Atlant where he led development of a real estate tokenization platform on top of Ethereum and authored the ERC-1462 security token standard. He notably also has 3 years of experience using Tendermint/Cosmos-SDK which he used in its early days to design an in-game blockchain based reward system for a distributed MMORPG at Gamma Innovations (acquired). Maxim is also an avid open-source contributor and is an expert in the Go programming language. 

Michael Siedlecki (Software Engineer) - Michael has 10 years of programming experience and was an early/founding-engineer at several Y-Combinator funded startups. He worked for 2 years at EMX where he worked full-stack on the company’s centralized crypto derivatives exchange. Coming from a centralized exchange that went head-to-head with FTX, Michael spearheaded multiple derivatives trading competitions and has a very good understanding of product and growth-hacking.

Markus Waas (Blockchain Engineer) - Markus has 10 years of programming experience and has over 8 years of crypto-specific experience. He began mining Bitcoin in 2012 and has worked at several blockchain companies/projects in the past. Before joining Injective, Markus was a smart contract engineer at Laminar/Acala where he created a Forex CFD margin trading platform on Ethereum. Markus also worked at Juri where he designed and implemented a new type of staking pool as well as a fully decentralized oracle system. Markus graduated from Humboldt University in Berlin where he wrote his master’s thesis on randomness on the blockchain and has won awards at numerous Ethereum hackathons including ETHBerlin and Blockstack Berlin. He is a Solidity expert and is the author of https://soliditydeveloper.com.

Bojan Angjelkoski (Front-end Engineer) - Bojan has 8 years of programming experience and has experience at multiple startups as a full-stack engineer. He has also previously worked at the prestigious World Trade Organization (WTO) as a full-stack engineer. Bojan holds both a B.S. and M.S. degree in Computer Science.

Alexandros Athanasopoulos (Blockchain Engineer) - Alex has 5 years of programming experience and has been developing on Ethereum for 3 years. Alex has a plethora of experience building decentralized applications and games on top of Ethereum. Some projects he worked prior to joining Injective include Global Crypto Alliance (a blockchain reputation-based incentivized news platform), Aries Blockchain (a no-code dApp startup) as well as numerous other projects involving escrows, insurance, and gaming. He is a graduate of the National Technical University of Athens where he wrote his masters thesis on decentralized finance.

### Team Code Repos
* https://github.com/InjectiveLabs

### Team LinkedIn Profiles
* https://www.linkedin.com/in/ericchenmelt/
* https://www.linkedin.com/in/albertchon/
* https://www.linkedin.com/in/themirzauddin/
* https://www.linkedin.com/in/mkupriianov/
* https://www.linkedin.com/in/michaelsiedlecki/
* https://www.linkedin.com/in/markuswaas/
* https://www.linkedin.com/in/bangjelkoski/
* https://www.linkedin.com/in/alexandros-athanasopoulos-gr/

## Development Roadmap :nut_and_bolt: 

### Overview
* **Total Estimated Duration:** 3 months
* **Full-time equivalent (FTE):**  3 FTE
* **Total Costs:** 20000 DAI

### Milestone 1 Implementation of Smart Contracts 
* **Estimated Duration:** 1 month
* **FTE:**  1
* **Costs:** 7000 DAI

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- |
| 0a. | License | Apache 2.0 / MIT / Unlicense |
| 0b. | Documentation | Documentation will be provided on how smart contracts for the bridge designed exactly. |
| 0c. | Testing Guide | The smart contracts code will be tested in local environment. | 
| 1. | Depositor Smart Contract | A depositor smart contract will be created, which will be responsible for locking the assets. |  
| 2. | Handler Smart Contract | A handler smart contract will be created, which will be responsible for executing on deposit. |  
| 3. | Multisig Smart Contract | A multisig smart contract will be created, which will be responsible for validating the bridging. |  
| 4. | Smart Contract tests | Tests for all those smart contracts and the interconnection between them will be delivered. |  
| 5. | README | A README.md file will be added to the repo, which will describe the steps to migrate and test the smart contracts flow. |

### Milestone 2 Implementation of relayer code
* **Estimated Duration:** 1 month
* **FTE:**  1
* **Costs:** 7000 DAI

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- |
| 0a. | License | Apache 2.0 / MIT / Unlicense |
| 0b. | Documentation | Documentation will be provided on how relayers are designed to interact with the bridging smart contracts. |
| 0c. | Testing Guide | Relayers' workflow will be tested. | 
| 1. | Relayer Software | The software on how relayers will interact with the bridge on the two different chains. |  
| 2. | Relayer Tests | Tests for relayers and the interconnection between them and smart contracts will be delivered. |  
| 3. | README | A README.md file will be added to the repo, which will describe the steps to run the whole bridge in a local environment. |


### Milestone 3 UI implementation
* **Estimated Duration:** 1 month
* **FTE:**  1
* **Costs:** 6000 DAI

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- |
| 0a. | License | Apache 2.0 / MIT / Unlicense |
| 0b. | Documentation | Documentation and/or article will be provided on how everyone can test the bridge real time between Moonbeam testnet and Injective testnet. |
| 0c. | Testing Guide | The whole bridge's workflow will be tested between Moonbeam's and Injective's testnet. | 
| 1. | FrontEnd Software | The software for the front end will be developed. |  
| 2. | Interaction Website | The Frontend will be deployed and everyone will be able to interact with it. |  
| 3. | Interaction Page | The Frontend will be deployed. |  
| 4. | Article | A step by step guide and/or video will be published about the interaction with the bridge. |

## Future Plans
Our whole project, which includes the whole exchange and chain will be on mainnet approximately Q2-Q3 2021, so that is when the bridge will have 
the actual purpose. 

## Additional Information :heavy_plus_sign:   
There are no teams that have contributed financially at the moment. We are planning to work with Moonbeam but there was no financial contribution.
There are not yet any other applications of ours for other grants.

