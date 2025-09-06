# 🚀 AWS Services Overview

This document provides a categorized list of **AWS services** with **purpose**, **costing**, and **Free Tier eligibility**.

---

## 1. Compute Services

| Service         | Why Use It                                                                           | Costing                                                 | Free Tier                                                            |
| --------------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------- | -------------------------------------------------------------------- |
| **EC2**         | Run virtual machines with full control over OS, networking, and storage.             | Pricing varies by instance type, region, usage.         | 750 hours per month of t2.micro or t3.micro instances for 12 months. |
| **Lambda**      | Serverless compute – run code without managing servers, pay only for execution time. | \$0.20 per 1M requests, \$0.00001667 per GB-second.     | 1M requests & 400,000 GB-seconds per month for 12 months.            |
| **ECS**         | Orchestrate Docker containers easily on AWS-managed infrastructure.                  | Pricing depends on EC2 or Fargate launch type.          | No Free Tier.                                                        |
| **EKS**         | Run Kubernetes without managing control plane, integrate with AWS services.          | \$0.10/hour per cluster + EC2/Fargate costs.            | No Free Tier.                                                        |
| **Lightsail**   | Simple VMs for small apps, websites, quick prototyping.                              | Starts at \$3.50/month for 512MB RAM, 1 vCPU, 20GB SSD. | 750 hours per month of Lightsail usage for 12 months.                |
| **Batch**       | Run batch computing jobs at scale.                                                   | Depends on resources used.                              | No Free Tier.                                                        |
| **Outposts**    | Bring AWS infrastructure on-premises for hybrid cloud.                               | Depends on configuration.                               | No Free Tier.                                                        |
| **Local Zones** | Extend AWS services close to end-users for low-latency apps.                         | Depends on services used.                               | No Free Tier.                                                        |

---

## 2. Storage Services

| Service             | Why Use It                                              | Costing                          | Free Tier                                                                  |
| ------------------- | ------------------------------------------------------- | -------------------------------- | -------------------------------------------------------------------------- |
| **S3**              | Object storage – files, images, backups.                | \$0.023 per GB (first 50TB).     | 5GB Standard Storage, 20,000 GET & 2,000 PUT requests/month for 12 months. |
| **EBS**             | Block storage for EC2, persistent disks.                | \$0.08 per GB gp2.               | 30GB gp2, 2M I/Os, 1GB snapshot storage/month for 12 months.               |
| **EFS**             | Fully managed scalable file system for multiple EC2s.   | \$0.30/GB/month.                 | 5GB Standard storage/month for 12 months.                                  |
| **FSx**             | Managed Windows File Server & Lustre for HPC workloads. | Pricing varies by configuration. | No Free Tier.                                                              |
| **Glacier**         | Low-cost long-term archival storage.                    | \$0.004/GB/month.                | 10GB/month for 12 months.                                                  |
| **Storage Gateway** | Connect on-prem systems to AWS storage.                 | \$0.025 per GB stored.           | First 100GB/month free.                                                    |

---

## 3. Database Services

| Service         | Why Use It                                                   | Costing                            | Free Tier                                                        |
| --------------- | ------------------------------------------------------------ | ---------------------------------- | ---------------------------------------------------------------- |
| **RDS**         | Managed relational databases.                                | Depends on engine, instance type.  | 750 hours db.t2.micro/db.t3.micro instances/month for 12 months. |
| **Aurora**      | High-performance MySQL/Postgres-compatible DB.               | \$0.10/ACU-hour Aurora Serverless. | 750 hours t2.micro/t3.micro instances/month for 12 months.       |
| **DynamoDB**    | Fully managed NoSQL DB with millisecond response.            | \$1.25 per WCU/RCU per month.      | 25GB storage, 25 WCU & 25 RCU/month for 12 months.               |
| **ElastiCache** | Managed Redis/Memcached for caching & real-time performance. | \$0.021/hour for cache.m5.large.   | No Free Tier.                                                    |
| **Neptune**     | Graph DB for relationships & connected data.                 | \$0.10/hour db.r5.large.           | 30-day trial: 750 hours db.t3.medium, 5GB storage, 30M IOs.      |
| **Redshift**    | Data warehouse for analytics.                                | \$0.25/hour dc2.large node.        | 2-month trial: 750 hours dc2.large usage.                        |
| **DocumentDB**  | MongoDB-compatible managed NoSQL DB.                         | \$0.30/hour db.r5.large.           | 30-day trial: 750 hours db.t3.medium, 5GB storage, 30M IOs.      |
| **Timestream**  | Time-series DB for IoT, monitoring, analytics.               | \$0.50 per TB ingested.            | 1M writes & 1M reads/month for 12 months.                        |

---

## 4. Networking & Content Delivery

| Service                | Why Use It                                           | Costing                                              | Free Tier                                                            |
| ---------------------- | ---------------------------------------------------- | ---------------------------------------------------- | -------------------------------------------------------------------- |
| **VPC**                | Isolated network with subnets, routing, firewalls.   | No charge for VPC itself; charges for NAT, VPN, etc. | No Free Tier.                                                        |
| **Route 53**           | Scalable DNS & domain registration.                  | \$0.40/hosted zone, \$0.09/million queries.          | No Free Tier.                                                        |
| **CloudFront**         | CDN for low-latency content distribution.            | \$0.085/GB for first 10TB.                           | 1TB data transfer out + 10M HTTP/HTTPS requests/month for 12 months. |
| **API Gateway**        | Manage, secure, scale APIs.                          | REST: \$3.50/million requests; HTTP: \$1/million.    | 1M requests/month for REST & HTTP APIs for 12 months.                |
| **Direct Connect**     | Dedicated network link to AWS.                       | \$0.25/hour for 1Gbps connection.                    | No Free Tier.                                                        |
| **Global Accelerator** | Improve app availability & performance.              | \$0.025/hour + \$0.008/GB data.                      | No Free Tier.                                                        |
| **PrivateLink**        | Secure private connectivity between VPCs & services. | \$0.01/GB data processed.                            | No Free Tier.                                                        |

---

## 5. Security, Identity & Compliance

| Service             | Why Use It                       | Costing                                                            | Free Tier                                 |
| ------------------- | -------------------------------- | ------------------------------------------------------------------ | ----------------------------------------- |
| **IAM**             | Manage users, roles, policies.   | Free.                                                              | Always free.                              |
| **Cognito**         | User authentication, federation. | \$0.0055 per MAU (after free).                                     | 50,000 MAU/month free for 12 months.      |
| **Secrets Manager** | Store & rotate secrets.          | \$0.40/secret/month + \$0.05 per 10,000 API calls.                 | 30-day trial for 1 secret.                |
| **KMS**             | Create & manage encryption keys. | \$1 per key/month + \$0.03 per 10k requests.                       | 20,000 free requests/month for 12 months. |
| **Shield**          | DDoS protection.                 | Standard included; Advanced \$3,000/month.                         | Standard free.                            |
| **WAF**             | Web application firewall.        | \$5/month per WebACL + \$1 per rule + \$0.60 per million requests. | No Free Tier.                             |
| **Inspector**       | Security assessment.             | \$0.30 per assessment target per month.                            | No Free Tier.                             |
| **GuardDuty**       | Threat detection & monitoring.   | \$1 per GB analyzed.                                               | 30-day free trial.                        |
| **Macie**           | Detect sensitive data using ML.  | \$5 per GB of data processed.                                      | 30-day free trial.                        |

---

## 6. Analytics & Big Data

| Service           | Why Use It                                 | Costing                                              | Free Tier                                    |
| ----------------- | ------------------------------------------ | ---------------------------------------------------- | -------------------------------------------- |
| **Athena**        | Query S3 using SQL.                        | \$5 per TB scanned.                                  | 1TB scanned/month free for 12 months.        |
| **EMR**           | Big data processing (Hadoop, Spark, Hive). | \$0.07 per EC2 instance-hour + EMR fees.             | No Free Tier.                                |
| **Kinesis**       | Real-time streaming.                       | \$0.015 per shard-hour + \$0.015 per GB PUT payload. | 1M PUT payload units/month free.             |
| **QuickSight**    | Business intelligence dashboards.          | \$9/user/month (standard).                           | 1 user free for 12 months.                   |
| **Data Pipeline** | Move/process data between services.        | \$1 per pipeline per month + EC2 costs.              | No Free Tier.                                |
| **Glue**          | ETL for preparing datasets.                | \$0.44 per DPU-hour.                                 | 1M requests & 1TB data processed/month free. |





# 🌐 Amazon VPC Features

Amazon Virtual Private Cloud (VPC) lets you launch AWS resources in a logically isolated network that you define.  
Below is a list of VPC features, why they are useful, and examples of how they are applied.

---

## 🔑 Core Features of VPC

| Feature | Why Use It | Example |
|---------|------------|---------|
| **Subnets** | Separate resources into **public** (internet-facing) and **private** (internal only) networks for security and better architecture design. | Web servers run in a **public subnet** while databases stay in a **private subnet** for isolation. |
| **Route Tables** | Control how traffic flows within the VPC, to the internet, or to other networks. | A route table sends all `0.0.0.0/0` traffic to the **Internet Gateway** for public internet access. |
| **Internet Gateway (IGW)** | Enables internet connectivity for resources in public subnets. | A web server in a public subnet uses IGW to serve content to global users. |
| **NAT Gateway / NAT Instance** | Lets private subnet resources access the internet **outbound** without exposing them to inbound internet traffic. | A database downloads OS patches via **NAT Gateway** without being exposed to the internet. |
| **Elastic IPs** | Provides a **static public IP** for resources, useful for whitelisting or external access. | Assign a fixed IP to a **bastion host** so administrators can always connect securely. |
| **VPC Peering** | Connects two VPCs privately over AWS’s backbone network. | A **Dev VPC** securely communicates with a **Prod VPC** without internet exposure. |
| **Transit Gateway** | Acts as a central hub to connect multiple VPCs and on-premises networks, simplifying complex topologies. | An enterprise with **10 VPCs** and **2 data centers** uses Transit Gateway for hub-and-spoke networking. |
| **VPC Endpoints (Interface/Gateway)** | Securely connect to AWS services (e.g., S3, DynamoDB) without using public internet. | An app in a private subnet retrieves images from **S3** via a VPC Gateway Endpoint. |
| **Security Groups (SGs)** | Instance-level firewalls that allow only required inbound/outbound traffic. | A DB SG allows connections **only from the App Server SG**, blocking everything else. |
| **Network ACLs (NACLs)** | Subnet-level firewalls that control inbound and outbound traffic (stateless). | Block a known malicious IP range at the **subnet level** for added security. |
| **Flow Logs** | Capture IP traffic logs for troubleshooting, monitoring, and compliance. | Detect suspicious spikes in traffic by analyzing **VPC Flow Logs** in CloudWatch. |
| **Elastic Network Interfaces (ENIs)** | Attach multiple NICs to an EC2 instance for failover or network segregation. | A server has one ENI for **public traffic** and another for **internal-only communication**. |
| **DHCP Options Sets** | Customize DNS and DHCP settings for resources in the VPC. | Point instances to use **corporate DNS servers** instead of AWS defaults. |
| **VPN Connections** | Connect on-premises networks securely to AWS via encrypted IPsec tunnels. | A corporate office establishes a **VPN tunnel** to access workloads in AWS. |
| **AWS Direct Connect** | Provides private, low-latency, high-bandwidth dedicated links from data centers to AWS. | A **bank** uses Direct Connect for fast, secure connections to its AWS workloads. |
| **PrivateLink** | Access services in another VPC privately without internet or VPC peering. | A SaaS vendor exposes its service using **PrivateLink**, and customers consume it securely. |
| **IPv6 Support** | Provides scalable addressing for global applications and IoT. | A global e-commerce app uses **IPv6** to handle millions of devices worldwide. |
| **Carrier Gateway (CGW)** | Connect mobile networks (4G/5G) with AWS for telecom workloads. | A **5G IoT platform** connects mobile devices directly to AWS workloads via Carrier Gateway. |



# 🔐 AWS IAM (Identity and Access Management) Features

AWS IAM helps you securely control access to AWS services and resources.  
You can manage **who** is authenticated (identity) and **what** they are authorized to do (permissions).

---

## 🔑 Core IAM Features

| Feature | Why Use It | Example |
|---------|------------|---------|
| **IAM Users** | Represents individual people or applications needing access to AWS resources. Each user has credentials. | Create a user **developer1** with programmatic access keys for CLI use. |
| **IAM Groups** | Organize multiple users and attach permissions collectively instead of managing them individually. | Add all developers to a **Developers Group** that has EC2 read-only permissions. |
| **IAM Roles** | Provide temporary permissions to AWS resources without long-term credentials. | An **EC2 instance role** lets an app access S3 buckets without storing keys. |
| **Policies** | JSON documents that define permissions (allow/deny actions on resources). | Attach an **S3FullAccess policy** to a role so an app can manage S3 objects. |
| **Temporary Security Credentials (STS)** | Provide time-limited credentials for secure access. | A contractor gets **12-hour temporary credentials** to access a DynamoDB table. |
| **IAM Federation (SSO)** | Allow users to log in with corporate credentials or third-party identity providers (Google, AD, Okta). | Employees use their **company Active Directory** login to access AWS Console. |
| **Access Keys** | Programmatic credentials (ID + secret) for CLI/SDK/API access. | An automation script uses **access keys** to call AWS APIs. |
| **Multi-Factor Authentication (MFA)** | Adds an extra layer of security beyond username/password. | Require admins to use **MFA tokens** when accessing the AWS Console. |
| **Service-Linked Roles** | Roles created automatically by AWS services to perform tasks on your behalf. | **CloudWatch** creates a service-linked role to push logs securely. |
| **Permissions Boundaries** | Limit the maximum permissions an IAM entity (user/role) can have. | A developer role has permissions, but the boundary prevents creating IAM users. |
| **Resource-Based Policies** | Policies attached directly to resources (like S3, SNS, SQS) for fine-grained control. | An **S3 bucket policy** allows access only from a specific VPC. |
| **Access Analyzer** | Helps identify resources shared publicly or with external accounts. | Detects that an **S3 bucket is accidentally public** and alerts admins. |
| **Credential Report & Access Advisor** | Provide visibility into user activity and unused permissions. | Identify IAM users with **unused keys** or roles that haven’t been used in 90 days. |
| **Identity Center (AWS SSO)** | Centralized single sign-on for multiple AWS accounts and applications. | A user logs in once and gets access to **multiple AWS accounts** via Identity Center. |



## 🔑 Core EC2 Features

| Feature | Why Use It | Example |
|---------|------------|---------|
| **Instance Types** | Choose from a wide variety of instance types optimized for compute, memory, storage, or GPU. | Use **C7g instances** for high-performance compute workloads, or **R6g** for memory-heavy databases. |
| **Amazon Machine Images (AMIs)** | Launch preconfigured instances with OS, apps, and software. | Start a server with a **Linux + Apache pre-built AMI**. |
| **Elastic Block Store (EBS)** | Persistent block storage volumes that survive instance stop/start. | Attach a 100 GB EBS volume to an EC2 running MySQL for database storage. |
| **Instance Store** | Temporary block storage physically attached to the host (fast but non-persistent). | Use for **cache** or temporary logs that don’t need to persist. |
| **Elastic IPs** | Assign a static public IP address to an instance. | A **bastion host** keeps the same IP address even if restarted. |
| **Security Groups** | Virtual firewalls at the instance level. | Allow only **port 22 (SSH)** for admins and **port 443 (HTTPS)** for users. |
| **Key Pairs (SSH/RDP)** | Secure login to instances without passwords. | Use an SSH key to log into a Linux EC2 server. |
| **Elastic Load Balancer (ELB)** | Distribute incoming traffic across multiple EC2 instances. | A web app uses an **ALB** to balance traffic between 3 EC2 servers. |
| **Auto Scaling** | Automatically increase or decrease EC2 capacity based on demand. | Scale from **2 to 10 EC2 instances** during traffic spikes, then scale back down. |
| **Placement Groups** | Control how instances are placed across hardware (cluster, spread, partition). | Run **HPC workloads** with low-latency networking in a cluster placement group. |
| **EC2 Spot Instances** | Use spare AWS capacity at up to 90% lower cost. | Run **big data batch jobs** cost-effectively on Spot instances. |
| **EC2 Reserved Instances / Savings Plans** | Save money with 1–3 year commitments. | A production web app runs on **Reserved Instances** for predictable workloads. |
| **Dedicated Hosts / Instances** | Run EC2 on dedicated physical servers for compliance or licensing. | A financial company needs **dedicated servers** for regulatory compliance. |
| **Elastic Network Interfaces (ENIs)** | Attach multiple NICs to an instance for failover or network segregation. | Use one ENI for **public internet traffic** and another for **internal-only communication**. |
| **User Data & Metadata** | Pass startup scripts or retrieve instance information programmatically. | Use **User Data** to auto-install Nginx on boot. |
| **Monitoring (CloudWatch)** | Track performance metrics like CPU, memory, and network. | Set a **CloudWatch alarm** to restart an instance if CPU usage stays at 0%. |
| **EC2 Hibernate** | Pause an instance and resume later with the same memory and state. | A developer pauses a test server at night and resumes it in the morning. |
| **Elastic Fabric Adapter (EFA)** | Provides high-performance networking for HPC and ML workloads. | Train ML models on **GPU clusters** with low-latency communication. |
| **Launch Templates & Configurations** | Define standard instance settings for consistency. | Use a **launch template** for auto-scaling a fleet of identical servers. |


# 🌐 Amazon API Gateway Features with Costing & Free Tier

Amazon API Gateway is a fully managed service to create, publish, maintain, monitor, and secure APIs at any scale.  
It acts as the **front door** for applications to access data, business logic, or functionality from your backend services.

---

## 🎁 Free Tier (12 Months)

- **HTTP APIs** → 1 million requests per month  
- **REST APIs** → 1 million requests per month  
- **WebSocket APIs** → 1 million messages + 750,000 connection minutes per month  
- **Data Transfer** → Counts separately under AWS free tier (1 GB outbound free per month)  
- **Other Features** (like Custom Domain, Caching, VPC Links, CloudWatch logs) → **not included** in free tier (billed separately)

---

## 🔑 Core API Gateway Features with Costing

| Feature | Why Use It | Example | Costing |
|---------|------------|---------|---------|
| **API Types (REST, HTTP, WebSocket)** | Choose the right API type depending on workload. | Use **HTTP API** for microservices, **REST API** for enterprise, **WebSocket API** for chat apps. | **HTTP API**: $1 per million requests (first 300M). <br> **REST API**: $3.50 per million (first 333M). <br> **WebSocket API**: $1 per million messages + $0.25 per million connection minutes. |
| **Custom Domain Names** | Branded domains instead of AWS URLs. | `https://api.mycompany.com`. | $0.40 per custom domain/month + ACM cert (free). |
| **Stages & Stage Variables** | Maintain environments (dev, test, prod). | `/dev` vs `/prod`. | No extra cost. |
| **Request & Response Transformation** | Modify request/response payloads. | Convert XML → JSON before sending to Lambda. | Included in request cost. |
| **Authorization & Authentication** | Secure access via IAM, Cognito, JWT, Lambda authorizers. | Only logged-in **Cognito users** access `/orders`. | Lambda authorizer adds **extra Lambda cost** per execution. |
| **Rate Limiting & Throttling** | Prevent abuse and protect backend. | Limit partner API calls to 100 RPS. | Included in request cost. |
| **API Keys & Usage Plans** | Manage partner/customer access with quotas. | Issue key with 1M requests/month. | No extra cost (requests billed normally). |
| **Caching (REST APIs only)** | Reduce backend calls, improve latency. | Cache product catalog for 60s. | 0.5 GB = $0.02/hour, 1.6 GB = $0.038/hour, up to 237 GB = $3.80/hour. |
| **Integration with AWS Services** | Call Lambda, DynamoDB, S3, etc. | API → Lambda → DynamoDB. | Normal API Gateway request + backend service cost. |
| **Monitoring & Logging (CloudWatch, X-Ray)** | Track performance, errors, and latency. | Monitor **90% requests <100ms**. | CloudWatch Logs: $0.50/GB ingested. <br> X-Ray: $5 per 1M traces + $0.50/GB. |
| **SDK Generation** | Auto-generate SDKs for iOS/Android/JS. | Generate iOS SDK for mobile developers. | Free. |
| **VPC Links / Private Integrations** | Securely connect internal services. | API → Private EC2 in VPC. | $0.022/hour per VPC Link + data processed cost. |
| **Cross-Origin Resource Sharing (CORS)** | Allow cross-domain browser calls. | React app (`myapp.com`) → API (`api.mycompany.com`). | Included in request cost. |
| **WebSocket APIs** | Real-time, two-way communication. | Live sports score API. | $1 per million messages + $0.25 per million connection minutes. |
| **Deployment & Versioning** | Support multiple API versions. | `/v1/orders` vs `/v2/orders`. | No extra cost. |
| **Request Validation** | Validate schema before backend call. | Ensure valid JSON payload. | Included in request cost. |
| **Access Control with Resource Policies** | Restrict by IP, VPC, or account. | Allow only **corporate IPs**. | Included in request cost. |

---

## 💰 Cost Example Comparison

- **Scenario**: 10 million requests/month, 1 KB each  
  - **HTTP API**: 10M × $1 = **$10**  
  - **REST API**: 10M × $3.50 = **$35**  
  - **WebSocket API**: 10M messages + 1M connection minutes → **$12.50**  

---

## ✅ Summary

- **Free Tier** gives **1M requests/messages/month** (good for dev/testing).  
- **HTTP APIs** → Best for cost-sensitive, lightweight services.  
- **REST APIs** → Full-featured, enterprise-grade APIs (request validation, caching, usage plans).  
- **WebSocket APIs** → Real-time apps like chat, gaming, notifications, IoT.  











# aws-notes


    pricing by instance :
    ----------------------
    2cpu+1gb ram: $4 per months for 2GB its $8 and for 4GB its will be $16
    https://aws.amazon.com/ec2/pricing/on-demand/
    
    amazon ec2 default user:
    --------------------------
    
    normally , if you choose ubuntu image default user will be ubuntu
    if you choose Amazon linux image default user will be ec2-user ...etc
    you can connect via connect buttion of ec2 /you can see default user name aswell here.
    
    
  default user list 
  --------------------------------------
        
        Amazon Linux 2023: ec2-user
        Amazon Linux 2: ec2-user
        Amazon Linux: ec2-user
        CentOS:	centos or ec2-user
        Debian:	admin
        Fedora:	fedora or ec2-user
        RHEL:	ec2-user or root
        SUSE:	ec2-user or root
        Ubuntu:	ubuntu
        Oracle:	ec2-user
        Bitnami:	bitnami
        Other:	Check with the AMI provider

        reference:
        https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connection-prereqs.html



