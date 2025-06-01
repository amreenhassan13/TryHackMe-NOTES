# Room 2: Defensive Security Intro (TryHackMe)

This room introduces key defensive security domains, including SOC operations, threat intelligence, digital forensics, incident response, and malware analysis. You will also interact with a simulated SIEM (Security Information and Event Management) platform.

## 🧩 Challenge Overview

**Objective:** Block a malicious IP address using the firewall interface and retrieve the hidden message left by the attacker.

---

## ⚠️ Challenge Faced

When attempting to block an IP address, I encountered the following error:

> **"Invalid IP"**

This happened even when copying IPs directly from the logs.

---

## 🔍 Troubleshooting Steps

Upon inspection of the firewall interface, I noticed some IPs were already blocked:

- `101.34.37.231`
- `212.38.99.12`
- `213.106.84.35`

**Root Cause:**  
The system gives an "Invalid IP" error if you try to block an IP address that is already on the list. It does **not** allow duplicates.

---

## ✅ Solution

1. Went back to the provided logs and alerts (e.g., Suricata alerts, web access logs).
2. Identified a **new** suspicious IP address **not already blocked**.
3. Entered this new IP into the firewall block field.
4. Clicked **"Block IP Address"**.
5. Successfully blocked the new IP and the system revealed the hidden message left by the attacker.

---

## 📝 Final Note

Always cross-reference the IP you want to block with the already-blocked list. The "Invalid IP" error is likely just a duplicate entry warning.

If you're unsure which IP is malicious, revisit logs, alerts, or use packet capture analysis tools to find unusual traffic.

## 🛡️ Topics Covered

- Security Operations Center (SOC)
- Threat Intelligence
- Digital Forensics and Incident Response (DFIR)
- Malware Analysis
- SIEM Simulation (Hands-on)

---

## 🏢 Security Operations Center (SOC)

A SOC is a team that monitors, detects, and responds to security events on a network. Key responsibilities include:

- **Vulnerabilities**: Track and recommend fixes for discovered system weaknesses.
- **Policy Violations**: Monitor for improper actions (e.g., uploading company data to personal storage).
- **Unauthorized Activity**: Detect misuse of stolen credentials and unusual account behavior.
- **Network Intrusions**: Identify and respond to malicious access, whether through phishing or exploit.

SOC teams use **Threat Intelligence** to stay informed and prepared.

---

## 🧠 Threat Intelligence

Threat Intelligence is the process of collecting, analyzing, and applying data about potential or active threats.

- **Sources**: Network logs, forums, malware feeds
- **Stages**: Data collection → Processing → Analysis
- **Purpose**:
  - Understand adversaries (actors, tactics, and goals)
  - Inform defense strategy
  - Enable proactive response

---

## 🧪 Digital Forensics and Incident Response (DFIR)

### 🔍 Digital Forensics

Focuses on identifying and analyzing digital evidence from:

- **File Systems**: Recover deleted/overwritten files and program traces.
- **Memory (RAM)**: Analyze running malware not saved to disk.
- **System Logs**: Investigate events and attacker actions.
- **Network Logs**: Examine packet data for traces of communication.

### 🚨 Incident Response

A structured approach to managing security incidents:

1. **Preparation** – Train staff and develop prevention strategies.
2. **Detection & Analysis** – Identify and assess incidents using tools like SIEM.
3. **Containment, Eradication & Recovery** – Limit damage, remove threats, restore systems.
4. **Post-Incident Activity** – Document lessons learned and improve defenses.

---

## 🦠 Malware Analysis

Malware = Malicious Software. Types include:

- **Virus**: Spreads by modifying other programs.
- **Trojan Horse**: Appears useful but contains harmful code.
- **Ransomware**: Encrypts files and demands payment for decryption.

### Analysis Techniques:

- **Static Analysis**: Examine code without execution (e.g., file inspection, reverse engineering).
- **Dynamic Analysis**: Execute in sandbox environment to observe behavior.

### AbuseIPDB and Cisco Talos Intelligence

AbuseIPDB and Cisco Talos Intelligence are open-source databases used to check the reputation and location of IP addresses. These tools are commonly used by security analysts to assist in alert investigations.

