PROJECT LIBERTY — Decision Log

Version: 0.1
Status: Working Draft

1. Purpose

This document records important project decisions and distinguishes confirmed principles from proposals that still require research and approval.

2. Confirmed Project Direction

D-001 — Monero Core as the research and development foundation

Status: Accepted direction; implementation not started.

PROJECT LIBERTY will investigate forking Monero Core rather than building an entirely new blockchain from scratch.

Before implementation:

- Review the upstream license and all dependency licenses.
- Study the architecture and establish a reproducible baseline build.
- Avoid changing cryptographic and consensus components without research and testing.
- Do not assume that a fork automatically inherits Monero's security or privacy guarantees.

D-002 — Permissionless application development

Status: Accepted principle.

Developers must be able to create and publish compatible applications without paying a protocol-level listing or registration fee and without requesting permission from a central authority.

Ordinary network fees may apply when applications use network resources.

D-003 — Permissionless node operation

Status: Accepted principle.

Anyone should be able to run an independent node and verify the network according to published protocol rules without permission from a central organization.

Running a node does not automatically grant block production rights. Those rights depend on the consensus mechanism, which remains undecided.

D-004 — Privacy and user control

Status: Accepted principles.

The project prioritizes:

- Privacy by design.
- Open-source development.
- User control over cryptographic keys.
- Independent infrastructure.
- Transparent economics.
- Independent security reviews.

The project must not promise absolute privacy or security.

D-005 — CryptoPhoto

Status: Accepted product direction; design not finalized.

CryptoPhoto is the first planned flagship application.

It is intended to protect photographs using encryption and a separate encrypted storage layer.

Large files should not be stored directly on the blockchain. File encryption and transaction privacy are separate security layers.

3. Preliminary Technical Preferences

These are planning preferences, not final implementation decisions:

- C++ for blockchain core development.
- Rust for suitable independent modules.
- Kotlin for Android application development.
- Source-code research and license review before modifications.
- Local test network before any public network launch.

4. Open Decisions — Not Yet Approved

The following topics require further research and explicit approval:

1. Consensus mechanism and block production rules.
2. Token supply, emission, fees, burns, and funding model.
3. Application execution and network interaction architecture.
4. Encrypted file storage and availability.
5. Key backup and recovery mechanisms.
6. Governance and upgrade procedures.
7. Security audit and launch requirements.

A 2-of-3 secret-sharing recovery model has been discussed, but it is only a proposal and is not approved.

5. Decision Changes

When a decision changes:

- Record its new status: Proposed, Accepted, Superseded, or Rejected.
- Explain the reasons and trade-offs.
- Update related architecture and roadmap documents.

6. Current Project Status

PROJECT LIBERTY is in the research and architecture-planning stage.

This document records project direction and principles. It does not claim that a blockchain, token, wallet, application, or production network has already been implemented or audited.
