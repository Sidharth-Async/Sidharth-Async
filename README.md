### Hi, I'm Sidharth 👋
**Java Backend Developer | Spring Boot | PostgreSQL**

I build secure, scalable backend architectures and robust RESTful APIs. My focus is on designing reliable database schemas, optimizing query performance, and containerizing distributed systems to ensure seamless deployment.

### 🛠 Technical Arsenal
* **Backend & APIs:** Java, Spring Boot, RESTful Architecture, Microservices
* **Data & Infrastructure:** PostgreSQL, Redis, Docker, CI/CD (GitHub Actions)
* **Systems & Deployment:** Ubuntu Server, Arch Linux

---
### 💻 Featured Projects

#### [Remitlytics Core Engine](https://github.com/Sidharth-Async/remitlytics-core.git)
*An event-driven, fault-tolerant financial backend designed to handle invoice lifecycles and guarantee transaction integrity.*
* **Tech Stack:** Java 21, Spring Boot 3, PostgreSQL, Flyway, Docker
* **Event-Driven Architecture:** Implemented asynchronous webhook dispatching using `@TransactionalEventListener` to guarantee external third-party notifications only fire after successful database commits, preventing phantom reads.
* **Resilience:** Engineered a custom fault-tolerance mechanism utilizing exponential backoff and a PostgreSQL-backed Dead Letter Queue (DLQ) to safely park and recover failed webhook deliveries.
* **Data Integrity:** Designed a strict state-machine (DRAFT ➔ SENT ➔ PAID) that automatically triggers an immutable double-entry ledger system to ensure credits and debits always balance.

#### [Sentinel (Distributed Task Queue)](https://github.com/Sidharth-Async/task-queue-backend.git)
*Engineered a horizontally scalable background task processing queue to handle concurrent workloads without data corruption.*
* **Tech Stack:** Java, Spring Boot, PostgreSQL, Docker, CI/CD
* **Concurrency:** Solved worker collision bottlenecks by implementing PostgreSQL `FOR UPDATE SKIP LOCKED`, allowing multiple independent nodes to pull from the same queue safely.
* **Resilience:** Architected a self-healing "Janitor" mechanism using JPQL scheduled tasks to automatically detect and recycle orphaned processes resulting from simulated node failures.

#### [EcoStream (Logistics Tracking API)](https://github.com/Sidharth-Async/ecostream.git)
*Built a distributed backend service to handle and track real-time logistics data.*
* **Tech Stack:** Java, Spring Boot, Microservices, Redis
* **Performance:** Decoupled heavy data-processing tasks from the main user API to prevent the server from blocking during high-traffic spikes.
* **Optimization:** Implemented Redis caching strategies for frequently accessed routing data, significantly reducing direct read-load on the primary database and improving API response latency.
---

### 📬 Let's Connect
* **Upwork:** [View my Upwork Profile](https://www.upwork.com/freelancers/~01cac3d2726625b693?mp_source=share)
* **Email:** [sidharthyadav134134@gmail.com]
