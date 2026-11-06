PROJECT LIBERTY — Monero Core Research

Document: MONERO_RESEARCH.md
Version: 0.1
Status: Preliminary Research

1. Research Objective

The objective is to study Monero Core as a technical foundation for the future development of PROJECT LIBERTY.

No code modifications or protocol decisions are approved by this document.

2. Main Components

2.1. Monero Daemon

The "monerod" process is responsible for:

- Connecting to other network nodes.
- Receiving and propagating blocks and transactions.
- Maintaining blockchain data.
- Validating blocks and network rules.
- Providing node services to wallets and applications.

2.2. Wallet Architecture

The wallet manages keys, constructs transactions, communicates with a node, and scans blockchain data for relevant transactions.

Wallet security and node security must be studied separately.

2.3. P2P Network

The peer-to-peer network allows independent nodes to exchange blockchain data without relying on one central server.

Research areas:

- Peer discovery.
- Block propagation.
- Transaction propagation.
- Network synchronization.
- Connection security and metadata privacy.

2.4. Consensus

Monero uses Proof of Work with RandomX.

The consensus mechanism determines how blocks are produced and how nodes agree on the valid blockchain.

PROJECT LIBERTY has not selected its consensus mechanism.

3. Privacy Technologies

3.1. Ring Signatures

Used to obscure the actual spent output among a set of possible outputs.

3.2. Stealth Addresses

Used to create one-time recipient addresses and protect recipient privacy.

3.3. Ring Confidential Transactions

Used to conceal transaction amounts while allowing network verification.

3.4. Network-Level Privacy

Dandelion++ helps reduce the traceability of transaction propagation.

It does not provide complete protection against all network-level observers.

4. PROJECT LIBERTY Research Questions

1. Which Monero Core components can be reused?
2. Which components require adaptation?
3. What are the upstream license and dependency obligations?
4. How are consensus rules validated?
5. How do wallets communicate with nodes?
6. What changes would be required for a separate blockchain network?
7. How can CryptoPhoto operate without storing large encrypted files directly on-chain?
8. How should application developers interact with the network?

5. Research and Development Sequence

1. Study the upstream source tree.
2. Identify the main modules and their responsibilities.
3. Review the license and dependency inventory.
4. Study transaction construction and validation.
5. Study node synchronization and P2P communication.
6. Study consensus and mining.
7. Establish a reproducible baseline build.
8. Design a local test environment.
9. Only then evaluate possible modifications.

6. Important Security Principle

A fork does not automatically inherit the security, privacy, decentralization, or economic properties of its upstream project.

Every change to cryptography, consensus, transaction validation, and network behavior requires careful analysis and testing.

7. Current Status

Research only.

No consensus mechanism, tokenomics, cryptographic modifications, or production implementation is approved by this document.

8. Primary Sources

- Monero source code: https://github.com/monero-project/monero
- Official technical specifications: https://docs.getmonero.org/technical-specs/
- Official Monero documentation: https://docs.getmonero.org/
- Official project information: https://www.getmonero.org/resources/about/


## 3. Node and Wallet Architecture

### 3.1 Monero Daemon

The monerod daemon:
- Connects to the P2P network.
- Downloads and validates blockchain data.
- Maintains the local blockchain database.
- Does not store or access wallet private keys.

### 3.2 Wallet Architecture

Wallet functionality is separated from the daemon.
Wallets communicate with the node through defined interfaces.

### 3.3 PROJECT LIBERTY Research Notes

Potentially reusable architectural principles:
- Separation of node and wallet responsibilities.
- Local control of private keys.
- Independent node operation.
- Clearly defined communication interfaces.

No implementation decisions are finalized.
All components must undergo independent security review.


4. Cryptographic Privacy Architecture

Status: Research — No implementation decisions approved.

4.1 Ring Signatures

Purpose:

- Obscure the actual spent output among decoy outputs.
- Make transaction input tracing more difficult.
- Provide plausible deniability.

Modern Monero uses CLSAG signatures.

Research requirements:

- Understand ring construction.
- Study decoy selection.
- Understand linkability and double-spend prevention.
- Review security assumptions.

4.2 Stealth Addresses

Purpose:

- Generate unique one-time recipient addresses.
- Prevent direct publication of the recipient's public wallet address.
- Reduce the ability to link incoming payments.

Research requirements:

- Study public and private view keys.
- Study transaction public keys.
- Understand one-time output key derivation.
- Review wallet scanning and recovery.

4.3 Ring Confidential Transactions (RingCT)

Purpose:

- Conceal transaction amounts.
- Allow verification of transaction balance.
- Prevent unauthorized creation of additional currency.

Important technologies:

- Pedersen commitments.
- CLSAG signatures.
- Bulletproofs+ range proofs.

Research requirements:

- Study commitment construction.
- Understand range proofs.
- Study balance verification.
- Review transaction validation.

4.4 PROJECT LIBERTY Security Principles

Proposed principles:

1. Use established and independently reviewed cryptographic constructions.
2. Do not invent proprietary cryptographic algorithms without expert research.
3. Preserve independent verification of transactions.
4. Protect user keys and recovery mechanisms.
5. Require independent security audits before production deployment.

4.5 Open Research Questions

- Which Monero cryptographic components can be reused?
- What are the licensing and implementation requirements?
- What changes would require a new cryptographic audit?
- How can CryptoPhoto encryption remain independent of blockchain transaction privacy?
- What privacy guarantees can realistically be provided?

4.6 Current Status

Research only.

No cryptographic modifications or implementation decisions have been approved.
