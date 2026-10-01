Great 👍 Let's continue.

### Step 9 — Add the README content

If the **README editor** is open, paste this entire content:

```markdown
# AI Email Agent

An AI-powered email assistant built with n8n, OpenAI and Zoho Mail.

The workflow reads incoming emails, understands the sender's intent, decides whether a response is required, and creates a professional email draft for human review.

## 🚀 Features

- 📩 Reads incoming emails using IMAP
- 🤖 Uses AI to understand email context
- 🧠 Detects whether a reply is actually required
- 🚫 Ignores information-only emails
- ✍️ Generates concise and professional replies
- 📝 Saves replies as email drafts
- 👤 Keeps a human in control before sending
- 🔐 Uses OAuth for secure API access
- 🧵 Supports replying to the original email using the message ID
- 🌏 Understands relative dates using Asia/Kolkata (IST)

## 🔄 Workflow

```text
Email Trigger (IMAP)
        ↓
    AI Agent
        ↓
       IF
     /    \
    /      \
NO_REPLY   REPLY
   ↓         ↓
 STOP    Refresh Token
              ↓
        Create Zoho Draft
              ↓
         Human Review
              ↓
          Manual Send
```

## 🧠 How the AI Decides

### Information-only email

Example:

> FYI, the server has been restarted.

Result:

```text
NO_REPLY
```

No draft is created.

### Email requiring a response

Example:

> Vijay, are you coming tomorrow?

Result:

```text
REPLY
Hi, yes, I will join tomorrow.
```

The reply is saved as a draft for review.

## 🛠️ Technologies Used

- n8n
- OpenAI
- Zoho Mail
- IMAP
- OAuth 2.0
- REST API
- JSON

## 📂 Documentation

### Workflow Documentation

[AI Email Reply Workflow](./Vijay_Sharma_AI_Email_Reply_Workflow.docx)

[AI Email to Zoho Draft Workflow](./Vijay_Sharma_AI_Email_to_Zoho_Draft_Workflow.docx)

## 📸 Screenshots

### n8n Workflow

![n8n Workflow](./n8n-workflow.jpeg)

### Email Draft

![Email Draft](./email-draft.jpeg)

### Example Email

![Example Email](./email-example.jpeg)

## 🔐 Security

No real credentials are included in this repository.

Client IDs, client secrets, refresh tokens, passwords and other sensitive credentials should always be stored securely and never committed to GitHub.

Example:

```text
Client ID      = xxxxx_CLIENT_ID
Client Secret  = xxxxx_CLIENT_SECRET
Refresh Token  = xxxxx_REFRESH_TOKEN
```

## 🎯 Project Goal

The goal of this project is to demonstrate how AI can be combined with workflow automation and email APIs to reduce repetitive email work while keeping humans in control of the final communication.

## 👨‍💻 Created By

**Vijay Sharma**
```

