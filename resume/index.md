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

Greenville, SC • kennangrant [ at ] gmail [ dot ] com

---

Full-stack engineer specializing in data-intensive applications and performance engineering. I find the strategic problem — technical or organizational — before writing code, place deliberate bets, and own them to production. Most recently I replaced a vendor analytics platform with a self-hosted full-stack system that is **93% faster** on the heaviest dashboards — built solo from proposal to deployment — then drove the architecture and team-structure changes that made it sustainable.

---

### Experience

**Software Engineer (I → II)** _at_ Simpliphy (_2024 – Present_)

- Identified a strategic mismatch between the company’s analytics product vision and its existing tooling (embedded Tableau), and made the case to leadership for a full-stack, open-source replacement.
- Placed an early bet that agentic AI development had matured enough to match the iteration speed of BI tools — then proved it: built the MVP solo and drove it to full functional parity within a year.
- Achieved a **93% latency reduction** versus the legacy product on the most computationally intensive dashboards.
- Delivered capabilities the legacy tool could not: version-controlled and testable calculation logic, direct inspectability for client Q&A, custom UX and brand coherence, and elimination of vendor lock-in.
- Architected the stack end to end: MySQL (db) → DuckDB (cache) → Go (api) → Nginx (proxy) → React (spa).
- Diagnosed a gap in data-system ownership — no directly responsible individual, and misaligned incentives between product and engineering — and persuaded leadership to move analytics engineers under engineering, aligning accountability for long-lived data integrity.
- Proposed and led migration of analytics pipelines from fragile MySQL stored procedures to an orchestrated Snowflake pipeline (Dagster/Prefect) with retries and observability the prior system lacked; cut the nightly data pull from hours to **under an hour** via parallelization, making client data reliably ready each morning.
- Founded the company’s internal AI practice — an AI channel, weekly talks, and shared tooling — driving adoption of agentic development; multiple engineers credit significant productivity gains to this influence.
- Built a production documentation chatbot and established the company’s first agentic AI development practices.

**Data Science Engineer** _at_ Metis Machine (_2018_)

- Built an ML pipeline for a classification model in Python and Spark SQL.
- Detected and removed a “future leak” in legacy training data that had inflated accuracy by 25 percentage points.
- Engineered new features and retrained the model on clean data, restoring reliable performance.

<!-- EDITOR NOTE: 2018–2024 gap needs a truthful one-line entry here (consulting, sabbatical, study, project). Do not leave the timeline unexplained at senior level. -->

**Data Analyst** _at_ Elder Research (_2016 – 2017_)

- Cleaned and processed a 1 TB healthcare dataset using PySpark and Spark SQL.
- Developed a logistic-regression model in R to predict donor propensity for a university fundraising campaign; deployed in MS SQL per client requirements.
- Built a patient no-show prediction model that informed scheduling optimizations.

---

### Technical Competencies

- **Languages:** Go, Python, JavaScript/TypeScript, R, SQL
- **Data & analytics:** DuckDB, Snowflake, MySQL, Spark / Spark SQL, PySpark
- **Web:** React, Nginx, full-stack architecture, REST APIs
- **Orchestration & infra:** Dagster/Prefect, replication, self-hosted open-source deployments
- **AI / agentic:** agentic development workflows, LLM-powered application features, internal enablement
- **Focus areas:** performance engineering, database internals, data-intensive systems, data-pipeline reliability
  
---

### Education

- **M.S., Data Science** _at_ University of Virginia (_2017 – 2018_)<br>
  - GPA **3.93**<br>
  - Winner – Statistical-modeling competition. Lowest recorded error in competition's history.<br>
  - Best Analyst - Peer-voted<br>
- **M.S., Commerce** _at_ University of Virginia (_2014 – 2015_)<br>
  - 1st rank in class (quantitative finance)
  - Highest academic honor - Beta Gamma Sigma
- **B.A., English Literature** _at_ University of Virginia (_2010 – 2014_)
