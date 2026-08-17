# Vishnu Kanchi

Software engineer focused on backend services, distributed systems, and reliable software delivery. I build production-minded applications in Java and Python, with hands-on experience in transactional data, asynchronous job processing, real-time collaboration, Docker, and CI/CD.

My background in production GCP incident response shapes how I build: correctness, failure handling, observability, and automated verification are part of the implementation rather than an afterthought.

## Featured software projects

### [Pulse Queue](https://github.com/vishnukanchi9/pulse-queue)

Distributed task queue with durable job state, retries, and dead-letter handling.

- Separate Spring Boot API and worker containers with PostgreSQL as the source of truth.
- Redis ready, retry, and dead-letter queues; exponential backoff capped at five minutes.
- Browser monitoring dashboard plus GitHub Actions that test and build the production image on every push.

`Java` `Spring Boot` `PostgreSQL` `Redis` `Docker` `Flyway`

### [Ledger Service](https://github.com/vishnukanchi9/ledger-service)

Double-entry ledger API designed for correctness under concurrency.

- Idempotent transfers, deadlock-free row locking, immutable entries, and database-enforced no-overdraft protection.
- CI proves money conservation across 120 concurrent transfers and ensures repeated concurrent requests post once.

`Python` `FastAPI` `PostgreSQL` `SQLAlchemy` `Alembic` `pytest`

### [TeamBoard](https://github.com/vishnukanchi9/teamboard)

Real-time collaborative task workspace with a browser-first Kanban interface.

- Drag-and-drop task workflows, filtering, comments, member management, profile editing, and activity history.
- FastAPI WebSocket updates keep connected clients current; Docker packaging and GitHub Actions verify the app automatically.

`Python` `FastAPI` `WebSockets` `SQLite` `Docker` `pytest`

## Additional systems work

- [Kubernetes SLO Platform](https://github.com/vishnukanchi9/k8s-slo-platform) - Kubernetes reliability properties verified in CI through live traffic, failure injection, rolling updates, HPA scaling, and burn-rate alerts.
- [GCP Landing Zone](https://github.com/vishnukanchi9/gcp-landing-zone) - Multi-environment Terraform foundation delivered through keyless GitHub Actions with Workload Identity Federation.
- [Weather ETL Pipeline](https://github.com/vishnukanchi9/weather-etl-pipeline) - Idempotent Python ETL pipeline with BigQuery/SQLite warehousing and data-quality gates.

## Technologies

- **Languages:** Java, Python, JavaScript, SQL, Bash
- **Backend:** Spring Boot, FastAPI, REST APIs, WebSockets, SQLAlchemy
- **Data:** PostgreSQL, Redis, SQLite, BigQuery; transactions, schema design, Flyway, Alembic
- **Cloud & delivery:** Docker, Kubernetes, GCP, AWS, Terraform, GitHub Actions, Prometheus, Grafana

## Background

- M.S. in Computer Science, Stevens Institute of Technology - GPA 3.83/4.0
- Google Associate Cloud Engineer certified
- Previously supported production systems across Compute Engine, GKE, Cloud Storage, and IAM at Infosys

[LinkedIn](https://linkedin.com/in/vishnukanchi) · [GitHub](https://github.com/vishnukanchi9)
