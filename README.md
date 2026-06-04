# ☁️ AWS Cloud Portfolio – Amy Zepeda

A documentation of my hands-on AWS projects as I transition into cloud computing. This repo tracks my progress building real infrastructure on AWS, working toward the AWS Solutions Architect Associate (SAA-C03) certification, and developing skills in cloud architecture and operations.

-----

## 🔧 Environment Setup

### AWS Account Baseline

Configured a new AWS account following security best practices before deploying any resources:

- **Billing Alerts** – Set up billing preferences and CloudWatch billing alarms to monitor spend and avoid unexpected charges
- **Root Account Protection** – Enabled MFA on the root account; root is not used for day-to-day operations
- **Domain** – Registered `junkbeetle.cloud` via Namecheap for future portfolio site deployment

-----

## 🔐 IAM Structure

Designed IAM with separation of concerns — no direct policy attachments to users, and root access locked down from the start.

### Groups

|Group      |Policy             |Purpose                                  |
|-----------|-------------------|-----------------------------------------|
|`Admins`   |AdministratorAccess|Console access for managing AWS resources|
|`CLI-Users`|AdministratorAccess|Programmatic access via AWS CLI          |

Note: For a production environment, CLI-Users would follow least-privilege principles with scoped permissions rather than full AdministratorAccess.


### Design Decisions

- **Groups over direct policy attachment** – Policies are attached to groups, not individual users. This makes permission management scalable as the environment grows.
- **Separate console and CLI users** – Follows least privilege principles and mirrors real-world IAM best practices. Console user has MFA; CLI user has access keys only.
- **No root usage after setup** – Root account is reserved for account-level emergencies only.

-----

## 🗂️ Upcoming Projects

- [X] S3 static website hosting for `junkbeetle.cloud`
- [ ] CloudFront distribution + ACM SSL certificate
- [ ] Route 53 DNS configuration
- [X] AWS CLI configuration on Linux home lab
- [ ] EC2 instance setup and SSH access

-----

## 📚 Certifications In Progress

- **AWS Solutions Architect Associate (SAA-C03)** – In progress
  - Study resources: Stephane Maarek (Udemy), Tutorials Dojo practice exams
- **AWS Academy** – Cloud Foundations ✅ | Cloud Architecting ✅ | Cloud Developing ✅

-----

## 🛠️ Tools & Technologies

- AWS (IAM, S3, CloudFront, Route 53, EC2, CloudWatch)
- Linux (Ubuntu home lab)
- AWS CLI
- Git / GitHub

-----

*This portfolio is actively updated as I build and learn. Each project folder will contain its own documentation, architecture diagrams, and deployment notes.*
