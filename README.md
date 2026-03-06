# Python Detection Engine: Authentication Log Analyzer

## 🛡️ Project Overview
This project is a lightweight **Detection Engine** designed to automate the analysis of authentication logs. It simulates the core logic of a SIEM (Security Information and Event Management) system by parsing login metadata to identify potential brute-force attacks and segmenting traffic based on network origin.



Key Features
**Threshold-Based Alerting:** Automatically categorizes security events into four threat levels (Low, Medium, High, Critical) based on failed attempt counts.
**Traffic Segmentation:** Differentiates between **Internal (Trusted)** and **External (Untrusted)** IP addresses using prefix validation.
 **Incident Response Trigger:** Features a "Security Threshold" logic that flags the entire system for action if multiple high-risk events are detected in a single session.

## Logic Matrix
The engine evaluates incoming log data against the following security thresholds:

| Failed Attempts | Threat Level | Response Action |
| :--- | :--- | :--- |
| 100+ | **CRITICAL** | Immediate System Shutdown / Lockout |
| 20 - 99 | **HIGH** | Priority Admin Investigation |
| 10 - 19 | **MEDIUM** | Suspicious Activity Flag |
| 1 - 9 | **LOW** | Routine Monitoring |
| 0 | **SAFE** | No Action Required |

## Technical Stack
* **Language:** Python 3.x
* **Libraries:** Standard Library (No external dependencies for easy deployment)

## Usage
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/manisha2580/Python-Detection-Engine.git](https://github.com/manisha2580/Python-Detection-Engine.git)
