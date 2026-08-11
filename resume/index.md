---
layout: default
title: Resume
---

<style>
  h1 a {
    color: black; /* This specifically targets anchor tags inside h1 and sets their color */
    text-decoration: none; /* Optional: remove the underline if you don't want it */
  }

  /* You might also want to consider hover/active/visited states for the link */
  h1 a:hover {
    color: darkgray; /* Example: make it darker on hover */
  }

  h1 a:visited {
    color: black; /* Keep visited links black */
  }
</style>

Greenville, SC • [kennan.grant@gmail.com](mailto:kennan.grant@gmail.com) • [LinkedIn](https://www.linkedin.com/in/kennangrant/)

---

Engineer specializing in data-intensive applications, performance engineering, and agent-directed software development. I find the strategic problem, technical or organizational, before writing code, place deliberate bets, and own them to production. Most recently I replaced a vendor analytics platform with a self-hosted full-stack system that is **93% faster** on the heaviest dashboards, built solo from proposal to deployment, then drove the architecture and team-structure changes that made it sustainable.

---

### Experience

**Software Engineer (I → II)** *at* Simpliphy (*2024 – Present*)

- Identified a strategic mismatch between the company’s analytics product vision and its existing tooling (embedded Tableau), and made the case to leadership for a full-stack, open-source replacement.
- Placed an early bet that agentic AI development had matured enough to match the iteration speed of BI tools — then proved it: built the MVP solo and drove it to full functional parity within a year.
- Contributed to **$3M** in new ARR in which the analytics platform was a differentiating part of the enterprise product bundle.
- Achieved a **93% latency reduction** versus the legacy product on the most computationally intensive dashboards.
- Delivered capabilities the legacy tool could not: version-controlled and testable calculation logic, direct inspectability for client Q&A, custom UX and brand coherence, and elimination of vendor lock-in.
- Architected the stack end to end: MySQL (db) → DuckDB (cache) → Go (api) → Nginx (proxy) → React (spa). Roughly 125K lines of Go and TypeScript across 23 interactive analytics pages, operated as a one-person engineering team.
- Designed the multi-tenant security model: per-tenant DuckDB databases with row-level security as the source of truth, a backend capability registry with explicit route classification, and drift tests that keep routes, capabilities, and navigation aligned as pages are added.
- Diagnosed a gap in data-system ownership (no directly responsible individual, and misaligned incentives between product and engineering) and persuaded leadership to move analytics engineers under engineering, aligning accountability for long-lived data integrity.
- Proposed and supported migration of analytics pipelines from fragile MySQL stored procedures to an orchestrated Snowflake pipeline (Prefect) with retries and observability the prior system lacked; cut the nightly data pull from hours to **under an hour** via parallelization, making client data reliably ready each morning. Validated the cutover with side-by-side parity snapshots of MySQL-built and Snowflake-built caches.
- Resolved a two-year pattern of near-nightly reporting-database outages that corrupted downstream Snowflake data and forced manual morning re-runs. Diagnosed the system with Grafana and MySQL performance counters, tracing independent failure modes across the extraction, query, database-configuration, and operating-system layers: a non-sargable modulo shard predicate that multiplied read load ~10x; inefficient patterns across roughly 15 multi-tenant stored procedures; and persistent replication memory growth caused by Ubuntu’s default Transparent Huge Pages configuration. Rewrote rolling self-joins with window functions, corrected predicates and join order, indexed temporary tables, tuned InnoDB redo and flushing, and disabled Transparent Huge Pages. The full nightly load now completes without swap or progressive memory growth, with no hardware upgrade, validated across 60+ tenant schemas using row-count and row-hash parity.
- Traced a recurring server-side query spike to a per-row stored-function call and replaced it with set-based weekday arithmetic, cutting one core procedure's peak from **2.8M internal queries per second to under 500**.
- Founded the company’s internal AI practice (AI channel, weekly talks, shared tooling) and drove adoption of agentic development across the engineering team.
- Built **Yggdrasil**, a Go CLI/TUI (~50K LOC incl. tests) that lets me supervise many AI coding agents at once. Each agent works in its own git worktree with a dedicated branch, port block, and tmux workspace; agents signal through lifecycle hooks when they need me, and I can triage and respond from my phone. This tooling is how one engineer shipped the analytics platform solo.
- Every significant change starts from a spec. I authored an agent skill that produces design docs with explicit goals and non-goals, boundary contracts, invariants, and verifiable acceptance criteria, written so work can be handed between humans and agents without losing context.
- Agent output is held to **IguanaStyle**, my adaptation of TigerBeetle’s TigerStyle for application-layer Go: asserted invariants, explicit state transitions, no silent failure paths. The conventions live in agent-readable repo docs, are enforced by hooks, CI, and review checklists, and get refined continuously as part of the harness.
- The agent harness improves on a deliberate loop: after tasks, agents log mishaps and automation opportunities to a pattern log, and periodic reviews of that log decide whether to write a new skill, refine an existing one, or change policy. More than two dozen skills now cover root-cause analysis, CI repair, browser smoke checks, and supervised production data repairs.
- Currently building an agentic support layer enabling the client team to self-serve answers about dashboard logic.

**Career Break** (*2019 – 2024*)

- Stepped away from engineering; worked in hospitality in Miami, completed graduate coursework in another field, then returned.

**Data Science Engineer** *at* Metis Machine (*2018*)

- Built an ML pipeline for a classification model in Python and Spark SQL.
- Detected and removed a “future leak” in legacy training data that had inflated accuracy by 25 percentage points.
- Engineered new features and retrained the model on clean data, restoring reliable performance.

**Data Analyst** *at* Elder Research (*2016 – 2017*)

- Cleaned and processed a 1 TB healthcare dataset using PySpark and Spark SQL.
- Developed a logistic-regression model in R to predict donor propensity for a university fundraising campaign; deployed in MS SQL per client requirements.
- Built a patient no-show prediction model that informed scheduling optimizations.

---

### Independent Systems Work

**Rust Grind** — first-principles systems engineering in Rust

- Building small systems components from primitives to develop direct fluency with memory, concurrency, storage, networking, and operating-system behavior.

---

### Focus

- **Depth:** performance engineering, database internals, data-intensive systems, pipeline reliability, multi-tenant security, agentic development at scale
- **Working stack:** Go, TypeScript/React · DuckDB, Snowflake, MySQL · Prefect · self-hosted open-source infrastructure
- **Systems practice:** Rust through first-principles work in memory, concurrency, storage, networking, and operating-system interfaces

---

### Education

- **M.S., Computer Science** *at* Georgia Institute of Technology (*expected 2030*)<br>
  - Computing Systems specialization, focused on ML systems and compilers for AI accelerators — the software side of hardware-software co-design.
- **M.S., Data Science** *at* University of Virginia (*2017 – 2018*)<br>
  - GPA **3.93**<br>
  - Winner – Statistical-modeling competition. Lowest recorded error in competition’s history.<br>
  - Best Analyst - Peer-voted<br>
- **M.S., Commerce** *at* University of Virginia (*2014 – 2015*)<br>
  - 1st rank in class (quantitative finance)
  - Highest academic honor - Beta Gamma Sigma
- **B.A., English Literature** *at* University of Virginia (*2010 – 2014*)