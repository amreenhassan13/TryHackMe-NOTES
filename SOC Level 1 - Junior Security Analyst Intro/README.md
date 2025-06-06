# 🛡️ TryHackMe: SOC Level 1 - Junior Security Analyst Intro

## 📘 Room Overview
This TryHackMe room introduces the **SOC Level 1 Junior Security Analyst** role, focused on triage and initial incident response within a Security Operations Center (SOC).

You will act as a **Triage Specialist**, using a static SIEM dashboard to detect, analyze, and respond to suspicious activity.

---

## 🎯 Objectives

- Understand the role of a SOC Tier 1 Analyst
- Detect suspicious activity via alerts
- Identify malicious IP addresses
- Validate threats using external tools
- Escalate events when needed
- Block threats after approval
- Investigate any messages or indicators left by the attacker

---

## 🔄 Workflow

1. **Detect**  
   Monitor alerts in the SIEM dashboard to find anomalies.

2. **Validate**  
   Use IP scanning tools to check if the IP is malicious.

3. **Escalate**  
   If needed (e.g., successful login from malicious IP), escalate to a higher-level SOC analyst.

4. **Block**  
   After approval, block the confirmed malicious IP.

5. **Investigate**  
   Analyze any attacker messages or system changes.

---

## 🛠️ Tools Used

- SIEM Dashboard (provided in lab)
- IP Scanners (e.g., VirusTotal, AbuseIPDB)

---

## ✅ Completion
After completing the steps, you’ll have triaged a basic incident and escalated/responded appropriately — a core task of SOC Level 1 Analysts.
