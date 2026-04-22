# Syllabus 2: Mid-Level Cloud/DevOps Engineer Roadmap

## 🎯 12-Week Production-Grade Engineering Program (AWS + Kubernetes Focus)


## Program Overview

| Field | Detail |
|-------|--------|
| **Target Roles** | Cloud Engineer, DevOps Engineer, Platform Engineer, SRE (Junior), Infrastructure Engineer |
| **Duration** | 3 Months (12 Weeks) |
| **Commitment** | 20–25 hours/week (3–4 hours daily) |
| **Prerequisite** | Syllabus 1 complete OR equivalent hands-on AWS experience (6+ months) |
| **Cloud Focus** | AWS + Kubernetes (cloud-agnostic skills) |
| **Expected Outcome** | Ready for Mid-Level roles, able to design and manage production systems independently |


## High-Level Roadmap

```
Month 1: IaC + Containers              Month 2: Kubernetes + CI/CD            Month 3: Observability + Projects
├── Week 1: Terraform Fundamentals     ├── Week 5: Kubernetes Fundamentals    ├── Week 9:  Prometheus + Grafana
├── Week 2: Terraform Advanced + Ansible├── Week 6: Kubernetes Advanced + Helm ├── Week 10: Logging + Tracing
├── Week 3: Docker Deep Dive           ├── Week 7: GitHub Actions + Jenkins   ├── Week 11: Capstone Project
└── Week 4: Docker Compose + Registry  └── Week 8: GitOps + EKS (Managed K8s) └── Week 12: Mid-Level Interview Prep
```


## Syllabus 1 থেকে পার্থক্য

| বিষয় | Syllabus 1 (Junior) | Syllabus 2 (Mid-Level) |
|------|---------------------|------------------------|
| Focus | AWS console + basics | Automation + production patterns |
| Infrastructure | Manual console clicks | Terraform (everything as code) |
| Deployment | Single EC2/S3 | Kubernetes clusters |
| CI/CD | Basic GitHub Actions | Full pipelines + GitOps |
| Monitoring | CloudWatch only | Prometheus + Grafana + ELK |
| Mindset | "How do I use AWS?" | "How do I design reliable systems?" |


# MONTH 1: INFRASTRUCTURE AS CODE + CONTAINERS

Manual clicks এখন শেষ। এই মাসে সব infrastructure code হিসেবে লিখবে, এবং application গুলোকে container-এ pack করবে।


## 🗓️ Week 1: Terraform Fundamentals

**Focus:** Infrastructure as Code — AWS resources কোড দিয়ে provision করা

### 🎯 Learning Objectives
- Infrastructure as Code (IaC) এর concept এবং benefits বুঝতে পারবে
- Terraform HCL syntax দিয়ে AWS resources provision করতে পারবে
- Terraform workflow (init → plan → apply → destroy) master করতে পারবে
- Variables, outputs, এবং data sources effectively ব্যবহার করতে পারবে

### Lecture Topics

| # | Lecture Title |
|---|---------------|
| 1.1 | What is Infrastructure as Code and Why It Matters |
| 1.2 | IaC Tools Comparison (Terraform vs CloudFormation vs Pulumi vs CDK) |
| 1.3 | Terraform Installation and Authentication Setup |
| 1.4 | HCL (HashiCorp Configuration Language) Syntax Basics |
| 1.5 | Providers, Initialization, and terraform init |
| 1.6 | Resources — Core Building Block |
| 1.7 | Input Variables (variables.tf, .tfvars files) |
| 1.8 | Output Values and Locals |
| 1.9 | Data Sources — Reading Existing Infrastructure |
| 1.10 | The Terraform Workflow (plan, apply, destroy) |
| 1.11 | Understanding Terraform State File |
| 1.12 | Meta-arguments (count, for_each, depends_on, lifecycle) |
| 1.13 | Built-in Functions and Expressions |
| 1.14 | Provisioners (when and why to avoid them) |
| 1.15 | Dynamic Blocks |

### Hands-on Tasks
- [ ] Terraform দিয়ে একটা VPC তৈরি করো (2 public + 2 private subnets, IGW, NAT, route tables)
- [ ] EC2 instance launch করো Terraform দিয়ে, user-data script সহ
- [ ] S3 bucket create করো versioning, encryption, lifecycle rules সহ
- [ ] RDS MySQL instance provision করো proper security groups দিয়ে
- [ ] Variables ব্যবহার করে dev/prod environment switching করতে পারো এমন config লিখো
- [ ] `terraform destroy` করে সব resources clean up করো (unexpected bill থেকে বাঁচতে)

### Resources
- **Free:** [HashiCorp Learn Terraform](https://developer.hashicorp.com/terraform/tutorials) (official, excellent)
- **YouTube:** TechWorld with Nana's Terraform course (full free course), Anton Putra
- **Docs:** [Terraform AWS Provider Docs](https://registry.terraform.io/providers/hashicorp/aws/latest/docs) (bookmark this!)
- **Practice:** [Terraform Associate Practice Exam](https://www.udemy.com/course/terraform-associate-practice-exam/)

### Week 1 Checkpoint
**Deliverable:** GitHub repo `terraform-aws-starter` তৈরি করো যেখানে ৫টা reusable Terraform configuration থাকবে — VPC, EC2, S3, RDS, IAM। প্রতিটার জন্য আলাদা README, এবং main README-এ usage instructions। Screenshot দিয়ে prove করো সব resources successfully deploy হয়েছে।


## 🗓️ Week 2: Terraform Advanced + Ansible Basics

**Focus:** Production-ready Terraform patterns + Configuration Management with Ansible

### 🎯 Learning Objectives
- Reusable Terraform modules design এবং implement করতে পারবে
- Remote state management S3 + DynamoDB দিয়ে setup করতে পারবে
- Multiple environments (dev, staging, prod) manage করতে পারবে Terraform workspaces/directories দিয়ে
- Ansible দিয়ে server configuration automate করতে পারবে

### Lecture Topics

**Part A: Terraform Advanced**

| # | Lecture Title |
|---|---------------|
| 2.1 | Terraform Modules — Creating and Using |
| 2.2 | Module Sources (Local, Git, Registry) |
| 2.3 | Public Module Registry (terraform-aws-modules) |
| 2.4 | Private Module Repositories |
| 2.5 | Remote State Backend (S3 + DynamoDB Locking) |
| 2.6 | Terraform Workspaces vs Directory-based Environments |
| 2.7 | Managing Multiple Environments (dev/staging/prod) |
| 2.8 | Importing Existing Infrastructure (terraform import) |
| 2.9 | Refactoring and Moving Resources (moved blocks) |
| 2.10 | Terraform Cloud and Terraform Enterprise Overview |
| 2.11 | Best Practices and Anti-patterns |
| 2.12 | Terraform Testing (terratest, terraform test) |

**Part B: Ansible Basics**

| # | Lecture Title |
|---|---------------|
| 2.13 | Configuration Management vs Infrastructure Provisioning |
| 2.14 | Ansible Architecture (Control Node, Managed Nodes, SSH) |
| 2.15 | Installation and Inventory File Structure |
| 2.16 | Ad-hoc Commands for Quick Tasks |
| 2.17 | Playbooks and YAML Syntax |
| 2.18 | Modules (apt, copy, template, service, user) |
| 2.19 | Variables, Facts, and Jinja2 Templates |
| 2.20 | Handlers and Conditional Execution |
| 2.21 | Roles and Ansible Galaxy |
| 2.22 | Ansible Vault for Secrets Management |
| 2.23 | Terraform + Ansible Integration Pattern |

### Hands-on Tasks
- [ ] একটা reusable VPC module তৈরি করো যেটা যেকোনো project-এ use করা যাবে
- [ ] Remote state backend setup করো S3 + DynamoDB দিয়ে (state locking সহ)
- [ ] Same Terraform code থেকে dev এবং prod environment deploy করো different variables দিয়ে
- [ ] Ansible playbook লিখো যেটা একটা fresh Ubuntu server-এ Nginx + Node.js + PM2 install করবে
- [ ] Terraform দিয়ে EC2 provision করে Ansible দিয়ে configure করো (integrated workflow)

### Resources
- **Terraform Modules:** [AWS VPC Module](https://github.com/terraform-aws-modules/terraform-aws-vpc) (study the source code)
- **YouTube:** Anton Putra's "Terraform for Production" series, Jeff Geerling's Ansible tutorials
- **Book:** "Terraform: Up & Running" by Yevgeniy Brikman (recommended)
- **Ansible:** [Ansible Official Documentation](https://docs.ansible.com/) (excellent structure)

### Week 2 Checkpoint
**Deliverable:** GitHub repo `terraform-modules-collection` যেখানে ৩টা production-ready modules থাকবে — `vpc`, `eks-cluster-base`, `ecs-service`। সাথে একটা `environments/` folder যেখানে dev/staging/prod এর জন্য আলাদা config। Ansible playbook collection `ansible-lamp-stack` GitHub-এ push করো।


## 🗓️ Week 3: Docker Deep Dive

**Focus:** Containerization mastery — "It works on my machine" সমস্যার permanent solution

### 🎯 Learning Objectives
- Container vs VM এর difference বুঝতে পারবে architectural level-এ
- Production-ready Dockerfile লিখতে পারবে multi-stage builds সহ
- Container networking এবং storage concepts master করতে পারবে
- Image security best practices apply করতে পারবে

### Lecture Topics

| # | Lecture Title |
|---|---------------|
| 3.1 | Why Containers? Problems They Solve |
| 3.2 | Container vs Virtual Machine — Architectural Differences |
| 3.3 | Docker Architecture (Daemon, Client, Images, Registry) |
| 3.4 | Installing Docker on Linux, Mac, Windows |
| 3.5 | Docker Desktop vs Docker Engine |
| 3.6 | Images vs Containers — Clear Distinction |
| 3.7 | Essential Commands (run, ps, exec, logs, inspect, stop, rm) |
| 3.8 | Dockerfile Instructions Deep Dive (FROM, RUN, COPY, ENV, EXPOSE, CMD, ENTRYPOINT) |
| 3.9 | CMD vs ENTRYPOINT — The Common Confusion Solved |
| 3.10 | Building and Tagging Custom Images |
| 3.11 | Understanding Image Layers and Caching Strategy |
| 3.12 | Multi-Stage Builds for Small Production Images |
| 3.13 | Choosing Base Images (Alpine, Slim, Distroless) |
| 3.14 | Docker Networking Types (bridge, host, none, overlay) |
| 3.15 | Custom Networks and Container Communication |
| 3.16 | Data Persistence (Volumes vs Bind Mounts vs tmpfs) |
| 3.17 | Docker Compose Preview (covered in Week 4) |
| 3.18 | Container Security Best Practices |
| 3.19 | Image Vulnerability Scanning (Trivy, Snyk) |
| 3.20 | Debugging Containers (exec, logs, inspect, events) |

### Hands-on Tasks
- [ ] Node.js application-এর জন্য optimized Dockerfile লিখো multi-stage build সহ (final image < 100MB)
- [ ] Python Flask app containerize করো, gunicorn দিয়ে production-ready করো
- [ ] ৩টা container run করো custom bridge network-এ — web, app, db — inter-container communication verify করো
- [ ] Named volume দিয়ে PostgreSQL data persist করো container restart-এর পরেও
- [ ] Trivy দিয়ে একটা image scan করো, vulnerabilities fix করে re-scan করো

### Resources
- **Free Full Course:** [TechWorld with Nana's Docker Tutorial (3 hours)](https://www.youtube.com/watch?v=3c-iBn73dDE)
- **Interactive:** [Play with Docker](https://labs.play-with-docker.com/) (free sandbox)
- **Docs:** [Docker Official Documentation](https://docs.docker.com/)
- **Best Practices:** [Dockerfile Best Practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)

### Week 3 Checkpoint
**Deliverable:** GitHub repo `docker-practical-examples` যেখানে ৫টা different application-এর containerized version থাকবে — Node.js API, Python Flask, Go binary, React frontend, PostgreSQL custom image। প্রতিটার জন্য optimized Dockerfile এবং detailed README (build time, image size, security scan result সহ)।


## 🗓️ Week 4: Docker Compose + Multi-Container Applications + Registry

**Focus:** Multiple containers একসাথে orchestrate করা এবং production-grade image registry

### 🎯 Learning Objectives
- Docker Compose দিয়ে multi-container applications define এবং run করতে পারবে
- AWS ECR ব্যবহার করে private image registry manage করতে পারবে
- Development এবং production environment-এর জন্য আলাদা compose configurations বানাতে পারবে
- Container image security এবং optimization techniques apply করতে পারবে

### Lecture Topics

**Part A: Docker Compose**

| # | Lecture Title |
|---|---------------|
| 4.1 | Why Docker Compose? Multi-Container Orchestration |
| 4.2 | docker-compose.yml Structure and Version |
| 4.3 | Services, Networks, Volumes Definition |
| 4.4 | Environment Variables and .env Files |
| 4.5 | depends_on, Health Checks, and Startup Order |
| 4.6 | Scaling Services with Compose |
| 4.7 | Override Files (docker-compose.override.yml) |
| 4.8 | Building Images via Compose |
| 4.9 | Profiles for Conditional Services |
| 4.10 | Compose for Development vs Production |
| 4.11 | Limitations of Compose (Why Kubernetes?) |

**Part B: Registries and Production Images**

| # | Lecture Title |
|---|---------------|
| 4.12 | Public vs Private Registries |
| 4.13 | DockerHub Deep Dive (Rate Limits, Official Images) |
| 4.14 | AWS ECR (Elastic Container Registry) Setup |
| 4.15 | ECR Authentication and Pushing Images |
| 4.16 | ECR Lifecycle Policies for Cost Management |
| 4.17 | Image Tagging Strategies (latest, semantic versioning, git SHA) |
| 4.18 | Self-Hosted Registry (Harbor Introduction) |
| 4.19 | Image Signing with Cosign |
| 4.20 | Introduction to Container Orchestration (Leading to Kubernetes) |

### Hands-on Tasks
- [ ] একটা full-stack application docker-compose.yml বানাও — React frontend + Node.js API + PostgreSQL + Redis
- [ ] Development এবং production এর জন্য আলাদা compose files লিখো (override pattern ব্যবহার করে)
- [ ] AWS ECR-এ একটা private repository create করো এবং Docker image push করো
- [ ] GitHub Actions দিয়ে automated image build + push to ECR pipeline বানাও
- [ ] Harbor self-hosted registry deploy করো একটা EC2 instance-এ (bonus advanced task)

### Resources
- **YouTube:** "Docker Compose will change how you use Docker" by ArjanCodes
- **ECR Tutorial:** [AWS ECR Getting Started](https://docs.aws.amazon.com/AmazonECR/latest/userguide/getting-started-cli.html)
- **Compose Examples:** [awesome-compose](https://github.com/docker/awesome-compose) (100+ real examples)

### Week 4 Checkpoint
**Deliverable:** GitHub repo `multi-container-webapp` যেখানে complete MERN stack বা similar stack docker-compose দিয়ে run হবে। GitHub Actions workflow automated image push করবে ECR-এ। Blog post লিখো "Docker Compose to Production: A Practical Guide" title-এ।


# 📅 MONTH 2: KUBERNETES + CI/CD

এই মাস হলো সবচেয়ে important। Industry-এ Kubernetes skill-এর demand সবচেয়ে বেশি। ধৈর্য সহকারে শিখতে হবে।

## 🗓️ Week 5: Kubernetes Fundamentals

**Focus:** Kubernetes এর core concepts — Pods থেকে Deployments পর্যন্ত

### 🎯 Learning Objectives
- Kubernetes কেন দরকার এবং এটা Docker Compose থেকে কীভাবে আলাদা সেটা explain করতে পারবে
- Local Kubernetes cluster (Minikube/kind) setup এবং manage করতে পারবে
- Pods, Deployments, Services deploy এবং manage করতে পারবে kubectl দিয়ে
- YAML manifests লিখতে পারবে Kubernetes resources-এর জন্য

### Lecture Topics

| # | Lecture Title |
|---|---------------|
| 5.1 | Why Kubernetes? Problems Docker Compose Cannot Solve |
| 5.2 | Kubernetes Architecture Deep Dive |
| 5.3 | Control Plane Components (API Server, etcd, Scheduler, Controller Manager) |
| 5.4 | Worker Node Components (kubelet, kube-proxy, Container Runtime) |
| 5.5 | Setting Up Local Cluster (Minikube, kind, Docker Desktop) |
| 5.6 | kubectl — The Command Line Interface |
| 5.7 | kubectl Essentials (get, describe, logs, exec, apply, delete) |
| 5.8 | Pods — The Smallest Deployable Unit |
| 5.9 | Pod Lifecycle and Phases |
| 5.10 | Multi-Container Pods (Sidecar, Ambassador, Adapter patterns) |
| 5.11 | ReplicaSets — Ensuring Desired State |
| 5.12 | Deployments — The Most Used Resource |
| 5.13 | Rolling Updates and Rollbacks |
| 5.14 | Services — Networking in Kubernetes |
| 5.15 | Service Types (ClusterIP, NodePort, LoadBalancer, ExternalName) |
| 5.16 | Namespaces for Organization |
| 5.17 | Labels, Selectors, and Annotations |
| 5.18 | Imperative vs Declarative Approach |
| 5.19 | Writing Effective YAML Manifests |
| 5.20 | Debugging Pods (Common Errors: ImagePullBackOff, CrashLoopBackOff) |

### Hands-on Tasks
- [ ] Minikube বা kind দিয়ে local Kubernetes cluster setup করো
- [ ] একটা simple web app deploy করো Deployment + Service দিয়ে
- [ ] Deployment scale up করো 1 থেকে 5 replicas-এ, verify pods distribute হচ্ছে
- [ ] Rolling update perform করো, এরপর rollback করো previous version-এ
- [ ] 3 namespaces তৈরি করো (dev, staging, prod), same app deploy করো প্রতিটায়
- [ ] Intentionally একটা bad pod create করো (wrong image), debug করে fix করো

### Resources
- **Free Full Course:** [TechWorld with Nana's Kubernetes Crash Course (4 hours)](https://www.youtube.com/watch?v=s_o8dwzRlu4)
- **Interactive:** [Killercoda Kubernetes Scenarios](https://killercoda.com/kubernetes) (free hands-on labs)
- **Docs:** [Kubernetes Official Documentation](https://kubernetes.io/docs/home/)
- **Cheat Sheet:** [kubectl Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

### Week 5 Checkpoint
**Deliverable:** GitHub repo `kubernetes-basics-lab` যেখানে ১০+ YAML manifests থাকবে বিভিন্ন scenarios-এর জন্য। প্রতিটা YAML-এ inline comments থাকবে explaining each field। Architecture diagram (draw.io) তৈরি করো explaining how components interact।


## 🗓️ Week 6: Kubernetes Advanced + Helm

**Focus:** Production-grade Kubernetes — configuration management, storage, security, এবং Helm

### 🎯 Learning Objectives
- Sensitive data এবং configuration properly manage করতে পারবে (Secrets, ConfigMaps)
- Stateful applications deploy করতে পারবে StatefulSets এবং PersistentVolumes দিয়ে
- Ingress controllers ব্যবহার করে HTTP routing করতে পারবে
- RBAC দিয়ে cluster security enforce করতে পারবে
- Helm charts ব্যবহার করে এবং বানিয়ে complex applications package করতে পারবে

### Lecture Topics

**Part A: Configuration and Storage**

| # | Lecture Title |
|---|---------------|
| 6.1 | ConfigMaps for Non-Sensitive Configuration |
| 6.2 | Secrets for Sensitive Data (and Their Limitations) |
| 6.3 | Mounting ConfigMaps/Secrets as Files vs Env Variables |
| 6.4 | External Secrets Operator (AWS Secrets Manager integration) |
| 6.5 | Persistent Volumes (PV) and Persistent Volume Claims (PVC) |
| 6.6 | StorageClasses and Dynamic Provisioning |
| 6.7 | StatefulSets for Databases and Ordered Workloads |
| 6.8 | DaemonSets for Node-Level Agents (logging, monitoring) |
| 6.9 | Jobs and CronJobs for Batch Workloads |

**Part B: Networking and Ingress**

| # | Lecture Title |
|---|---------------|
| 6.10 | Kubernetes Networking Model |
| 6.11 | Ingress Concept and Ingress Controllers |
| 6.12 | Nginx Ingress Controller Setup |
| 6.13 | SSL/TLS Termination with cert-manager |
| 6.14 | Path-based and Host-based Routing |
| 6.15 | Network Policies for Pod-to-Pod Security |

**Part C: Scaling and Security**

| # | Lecture Title |
|---|---------------|
| 6.16 | Resource Requests and Limits |
| 6.17 | Horizontal Pod Autoscaler (HPA) — Metrics-based Scaling |
| 6.18 | Vertical Pod Autoscaler (VPA) Overview |
| 6.19 | Cluster Autoscaler Concept |
| 6.20 | RBAC (Roles, RoleBindings, ClusterRoles, ClusterRoleBindings) |
| 6.21 | ServiceAccounts and Pod Security |
| 6.22 | Pod Security Standards (Restricted, Baseline, Privileged) |

**Part D: Helm — The Package Manager**

| # | Lecture Title |
|---|---------------|
| 6.23 | Why Helm? Templating Problem Explained |
| 6.24 | Installing Helm and Using Public Charts |
| 6.25 | Helm Chart Structure (Chart.yaml, values.yaml, templates/) |
| 6.26 | Template Syntax and Go Templating |
| 6.27 | Creating Your Own Helm Chart |
| 6.28 | Chart Dependencies and Repositories |
| 6.29 | Helm Hooks and Testing |

### Hands-on Tasks
- [ ] একটা application deploy করো ConfigMap + Secret ব্যবহার করে, AWS Secrets Manager-এর সাথে integrate করো External Secrets Operator দিয়ে
- [ ] PostgreSQL StatefulSet deploy করো PersistentVolume সহ, pod delete-এর পরেও data persist হচ্ছে verify করো
- [ ] Nginx Ingress Controller install করো, ৩টা different domains-এ ৩টা services route করো
- [ ] cert-manager দিয়ে Let's Encrypt SSL certificates automatic manage করো
- [ ] HPA setup করো একটা deployment-এ — load test চালিয়ে pods auto-scale হচ্ছে verify করো
- [ ] একটা custom Helm chart বানাও তোমার previous web app-এর জন্য, values.yaml দিয়ে customizable করো

### Resources
- **Helm:** [Helm Official Documentation](https://helm.sh/docs/)
- **Ingress:** [Nginx Ingress Controller Docs](https://kubernetes.github.io/ingress-nginx/)
- **cert-manager:** [cert-manager Tutorial](https://cert-manager.io/docs/tutorials/)
- **Interactive:** [Katacoda Kubernetes Scenarios](https://killercoda.com/kubernetes)
- **Book (advanced):** "Kubernetes in Action" by Marko Lukša (highly recommended)

### Week 6 Checkpoint
**Deliverable:** GitHub repo `kubernetes-production-patterns` যেখানে একটা multi-service application থাকবে (frontend + backend + database) full production setup সহ — Ingress, SSL, HPA, Secrets, Persistent storage। সাথে একটা custom Helm chart যেটা same application deploy করে।


## 🗓️ Week 7: CI/CD — GitHub Actions + Jenkins

**Focus:** Automated build, test, এবং deployment pipelines

### 🎯 Learning Objectives
- Continuous Integration এবং Continuous Delivery/Deployment-এর difference বুঝতে পারবে
- GitHub Actions দিয়ে complete CI/CD pipelines design করতে পারবে
- Jenkins-এ declarative pipelines লিখতে পারবে
- Secrets এবং credentials securely manage করতে পারবে pipelines-এ
- Deployment strategies (blue-green, canary, rolling) implement করতে পারবে

### Lecture Topics

**Part A: CI/CD Fundamentals**

| # | Lecture Title |
|---|---------------|
| 7.1 | CI vs CD vs CD (Continuous Delivery vs Continuous Deployment) |
| 7.2 | Why CI/CD? Problems It Solves |
| 7.3 | Anatomy of a CI/CD Pipeline |
| 7.4 | Trunk-based Development vs GitFlow |

**Part B: GitHub Actions (Primary Focus)**

| # | Lecture Title |
|---|---------------|
| 7.5 | GitHub Actions Architecture |
| 7.6 | Workflows, Jobs, Steps, Actions — The Hierarchy |
| 7.7 | Workflow Triggers (push, pull_request, schedule, workflow_dispatch) |
| 7.8 | Runners (GitHub-hosted vs Self-hosted) |
| 7.9 | Marketplace Actions and Their Security Implications |
| 7.10 | Secrets and Environment Variables |
| 7.11 | Matrix Builds for Multiple Versions/OSs |
| 7.12 | Artifacts and Caching |
| 7.13 | Reusable Workflows |
| 7.14 | Composite Actions |
| 7.15 | OIDC Authentication with AWS (No More Access Keys!) |
| 7.16 | Building and Pushing Docker Images to ECR |
| 7.17 | Deploying to Kubernetes from GitHub Actions |
| 7.18 | Pull Request Workflows (Testing, Linting, Preview Deployments) |

**Part C: Jenkins**

| # | Lecture Title |
|---|---------------|
| 7.19 | Why Jenkins Still Matters (Enterprise Reality) |
| 7.20 | Jenkins Architecture (Master-Agent) |
| 7.21 | Installing Jenkins on Kubernetes with Helm |
| 7.22 | Plugins and Their Importance |
| 7.23 | Declarative vs Scripted Pipelines |
| 7.24 | Jenkinsfile Syntax |
| 7.25 | Parameterized Builds |
| 7.26 | Shared Libraries for DRY Pipelines |
| 7.27 | Jenkins vs GitHub Actions — When to Use What |

**Part D: Deployment Strategies**

| # | Lecture Title |
|---|---------------|
| 7.28 | Rolling Deployment |
| 7.29 | Blue-Green Deployment |
| 7.30 | Canary Deployment |
| 7.31 | Feature Flags and Progressive Delivery |

### Hands-on Tasks
- [ ] Complete GitHub Actions pipeline বানাও — lint → test → build → push to ECR → deploy to EKS
- [ ] OIDC authentication setup করো GitHub Actions থেকে AWS-এ (no hardcoded credentials)
- [ ] Matrix build setup করো Node.js application-এ (test on Node 18, 20, 22)
- [ ] Pull request preview deployment system বানাও
- [ ] Jenkins install করো Kubernetes cluster-এ Helm দিয়ে
- [ ] Jenkinsfile লিখো parameterized pipeline সহ
- [ ] Blue-green deployment implement করো Kubernetes-এ (manual switch)

### Resources
- **GitHub Actions:** [GitHub Actions Official Docs](https://docs.github.com/en/actions)
- **YouTube:** "GitHub Actions Tutorial" by TechWorld with Nana
- **Jenkins:** [Jenkins Handbook](https://www.jenkins.io/doc/book/) (free, comprehensive)
- **Hands-on:** [GitHub Skills](https://skills.github.com/)

### Week 7 Checkpoint
**Deliverable:** একটা real-world project (তোমার Week 6-এর multi-service app) এর জন্য production-grade CI/CD pipeline লিখো। GitHub repo-তে `.github/workflows/` folder-এ ৩টা workflows থাকবে — `ci.yml` (test on PR), `build.yml` (image build on merge), `deploy.yml` (deploy to EKS on tag)। Blog post লিখো "Zero to Production CI/CD with GitHub Actions"।


## 🗓️ Week 8: GitOps + Managed Kubernetes (Amazon EKS)

**Focus:** Cloud-native deployment patterns এবং production Kubernetes on AWS

### 🎯 Learning Objectives
- GitOps philosophy এবং কেন এটা traditional CD-এর থেকে superior সেটা বুঝতে পারবে
- ArgoCD দিয়ে declarative continuous deployment setup করতে পারবে
- Amazon EKS cluster তৈরি এবং manage করতে পারবে production-grade configuration-এ
- EKS-specific features (IRSA, VPC CNI, Fargate) use করতে পারবে

### Lecture Topics

**Part A: GitOps**

| # | Lecture Title |
|---|---------------|
| 8.1 | What is GitOps? Core Principles |
| 8.2 | Push vs Pull Deployment Models |
| 8.3 | Why GitOps is More Secure |
| 8.4 | ArgoCD Introduction and Installation |
| 8.5 | Application, Project, and Repository Concepts |
| 8.6 | Sync Strategies (Manual, Auto, Auto-Prune, Self-Heal) |
| 8.7 | App of Apps Pattern |
| 8.8 | ApplicationSets for Multi-Environment |
| 8.9 | ArgoCD Rollouts (Blue-Green, Canary via Argo Rollouts) |
| 8.10 | Flux CD Overview and Comparison |
| 8.11 | Secrets in GitOps (Sealed Secrets, SOPS, External Secrets) |

**Part B: Amazon EKS Deep Dive**

| # | Lecture Title |
|---|---------------|
| 8.12 | Why Managed Kubernetes? EKS vs Self-Managed |
| 8.13 | EKS Architecture (Control Plane Managed by AWS) |
| 8.14 | Creating EKS Cluster Methods (eksctl, Terraform, Console) |
| 8.15 | EKS Node Groups (Managed, Self-Managed, Fargate) |
| 8.16 | IAM Roles for Service Accounts (IRSA) — AWS Best Practice |
| 8.17 | AWS Load Balancer Controller for ALB/NLB |
| 8.18 | EBS CSI Driver for Persistent Storage |
| 8.19 | EFS CSI Driver for Shared Storage |
| 8.20 | VPC CNI — Pod Networking in EKS |
| 8.21 | Cluster Autoscaler vs Karpenter |
| 8.22 | Karpenter — Modern Node Provisioner |
| 8.23 | EKS Add-ons Management |
| 8.24 | EKS Security Best Practices |
| 8.25 | EKS Cost Optimization Strategies |
| 8.26 | Upgrading EKS Cluster Safely |

### Hands-on Tasks
- [ ] Terraform দিয়ে production-grade EKS cluster provision করো (VPC, node groups, IRSA setup সহ)
- [ ] AWS Load Balancer Controller install করো, ALB-based Ingress setup করো
- [ ] ArgoCD install করো EKS cluster-এ, তোমার application Git-based deploy করো
- [ ] App-of-apps pattern implement করো multi-environment setup-এর জন্য
- [ ] Karpenter install করো Cluster Autoscaler-এর পরিবর্তে
- [ ] External Secrets Operator setup করো AWS Secrets Manager-এর সাথে
- [ ] একটা application deploy করো যেটা সম্পূর্ণভাবে GitOps workflow follow করে

### Resources
- **ArgoCD:** [Argo CD Documentation](https://argo-cd.readthedocs.io/)
- **EKS:** [EKS Workshop](https://www.eksworkshop.com/) (HANDS-ON MUST-DO, free)
- **YouTube:** "GitOps with ArgoCD" by TechWorld with Nana, Viktor Farcic's DevOps Toolkit
- **Terraform EKS:** [terraform-aws-modules/eks](https://github.com/terraform-aws-modules/terraform-aws-eks)

### Week 8 Checkpoint
**Deliverable:** একটা complete production setup GitHub-এ। Repo structure: `infrastructure/` (Terraform for EKS), `apps/` (Kubernetes manifests/Helm charts), `argocd/` (ArgoCD applications)। ArgoCD dashboard screenshot যেখানে সব apps healthy এবং synced। Blog post লিখো "From Zero to GitOps: My EKS Journey"।


# MONTH 3: OBSERVABILITY + CAPSTONE PROJECT + INTERVIEW PREP

শেষ মাস — সবকিছু একসাথে জুড়ে production-grade system বানাবে, এবং mid-level role-এর জন্য ready হবে।


## 🗓️ Week 9: Monitoring Stack — Prometheus + Grafana

**Focus:** Metrics-based monitoring এবং alerting

### 🎯 Learning Objectives
- Observability-এর 3 pillars (Metrics, Logs, Traces) বুঝতে পারবে
- Prometheus-এর architecture এবং data model master করতে পারবে
- PromQL দিয়ে meaningful queries লিখতে পারবে
- Grafana-তে production-grade dashboards design করতে পারবে
- Alertmanager দিয়ে intelligent alerting setup করতে পারবে

### Lecture Topics

| # | Lecture Title |
|---|---------------|
| 9.1 | Monitoring vs Observability — Clear Distinction |
| 9.2 | The Three Pillars — Metrics, Logs, Traces |
| 9.3 | Four Golden Signals (Latency, Traffic, Errors, Saturation) |
| 9.4 | USE and RED Methods |
| 9.5 | Prometheus Architecture |
| 9.6 | Time-Series Data Model |
| 9.7 | Installing Prometheus on Kubernetes (kube-prometheus-stack) |
| 9.8 | Prometheus Configuration Deep Dive |
| 9.9 | Service Discovery (Kubernetes, EC2, File-based) |
| 9.10 | ServiceMonitor and PodMonitor (Prometheus Operator) |
| 9.11 | PromQL Fundamentals (instant vectors, range vectors) |
| 9.12 | PromQL Advanced (rate, irate, increase, histogram_quantile) |
| 9.13 | Recording Rules for Performance |
| 9.14 | Alerting Rules — Writing Effective Alerts |
| 9.15 | Alertmanager Configuration |
| 9.16 | Alert Routing, Grouping, Inhibition, Silencing |
| 9.17 | Integrating Slack, Email, PagerDuty |
| 9.18 | Exporters Deep Dive (node_exporter, blackbox_exporter, kube-state-metrics) |
| 9.19 | Custom Metrics from Your Application (client libraries) |
| 9.20 | Grafana Installation and Data Sources |
| 9.21 | Building Custom Dashboards |
| 9.22 | Variables and Templating in Grafana |
| 9.23 | Dashboards as Code (Grafonnet, Terraform) |
| 9.24 | SLI, SLO, SLA — Defining Reliability |
| 9.25 | Error Budgets and Burn Rate Alerts |

### Hands-on Tasks
- [ ] kube-prometheus-stack install করো Helm দিয়ে তোমার EKS cluster-এ
- [ ] Custom application metrics expose করো Prometheus client library দিয়ে (Node.js বা Python)
- [ ] ১০টা meaningful PromQL queries লিখে practice করো
- [ ] ৫টা production-grade dashboards build করো Grafana-তে — cluster overview, node metrics, application metrics, API performance, business metrics
- [ ] ১০টা alerting rules লিখো proper severity labels সহ
- [ ] Alertmanager configure করো Slack integration দিয়ে
- [ ] SLO define করো একটা service-এর জন্য (e.g., "99.5% requests under 200ms")

### Resources
- **YouTube:** "Prometheus Monitoring // Kubernetes Tutorial" by TechWorld with Nana
- **Course:** [Prometheus Certified Associate (PCA) study materials](https://training.linuxfoundation.org/certification/prometheus-certified-associate/)
- **PromQL:** [Awesome Prometheus Alerts](https://samber.github.io/awesome-prometheus-alerts/) (copy-paste ready alerts)
- **Grafana:** [Grafana Official Tutorials](https://grafana.com/tutorials/)
- **Dashboards:** [Grafana Dashboard Library](https://grafana.com/grafana/dashboards/) (free dashboards for common services)

### Week 9 Checkpoint
**Deliverable:** Live Grafana dashboard publicly accessible (behind auth), showing metrics from an actual running application on your EKS cluster. Alerting rules GitHub-এ stored। Blog post লিখো "Production Monitoring in Kubernetes: Prometheus + Grafana Setup Guide"।


## 🗓️ Week 10: Logging Stack + Distributed Tracing

**Focus:** Centralized logging এবং distributed tracing — production debugging-এর জন্য essential

### 🎯 Learning Objectives
- Centralized logging-এর importance বুঝতে পারবে এবং ELK/EFK/Loki-এর মধ্যে choice করতে পারবে
- Structured logging implement করতে পারবে applications-এ
- Distributed tracing concepts বুঝতে পারবে এবং OpenTelemetry implement করতে পারবে
- Metrics, logs, এবং traces correlate করতে পারবে incident investigation-এর সময়

### Lecture Topics

**Part A: Centralized Logging**

| # | Lecture Title |
|---|---------------|
| 10.1 | Why Centralized Logging in Distributed Systems |
| 10.2 | ELK Stack (Elasticsearch, Logstash, Kibana) Overview |
| 10.3 | EFK Stack (Fluentd replaces Logstash) — Kubernetes Preferred |
| 10.4 | Loki + Promtail — Grafana's Log Stack |
| 10.5 | ELK vs EFK vs Loki — Cost and Complexity Trade-offs |
| 10.6 | Installing EFK Stack on Kubernetes |
| 10.7 | Installing Loki + Promtail |
| 10.8 | Elasticsearch Basics (Indices, Mappings, Queries) |
| 10.9 | Logstash Pipelines and Grok Patterns |
| 10.10 | Fluentd vs Fluent Bit — When to Use What |
| 10.11 | Kibana Dashboards and Lens |
| 10.12 | LogQL for Loki (similar to PromQL) |
| 10.13 | Structured Logging Best Practices (JSON logs) |
| 10.14 | Log Levels and When to Use Each |
| 10.15 | Log Retention, Rotation, and Cost Management |
| 10.16 | AWS CloudWatch Logs Integration |
| 10.17 | Parsing Unstructured Logs |

**Part B: Distributed Tracing**

| # | Lecture Title |
|---|---------------|
| 10.18 | What is Distributed Tracing? Why It Matters |
| 10.19 | Traces, Spans, and Context Propagation |
| 10.20 | OpenTelemetry — The Standard |
| 10.21 | Jaeger Architecture and Installation |
| 10.22 | Grafana Tempo — Cost-Efficient Alternative |
| 10.23 | Instrumenting Applications (Auto vs Manual) |
| 10.24 | Correlating Traces with Logs and Metrics |
| 10.25 | AWS X-Ray Integration |

**Part C: Full Observability**

| # | Lecture Title |
|---|---------------|
| 10.26 | Building Observability Culture |
| 10.27 | Incident Response Workflow |
| 10.28 | Post-mortems and Blameless Culture |
| 10.29 | Chaos Engineering Introduction |

### Hands-on Tasks
- [ ] Loki + Promtail install করো তোমার EKS cluster-এ
- [ ] Application-এ structured JSON logging implement করো (trace IDs সহ)
- [ ] Kibana বা Grafana-তে log dashboards build করো
- [ ] OpenTelemetry SDK integrate করো একটা multi-service application-এ
- [ ] Jaeger UI-তে distributed traces visualize করো
- [ ] একটা end-to-end scenario debug করো — user request থেকে database query পর্যন্ত trace করো
- [ ] একটা intentional failure inject করো এবং logs + metrics + traces দিয়ে root cause analysis করো

### Resources
- **YouTube:** "Logging in Kubernetes with Loki" by DevOps Toolkit
- **OpenTelemetry:** [OpenTelemetry Official Docs](https://opentelemetry.io/docs/)
- **Book:** "Observability Engineering" by Charity Majors (highly recommended)
- **Practice:** [Open Observability Workshop](https://github.com/grafana/intro-to-mltp)

### Week 10 Checkpoint
**Deliverable:** Complete observability stack deployed। একটা "incident investigation" blog post লিখো যেখানে simulated failure describe করবে এবং কীভাবে metrics + logs + traces use করে root cause find করেছো সেটা step-by-step দেখাবে। Screen recording (5-10 min) YouTube-এ upload করো।


## 🗓️ Week 11: Capstone Project — Production Microservices Platform

**Focus:** সব skills একসাথে জুড়ে একটা real-world production-grade system build করা

### 🎯 Project Overview

**Project Name:** `cloud-native-microservices-platform`

একটা e-commerce বা similar real application deploy করবে যেটাতে থাকবে:

- ✅ Multiple microservices (minimum 3: e.g., User Service, Product Service, Order Service)
- ✅ API Gateway / Ingress
- ✅ Database (RDS PostgreSQL)
- ✅ Cache layer (Redis/ElastiCache)
- ✅ Message queue (SQS বা RabbitMQ)
- ✅ Complete CI/CD (GitHub Actions → ECR → EKS via ArgoCD)
- ✅ Monitoring (Prometheus + Grafana)
- ✅ Logging (Loki)
- ✅ Tracing (Jaeger/Tempo)
- ✅ Alerting (Alertmanager + Slack)
- ✅ All infrastructure as Terraform
- ✅ HTTPS with Let's Encrypt via cert-manager
- ✅ Auto-scaling (HPA)
- ✅ Secrets properly managed (AWS Secrets Manager + External Secrets Operator)

### Architecture

```
Internet
   ↓
Route 53 → CloudFront → ALB (via AWS Load Balancer Controller)
                         ↓
                    Nginx Ingress Controller
                         ↓
            ┌────────────┼────────────┐
            ↓            ↓            ↓
      User Service  Product Svc  Order Service
            │            │            │
            └────────────┼────────────┘
                         ↓
                RDS PostgreSQL (Multi-AZ)
                ElastiCache Redis
                SQS Queue

Monitoring Flow:
All Services → Prometheus → Grafana (dashboards)
All Services → Promtail → Loki → Grafana (logs)
All Services → OpenTelemetry → Tempo → Grafana (traces)
```

### 🗓️ 7-Day Execution Plan

| Day | Task |
|-----|------|
| **Day 1** | Project structure setup, microservices code (boilerplate), local Docker Compose test |
| **Day 2** | Terraform for infrastructure (VPC, EKS, RDS, ElastiCache, ECR repos) |
| **Day 3** | Helm charts for each microservice, local Kubernetes test (kind) |
| **Day 4** | CI/CD pipelines (GitHub Actions) — build, test, push to ECR |
| **Day 5** | ArgoCD setup, GitOps deployment to EKS, Ingress + SSL configuration |
| **Day 6** | Observability stack — Prometheus, Grafana, Loki, Tempo integration |
| **Day 7** | Load testing, alerting setup, documentation, demo video recording |

### 📝 Deliverables

- ✅ Live production URL (subdomain-এ hosted)
- ✅ GitHub repo with complete code (minimum 3 separate repos: `infrastructure`, `applications`, `k8s-manifests`)
- ✅ Comprehensive README explaining architecture, setup, and design decisions
- ✅ Architecture diagram (high-resolution)
- ✅ Grafana dashboard screenshots
- ✅ 10-minute demo video on YouTube showing:
  - Application working
  - Making a change via Git → automatic deployment via ArgoCD
  - Monitoring dashboards
  - Simulated failure and recovery
- ✅ Detailed blog post (Medium/Dev.to) covering the journey
- ✅ Post-mortem document: "Challenges I faced and how I solved them"

### Pro Tips
- ছোট শুরু করো — 1টা microservice দিয়ে শুরু, তারপর grow করো
- প্রতিদিনের progress commit করো with meaningful messages
- Free tier limits monitor করো — EKS itself costs ~$72/month
- Project শেষে resources terminate করো (বিশেষত EKS, NAT Gateway), screenshots আর code থেকে guide-এ যথেষ্ট

### 🎯 Why This Project Matters for Employers

এই একটা project তোমার:
- Cloud architecture skills prove করে
- IaC proficiency দেখায়
- Kubernetes mastery show করে
- CI/CD experience establish করে
- Observability knowledge demonstrate করে
- Production thinking reflect করে

**Interview-এ এই ১টা project সবচেয়ে বড় talking point হবে।**


## 🗓️ Week 12: Mid-Level Interview Preparation + Career Advancement

**Focus:** Mid-level positions-এর জন্য interview-ready হওয়া এবং strategic job hunting

### 🎯 Learning Objectives
- Mid-level technical interview-এর common patterns বুঝতে পারবে
- System design interviews basic level confidently handle করতে পারবে
- Troubleshooting/debugging scenarios explain করতে পারবে practically
- Salary negotiation এবং offer evaluation effectively করতে পারবে
- Long-term career planning করতে পারবে

### Topics to Master

**Part A: Technical Interview Preparation**

| # | Topic |
|---|-------|
| 12.1 | Common Mid-Level DevOps Interview Questions (Top 100) |
| 12.2 | Kubernetes Troubleshooting Scenarios (pod stuck in Pending, CrashLoopBackOff, OOMKilled) |
| 12.3 | Production Incident Walkthrough Examples |
| 12.4 | Terraform Interview Questions (state, modules, drift) |
| 12.5 | AWS Architecture Questions (design a scalable system) |
| 12.6 | CI/CD Pipeline Design Questions |
| 12.7 | Networking Deep-Dive Questions (VPC, DNS, Load Balancer internals) |
| 12.8 | Security Scenario Questions (IAM, secrets, compliance) |

**Part B: System Design for DevOps**

| # | Topic |
|---|-------|
| 12.9 | System Design Interview Framework |
| 12.10 | Design a CI/CD Pipeline for 100 Microservices |
| 12.11 | Design a Logging System for a Large Organization |
| 12.12 | Design a Multi-Region Deployment Strategy |
| 12.13 | Design an Auto-Scaling Architecture |
| 12.14 | Design a Disaster Recovery Plan |
| 12.15 | Capacity Planning and Cost Estimation |

**Part C: Behavioral + Communication**

| # | Topic |
|---|-------|
| 12.16 | STAR Method for Advanced Stories (production incidents, team conflicts) |
| 12.17 | "Tell me about a time you broke production" — Answering Well |
| 12.18 | Discussing Trade-offs (technical decisions you made) |
| 12.19 | Explaining Complex Technical Concepts Simply |
| 12.20 | Asking Good Questions to Interviewers |

**Part D: Career Strategy**

| # | Topic |
|---|-------|
| 12.21 | Resume Update for Mid-Level (Quantify Impact) |
| 12.22 | LinkedIn Optimization for Recruiter Outreach |
| 12.23 | Networking and Personal Brand Building |
| 12.24 | Choosing Between Offers — Beyond Salary |
| 12.25 | Salary Negotiation Tactics (The Levels Framework) |
| 12.26 | Remote vs Hybrid vs On-Site Trade-offs |
| 12.27 | Contract vs Full-Time Considerations |
| 12.28 | When to Specialize (DevOps vs SRE vs Platform vs Cloud Architect) |

### Week 12 Action Items

- [ ] Resume সম্পূর্ণ rewrite করো mid-level focus-এ (projects quantify করে — "reduced deployment time by 70%", "saved $X/month on cloud costs" ইত্যাদি)
- [ ] LinkedIn profile update করো, relevant keywords inject করো
- [ ] ১০০টি mid-level DevOps interview questions-এর answer লিখো এবং practice করো
- [ ] ৫টা mock system design interviews করো (Pramp, Interviewing.io)
- [ ] ১০টা behavioral stories prepare করো STAR format-এ (must include: production incident, team conflict, tough technical decision, mentoring, dealing with ambiguity)
- [ ] Previous projects-এর code review করো — interview-এ explain করতে ready হও
- [ ] Salary research করো (levels.fyi, Glassdoor) তোমার region-এর জন্য
- [ ] ৩০+ mid-level positions-এ apply করো
- [ ] ৫-১০ জন recruiters-এর সাথে connect করো LinkedIn-এ

### Resources

- **System Design:** [System Design Interview by Alex Xu](https://bytebytego.com/), [ByteByteGo YouTube](https://www.youtube.com/c/ByteByteGo)
- **DevOps Interview:** [DevOps Interview Questions GitHub](https://github.com/bregman-arie/devops-exercises) (highly comprehensive)
- **Kubernetes Troubleshooting:** [Learnk8s Troubleshooting Flowchart](https://learnk8s.io/troubleshooting-deployments)
- **Salary Data:** [levels.fyi](https://www.levels.fyi/), [Glassdoor](https://www.glassdoor.com/)
- **Negotiation:** [Haseeb Qureshi's Negotiation Guide](https://haseebq.com/how-not-to-bomb-your-offer-negotiation/)

### Week 12 + Syllabus 2 Final Outcomes

এই ১২ সপ্তাহ শেষে তোমার থাকবে:

| Asset | Status |
|-------|--------|
| Terraform expertise (reusable modules, remote state, multi-env) | ✅ |
| Docker mastery (production Dockerfiles, registry) | ✅ |
| Kubernetes production experience (EKS, Helm, RBAC, HPA) | ✅ |
| CI/CD pipelines (GitHub Actions + Jenkins exposure) | ✅ |
| GitOps workflow (ArgoCD) | ✅ |
| Full observability stack (Prometheus, Grafana, Loki, Tempo) | ✅ |
| Major capstone project (production microservices platform) | ✅ |
| 4-5 substantial blog posts on your learning journey | ✅ |
| Updated resume, LinkedIn, GitHub | ✅ |
| Applied to 30+ mid-level positions | ✅ |


## 🎯 Syllabus 2 Final Assessment Checklist

তুমি ready for mid-level role যদি প্রত্যেকটায় "Yes" বলতে পারো:

- [ ] Greenfield project-এ scratch থেকে complete infrastructure Terraform দিয়ে build করতে পারো?
- [ ] Kubernetes-এ pod-level থেকে cluster-level পর্যন্ত troubleshoot করতে পারো?
- [ ] Production CI/CD pipeline design এবং implement করতে পারো security best practices সহ?
- [ ] একটা system down হলে metrics + logs + traces use করে systematically root cause খুঁজতে পারো?
- [ ] "Why Kubernetes over ECS?" বা "When to use Helm vs Kustomize?" type questions-এর thoughtful answer দিতে পারো?
- [ ] Helm chart বানিয়ে একটা complex application packaging করতে পারো?
- [ ] GitOps workflow explain এবং implement করতে পারো ArgoCD দিয়ে?
- [ ] SLI/SLO define করতে পারো একটা service-এর জন্য?
- [ ] Cost optimization-এর concrete examples দিতে পারো?
- [ ] Incident response workflow describe করতে পারো তোমার own experience থেকে?
- [ ] অন্তত ৪টা production-grade projects GitHub-এ show করতে পারো?

যদি ৯+ "Yes" হয় → **Syllabus 3 শুরু করার time!**


## 🚨 Important Notes

### What NOT to Do

- ❌ সব tool-এ shallow knowledge-এ satisfied হয়ো না — অন্তত ২-৩টায় deep expertise গড়ো
- ❌ "I can set up EKS" বলো না unless তুমি troubleshoot করতে পারো when things break
- ❌ ArgoCD install করেই GitOps expert claim করো না — real challenges (secret management, multi-env, rollback strategies) solve করতে পারতে হবে
- ❌ Capstone project rush করো না Week 11-এ — quality matters more than timeline

### What TO Do

- ✅ Deliberately break things in test environments এবং fix করো — এটাই শেখার fastest way
- ✅ Open source contribute করো — Kubernetes, Terraform providers, Helm charts-এর issues-এ কাজ করো
- ✅ AWS Well-Architected Framework study করো — interview-এ impressive sounding
- ✅ Kubecon/HashiConf/AWS re:Invent talks দেখো YouTube-এ — industry trends সম্পর্কে up-to-date থাকো
- ✅ DevOps community-এ join করো — r/devops, r/kubernetes, CNCF Slack, HashiCorp community


## Estimated Costs for Syllabus 2

| Item | Cost |
|------|------|
| AWS EKS cluster (running during active learning, terminate when not) | **$50–$100** |
| AWS other resources (NAT Gateway, RDS, ALB, etc.) | **$30–$60** |
| Domain name + Route 53 | **$15–$20** |
| Udemy courses (optional, on sale) | **$30–$50** |
| Certification: CKA (Certified Kubernetes Administrator) — highly recommended | **$395** |
| Certification: Terraform Associate — recommended | **$70.50** |
| **Total (without certs)** | **~$125–$230** |
| **Total (with both certs)** | **~$600–$695** |

### Cost Saving Tips
- EKS cluster শুধু actively learning করার সময় running রাখো (rest of the time: `terraform destroy`)
- Spot instances use করো node groups-এ (70-90% discount)
- AWS Activate credits apply করো (up to $1000 free credits for startups/students)
- Local Kubernetes (kind, minikube) যখনই possible ব্যবহার করো instead of EKS

## Recommended Certifications

| Certification | Priority | Value |
|---------------|----------|-------|
| **CKA (Certified Kubernetes Administrator)** | High | Industry gold standard for K8s |
| **HashiCorp Certified Terraform Associate** | High | Validates IaC skills |
| **AWS Solutions Architect Associate** (if skipped in Syllabus 1) | Medium | Still useful |
| **AWS DevOps Engineer Professional** | Medium-High | Advanced but valuable |
| **CKAD (Certified Kubernetes Application Developer)** | Medium | If more app-focused |

**My recommendation:** CKA + Terraform Associate = strongest signal for mid-level positions.


## After Syllabus 2

Next: **Syllabus 3 (Weeks 1-12)** — Senior Engineer / Specialist Track

Focus: Advanced Security (DevSecOps), Advanced Observability, Service Mesh, Cost Optimization (FinOps), Architecture & System Design, Specialization (SRE / Platform / Security / Multi-cloud Architect)

## 📊 Where You Stand After Syllabus 2

| Experience Equivalent | Real-world Capability |
|-----------------------|----------------------|
| ~2 years of hands-on experience | Can independently manage production systems |
| Mid-level positions eligible | Cloud Engineer, DevOps Engineer, SRE (Junior) |
| Expected salary range (location-dependent) | Globally: $60K-$110K \| South Asia: ৳80K-৳250K/month |

তবে remember — **salary comes from impact, not syllabus completion**। যত প্রকৃত production experience গড়বে, তত salary বাড়বে।

---

**Made with ❤️ for your Cloud Engineering Journey**  
*Remember: Mid-level engineers solve problems. Senior engineers prevent problems. Keep climbing.*
