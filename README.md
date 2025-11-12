# 📰 AI-Powered Tech News Newsletter Automation

This workflow automatically collects, summarizes, and sends a curated daily tech news newsletter using AI.  
It integrates RSS feeds, an AI summarization agent, and automated email delivery.

---

## 🚀 Overview

The workflow automates the following process:
1. Fetch daily tech news articles from RSS feeds.
2. Normalize and filter the data.
3. Use an AI model to generate concise summaries.
4. Email the generated newsletter to subscribers.

---

## 🧩 Workflow Structure

### 1. **Get Articles Daily**
A scheduled trigger that runs once per day to start the pipeline.

### 2. **Set Tech News RSS Feeds**
Defines a list of RSS feeds for tech-related news sources (e.g., TechCrunch, The Verge, Wired).

### 3. **Split Out**
Splits the list of feeds into individual items for separate processing.

### 4. **Read RSS News Feeds**
Parses each RSS feed to extract article metadata such as:
- Title  
- URL  
- Description  
- Publication date  

### 5. **Set and Normalize Fields**
Cleans and normalizes the extracted data to ensure consistent formatting.

### 6. **Limit**
Restricts the number of articles to a manageable amount (e.g., top 2 latest articles).

### 7. **AI NEWS Agent**
Uses the `llama3.2 Chat Model` to summarize and generate readable newsletter content:
- Summarizes articles into concise paragraphs.
- Adds AI-generated commentary or highlights.

### 8. **Send Newsletter**
Automatically sends the generated content via Gmail to a mailing list of subscribers.

---

## 🧠 AI Model

- **Model Used:** llama3.2 Chat Model  
- **Purpose:** Generate short, engaging summaries and commentary from fetched articles.

---

## 📬 Output

Subscribers receive an email newsletter containing:
- Article titles
- AI-generated summaries
- Links to the original articles

Example email structure:

---

## ⚙️ Configuration

| Variable | Description | Example |
|-----------|-------------|----------|
| RSS_FEEDS | Comma-separated list of RSS URLs | `https://techcrunch.com/feed, https://www.theverge.com/rss` |
| DAILY_TRIGGER | Cron or scheduler config | Every 24 hours |
| EMAIL_RECIPIENTS | Target email addresses | `team@example.com` |

---

## 🧾 Notes

- You can adjust the **Limit** node to include more or fewer articles per newsletter.  
- Ensure Gmail API or SMTP credentials are properly configured in the **Send Newsletter** step.  
- The **AI NEWS Agent** can be replaced with other LLMs if needed (e.g., GPT-based models).

---

## 📈 Benefits

- Fully automated daily tech news summary.
- Saves manual effort in curation.
- Keeps readers updated with minimal noise and maximum clarity.

---

## 🧰 Tech Stack

- **Automation Tool:** Custom Workflow Engine / n8n-style Automation  
- **Data Source:** RSS Feeds  
- **AI Engine:** llama3.2 Chat Model  
- **Delivery:** Gmail Integration

---

## 👤 Author

**Created by:** _Legion_  
**Purpose:** Automate daily tech news curation using AI summarization.

---
