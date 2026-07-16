# Security Portfolio — Deepak M

VAPT / offensive security portfolio documenting hands-on penetration testing work performed in isolated lab environments, alongside CTF writeups.

##  Disclaimer
All testing in this repository was performed against self-hosted, intentionally vulnerable systems (OWASP Juice Shop, Metasploitable2) or authorized CTF platforms (TryHackMe), within isolated lab environments. This work is for educational purposes only — none of it targets real-world, unauthorized systems.

## Projects

| Project | Target | Type | Key Findings | Report |
|---|---|---|---|---|
| OWASP Juice Shop VAPT | OWASP Juice Shop | Web Application (Black Box) | SQL Injection, XSS, IDOR, Information Disclosure, Input Validation | [Full report →](./owasp-juiceshop-vapt/) |
| Metasploitable2 VAPT | Metasploitable2 | Network / Host-based | vsftpd 2.3.4 Backdoor RCE (CVE-2011-2523, CVSS 9.8) | [Full report →](./metasploitable2-vapt/) |

## TryHackMe Writeups
Guided CTF-style writeups documenting enumeration and exploitation methodology across a range of rooms. See [`/writeups`](./writeups/) for the full index.

## Tools & Skills
- Kali Linux, Nmap, Burp Suite, Metasploit Framework, Searchsploit
- Manual-first enumeration methodology, automated tooling second
- Web application testing (OWASP Top 10), network/host penetration testing, Windows privilege escalation
- Working toward: eJPT (near-term), OSCP (18–24 months)

## About
Third-year IT student focused on offensive security / VAPT. This repo tracks hands-on lab work and CTF practice as part of an off-campus job search into penetration testing roles.
