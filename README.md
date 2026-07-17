# Bloomberg-TKH-CTF-2026
Bloomberg x The Knowledge House Hackathon 🌐 : Capture the Flag 🚩
# 🏆 Capture The Flag — Official Write-Up
**Team:** Phish & Chips  
**Placement:** 4th Place  
**Progress:** 25 / 25 Levels Completed  
**Note:** Level 25 was a surprise bonus level unlocked only after completing the entire challenge.

---

## ⚠️ Authorization & Ethics
All testing was performed under sanctioned conditions with explicit permission from the event organizers.  
No production systems were accessed.  
Sensitive information, flags, and internal paths have been intentionally redacted.

---

# 📊 Leaderboard


![Leaderboard Screenshot](CTF.png
)



---

# Summary

---

| Level | Category | Technique | Result |
|-------|----------|-----------|--------|
| −1 | Information Disclosure | Hidden HTML comment in source | ![redacted](https://img.shields.io/badge/Path-REDACTED-red) |
| 0 | Forced Browsing | Sequential URL tampering | ![redacted](https://img.shields.io/badge/Path-REDACTED-orange) |
| 1 | Broken Authentication | Default credentials (admin:admin) | ![auto](https://img.shields.io/badge/Auto--Advanced-blue) |
| 2 | Sensitive Data Exposure | Leaked custom HTTP response header | ![leaked](https://img.shields.io/badge/Next--Level-Leaked-yellow) |
| 3 | Client-Side Secrets | window.nextLevelKey via atob() Base64 | ![redacted](https://img.shields.io/badge/REDACTED-red) |
| 4 | Parameter Tampering | Hidden field has_accepted_eula → no | ![bypassed](https://img.shields.io/badge/EULA-Bypassed-green) |
| 5 | Insecure Session Mgmt | Forged cookie isAuthenticated=1 | ![bypassed](https://img.shields.io/badge/Auth-Bypassed-green) |
| 6 | Broken JWT Validation | Flipped isAdmin:0 → 1 | ![escalation](https://img.shields.io/badge/Privilege-Escalation-purple) |
| 7 | Access Control Bypass | X-Forwarded-For: 127.0.0.1 spoof | ![localhost](https://img.shields.io/badge/Localhost-Bypassed-teal) |
| 8 | Hardcoded Credentials | strings on ELF binary | ![redacted](https://img.shields.io/badge/REDACTED-red) |
| 9 | Insecure Client Crypto | SHA-256 hash cracked | ![redacted](https://img.shields.io/badge/REDACTED-red) |
| 10 | Open Redirect | Schemaless / mixed-slash bypass /\ | ![redirect](https://img.shields.io/badge/Redirect-Forced-blueviolet) |
| 11 | Verbose Error / HPP | HTTP Parameter Pollution ?q[]= | ![stacktrace](https://img.shields.io/badge/Stack--Trace-Leaked-yellowgreen) |
| 12 | Client Crypto / Obfuscation | CryptoJS AES decrypt | ![redacted](https://img.shields.io/badge/REDACTED-red) |
| 13 | Hidden Asset Disclosure | Unlinked PNG via Network tab | ![redacted](https://img.shields.io/badge/REDACTED-red) |
| 14 | Prompt Injection | "Ignore previous instructions" override | ![redacted](https://img.shields.io/badge/REDACTED-red) |
| 15 | SQL Injection | admin' OR '1'='1 | ![loggedin](https://img.shields.io/badge/Logged--In-Without_Password-critical) |
| 16 | Command Injection | ; id command separator | ![rce](https://img.shields.io/badge/RCE-uid%3D33(www--data)-black) |
| 17 | Network Fundamentals | /27 subnet math | ![network](https://img.shields.io/badge/Subnet-Calculated-lightgrey) |
| 18 | Code Analysis | Python socket scanner | ![analysis](https://img.shields.io/badge/Code-Analyzed-lightblue) |
| 19 | Reverse Engineering | JS C2 beacon deobfuscation | ![redacted](https://img.shields.io/badge/REDACTED-red) |
| 20 | Predictable Tokens | MD5 of sequential integer | ![redacted](https://img.shields.io/badge/REDACTED-red) |
| 21 | Path Traversal | Non-recursive filter bypass | ![redacted](https://img.shields.io/badge/REDACTED-red) |
| 22 | Business Logic | Negative-value credit transfer | ![inflated](https://img.shields.io/badge/Balance-Inflated-success) |
| 23 | Chained Exploit | JWT secret + forged token + IP spoof | ![redacted](https://img.shields.io/badge/REDACTED-red) |
| 24 | Hidden Content | Decoy page + hidden DOM link | ![found](https://img.shields.io/badge/Secret-Level-Found-brightgreen) |
| 25 | Meta Challenge | "Information hidden in plain sight" | ![master](https://img.shields.io/badge/Master_of_Security-🏅-gold) |

---



---

# 🧠 Detailed Write-Ups

Below is the structure for each level.  
Since screenshots of the challenge itself cannot be shared, each write-up is documented at a high level.

---

### **Level X — [Challenge Category]**
**Objective:**  
Find the hidden entry point from a landing page with no visible navigation. Technique: Manual source-code review (View Source) revealed a developer HTML comment documenting the first challenge route. Result: Next-level path → [REDACTED] Lesson: Comments ship to the client. Routing details and architectural notes leaked in source are reconnaissance gold.

**Technique:**  
Explain the method used (e.g., DevTools inspection, cookie manipulation, SQL injection payload, hash cracking, etc.).

**Result:**  
State that you successfully advanced to the next level or retrieved the flag.

**Lesson:**  
Summarize the security principle demonstrated by the challenge.

---

### **Level 25 — Surprise Bonus Level**
**Category:** Meta Challenge  
**Objective:**  
Identify hidden content disguised as the “end” of the CTF.

**Technique:**  
Discovered a concealed path or DOM element that unlocked the final bonus level.

**Result:**  
Completed the secret level and achieved full completion of the CTF.

**Lesson:**  
Information is often hidden in plain sight — always inspect the DOM, source code, and network activity.

---

# 🧰 Tools & Techniques Used
- Browser DevTools (Elements, Network, Application)
- CyberChef (Base64, JWT, hashing)
- curl (custom headers)
- Python (hashlib, hmac, socket)
- Hash cracking tools (CrackStation, etc.)
- Linux utilities (strings, grep)
- Additional tools as needed

---

# 🦊 Key Takeaways
- Client-side data is never trustworthy.  
- Encoding is not encryption.  
- Verbose errors leak sensitive information.  
- Business logic flaws can be exploited just like technical ones.  
- Chained vulnerabilities often lead to full compromise.  
- Always inspect the DOM, source, and network — hidden content is everywhere.  
- Persistence and curiosity unlock bonus levels.

---

# ✍️ Write-Up by Jasmine  
**Team:** Phish & Chips  
**Placement:** 4th Place  
**Completion:** 25/25 Levels

