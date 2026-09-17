### Hi, I'm Sidharth 👋
**Java Backend Developer | Spring Boot | PostgreSQL**

I build secure, scalable backend architectures and robust RESTful APIs. My focus is on designing reliable database schemas, optimizing query performance, and containerizing distributed systems to ensure seamless deployment.

### 🛠 Technical Arsenal
* **Backend & APIs:** Java, Spring Boot, RESTful Architecture, Microservices
* **Data & Infrastructure:** PostgreSQL, Redis, Docker, CI/CD (GitHub Actions)
* **Systems & Deployment:** Ubuntu Server, Arch Linux

---
### 💻 Featured Projects

#### [Remitlytics | Financial Core Engine & Invoicing Platform](https://github.com/Sidharth-Async/remitlytics-core.git)
*An event-driven, fault-tolerant financial backend and dashboard guaranteeing double-entry accounting integrity and zero-data-loss event delivery.*
* **Tech Stack:** Java 21, Spring Boot 3.3, PostgreSQL 16, Bucket4j, Flyway, Docker, Next.js 16
* **Double-Entry Ledger & State Invariants:** Architected an append-only, multi-tenant double-entry ledger enforcing balanced debit/credit transaction boundaries in PostgreSQL across `DRAFT ➔ SENT ➔ PAID/OVERDUE` invoice lifecycles.
* **Event-Driven Webhook Pipeline:** Decoupled external HTTP notifications using `@Async` event workers bound to `@TransactionalEventListener(AFTER_COMMIT)`, dropping API response latencies below 50ms and preventing phantom notifications on rolled-back transactions.
* **Resilience & Replay Engine:** Built an exponential backoff retry state machine with PostgreSQL-backed delivery tracking, dead-letter storage, and administrative replay endpoints (`/retry`) to recover failed dispatches.
* **Zero-Bypass Traffic Shaping:** Implemented an `@Order(1)` Bucket4j token-bucket servlet filter enforcing 300 req/min backpressure ahead of Spring's DispatcherServlet, complete with CORS preflight handling and standard `429 Too Many Requests` headers.

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
