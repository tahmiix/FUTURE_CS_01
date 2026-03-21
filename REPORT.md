Future Interns Cybersecurity Report

Task 1: Web Application Security Assessment Report

Repository Name : FUTURE_CS_01

Candidate details
Name: Thamsanqa Gift Skenjana

Objective
To perform a security assessment on a locally hosted Multi-factor Authentication (MFA) web application using industry-
standard tools and identify potential vulnerabilities.

Tools used
  OWASP-ZAP
  NMAP

Target Application
URL:http://127.0.0.1:3000
Environment: Localhost
Application Type: MFA Authentication System

OWASP Scan Summary
The scan identified multiple low to medium risk vulnerabilities, primarily related to security misconfigurations and
missing HTTP headers

Vulnerabilities Identified:
1. Content Security Policy (CSP) Not Set
Risk Level: Medium
Description:
  The application does not define a Content Security Policy header, which increases the risk of Cross-Site Scripting
  (XSS) attacks.
Impact:
  Attackers may inject malicious scripts into web pages.
Recommendation:
  Content-Security-Policy: default-src 'self';

2. Missing Anti-Clickjacking Header
Risk Level: Medium
Description:
  The application is vulnerable to clickjacking due to absence of protection headers.
Impact:
  Users may unknowingly interact with hidden malicious elements.
Recommendation:
  X-Frame-Options: DENY

3. X-Content-Type-Options Header Missing
Risk Level: Low
Description:
  The browser may MIME-sniff responses, increasing exposure to attacks.
Recommendation:
  X-Content-Type-Options: nosniff

4. Server Information Disclosure
Risk Level: Low
Description:
The response header exposes server technology:
  X-Powered-By: Express
Impact:
  Attackers can tailor exploits based on known vulnerabilities.
Recommendation:
  Disable this header in your backend:
  app.disable('x-powered-by');

5. Cross-Domain Misconfiguration
Risk Level: Medium
Description:
  The application allows all origins:
  Access-Control-Allow-Origin: *
Impact:
  Unauthorized domains can interact with your API.
Recommendation:
Restrict allowed origins:
  Access-Control-Allow-Origin: http://trusted-domain.com

Nmap Scan Summary
Open ports identified:
  3000 (Web Application)
  3306 (MySQL Database)
  No immediate critical vulnerabilities detected at the network level.

MFA-Specific Security Testing
Additional manual testing was performed on the authentication system:
  Login functionality works as expected
  Potential lack of OTP rate limiting
  OTP reuse should be restricted
  No visible brute-force protection mechanisms

🛡 Recommendations
  Implement HTTP security headers
  Add rate limiting on login and OTP endpoints
  Enforce OTP expiration and one-time usage
  Restrict CORS policy
  Hide server technology stack
  Implement logging and monitoring
  
Conclusion
  The MFA web application demonstrates a solid functional foundation but requires improvements in security
  configuration and hardening.
  Addressing the identified vulnerabilities will significantly enhance the application's resilience against common web-
  based attacks.
