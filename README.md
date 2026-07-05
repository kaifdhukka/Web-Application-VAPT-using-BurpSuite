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

# Screenshots

## 1. Burp Proxy Intercept
![Burp Proxy](Screenshots/01-Burp-Proxy-Intercept-Request.jpeg)

---

## 2. HTTP History
![HTTP History](Screenshots/02-Burp-HTTP-History-Overview.jpeg)

---

## 3. Failed Login (401 Unauthorized)
![Failed Login](Screenshots/03-Burp-Failed-Login-401-Unauthorized.jpeg)

---

## 4. Successful Login (JWT Response)
![Successful Login](Screenshots/04-Burp-Successful-Login-JWT-Token.jpeg)

---

## 5. XSS Payload Injection
![XSS Payload](Screenshots/05-XSS-Payload-Entered.jpeg)

---

## 6. XSS Successfully Executed
![XSS Executed](Screenshots/06-XSS-Alert-Executed.jpeg)

---

## 7. IDOR Request Manipulation
![IDOR Request](Screenshots/07-IDOR-Basket-Request-Manipulation.jpeg)

---

## 8. IDOR Response
![IDOR Response](Screenshots/08-IDOR-Basket-Response-Data.jpeg)

---

## 9. robots.txt Information Disclosure
![robots.txt](Screenshots/09-Robots.txt-Disclosure.jpeg)

---

## 10. Public FTP Directory Listing
![FTP Directory Listing](Screenshots/10-FTP-Directory-Listing-Exposed-Files.jpeg)

### FTP Exposed Files
![FTP Exposed Files](Screenshots/10-FTP-Directory-Listing-Exposed-Files1.jpeg)

---

## 11. Swagger API Documentation Exposure
![Swagger API](Screenshots/11-Swagger-API-Documentation-Exposure.jpeg)

---

## 12. SSRF Image URL Request
![SSRF Request](Screenshots/12-SSRF-Image-URL-Request.jpeg)

---

## 13. SSRF Test Response (302 Redirect)
![SSRF Response](Screenshots/13-SSRF-Response-No-Vulnerability.jpeg)
