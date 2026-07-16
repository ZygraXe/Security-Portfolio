# Metasploitable2 — VAPT Report

**Target:** Metasploitable2
**Assessment Type:** Network / Host-based Penetration Testing
**Tools:** Kali Linux, Nmap, Metasploit Framework, Searchsploit
**Environment:** Kali Linux ↔ Metasploitable2, NAT/Bridged network

> ⚠️ Testing was performed against Metasploitable2, an intentionally vulnerable virtual machine built for security training, in an isolated lab environment.

📄 [Full PDF report](./Metasploitable2-VAPT-Report.pdf)

## Objective
- Identify open ports and running services on the target
- Analyze discovered services for known vulnerabilities
- Exploit one critical vulnerability and verify impact
- Recommend mitigation measures

## Key Finding

**vsftpd 2.3.4 — Backdoor Command Execution**
- **CVE:** CVE-2011-2523
- **Severity:** Critical
- **CVSS v3.1:** 9.8 (`AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H`)
- **Exploit used:** `exploit/unix/ftp/vsftpd_234_backdoor`

## Methodology
1. **Recon:** Full TCP port scan (`nmap -p- -T4`) — 24 open ports identified
2. **Service/version detection:** `nmap -sC -sV -O` — vsftpd 2.3.4 flagged as outdated and vulnerable
3. **Enumeration:** FTP anonymous login attempted; no valid credentials found
4. **Vulnerability identification:** vsftpd 2.3.4 matched to known backdoor CVE
5. **Exploitation:** Metasploit module executed against target
6. **Post-exploitation:** Meterpreter shell obtained with root-level privileges, confirmed via `id`

## Impact
Full unauthorized remote access with root privileges — complete compromise of confidentiality, integrity, and availability on the target system.

## Evidence
Screenshots included for each stage: port scan, service detection, exploit execution, and shell access — see `/images` or the full PDF report.

## Key Takeaways
- Practiced the end-to-end VAPT lifecycle: recon → enumeration → exploitation → post-exploitation
- Reinforced the importance of patch management — this backdoor existed in a version released in 2011
