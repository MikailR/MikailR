# **Mikail Rahman**
[Email](mailto:mikail@chaintail.xyz) | [GitHub: https://github.com/MikailR](https://github.com/MikailR) | Toronto, ON

---

## 🧑‍💻 **Summary**

Engineer and founder working on **on-chain financial products**: tokenized equities, prediction markets with state-channel settlement, and the infrastructure that keeps a protocol running.

What I usually own, end to end:
- **Protocol and settlement design**, such as state-channel settlement where each prediction is a signed agreement that is final when placed, with no per-prediction gas fee.
- **Production infrastructure**: validator nodes, cross-chain infrastructure, and autoscaling cloud services serving hundreds of thousands of users.
- **Data pipelines**: real-time chain indexing into BigQuery, and a 20-year SPX options warehouse in Parquet and DuckDB.

Outside of engineering, I am a classically trained pianist (ABRSM Grade 8).

## 🛠️ **Technical Skills**

- **Blockchain & Protocol:** Solana, Token-2022 (Solana's extended token standard, including transfer hooks), Base, Shibarium, EVM smart contracts, Yellow Network state channels, validator and sentry node operations, cross-chain infrastructure
- **Data:** BigQuery, Parquet, DuckDB, ETL pipelines, real-time transaction and event indexing
- **Custody & Security:** Fireblocks, multisig custody, off-chain encryption and key wrapping, trusted-execution-style secret storage, incident response and stolen-fund tracing
- **Infra:** Autoscaling cloud infrastructure, phone-driven cloud dev environments
- **Tooling:** Coding agents and multi-agent build harnesses, automated invariant checks
- **Concepts:** Settlement design, liquidity aggregation and routing, tokenized real-world assets, distributed systems, applied cryptography

---

## 🏢 **Professional Experience**

### **Founder** | Independent
*Jan 2025 to Present*

- **Folio**
  - Building a brokerage-style app that gives emerging-market users access to US equities through tokenized stocks, with the crypto rails hidden from the user.
  - Architecting the core aggregation engine: it sources tokenized-equity liquidity across multiple venues and chains, with a fungibility layer that treats different issuers' tokens for the same stock as one routable asset.
- **PulsePlay**
  - Shipped in-play prediction markets to closed beta (Jun to Jul 2026) on Yellow Network state channels, then on Solana.
  - Designed settlement where each prediction is a signed state-channel agreement with the liquidity pool, final on placement: one on-chain open and close per session, no per-prediction gas, and no ghost fills (trades that look filled but never settle).

---

### **Cofounder / Engineer** | Chaintail Labs
*Jan 2024 to Dec 2025*

A lab for rapid product and protocol experiments, long-term contract work, and agent-driven shipping.

- **Long-term contract for a liquid-staking protocol**
  - Architected and operated the protocol's validator, sentry, and cross-chain infrastructure, securing millions of dollars in assets and tens of millions in transaction volume with 100% uptime.
  - Re-architected the application from a single server into autoscaling cloud infrastructure serving hundreds of thousands of users while continuously processing on-chain activity.
  - Built real-time indexing from the raw chain up, decoding transactions, function calls, parameters, logs, and events into BigQuery for analytics, security automation, and operations.
  - Built the airdrop's wallet scoring and verification: cached full two-chain histories for ~750,000 wallets, and verified X engagement through one interface over official and third-party APIs.
  - Supported incident response to a hack of the underlying chain, tracing stolen funds and helping contain a seven-figure exploit.
  - Implemented the protocol's migration from Shibarium to Base to sunset the project.
- **SPX options research:** ETL pipeline ingesting 20 years of SPX options quotes (2005 to 2025, 483 monthly files) into a Parquet and DuckDB warehouse, with a phone and desktop explorer for mean-reversion research.
- **Claude's World ([claude.do](https://claude.do)):** Phone-driven shell that turns a cloud server into a personal computer and hands coding work to agents.
- **Vellum:** Solana proof of concept where a Token-2022 NFT controls access to a secret sealed in a trusted-execution-style service, with off-chain encryption, key wrapping, signed transcripts, and a transfer hook that only allows approved transfers.
- **Agent UI Bakeoff Harness:** Runs one design brief through multiple coding agents in parallel and compares the results on a live board.
- **Gravity Lab:** Single-file browser gravity simulation of 6,000 interactive particles, with automated invariant checks.

---

### **Engineer to CTO** | Deutsches Edelsteinhaus (GEMtrust)
*Apr 2023 to Aug 2025*

An investment-grade gemstone brokerage. We tokenized the asset for professional investors under European rules.

- Led engineering from prototype to production, designing smart-contract issuance and custody to meet European regulation.
- Integrated Fireblocks and multisig custody so no single key could move assets or perform admin actions.
- Promoted from external consultant (Apr 2023) to CTO (Aug 2023); now a light board advisor.

---

## 📄 **Publications & Press**

- *Technical deep dive: Solana Subscriptions & Allowances*, published on Superteam Earn (winning entry). <!-- TODO: add link -->
- Featured in a **CoinDesk** article covering the Consensus Miami Hackathon. <!-- TODO: add link -->

---

## 📚 **Education**

**Bachelor of Mathematics, Computer Science** | University of Waterloo, Waterloo, ON
Minor in Physics

Relevant courses: Data Structures and Algorithms, Algorithm Design and Analysis, Networks and Distributed Computer Systems, Applied Cryptography, Neural Networks, Numerical Computation

---

## 🏅 **Achievements & Awards**

- **TxODDS Superteam Hackathon:** 1st, Prediction Markets & Settlement
- **TxODDS Superteam Hackathon:** 3rd, Consumer & Fan Experiences
- **ETHGlobal HackMoney:** 1st, Prediction Markets
- **ETHGlobal OpenAgents:** 1st, Autonomous Agentic Gaming
- **Chainlink Hackathon:** 1st, Best use of CRE Runtime with Confidential Compute
- **Yellow Network Accelerator:** 1st place in the full cohort
- **Colosseum Canada Demo Day:** 2nd, Agentic Privacy Primitives on Solana
- **Consensus Toronto Hackathon:** 2nd, Forte Compliance Track
- **Consensus Miami Hackathon:** 3rd, EasyA Track
- **Superteam Earn:** Winner, technical deep dive on Solana Subscriptions & Allowances
