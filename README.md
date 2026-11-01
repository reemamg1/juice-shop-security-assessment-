
<div align="center">

# 🛡️ Web Application Security Assessment

### OWASP Juice Shop | Cybersecurity Project

**A Practical Security Testing & Vulnerability Analysis Project**

<br>

![Security](https://img.shields.io/badge/Domain-Web%20Application%20Security-blue)
![Testing](https://img.shields.io/badge/Testing-OWASP%20Juice%20Shop-orange)
![Tool](https://img.shields.io/badge/Tool-Burp%20Suite-purple)
![Status](https://img.shields.io/badge/Status-Completed%20Initial%20Assessment-success)

</div>

---

## 📌 About The Project

This project presents a practical security assessment of **OWASP Juice Shop**, an intentionally vulnerable web application developed for cybersecurity education and training.

The assessment focuses on exploring common web application vulnerabilities, analyzing HTTP traffic, documenting security observations, and identifying appropriate mitigation techniques.

## 🎯 Objectives

- Identify and explore common web application vulnerabilities.
- Perform SQL Injection (SQLi) testing.
- Investigate Cross-Site Scripting (XSS).
- Analyze HTTP requests and responses.
- Document findings and recommend security improvements.

## 🧰 Tools & Technologies

| Tool | Purpose |
|:---|:---|
| OWASP Juice Shop | Vulnerable testing application |
| Burp Suite Community Edition | HTTP traffic inspection |
| Browser Developer Tools | Browser-side analysis |
| Docker | Local lab environment |
| macOS | Operating system |

## 🔍 Security Assessment Findings

| Test | Observation | Status |
|:---|:---|:---|
| SQL Injection | Successful authentication observed during login testing | Observed |
| XSS | JavaScript alert dialog appeared after search input | Observed |
| HTTP Analysis | Login request and HTTP 200 response captured | Completed |

### 01 — SQL Injection (SQLi)

A login test involving SQL Injection resulted in successful authentication.

**Security Recommendation:**
- Use parameterized queries.
- Implement prepared statements.
- Apply least-privilege database permissions.

### 02 — Cross-Site Scripting (XSS)

A JavaScript alert dialog was observed after submitting a crafted search input.

**Security Recommendation:**
- Implement context-aware output encoding.
- Avoid unsafe HTML insertion.
- Use safe DOM manipulation methods.

### 03 — HTTP Traffic Analysis

Burp Suite Community Edition was used to inspect application traffic.

A `POST` request to `/rest/user/login` was captured, and the server returned `HTTP/1.1 200 OK`.

**Security Recommendation:**

Review request handling, response headers, and authentication mechanisms.

---

## 📸 Evidence & Screenshots

View the documented testing evidence below:

| Evidence | Description |
|:---|:---|
| [SQL Injection Screenshot](evidence/sqli-login-test.png) | Login test observation |
| [XSS Screenshot](evidence/xss-alert-test.png) | JavaScript alert observation |
| [Burp Suite Screenshot](evidence/burp-traffic-analysis.png) | HTTP request and response analysis |

📁 [View All Evidence](evidence/README.md)

## 📄 Detailed Report

For the complete assessment methodology, findings, limitations, and recommendations:

**[View Security Assessment Report →](reports/assessment-report.md)**

---

## 🧪 Testing Environment

| Configuration | Details |
|:---|:---|
| Target | OWASP Juice Shop |
| URL | `http://localhost:3000` |
| Environment | Local Testing Lab |
| Operating System | macOS |
| Proxy Tool | Burp Suite Community Edition |

## ⚠️ Scope & Disclaimer

All testing activities were conducted against a locally running instance of OWASP Juice Shop.

This project is intended strictly for educational purposes. No third-party or production systems were tested.

The documented observations are preliminary and do not represent a comprehensive security audit.

---

<div align="center">

**Cybersecurity | Web Application Security | Vulnerability Assessment**

</div>

This project was conducted for educational purposes only. All tests were performed on a deliberately vulnerable local application.
