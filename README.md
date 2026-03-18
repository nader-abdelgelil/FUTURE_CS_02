# 🕵️‍♂️ Threat Intel & Forensic PDF Analyzer

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Forensics-red.svg)
![Status](https://img.shields.io/badge/Status-Active-success.svg)

## 📖 Overview
A lightweight, high-efficiency Python tool designed for Security Operations Center (SOC) analysts and threat hunters. This script automates the parsing of threat intelligence reports—specifically targeting `Phase 1 Threat Intelligence & Forensic Analysis.pdf`—to extract critical Indicators of Compromise (IoCs) without relying on bloated or complex frameworks. 

## ✨ Key Features
* **Automated IoC Extraction:** Instantly parses PDF text to identify and pull IPv4 addresses, MD5, and SHA-256 hashes.
* **Smart Deduplication:** Utilizes native Python sets to filter out redundant data, ensuring each unique IoC is only reported once, optimizing analysis time.
* **Regex-Powered Accuracy:** Employs precise Regular Expressions (`re`) to guarantee exact pattern matching for forensic artifacts.
* **Lightweight Architecture:** Requires only standard Python libraries and `PyPDF2` for minimal resource overhead.

## ⚙️ Prerequisites & Installation

To run this tool, you will need Python 3.x installed on your system.

1. Clone or download this repository to your local machine.
2. Install the required PDF parsing dependency using pip:

```bash
pip install PyPDF2
