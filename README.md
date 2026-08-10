## Vishnu Kanchi

Cloud and reliability engineer. Google Cloud certified, M.S. in Computer Science from
Stevens Institute of Technology. Spent two years on the front line of production GCP
incidents at Infosys — Compute Engine, GKE, Cloud Storage, networking, IAM — and now
build the infrastructure and backend side of that work.

I care about systems whose correctness is *demonstrable*. Every repository below proves
its own central claim in CI on each push, rather than asserting it in a README.

---

### Projects

**[k8s-slo-platform](https://github.com/vishnukanchi9/k8s-slo-platform)** — A Kubernetes
service platform that attacks itself on every push. CI builds a real three-node cluster,
deploys, then verifies that a rolling restart under live traffic drops **zero** requests,
that an unready pod leaves the load balancer **without being restarted**, that the HPA
actually scales under CPU load, and that a deliberately burned error budget fires a
multi-window burn-rate alert and clears when the fault is removed.
`Kubernetes · Prometheus · Grafana · Alertmanager · kind · FastAPI`

**[ledger-service](https://github.com/vishnukanchi9/ledger-service)** — A double-entry
ledger API where the hard part is correctness under concurrency. Money is never created
or destroyed across 120 parallel transfers, thirty simultaneous withdrawals against ten
withdrawals' worth of balance yield exactly ten successes, and eight concurrent requests
sharing an idempotency key post exactly once. Guarantees rest on database constraints and
row locks taken in sorted order, not on application checks.
`FastAPI · PostgreSQL · SQLAlchemy · Alembic · pytest`

**[gcp-landing-zone](https://github.com/vishnukanchi9/gcp-landing-zone)** — Multi-environment
GCP foundation in Terraform, delivered by a pipeline that authenticates through Workload
Identity Federation with **no service account keys anywhere**. Private subnets with Cloud NAT
egress, IAP-only SSH, deny-by-default firewall logging, least-privilege service accounts, and
isolated remote state per environment. Every change gated behind a plan, a Checkov scan, and
review.
`Terraform · GCP · GitHub Actions · Workload Identity Federation`

**[weather-etl-pipeline](https://github.com/vishnukanchi9/weather-etl-pipeline)** — An
idempotent ETL pipeline loading API data into a star-schema warehouse on BigQuery and SQLite,
with MD5 surrogate keys, delete-then-insert loads that hold row counts constant across re-runs,
and data quality gates between transform and load.
`Python · BigQuery · SQLite · GitHub Actions`

---

### Working with

**Cloud** · GCP (Compute Engine, GKE, VPC, Cloud NAT, IAM, IAP, BigQuery), AWS
**Infrastructure as code** · Terraform, Kustomize, Checkov
**Containers & orchestration** · Docker, Kubernetes
**Reliability** · SLIs/SLOs, error budgets, burn-rate alerting, postmortems, runbooks
**Backend** · Python, FastAPI, SQLAlchemy, PostgreSQL, pytest
**CI/CD** · GitHub Actions

**Certified** · Google Cloud Associate Cloud Engineer

---

[LinkedIn](https://linkedin.com/in/vishnukanchi)
