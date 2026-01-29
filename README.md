# KYC Evidence Bundle (IPFS / Filecoin)

Open-source utility to create, encrypt, and store verifiable KYC and compliance evidence bundles on IPFS and Filecoin with auditable retrieval.

## What this is
This repository provides a small, composable module that:
- Generates sanitized compliance evidence bundles (JSON or files)
- Encrypts the bundle locally
- Uploads the encrypted artifact to IPFS
- Anchors the content identifier (CID) to Filecoin
- Enables later retrieval and verification for audits

This is designed for compliance, RegTech, and Web3 infrastructure builders who need **immutable, verifiable storage** of audit artifacts.

## What this is NOT
- This is **not** a full KYC platform
- This repo does **not** include identity verification logic
- This repo does **not** process real PII

The main KYC platform using this module is proprietary and maintained separately.

## Why Filecoin
Compliance evidence must be:
- Tamper-resistant
- Verifiable
- Retrievable years later

IPFS provides content addressing, and Filecoin provides durable, decentralized storage guarantees. This module demonstrates real Filecoin usage for compliance-grade data storage.

## High-level Flow
1. Input: sanitized compliance output (JSON / files)
2. Encrypt bundle locally
3. Upload encrypted bundle to IPFS
4. Store CID via Filecoin
5. Retrieve + verify integrity when required

## Planned Features
- CLI to generate encrypted evidence bundles
- IPFS upload helper
- Filecoin storage adapter
- Retrieval and verification scripts
- Minimal test coverage

## Grant Scope
This repository is developed as part of a Filecoin Devgrants proposal.
Deliverables, milestones, and acceptance criteria are defined in `MILESTONES.md`.

## License
MIT
