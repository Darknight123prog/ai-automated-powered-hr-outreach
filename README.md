# 🤖 n8n Workflow – Automated HR Outreach

This repository contains an **n8n workflow** that automates the process of extracting HR profiles from LinkedIn (via Apify), generating personalized cold emails with AI, and sending them automatically through Gmail.

---

## 📌 Workflow Overview
<img width="1185" height="358" alt="Screenshot 2025-09-30 at 11 23 28 AM" src="https://github.com/user-attachments/assets/8c40d44f-8f59-4195-840f-e2c093499b8a" />



1. **Scrape HR Data**  
   - Uses **Apify LinkedIn Scraper Actor** (via HTTP Request).  
   - Extracts HR profile details such as:  
     - Name & Title  
     - Company  
     - Email (if available)  
     - LinkedIn Profile Link  

2. **Store Data**  
   - Extracted data is stored in a **Google Sheet** for tracking & future use.  

3. **Generate Cold Email**  
   - Data is passed to an **AI Agent** (via OpenRouter model).  
   - The AI generates a professional cold email with subject + body text.  

4. **Send Cold Email**  
   - Email is sent automatically using the **Gmail Node**.  
   - Supports bulk sending with loop execution.  

---

## 🚀 Features

- 🔎 Automated **HR scraping** via Apify  
- 📊 Data **storage & deduplication** in Google Sheets  
- ✍️ AI-powered **email generation** (customized for each HR profile)  
- 📩 Automated **cold outreach** with Gmail integration  
- 🔄 Runs in bulk (loop over multiple HR contacts)  

---

## 🛠️ Requirements

- [n8n](https://n8n.io/) (self-hosted or cloud)  
- [Apify account](https://apify.com/) + LinkedIn scraper actor  
- [Google Sheets API credentials](https://developers.google.com/sheets/api)  
- [OpenRouter API key](https://openrouter.ai/)  
- [Gmail API credentials](https://developers.google.com/gmail/api)  

---

## ⚙️ Setup Instructions

1. **Clone this repo**
   ```bash
   git clone https://github.com/<your-username>/n8n-hr-outreach.git
   cd n8n-hr-outreach
