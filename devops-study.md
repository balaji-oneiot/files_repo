# 🚀 DevOps Learning 


---

## 📌 Learning Order (Follow This Sequence)

```
Linux → Git → Networking → Docker → CI/CD (GitHub Actions)
  → Cloud (AWS) → Terraform → Kubernetes → Monitoring
  → Databases → Programming (Python + Bash)
```


---

## 🗂️ Full Summary Table

| #   | Topic | [Roadmap.sh](http://Roadmap.sh) Link |
|-----|-------|-----------------|
| 1   | Linux | [roadmap.sh/linux](https://roadmap.sh/linux) |
| 2   | Git   | [roadmap.sh/git-github](https://roadmap.sh/git-github) |
| 3   | Networking | [roadmap.sh/devops](https://roadmap.sh/devops) |
| 4   | Docker | [roadmap.sh/docker](https://roadmap.sh/docker) |
| 5   | CI/CD | [roadmap.sh/devops/automation-tools](https://roadmap.sh/devops/automation-tools) |
| 6   | Cloud (AWS) | [roadmap.sh/aws](https://roadmap.sh/aws) |
| 7   | Terraform | [developer.hashicorp.com/terraform/tutorials](https://developer.hashicorp.com/terraform/tutorials) |
| 8   | Kubernetes | [roadmap.sh/kubernetes](https://roadmap.sh/kubernetes) |
| 9   | Ansible | [roadmap.sh/devops/automation-tools](https://roadmap.sh/devops/automation-tools) |
| 10  | Monitoring | [roadmap.sh/devops/lifecycle](https://roadmap.sh/devops/lifecycle) |
| 11  | Databases | [roadmap.sh/sql](https://roadmap.sh/sql) · [roadmap.sh/mongodb](https://roadmap.sh/mongodb) |
| 12  | Programming | [roadmap.sh/python](https://roadmap.sh/python) · [roadmap.sh/devops/skills](https://roadmap.sh/devops/skills) |


---


---

## 1. 🐧 Linux & Shell Scripting

> The absolute foundation. Nearly all servers run Linux. You cannot be a DevOps engineer without it.

### What to Learn

**File System & Navigation**

* `ls`, `cd`, `pwd`, `mkdir`, `rm`, `cp`, `mv`, `find`, `locate`
* Understanding `/etc`, `/var`, `/home`, `/usr`, `/tmp` directories
* File permissions: `chmod`, `chown`, `chgrp`
* Reading: `cat`, `less`, `head`, `tail`, `grep`, `awk`, `sed`

**Users & Groups**

* `useradd`, `usermod`, `passwd`, `groups`
* `sudo` and the sudoers file — how privilege escalation works

**Processes**

* `ps aux`, `top`, `htop`, `kill`, `pkill`
* Background jobs: `&`, `fg`, `bg`, `nohup`
* `systemctl start/stop/enable/status` — managing services with systemd

**Networking Commands**

* `ping`, `curl`, `wget` — testing connectivity
* `netstat`, `ss` — viewing open ports and connections
* `ip addr`, `ifconfig` — checking network interfaces
* `nslookup`, `dig` — DNS lookups
* `ssh user@host`, `scp`, `rsync` — remote access and file transfer
* `ufw` / `iptables` — basic firewall rules

**Shell Scripting (Bash)**

* Variables, loops (`for`, `while`), conditionals (`if/else`)
* Functions and script arguments (`$1`, `$2`, `$@`)
* Cron jobs (`crontab -e`) — scheduling tasks
* Writing a simple deploy script (a real-world beginner project)

**Package Management**

* `apt` (Ubuntu/Debian): `apt install`, `apt update`, `apt upgrade`
* `yum`/`dnf` (RHEL/CentOS)

### 📚 Resources

| Resource | Link |
|----------|------|
| Linux Journey (interactive) | <https://linuxjourney.com> |
| The Linux Command Line (free book) | <https://linuxcommand.org/tlcl.php> |
| OverTheWire: Bandit (practice) | <https://overthewire.org/wargames/bandit> |
| [roadmap.sh](http://roadmap.sh) Linux Roadmap | <https://roadmap.sh/linux> |


---


---

## 2. 🔀 Git & Version Control

> Every single piece of infrastructure and code lives in Git. Non-negotiable skill.

### What to Learn

**Core Basics**

* `git init`, `git clone`, `git status`, `git log`
* The 3 stages: Working Directory → Staging (`git add`) → Repository (`git commit`)
* `.gitignore` — what to exclude from tracking

**Branching & Merging**

* `git branch`, `git checkout -b`, `git switch`
* `git merge` vs `git rebase` — know the difference
* Resolving merge conflicts (this WILL happen)

**Remote Repositories**

* `git push`, `git pull`, `git fetch`
* `git remote add origin <url>`
* Pull Requests (PRs) — the standard way to collaborate

**Workflows**

* **Feature Branch Workflow** — branch per feature, PR to merge
* **Trunk-based Development** — commit directly to main with feature flags
* `git tag v1.0.0` — marking releases
* `git stash` — temporarily saving unfinished work

**Practical DevOps Git Skills**

* Signing commits with GPG
* Using Git hooks for pre-commit checks
* Branch protection rules on GitHub/GitLab

### 📚 Resources

| Resource | Link |
|----------|------|
| Pro Git Book (official, free) | <https://git-scm.com/book/en/v2> |
| Learn Git Branching (visual, interactive) | <https://learngitbranching.js.org> |
| Atlassian Git Tutorials | <https://www.atlassian.com/git/tutorials> |
| [roadmap.sh](http://roadmap.sh) Git Roadmap | <https://roadmap.sh/git-github> |


---


---

## 3. 🌐 Networking Basics

> You need to understand how data travels so you can debug why things break.

### What to Learn

**Core Concepts**

* **IP Addresses** — IPv4 vs IPv6, public vs private (`192.168.x.x`)
* **Subnets & CIDR** — e.g. `10.0.0.0/24` means 256 addresses
* **DNS** — how domain names resolve to IP addresses; A records, CNAME, MX
* **Ports** — common ones: 22 (SSH), 80 (HTTP), 443 (HTTPS), 3306 (MySQL), 5432 (Postgres)

**Protocols**

* **TCP vs UDP** — TCP is reliable (web), UDP is fast (video calls)
* **HTTP/HTTPS** — request/response, status codes (200, 301, 404, 500, 503)
* **SSL/TLS** — how HTTPS certificates work; Let's Encrypt for free certs

**Practical Tools**

* `curl -v https://example.com` — see full HTTP headers
* `ping 8.8.8.8` — test basic connectivity
* `traceroute google.com` — see every hop between you and a server
* `nslookup` / `dig` — test DNS resolution
* `telnet host port` / `nc -zv host port` — test if port is open

**Load Balancing & Proxies**

* What a reverse proxy does (Nginx, HAProxy)
* Round-robin vs least-connections load balancing concepts

### 📚 Resources

| Resource | Link |
|----------|------|
| Cloudflare Learning Center | <https://www.cloudflare.com/learning> |
| Practical Networking | <https://www.practicalnetworking.net> |


---


---

## 4. 🐳 Docker & Containers

> The single most important tool to master early. Everything in modern DevOps runs in containers.

### What to Learn

**Core Concepts**

* What a container is vs a VM — containers share the OS kernel (much lighter)
* Images vs Containers — image is a blueprint, container is the running instance
* Docker Hub — the public registry for images

**Essential Commands**

```bash
docker pull nginx              # download image
docker run -d -p 80:80 nginx   # run container, map port
docker ps                      # list running containers
docker ps -a                   # all containers (including stopped)
docker exec -it <id> bash      # shell into a running container
docker logs <id>               # view container logs
docker stop / rm <id>          # stop and delete
docker images                  # list local images
docker rmi <image>             # remove image
```

**Writing Dockerfiles**

```dockerfile
FROM node:18-alpine       # base image
WORKDIR /app              # set working directory
COPY package*.json ./     # copy dependency files first (layer caching)
RUN npm install           # install dependencies
COPY . .                  # copy source code
EXPOSE 3000               # document the port
CMD ["node", "server.js"] # start command
```

* Understand layer caching — put infrequently changing stuff first
* Use `.dockerignore` (like `.gitignore` but for Docker)
* Multi-stage builds — keep final images small

**Docker Compose**

* Define multi-container apps (app + database + redis) in one YAML file
* `docker compose up -d`, `docker compose down`, `docker compose logs`

**Volumes & Networks**

* Volumes: persist data outside the container lifecycle
* Networks: containers communicate by service name (not IP)

### 📚 Resources

| Resource | Link |
|----------|------|
| Docker Official Docs | <https://docs.docker.com/get-started> |
| Play With Docker (browser labs, free) | <https://labs.play-with-docker.com> |
| Docker Curriculum | <https://docker-curriculum.com> |
| [roadmap.sh](http://roadmap.sh) Docker Roadmap | <https://roadmap.sh/docker> |


---


---

## 5. ⚙️ CI/CD Pipelines

> Automates the build → test → deploy cycle. "The backbone of modern DevOps." Start with GitHub Actions.

### What to Learn

**Core Concepts**

* **CI (Continuous Integration)** — every code push triggers automated build + tests
* **CD (Continuous Delivery)** — passing code is auto-deployed to staging
* **CD (Continuous Deployment)** — auto-deploys to production (no manual step)

**GitHub Actions (Start Here)**

* Workflows live in `.github/workflows/your-pipeline.yml`
* Triggers: `on: push`, `on: pull_request`, `on: schedule`
* Jobs and Steps — a job has multiple steps, steps run commands or Actions
* Marketplace Actions — pre-built steps (e.g., `actions/checkout@v4`, `docker/build-push-action`)

**A Basic Pipeline to Build**

```yaml
name: CI
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Run tests
        run: npm test
      - name: Build Docker image
        run: docker build -t myapp .
```

**What Pipelines Typically Do**


1. Lint code
2. Run unit tests
3. Build Docker image
4. Push to container registry
5. Deploy to staging/production

**Other Tools to Know**

* **Jenkins** — most widely used in enterprise; complex but powerful
* **GitLab CI** — tightly integrated if you use GitLab
* **CircleCI** — fast, easy to set up

### 📚 Resources

| Resource | Link |
|----------|------|
| GitHub Actions Official Docs | <https://docs.github.com/en/actions> |
| Jenkins Getting Started | <https://www.jenkins.io/doc/tutorials> |
| [roadmap.sh](http://roadmap.sh): DevOps Lifecycle | <https://roadmap.sh/devops/lifecycle> |
| [roadmap.sh](http://roadmap.sh): Automation Tools | <https://roadmap.sh/devops/automation-tools> |


---


---

## 6. ☁️ Cloud Platform (AWS First)

> Pick ONE cloud. AWS has the largest market share. Learn the core services deeply first.

### What to Learn (AWS)

**Compute**

* **EC2** — virtual machines in the cloud; instance types, key pairs, security groups
* **Lambda** — serverless functions; no server management

**Storage**

* **S3** — object storage for files, backups, static sites; bucket policies
* **EBS** — block storage attached to EC2 (like a hard drive)

**Networking**

* **VPC** — your private network in AWS; subnets, route tables, internet gateway
* **Security Groups** — stateful firewall rules per instance
* **IAM** — users, roles, policies; **never use root account**

**Managed Services**

* **RDS** — managed databases (MySQL, Postgres)
* **ECS/EKS** — run containers (ECS is easier, EKS is Kubernetes)
* **CloudWatch** — logs + metrics + alerts

**Cost Awareness**

* Set billing alerts so you don't get surprise bills
* Know the difference between on-demand vs reserved vs spot instances

### 📚 Resources

| Resource | Link |
|----------|------|
| AWS Free Tier | <https://aws.amazon.com/free> |
| AWS Skill Builder (free courses) | <https://skillbuilder.aws> |
| [roadmap.sh](http://roadmap.sh) AWS Roadmap | <https://roadmap.sh/aws> |
| Cloud Practitioner Exam (entry cert) | <https://aws.amazon.com/certification/certified-cloud-practitioner> |


---


---

## 7. 🏗️ Terraform (Infrastructure as Code)

> Write infrastructure as code — provision cloud resources reproducibly.

### What to Learn

**Core Concepts**

* IaC means your infrastructure is versioned in Git just like code
* Terraform is **declarative** — you describe desired state, Terraform figures out how

**Terraform Basics**

```hcl
# main.tf
provider "aws" {
  region = "us-east-1"
}

resource "aws_instance" "web" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"
}
```

* `terraform init` — download providers
* `terraform plan` — preview changes (always do this first!)
* `terraform apply` — create/update resources
* `terraform destroy` — tear everything down

**Key Concepts**

* **State file** (`terraform.tfstate`) — tracks what Terraform manages; **never commit to Git** (use remote state in S3)
* **Variables** (`variables.tf`) — parameterize your configs
* **Outputs** (`outputs.tf`) — expose values like IP addresses
* **Modules** — reusable terraform components (like functions)
* **Data sources** — read existing resources not managed by Terraform

### 📚 Resources

| Resource | Link |
|----------|------|
| HashiCorp Terraform Tutorials (official, free) | <https://developer.hashicorp.com/terraform/tutorials> |
| Terraform Registry (modules) | <https://registry.terraform.io> |
| [roadmap.sh](http://roadmap.sh): IaC Best Practices | <https://roadmap.sh/devops/best-practices> |


---


---

## 8. ☸️ Kubernetes (K8s)

> Container orchestration at scale. Learn Docker FIRST — Kubernetes manages Docker containers across many machines.

### What to Learn

**Why Kubernetes?**

* Docker Compose works on 1 machine. Kubernetes works across 100s of machines.
* Self-healing: crashed containers restart automatically
* Scaling: add/remove container replicas based on traffic

**Core Objects**

| Object | What it Does |
|--------|--------------|
| **Pod** | Smallest unit — 1+ containers running together |
| **Deployment** | Manages multiple replicas of a Pod; handles rolling updates |
| **Service** | Stable network endpoint to reach Pods (ClusterIP, NodePort, LoadBalancer) |
| **ConfigMap** | Store non-secret config (env variables, config files) |
| **Secret** | Store sensitive data (passwords, API keys) — base64 encoded |
| **Namespace** | Virtual cluster to isolate workloads |
| **Ingress** | HTTP/HTTPS routing rules into the cluster |

**Essential kubectl Commands**

```bash
kubectl get pods                              # list pods
kubectl get pods -n kube-system               # in a namespace
kubectl describe pod <name>                   # detailed info + events
kubectl logs <pod-name>                       # view logs
kubectl exec -it <pod-name> -- bash           # shell into pod
kubectl apply -f deployment.yaml              # apply a config
kubectl delete -f deployment.yaml             # delete resources
kubectl get services                          # list services
kubectl scale deployment myapp --replicas=3   # scale up/down
```

**A Simple Deployment YAML**

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: myapp
spec:
  replicas: 2
  selector:
    matchLabels:
      app: myapp
  template:
    metadata:
      labels:
        app: myapp
    spec:
      containers:
      - name: myapp
        image: myapp:1.0
        ports:
        - containerPort: 3000
```

**Helm (Package Manager for K8s)**

* Like `apt` but for Kubernetes apps
* `helm install my-nginx bitnami/nginx`
* Use Helm charts to install complex apps (databases, monitoring stacks)

**Where to Practice (Free)**

* `minikube` — run K8s locally on your laptop
* `kind` (K8s in Docker) — even lighter than minikube
* Killercoda — browser-based K8s labs, no install needed

### 📚 Resources

| Resource | Link |
|----------|------|
| Official Kubernetes Docs | <https://kubernetes.io/docs/home> |
| [roadmap.sh](http://roadmap.sh) Kubernetes Roadmap | <https://roadmap.sh/kubernetes> |
| Killercoda Interactive Labs | <https://killercoda.com> |
| Play with Kubernetes (browser) | <https://labs.play-with-k8s.com> |


---

## 10. 📊 Monitoring & Observability

> "Collecting metrics, logs, and traces to understand what is happening inside the system." If you can't see it, you can't fix it.

### What to Learn

**The 3 Pillars of Observability**

| Pillar | What it Is | Tool |
|--------|------------|------|
| **Metrics** | Numbers over time (CPU %, request rate, error rate) | Prometheus + Grafana |
| **Logs** | Text records of events that happened | ELK Stack / Loki |
| **Traces** | Following a request through multiple services | Jaeger / Zipkin |

**Prometheus + Grafana (Start Here)**

* **Prometheus** scrapes metrics from targets (apps, servers, K8s)
* `promql` basics: `rate(http_requests_total[5m])` — request rate over 5 min
* **Grafana** visualizes Prometheus data in dashboards
* Set up alerts: "Alert me when CPU > 85% for 5 minutes"

**ELK Stack (Logs)**

* **Elasticsearch** — stores and indexes logs
* **Logstash** — collects and parses logs from many sources
* **Kibana** — UI for searching and visualizing logs
* Modern alternative: **Loki + Grafana** (lighter, simpler)

**Key Metrics to Monitor**

* **Infrastructure:** CPU, memory, disk, network I/O
* **Application:** request latency (p50/p95/p99), error rate, throughput
* **Kubernetes:** pod restarts, node pressure, PVC usage

**Alerting Principles**

* Alert on **symptoms** (user-facing impact), not just causes
* Avoid alert fatigue — too many alerts = ignored alerts
* Use SLOs (Service Level Objectives) to set targets

### 📚 Resources

| Resource | Link |
|----------|------|
| Prometheus Official Docs | <https://prometheus.io/docs/introduction/overview> |
| Grafana Tutorials | <https://grafana.com/tutorials> |
| [roadmap.sh](http://roadmap.sh): DevOps Lifecycle | <https://roadmap.sh/devops/lifecycle> |
| Google SRE Book (free) | <https://sre.google/sre-book/table-of-contents> |


---


---

## 11. 🗄️ Database Basics

> DevOps engineers don't build databases — but you **will** manage them, back them up, tune them, monitor them, and connect apps to them.

### Core Concepts First

* **Database** — organized collection of structured data
* **DBMS** — the software managing it (MySQL, PostgreSQL, MongoDB)
* **SQL vs NoSQL** — relational tables (SQL) vs documents/key-value (NoSQL)
* **Schema** — structure/blueprint of the data (tables, columns, types)
* **ACID** — Atomicity, Consistency, Isolation, Durability — why transactions are safe
* **Index** — like a book index; speeds up queries dramatically on large tables


---

### Part A: SQL (Relational Databases)

> PostgreSQL is the gold standard. MySQL is everywhere. Learn SQL syntax — it works on both.

**SQL Commands**

```sql
-- Create a table
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100),
  email VARCHAR(150) UNIQUE NOT NULL,
  created_at TIMESTAMP DEFAULT NOW()
);

-- Insert data
INSERT INTO users (name, email) VALUES ('Alice', 'alice@example.com');

-- Query data
SELECT * FROM users;
SELECT name, email FROM users WHERE id = 1;
SELECT * FROM users ORDER BY created_at DESC;
SELECT * FROM users LIMIT 10 OFFSET 20;          -- pagination

-- Update & Delete
UPDATE users SET name = 'Bob' WHERE id = 1;
DELETE FROM users WHERE id = 1;

-- Joins (critical to understand)
SELECT orders.id, users.name
FROM orders
INNER JOIN users ON orders.user_id = users.id;

-- Aggregates
SELECT COUNT(*), AVG(price), MAX(price) FROM products;
SELECT category, COUNT(*) FROM products GROUP BY category;
```

**Key SQL Concepts**

* **PRIMARY KEY** — unique identifier for each row
* **FOREIGN KEY** — links one table to another (referential integrity)
* **JOIN types** — `INNER JOIN` (matching rows only), `LEFT JOIN` (all from left + matching from right)
* **Transactions** — `BEGIN`, `COMMIT`, `ROLLBACK` — group operations atomically
* **Indexes** — `CREATE INDEX idx_email ON users(email);` — know when to use them
* **Views** — saved queries as virtual tables
* **Normalization basics** — 1NF, 2NF, 3NF — eliminate data duplication

**DevOps-Specific DB Tasks**

* Connection strings: `postgresql://user:pass@host:5432/dbname`
* Backup: `pg_dump mydb > backup.sql`
* Restore: `psql mydb < backup.sql`
* **Migrations** — versioned schema changes (tools: Flyway, Liquibase, Alembic)


---

### Part B: NoSQL Databases

**MongoDB Basics**

* Stores data as **JSON-like documents** instead of rows/columns
* **Collection** = table, **Document** = row, **Field** = column

```js
// Insert
db.users.insertOne({ name: "Alice", age: 25, tags: ["devops", "cloud"] })

// Query
db.users.find({ age: { $gt: 20 } })
db.users.findOne({ name: "Alice" })

// Update
db.users.updateOne({ name: "Alice" }, { $set: { age: 26 } })

// Delete
db.users.deleteOne({ name: "Alice" })
```

**Redis Basics**

* **In-memory key-value store** — extremely fast (microseconds)
* Used for: caching, session storage, rate limiting, pub/sub

```bash
SET session:user123 "{'id':1,'name':'Alice'}"   # store
GET session:user123                              # retrieve
EXPIRE session:user123 3600                     # expire in 1hr
DEL session:user123                             # delete
INCR page_views                                 # atomic counter
```

**When to Use What**

| Scenario | Use |
|----------|-----|
| User accounts, orders, financial data | PostgreSQL / MySQL |
| Product catalogs, CMS content, logs | MongoDB |
| Session storage, caching, leaderboards | Redis |
| Search (full text) | Elasticsearch |
| Time-series metrics | InfluxDB / TimescaleDB |

### 📚 Resources

| Resource | Link |
|----------|------|
| [roadmap.sh](http://roadmap.sh) SQL Roadmap | <https://roadmap.sh/sql> |
| [roadmap.sh](http://roadmap.sh) PostgreSQL DBA Roadmap | <https://roadmap.sh/postgresql-dba> |
| [roadmap.sh](http://roadmap.sh) MongoDB Roadmap | <https://roadmap.sh/mongodb> |
| SQLZoo (interactive SQL practice) | <https://sqlzoo.net> |
| SQLBolt (beginner SQL) | <https://sqlbolt.com> |
| PostgreSQL Official Docs | <https://www.postgresql.org/docs> |
| MongoDB University (free) | <https://learn.mongodb.com> |
| Redis Official Docs | <https://redis.io/docs> |


---


---

## 12. 💻 Basic Programming Concepts

> You don't need to be a full developer. But DevOps engineers write scripts, pipelines, and automation code daily. **Python + Bash are the two must-know languages for DevOps.**


---

### Part A: Universal Programming Concepts

**Variables & Data Types**

```python
name = "Alice"           # String — text
age = 30                 # Integer — whole number
price = 9.99             # Float — decimal number
is_active = True         # Boolean — True or False
tags = ["web", "ops"]    # List/Array — ordered collection
config = {"port": 8080}  # Dictionary/Object — key-value pairs
```

**Operators**

```python
# Arithmetic
x = 10 + 5     # 15
x = 10 % 3     # 1 (modulo — remainder)

# Comparison (returns True/False)
10 > 5         # True
10 == 10       # True
10 != 5        # True

# Logical
True and False  # False
True or False   # True
not True        # False
```

**Control Flow**

```python
if cpu_usage > 90:
    print("CRITICAL: CPU too high")
elif cpu_usage > 70:
    print("WARNING: CPU elevated")
else:
    print("OK")

servers = ["web-01", "web-02", "db-01"]
for server in servers:
    print(f"Deploying to {server}")

retries = 0
while retries < 3:
    if deploy():
        break
    retries += 1
```

**Functions**

```python
def restart_service(service_name, host):
    print(f"Restarting {service_name} on {host}")
    return True

restart_service("nginx", "web-01")
```

**Error Handling**

```python
try:
    result = connect_to_db(host)
except ConnectionError as e:
    print(f"DB connection failed: {e}")
    exit(1)
finally:
    cleanup()   # always runs
```

**Working with Files**

```python
# Read a config file
with open("config.txt", "r") as f:
    content = f.read()

# Write a log
with open("deploy.log", "a") as f:
    f.write("Deployment started at 2024-01-01\n")

# Parse JSON (very common in DevOps)
import json
with open("config.json") as f:
    config = json.load(f)
print(config["database"]["host"])
```


---

### Part B: Python for DevOps (Priority Language)

**Why Python for DevOps?**

* AWS SDK (`boto3`) is Python
* Almost every DevOps tool has a Python API/SDK
* Great for automation scripts, API calls, data processing

**Key Python Skills for DevOps**

```python
# 1. Run shell commands from Python
import subprocess
result = subprocess.run(["git", "status"], capture_output=True, text=True)
print(result.stdout)

# 2. Work with environment variables
import os
db_password = os.environ.get("DB_PASSWORD", "default")
port = int(os.environ.get("PORT", 8080))

# 3. HTTP requests (call APIs)
import requests
response = requests.get("https://api.github.com/repos/torvalds/linux")
data = response.json()
print(f"Stars: {data['stargazers_count']}")

# 4. AWS with boto3
import boto3
s3 = boto3.client("s3")
s3.upload_file("backup.tar.gz", "my-bucket", "backups/backup.tar.gz")

# 5. Parse YAML (Kubernetes manifests, CI configs)
import yaml
with open("deployment.yaml") as f:
    manifest = yaml.safe_load(f)
print(manifest["spec"]["replicas"])
```

**Python Libraries to Know (DevOps focused)**

| Library | What It Does |
|---------|--------------|
| `subprocess` | Run shell commands from Python |
| `os` / `pathlib` | File system operations |
| `requests` | HTTP calls to APIs |
| `boto3` | AWS SDK — manage AWS resources |
| `paramiko` | SSH into servers programmatically |
| `PyYAML` | Read/write YAML files |
| `click` / `argparse` | Build CLI tools |
| `logging` | Proper logging (not just `print`) |


---

### Part C: Bash Scripting for DevOps

**Core Bash for DevOps**

```bash
#!/bin/bash
set -e          # exit on any error
set -u          # error on undefined variable

APP_NAME="myapp"
VERSION=$1      # first argument passed to script

if [ -f "docker-compose.yml" ]; then
    echo "Compose file found"
fi

if [ -z "$VERSION" ]; then
    echo "Error: No version specified"
    exit 1
fi

for env in dev staging prod; do
    echo "Deploying to $env"
    kubectl set image deployment/$APP_NAME \
        app=$APP_NAME:$VERSION \
        -n $env
done

log() {
    echo "[$(date '+%Y-%m-%d %H:%M:%S')] $1"
}
log "Deployment started"

CURRENT_PODS=$(kubectl get pods --no-headers | wc -l)
log "Current pod count: $CURRENT_PODS"
```

**Important Bash Patterns**

```bash
# Check if command succeeded
if ! docker build -t myapp:$VERSION .; then
    echo "Build failed!"
    exit 1
fi

# Redirect output
command > output.log 2>&1    # stdout + stderr to file
command >> output.log         # append (don't overwrite)
command 2>/dev/null           # suppress errors

# Here-doc (write multi-line content)
cat <<EOF > config.yaml
host: localhost
port: 5432
database: myapp
EOF
```


---

### Part D: Key Programming Terms Every DevOps Should Know

| Term | What It Means |
|------|---------------|
| **API** | Interface for programs to talk to each other; REST APIs use HTTP |
| **REST** | Architectural style for APIs: GET/POST/PUT/DELETE on URLs |
| **JSON** | Data format: `{"key": "value"}` — used everywhere |
| **YAML** | Human-readable config format used in Docker, K8s, CI pipelines |
| **Environment Variable** | Config value injected at runtime (`DB_HOST=localhost`) |
| **Idempotency** | Running something twice has the same result as running it once |
| **Dependency** | Code/library that your code needs to function |
| **Daemon** | Background process running continuously (e.g. `nginx`, `sshd`) |
| **Port** | Numbered endpoint on a server (80=HTTP, 443=HTTPS, 22=SSH) |
| **Endpoint** | A specific URL that an API exposes (`/api/users`) |
| **Payload** | The data body of an HTTP request/response |
| **Timeout** | Max time to wait for a response before giving up |
| **Retry logic** | Automatically try again if something fails |
| **Race condition** | Two processes modifying the same thing simultaneously — causes bugs |
| **Mutex/Lock** | Prevents race conditions by allowing only one process at a time |
| **Singleton** | Only one instance of something runs at a time |
| **Immutable** | Cannot be changed after creation (immutable infra = never patch, just replace) |
| **Stateless** | Doesn't remember previous requests (easier to scale) |
| **Stateful** | Remembers state between requests (databases, sessions) |
| **SDK** | Pre-built library to interact with a service (e.g. AWS SDK) |
| **OOP** | Object-Oriented Programming — code organized into objects with data + methods |
| **Refactoring** | Improving code structure without changing behavior |
| **Technical Debt** | Shortcuts taken now that make future work harder |

### 📚 Resources

| Resource | Link |
|----------|------|
| [roadmap.sh](http://roadmap.sh) Python Roadmap | <https://roadmap.sh/python> |
| [roadmap.sh](http://roadmap.sh): DevOps Skills (scripting section) | <https://roadmap.sh/devops/skills> |
| Python Official Tutorial (free) | <https://docs.python.org/3/tutorial> |
| Automate the Boring Stuff with Python (free book) | <https://automatetheboringstuff.com> |
| Bash Guide for Beginners (free) | <https://tldp.org/LDP/Bash-Beginners-Guide/html> |
| Exercism Python track (practice) | <https://exercism.org/tracks/python> |
| [roadmap.sh](http://roadmap.sh): Automation in DevOps | <https://roadmap.sh/devops/automation> |


---


---


