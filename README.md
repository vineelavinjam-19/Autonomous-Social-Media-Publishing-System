# Autonomous-Social-Media-Publishing-System
# AI-Powered LinkedIn Content Automation System

An autonomous content generation and publishing workflow built using **n8n**, **Google Gemini AI**, **Google Sheets**, and the **LinkedIn API**.

This system automatically generates professional LinkedIn posts from structured prompts, performs approval-based validation, and publishes content directly to LinkedIn with minimal human intervention.

---

## 🚀 Features

- Automated LinkedIn post generation using Google Gemini
- Scheduled content publishing
- Google Sheets integration for content management
- Approval/Rejection workflow
- Automatic content regeneration for rejected posts
- Direct publishing through LinkedIn API
- Gmail notifications after successful publishing
- Low-code workflow orchestration using n8n

---

## 🏗️ Workflow Architecture

```text
Schedule Trigger
       │
       ▼
Google Sheets (Content Ideas)
       │
       ▼
AI Agent (Google Gemini)
       │
       ▼
Generate LinkedIn Post
       │
       ▼
Approval Check
   ┌─────────┴─────────┐
   ▼                   ▼
Accepted          Rejected
   │                   │
   ▼                   ▼
LinkedIn API     Regenerate Content
   │                   │
   └─────────┬─────────┘
             ▼
     Gmail Notification
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|----------|
| n8n | Workflow Automation |
| Google Gemini API | AI Content Generation |
| Google Sheets API | Content Storage |
| LinkedIn API | Social Media Publishing |
| Gmail API | Email Notifications |
| HTTP Requests | External API Communication |

---

## 📋 How It Works

### Step 1: Content Collection
Content prompts and publishing details are stored in Google Sheets.

### Step 2: AI Content Generation
The workflow retrieves prompts and sends them to Google Gemini for professional LinkedIn post creation.

### Step 3: Approval Validation
Generated content is checked against an approval flag.

- Approved → Publish to LinkedIn
- Rejected → Regenerate content using Gemini

### Step 4: LinkedIn Publishing
Approved posts are automatically published through the LinkedIn API.

### Step 5: Notification
A confirmation email is sent after successful publication.

---

## 📂 Project Structure

```text
linkedin-content-automation/
│
├── workflows/
│   └── linkedin_automation.json
│
├── docs/
│   └── architecture.png
│
├── screenshots/
│   ├── workflow.png
│   ├── sheets.png
│   ├── linkedin-post.png 
│   └──  linkedin-posts-of-workflow&automated-post.png
│
└── README.md
```

---

## ⚙️ Setup

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/linkedin-content-automation.git
cd linkedin-content-automation
```

### 2. Configure APIs

- Google Gemini API Key
- LinkedIn Developer Credentials
- Google Sheets Access
- Gmail Credentials

### 3. Import Workflow

Import the provided workflow JSON into n8n.

### 4. Configure Environment Variables

```env
GEMINI_API_KEY=your_api_key
LINKEDIN_CLIENT_ID=your_client_id
LINKEDIN_CLIENT_SECRET=your_client_secret
GOOGLE_SHEETS_ID=your_sheet_id
```

### 5. Activate Workflow

Enable the schedule trigger and start automated publishing.

---

## 📈 Future Enhancements

- Multi-platform publishing
- GitHub activity based content generation
- LeetCode progress sharing
- Analytics dashboard
- AI-generated image support
- Engagement tracking
- Personal branding insights

---

## 🎯 Use Cases

- Personal branding
- Student portfolios
- Developer communities
- Startup founders
- Content creators
- Recruiters and professionals

---

## 📜 License

MIT License

---

## 👨‍💻 Author

Built with n8n, Google Gemini, and LinkedIn APIs to automate professional content publishing and personal branding workflows.
