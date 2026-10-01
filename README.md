# NETWORKWALKS-NGOR-B083-WK4-PENETRATION-TESTING-PROJECT
# Penetration Testing Report: Mediroza General Hospital

# 01. Executive Summary

This report details the findings of the comprehensive security penetration testing engagement conducted against MediRoza General Hospital. The assessment evaluated the organization's overall security posture through structured, authorized testing procedures (Milestone 4).The primary objective was to identify exploitable vulnerabilities, validate the security controls protecting critical assets, and provide clear remediation guidance

# Key Findings and Risk Overview

Overall Risk Level: High

Total Vulnerabilities Identified: Multiple critical and medium-severity issues spanning information leakage, weak authentication pathways, and web application vulnerabilities.

Impact: Successful exploitation of these findings could allow malicious actors to perform unauthorized reconnaissance, bypass authentication controls, or access sensitive patient health data.

# 02. Scope and Methodology

## Scope ##

👁️ Target: MediRoza General Hospital Web Infrastructure ([https://medirozahospital.com](https://medirozahospital.com))

✍️ Engagement Type: Black-box / Authorized Web Application Penetration Test

✔️ Environment: Controlled simulation environment conducted for educational and security hardening purposes.

# Methodology

The assessment followed an industry-standard structured methodology aligned with the project milestones:
1. Reconnaissance & Footprinting: Gathering target information, mapping directories, and identifying active services.
   
2. Vulnerability Assessment: Scanning for known application flaws, misconfigurations, and weak credential practices (utilizing tools such as Nmap, John the Ripper, and Burp Suite).

3. Exploitation & Validation: Simulating real-world attack vectors to verify vulnerabilities without causing system disruption.
  
4. Reporting: Documenting findings, risk ratings, and actionable remediation steps.

# 03. Findings and Proof of Exploitation

🗝️ Finding 1: Information Disclosure via Open Directories and Port Scanning

Description: Reconnaissance phases exposed unauthenticated directories and unnecessary open ports containing server version details and sensitive administrative patterns.

Evidence: Nmap and directory brute-forcing tools mapped hidden folders revealing application structural components.

<img width="701" height="453" alt="image" src="https://github.com/user-attachments/assets/08568aab-e987-400d-b1fa-a1e41410a618" />

<img width="697" height="421" alt="image" src="https://github.com/user-attachments/assets/a0c37f7a-f59d-4c04-b3a3-3bf50ac47f8d" />

<img width="686" height="241" alt="image" src="https://github.com/user-attachments/assets/94893c1d-ba4e-4d6b-a7f1-84c032957b47" />


🗝️ Finding 2: Weak Password Policies and Credential Exposure

Description: Assessment of sample credential hashes and login forms indicated vulnerability to dictionary and brute-force attacks (leveraging tools like John the Ripper and custom wordlists).

<img width="668" height="392" alt="image" src="https://github.com/user-attachments/assets/3ec55a43-9594-4d91-b536-8b4b1959ce46" />

<img width="658" height="394" alt="image" src="https://github.com/user-attachments/assets/de01303c-3e81-4ec3-8227-628c8691b1b3" />

<img width="659" height="403" alt="image" src="https://github.com/user-attachments/assets/77cf2d74-2aaa-47a4-aed9-9b920b4a65d3" />


Evidence: Weak administrative and user passwords were successfully cracked within minimal timeframes during simulated offline authentication audits.

<img width="347" height="488" alt="image" src="https://github.com/user-attachments/assets/bd72379a-c9bb-441d-addc-6dc543407bdd" />

<img width="335" height="473" alt="image" src="https://github.com/user-attachments/assets/a9369c5d-0958-4876-9892-96559a00cb13" />

<img width="325" height="461" alt="image" src="https://github.com/user-attachments/assets/5304db04-4312-42c0-8726-2722b444ad96" />


 🗝️ Finding 3: Web Application Input Validation Flaws

Description: Specific parameters lacked proper sanitization, presenting potential pathways for injection attacks and application-level logic abuse.

Evidence: Interception via Burp Suite confirmed improper handling of crafted HTTP inputs.



04. Risk Rating
  
   Vulnerabilities discovered during the engagement are categorized based on their severity and potential business impact:
   
 <img width="1017" height="373" alt="image" src="https://github.com/user-attachments/assets/e0831e3b-eacf-49b1-81dd-8a8f1be83a6c" />

   
   05. Recommendations and Remediation
     
To mitigate the identified risks and secure MediRoza General Hospital’s infrastructure, the following actionable steps are recommended:

1. Enforce Robust Authentication Policies: Implement strict password complexity requirements (minimum length, mixed characters, special symbols) and integrate multi-factor authentication (MFA) across all administrative portals.

2. Harden Web Applications & Input Filtering: Implement rigorous server-side input validation and parameter sanitization to neutralize injection attacks. Disable verbose error messages and directory listing on production web servers.

3. Continuous Monitoring & Log Reviews: Deploy Web Application Firewalls (WAF) and real-end monitoring tools to detect brute-force attempts and anomalous HTTP traffic patterns promptly.
   
4. Regular Security Assessments: Schedule routine vulnerability scans and periodic third-party penetration tests to maintain security hygiene.
