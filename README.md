🛡️ AWS Cloud Security Automation Suite
A production-grade collection of Python tools for automated security auditing, compliance monitoring, and threat detection using Boto3.
🚀 Projects Overview:
01. CIS Compliance Checker
Description: Audits the entire AWS environment against the CIS AWS Foundations Benchmark v1.4.0.

Key Features: Automated checks for Identity (IAM), Logging, and Networking standards.

Impact: Ensures the infrastructure adheres to global security best practices and compliance requirements.

02. Cloud Attack Surface Mapper
Description: Maps all internet-facing assets to identify potential entry points for attackers.

Key Features: Detects Public IPs and identifies unrestricted Security Group rules (e.g., Port 22 open to 0.0.0.0/0).

Impact: Minimizes the external attack vector and reduces the overall exposure of the cloud environment.

03. Cloud Backup & Disaster Recovery Validator
Description: Verifies the integrity and encryption status of AWS Backup jobs.

Key Features: Flags failed backup jobs and identifies unencrypted recovery points.

Impact: Guarantees data recoverability during Ransomware attacks or accidental deletion events.

04. Cloud Backup Recency (RPO) Monitor
Description: Tracks the exact timestamp of the latest successful backup to monitor the Recovery Point Objective (RPO).

Key Features: Calculates the time gap since the last backup in a high-precision UTC format.

Impact: Prevents significant data loss by ensuring backups are up-to-date and within compliance limits.

05. Cloud Cost Abuse (Crypto-jacking) Detector
Description: Detects resource hijacking and unauthorized crypto-mining activities.

Key Features: Monitors for sudden, unexpected daily cost anomalies and resource spikes.

Impact: Prevents massive financial losses due to account compromise or "Crypto-jacking".

06. Cloud Resource Inventory
Description: Generates a real-time snapshot of all active resources across the AWS account.

Key Features: Lists EC2 instances, S3 buckets, and RDS databases for comprehensive asset management.

Impact: Eliminates "Shadow IT" by providing 100% visibility into deployed cloud assets.

07. CloudTrail Logging & Visibility Audit
Description: Audits AWS CloudTrail to ensure management events are being recorded properly.

Key Features: Checks for multi-region trail logging and ensures log file validation is active.

Impact: Provides an immutable and reliable audit trail for security investigations.

08. EC2 Security Group (Firewall) Auditor
Description: Performs deep inspection of Virtual Firewall (Security Group) rules.

Key Features: Detects "Anywhere" (0.0.0.0/0) ingress rules and identifies unused/stale security groups.

Impact: Hardens the network perimeter and prevents unauthorized remote access.

09. Forensic Logging Compliance Checker
Description: Ensures that forensic-level logging (VPC Flow Logs, DNS Logs) is enabled.

Key Features: Verifies if network-level visibility is active for deep traffic analysis.

Impact: Enables rapid root-cause analysis and threat hunting during a security breach.

10. IAM (Identity) Auditor
Description: Audits IAM users, groups, and roles for basic credential hygiene.

Key Features: Identifies users without MFA enabled and checks for old, unused access keys.

Impact: Reduces the risk of credential theft and unauthorized account access.

11. IAM Identity Auditor (MFA & Key Rotation)
Description: Performs a specific deep-dive into Multi-Factor Authentication compliance and key lifecycle.

Key Features: Flags access keys older than 90 days and enforces MFA for privileged accounts.

Impact: Hardens the identity perimeter by ensuring only active, verified users have access.

12. IAM Identity Auditor (Password Policy)
Description: Audits account-level password complexity and reuse requirements.

Key Features: Checks for minimum password length, character variety, and expiration settings.

Impact: Protects against brute-force attacks by enforcing strong password standards.

13. IAM Privilege Escalation Auditor
Description: (Proactive) Identifies risky policy configurations that could allow users to self-elevate permissions.

Key Features: Scans for "Indirect Admin" permissions like iam:PassRole or iam:CreateAccessKey.

Impact: Prevents users from granting themselves AdministratorAccess.

14. IAM Privilege Escalation Detector
Description: (Reactive) Monitors for active attempts to bypass elevation controls.

Key Features: Flags wildcard (*) permissions and monitors for suspicious API calls that elevate privileges.

Impact: Enforces the Principle of Least Privilege (PoLP) in real-time.

15. MITRE ATT&CK Threat Mapper
Description: Maps security findings to the MITRE ATT&CK for Cloud framework.

Key Features: Translates technical gaps into attacker Tactics (e.g., Persistence, Exfiltration).

Impact: Provides high-level threat context for SOC teams and business stakeholders.

16. S3 PUBLIC ACCESS SCANNER
Description: Scans S3 buckets for public read/write permissions.

Key Features: Inspects Bucket Policies and Access Control Lists (ACLs) for unintended exposure.

Impact: Prevents data breaches caused by misconfigured cloud storage.

17. Sentinel Cloud Auditor
Description: A unified auditing engine for a security posture snapshot.

Key Features: Aggregates findings from across all services into a single, actionable report.

Impact: Provides a holistic view of the account's security health at any given moment.
/Cloud-Security-Automation-Suite
/Cloud-Security-Automation-Suite
├── 01_CIS_Compliance_Checker/       # Global Standard Hardening (v1.4.0)
├── 02_Attack_Surface_Mapper/        # External Exposure & Port Analysis
├── 03_Backup_DR_Validator/          # Recovery Readiness & KMS Audit
├── 04_Backup_Recency_Monitor/       # RPO (Recovery Point Objective) Tracking
├── 05_Cost_Abuse_Detector/          # Crypto-jacking & Anomaly Detection
├── 06_Resource_Inventory/           # Asset Visibility & Shadow IT Discovery
├── 07_CloudTrail_Audit/             # Management Event & Audit Trail Verification
├── 08_EC2_Firewall_Auditor/         # Network Ingress & Security Group Risk Analysis
├── 09_Forensic_Logging/             # VPC Flow Logs & Network Traceability
├── 10_IAM_Identity_Auditor/         # MFA, Key Age & Credential Hygiene
├── 11_IAM_Identity_MFA_Key/         # Deep-dive MFA & Access Key Lifecycle Audit
├── 12_IAM_Password_Policy_Auditor/  # Account-level Password Complexity Audit
├── 13_IAM_Privilege_Auditor/        # Proactive: Static Configuration Risk Audit
├── 14_IAM_Privilege_Detector/       # Reactive: Real-time Escalation Vector Detection
├── 15_MITRE_ATTACK_Mapper/          # Threat Context & Tactic Correlation
├── 16_S3_Public_Access_Scanner/     # Data Leakage & Bucket Policy Auditor
└── 17_Sentinel_Cloud_Auditor/       # Unified Security Posture Dashboard & Reporting
🛠️ Tech Stack
Language: Python 3.10+

SDK: boto3 (AWS SDK for Python)

Standards: MITRE ATT&CK for Cloud, CIS AWS Foundations Benchmark

Compliance Readiness: HIPAA, SOC2, and PCI-DSS

👨‍💻 Author
Anuj Sharma Cloud Security Automation Enthusiast | DevSecOps Specialist | Python & Boto3 Expert
