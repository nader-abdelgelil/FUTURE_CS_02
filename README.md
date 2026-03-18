# 🎣 Phishing Email Detection & Awareness System (CS-Task-02)

[![Cyber Security Internship](https://img.shields.io/badge/Internship-Cyber%20Security-blue?style=flat-square&logo=keybase)](https://futureinterns.com/)
[![Track: CS](https://img.shields.io/badge/Track-CS-green?style=flat-square&logo=shield)](https://github.com/nader-abdelgelil/FUTURE_CS_02)
[![Task Status: Complete](https://img.shields.io/badge/Status-Complete-success?style=flat-square&logo=check)](https://github.com/nader-abdelgelil/FUTURE_CS_02)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square&logo=git)](https://opensource.org/licenses/MIT)

## 📌 Project Overview
This project focuses on identifying, cataloging, and mitigating advanced phishing email threats. Developed during the Cybersecurity Internship at **Future Interns**, this repository serves as a comprehensive "client-ready" deliverable. 

The goal is to bridge the gap between technical threat intelligence and corporate security awareness by providing a complete workflow for detecting, analyzing, and documenting malicious email campaigns.

---

## 🔍 Featured Case Study: The "PayPal Security" Campaign
To demonstrate the analysis pipeline, a real-world phishing email impersonating **PayPal** was utilized as a simulation target. The incident response workflow was structured to simulate a Tier-1 SOC Analyst investigation.

<details>
<summary>📂 <b>Methodology Breakdown (Click to Expand)</b></summary>
A multi-layered analysis methodology was applied, combining visual heuristics with technical forensics.

1.  **Phase 1: Visual Heuristics:** Identifying brand hijacking, social engineering triggers (urgency), and typosquatting domains.
2.  **Phase 2: Payload Analysis:** Extracting hidden URLs and verifying malicious redirects.
3.  **Phase 3: Header Forensics:** Analyzing mail server routing and authentication metadata (SPF/DKIM/DMARC) to prove spoofing.
4.  **Phase 4: Awareness Reporting:** Translating complex forensic data into actionable prevention guidelines for non-technical enterprise users.
</details>

---

## 🛠 Project Visuals & Proof of Concepts

This section showcases the key stages of the investigation, moving from detection to technical proof.

### 🛡 Phase 1: Threat Identification (The Email)

The initial threat vector was identified as a well-crafted brand impersonation email. We analyzed the visual indicators and social engineering tactics.

| Phishing Indicators | Description | Screenshot |
| :--- | :--- | :--- |
| **Urgent Language** | "24 hours to solve... disabled" - Creates panic. | <img src="https://raw.githubusercontent.com/nader-abdelgelil/FUTURE_CS_02/main/Phishing_Analysis_Report_files/image001.png" width="250" alt="PayPal Phishing Email Screenshot"> |
| **Generic Salutation** | "Dear PayPal customer" - Non-personalized. | |
| **Typosquatting Sender** | `services@paypal-accounts.com` - Look-alike domain. | |

> Legitimate communications from PayPal exclusively originate from the `@paypal.com` domain.

### ⚠️ Phase 2: Technical Evasion (The VirusTotal Mystery)

This is the most critical technical finding of the project. **Automated scanners are not foolproof.**

Upon analyzing the payload URL `http://confirm-paypal-secure-login.com`, the **automated VirusTotal scan initially returned a 0/95 (Clean) result**. This is a prime example of **Zero-Day Phishing Evasion**. The attacker had just registered the domain, and security vendors had not yet blacklisted it.

<img src="https://raw.githubusercontent.com/nader-abdelgelil/FUTURE_CS_02/main/virus_total_green.jpg" width="600" alt="VirusTotal Clean Score Screenshot">

> **Conclusion (Human Analysis):** Despite the "clean" automated result, the URI structure clearly mimics a banking portal (`confirm-paypal-secure-login`). This confirms the link is malicious and designed for **Credential Harvesting**. Relying solely on automated scanners is a high-risk security flaw.

### 🔴 Phase 3: Technical Proof (The MXToolbox Forensic)

To technically invalidate the email's claim of being from PayPal, we performed a deep forensic analysis of the email headers using MXToolbox. The results provide definitive proof of a forgery.

<img src="https://raw.githubusercontent.com/nader-abdelgelil/FUTURE_CS_02/main/mxtoolbox_analysis.jpg" width="600" alt="MXToolbox Header Analysis Screenshot">

**Critical Mismatch Found:** While the `From` address claims "Team Support", the `Return-Path` and `Relay Information` prove the email originated from an external, unverified server (`mail.fake-domain-123.com`) on an unauthorized IP address. This is a definitive **Sender Spoofing** authentication failure.

---

## 📋 Standardized Threat Classification Framework

To operationalize the awareness system, incoming communications are classified using the following risk-based standard:

| Risk Classification | Behavioral Indicators | Recommended Action |
| :--- | :--- | :--- |
| ✅ **Safe** | Verified SPF/DKIM/DMARC, known sender history, expected content. | Normal interaction. |
| ⚠️ **Suspicious** | External origin, generic salutation, unusual attachment type. | **Hold.** Verify identity via secondary channel (phone). Do not click. |
| 🚨 **Phishing** | Urgency/threats, spoofed headers, newly registered domain. | **Report to SOC/IT immediately & Delete.** |

---

## 📂 Deliverables

* 📄 **`Phishing_Detection_Report.pdf`**: The complete, client-ready professional report including executive summary, multi-phase technical evidence (screenshots), and formalized enterprise prevention guidelines.

---

## 🛡 Skills Demonstrated
* **Email Threat Intelligence & IOC Identification.**
* **Typosquatting & Brand Hijacking Detection.**
* **Advanced Email Forensic Analysis (Header metadata, SPF/DKIM/DMARC analysis).**
* **Understanding Automation Bypass Tactics (Zero-Day Evasion).**
* **Risk Classification & Business-Friendly Reporting (NIST-aligned communication).**

---
*Developed by **Nader Abdelgelil** | Cybersecurity Intern @ Future Interns*
