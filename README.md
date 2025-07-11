# Log Ingestor – Distributed Log Management System

Log Ingestor is a PostgreSQL-based project that enables scalable ingestion, analysis, and monitoring of log data across distributed server environments. Built as part of the IT214 (Database Management Systems) course, it addresses the real-world challenges of managing diverse and high-volume logs in cloud-native infrastructures.

## Objective

To design and implement a sharded database system for efficiently ingesting logs from multiple servers, while ensuring quick querying, structured storage, and use-case-specific analysis for developers, security teams, and administrators.

## Features

- Sharded Schema Design: Logs are divided server-wise into smaller, manageable table sets (log shards).
- Cluster Table: Central metadata table tracking each server's ID, IP, log format, and provider.
- Structured Logging: Tables for server logs, application logs, security events, and production logs per server.
- Log Format Mapping: Each server uses a consistent log format (CLF, ELF, Syslog, JSON, etc.) based on its service provider (e.g., AWS, Apache, Kubernetes).
- Fully Normalized: Schema adheres to BCNF for all relations with detailed functional dependency proofs.
- Query Optimized: Analytical queries support use cases like crash analysis, brute-force detection, and cost auditing.

## Project Structure

| File | Description |
|------|-------------|
| `1_ERD_Schema_FDs.pdf` | ER diagram, Relational Schema and functional dependencies |
| `2_DDL_Script.txt` | SQL script to create all tables and schema |
| `3_INSERT_Script.txt` | Sample data for logs across all log types |
| `4_Queries.txt` | Analytical SQL queries for key use cases |
| `Report.pdf` | Full project report with objectives, formats, and use cases |

## Use Case Scenarios

### System Administrators
- Monitor server health (CPU, memory, disk usage)
- Detect system crashes
- Track session-based cost and billing

### Company Administrators
- Analyze server traffic growth and campaign impact
- Estimate cloud usage cost and optimize server deployment

### Security Analysts
- Identify unauthorized access and failed logins
- Detect DDoS attacks and IP-based threats
- Monitor suspicious firewall and VPN activity

### Developers & DevOps Engineers
- Analyze API usage and response behavior
- Detect code failures via production logs
- Optimize microservice performance

## Sample SQL Queries

- Server health classification
- Peak hour traffic analysis
- System crash detection
- Server-wise cost summary
- Brute-force attack detection
- Cross-server access by the same IP
- Average system uptime calculation
- Application-security log correlation
- Resource usage trends per session
- Spike detection in CPU/memory usage

(Refer to `Queries.txt` for full list.)

## Team Members

- Jevik Rakholiya – 202301276  
- Dhruv Jain – 202301272  
- Rujal Jiyani – 202301277

## Course Information

IT214 – Database Management Systems  
Instructor: Prof. P. M. Jat  
Dhirubhai Ambani Institute of Information and Communication Technology (DAIICT)

