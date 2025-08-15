# Cybersecurity-Internship---Task-3
PC Security Assessment
Overview
This project documents the results of a comprehensive vulnerability scan performed on my local machine using Tenable Nessus Essentials, as part of Task 3 of my cybersecurity internship with Elevate Labs under the Ministry of MSME, Government of India.

📋 Objective
Use free vulnerability scanning tools to identify common security vulnerabilities on a personal computer

Gain hands-on experience with professional cybersecurity assessment tools

Document findings and develop remediation strategies

🛠️ Tools Used
Tenable Nessus Essentials (Version 10.9.2)

Target System: Windows x86_64 localhost (127.0.0.1)

Scan Policy: Basic Network Scan

CVSS Version: 3.0

🔍 Methodology
1. Tool Installation & Setup
Downloaded and installed Nessus Essentials from Tenable

Registered for free activation code

Completed initial setup and plugin compilation

Configured local scanner with admin credentials

2. Scan Configuration
Scan Name: PC Security Assessment

Target: localhost (127.0.0.1)

Scan Type: Basic Network Scan (unauthenticated)

Scan Duration: 12 minutes (6:24 PM - 6:36 PM)

Authentication: Failed (limited credential access)

3. Execution Process
Initiated full vulnerability scan targeting local machine

Monitored scan progress through Nessus web interface

Documented scan completion and results export

📊 Results Summary
Based on the completed vulnerability scan, the following security issues were identified:

Vulnerability Breakdown
Severity Level	Count	Description
Critical	0	No critical vulnerabilities detected
High	0	No high-risk vulnerabilities found
Medium	1	SMB Signing not required (CVSS 5.3)
Low	0	No low-severity issues
Info	22+	Informational findings (ports, services, SSL)
Key Findings
🔴 Medium Severity (CVSS 5.3)
SMB Signing Not Required

Impact: Man-in-the-middle attacks possible on SMB traffic

Affected Service: NetBIOS/SMB (Port 139, 445)

Recommendation: Enable SMB signing in Windows security policy

🔵 Informational Findings
Open Ports Detected: 29 ports identified via Netstat scanner

Port 135 (RPC Endpoint Mapper)

Port 139 (NetBIOS Session Service)

Port 445 (SMB/CIFS)

Port 8834 (Nessus Web Interface)

Various dynamic RPC ports (49000+ range)

SSL/TLS Issues: 4 SSL-related informational findings

Service Detection: Windows services and web servers identified

Platform Recognition: Microsoft Windows system detected

🛡️ Security Recommendations
Immediate Actions
Enable SMB Signing

Navigate to Local Security Policy → Local Policies → Security Options

Enable "Microsoft network client: Digitally sign communications"

Enable "Microsoft network server: Digitally sign communications"

General Security Improvements
Port Management

Review and close unnecessary open ports

Configure Windows Firewall rules for essential services only

Service Hardening

Disable unused Windows services

Implement principle of least privilege

Regular Updates

Ensure Windows Update is enabled and current

Keep all installed software updated

📁 Repository Structure
text
vulnerability-scan-task3/
├── README.md                          # This documentation file
├── scan-results/
│   └── PC-Security-Assessments.nessus # Raw Nessus scan export (XML)
├── screenshots/
│   ├── nessus-dashboard.jpg           # Main scan results view
│   ├── scan-configuration.jpg         # Scan setup and configuration
│   ├── vulnerability-details.jpg      # Detailed vulnerability listing
│   └── scan-completion.jpg            # Scan completion status
└── documentation/
    └── methodology.md                 # Detailed scan methodology
📸 Evidence Documentation
Screenshot 1: Nessus scan dashboard showing completed assessment

Screenshot 2: Vulnerability breakdown by severity levels

Screenshot 3: Detailed vulnerability listings and CVSS scores

Screenshot 4: Scan configuration and target settings

🎯 Learning Outcomes
Technical Skills Gained
Vulnerability Assessment: Hands-on experience with enterprise security scanning

Risk Analysis: Understanding CVSS scoring and vulnerability prioritization

Tool Proficiency: Practical knowledge of Nessus Essentials

Security Documentation: Professional reporting and remediation planning

Key Concepts Mastered
Vulnerability Scanning vs Penetration Testing: Automated identification vs manual exploitation

CVSS Framework: Common Vulnerability Scoring System (0-10 scale)

False Positive Management: Distinguishing real threats from scanning artifacts

Risk Prioritization: Severity-based remediation planning

💡 Interview Preparation Answers
1. What is vulnerability scanning?
Vulnerability scanning is an automated security assessment process that systematically examines systems, networks, and applications to identify potential security weaknesses before they can be exploited by attackers.

2. Difference between vulnerability scanning and penetration testing?
Vulnerability Scanning: Automated, broad coverage, identifies potential weaknesses

Penetration Testing: Manual, targeted, actively exploits vulnerabilities to prove impact

3. What are some common vulnerabilities in personal computers?
Unpatched software and operating systems

Weak or default credentials

Unnecessary open ports and services

Missing security configurations (like SMB signing)

Outdated SSL/TLS implementations

4. How do scanners detect vulnerabilities?
Scanners use multiple detection methods:

Banner grabbing: Identifying software versions

Port scanning: Finding open network services

Signature matching: Comparing against known vulnerability databases

Configuration checks: Verifying security settings

5. What is CVSS?
The Common Vulnerability Scoring System (CVSS) is a standardized framework for rating vulnerability severity on a scale of 0-10, considering factors like exploitability, impact, and environmental characteristics.

6. How often should vulnerability scans be performed?
Critical systems: Weekly to monthly

General infrastructure: Monthly to quarterly

After major changes: Immediately following updates or configuration changes

7. What is a false positive in vulnerability scanning?
A false positive occurs when a scanner incorrectly identifies a security issue that doesn't actually exist, often due to limited context or access during automated testing.

8. How do you prioritize vulnerabilities?
Prioritization should consider:

CVSS score (severity level)

Asset criticality (importance of affected system)

Exploitability (ease of attack)

Business impact (potential consequences)

Available patches (remediation feasibility)

🔗 Additional Resources
Tenable Nessus Documentation

NIST Vulnerability Management Guide

CVSS Calculator

Project Completed: August 11, 2025
Scan Duration: 12 minutes
Total Vulnerabilities Found: 23
Critical/High Risk Issues: 0
Medium Risk Issues: 1

This assessment was conducted as part of the cybersecurity internship program with Elevate Labs, supported by the Ministry of MSME, Government of India.
