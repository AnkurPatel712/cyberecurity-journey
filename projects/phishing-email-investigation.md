# 📧 SOC Investigation: Phishing Email Analysis (Case Study 02)

## 🧾 Objective
Analyze a suspicious email reported by an employee to determine if it is a phishing attempt and assess potential risks.

---

## 📊 Scenario

An employee from the finance department reported receiving an urgent email requesting password verification.

- Sender: security-update@paypaI-alerts.com  
- Subject: "Action Required: Verify Your Account Immediately"  
- Attachment: verify_account.html  
- Received Time: 11:08 AM  

---

## 🛠️ Tools & Techniques
- Email header analysis (basic)
- URL inspection
- Threat intelligence lookup (VirusTotal concept)
- Manual phishing indicator analysis

---

## 🔎 Investigation

### Step 1: Sender Analysis
- Domain uses typo: **paypaI-alerts.com** (capital “i” instead of “l”)
- Not an official PayPal domain
- Indicates domain spoofing

---

### Step 2: Email Content Review
- Uses urgent language: “Immediate action required”
- Requests sensitive information (login credentials)
- Contains generic greeting (no personalization)

---

### Step 3: Link & Attachment Analysis
- HTML attachment contains embedded login form
- Redirects to suspicious external domain
- Not associated with legitimate PayPal infrastructure

---

## ⏱️ Timeline

| Time       | Activity |
|------------|---------|
| 11:08 AM   | Email received by employee |
| 11:12 AM   | Reported to SOC team |
| 11:15 AM   | Analysis started |
| 11:25 AM   | Phishing confirmed |

---

## 🧠 Analyst Notes

The attacker used domain spoofing and urgency to trick the user into revealing credentials.  
The use of an HTML attachment suggests an attempt to capture login data via a fake page.

This aligns with common phishing tactics targeting financial accounts.

---

## 🧬 MITRE ATT&CK Mapping

- T1566.001 – Phishing: Spearphishing Attachment  
- T1566.002 – Phishing: Spearphishing Link  

---

## 🚨 Conclusion

Confirmed phishing attempt designed to steal user credentials.

---

## ✅ Response Actions (Simulated)

- Blocked sender domain organization-wide  
- Removed email from affected mailboxes  
- Alerted users about phishing attempt  

---

## 📌 Recommendations

- Enable Multi-Factor Authentication (MFA)  
- Conduct phishing awareness training  
- Implement advanced email filtering rules  
