# Web Application VAPT using Burp Suite and OWASP Juice Shop

## Project Overview
This project demonstrates manual Web Application Vulnerability Assessment and Penetration Testing on OWASP Juice Shop using Burp Suite Community Edition.

## Lab Setup
- Vulnerable Application: OWASP Juice Shop
- Tool: Burp Suite Community Edition
- Browser: Firefox
- Platform: VMware Workstation
- OS: Debian/Kali Linux

## Vulnerabilities Tested
- Authentication Testing
- SQL Injection
- Cross-Site Scripting (XSS)
- IDOR
- Broken Access Control
- Security Misconfiguration
- SSRF Testing
- API Enumeration

## Methodology
1. Configured Burp Suite proxy with Firefox.
2. Intercepted HTTP requests and responses.
3. Analyzed login, profile, basket, search, and API endpoints.
4. Used Burp Repeater for manual request manipulation.
5. Documented vulnerabilities with screenshots and remediation.

## Key Findings
### 1. Reflected XSS
A reflected XSS payload was tested in the search functionality.

### 2. IDOR
The basket endpoint was tested by modifying object identifiers in Burp Repeater.

### 3. Security Misconfiguration
The `/ftp` directory was publicly accessible and exposed backup/internal files.

### 4. API Documentation Exposure
Swagger API documentation was publicly accessible at `/api-docs`.

### 5. SSRF Testing
The profile image URL functionality was tested for SSRF. No confirmed SSRF vulnerability was identified.

## Tools Used
- Burp Suite Proxy
- Burp Repeater
- Firefox
- OWASP Juice Shop
- VMware Workstation

## Skills Learned
- HTTP request/response analysis
- Manual web application testing
- Burp Suite usage
- OWASP Top 10 testing
- API security testing
- Vulnerability documentation

## Disclaimer
This project was performed in a controlled lab environment using OWASP Juice Shop for educational purposes only.
