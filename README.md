# 🚀 AWS Services Overview

This document provides a categorized list of **AWS services** with short descriptions of **why we should use them**.

---

## 1. Compute Services

| Service | Why Use It |
|---------|------------|
| **EC2 (Elastic Compute Cloud)** | Run virtual machines in the cloud with full control over OS, networking, and storage. |
| **Lambda** | Serverless compute – run code without managing servers, pay only for execution time. |
| **ECS (Elastic Container Service)** | Orchestrate Docker containers easily on AWS-managed infrastructure. |
| **EKS (Elastic Kubernetes Service)** | Run Kubernetes without managing the control plane, integrate with AWS services. |
| **Lightsail** | Simple VMs for small apps, websites, and quick prototyping. |
| **Batch** | Run batch computing jobs at scale with automatic resource provisioning. |
| **Outposts** | Bring AWS infrastructure on-premises for hybrid cloud. |
| **Local Zones** | Extend AWS services close to end-users for low-latency apps. |

---

## 2. Storage Services

| Service | Why Use It |
|---------|------------|
| **S3 (Simple Storage Service)** | Object storage for files, images, backups – durable and highly scalable. |
| **EBS (Elastic Block Store)** | Block storage for EC2 instances, persistent disks. |
| **EFS (Elastic File System)** | Fully managed, scalable shared file system for multiple EC2 instances. |
| **FSx** | Managed Windows File Server and Lustre for HPC workloads. |
| **Glacier (S3 Glacier)** | Low-cost, long-term archival storage. |
| **Storage Gateway** | Connect on-premises systems to AWS cloud storage seamlessly. |

---

## 3. Database Services

| Service | Why Use It |
|---------|------------|
| **RDS** | Managed relational databases (MySQL, PostgreSQL, Oracle, SQL Server, MariaDB, Aurora). |
| **Aurora** | High-performance, MySQL/Postgres-compatible cloud database. |
| **DynamoDB** | Fully managed NoSQL database with millisecond response times. |
| **ElastiCache** | Managed Redis/Memcached for caching and real-time performance. |
| **Neptune** | Graph database for relationships and connected data. |
| **Redshift** | Data warehouse for analytics at scale. |
| **DocumentDB** | MongoDB-compatible managed NoSQL database. |
| **Timestream** | Time-series database for IoT, monitoring, analytics. |

---

## 4. Networking & Content Delivery

| Service | Why Use It |
|---------|------------|
| **VPC (Virtual Private Cloud)** | Isolated network environment with subnets, routing, and firewalls. |
| **Route 53** | Scalable DNS and domain registration service. |
| **CloudFront** | CDN for caching and distributing content globally with low latency. |
| **API Gateway** | Manage, secure, and scale APIs. |
| **Direct Connect** | Dedicated network link from on-premises to AWS. |
| **Global Accelerator** | Improves availability and performance of apps with static IPs. |
| **PrivateLink** | Secure private connectivity between VPCs and services. |

---

## 5. Security, Identity & Compliance

| Service | Why Use It |
|---------|------------|
| **IAM** | Control access with users, roles, and policies. |
| **Cognito** | User authentication, sign-in, and federation for apps. |
| **Secrets Manager** | Securely store and rotate credentials, API keys, and secrets. |
| **KMS** | Create and control encryption keys. |
| **Shield** | Managed DDoS protection. |
| **WAF (Web Application Firewall)** | Protect apps from common web exploits. |
| **Inspector** | Automated security assessment service. |
| **GuardDuty** | Threat detection and monitoring service. |
| **Macie** | Detect sensitive data (like PII) in S3 using ML. |

---

## 6. Analytics & Big Data

| Service | Why Use It |
|---------|------------|
| **Athena** | Query S3 data using SQL (serverless). |
| **EMR** | Big data processing with Hadoop, Spark, Hive. |
| **Kinesis** | Real-time streaming data processing. |
| **QuickSight** | Business intelligence and dashboards. |
| **Data Pipeline** | Move and process data between services. |
| **Glue** | ETL (Extract, Transform, Load) for preparing datasets. |

---

## 7. Machine Learning & AI

| Service | Why Use It |
|---------|------------|
| **SageMaker** | Build, train, and deploy ML models at scale. |
| **Rekognition** | Image and video analysis (faces, objects, moderation). |
| **Polly** | Text-to-speech with natural voices. |
| **Lex** | Build chatbots and conversational interfaces. |
| **Comprehend** | NLP for text analysis (sentiment, entities, language). |
| **Translate** | Language translation. |
| **Forecast** | Time-series forecasting using ML. |
| **Textract** | Extract text and data from scanned documents. |

---

## 8. Developer Tools

| Service | Why Use It |
|---------|------------|
| **CodeCommit** | Managed Git repositories. |
| **CodeBuild** | Build and test code in the cloud. |
| **CodeDeploy** | Automate deployments to EC2, Lambda, on-prem servers. |
| **CodePipeline** | CI/CD pipeline automation. |
| **Cloud9** | Web-based IDE. |
| **X-Ray** | Debug and analyze distributed applications. |

---

## 9. Management & Monitoring

| Service | Why Use It |
|---------|------------|
| **CloudWatch** | Monitor logs, metrics, and events across AWS resources. |
| **CloudTrail** | Track API calls and user activity for compliance and auditing. |
| **Config** | Track AWS resource configurations over time. |
| **Trusted Advisor** | Cost optimization, performance, and security recommendations. |
| **Systems Manager (SSM)** | Manage servers and automation tasks at scale. |
| **Service Catalog** | Manage approved IT service catalogs. |

---

## 10. Migration & Transfer

| Service | Why Use It |
|---------|------------|
| **DMS** | Migrate databases with minimal downtime. |
| **SMS** | Migrate on-premises servers to AWS. |
| **Snowball** | Transfer large datasets physically (petabyte-scale). |
| **Migration Hub** | Track and manage migrations across AWS services. |
| **DataSync** | Automate large data transfers between on-prem and AWS. |


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



