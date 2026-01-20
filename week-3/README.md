Advanced Exploitation & Web Security Practical Lab
Overview

This repository demonstrates a complete end-to-end cybersecurity practical covering exploitation, web application testing, reporting, post-exploitation, and evidence collection workflows. It simulates a realistic penetration testing scenario using offensive security tooling and industry methodologies.

1. Advanced Exploitation Lab
Activities

Chained exploits using Metasploit

Python PoC customization (from Exploit-DB)

Documentation and reporting

Exploit Chain
Exploit ID	Description	Status	Payload
004	XSS to RCE Chain	Success	Meterpreter
Python PoC Customization (Summary)

Modified an Exploit-DB Python PoC for a Git-based CVE by adjusting request parameters, updating payload execution logic, and fixing encoding issues for stable remote execution. Improved reliability and added basic exception handling. (~50 words)

Findings

CVE Identified: CVE-2021-22205

Host Impacted: Web server with file upload & image processing abuse

Remediation

Input sanitization

Secure upload validation

Update vulnerable Git-based service

2. Web Application Testing Lab
Activities

OWASP Top 10 testing simulations

Burp Suite interception and manipulation

SQL injection automation & manual XSS testing

Testing Log
Test ID	Vulnerability	Severity
001	SQL Injection	Critical
002	XSS Reflected	Medium
Checklist

 SQL Injection (sqlmap)

 XSS payload testing (manual)

 Session manipulation (Burp Suite)

 Authentication verification

 Optional scripting

Web Testing Summary (50 words)

Performed a focused application assessment targeting OWASP Top 10 weaknesses using automated and manual tooling. Successfully validated SQL injection and reflected XSS paths, confirmed session-related attack surfaces, and identified insecure input handling. Results demonstrate insufficient validation and weak trust boundaries within the tested application.

3. Reporting Practice
Report Template Sections

Executive Summary

Technical Findings

Remediation Plan

Findings Table
Finding ID	Vulnerability	CVSS Score	Remediation
F001	SQL Injection	9.1	Input validation
F002	Weak Password	7.5	Enforce complexity
Visualization

Network attack path diagram produced using Draw.io to illustrate lateral movement and exploitation phases.

Non-Technical Brief (100 words)

A simulated assessment identified critical weaknesses enabling unauthorized data access and remote execution. Attack chains demonstrated how a web-based flaw can escalate into system compromise without user interaction. Key risks relate to insufficient input validation, weak access controls, and outdated components. Recommended fixes include patching, enforcing strong authentication, and implementing secure development practices. Improving visibility and monitoring would reduce future exposure.

4. Post-Exploitation & Evidence Collection
Activities

Privilege escalation via Metasploit

Traffic capture via Wireshark

File acquisition and hashing for chain-of-custody

Evidence Log
Item	Description	Collected By	Date	Hash Value
Traffic Log	HTTP Traffic	Analyst	2026-01-12	SHA256
Evidence Collection Summary 

Collected and preserved network traffic and system artifacts for forensic review. Maintained hash-based integrity verification to support admissibility and reproducibility. Ensured consistent chain-of-custody and documentation throughout post-exploitation.

5. Capstone: Full VAPT Cycle
Activities

Full penetration test simulation

Exploitation via Metasploit

Detection via OpenVAS

Remediation & rescan validation

OpenVAS Detection Log
Timestamp	Vulnerability	PTES Phase
2026:14:01	Drupal RCE	Exploitation
PTES Report (200 words)

Performed a simulated PTES-aligned penetration test against a Linux-based VM environment. Reconnaissance identified exposed web services, outdated components, and weak authentication surfaces. Exploitation succeeded via a public RCE vulnerability, enabling system-access and partial persistence. Vulnerability scanning confirmed configuration and patching lapses. Remediation focused on patch cycles, input validation, and credential hygiene. Final rescan validated reductions in attack surface and confirmed resolution of high-risk findings. Overall, the assessment demonstrated realistic impact, adversarial chaining, and systemic shortcomings in patch management.

Manager Brief 
The assessment revealed critical weaknesses that could allow attackers to compromise the system. Exploits were successfully demonstrated using publicly available tools, indicating low barriers to real-world exploitation. Recommended actions include patching outdated services, enforcing strong access controls, and improving monitoring to detect malicious activity. Security improvements should be prioritized due to demonstrated risk.

Tools Used

Metasploit Framework

Python

Exploit-DB

Burp Suite

sqlmap

OWASP ZAP

Draw.io

Wireshark

OpenVAS

Kali Linux

Methodologies

PTES

OWASP Top 10

Vulnerability Scanning
