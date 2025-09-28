# Basic Vulnerability Scan - Deliverables

**Objective:** Perform a basic vulnerability scan of your PC using free tools (Nessus Essentials or OpenVAS/GVM), collect screenshots, and produce a scan report suitable for submission or upload to GitHub.

---

## What I include in this repo (copy-paste ready)
- `REPORT.md` — Ready-to-use vulnerability scan report template (fill placeholders).
- `README.md` — (this file) instructions to run a basic scan and capture evidence.
- `INTERVIEW_QA.md` — Short answers to common interview questions included in the task PDF.
- `scan_results_example.csv` — Example CSV with how to record results.
- `images/placeholder_scan_overview.png` — Placeholder image (replace with your real screenshots).
- `images/placeholder_vuln_details.png` — Placeholder image (replace with your real screenshots).

---

## Quick step-by-step (GUI-focused, Windows-first)

### Option A — **Nessus Essentials (recommended on Windows)**
1. Visit Tenable and register for **Nessus Essentials** (free). Obtain your activation code and download the Windows installer. (Tenable docs: official Tenable installation steps.) citeturn0search16
2. Run the downloaded installer and follow the InstallShield wizard. When finished, open the Nessus web console (usually `https://localhost:8834`). citeturn0search0
3. Register/activate Nessus using the activation code sent to your email. Create an account and log in. citeturn0search16
4. Create a new scan using the **Basic Network Scan** template:
   - Name: `Localhost Scan - <your_name_or_id>`
   - Targets: use `127.0.0.1` or your machine's local IP (run `ipconfig` if unsure).
   - Save & Launch the scan.
5. Let the scan run. Typical duration: **5–60 minutes** depending on system and plugin updates. Monitor progress in the web UI. citeturn0search5
6. When complete, export the scan results as **PDF** and **CSV** (Nessus UI: export options). Save these into this repo as `scan_report_<date>.pdf` and `scan_results.csv`.
7. Take screenshots of:
   - The scan summary/dashboard (Exposure overviews).
   - The "Top Vulnerabilities" list with CVSS scores.
   - One or two detailed vulnerability pages (expand a finding to show details).
   Save screenshots to `images/` and name them `scan_overview.png`, `top_vulns.png`, `vuln_<id>.png`.

### Option B — **OpenVAS / GVM (Linux or VM)**
1. OpenVAS/GVM requires a Linux environment (it does **not** natively run on Windows). Use a Linux VM (Ubuntu/Kali) or the Greenbone virtual appliance; you can also run it in WSL2/docker with advanced setup. citeturn0search7turn0search4
2. Install GVM/OpenVAS (or deploy Greenbone VM), start the web UI (Greenbone Security Assistant), create a Target containing `127.0.0.1` or the VM IP, then create a Task using a basic/full scan config, and run it. Greenbone's docs explain configuring and running scans. citeturn0search9turn0search17
3. Export results (PDF/CSV) and take the same screenshots as listed for Nessus.

---

## What to include in `REPORT.md` (already prepared in this repo — fill placeholders)
- Title, Date, Scanner used, Target IP, Duration, Executive summary (1–3 lines)
- Methodology (scan type, authenticated/unauthenticated)
- Findings summary (total issues by severity), Top 5 issues (CVE/CVSS/Description/Remediation)
- Detailed findings (with references)
- Conclusion and recommendations
- Appendix: raw export files and screenshots

## About CVSS (how to prioritise)
CVSS gives a numeric score (0–10) and qualitative severity (Low/Medium/High/Critical). Use CVSS to prioritise remediation but also consider exploitability, asset importance, and exposure. (See FIRST / NVD documentation.) citeturn0search1turn0search15

---

## How to capture screenshots on Windows (GUI methods)
- Press **Win + Shift + S** to open the Snip & Sketch tool, then draw a rectangle and paste into Paint or directly save.
- Or open **Snipping Tool** → New → Save.
- Save files into `images/` folder and use names suggested above.

---

## How to upload to GitHub (quick, using GitHub web UI)
1. Create a new repository on GitHub (click "Create repository").
2. Drag-and-drop the files/folders from your local machine to the web UI (or upload zipped folder).
3. Write a commit message and commit the upload.
(If you prefer `git` CLI, you can `git init`, `git add .`, `git commit -m "Add scan report"`, `git remote add origin <URL>`, `git push -u origin main`.)

---

## Files in this repository (already created for you)
- `REPORT.md` (fill in)
- `INTERVIEW_QA.md` (answers to interview questions)
- `scan_results_example.csv` (example)
- `images/*.png` (placeholders — replace with your screenshots)

---

### Need these details from you to fully personalise the report:
1. Which scanner did you use? **Nessus Essentials** or **OpenVAS/GVM**?
2. Your OS (Windows 10/11, Linux distro), and whether you ran the scanner locally or inside a VM.
3. Target IP used in scan (e.g., `127.0.0.1` or `192.168.x.x`)
4. Desired report author name & GitHub repo name (for README metadata).
5. If you want me to pre-fill the Top 5 vulnerabilities with generic mitigation text or make them specific, share the exported CSV or PDF results (you can paste text or upload files).

If you want, I already generated a downloadable repo bundle with templates and **placeholder screenshots** — see links below.
