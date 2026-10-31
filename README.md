# 📰 News Headlines Automation

An automated n8n workflow that collects news headlines from The Daily Star, uses an AI model to select the five most important stories, and emails them to you as a Word document.

## 🚀 Features
- Collects news headlines from The Daily Star
- Removes duplicate headlines with JavaScript
- Uses AI (Google Gemini 2.5 Flash via OpenRouter) to select the top 5 stories
- Prioritizes national politics, economy, international news, and important local events
- Converts the selected news into a Word document
- Sends the document through Gmail as an attachment
- Runs automatically every day at 8:01 AM

## 🛠️ Technologies Used
- **n8n**: workflow automation
- **OpenRouter**: AI model access
- **Google Gemini 2.5 Flash**: selects the top stories
- **ConvertAPI**: HTML to Word conversion
- **Gmail**: email delivery
- **JavaScript**: cleaning and de-duplicating headlines (n8n Code node)

## ⚙️ Workflow Overview
1. **Schedule Trigger** starts the workflow every day at 8:01 AM.
2. **HTTP Request** fetches the latest headlines page from The Daily Star.
3. **HTML Extract** pulls out headlines and article links.
4. **JavaScript (Code node)** processes the headlines and removes duplicates.
5. **AI (OpenRouter)** selects the five most important stories.
6. **ConvertAPI** converts the selected stories into a Word document.
7. **Gmail** sends the document as an email attachment.

## 📂 Project Structure
```
news-headlines-automation/
├── README.md
└── Q1rrFG5aC0gODfvG-SEND_HEADLINES.json   # n8n workflow export
```

## 🔧 Setup Instructions
1. Install or access an n8n instance.
2. Import `Q1rrFG5aC0gODfvG-SEND_HEADLINES.json` into n8n (**Workflows → Import from File**).
3. Add your OpenRouter API credentials.
4. Add your ConvertAPI credentials.
5. Connect your Gmail account using OAuth2.
6. Change the recipient email address in the Gmail node.
7. Test the workflow, then activate it.

## 🔐 Requirements
- An n8n instance
- OpenRouter API key
- ConvertAPI account and API key
- Gmail account with OAuth2 authorization

> **Note:** The workflow depends on The Daily Star's website structure and on external API services. Changes to either may require workflow updates.

## 👨‍💻 Author
**Md Nadim Molla** | [LinkedIn](https://linkedin.com/in/nadim-molla) | [GitHub](https://github.com/NadimMolla1010)
