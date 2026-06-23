# BugDNA | Crypto Vulnerability Intelligence Engine

**Proof-first Solidity security research, with human validation and explicit claim boundaries.**

Version represented by this showcase: `v2.2.0`

BugDNA is a local, modular Solidity security research assistant. It locks an exact authorized scope, ranks detector hypotheses, preserves evidence and limitations, and produces deterministic source-free bundles for human review. This public showcase presents the product architecture and measured evidence without publishing the private implementation.

## What is public here

This repository pack is a documentation-only product showcase. It contains evidence summaries, architecture boundaries, a bounded pilot offer, and machine-readable integrity metadata.
It deliberately excludes the implementation, detector source, Solidity target source, secrets, and personal data.

## Intended audience

independent Solidity auditors, protocol teams considering a bounded pilot, security engineers reviewing research tooling

## Current proof boundary

The evidence ledger contains 8 frozen entries. Synthetic and curated holdouts are reported with their limitations; they are not converted into a real-world accuracy claim.
BugDNA produces hypotheses for human validation. It is not an autonomous auditor, exploit bot, legal opinion, or guarantee of vulnerability coverage.

## Start here

1. Read `docs/EVIDENCE.md` with every limitation.
2. Read `docs/ARCHITECTURE.md` for the split-before-grow boundary.
3. Read `docs/PILOT.md` for a bounded authorized pilot shape.
4. Read `docs/LIMITATIONS.md` before relying on any metric.
5. Read `LICENSE_NOTICE.md` before copying or redistributing material.

## Integrity

Publication specification SHA-256: `fd88cd1f4aa47ea891f7ef6c1cc103c56404cbe4f5f7ec2abcb5ea825eb3f4cf`
Portfolio specification SHA-256: `cded028acfbd33dc9655326b7f88206e42abbb282ce9a220596195de21cae217`
All published files are listed in `SHA256SUMS.txt`.
