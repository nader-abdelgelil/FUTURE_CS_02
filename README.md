# 🎣 Phishing Email Detection & Awareness System (CS-Task-02)

![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-red.svg)
![Threat Intel](https://img.shields.io/badge/Skill-Threat%20Intelligence-blue.svg)
![Forensics](https://img.shields.io/badge/Skill-Email%20Forensics-blueviolet.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

## 📌 Project Overview
This project focuses on identifying, analyzing, and mitigating phishing email threats. Developed as part of the Cybersecurity Internship at **Future Interns**, this repository demonstrates technical proficiency in email threat intelligence, header analysis, and corporate risk communication. 

The primary objective is to bridge the gap between technical forensic detection and end-user security awareness by providing a comprehensive, client-ready **Phishing Detection & Awareness Report**.

---

## 🔍 Case Study: The "PayPal" Phishing Campaign
To demonstrate the analysis process, a real-world phishing simulation impersonating **PayPal** was utilized. The analysis was broken down into a structured incident response workflow:

### 🛠 Step-by-Step Analysis Methodology

1. **Visual & Heuristic Inspection:** * Analyzed the email for Social Engineering tactics (e.g., manufactured urgency: *"You have 24 hours..."*).
   * Identified Brand Hijacking and Display Name Spoofing (`services@paypal-accounts.com` instead of the legitimate `@paypal.com`).
2. **Payload & URL Analysis:** * Extracted the hidden URL behind the Call-to-Action (CTA) button.
   * Scanned the endpoint to identify credential-harvesting portals and discussed **Zero-Day Evasion** tactics when scanners initially return false negatives.
3. **Forensic Header Analysis:** * Extracted the raw email headers to trace the true origin.
   * Analyzed routing data to prove a mismatch between the `From` address and the actual `Return-Path` IP address.
4. **Risk Communication:** * Translated complex technical findings into actionable, business-friendly prevention guidelines for employees.

---

## 🧰 Tools & Technologies Used

| Tool / Technology | Purpose | Application in this Project |
| :--- | :--- | :--- |
| **MXToolbox** | Email Header Forensics | Tracing source IPs and verifying SPF/DKIM/DMARC authentication failures. |
| **VirusTotal** | URL & Payload Scanning | Inspecting embedded links for malicious redirects and zero-day threats. |
| **Browser DevTools** | Link Extraction | Safely hovering and extracting underlying URIs without executing the payload. |
| **PDF Reporting** | Corporate Documentation | Structuring technical findings into a client-ready executive summary. |

---

## 📊 Email Threat Classification Framework

As part of the awareness system, incoming communications were classified using the following standard:

| Risk Level | Technical Indicators | Required Action |
| :--- | :--- | :--- |
| ✅ **Safe** | Verified SPF/DKIM, legitimate domain, expected content. | Normal interaction. |
| ⚠️ **Suspicious** | External sender, generic greeting, unusual attachment. | Verify identity via secondary channel (e.g., phone). |
| 🚨 **Phishing** | Spoofed IP, urgent threats, malicious Call-to-Action links. | **Report to IT/SOC immediately & Delete.** |

---

## 📂 Project Deliverables

* 📄 **`Phishing_Analysis_Report.pdf`**: The finalized, professional report containing the complete breakdown of the PayPal phishing simulation, technical proofs (screenshots), and security guidelines.

---

## 🛡 Skills Demonstrated
* **Threat Intelligence:** Identifying Indicators of Compromise (IOCs) and Typosquatting.
* **Forensic Analysis:** Deep-diving into email metadata and authentication protocols.
* **Vulnerability Management:** Understanding scanner bypass techniques (Evasion).
* **Security Awareness:** Drafting clear, non-technical prevention protocols for enterprise users.
## 📁 Repository Structure

```text
├── Phishing_Analysis_Report.pdf   # The main deliverable and executive summary
├── images/                        # Screenshots of headers, payload links, and analysis
└── README.md                      # This documentation file
---
*Developed by **Nader Abdelgelil** | Cybersecurity Intern @ Future Interns*
