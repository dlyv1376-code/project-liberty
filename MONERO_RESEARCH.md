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
