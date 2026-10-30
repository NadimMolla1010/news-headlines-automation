# 📰 News Headlines Automation

An automated n8n workflow that collects news headlines from **The Daily Star**, uses AI to select the five most important stories, and sends them to your email as a Word document.

## 🚀 Features

- Automatically collects news headlines from The Daily Star.
- Uses AI (Google Gemini 2.5 Flash via OpenRouter) to select the top 5 important stories.
- Prioritizes national politics, economy, international news, and important local events.
- Converts the selected news into a Word document.
- Sends the document directly to your email through Gmail.
- Runs automatically every day.

## 🛠️ Technologies Used

- **n8n** – Workflow automation
- **OpenRouter** – AI model integration
- **Google Gemini 2.5 Flash** – AI-powered news selection
- **The Daily Star** – News source
- **ConvertAPI** – HTML to Word document conversion
- **Gmail** – Email delivery

## ⚙️ Workflow Overview

1. Schedule Trigger starts the workflow every day at 8:01 AM.
2. HTTP Request fetches the latest headlines from The Daily Star.
3. HTML Extract extracts headlines and article links.
4. JavaScript processes the headlines and removes duplicates.
5. AI selects the five most important news stories.
6. The selected stories are converted into a Word document.
7. Gmail sends the document as an email attachment.

## 📂 Project Structure

```text
news-headlines-automation/
│
├── README.md
│
└── workflows/
    └── SEND_HEADLINES.json
```

## 🔧 Setup Instructions

1. Install or access an n8n instance.
2. Import `workflows/SEND_HEADLINES.json` into n8n.
3. Configure your OpenRouter API credentials.
4. Configure ConvertAPI credentials.
5. Connect your Gmail account using OAuth2.
6. Update the recipient email address in the Gmail node.
7. Test the workflow and activate it.

## 🔐 Requirements

- n8n instance
- OpenRouter API key
- ConvertAPI account and API key
- Gmail account with OAuth2 authorization

**Note:** The workflow depends on The Daily Star's website structure and external API services. Changes to these services may require workflow updates.

## 👨‍💻 Author

**Nadim Molla**

- GitHub: [@NadimMolla1010](https://github.com/NadimMolla1010)
