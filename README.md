# 📧 Daily HR Referral Cold Email System (n8n Workflow)

## 🚀 Overview

**Daily HR Referral Cold Email System v1** is an automated outreach workflow built using **n8n** that helps you efficiently connect with HR professionals through personalized cold emails.

This system eliminates manual effort by:

- 📥 Fetching HR data automatically
- 🔍 Filtering relevant contacts
- 📨 Sending controlled cold emails
- 📊 Tracking outreach status
- 🚫 Preventing duplicate emails

---

## 🧠 How It Works (End-to-End Flow)

```
Schedule Trigger → Get Data → Filter → Limit → Send Email → Wait → Update Sheet
```

### 🔹 Step-by-Step Execution

| Step | Node | Description |
|------|------|-------------|
| 1 | ⏰ **Schedule Trigger** | Workflow runs automatically at a fixed time (e.g., daily) |
| 2 | 📊 **Get Rows from Google Sheets** | Fetches HR contact data (Name, Email, Company, Status, etc.) |
| 3 | 🔍 **IF Condition (Filtering)** | Filters contacts not yet contacted, with valid emails and matching targeting criteria |
| 4 | ⚡ **Limit Node** | Restricts number of emails per run to prevent Gmail spam detection |
| 5 | 📨 **Send Email (Gmail Node)** | Sends personalized cold emails using dynamic variables like `{{Name}}` and `{{Company}}` |
| 6 | ⏳ **Wait Node** | Adds human-like delay between emails |
| 7 | ✅ **Update Google Sheet** | Marks contact as `Emailed` to ensure no duplicate outreach |

---

## 🏗️ Tech Stack

| Tool | Purpose |
|------|---------|
| [n8n](https://n8n.io) | Workflow Automation |
| Gmail API | Email Delivery |
| Google Sheets | Contact Database |
| n8n Logic Nodes | IF, Limit, Wait handling |

---

## 📁 Google Sheet Structure

| Name | Email | Company | Status | Last Contacted |
|------|-------|---------|--------|----------------|
| John Doe | john@email.com | ABC Corp | Pending | — |

### Status Values

| Value | Meaning |
|-------|---------|
| `Pending` | Not yet contacted |
| `Emailed` | Outreach sent |

---

## ✉️ Email Personalization Example

```
Subject: Quick Question Regarding Opportunities at {{Company}}

Hi {{Name}},

I came across your profile and wanted to reach out regarding
potential opportunities at {{Company}}.

I'd love to connect and explore how I can contribute.

Looking forward to your response.

Best regards,
[Your Name]
```

---

## ⚙️ Setup Instructions

### 1️⃣ Clone / Import Workflow

Import the n8n workflow JSON file into your n8n instance:

```
Settings → Import Workflow → Select JSON File
```

### 2️⃣ Connect Google Sheets

- Add your **Google Sheets credentials** in n8n
- Select your target spreadsheet and sheet tab

### 3️⃣ Setup Gmail

- Connect your **Gmail account via OAuth2** in n8n credentials

### 4️⃣ Configure Schedule

- Open the **Schedule Trigger** node
- Set your preferred run time (daily recommended)

### 5️⃣ Adjust Limits

- Open the **Limit Node**
- Set a safe daily email limit (recommended: **10–20 emails/day**)

---

## 🛡️ Anti-Spam Strategy

- ✅ Email limit per run
- ✅ Delay between emails
- ✅ Personalized content
- ✅ No duplicate sends

---

## 📊 Use Cases

- 🎯 HR outreach for referrals
- 💼 Job hunting automation
- 🤝 Networking with recruiters
- 📈 Lead generation

---

## 🚀 Future Improvements

- [ ] AI-generated email personalization
- [ ] Resume attachment automation
- [ ] Follow-up email sequences
- [ ] Analytics dashboard
- [ ] CRM integration

---

## ⚠️ Disclaimer

> This project is for **educational and ethical outreach purposes only.**
> Please avoid spamming and always follow email best practices and applicable laws (CAN-SPAM, GDPR, etc.).

---

## 🙌 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
