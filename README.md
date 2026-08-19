# Vishnu Kanchi

Software engineer focused on backend services, distributed systems, and reliable software delivery. I build production-minded applications in Java, Python, and TypeScript, with hands-on experience in transactional data, asynchronous job processing, live service consoles, Docker, and CI/CD.

My background in production GCP incident response shapes how I build: correctness, failure handling, observability, and automated verification are part of the implementation rather than an afterthought.

## Featured software projects

### [Pulse Queue](https://github.com/vishnukanchi9/pulse-queue)

Distributed task queue with durable job state, retries, and dead-letter handling.

- Separate Spring Boot API and worker containers with PostgreSQL as the source of truth.
- Redis ready, retry, and dead-letter queues; exponential backoff capped at five minutes.
- Browser monitoring dashboard plus GitHub Actions that test and build the production image on every push.

`Java` `Spring Boot` `PostgreSQL` `Redis` `Docker` `Flyway`

### [Ledger Service](https://github.com/vishnukanchi9/ledger-service) · [Java implementation](https://github.com/vishnukanchi9/ledger-service-java)

Double-entry ledger API designed for correctness under concurrency — built twice, in Python and Java, against one specification.

- Idempotent transfers, deadlock-free row locking, immutable entries, and database-enforced no-overdraft protection.
- CI proves money conservation across 120 concurrent transfers and ensures repeated concurrent requests post once.
- The Java build carries the same guarantees through `@Lock(PESSIMISTIC_WRITE)` and Testcontainers. Recovering from a duplicate-key race takes two Spring beans, because a self-invoked `@Transactional` call bypasses the proxy and never opens the new transaction.

`Python` `FastAPI` `SQLAlchemy` `Alembic` · `Java` `Spring Boot` `JPA` `Flyway` · `PostgreSQL` `pytest` `JUnit 5` `Testcontainers`

### [Sentinel](https://github.com/vishnukanchi9/sentinel)

Live incident command console — service health, SEV-ranked incidents, and an append-only timeline.

- FastAPI + WebSockets; PostgreSQL in Docker Compose, ephemeral SQLite for the test suite.
- Service health is derived from open incidents. Acknowledge / assign / resolve are closed transitions; resolve is terminal.
- Notify-then-refetch board updates so connected consoles cannot desynchronise.

`Python` `FastAPI` `WebSockets` `PostgreSQL` `Docker` `pytest`

### [KANCHI](https://github.com/vishnukanchi9/kanchi)

Engineering portfolio with a print-ready resume and live labs for Pulse, Ledger, and Sentinel.

- React / TypeScript / TanStack Start. The labs implement the same contracts as the standalone services.
- Postgres-backed, guest-safe demos with optional sign-in for isolated workspaces.

`TypeScript` `React` `TanStack Start` `PostgreSQL`

## Additional systems work

- [Kubernetes SLO Platform](https://github.com/vishnukanchi9/k8s-slo-platform) - Kubernetes reliability properties verified in CI through live traffic, failure injection, rolling updates, HPA scaling, and burn-rate alerts.
- [GCP Landing Zone](https://github.com/vishnukanchi9/gcp-landing-zone) - Multi-environment Terraform foundation delivered through keyless GitHub Actions with Workload Identity Federation.
- [Weather ETL Pipeline](https://github.com/vishnukanchi9/weather-etl-pipeline) - Idempotent Python ETL pipeline with BigQuery/SQLite warehousing and data-quality gates.
- [TeamBoard](https://github.com/vishnukanchi9/teamboard) - Real-time collaborative Kanban board in FastAPI with WebSocket broadcast and Docker packaging.

## Technologies

- **Languages:** Java, Python, TypeScript, SQL, Bash
- **Testing:** JUnit 5, Testcontainers, pytest; integration and concurrency testing
- **Backend:** Spring Boot, FastAPI, REST APIs, WebSockets, SQLAlchemy
- **Data:** PostgreSQL, Redis, SQLite, BigQuery; transactions, schema design, Flyway, Alembic
- **Cloud & delivery:** Docker, Kubernetes, GCP, AWS, Terraform, GitHub Actions, Prometheus, Grafana

## Background

- M.S. in Computer Science, Stevens Institute of Technology
- Google Associate Cloud Engineer certified
- Previously supported production systems across Compute Engine, GKE, Cloud Storage, and IAM at Infosys

[LinkedIn](https://linkedin.com/in/vishnukanchi) · [GitHub](https://github.com/vishnukanchi9)
