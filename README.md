# **Mikail Rahman**
[mikail@chaintail.xyz](mailto:mikail@chaintail.xyz) | Toronto, ON

---

## 🧑‍💻 **Summary**

Software engineer with 10+ years of experience across software architecture, product ownership, backend systems, databases, frontends, and smart contracts.

My focus now is **Folio**, a consumer app for buying tokenized US stocks. The vision I am building toward:
- **One market from many sources.** Aggregate tokenized equities across issuers and trading venues, work across chains, and balance the book so inventory stays in line with what users hold.
- **An app people come back to.** A tight feedback loop with customers, fast iteration, and research into how users actually behave, used to drive retention.

## 🛠️ **Technical Skills**

- **Languages:** Rust, TypeScript, Python, Bash, C, C++, Swift, Java, Solidity, Kotlin, SQL
- **Blockchain & Protocol:** Solana, Ethereum and EVM chains including L2s (Arbitrum, Base), state channels, cross-chain bridges, multisig and custody
- **Data:** BigQuery, Parquet, DuckDB, SQLite, PostgreSQL, MongoDB, ETL pipelines, on-chain indexing
- **Infra & DevOps:** Autoscaling cloud infrastructure, AWS, Cloudflare tunnels, validator and node operations, CI on every pull request
- **Ownership areas:** Software architecture, product ownership, UX, QA, backend, databases, frontend, smart contracts, infrastructure

---

## 🏢 **Professional Experience**

### **Co-founder** - [Folio](https://github.com/ECS-Folio)
*Sep 2026 to Present | Toronto, Canada*

Folio spun out of Chaintail Labs. It is a Solana consumer app for buying tokenized US stocks with USDC.

- **Aggregation and trading**
  - One catalog across tokenized-stock issuers (xStocks, Ondo, Backpack), so the same stock appears once no matter who issued it.
  - Pricing, quoting, and routing through Jupiter, a Solana trade router, under one shared rate-limit budget. Price fetches are batched and cached, and trades get priority over background polling.
  - Daily price history is backfilled and live marks are recorded. Prices are stored per issuer so spreads between issuers can be analyzed.
  - Designed to work across chains and to balance the book, keeping inventory matched to user positions. This part is still being built.
- **Wallets and app**
  - Self-custody signing through an embedded email wallet or the Solana Seeker phone's wallet, with Sign-In-With-Solana.
  - Native Android app in Kotlin and Jetpack Compose for the Solana Seeker.
  - A quiet stock-app interface with no crypto look: Buy and Sell wording, a watchlist, personalized news, portfolio charts, and a deposit sheet that lists funding options by region.
- **Backend**
  - Node and TypeScript API and trading services on SQLite, hosted behind a Cloudflare tunnel.
  - A versioned OpenAPI contract with a mock server, so the app and backend are built in parallel against the same spec.

---

### **Cofounder / Engineer** - [Chaintail Labs](https://github.com/chaintail)
*Jan 2024 to Present | Toronto, Canada*

An experimental lab where we prototype quickly, test the limits of AI, and build for the sake of building. It takes contract work now and then, and spins projects with traction out into their own companies. Folio is the latest.

- **Long-term contract for a liquid-staking protocol**
  - Architected and operated the protocol's validator, sentry, and cross-chain infrastructure, securing millions of dollars in assets and tens of millions in transaction volume with 100% uptime.
  - Re-architected the application from a single server into autoscaling cloud infrastructure serving hundreds of thousands of users while continuously processing on-chain activity.
  - Built real-time indexing from the raw chain up in Python. It ingests blocks, receipts, and logs, decodes function calls and events, and loads them into BigQuery for analytics, security automation, and operations.
  - Built the airdrop's wallet scoring and verification. It cached full two-chain histories for about 750,000 wallets and verified X engagement through one interface over official and third-party APIs.
  - Supported incident response to a hack of the underlying chain, tracing stolen funds and helping contain a seven-figure exploit.
  - Implemented the protocol's migration from its original chain to Base to sunset the project.
- **[PulsePlay](https://github.com/Pulse-Play-HackMoney/pulse-play), in-play prediction markets**
  - Bets on 10 to 30 second windows are signed off-chain over state channels, so each one is final when placed and costs no gas. There is one on-chain open and close per session.
  - Prices come from an LMSR market maker (a formula that always quotes a price) or a peer-to-peer order book. Liquidity providers deposit USDC and get pool shares.
  - Built on Fastify, SQLite, and Next.js, settling in USDC on Base. Shipped to closed beta in Jun to Jul 2026, then rebuilt on Solana.
  - [Touchline](https://github.com/0xPulsePlay/touchline), the Solana version's barrier markets, settles with a Merkle proof of a single odds tick checked against a root anchored on Solana.
- **SPX options research**
  - Python ETL that turns 20 years of SPX options quotes (2005 to 2025, 483 monthly files) into a Parquet warehouse queried with DuckDB.
  - Static explorer for phone and desktop, used for mean-reversion research. The report is published [encrypted](https://github.com/MikailR/spx-data-reports).
- **Claude's World ([claude.do](https://claude.do))**
  - A phone-driven shell that turns a cloud server into a personal computer and hands coding work to agents.
  - PostgreSQL holds the state of every agent session. Sessions are driven through Telegram, a live terminal mini app, and voice, with human approval for risky steps.
  - Releases install as immutable versions, with runbooks for backup, restore, and rollback.
- **[Vellum](https://github.com/clan-world/sealed-skill-nft-demo)**
  - Solana proof of concept where an NFT controls who can use a secret held in a trusted-execution-style service. The NFT never contains the secret.
  - Off-chain encryption, key wrapping between services, and signed transcripts for every action.
  - A transfer hook on the token blocks transfers the broker has not approved.
- **Agent UI bakeoff**
  - Runs one design brief through several coding agents in parallel and compares the results side by side on a [live board](https://mikailr.github.io/GUI/).
- **[Gravity Lab](https://mikailr.github.io/gravity-lab/)**
  - Single-file browser simulation of 6,000 particles following two moving cores, with three scenes.
  - A separate script checks the simulation's invariants automatically.
- **[Solana Bunker](https://github.com/chaintail/solana-bunker)**
  - One permanent treasury address whose signing rules can be replaced, using hash-based keys (SHA-256 secrets, Merkle secrets, XMSS) written in Rust.
- **[GOLD bridge](https://github.com/clan-world/gold-bridge-monorepo)**
  - Bridges a game token between Solana and Base with Wormhole NTT, including the ERC-20 contract and a monitoring dashboard.

---

### **Engineer to CTO** - Deutsches Edelsteinhaus (GEMtrust) <!-- TODO: add company link -->
*Apr 2023 to Aug 2025 | Amtzell, Germany*

An investment-grade gemstone brokerage. We tokenized the asset for professional investors under European rules.

- **Contracts on Arbitrum One**
  - Solidity contracts on OpenZeppelin, built and deployed with Hardhat. Each physical gem is an NFT carrying its appraisal history, and a vault issues an ERC-20 token backed by the gems it holds.
  - Separate roles for appraising, minting, locking, and burning. The vault is upgradeable, and the USDC swap can be paused.
  - A separate contract splits owning a gem from the right to earn from it.
- **Custody**
  - Integrated Fireblocks and Safe multisig custody so no single key could move assets or perform admin actions.
- **Platform**
  - Express and TypeScript backend on MongoDB, covering purchases, transactions, price history, liquidity, and referral commissions.
  - Identity checks through Sumsub, and a fiat onramp whose webhooks trigger on-chain fulfilment.
  - React frontend with KYC gating and vault, unvault, and appraisal views.
- Led engineering from prototype to production. Promoted from external consultant (Apr 2023) to CTO (Aug 2023), and now a light board advisor.

---

## 📄 **Publications & Press**

- [*Technical deep dive: Solana Subscriptions & Allowances*](https://x.com/mikail_xyz/status/2069551830401482787), winning entry on Superteam Earn.
- Featured in [CoinDesk's coverage of the Consensus Miami EasyA Hackathon](https://www.coindesk.com/tech/2026/05/08/ai-agents-fueled-a-frenzy-of-startup-building-at-the-consensus-miami-easya-hackathon).
- [*GTII: Naked Short Squeeze, Ultimate DD*](https://www.reddit.com/r/GTII/comments/n016y1/gtii_naked_short_squeeze_ultimate_dd/), my equity research report on GTII.

---

## 📚 **Education**

**Bachelor of Mathematics, Computer Science** - University of Waterloo, Waterloo, ON
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
