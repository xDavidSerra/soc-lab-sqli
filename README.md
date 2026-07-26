SOC Lab — SQL Injection Attack & Detection

A hands-on lab simulating a full security incident lifecycle: reconnaissance, exploitation, detection, and response — from both an attacker's and a SOC analyst's perspective.

Overview
Attacker machine: Kali Linux
Victim machine: Ubuntu + Docker running DVWA (Damn Vulnerable Web Application)
Network: Isolated NAT network
What was done
Reconnaissance — Nmap scan to identify exposed services on the victim
Exploitation (manual) — SQL Injection via a crafted payload (1' OR '1'='1) in the DVWA login form
Exploitation (automated) — Used sqlmap to dump the users table and crack extracted password hashes
Detection — Analyzed Apache/Docker logs to confirm the attack left a clear, identifiable trail
MITRE ATT&CK mapping — Mapped actions to T1190 (Exploit Public-Facing Application) and T1213 (Data from Information Repositories)
Report

Full write-up, including commands, screenshots, and mitigation recommendations: incident_report_final_en.pdf

Disclaimer

This project was carried out entirely in an isolated, self-hosted lab environment against an application (DVWA) intentionally built for security training. No real or third-party systems were involved.

Author: David Serra
