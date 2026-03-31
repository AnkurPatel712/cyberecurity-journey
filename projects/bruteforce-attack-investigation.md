# 🚨 SOC Investigation: Suspicious Login Activity (Case Study 01)

## 🧾 Objective
Investigate abnormal login behavior detected in authentication logs and determine whether it indicates a security incident.

---

## 📊 Scenario

During routine monitoring, multiple failed login attempts were detected targeting a privileged account.

- Target User: finance_admin01
- Source IP: 185.243.115.21
- Time Window: 09:12 AM – 09:18 AM

---

## 🛠️ Tools & Environment
- Simulated SIEM environment (TryHackMe)
- Windows Event Logs
- Manual log analysis

---

## 🔎 Investigation

### Step 1: Failed Login Analysis
- Event ID 4625 observed 27 times within 6 minutes
- All attempts originated from the same IP address

### Step 2: Successful Login Detection
- Event ID 4624 recorded after failed attempts
- Login success for privileged account

### Step 3: Behavioral Indicators
- Login occurred outside normal working hours
- IP address not previously seen for this user

---

## ⏱️ Timeline

| Time       | Activity |
|------------|---------|
| 09:12 AM   | Failed login attempts begin |
| 09:16 AM   | Continued rapid login failures |
| 09:17 AM   | Successful login detected |
| 09:18 AM   | Suspicious session activity |

---

## 🧠 Analyst Notes

The high frequency of failed login attempts suggests automated brute-force activity.  
The successful login following multiple failures strongly indicates possible credential compromise.

Unusual login timing and unfamiliar IP further confirm suspicious behavior.

---

## 🧬 MITRE ATT&CK Mapping

- T1110 – Brute Force  
- T1078 – Valid Accounts  

---

## 🚨 Conclusion

This activity indicates a successful brute-force attack leading to unauthorized access.

---

## ✅ Response Actions (Simulated)

- Disabled affected account  
- Reset credentials  
- Blocked malicious IP  
- Notified security team  

---

## 📌 Recommendations

- Enable MFA  
- Implement account lockout policy  
- Monitor privileged accounts closely  
