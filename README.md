Web Application Security Assessment Using OWASP Juice Shop

Project Overview

This project presents a beginner-level security assessment of OWASP Juice Shop, an intentionally vulnerable web application designed for cybersecurity training and practice.

The purpose of this project is to explore common web application security vulnerabilities, perform controlled security tests, document observations, and provide recommendations to improve application security.

Objectives

* Understand common web application vulnerabilities.
* Perform controlled security testing in a local lab environment.
* Explore SQL Injection and Cross-Site Scripting (XSS).
* Use Burp Suite to inspect HTTP traffic.
* Document test results and security recommendations.

Tools and Technologies

* OWASP Juice Shop
* Burp Suite Community Edition
* Web Browser Developer Tools
* Docker
* macOS

Testing Environment

All testing activities were conducted against a locally running OWASP Juice Shop instance.

Target URL: http://localhost:3000

No third-party or production systems were tested.

Security Testing Summary

1. SQL Injection

A login test involving SQL Injection resulted in successful authentication.

Further documentation of the exact input and testing steps is required to make the result fully reproducible.

2. Cross-Site Scripting (XSS)

A JavaScript alert dialog was observed after submitting a crafted search input.

The exact execution context and XSS subtype have not yet been confirmed.

Tools Used for Analysis

Burp Suite was used to inspect application traffic. Browser Developer Tools were also used to examine application behavior.

Security Recommendations

* Use parameterized queries and prepared statements to prevent SQL Injection.
* Validate and sanitize untrusted input where appropriate.
* Encode output according to its context to reduce XSS risks.
* Avoid inserting untrusted data using unsafe HTML methods such as innerHTML.
* Apply a Content Security Policy (CSP) as an additional security layer.

Project Scope and Limitations

This assessment was conducted in a controlled local training environment using OWASP Juice Shop.

The findings are educational observations and should not be interpreted as confirmed vulnerabilities in a production system.

Repository Structure

* README.md: Project overview and summary.
* reports/assessment-report.md: Detailed security assessment report.
* evidence/README.md: Evidence documentation and checklist.

Disclaimer

This project was conducted for educational purposes only. All tests were performed on a deliberately vulnerable local application.
