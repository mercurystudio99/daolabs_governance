---
title: 'Ethereum Glossary'
sidebar_position: 3
---

:::info
The following definitions have been taken from the [Ethereum.org Glossary](https://ethereum.org/en/glossary/) and may not be up to date. These definitions have been provided for reference purposes.
:::

## 0-9

### 51% attack

A type of attack on a decentralized [network](#network) where a group gains control of the majority of [nodes](#node). This would allow them to defraud the blockchain by reversing [transactions](#transaction) and double spending [ether](#ether) and other tokens.

---

## A

### account

An object containing an [address](#address), balance, [nonce](#nonce), and optional storage and code. An account can be a [contract account](#contract-account) or an [externally owned account (EOA)](#eoa).

_See [Ethereum Accounts](https://ethereum.org/en/developers/docs/accounts/)._

### address

Most generally, this represents an [EOA](#eoa) or [contract](#contract-accouint) that can receive (destination address) or send (source address) [transactions](#transaction) on the blockchain. More specifically, it is the rightmost 160 bits of a [Keccak hash](#keccak-256) of an [ECDSA](#ecdsa) [public key](#public-key).

### application binary interface (ABI)

The standard way to interact with [contracts](#contract-account) in the Ethereum ecosystem,
both from outside the blockchain and for contract-to-contract interactions.

_See [ABI](https://ethereum.org/developers/docs/smart-contracts/compiling/#web-applications)._

### application programming interface

An Application Programming Interface (API) is a set of definitions for how to use a piece of software. An API sits between an application and a web server, and facilitates the transfer of data between them.

### ASIC

Application-specific integrated circuit. This usually refers to an integrated circuit, custom-built for cryptocurrency mining.

### assert

In [Solidity](#solidity), `assert(false)` compiles to `0xfe`, an invalid opcode, which uses up all remaining [gas](#gas) and reverts all changes. When an `assert()` statement fails, something very wrong and unexpected is happening, and you will need to fix your code. You should use `assert()` to avoid conditions that should never, ever occur.

_See [Smart contract security](https://ethereum.org/developers/docs/smart-contracts/security/)._

### attestation

A validator vote for a [Beacon Chain](#beacon-chain) or [shard](#shard) [block](#block). Validators must attest to blocks, signaling that they agree with the state proposed by the block.

_See [Attestations](https://ethereum.org/developers/docs/consensus-mechanisms/pos/attestations/)._

---

## B

### Base Fee

Every [block](#block) has a reserve price known as the 'base fee'. It is the minimum [gas](#gas) fee a user must pay to include a transaction in the next block.

_See [Gas and fees](https://ethereum.org/developers/docs/gas/)._

### Beacon Chain

A network upgrade that introduced a new consensus layer, which will become the coordinator for the entire Ethereum network. It introduces [proof-of-stake](#pos) and [validators](#validator) to Ethereum. It will eventually be merged with [Mainnet](#mainnet).

_See [Beacon Chain](https://ethereum.org/upgrades/beacon-chain/)._

### big-endian

A positional number representation where the most significant digit is first in memory. The opposite of little-endian, where the least significant digit is first.

### block

A collection of required information (a block header) about the comprised [transactions](#transaction), and a set of other block headers known as [ommers](#ommer). Blocks are added to the Ethereum network by [miners](#miner).

_See [Blocks](https://ethereum.org/developers/docs/blocks/)._

### block explorer

An interface that allows a user to search for information from, and about, a blockchain. This includes retrieving individual transactions, activity associated with specific addresses and information about the network.

### block header

The data in a block which is unique to its content and the circumstances in which it was created. It includes the hash of the previous block’s header, the version of the software the block is mined with, the timestamp and the merkle root hash of the contents of the block.

### block propagation

The process of transmitting a confirmed block to all other nodes in the network.

### block reward

The amount of ether rewarded to the producer of a new valid block.

### block time

The average time interval between blocks being added to the blockchain.

### block validation

Checking of the coherence of the cryptographic signature of the block with the history stored in the entire blockchain.

### blockchain

In Ethereum, a sequence of [blocks](#block) validated by the [proof-of-work](#pow) system, each linking to its predecessor all the way to the [genesis block](#genesis-block). There is no block size limit; it instead uses varying [gas limits](#gas-limit).

_See [What is a Blockchain?](https://ethereum.org/developers/docs/intro-to-ethereum#what-is-a-blockchain)._

### bootnode

The nodes which can be used to initiate the discovery process when running a node. The endpoints of these nodes are recorded in the Ethereum source code.

### bytecode

An abstract instruction set designed for efficient execution by a software interpreter or a virtual machine. Unlike human-readable source code, bytecode is expressed in numeric format.

### Byzantium fork

The first of two [hard forks](#hard-fork) for the [Metropolis](#metropolis) development stage. It included EIP-649 Metropolis [Difficulty Bomb](#difficulty-bomb) Delay and Block Reward Reduction, where the [Ice Age](#ice-age) was delayed by 1 year and the block reward was reduced from 5 to 3 ether.

---

## C

### Casper-FFG

Casper-FFG is a proof-of-stake consensus protocol used in conjunction with the [LMD-GHOST](#lmd-ghost) fork choice algorithm to allow [consensus clients](#consensus-client) to agree on the head of the Beacon Chain.

### checkpoint

The [Beacon Chain](#beacon-chain) has a tempo divided into slots (12 seconds) and epochs (32 slots). The first slot in each epoch is a checkpoint. When a [supermajority](#supermajority) of validators attests to the link between two checkpoints, they can be [justified](#justification) and then when another checkpoint is justified on top, they can be [finalized](#finality).

### compiling

Converting code written in a high-level programming language (e.g., [Solidity](#solidity)) into a lower-level language (e.g., EVM [bytecode](#bytecode)).

_See [Compiling Smart Contracts](https://ethereum.org/developers/docs/smart-contracts/compiling/)._

### committee

A group of at least 128 [validators](#validator) assigned to beacon and shard blocks at random by [the Beacon Chain](#beacon-chain).

### computational infeasibility

A process is computationally infeasible if it would take an impracticably long time (eg. billions of years) to do it for anyone who might conceivably have an interest in carrying it out.

### consensus

When numerous nodes (usually most nodes on the network) all have the same blocks in their locally validated best blockchain. Not to be confused with [consensus rules](#consensus-rules).

### consensus client

Consensus clients (such as Prysm, Teku, Nimbus, Lighthouse, Lodestar) run Ethereum's [proof-of-stake](#pos) consensus algorithm allowing the network to reach agreement about the head of the Beacon Chain. Consensus clients do not participate in validating/broadcasting transactions or executing state transitions. This is done by [execution clients](#execution-client).

### consensus layer

Ethereum's consensus layer is the network of [consensus clients](#consensus-client).

### consensus rules

The block validation rules that full nodes follow to stay in consensus with other nodes. Not to be confused with [consensus](#consensus).

### Constantinople fork

The second part of the [Metropolis](#metropolis) stage, originally planned for mid-2018. Expected to include a switch to a hybrid [proof-of-work](#pow)/[proof-of-stake](#pos) consensus algorithm, among other changes.

### contract account

An account containing code that executes whenever it receives a [transaction](#transaction) from another [account](#account) ([EOA](#eoa) or [contract](#contract-account)).

### contract creation transaction

A special [transaction](#transaction), with the [zero address](#zero-address) as the recipient, that is used to register a [contract](#contract-account) and record it on the Ethereum blockchain.

### crosslink

A crosslink provides a summary of a shard's state. It's how [shard](#shard) chains will communicate with one another via the [Beacon Chain](#beacon-chain) in the sharded [proof-of-stake system](#proof-of-stake).

_See [Proof-of-stake](https://ethereum.org/developers/docs/consensus-mechanisms/pos/#how-does-validation-work)._

### cryptoeconomics

The economics of cryptocurrencies.

---

## D

### Đ

Đ (D with stroke) is used in Old English, Middle English, Icelandic, and Faroese to stand for an uppercase letter “Eth”. It is used in words like ĐEV or Đapp (decentralized application), where the Đ is the Norse letter “eth”. The uppercase eth (Ð) is also used to symbolize the cryptocurrency Dogecoin. This is commonly seen in older Ethereum literature but is used less often today.

### DAG

DAG stands for Directed Acyclic Graph. It is a data structure composed of nodes and links between them. Ethereum uses a DAG in its [proof of work](#proof-of-work) algorithm, [Ethash](#ethash).

### Dapp

Decentralized application. At a minimum, it is a [smart contract](#smart-contract) and a web user interface. More broadly, a dapp is a web application that is built on top of open, decentralized, peer-to-peer infrastructure services. In addition, many dapps include decentralized storage and/or a message protocol and platform.

_See [Introduction to dapps](https://ethereum.org/developers/docs/dapps/)._

### data availability

The property of a state that any node connected to the network could download any specific part of the state that they wish to.

### decentralization

The concept of moving the control and execution of processes away from a central entity.

### decentralized autonomous organization (DAO)

A company or other organization that operates without hierarchical management. DAO may also refer to a contract named "The DAO" launched on April 30, 2016, which was then hacked in June 2016; this ultimately motivated a [hard fork](#hard-fork) (codenamed DAO) at block 1,192,000, which reversed the hacked DAO contract and caused Ethereum and Ethereum Classic to split into two competing systems.

_See [Decentralized autonomous organizations (DAOs)](https://ethereum.org/dao/)._

### decentralized exchange (DEX)

A type of [dapp](#dapp) that lets you swap tokens with peers on the network. You need [ether](#ether) to use one (to pay [transactions fees](#transaction-fee)) but they are not subject to geographical restrictions like centralized exchanges – anyone can participate.

_See [Decentralized exchanges](https://ethereum.org/get-eth/#dex)._

### deed

See [non-fungible token (NFT)](#nft)

### DeFi

Short for "decentralized finance," a broad category of [dapps](#dapp) aiming to provide financial services backed by the blockchain, without any intermediaries, so anyone with an internet connection can participate.

_See [Decentralized Finance (DeFi)](https://ethereum.org/defi/)._

### difficulty

A network-wide setting that controls how much computation is required to produce a [proof-of-work](#pow).

### difficulty bomb

Planned exponential increase in [proof-of-work](#pow) [difficulty](#difficulty) setting designed to motivate the transition to [proof-of-stake](#pos), reducing the chances of a [fork](#hard-fork)

### digital signature

A short string of data a user produces for a document using a [private key](#private-key) such that anyone with the corresponding [public key](#public-key), the signature, and the document can verify that (1) the document was "signed" by the owner of that particular private key, and (2) the document was not changed after it was signed.

---

### discovery

The process by which an Ethereum node finds other nodes to connect to.

### distributed hash table (DHT)

A data structure containing `(key, value)` pairs used by Ethereum nodes to identify peers to connect to and determine which protocols to use to communicate.

### double spend

A deliberate blockchain fork, where a user with a sufficiently large amount of mining power/stake sends a transaction moving some currency off-chain (e.g. exiting into fiat money or making an off-chain purchase) then reorganising the blockchain to remove that transaction. A successful double spend leaves the attacker with both their on and off-chain assets.

---

## E

### elliptic curve digital signature algorithm (ECDSA)

A cryptographic algorithm used by Ethereum to ensure that funds can only be spent by their owners. It's the preferred method for creating public and private keys. Relevant for account [address](#address) generation and [transaction](#transaction) verification.

### encryption

Encryption is the conversion of electronic data into a form unreadable by anyone except the owner of the correct decryption key.

### entropy

In the context of cryptography, lack of predictability or level of randomness. When generating secret information, such as [private keys](#private-key), algorithms usually rely on a source of high entropy to ensure the output is unpredictable.

### epoch

A period of 32 [slots](#slot) (6.4 minutes) in the [Beacon Chain](#beacon-chain)-coordinated system. [Validator](#validator) [committees](#committee) are shuffled every epoch for security reasons. There's an opportunity at each epoch for the chain to be [finalized](#finality). The term is also used on the [execution layer](#execution-layer) to mean the interval between each regeneration of the database used as a seed by the proof-of-work algorithm [Ethash](#Ethash). The epoch in specified as 30000 blocks.

_See [proof of stake](https://ethereum.org/developers/docs/consensus-mechanisms/pos/#how-does-validation-work)._

### equivocation

A validator sending two messages that contradict each other. One simple example is a transaction sender sending two transactions with the same nonce. Another is a block proposer proposing two blocks at the same block height (or for the same slot).

### Eth1

'Eth1' is a term that referred to Mainnet Ethereum, the existing proof-of-work blockchain. This term has since been deprecated in favor of the 'execution layer'. [Learn more about this name change](https://blog.ethereum.org/2022/01/24/the-great-eth2-renaming/).

_See [More on the Ethereum upgrades](https://ethereum.org/upgrades/)._

### Eth2

'Eth2' is a term that referred to a set of Ethereum protocol upgrades, including Ethereum's transition to proof-of-stake. This term has since been deprecated in favor of the 'consensus layer'. [Learn more about this name change](https://blog.ethereum.org/2022/01/24/the-great-eth2-renaming/).

_See [More on the Ethereum upgrades](https://ethereum.org/upgrades/)._

### etherbase

The default name of the primary account on an Ethereum client. Mining rewards are credited to this account. This is an Ethereum-specific version of "coinbase" which is applicable to other cryptocurrencies.

### Ethereum Improvement Proposal (EIP)

A design document providing information to the Ethereum community, describing a proposed new feature or its processes or environment (see [ERC](#erc)).

_See [Introduction to EIPs](https://ethereum.org/eips/)._

### Ethereum Name Service (ENS)

The ENS registry is a single central [contract](#smart-contract) that provides a mapping from domain names to owners and resolvers, as described in [EIP](#eip) 137.

[Read more at ens.domains](https://ens.domains)

### execution client

Execution clients (f.k.a. "Eth1 clients"), such as Besu, Erigon, go-ethereum, Nethermind, are tasked with processing and broadcasting transactions, as well as with managing Ethereum's state. They run the computations for each transaction in the [Ethereum Virtual Machine](#evm) to ensure that the rules of the protocol are followed. Today, they also handle [proof-of-work](#pow) consensus. After the transition to [proof-of-stake](#pos), they will delegate this to consensus clients.

### execution layer

Ethereum's execution layer is the network of [execution clients](#execution-client).

### externally owned account (EOA)

Externally owned accounts (EOAs) are [accounts](#account) that are controlled by users who control the [private keys](#private-key) for an account, typically generated using a [seed phrase](#hd-wallet-seed). Externally owned accounts are accounts without any code associated with them. Typically these accounts are used with a [wallet](#wallet).

### Ethereum Request for Comments (ERC)

A label given to some [EIPs](#eip) that attempt to define a specific standard of Ethereum usage.

_See [Introduction to EIPs](https://ethereum.org/eips/)._

### Ethash

A [proof-of-work](#pow) algorithm for Ethereum 1.0.

[Read more at eth.wiki](https://eth.wiki/en/concepts/ethash/ethash)

### ether

The native cryptocurrency used by the Ethereum ecosystem, which covers [gas](#gas) costs when executing transactions. Also written as ETH or its symbol Ξ, the Greek uppercase Xi character.

_See [Currency for our digital future](https://ethereum.org/eth/)._

### events

Allows the use of [EVM](#evm) logging facilities. [Dapps](#dapp) can listen for events and use them to trigger JavaScript callbacks in the user interface.

_See [Events and Logs](https://ethereum.org/developers/docs/smart-contracts/anatomy/#events-and-logs)._

### Ethereum Virtual Machine (EVM)

A stack-based virtual machine that executes [bytecode](#bytecode). In Ethereum, the execution model specifies how the system state is altered given a series of bytecode instructions and a small tuple of environmental data. This is specified through a formal model of a virtual state machine.

_See [Ethereum Virtual Machine](https://ethereum.org/developers/docs/evm/)._

### EVM assembly language

A human-readable form of EVM [bytecode](#bytecode).

---

## F

### fallback function

A default function called in the absence of data or a declared function name.

### faucet

A service carried out via [smart contract](#smart-contract) that dispenses funds in the form of free test ether that can be used on a testnet.

_See [Testnet Faucets](https://ethereum.org/developers/docs/networks/#testnet-faucets)._

### finality

Finality is the guarantee that a set of transactions before a given time will not change and can't be reverted.

_See [Proof-of-work finality](https://ethereum.org/developers/docs/consensus-mechanisms/pow/#finality)._

### finney

A denomination of [ether](#ether). 1 finney = 10<sup>15</sup> [wei](#wei). 10<sup>3</sup> finney = 1 ether.

### fork

A change in protocol causing the creation of an alternative chain, or a temporal divergence in two potential block paths during mining.

### fork-choice algorithm

The algorithm used to identify the head of the blockchain. On the execution layer the head of the chain is identified as the one with the greatest total difficulty behind it. This means the true head of the chain is the one that required the most work to mine it. On the consensus layer the algorithm observes the accumulated attestations from validators ([LMD_GHOST](#lmd-ghost)).

### fraud proof

A security model for certain [layer 2](#layer-2) solutions where, to increase speed, transactions are [rolled up](#rollups) into batches and submitted to Ethereum in a single transaction. They are assumed valid but can be challenged if fraud is suspected. A fraud proof will then run the transaction to see if fraud took place. This method increases the amount of transactions possible while maintaining security. Some [rollups](#rollups) use [validity proofs](#validity-proof).

_See [Optimistic rollups](https://ethereum.org/developers/docs/scaling/optimistic-rollups/)._

### frontier

The initial test development stage of Ethereum, which lasted from July 2015 to March 2016.

---

## G

### gas

A virtual fuel used in Ethereum to execute smart contracts. The [EVM](#evm) uses an accounting mechanism to measure the consumption of gas and limit the consumption of computing resources (see [Turing complete](#turing-complete)).

_See [Gas and Fees](https://ethereum.org/developers/docs/gas/)._

### gas limit

The maximum amount of [gas](#gas) a [transaction](#transaction) or [block](#block) may consume.

### gas price

Price in ether of one unit of gas specified in a transaction.

### genesis block

The first block in a [blockchain](#blockchain), used to initialize a particular network and its cryptocurrency.

### geth

Go Ethereum. One of the most prominent implementations of the Ethereum protocol, written in Go.

[Read more at geth.ethereum.org](https://geth.ethereum.org/)

### gwei

Short for gigawei, a denomination of [ether](#ether), commonly utilized to price [gas](#gas). 1 gwei = 10<sup>9</sup> [wei](#wei). 10<sup>9</sup> gwei = 1 ether.

---

## H

### hard fork

A permanent divergence in the [blockchain](#blockchain); also known as a hard-forking change. One commonly occurs when nonupgraded nodes can't validate blocks created by upgraded nodes that follow newer [consensus rules](#consensus-rules). Not to be confused with a fork, soft fork, software fork, or Git fork.

### hash

A fixed-length fingerprint of variable-size input, produced by a hash function. (See [keccak-256](#keccak-256)).

### hashrate

The number of hash calculations made per second by computers running mining software.

### HD wallet

A [wallet](#wallet) using the hierarchical deterministic (HD) key creation and transfer protocol.

[Read more at github.com](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)

### HD wallet seed

A value used to generate the master [private key](#private-key) and master chain code for an HD [wallet](#wallet). The wallet seed can be represented by mnemonic words, making it easier for humans to copy, back up, and restore private keys.

### homestead

The second development stage of Ethereum, launched in March 2016 at block 1,150,000.

---

## I

### index

A network structure meant to optimize the querying of information from across the [blockchain](#blockchain) by providing an efficient path to its storage source.

### Inter-exchange Client Address Protocol (ICAP)

An Ethereum address encoding that is partly compatible with the International Bank Account Number (IBAN) encoding, offering a versatile, checksummed, and interoperable encoding for Ethereum addresses. ICAP addresses use a new IBAN pseudo-country code- XE, standing for "eXtended Ethereum," as used in nonjurisdictional currencies (e.g., XBT, XRP, XCP).

### Ice Age

A [hard fork](#hard-fork) of Ethereum at block 200,000 to introduce an exponential [difficulty](#difficulty) increase (aka [difficulty bomb](#difficulty-bomb)), motivating a transition to [proof-of-stake](#pos).

### integrated development environment (IDE)

A user interface that typically combines a code editor, compiler, runtime, and debugger.

_See [Integrated Development Environments](https://ethereum.org/developers/docs/ides/)._

### immutable deployed code problem

Once a [contract's](#smart-contract) (or [library's](#library)) code is deployed, it becomes immutable. Standard software development practices rely on being able to fix possible bugs and add new features, so this represents a challenge for smart contract development.

_See [Deploying Smart Contracts](https://ethereum.org/developers/docs/smart-contracts/deploying/)._

### internal transaction

A [transaction](#transaction) sent from a [contract account](#contract-account) to another contract account or an [EOA](#eoa) (see [message](#message)).

### issuance

The minting of new ether to reward block proposal, attestation and whistle-blowing.

---

## K

### key derivation function (KDF)

Also known as a "password stretching algorithm," it is used by [keystore](#keystore-file) formats to protect against brute-force, dictionary, and rainbow table attacks on passphrase encryption, by repeatedly hashing the passphrase.

_See [Smart contract security](https://ethereum.org/developers/docs/smart-contracts/security/)._

### keystore

Every account’s private key/address pair exists as a single keyfile in an Ethereum client. These are JSON text files which contains the encrypted private key of the account, which can only be decrypted with the password entered during account creation.

### keccak-256

Cryptographic [hash](#hash) function used in Ethereum. Keccak-256 was standardized as [SHA](#sha)-3.

---

## L

### layer 2

An area of development focused on layering improvements on top of the Ethereum protocol. These improvements are related to [transaction](#transaction) speeds, cheaper [transaction fees](#transaction-fee), and transaction privacy.

_See [Layer 2](https://ethereum.org/layer-2/)._

### LevelDB

An open source on-disk key-value store, implemented as a lightweight, single-purpose [library](#library), with bindings to many platforms.

### library

A special type of [contract](#smart-contract) that has no payable functions, no fallback function, and no data storage. Therefore, it cannot receive or hold ether, or store data. A library serves as previously deployed code that other contracts can call for read-only computation.

_See [Smart Contract Libraries](https://ethereum.org/developers/docs/smart-contracts/libraries/)._

### lightweight client

An Ethereum client that does not store a local copy of the [blockchain](#blockchain), or validate blocks and [transactions](#transaction). It offers the functions of a [wallet](#wallet) and can create and broadcast transactions.

### LMD_GHOST

The [fork-choice algorithm](#fork-choice-algorithm) used by Ethereum's consensus clients to identify the head of the chain. LMD-GHOST is an acronym standing for "Latest Message Driven Greediest Heaviest Observed SubTree" which means that the head of the chain is the block with the greatest accumulation of [attestations](#attestation) in its history.

---

## M

### Mainnet

Short for "main network," this is the main public Ethereum [blockchain](#blockchain). Real ETH, real value, and real consequences. Also known as layer 1 when discussing [layer 2](#layer-2) scaling solutions. (Also, see [testnet](#testnet))

_See [Ethereum networks](https://ethereum.org/developers/docs/networks/)._

### memory-hard

Memory hard functions are processes that experience a drastic decrease in speed or feasibility when the amount of available memory even slightly decreases. An example is the Ethereum mining algorithm [Ethash](#ethash).

### Merkle Patricia trie

A data structure used in Ethereum to efficiently store key-value pairs.

### message

An [internal transaction](#internal-transaction) that is never serialized and only sent within the [EVM](#evm).

### message call

The act of passing a [message](#message) from one account to another. If the destination account is associated with [EVM](#evm) code, then the VM will be started with the state of that object and the message acted upon.

### Metropolis

The third development stage of Ethereum, launched in October 2017.

### mining

The process of verifying transactions and contract execution on the Ethereum blockchain in exchange for a reward in ether with the mining of every block.

### mining pool

The pooling of resources by miners who share their processing power and split [block rewards](#block-reward).

### miner

A network [node](#node) that finds valid [proof-of-work](#pow) for new blocks, by repeated pass hashing (see [Ethash](#ethash)).

_See [Mining](https://ethereum.org/developers/docs/consensus-mechanisms/pow/mining/)._

### mint

Minting is the process of creating new tokens and bringing them into circulation so that they can be used. It's a decentralized mechanism to create a new token without the involvement of the central authority.

---

## N

### network

Referring to the Ethereum network, a peer-to-peer network that propagates transactions and blocks to every Ethereum node (network participant).

_See [Networks](https://ethereum.org/developers/docs/networks/)._

### network hashrate

The collective [hashrate](#hashrate) produced by the entire Ethereum mining network.

### non-fungible token (NFT)

Also known as a "deed," this is a token standard introduced by the ERC-721 proposal. NFTs can be tracked and traded, but each token is unique and distinct; they are not interchangeable like ETH and [ERC-20 tokens](#token-standard). NFTs can represent ownership of digital or physical assets.

_See [Non-Fungible Tokens (NFTs)](https://ethereum.org/nft/)._
_See [ERC-721 Non-Fungible Token Standard](https://ethereum.org/developers/docs/standards/tokens/erc-721/)._

### node

A software client that participates in the network.

_See [Nodes and Clients](https://ethereum.org/developers/docs/nodes-and-clients/)._

### nonce

In cryptography, a value that can only be used once. There are two types of nonce used in Ethereum- an account nonce is a transaction counter in each account, which is used to prevent replay attacks; a [proof-of-work](#pow) nonce is the random value in a block that was used to satisfy the [proof-of-work](#pow).

---

## O

### ommer (uncle) block

When a [miner](#miner) finds a valid [block](#block), another miner may have published a competing block which is added to the tip of the blockchain first. This valid, but stale, block can be included by newer blocks as _ommers_ and receive a partial block reward. The term "ommer" is the preferred gender-neutral term for the sibling of a parent block, but this is also sometimes referred to as an "uncle".

### optimistic rollup

A [rollup](#rollups) of transactions that use [fraud proofs](#fraud-proof) to offer increased [layer 2](#layer-2) transaction throughput while using the security provided by [Mainnet](#mainnet) (layer 1). Unlike [Plasma](#plasma), a similar layer 2 solution, Optimistic rollups can handle more complex transaction types – anything possible in the [EVM](#evm). They do have latency issues compared to [Zero-knowledge rollups](#zk-rollups) because a transaction can be challenged via the fraud proof.

_See [Optimistic Rollups](https://ethereum.org/developers/docs/scaling/optimistic-rollups/)._

### Oracle

An oracle is a bridge between the [blockchain](#blockchain) and the real world. They act as on-chain [APIs](#api) that can be queried for information and used in [smart contracts](#smart-contract).

_See [Oracles](https://ethereum.org/developers/docs/oracles/)._

---

## P

### parity

One of the most prominent interoperable implementations of the Ethereum client software.

### peer

Connected computers running Ethereum client software that have identical copies of the [blockchain](#blockchain).

### peer to peer network

A network of computers ([peers](#peer)) that are collectively able to perform functionalities without the need for centralized, server-based services.

### Plasma

An off-chain scaling solution that uses [fraud proofs](#fraud-proof), like [Optimistic rollups](#optimistic-rollups). Plasma is limited to simple transactions like basic token transfers and swaps.

_See [Plasma](https://ethereum.org/developers/docs/scaling/plasma)._

### private key (secret key)

A secret number that allows Ethereum users to prove ownership of an account or contracts, by producing a digital signature (see [public key](#public-key), [address](#address), [ECDSA](#ecdsa)).

### private chain

A fully private blockchain is one with permissioned access, not publicly available for use.

### proof-of-stake (PoS)

A method by which a cryptocurrency blockchain protocol aims to achieve distributed [consensus](#consensus). PoS asks users to prove ownership of a certain amount of cryptocurrency (their "stake" in the network) in order to be able to participate in the validation of transactions.

_See [Proof-of-stake](https://ethereum.org/developers/docs/consensus-mechanisms/pos/)._

### proof-of-work (PoW)

A piece of data (the proof) that requires significant computation to find. In Ethereum, [miners](#miner) must find a numeric solution to the [Ethash](#ethash) algorithm that meets a network-wide [difficulty](#difficulty) target.

_See [Proof-of-work](https://ethereum.org/developers/docs/consensus-mechanisms/pow/)._

### public key

A number, derived via a one-way function from a [private key](#private-key), which can be shared publicly and used by anyone to verify a digital signature made with the corresponding private key.

---

## R

### receipt

Data returned by an Ethereum client to represent the result of a particular [transaction](#transaction), including a [hash](#hash) of the transaction, its [block](#block) number, the amount of [gas](#gas) used, and, in case of deployment of a [smart contract](#smart-contract), the [address](#address) of the contract.

### re-entrancy attack

An attack that consists of an attacker contract calling a victim contract function in such a way that during execution the victim calls the attacker contract again, recursively. This can result, for example, in the theft of funds by skipping parts of the victim contract that update balances or count withdrawal amounts.

_See [Re-entrancy](https://ethereum.org/developers/docs/smart-contracts/security/#re-entrancy)._

### reward

An amount of ether included in each new block as a reward by the network to the [miner](#miner) who found the [proof-of-work](#pow) solution.

### Recursive Length Prefix (RLP)

An encoding standard designed by the Ethereum developers to encode and serialize objects (data structures) of arbitrary complexity and length.

### rollups

A type of [layer 2](#layer-2) scaling solution that batches multiple transactions and submits them to [the Ethereum main chain](#mainnet) in a single transaction. This allows for reductions in [gas](#gas) costs and increases in [transaction](#transaction) throughput. There are Optimistic and Zero-knowledge rollups which use different security methods to offer these scalability gains.

_See [Rollups](https://ethereum.org/developers/docs/scaling/#rollups)._

### RPC

**Remote procedure call (RPC)** is a protocol that a program uses to request a service from a program located on another computer in a network without having to understand the network details.

---

## S

### Secure Hash Algorithm (SHA)

A family of cryptographic hash functions published by the National Institute of Standards and Technology (NIST).

### Serenity

The stage of Ethereum development that initiated a set of scaling and sustainability upgrades, previously known as 'Ethereum 2.0', or 'Eth2'.

_See [Ethereum upgrades](https://ethereum.org/upgrades/)._

### serialization

The process of converting a data structure into a sequence of bytes.

### shard / shard chain

A [proof-of-stake](#pos) chain that is coordinated by the [Beacon Chain](#beacon-chain) and secured by [validators](#validator). There will be 64 added to the network as part of the shard chain upgrade. Shard chains will offer increased transaction throughput for Ethereum by providing additional data to [layer 2](#layer-2) solutions like [optimistic rollups](#optimistic-rollups) and [ZK-rollups](#zk-rollups).

_See [Shard chains](https://ethereum.org/upgrades/shard-chains)._

### sidechain

A scaling solution that uses a separate chain with different, often faster, [consensus rules](#consensus-rules). A bridge is needed to connect these sidechains to [Mainnet](#mainnet). [Rollups](#rollups) also use sidechains, but they operate in collaboration with [Mainnet](#mainnet) instead.

_See [Sidechains](https://ethereum.org/developers/docs/scaling/sidechains/)._

### signing

Demonstrating cryptographically that a transaction was approved by the holder of a specific private key.

### singleton

A computer programming term that describes an object of which only a single instance can exist.

### slot

A period of time (12 seconds) in which a new [Beacon Chain](#beacon-chain) and [shard](#shard) chain block can be proposed by a [validator](#validator) in the [proof-of-stake](#pos) system. A slot may be empty. 32 slots make up an [epoch](#epoch).

_See [Proof-of-stake](https://ethereum.org/developers/docs/consensus-mechanisms/pos/#how-does-validation-work)._

### smart contract

A program that executes on the Ethereum computing infrastructure.

_See [Introduction to Smart Contracts](https://ethereum.org/developers/docs/smart-contracts/)._

### SNARK

Short for "succinct non-interactive argument of knowledge", a SNARK is a type of [zero-knowledge proof](#zk-proof).

_See [Zero-knowledge rollups](https://ethereum.org/developers/docs/scaling/zk-rollups/)._

### soft fork

A divergence in a [blockchain](#blockchain) that occurs when the [consensus rules](#consensus-rules) become change. Contrary to a [hard fork](#hard-fork), a soft fork is backwards compatible; upgraded nodes can validate blocks created by non-upgraded nodes as long as they follow the new consensus rules.

### Solidity

A procedural (imperative) programming language with syntax that is similar to JavaScript, C++, or Java. The most popular and most frequently used language for Ethereum [smart contracts](#smart-contract). Created by Dr. Gavin Wood.

_See [Solidity](https://ethereum.org/developers/docs/smart-contracts/languages/#solidity)._

### Solidity inline assembly

[EVM](#evm) assembly language in a [Solidity](#solidity) program. Solidity's support for inline assembly makes it easier to write certain operations.

### Spurious Dragon

A [hard fork](#hard-fork) of the Ethereum blockchain, which occurred at block 2,675,000 to address more denial-of-service attack vectors and clear state (see [Tangerine Whistle](#tangerine-whistle)). Also, a replay attack protection mechanism (see [nonce](#nonce)).

### stablecoin

An [ERC-20 token](#token-standard) with a value pegged to another asset's value. There are stablecoins backed by fiat currency like dollars, precious metals like gold, and other cryptocurrencies like Bitcoin.

_See [ETH isn't the only crypto on Ethereum](https://ethereum.org/eth/#tokens)._

### staking

Depositing a quantity of [ether](#ether) (your stake) to become a validator and secure the [network](#network). A validator checks [transactions](#transaction) and proposes [blocks](#block) under a [proof-of-stake](#pos) consensus model. Staking gives you an economic incentive to act in the best interests of the network. You'll get rewards for carrying out your [validator](#validator) duties, but lose varying amounts of ETH if you don't.

_See [Stake your ETH to become an Ethereum validator](https://ethereum.org/staking/)._

### STARK

Short for "scalable transparent argument of knowledge", a STARK is a type of [zero-knowledge proof](#zk-proof).

_See [Zero-knowledge rollups](https://ethereum.org/developers/docs/scaling/zk-rollups/)._

### state

A snapshot of all balances and data at a particular point in time on the blockchain, normally referring to the condition at a particular block.

### state channels

A [layer 2](#layer-2) solution where a channel is set up between participants, where they can transact freely and cheaply. Only a [transaction](#transaction) to set up the channel and close the channel is sent to [Mainnet](#mainnet). This allows for very high transaction throughput, but does rely on knowing number of participants up front and locking up of funds.

_See [State channels](https://ethereum.org/developers/docs/scaling/state-channels/#state-channels)._

### supermajority

Supermajority is the term given for an amount exceeding 2/3 (66%) of the total staked ether on the [Beacon Chain](#beacon-chain). A supermajority vote is required for blocks to be [finalized](#finality) on the Beacon Chain.

### syncing

The process of downloading the entire latest version of a blockchain to a node.

### sync committee

A sync committee is a randomly selected group of [validators](#validator) on the [Beacon Chain](#beacon-chain) that refresh every ~27 hours. Their purpose is to add their signatures to valid block headers. Sync committees allow [light clients](#lightweight-client) to keep track of the head of the blockchain without having to access the entire validator set.

### szabo

A denomination of [ether](#ether). 1 szabo = 10<sup>12</sup> [wei](#wei), 10<sup>6</sup> szabo = 1 ether.

---

## T

### Tangerine Whistle

A [hard fork](#hard-fork) of the Ethereum blockchain, which occurred at block 2,463,000 to change the [gas](#gas) calculation for certain I/O-intensive operations and to clear the accumulated state from a denial-of-service attack, which exploited the low gas cost of those operations.

### terminal total difficulty (TTD)

The total difficulty is the sum of the Ethash mining difficulty for all blocks up to some specific point in the blockchain. The terminal total difficulty is a specific value for the total difficulty that will be used as the trigger for execution clients to switch off their mining and block gossip functions so the network can transition to proof-of-stake.

### testnet

Short for "test network," a network used to simulate the behavior of the main Ethereum network (see [Mainnet](#mainnet)).

_See [Testnets](https://ethereum.org/developers/docs/networks/#ethereum-testnets)._

### token

A tradable virtual good defined in smart contracts on the Ethereum blockchain.

### token standard

Introduced by ERC-20 proposal, this provides a standardized [smart contract](#smart-contract) structure for fungible tokens. Tokens from the same contract can be tracked, traded, and are interchangeable, unlike [NFTs](#nft).

_See [ERC-20 Token Standard](https://ethereum.org/developers/docs/standards/tokens/erc-20/)._

### transaction

Data committed to the Ethereum Blockchain signed by an originating [account](#account), targeting a specific [address](#address). The transaction contains metadata such as the [gas limit](#gas-limit) for that transaction.

_See [Transactions](https://ethereum.org/developers/docs/transactions/)._

### transaction fee

A fee you need to pay whenever you use the Ethereum network. Examples include sending funds from your [wallet](#wallet) or a [dapp](#dapp) interaction, like swapping tokens or buying a collectible. You can think of this like a service charge. This fee will change based on how busy the network is. This is because [miners](#miner), the people responsible for processing your transaction, are likely to prioritise transactions with higher fees – so congestion forces the price up.

At a technical level, your transaction fee relates to how much [gas](#gas) your transaction requires.

Reducing transaction fees is a subject of intense interest right now. See [Layer 2](#layer-2)

### trustlessness

The ability of a network to mediate transactions without any of the involved parties needing to trust a third party

### Turing complete

A concept named after English mathematician and computer scientist Alan Turing- a system of data-manipulation rules (such as a computer's instruction set, a programming language, or a cellular automaton) is said to be "Turing complete" or "computationally universal" if it can be used to simulate any Turing machine.

---

## V

### validator

A [node](#node) in a [proof-of-stake](#pos) system responsible for storing data, processing transactions, and adding new blocks to the blockchain. To active validator software, you need to be able to [stake](#staking) 32 ETH.

_See [Proof-of-stake](https://ethereum.org/developers/docs/consensus-mechanisms/pos)._
_See [Staking in Ethereum](https://ethereum.org/staking/)._

### validity proof

A security model for certain [layer 2](#layer-2) solutions where, to increase speed, transactions are [rolled up](/#rollups) into batches and submitted to Ethereum in a single transaction. The transaction computation is done off-chain and then supplied to the main chain with a proof of their validity. This method increases the amount of transactions possible while maintaining security. Some [rollups](#rollups) use [fraud proofs](#fraud-proof).

_See [Zero-knowledge rollups](https://ethereum.org/developers/docs/scaling/zk-rollups/)._

### validium

An off-chain solution that uses [validity proofs](#validity-proof) to improve transaction throughput. Unlike [Zero-knowledge rollups](#zk-rollup), Validium data isn't stored on layer 1 [Mainnet](#mainnet).

_See [Validium](https://ethereum.org/developers/docs/scaling/validium/)._

### Vyper

A high-level programming language with Python-like syntax. Intended to get closer to a pure functional language. Created by Vitalik Buterin.

_See [Vyper](https://ethereum.org/developers/docs/smart-contracts/languages/#vyper)._

---

## W

### wallet

Software that holds [private keys](#private-key). Used to access and control Ethereum [accounts](#account) and interact with [smart contracts](#smart-contract). Keys need not be stored in a wallet, and can instead be retrieved from offline storage (i.e. a memory card or paper) for improved security. Despite the name, wallets never store the actual coins or tokens.

_See [Ethereum Wallets](https://ethereum.org/wallets/)._

### Web3

The third version of the web. First proposed by Dr. Gavin Wood, Web3 represents a new vision and focus for web applications- from centrally owned and managed applications, to applications built on decentralized protocols (see [dapp](#dapp)).

_See [Web2 vs Web3](https://ethereum.org/developers/docs/web2-vs-web3/)._

### wei

The smallest denomination of [ether](#ether). 10<sup>18</sup> wei = 1 ether.

---

## Z

### zero address

A special Ethereum address, composed entirely of zeros, that is specified as the destination address of a [contract creation transaction](#contract-creation-transaction).

### zero-knowledge proof

A zero-knowledge proof is a cryptographic method that allows an individual to prove that a statement is true without conveying any additional information.

_See [Zero-knowledge rollups](https://ethereum.org/developers/docs/scaling/zk-rollups/)._

### zero-knowledge rollup

A [rollup](#rollups) of transactions that use [validity proofs](#validity-proof) to offer increased [layer 2](#layer-2) transaction throughput while using the security provided by [Mainnet](#mainnet) (layer 1). Although they can't handle complex transaction types, like [Optimistic rollups](#optimistic-rollups), they don't have latency issues because transactions are provably valid when submitted.

_See [Zero-knowledge Rollups](https://ethereum.org/developers/docs/scaling/zk-rollups/)._
