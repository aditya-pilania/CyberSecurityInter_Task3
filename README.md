# 🛡️ Task 3 - Vulnerability Scan Report

## 🎯 Objective
Perform a basic vulnerability assessment using **OpenVAS** to scan both the local Kali Linux system and the host Windows system, and generate a professional vulnerability report.

---

## 🛠 Tools Used
- 🐧 Kali Linux (in VirtualBox)
- 🌐 Greenbone Vulnerability Manager (OpenVAS)
- 🖥️ Windows Host System (Scanned from Kali)
- 📄 CVSS v3.1 Scoring System
- 📸 Screenshots and Report (included)

---

## 🧪 Scan Targets

| Target             | Description                    | Status   |
|--------------------|--------------------------------|----------|
| `127.0.0.1`         | Kali Linux (localhost)         | ✅ Scanned |
| `192.168.1.36`      | Windows Host (Bridged Adapter) | ✅ Scanned |

---

## 🔍 Kali Linux Vulnerability Summary

- **Scan Target:** `127.0.0.1`
- **Start Time:** June 26, 2025 15:22 UTC
- **End Time:** June 26, 2025 15:29 UTC
- **Total Vulnerabilities Found:** `1 (Medium)`
- **Low / Log / Info:** 22 (not shown in report PDF due to filters)

### 🧨 Medium Severity Finding (CVSS 5.9)
- **Port:** `5432/tcp`
- **Service:** PostgreSQL (TLS/SSL)
- **Issue:** Weak Cipher Suite: `TLS_RSA_WITH_SEED_CBC_SHA`
- **Detection Method:** SSL/TLS Supported Cipher Suite Check
- **Impact:** Can allow attackers to compromise encrypted sessions
- **Solution:** Disable weak ciphers and configure only strong TLS settings

---

## 🔒 Windows Host Vulnerability Summary

- **Scan Target:** `192.168.1.36`
- **Result:** No vulnerabilities detected
- **Reason:** Windows host had firewall enabled and no open services accessible

---

## 📸 Screenshots

All screenshots are located in the `screenshots/` folder:
- `dashboard.png` – Scan status as "Done"
- `vulnerability_list.png` – Found vulnerability details
- `vulnerability_detail.png` – CVSS, solution, and CVEs

---

## 📁 Report

The full OpenVAS scan report for Kali Linux is included in the `report/` folder:
- [`kali_scan_report.pdf`](./report/kali_scan_report.pdf)

---

## 🧠 Key Learnings

- Configured and operated a professional vulnerability scanner (OpenVAS)
- Understood how CVSS scoring works to prioritize risks
- Identified real-world issues like **weak SSL/TLS cipher suites**
- Learned to scan both **internal systems** and **external host machines**
- Understood firewall’s role in securing a machine from network scans

---
**Aditya Pilania**  
Cybersecurity Intern – Elevates Lab  
GitHub: [@aditya-pilania](https://github.com/aditya-pilania)

---

## 📌 Note

This report was prepared as part of a cybersecurity internship task for educational purposes. The findings are based on simulated/internal systems only.

