# Blockchain Technology & its Applications ![](https://img.shields.io/badge/-Live-Green)
![](https://img.shields.io/badge/College-St._Joseph's_College_Of_Engineering_and_Technology-blue) ![](https://img.shields.io/badge/Location-Palai,_Kottayam,_Kerala-blue)

<p align="center">

 <img src="https://ramagururadhakrishnan.github.io/images/2023_Jan_FDP_St_Joseph_Palai_Blockchain_Applications_DApp.jpg" width="800">
</p>


## Blockchain - Distributed Applications

### What is Blockchain?

**Blockchain Ledger** is a data structure similar to linked list, every block is a container linked to each other cryptographically. <br/>
**Blockchain Technology** is a decentralized computation and distributed ledger platform to immutably store transactions in a verifiable manner efficiently, through rational decision making process among multiple parties in an open and public system.

### What is DApp? 

Decentralized Application (DApp) is a computer application that is deployed and gets executed on a Distributed system usually Blockchain or Distributed Ledger Technology. DApp is a set of Smart Contracts interfaced with a UI. <br/> 
Some features of DApp as defined by the Ethereum
 - Decentralized
 - Deterministic
 - Turing complete
 - Isolated

### What is a Smart Contract?


### Benefits of DApps

- **Zero downtime:** Once the smart contract of the Distributed App is deployed on the blockchain, No malicious actors can launch a Denial
of Service because the blockchain network as a whole will always be able to serve clients with the smart contracts.
- **Privacy:** Blockchain accounts and transactions are
pseudo-anonymous there is no need to provide real-world identity to deploy or interact with a dapp.
- **Resistance to censorship:** The application cannot be controlled by a single entity on the network or stop any users from submitting 
transactions, deploying DApps, or reading data from the blockchain.
- **Data Integrity:** Just like the ata stored on the blockchain is immutable and indisputable, this property holds good for the smart contracts deployed in Blockchain.
-  *Verifiable Behavior:* As smart contracts can be analyzed and are guaranteed to execute in predictable ways, the same holds good for DApp also

### Implications of DApp

- **Maintenance** can be harder because of immutability of smart contracts. So any security bugs or updates cannot be made once the contracts are deployed.
- **Performance overhead** due to the choice of consensus algorithm and storage.
- **Network congestion** is a major implication at least in the current model. Even if a DApp is using too many computational resources, the entire network gets congested. In Ethereum, the network is only able to process about 10-15 transactions per second; if transactions are faster than this, the pool of unconfirmed transactions and transaction fee shall go high.
- **User experience** atleast at present is harder to provide user-friendly experiences. The average end user might find it too difficult to set up necessary tool stack necessary to interact with the blockchain in a truly secure fashion

### Core App and DApp Development Comparison

|      *      |    Core App    |     DApp     |
|:------------|:---------------|:-------------| 
|    Code     | Centralized Server | Distributed Systems like Blockchain |
|    Model    |  Trusted   |    Trust-less  |
|  Implementation |  Scrutiny Required |  Very High Scrutiny |
| Time | Faster Iteration | Generally slower |
| Maintenance | Easy | Very hard |
| Tools | Simple setup | Difficult to set up.  A tool stack necessary |
| Failure | High | Very Low |
| Transparency | No to Very Less | Completely Transparent (if Permissionless) |
| User Privacy | No to Very Less | High |
| Performance  | Less  | High |

### Sample DApp - Single Solidity Code

```
pragma solidity ^0.8.0;

contract SimpleDApp {
    address payable owner;
    mapping(address => uint) balances;

    constructor() public {
        owner = msg.sender;
    }

    function deposit() public payable {
        require(msg.value > 0, "Deposit amount must be greater than 0");
        balances[msg.sender] += msg.value;
    }

    function withdraw(uint amount) public {
        require(amount > 0, "Withdraw amount must be greater than 0");
        require(amount <= balances[msg.sender], "Insufficient funds");
        msg.sender.transfer(amount);
        balances[msg.sender] -= amount;
    }

    function getBalance() public view returns (uint) {
        return balances[msg.sender];
    }
}

```

### Examples of DApps 

- [**CryptoKitties**](https://www.cryptokitties.co/): A blockchain-based game that allows users to collect and breed virtual cats.
- **Augur**: A decentralized prediction market platform that allows users to create and trade predictions on the outcome of events.
- **OpenSea**: A marketplace for buying and selling digital collectibles such as in-game items and virtual real estate.
- **Uniswap**: A decentralized exchange (DEX) that allows users to trade cryptocurrencies without the need for a centralized intermediary.
- **MakerDAO**: A decentralized lending platform that uses a stablecoin called DAI to provide loans in a decentralized manner.
- **Ethlance**: A decentralized freelance marketplace that allows users to find and hire freelance talent in a trustless manner
- **Compound**: A decentralized finance (DeFi) platform that allows users to lend and borrow cryptocurrencies.
- **Steemit**: A blockchain-based social media platform that rewards users for creating and curating content.

### Examples of DApps - Non-Ethereum

- **EOS**: EOS is a blockchain platform that is designed for high-performance decentralized applications. Some examples of DApps built on EOS include:
  - **PRA CandyBox**: A blockchain-based game that allows users to earn rewards by playing mini-games.
  - **Everipedia**: A decentralized version of Wikipedia that allows users to earn rewards for contributing content.
- **TRON**: TRON is a blockchain platform that aims to build a decentralized internet. Some examples of DApps built on TRON include:
  - **TRONbet**: A decentralized gambling platform that allows users to place bets on various games.
  - **BitTorrent**: A decentralized file-sharing platform that allows users to share files without the need for a centralized intermediary.
- **IOTA**: IOTA is a blockchain platform that is designed for the Internet of Things (IoT) applications. Some examples of DApps built on IOTA include:
  - **IOTASeed**: A decentralized seed generation service that allows users to generate seeds for their IOTA wallets in a secure and private manner.
  - **IOTA Identity**: A decentralized identity management system that allows users to create and manage their digital identities in a secure and private manner.
- **Cosmos**: Cosmos is a blockchain ecosystem that allows for interoperability between different blockchains. Some examples of DApps built on Cosmos include:
  - **Terra Station**: A decentralized exchange that allows users to trade different assets across different blockchains.
  - **ChainGuard**: A decentralized security platform that allows users to secure their assets on different blockchains.
