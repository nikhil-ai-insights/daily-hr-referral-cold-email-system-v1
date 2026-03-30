# 📧 n8n Email Outreach System v1

## 🚀 Brief One Line Summary
An automated cold email outreach system that efficiently connects with HR professionals using n8n workflows.

---

## 📌 Overview
This project is an end-to-end automation workflow built using n8n to streamline cold email outreach. It fetches HR contact data from Google Sheets, filters relevant leads, and sends personalized emails via Gmail while maintaining limits and delays to simulate human behavior.

---

## ❗ Problem Statement
Manual cold emailing is time-consuming, inconsistent, and prone to errors such as duplicate outreach and lack of tracking. There is a need for an automated system that can:
- Manage contacts efficiently  
- Send emails at scale without triggering spam filters  
- Track outreach status accurately  

---

## 📊 Dataset
- Source: Google Sheets  
- Data includes:
  - HR Name  
  - Company Name  
  - Email Address  
  - Status (Emailed / Not Emailed)  

---

## 🛠️ Tools and Technologies
- **n8n** – Workflow automation  
- **Google Sheets API** – Data storage and retrieval  
- **Gmail API** – Sending emails  
- **JavaScript (within n8n nodes)** – Data filtering and logic  

---

## ⚙️ Methods
1. Scheduled trigger initiates the workflow  
2. Fetch HR data from Google Sheets  
3. Filter contacts based on predefined conditions  
4. Send personalized emails via Gmail  
5. Apply rate limits and delays to avoid spam detection  
6. Update the sheet to mark contacts as "Emailed"  

---

## 🔍 Key Insights
- Automation significantly reduces manual effort  
- Controlled email limits improve deliverability  
- Tracking prevents duplicate outreach  
- Personalization increases response rates  

---

## ▶️ How to Run This Project
1. Clone the repository  
2. Import the workflow JSON into n8n  
3. Connect your:
   - Google Sheets account  
   - Gmail account  
4. Update your Google Sheet with HR data  
5. Configure email limits and delay settings  
6. Run the workflow manually or schedule it  

---

## 📈 Results and Conclusion
The system successfully automates cold outreach while maintaining efficiency and accuracy. It ensures scalable email sending, avoids duplication, and improves overall productivity. This workflow can be extended further with AI-based personalization and response tracking.

---

## 💡 Future Improvements
- AI-generated personalized email content  
- Reply tracking and analytics dashboard  
- Integration with CRM systems  
- Multi-channel outreach (LinkedIn, WhatsApp, etc.)

---

⭐ If you found this project useful, consider giving it a star!
