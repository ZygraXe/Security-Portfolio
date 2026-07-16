# OWASP Juice Shop — VAPT Report

**Target:** OWASP Juice Shop
**Assessment Type:** Black Box Web Application Penetration Testing
**Environment:** Kali Linux (VMware)
**Date:** July 6, 2026

> ⚠️ Testing was performed against a self-hosted instance of OWASP Juice Shop, an intentionally vulnerable application built for security training. No real-world systems were involved.

📄 [Full PDF report](./OWASP-JuiceShop-VAPT-Report.pdf)

## Objective
Perform a black-box penetration test against OWASP Juice Shop to identify common web application vulnerabilities, following OWASP Top 10 methodology.

## Findings Summary

| # | Finding | Severity | CVSS v3.1 |
|---|---|---|---|
| 1 | SQL Injection in Login Page | Critical | 9.8 |
| 2 | Cross-Site Scripting (XSS) in Product Search | Medium | — |
| 3 | Information Disclosure via robots.txt | Low | — |
| 4 | Insecure Direct Object Reference (IDOR) in Cart | High | — |
| 5 | Improper Input Validation in Product Quantity | Medium | — |

*(See full report for CVSS vectors, reproduction steps/payloads, and remediation per finding. Fill in remaining CVSS scores to match Finding 1's format.)*

## Methodology
Reconnaissance → manual testing of authentication, search, cart, and product endpoints → payload crafting and validation via Burp Suite → impact analysis and remediation recommendations.

## Evidence
Each finding is documented with screenshots covering the vulnerable field, Burp Suite request/response, and payload used — see `/images` or the full PDF report.

## Key Takeaways
- Practiced systematic identification of OWASP Top 10 vulnerability classes in a black-box setting
- Reinforced parameterized queries, output encoding, and server-side validation as core remediations across nearly every finding
