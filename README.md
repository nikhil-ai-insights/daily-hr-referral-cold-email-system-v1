# 🚀 Daily HR Referral Cold Email System v1

> An automated n8n workflow that sends personalized cold emails to HR professionals daily with smart filtering, limits, and tracking.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Problem Statement](#-problem-statement)
- [Dataset](#-dataset)
- [Tools and Technologies](#️-tools-and-technologies)
- [Workflow Architecture](#️-workflow-architecture)
- [Key Insights](#-key-insights)
- [How to Run](#️-how-to-run-this-project)
- [Results and Conclusion](#-results-and-conclusion)
- [Future Improvements](#-future-improvements)

---

## 🧠 Overview

The **Daily HR Referral Cold Email System** is a fully automated outreach solution built using **n8n**. It streamlines the process of connecting with HR professionals by fetching contact data from Google Sheets, filtering relevant leads, and sending personalized emails through Gmail.

The system ensures efficiency, avoids spam detection, and maintains proper tracking by updating outreach status after each email.

---

## ❗ Problem Statement

Cold emailing manually is inefficient and prone to multiple issues:

- ⏱️ Time-consuming repetitive tasks
- 🔁 Risk of sending duplicate emails
- 📉 Lack of proper tracking
- 🚫 High chances of being flagged as spam

This project solves these problems by **automating the entire outreach pipeline**.

---

## 📊 Dataset

**Source:** Google Sheets

| Field | Description |
|---|---|
| HR Name | Full name of the HR contact |
| Company Name | Company the HR belongs to |
| Email Address | Professional email address |
| Status | `Emailed` / `Not Emailed` |

---

## 🛠️ Tools and Technologies

| Tool | Purpose |
|---|---|
| **n8n** | Workflow automation engine |
| **Google Sheets API** | Data storage and retrieval |
| **Gmail API** | Email delivery |
| **IF Node** | Conditional filtering of contacts |
| **Rate Limiting** | Controlled email sending |
| **Delay/Wait Node** | Human-like behavior simulation |

---

## ⚙️ Workflow Architecture

The workflow follows a structured automation pipeline:

```
Schedule Trigger
      ↓
Get Rows (Google Sheets)
      ↓
IF Node — Filter "Not Emailed" contacts
      ↓
Limit Node — Cap emails per run
      ↓
Gmail Node — Send personalized email
      ↓
Wait Node — Delay between sends
      ↓
Update Row (Google Sheets) — Mark as "Emailed"
```

### Step-by-Step Breakdown

1. **⏰ Schedule Trigger** — Automatically runs the workflow at a defined time daily
2. **📋 Get Rows (Google Sheets)** — Fetches all HR contact data from the sheet
3. **🔀 IF Node (Filter)** — Selects only contacts with status `Not Emailed`
4. **🔢 Limit Node** — Restricts the number of emails per run to avoid spam flags
5. **📧 Gmail Node** — Sends a personalized cold email to each contact
6. **⏳ Wait Node** — Adds a delay between emails for human-like behavior
7. **✅ Update Row (Google Sheets)** — Marks each contact as `Emailed` to prevent duplicates

---

## 🔍 Key Insights

- ⚡ Automation reduces manual effort by **90%+**
- 📬 Email limits improve deliverability and avoid spam filters
- 🔒 Tracking system ensures **zero duplicate outreach**
- 🤖 Delays make automation appear more human-like
- 📈 Fully scalable for high-volume daily outreach

---

## ▶️ How to Run This Project

### 1. Clone the Repository

```bash
git clone https://github.com/[your-username](https://github.com/nikhil-ai-insights)/daily-hr-referral-cold-email-system.git
cd daily-hr-referral-cold-email-system
```

### 2. Set Up n8n

- Install n8n locally or use the cloud version
- Import the `workflow.json` file into your n8n instance

### 3. Connect Services

- 🔗 Connect your **Google Sheets** account via OAuth
- 🔗 Connect your **Gmail** account via OAuth

### 4. Configure Your Google Sheet

Ensure your sheet contains the following columns:

```
| Name | Email | Company | Status |
```

### 5. Customize the Workflow

- Set your preferred **daily schedule**
- Adjust the **email sending limit** per run
- Modify the **delay timing** between emails
- Personalize the **email template** content

### 6. Run the Workflow

```bash
# Option A: Trigger manually from the n8n dashboard
# Option B: Enable the Schedule Trigger for full automation
```

---

## 📈 Results and Conclusion

This system successfully automates daily cold outreach while maintaining efficiency and accuracy. It prevents duplicate emails, ensures proper tracking, and improves productivity significantly.

The workflow is **scalable** and can be adapted for different outreach use cases such as sales, networking, or recruitment.

---

## 💡 Future Improvements

- [ ] 🤖 AI-generated personalized email content
- [ ] 📊 Email open/reply tracking
- [ ] 📉 Dashboard for analytics
- [ ] 🔗 CRM integration
- [ ] 🌐 Multi-channel outreach (LinkedIn, WhatsApp)

---

## ⭐ Support

If you found this project helpful, please consider giving it a **⭐ star** on GitHub — it means a lot!

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
