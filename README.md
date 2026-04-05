🔐 FUTURE_CS_01 – MFA Web Application Security Assessment
📌 Overview

This repository contains the submission for Future Interns Cyber Security Track (CS) – Task 1.

The project focuses on performing a security assessment of a locally developed Multi-Factor Authentication (MFA) web application using industry-standard tools.

🎯 Objectives

Perform vulnerability scanning on a web application

Identify security misconfigurations

Analyze risks and impacts

Provide remediation recommendations

Document findings professionally

🛠️ Tools Used

OWASP ZAP (Web Application Security Scanner)

Nmap (Network Scanning Tool)

🌐 Target Application

App Type: MFA Authentication System

Environment: Localhost

URL: http://127.0.0.1:3000

🔗 MFA Application Repository

👉 https://github.com/tahmiix/mfa-authentication-demo

🚨 Key Findings

Vulnerability	Risk Level

Missing Content Security Policy	Medium

Missing Anti-Clickjacking Header	Medium

X-Content-Type-Options Missing	Low

Server Information Disclosure	Low

CORS Misconfiguration	Medium

🛡️ Recommendations

Implement security headers (CSP, X-Frame-Options, etc.)

Restrict CORS policy

Disable X-Powered-By header

Add rate limiting on authentication endpoints

Enforce OTP expiration and one-time use

Implement logging and monitoring


Detailed findings are available in:

REPORT.md

📈 Skills Demonstrated

Web Application Security Testing

Vulnerability Analysis

Security Misconfiguration Detection

Use of Industry Tools

Technical Documentation

⚠️ Disclaimer

This project was conducted in a controlled environment for educational purposes only.

👨‍💻 Author

Thamsanqa Gift Skenjana

⭐ Acknowledgement

This project aligns with best practices from OWASP standards for web security testing.

