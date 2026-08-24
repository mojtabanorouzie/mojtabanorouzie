# Mojtaba Norouzi

**Senior Software Engineer — backend and distributed systems.** Tehran, Iran. Open to relocation in the EU.

Eight years building backend systems for e-commerce, logistics and financial services; the last four at Okala, one of Iran's largest online grocery platforms. Day to day that means C#/.NET, event-driven services over Kafka, Clean Architecture and DDD, running on Kubernetes.

Before that, an M.Sc. in Artificial Intelligence from the Multi-Agent Systems Lab at Shahid Beheshti University, and a peer-reviewed paper on transfer learning for traffic signal control. The repositories below are personal work — research code, streaming systems, and things built to understand a problem properly.

---

### Selected work

| Project | What it is |
| :--- | :--- |
| **[delayed-order-sms-flink](https://github.com/mojtabanorouzie/delayed-order-sms-flink)** | Apache Flink job that detects orders which pass their expected delivery time without being delivered or cancelled, and emits idempotent SMS commands to Kafka. Keyed per-order state with processing-time timers that reschedule when the ETA moves; malformed events routed to a dead-letter topic via side outputs. Java, with a Docker Compose lab and an end-to-end suite. |
| **[kondor](https://github.com/mojtabanorouzie/kondor)** | Cross-platform spaced-repetition flashcards. The substance is the sync layer: a last-write-wins merge that is commutative and idempotent, deletion tombstones so a delete is never resurrected by a peer that never saw it, and a delta protocol shipping only what changed since a client's last cursor. Expo/React Native over a self-hosted Fastify server. |
| **[Reinforcement-Learning-TSC](https://github.com/mojtabanorouzie/Reinforcement-Learning-TSC)** | Multi-agent reinforcement learning for traffic signals, built in 2018 against the Aimsun microsimulator. One tabular agent per junction ranks its four approach queues into 24 states and redistributes green time across 19 fixed-cycle splits, learning on-line from the change in delay. |
| **[Holonic-Multi-Agent-System-TSC](https://github.com/mojtabanorouzie/Holonic-Multi-Agent-System-TSC)** | The two-level extension of that work. Intersections still learn independently, but are clustered at runtime into *holons* by measured traffic coupling; each holon's agent constrains which timings its members may choose and supplies 30% of their reward — so coordination emerges without a joint action space. |
| **[prism-cognitive-model](https://github.com/mojtabanorouzie/prism-cognitive-model)** | Three cooperating Claude Code sub-agents that reverse-engineer a behavior into competing falsifiable hypotheses, then test them with small pre-registered experiments. Built around a single-writer rule: two agents propose confidence changes, only the third commits them. No code — the agents are prompts. English and Persian. |

---

### Research

**Experience classification for transfer learning in traffic signal control**
Norouzi, Abdoos, Bazzan — *The Journal of Supercomputing* **77**, 780–795 (2021)
[doi.org/10.1007/s11227-020-03287-x](https://doi.org/10.1007/s11227-020-03287-x)

Both traffic-signal repositories above come from this line of work: `Reinforcement-Learning-TSC` holds the single-level source-task code that generates and exports agent experience, and `Holonic-Multi-Agent-System-TSC` the hierarchical extension.

---

### Stack

**Languages & frameworks** — C#, .NET 6–10, ASP.NET Core, Entity Framework Core
**Architecture** — Clean Architecture, DDD, event-driven design, transactional outbox, REST versioning
**Messaging & data** — Apache Kafka, RabbitMQ, Redis, SQL Server, geospatial (NetTopologySuite)
**Infrastructure** — Kubernetes, Docker, GitLab CI
**Observability** — Prometheus, Serilog, Elasticsearch, Elastic APM
**Testing** — xUnit, Testcontainers, BDD (Gherkin/Reqnroll)

---

### Elsewhere

[mojtaba.tech](https://mojtaba.tech) · [LinkedIn](https://www.linkedin.com/in/mojtabanorouzi/) · [mojtaba.norouzie@gmail.com](mailto:mojtaba.norouzie@gmail.com)
