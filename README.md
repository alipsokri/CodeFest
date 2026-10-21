# 🛡️ BizGuard — SME Cybersecurity Assistant

BizGuard is an affordable, centralized, and user-friendly cybersecurity platform built for small and medium enterprises (SMEs) in Malaysia. It helps business owners detect scams, monitor financial fraud, train staff, and manage compliance — all without needing technical expertise or a dedicated IT team.

---

## 🚨 Problem Statement

SMEs face increasing cybersecurity threats but often lack the budget, technical expertise, and resources to manage them effectively. Limited scam detection, financial fraud monitoring, staff awareness, and compliance management leave businesses vulnerable to cyberattacks and financial losses.

BizGuard addresses this by providing a single platform that covers all four gaps in a way that is accessible to any business owner.

---

## ✨ Features

### Dashboard
- Real-time security health score (0–100)
- Risk breakdown by business area (email, financial, staff access, hygiene)
- 7-day threat activity chart (fraud, phishing, account access)
- Top risks to fix, ranked by severity
- Recent alerts with one-tap resolve and incident response guide

### Scam & Invoice Checker
- Paste any email, SMS, invoice, or WhatsApp message
- 17+ detection rules covering urgency pressure, bank-detail changes, lookalike domains, shortened links, authority impersonation, and more
- Works in English and Bahasa Malaysia
- AI second opinion powered by OpenAI
- Full check history saved locally with timestamps

### Financial Security
- Score any outgoing payment against your transaction history
- Flags new recipients, unusual hours, large amounts, and recently changed bank details
- Hold high-risk payments with one click and auto-create a security incident
- Full payment history log

### Staff Training
- Interactive phishing awareness drills
- Staff identify red flags in real-looking scam messages
- Instant scoring and feedback on what was missed
- Training scores feed directly into the health score

### Staff Report Cards
- Per-employee security breakdown
- Shows training score, MFA status, incident involvement, and last drill date

### Team & Access
- Manage employee MFA status
- Offboard and restore staff access
- Changes update the health score in real time

### Compliance & Hygiene Checklist
- Tracks 7 practical security checks: DMARC, SPF, DKIM, backups, password manager, software updates, HTTPS
- Plain-language fix instructions for each item

### Weekly Digest
- 7-day summary of security score changes, incidents, scam checks, and team status
- Top actions to take this week

### Trust Report
- Shareable security snapshot for banks, partners, or investors
- Shows score, area breakdowns, MFA coverage, compliance pass rate, and open items

### AI Security Assistant
- Floating chat available on every page
- Answers questions about your score, what to fix, and how to handle threats
- Powered by your live dashboard data

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML, CSS, JavaScript (single file, no framework) |
| Backend | Node.js + Express |
| AI | Google Gemini (gemini-flash-latest) via OpenAI-compatible API |
| Storage | Browser localStorage (client-side persistence) |
| Styling | CSS custom properties with dark/light mode support |


---

## 📁 Project Structure

```
bizguard-ai/
├── public/
│   └── index.html        # Full frontend (dashboard, all tabs, AI chat)
├── server.js             # Express server — /api/chat and /api/analyze
├── .env                  # Environment variables (not committed)
├── .gitignore
├── package.json
└── README.md
```

---

## 🇲🇾 Malaysian Context

BizGuard is built specifically for the Malaysian SME market:
- Scam detection covers Bahasa Malaysia and Manglish patterns
- References local authorities: LHDN, SSM, PDRM, BNM, KWSP, MCMC
- Includes real Malaysian hotlines: NSRC 997, BNM 1-300-88-5465, CyberSecurity Malaysia 1-300-88-2999
- Recognises Malaysian banks and courier services in lookalike domain detection
  
---

Open your BizGuard at **https://bizguard-rorr.onrender.com/**
