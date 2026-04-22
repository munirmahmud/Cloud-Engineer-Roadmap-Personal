# Syllabus 1: Junior Cloud/DevOps Engineer Roadmap
## 🎯 12-Week Beginner-to-Job-Ready Program (AWS Focus)

## 📋 Program Overview

| Field | Detail |
|-------|--------|
| **Target Roles** | Junior Cloud Engineer, Junior DevOps Engineer, Cloud Associate, Cloud Support Engineer |
| **Duration** | 3 Months (12 Weeks) |
| **Commitment** | 15–20 hours/week (2–3 hours daily) |
| **Prerequisite** | None — Complete beginner friendly |
| **Cloud Focus** | AWS (Amazon Web Services) |
| **Expected Outcome** | Job-ready for Junior Cloud/DevOps roles with portfolio + certification |

## High-Level Roadmap

```
Month 1: IT Foundations          Month 2: AWS Core Services       Month 3: Projects + Job Prep
├── Week 1: Linux Basics         ├── Week 5: AWS Foundations      ├── Week 9:  Capstone Project 1
├── Week 2: Bash Scripting       ├── Week 6: Compute + Storage    ├── Week 10: Capstone Project 2
├── Week 3: Networking           ├── Week 7: VPC + Databases      ├── Week 11: Certification Prep
└── Week 4: Git + Python         └── Week 8: Monitoring + Cost    └── Week 12: Interview + Jobs
```


# MONTH 1: IT FOUNDATIONS

ক্লাউড শেখার আগে IT fundamentals strong হতে হবে। বাড়ি বানাতে গেলে যেভাবে foundation লাগে, ঠিক তেমন।


## 🗓️ Week 1: Linux Fundamentals

**Focus:** Linux operating system basics — the backbone of every cloud workload

### 🎯 Learning Objectives
- Terminal দিয়ে Linux file system efficiently navigate করতে পারবে
- File permissions ও ownership manage করতে পারবে
- Software package install/update/remove করতে পারবে
- Basic system administration tasks করতে পারবে

### Lecture Topics

| # | Lecture Title |
|---|---------------|
| 1.1 | Introduction to Linux and Why It Matters in Cloud |
| 1.2 | Linux Distributions Overview (Ubuntu, CentOS, Amazon Linux, Debian) |
| 1.3 | Setting Up Linux Environment (VirtualBox / WSL2 / AWS Cloud Shell) |
| 1.4 | Terminal and Shell Basics (Bash Introduction) |
| 1.5 | Linux File System Hierarchy (/etc, /home, /var, /opt, /tmp) |
| 1.6 | Essential Navigation Commands (ls, cd, pwd, tree) |
| 1.7 | File Operations (mkdir, cp, mv, rm, touch) |
| 1.8 | Viewing File Contents (cat, less, more, head, tail) |
| 1.9 | File Search (find, locate, which, whereis) |
| 1.10 | Understanding File Permissions (rwx, octal notation) |
| 1.11 | Permission Management (chmod, chown, chgrp) |
| 1.12 | User and Group Management (useradd, usermod, groupadd, sudo) |
| 1.13 | Package Management on Debian/Ubuntu (apt, dpkg) |
| 1.14 | Package Management on RHEL/CentOS (yum, dnf, rpm) |

### Hands-on Tasks
- [ ] VirtualBox-এ Ubuntu 22.04 install করো (or WSL2 on Windows)
- [ ] ৫০+ commands practice করো cheat sheet বানাতে বানাতে
- [ ] ৩ জন new user create করো different permissions সহ
- [ ] Nginx install করে browser থেকে access করো
- [ ] `/var/log/` directory explore করে system logs analyze করো

### Resources
- **Free:** [Linux Journey](https://linuxjourney.com/), [freeCodeCamp - Linux for Hackers](https://www.youtube.com/watch?v=sWbUDq4S6Y8)
- **YouTube:** NetworkChuck's "Linux for Beginners", TechWorld with Nana's Linux tutorial
- **Official Docs:** [Ubuntu Documentation](https://ubuntu.com/tutorials)
- **Book (optional):** "The Linux Command Line" by William Shotts (Free PDF)

### Week 1 Checkpoint
**Deliverable:** GitHub-এ একটা repo বানাও `linux-week-1` name দিয়ে, একটা `NOTES.md` file-এ top 50 commands cheat sheet লিখে commit করো। + একটা 5-minute screen recording বানাও YouTube-এ (unlisted) কীভাবে তুমি file permissions manage করছো।


## 🗓️ Week 2: Linux Advanced + Bash Scripting

**Focus:** Automation এর প্রথম step — Bash scripting দিয়ে repetitive কাজ automate করা

### 🎯 Learning Objectives
- Processes manage করতে পারবে (start, stop, monitor, kill)
- System logs ও resources monitor করতে পারবে
- Functional Bash scripts লিখতে পারবে
- Cron দিয়ে scheduled automation করতে পারবে

### Lecture Topics

| # | Lecture Title |
|---|---------------|
| 2.1 | Process Management (ps, top, htop, kill, nice) |
| 2.2 | Background vs Foreground Processes (&, jobs, fg, bg) |
| 2.3 | systemd and systemctl (service management) |
| 2.4 | Disk Management (df, du, lsblk, mount, umount) |
| 2.5 | Archive and Compression (tar, gzip, zip, unzip) |
| 2.6 | Text Processing I: grep and Regular Expressions |
| 2.7 | Text Processing II: sed (stream editor) |
| 2.8 | Text Processing III: awk basics |
| 2.9 | I/O Redirection and Pipes (\|, >, <, >>, 2>&1) |
| 2.10 | Bash Scripting Basics (shebang, variables, execution) |
| 2.11 | Conditional Statements (if, elif, else, case) |
| 2.12 | Loops (for, while, until) |
| 2.13 | Functions and Arguments ($1, $@, $?) |
| 2.14 | Error Handling and Exit Codes |
| 2.15 | Cron Jobs and Task Scheduling (crontab) |
| 2.16 | SSH Basics (ssh, scp, ssh-keygen, authorized_keys) |

### Hands-on Tasks
- [ ] একটা backup script লেখো যে specific directory `.tar.gz` বানাবে
- [ ] একটা monitoring script লেখো যে CPU 80%+ হলে alert দেবে
- [ ] SSH key-pair generate করে passwordless login setup করো
- [ ] Cron job setup করো প্রতেক দিন রাত ১২টায় auto backup নিতে
- [ ] Log parser script লেখো যে nginx access log থেকে top 10 IP বের করবে

### Resources
- **Free:** [LearnShell.org](https://www.learnshell.org/), [Bash Scripting Tutorial on YouTube by Joe Collins](https://www.youtube.com/watch?v=e7BufAVwDiM)
- **YouTube:** NetworkChuck Bash series, ExplainingComputers
- **Docs:** [GNU Bash Manual](https://www.gnu.org/software/bash/manual/)
- **Practice:** [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) — fun way to master Linux

### Week 2 Checkpoint
**Deliverable:** GitHub repo `bash-automation-toolkit` বানাও, এতে ৫টা useful script থাকবে — `backup.sh`, `system-monitor.sh`, `log-analyzer.sh`, `user-onboarding.sh`, `disk-cleanup.sh`। Proper README লেখো কীভাবে use করতে হয়।


## 🗓️ Week 3: Networking Fundamentals

**Focus:** Network বুঝতে না পারলে cloud-এ trouble-shoot করা impossible

### 🎯 Learning Objectives
- OSI model ও TCP/IP stack বুঝতে পারবে
- IP addressing, subnetting, CIDR calculate করতে পারবে
- DNS, load balancing, firewall concepts explain করতে পারবে
- Basic network troubleshooting tools use করতে পারবে

### Lecture Topics

| # | Lecture Title |
|---|---------------|
| 3.1 | What is a Network? LAN, WAN, MAN Overview |
| 3.2 | OSI Model — 7 Layers Explained with Examples |
| 3.3 | TCP/IP Model and How It Maps to OSI |
| 3.4 | IP Addressing: IPv4 Structure and Classes |
| 3.5 | Public vs Private IP Addresses |
| 3.6 | Subnetting and CIDR Notation (The MOST Important Topic!) |
| 3.7 | IPv6 Basics and Why It Exists |
| 3.8 | TCP vs UDP Protocol Comparison |
| 3.9 | Common Ports and Protocols (80, 443, 22, 3306, etc.) |
| 3.10 | DNS — How Domain Names Resolve to IPs |
| 3.11 | DHCP — How Devices Get IP Addresses |
| 3.12 | HTTP/HTTPS Deep Dive |
| 3.13 | SSL/TLS and Symmetric vs Asymmetric Encryption |
| 3.14 | Firewalls, NAT, and Port Forwarding |
| 3.15 | Load Balancers: Layer 4 vs Layer 7 |
| 3.16 | Reverse Proxy vs Forward Proxy |
| 3.17 | Network Troubleshooting Tools (ping, traceroute, nslookup, dig, netstat, ss, tcpdump) |

### Hands-on Tasks
- [ ] ১০টা subnetting problem solve করো (pen-and-paper)
- [ ] Wireshark install করে HTTP request packet capture করো
- [ ] `dig` ও `nslookup` দিয়ে different DNS records check করো (A, MX, CNAME, TXT)
- [ ] `traceroute google.com` run করে প্রতেক hop explain করো
- [ ] iptables দিয়ে simple firewall rule create করো

### Resources
- **Free:** [Professor Messer Network+ Course](https://www.professormesser.com/network-plus/n10-008/n10-008-video/n10-008-training-course/) (GOLD STANDARD)
- **YouTube:** PowerCert Animated Videos (visual learners এর জন্য perfect), NetworkChuck
- **Subnetting Practice:** [subnettingquestions.com](https://www.subnettingquestions.com/)
- **Interactive:** [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer)

### Week 3 Checkpoint
**Deliverable:** একটা Medium/LinkedIn/Dev.to blog post লেখো "10 Networking Concepts Every Cloud Engineer Must Know" title-এ। Proper diagrams add করো (Excalidraw or draw.io use করো)। এইটা তোমার portfolio-র first public proof হবে।

## 🗓️ Week 4: Git, GitHub, and Python Basics

**Focus:** Version control (Git) + automation language (Python) — যেকোনো DevOps role এর must-have

### 🎯 Learning Objectives
- Git দিয়ে code version control করতে পারবে professionally
- GitHub-এ collaborate, pull request, code review করতে পারবে
- Python দিয়ে simple scripts ও AWS automation লিখতে পারবে
- Boto3 (AWS SDK for Python) দিয়ে programmatically AWS resource manage করতে পারবে

### Lecture Topics

**Part A: Git & GitHub (First Half)**

| # | Lecture Title |
|---|---------------|
| 4.1 | Version Control Concepts and Why Git |
| 4.2 | Installing and Configuring Git (git config) |
| 4.3 | Git Basics (init, add, commit, status, log) |
| 4.4 | Branching and Merging (branch, checkout, merge) |
| 4.5 | Resolving Merge Conflicts |
| 4.6 | Remote Repositories (remote, push, pull, fetch) |
| 4.7 | GitHub Workflow (Fork, Clone, PR, Code Review) |
| 4.8 | `.gitignore` and Best Practices |
| 4.9 | Git Tags and Releases |
| 4.10 | Advanced: Rebase, Cherry-pick, Stash |

**Part B: Python Basics (Second Half)**

| # | Lecture Title |
|---|---------------|
| 4.11 | Python Installation and Virtual Environments (venv, pip) |
| 4.12 | Variables, Data Types, and Operators |
| 4.13 | Control Flow (if/else, for, while) |
| 4.14 | Data Structures (list, tuple, dict, set) |
| 4.15 | Functions and Lambda Expressions |
| 4.16 | File I/O and Exception Handling |
| 4.17 | Modules, Packages, and pip |
| 4.18 | Working with JSON and YAML |
| 4.19 | Making HTTP Requests (requests library) |
| 4.20 | Introduction to Boto3 (AWS SDK) |

### Hands-on Tasks
- [ ] GitHub-এ professional profile বানাও (bio, pinned repos, README profile)
- [ ] ৫টা different repository বানাও different branches দিয়ে
- [ ] একটা open-source project-এ first PR contribute করো (documentation typo fix-ও adequate)
- [ ] Python script লেখো যে disk usage check করে alert দেবে
- [ ] Boto3 দিয়ে script লেখো যে all S3 buckets list করবে

### Resources
- **Git/GitHub:** [GitHub Skills](https://skills.github.com/), [Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials)
- **Python:** [Python for Everybody by Dr. Chuck](https://www.py4e.com/) (Free), [Automate the Boring Stuff](https://automatetheboringstuff.com/)
- **Boto3:** [AWS Boto3 Documentation](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
- **Interactive:** [Learn Git Branching](https://learngitbranching.js.org/) — visual + fun

### Week 4 Checkpoint
**Deliverable:** GitHub profile complete (pinned 4 repos, bio, README)। একটা Python project `aws-resource-checker` বানাও যে boto3 দিয়ে EC2, S3, RDS resources list করবে। Code-এ proper docstrings, error handling, README থাকবে।


# 📅 MONTH 2: AWS CORE SERVICES

এখন actual AWS-এ dive করবো। Free Tier account দিয়ে practical কাজ করতে হবে প্রতি week-এ।


## 🗓️ Week 5: AWS Foundations + IAM

**Focus:** AWS-এর global architecture বুঝতে হবে + security first approach শিখতে হবে

### 🎯 Learning Objectives
- AWS global infrastructure (Regions, AZs, Edge Locations) বুঝতে পারবে
- AWS CLI install করে configure করতে পারবে
- IAM users, groups, roles, policies properly setup করতে পারবে
- Least privilege principle follow করে secure environment build করতে পারবে

### Lecture Topics

| # | Lecture Title |
|---|---------------|
| 5.1 | Cloud Computing Fundamentals (IaaS, PaaS, SaaS) |
| 5.2 | Why AWS? Market Share and Service Overview |
| 5.3 | AWS Global Infrastructure (Regions, AZs, Edge Locations, Local Zones) |
| 5.4 | AWS Free Tier Explained — কোন service free, কোনটা নয় |
| 5.5 | Creating AWS Account Safely (Root vs IAM User) |
| 5.6 | AWS Billing Dashboard and Budget Alerts (IMPORTANT!) |
| 5.7 | AWS Console Tour and Navigation |
| 5.8 | AWS CLI Installation and Configuration (aws configure) |
| 5.9 | Understanding IAM — The Security Backbone |
| 5.10 | IAM Users, Groups, and Access Keys |
| 5.11 | IAM Policies (Managed, Custom, Inline) — JSON Structure |
| 5.12 | IAM Roles and When to Use Them |
| 5.13 | MFA (Multi-Factor Authentication) Setup |
| 5.14 | AWS CloudShell vs Local CLI |
| 5.15 | AWS Organizations Basics (Multi-Account Concept) |
| 5.16 | Shared Responsibility Model |

### Hands-on Tasks
- [ ] AWS Free Tier account create করো, root user-এ MFA enable করো
- [ ] Billing alert setup করো $5 threshold-এ (SURPRISE bill থেকে বাঁচবে!)
- [ ] IAM user create করো নিজের কাজের জন্য (root use NEVER করবে না)
- [ ] AdminGroup, DevGroup, ReadOnlyGroup — ৩টা group create করো different permissions দিয়ে
- [ ] EC2-read only IAM role create করো
- [ ] AWS CLI install করে `aws s3 ls` command run করো

### Resources
- **Free:** [AWS Cloud Practitioner Essentials (Official)](https://aws.amazon.com/training/learn-about/cloud-practitioner/) — FREE and official
- **YouTube:** Stephane Maarek's AWS channel, freeCodeCamp AWS Practitioner course
- **Docs:** [AWS IAM Documentation](https://docs.aws.amazon.com/iam/)
- **Hands-on:** [AWS Skill Builder](https://skillbuilder.aws/) — free labs

### Week 5 Checkpoint
**Deliverable:** Screenshot document (PDF) বানাও ১০ pages — তোমার IAM setup দেখিয়ে (users, groups, roles, policies, MFA enabled)। GitHub-এ একটা repo `aws-iam-lab` push করো যেতে IAM policy JSONs থাকবে।


## 🗓️ Week 6: AWS Compute (EC2) + Storage (S3, EBS)

**Focus:** AWS-এর দুইটা most-used services — EC2 (virtual servers) and S3 (object storage)

### 🎯 Learning Objectives
- EC2 instance launch, connect, manage করতে পারবে
- Proper security group configuration করতে পারবে
- S3 bucket বানাতে, files upload করতে, permissions set করতে পারবে
- EBS volumes attach, snapshot, backup করতে পারবে

### Lecture Topics

**Part A: EC2 (Elastic Compute Cloud)**

| # | Lecture Title |
|---|---------------|
| 6.1 | What is EC2 and Virtual Machines in Cloud |
| 6.2 | EC2 Instance Types (t2.micro, m5, c5, r5 — when to use what) |
| 6.3 | AMI (Amazon Machine Image) Deep Dive |
| 6.4 | Launching Your First EC2 Instance Step-by-Step |
| 6.5 | Key Pairs and SSH Access (.pem files) |
| 6.6 | Security Groups vs Network ACLs |
| 6.7 | Elastic IP Addresses |
| 6.8 | EC2 Instance States (running, stopped, terminated) |
| 6.9 | EC2 Pricing Models (On-Demand, Reserved, Spot, Savings Plans) |
| 6.10 | User Data Scripts for Auto-Configuration |

**Part B: Storage Services**

| # | Lecture Title |
|---|---------------|
| 6.11 | AWS Storage Types Overview (Object, Block, File) |
| 6.12 | S3 (Simple Storage Service) Deep Dive |
| 6.13 | S3 Storage Classes (Standard, IA, Glacier, Deep Archive) |
| 6.14 | S3 Bucket Policies and ACLs |
| 6.15 | S3 Versioning and Lifecycle Rules |
| 6.16 | S3 Static Website Hosting |
| 6.17 | EBS (Elastic Block Store) — Volumes and Snapshots |
| 6.18 | EBS Volume Types (gp3, io2, st1, sc1) |
| 6.19 | EFS (Elastic File System) Introduction |

### Hands-on Tasks
- [ ] t2.micro EC2 instance launch করো Amazon Linux 2 দিয়ে
- [ ] SSH দিয়ে connect করো, Nginx install করো, browser থেকে access করো
- [ ] User Data script দিয়ে EC2 launch time-এ auto-install করো Apache
- [ ] S3 bucket create করে static HTML website host করো
- [ ] S3 bucket-এ versioning enable করে file delete-এর পর restore করো
- [ ] EBS snapshot নাও, তার থেকে new volume create করে other AZ-এ attach করো
- [ ] একটা EC2 stop/start করলে IP change হয় vs Elastic IP use করলে হয় না — এইটা prove করো

### Resources
- **YouTube:** Stephane Maarek's EC2 section, TechWorld with Nana AWS series
- **Docs:** [EC2 User Guide](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/), [S3 User Guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/)
- **Labs:** [AWS Skill Builder EC2 Labs](https://skillbuilder.aws/)

### Week 6 Checkpoint
**Deliverable:** S3-এ hosted একটা portfolio website (custom HTML/CSS)। এইটা তোমার first cloud-hosted project — link টা resume-এ add করবে। EC2-এ একটা LAMP stack manually install করে screenshot proof দাও।


## 🗓️ Week 7: AWS Networking (VPC) + Databases

**Focus:** VPC — AWS-এর most confusing but most important service। + Managed databases।

### 🎯 Learning Objectives
- Custom VPC design ও implement করতে পারবে with public/private subnets
- Internet Gateway, NAT Gateway, Route Tables configure করতে পারবে
- RDS দিয়ে managed relational database launch করতে পারবে
- DynamoDB basics বুঝতে পারবে (NoSQL)

### Lecture Topics

**Part A: VPC (Virtual Private Cloud)**

| # | Lecture Title |
|---|---------------|
| 7.1 | Why VPC? Default VPC vs Custom VPC |
| 7.2 | VPC CIDR Blocks and IP Planning |
| 7.3 | Subnets — Public vs Private Explained |
| 7.4 | Internet Gateway (IGW) and Route Tables |
| 7.5 | NAT Gateway vs NAT Instance |
| 7.6 | Security Groups vs NACLs (Deep Comparison) |
| 7.7 | VPC Peering Basics |
| 7.8 | VPC Endpoints (Gateway vs Interface) |
| 7.9 | Elastic Load Balancer (ELB) Overview |
| 7.10 | ALB vs NLB vs CLB — When to Use What |
| 7.11 | Auto Scaling Groups (ASG) Basics |
| 7.12 | Route 53 — DNS Service Introduction |

**Part B: Databases on AWS**

| # | Lecture Title |
|---|---------------|
| 7.13 | RDS (Relational Database Service) Overview |
| 7.14 | Supported Engines (MySQL, PostgreSQL, MariaDB, Oracle, SQL Server) |
| 7.15 | RDS Multi-AZ vs Read Replicas |
| 7.16 | Automated Backups and Point-in-Time Recovery |
| 7.17 | DynamoDB Introduction (NoSQL Key-Value Store) |
| 7.18 | ElastiCache (Redis, Memcached) Overview |
| 7.19 | Database Security (Encryption, Parameter Groups, Security Groups) |

### Hands-on Tasks
- [ ] Custom VPC বানাও 10.0.0.0/16 CIDR-এ with ২ public + ২ private subnets (multi-AZ)
- [ ] IGW attach করো, route table configure করো, NAT Gateway setup করো
- [ ] Public subnet-এ একটা EC2 launch করো, private subnet-এ অন্য একটা — private থেকে internet access prove করো NAT দিয়ে
- [ ] Application Load Balancer setup করো ২টা EC2 এর সাথে, different AZ-এ
- [ ] Private subnet-এ RDS MySQL launch করো, EC2 থেকে connect করো
- [ ] DynamoDB table বানাও, items insert/query করো AWS CLI দিয়ে

### Resources
- **YouTube:** "AWS VPC Core Concepts" by Stephane Maarek, "VPC Peering" by Be A Better Dev
- **Docs:** [VPC User Guide](https://docs.aws.amazon.com/vpc/latest/userguide/), [RDS User Guide](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/)
- **Visual:** [VPC Builder Tool](https://aws.amazon.com/vpc/)

### Week 7 Checkpoint
**Deliverable:** VPC architecture diagram বানাও (draw.io/Excalidraw) showing 3-tier architecture (Public ALB → Private App Servers → Private RDS)। GitHub-এ push করো with detailed README explaining each component-এর purpose।

## 🗓️ Week 8: Monitoring, Cost Management & Other Essential AWS Services

**Focus:** Observability + cost optimization + other must-know services

### 🎯 Learning Objectives
- CloudWatch দিয়ে metrics, logs, alarms setup করতে পারবে
- CloudTrail দিয়ে audit trail বুঝতে পারবে
- AWS cost optimize করতে পারবে (very attractive skill for employers!)
- Lambda basics + other essential services overview

### Lecture Topics

**Part A: Monitoring & Logging**

| # | Lecture Title |
|---|---------------|
| 8.1 | CloudWatch — The Monitoring Swiss Army Knife |
| 8.2 | CloudWatch Metrics (Basic vs Detailed Monitoring) |
| 8.3 | CloudWatch Logs and Log Groups |
| 8.4 | CloudWatch Alarms and SNS Notifications |
| 8.5 | CloudWatch Dashboards |
| 8.6 | CloudTrail — Who Did What When in AWS |
| 8.7 | AWS Config Introduction |

**Part B: Serverless & Other Services**

| # | Lecture Title |
|---|---------------|
| 8.8 | Lambda — Serverless Compute Introduction |
| 8.9 | API Gateway Basics |
| 8.10 | SNS (Simple Notification Service) |
| 8.11 | SQS (Simple Queue Service) |
| 8.12 | Route 53 Deep Dive (Routing Policies) |
| 8.13 | CloudFront (CDN) Basics |
| 8.14 | Systems Manager (SSM) for Instance Management |

**Part C: Cost Management**

| # | Lecture Title |
|---|---------------|
| 8.15 | AWS Cost Explorer and Billing Dashboard |
| 8.16 | AWS Budgets and Anomaly Detection |
| 8.17 | Cost Optimization Strategies (Right-sizing, Reserved Instances, Spot) |
| 8.18 | Tagging Strategy for Cost Allocation |
| 8.19 | AWS Trusted Advisor |

### Hands-on Tasks
- [ ] EC2 instance-এ CloudWatch agent install করো ও custom metrics push করো
- [ ] CloudWatch alarm setup করো CPU > 70% হলে email alert পেতে
- [ ] Lambda function লেখো Python-এ যে S3-এ file upload হলে automatically resize করবে
- [ ] SNS topic create করে email subscription add করো, test message পাঠাও
- [ ] Cost Explorer explore করো, তোমার last-30-days spending analyze করো
- [ ] Tags add করো প্রতেক resource-এ: `Environment`, `Project`, `Owner`

### Resources
- **YouTube:** Be A Better Dev's CloudWatch series, Stephane Maarek's Lambda tutorial
- **Docs:** [CloudWatch User Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/), [Lambda Developer Guide](https://docs.aws.amazon.com/lambda/latest/dg/)
- **Cost:** [AWS Well-Architected — Cost Pillar](https://docs.aws.amazon.com/wellarchitected/latest/cost-optimization-pillar/welcome.html)

### Week 8 Checkpoint
**Deliverable:** Blog post লেখো "My First Month with AWS: 10 Services I Learned and 5 Mistakes I Made"। Social media (LinkedIn)-এ share করো — এইটা তোমার visibility boost করবে significantly। Recruiters এই post দেখে approach করতে পারে।


# 📅 MONTH 3: CAPSTONE PROJECTS + JOB PREP

Theoretical শেখার পর এখন production-style real project build করবে। **এইগুলাই তোমার interview-এ দেখানো হবে।**


## 🗓️ Week 9: Capstone Project 1 — Highly Available Static Website

**Focus:** End-to-end project: code → cloud → HTTPS → CDN

### 🎯 Project Architecture

```
Route 53 (DNS) → CloudFront (CDN + HTTPS) → S3 Bucket (Private, OAI) 
                                          ↓
                                    GitHub Actions (Auto-deploy)
```

### What You'll Build
একটা personal portfolio website host করবে যে:
1. S3-এ hosted (private bucket, OAI দিয়ে secured)
2. CloudFront দিয়ে globally cached + SSL
3. Custom domain Route 53 দিয়ে
4. GitHub Actions দিয়ে auto-deploy on push

### Step-by-Step Tasks
- [ ] **Day 1-2:** HTML/CSS portfolio template বানাও (TailwindCSS use করতে পারো)
- [ ] **Day 3:** S3 bucket create করো, static site enable করো
- [ ] **Day 4:** CloudFront distribution setup করো OAI দিয়ে (S3 directly public NA)
- [ ] **Day 5:** ACM থেকে SSL certificate নিয়ে CloudFront-এ attach করো
- [ ] **Day 6:** Domain name কিনো (Route 53 or external), Route 53 hosted zone setup করো
- [ ] **Day 7:** GitHub Actions workflow লেখো যে push হলে auto-sync করবে S3-এ

### Deliverables
- ✅ Live website URL
- ✅ GitHub repo with IaC (bonus: Terraform/CloudFormation version)
- ✅ Architecture diagram
- ✅ Detailed README with setup instructions
- ✅ Blog post explaining the architecture decisions


## 🗓️ Week 10: Capstone Project 2 — 3-Tier Web Application on AWS

**Focus:** Production-grade multi-tier application with HA + monitoring

### 🎯 Project Architecture

```
Internet → Route 53 → ALB (Public Subnet) 
                      ↓
                 Auto Scaling Group (Private Subnet) — EC2 instances running app
                      ↓
                 RDS Multi-AZ MySQL (Private Subnet)

+ CloudWatch Monitoring + SNS Alerts + S3 for static assets
```

### What You'll Build
একটা simple Node.js/Python Flask TODO app যেটা:
1. Multi-AZ deployment (2 subnets, 2 AZs)
2. Auto Scaling Group (min=2, max=4)
3. Application Load Balancer
4. RDS MySQL Multi-AZ
5. CloudWatch monitoring + alarms
6. Proper IAM roles (no access keys)

### Step-by-Step Tasks
- [ ] **Day 1:** Simple TODO app বানাও (Flask or Node.js + Express)
- [ ] **Day 2:** Custom VPC setup (Week 7-এর কাজ revise করো)
- [ ] **Day 3:** RDS MySQL launch private subnet-এ, connection test
- [ ] **Day 4:** Launch Template create করো User Data দিয়ে app auto-install
- [ ] **Day 5:** Auto Scaling Group + ALB setup করো
- [ ] **Day 6:** CloudWatch alarms + SNS topic (CPU, 5XX errors, DB connections)
- [ ] **Day 7:** Load test করো (Apache Bench or k6) — দেখো scaling কীভাবে কাজ করে

### Deliverables
- ✅ Live application URL
- ✅ GitHub repo (code + infrastructure docs)
- ✅ Architecture diagram with explanation
- ✅ Cost breakdown (monthly estimated)
- ✅ Demo video (3-5 min) showing: app working, scaling in action, monitoring dashboard
- ✅ Blog post with lessons learned


## 🗓️ Week 11: Review + AWS Certification Prep

**Focus:** Previous 10 weeks consolidate + certification exam — resume-এ credential add করবে

### 🎯 Learning Objectives
- AWS Certified Cloud Practitioner (CLF-C02) OR Solutions Architect Associate (SAA-C03) exam pass করবে
- Knowledge gaps identify করে fill করবে

### Recommended Certification Path

**Option A: AWS Certified Cloud Practitioner (CLF-C02)** — Easier, $100
- Timeline: 1 week prep enough
- Ideal for: First AWS cert, non-technical background
- Exam: 65 questions, 90 minutes

**Option B: AWS Certified Solutions Architect Associate (SAA-C03)** — Harder but more valuable, $150
- Timeline: 2-3 weeks prep (this week + extra)
- Ideal for: If you're confident with Month 2 material
- Exam: 65 questions, 130 minutes
- **Recommended by employers** — more weight than Practitioner

### Tasks This Week
- [ ] Full-length practice test নাও (Tutorials Dojo best)
- [ ] Weak areas identify করো, targeted revision করো
- [ ] Stephane Maarek's SAA course complete করো (Udemy — often on sale $10-15)
- [ ] Minimum ৩টা practice exam 75%+ score করো
- [ ] **Exam schedule করো** (Pearson VUE online from home possible)

### Resources
- **Course:** [Stephane Maarek's Ultimate AWS Certified Solutions Architect Associate](https://www.udemy.com/course/aws-certified-solutions-architect-associate-saa-c03/) (best-in-class)
- **Practice Tests:** [Tutorials Dojo](https://tutorialsdojo.com/) (most realistic practice tests)
- **Free:** [AWS Skill Builder - Exam Prep](https://explore.skillbuilder.aws/)

### Week 11 Checkpoint
**Deliverable:** Certification pass! Digital badge Credly থেকে LinkedIn-এ share করো। Resume update করো।


## 🗓️ Week 12: Interview Preparation + Job Hunting

**Focus:** Technical knowledge already achieved — এখন **communication + strategy** matter করে

### 🎯 Learning Objectives
- Cloud/DevOps Engineer role-এর জন্য ATS-friendly resume বানাতে পারবে
- Technical interview questions confidently answer করতে পারবে
- Behavioral questions STAR format-এ structure করতে পারবে
- Strategic job application করতে পারবে

### Topics to Master

**Resume & Portfolio**

| # | Topic |
|---|-------|
| 12.1 | ATS-Friendly Resume Writing for Tech (1 page) |
| 12.2 | Highlighting Projects Effectively (Action → Impact format) |
| 12.3 | LinkedIn Profile Optimization (Headline, About, Skills) |
| 12.4 | Building a Technical Portfolio Website (Week 9-এ already done!) |
| 12.5 | GitHub Profile as Resume (pinned repos, README) |

**Technical Interview Prep**

| # | Topic |
|---|-------|
| 12.6 | Common AWS Interview Questions (Top 50) |
| 12.7 | Linux Troubleshooting Scenarios |
| 12.8 | Networking Interview Questions (OSI, DNS, Load Balancer, etc.) |
| 12.9 | Simple System Design for Juniors (scalable web app) |
| 12.10 | Live Coding / Scripting Tasks (Bash, Python basic) |

**Behavioral Interview**

| # | Topic |
|---|-------|
| 12.11 | STAR Format (Situation, Task, Action, Result) |
| 12.12 | Common Behavioral Questions + Sample Answers |
| 12.13 | "Why DevOps?" and "Tell me about yourself" answers |
| 12.14 | Handling "I don't know" gracefully |
| 12.15 | Salary Negotiation Basics |

**Job Application Strategy**

| # | Topic |
|---|-------|
| 12.16 | Where to Apply (LinkedIn, RemoteOK, Wellfound, AWS Job Board, company careers pages) |
| 12.17 | Cold Outreach to Recruiters and Hiring Managers |
| 12.18 | Following Up Professionally |
| 12.19 | Tracking Applications (Notion/Spreadsheet) |

### Hands-on Tasks
- [ ] Resume বানাও, ৫ জনকে review করাও (Reddit r/EngineeringResumes useful)
- [ ] LinkedIn profile fully optimize করো (keyword-stuffed but natural)
- [ ] Mock interviews নাও — Pramp.com, Interviewing.io (free)
- [ ] ৫০টা Top AWS Interview Questions-এর answer লিখে practice করো
- [ ] ১০টা behavioral stories prepare করো STAR format-এ
- [ ] Apply to ২০ junior positions (minimum!) — Week 12-এর শেষের দিকে

### Resources
- **Resume:** [Tech Interview Handbook Resume Guide](https://www.techinterviewhandbook.org/resume/)
- **Interview Questions:** [DevOps Interview Questions GitHub](https://github.com/bregman-arie/devops-exercises)
- **Mock Interviews:** [Pramp](https://www.pramp.com/), [Interviewing.io](https://interviewing.io/)
- **Salary Data:** [levels.fyi](https://www.levels.fyi/), Glassdoor

### Week 12 Checkpoint + Syllabus 1 Final Outcome

**You should now have:**

| Asset | Status |
|-------|--------|
| Strong Linux + Networking + Python/Bash foundation | ✅ |
| Hands-on experience with 15+ AWS services | ✅ |
| AWS certification (CCP or SAA) | ✅ |
| 2 capstone projects on GitHub with detailed READMEs | ✅ |
| Live hosted portfolio website | ✅ |
| Active GitHub (12 weeks of commits) | ✅ |
| Professional LinkedIn profile | ✅ |
| 1-2 blog posts published | ✅ |
| Polished resume (ATS-friendly) | ✅ |
| Applied to 20+ jobs | ✅ |


## 🎯 Syllabus 1 Final Assessment Checklist

তুমি ready for Junior role যদি প্রতেকটাতে "Yes" বলতে পারো:

- [ ] Blank terminal-এ Linux command run করে comfortable?
- [ ] একটা simple Bash script লিখতে পারো without googling?
- [ ] VPC + subnet + routing structure কাগজে এঁকে বুঝাতে পারো?
- [ ] EC2 launch থেকে application deploy independently করতে পারো?
- [ ] IAM policy JSON read + write করতে পারো?
- [ ] Python দিয়ে simple AWS automation লিখতে পারো?
- [ ] একটা system down হলে CloudWatch + logs দেখে diagnose করার approach বোঝো?
- [ ] ১০ min-এ নিজের কোনো project whiteboard-এ explain করতে পারো?
- [ ] AWS certification already pass করেছো?
- [ ] Resume + LinkedIn + GitHub — ৩ টাই strong?

যদি ৮+ "Yes" হয় → **Syllabus 2 শুরু করার time!**


## 🚨 Important Notes

### What NOT to Do
- ❌ Tutorial hell-এ পড়ে যাবে না — ২ course-এর বেশি এক time-এ না
- ❌ Certification-এর জন্য memorize করে exam dumps use করবে না — long-term-এ loss
- ❌ "আমি যোগ্য না" mindset-এ আটকে থাকবে না — apply করো even at 70% readiness
- ❌ Projects GitHub-এ private রেখে দিবে না — public করো always (credentials ছাড়া)

### What TO Do
- ✅ প্রতি দিন commit করো (GitHub green squares = signal of activity)
- ✅ Weekly blog post বা LinkedIn post করো — "learning in public"
- ✅ Community-এ join করো: r/devops, r/aws, Discord servers
- ✅ Free Tier limit সতর্কতার সাথে — projects শেষ হলে resources terminate করো
- ✅ Note-taking system বানাও (Notion/Obsidian) — interview prep time-এ কাজে দেবে


## Estimated Costs for Syllabus 1

| Item | Cost |
|------|------|
| AWS Free Tier usage (if careful) | **$0–$10** |
| Udemy courses (Stephane Maarek bundle, on sale) | **$20–$30** |
| AWS Certification exam (CCP or SAA) | **$100–$150** |
| Domain name for portfolio | **$10–$15/year** |
| **Total** | **~$150–$200** |

যদি budget tight হয় — Free Tier + YouTube only দিয়ে কাজ চালাতে পারো। Certification defer করো Syllabus 2-এ।


## After Syllabus 1

Next: **Syllabus 2 (Weeks 13-24)** — Production-Grade Engineer  
Focus: Terraform + Docker + Kubernetes + CI/CD + Advanced Monitoring

এইটা complete করলে তুমি Mid-Level engineer হিসেবে apply করতে পারবে (এমনকি যদি full ২ years experience না থাকে — projects + skills speak louder than YoE)।

---

**Made with ❤️ for your Cloud Engineering Journey**  
*Remember: Consistency > Intensity. 2 hours daily > 14 hours Sunday.*
