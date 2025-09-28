# Vulnerability Scan Report

**Project:** Basic Vulnerability Scan on Personal Computer  
**Scanner:** <REPLACE_WITH_NESSUS_OR_OPENVAS>  
**Target IP:** <REPLACE_WITH_TARGET_IP>  
**Scan Date:** <REPLACE_WITH_SCAN_DATE>  
**Author:** <REPLACE_WITH_YOUR_NAME>

---

## Executive Summary
Briefly: This report summarises the results of a basic vulnerability scan performed against the target host. The scan identified issues of varying severity; remediation steps are included for the most critical items.

## Scope and Objective
- **Objective:** Identify common vulnerabilities affecting the target system using automated vulnerability scanning tools (Nessus Essentials or OpenVAS/GVM).
- **Scope:** Single host: `<REPLACE_WITH_TARGET_IP>`; Unauthenticated/Authenticated scan: `<REPLACE>`.

## Tools and Versions
- Scanner: `<REPLACE_WITH_SCANNER_AND_VERSION>`
- Feed/update state: `<REPLACE_WITH_DATE_OR_FEED_STATUS>`

## Scan Configuration
- Scan type: Basic Network Scan / Full Scan
- Authentication: None / Windows Credentials (if used)
- Target: `<REPLACE_WITH_TARGET_IP>`
- Duration: `<REPLACE_WITH_DURATION>`

## Summary of Findings
- Total findings: `<REPLACE_TOTAL_COUNT>`
- Critical: `<COUNT>` | High: `<COUNT>` | Medium: `<COUNT>` | Low: `<COUNT>` | Info: `<COUNT>`

## Top 5 Vulnerabilities (summary)
| # | Vulnerability (CVE if available) | CVSS | Short description | Recommended remediation |
|---|---:|---:|---|---|
| 1 | `<CVE-YYYY-XXXX or title>` | `<score>` | `<short desc>` | `<fix/remediation>` |
| 2 | ... | ... | ... | ... |
| 3 | ... | ... | ... |
| 4 | ... | ... | ... |
| 5 | ... | ... | ... |

## Detailed Findings
> Copy each finding exported by the scanner. For each finding include:
- **Title:**  
- **CVE:**  
- **CVSS:**  
- **Description:**  
- **Evidence / Proof:** (screenshot file path e.g. `images/vuln_1.png`)  
- **Remediation / Mitigation:**  
- **References:**  

## Conclusion & Recommendations
- Immediate action items for Critical/High issues.
- Medium-term: schedule authenticated scans, patch management, limit services, enable host firewall, remove unused software.
- Longer-term: implement vulnerability management process, periodic scanning cadence (weekly/monthly as appropriate).

---

## Appendix
- Raw export: `scan_results.csv` (attach)
- Export PDF: `scan_report.pdf` (attach)
- Screenshots: `images/scan_overview.png`, `images/top_vulns.png`, `images/vuln_<id>.png`
