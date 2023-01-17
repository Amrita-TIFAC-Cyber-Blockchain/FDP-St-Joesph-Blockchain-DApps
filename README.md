# Blockchain Technology & its Applications ![](https://img.shields.io/badge/-Live-Green)
![](https://img.shields.io/badge/College-St._Joseph's_College_Of_Engineering_and_Technology-blue) ![](https://img.shields.io/badge/Location-Palai,_Kottayam,_Kerala-blue)


<p text-align="center">
 <h1> One Week Faculty Development Programme on <br>  Blockchain Technology & its Applications </h1>
</p>


## Blockchain - Distributed Applications

### What is DApp? 


### What is a Smart Contract?


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

- CryptoKitties: A blockchain-based game that allows users to collect and breed virtual cats.
- Augur: A decentralized prediction market platform that allows users to create and trade predictions on the outcome of events.
- OpenSea: A marketplace for buying and selling digital collectibles such as in-game items and virtual real estate.
- Uniswap: A decentralized exchange (DEX) that allows users to trade cryptocurrencies without the need for a centralized intermediary.
- MakerDAO: A decentralized lending platform that uses a stablecoin called DAI to provide loans in a decentralized manner.
- Ethlance: A decentralized freelance marketplace that allows users to find and hire freelance talent in a trustless manner
- Compound: A decentralized finance (DeFi) platform that allows users to lend and borrow cryptocurrencies.
- Steemit: A blockchain-based social media platform that rewards users for creating and curating content.

## Examples of DApps - Non-Ethereum

- EOS: EOS is a blockchain platform that is designed for high-performance decentralized applications. Some examples of DApps built on EOS include:
  - PRA CandyBox: A blockchain-based game that allows users to earn rewards by playing mini-games.
  - Everipedia: A decentralized version of Wikipedia that allows users to earn rewards for contributing content.
- TRON: TRON is a blockchain platform that aims to build a decentralized internet. Some examples of DApps built on TRON include:
  - TRONbet: A decentralized gambling platform that allows users to place bets on various games.
  - BitTorrent: A decentralized file-sharing platform that allows users to share files without the need for a centralized intermediary.
- IOTA: IOTA is a blockchain platform that is designed for the Internet of Things (IoT) applications. Some examples of DApps built on IOTA include:
  - IOTASeed: A decentralized seed generation service that allows users to generate seeds for their IOTA wallets in a secure and private manner.
  - IOTA Identity: A decentralized identity management system that allows users to create and manage their digital identities in a secure and private manner.
- Cosmos: Cosmos is a blockchain ecosystem that allows for interoperability between different blockchains. Some examples of DApps built on Cosmos include:
  - Terra Station: A decentralized exchange that allows users to trade different assets across different blockchains.
  - ChainGuard: A decentralized security platform that allows users to secure their assets on different blockchains.
