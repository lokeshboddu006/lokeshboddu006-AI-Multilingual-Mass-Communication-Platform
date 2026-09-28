
<div align="center">

# 🌐 GovComm AI

### AI-Powered Multilingual Mass Communication & Public Awareness Platform

<p>
  <b>Create</b> •
  <b>Target</b> •
  <b>Generate</b> •
  <b>Translate</b> •
  <b>Distribute</b> •
  <b>Track</b> •
  <b>Analyze</b>
</p>

<br>

![Status](https://img.shields.io/badge/STATUS-ACTIVE%20DEVELOPMENT-00C853?style=for-the-badge)
![React](https://img.shields.io/badge/REACT-VITE-61DAFB?style=for-the-badge&logo=react&logoColor=white)
![Django](https://img.shields.io/badge/DJANGO-REST-092E20?style=for-the-badge&logo=django&logoColor=white)
![FastAPI](https://img.shields.io/badge/FASTAPI-AI%20SERVICE-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/POSTGRESQL-DATABASE-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![AI](https://img.shields.io/badge/AI-GROQ%20%7C%20INDICTRANS2-FF6F00?style=for-the-badge)

<br><br>

> **A unified platform for intelligent, multilingual, targeted and data-driven public communication.**

</div>

---

## 🌟 What is GovComm AI?

**GovComm AI** is a full-stack communication management platform designed to simplify the complete lifecycle of public-awareness communication.

From creating an announcement to targeting the right audience, generating content with AI, translating it into Indian languages, distributing it across communication channels, and tracking engagement — everything is brought together into one unified platform.

```text
┌───────────────┐
│   RECIPIENTS  │
└───────┬───────┘
        ↓
┌───────────────┐
│   TARGETING   │
└───────┬───────┘
        ↓
┌───────────────┐
│    CAMPAIGN   │
└───────┬───────┘
        ↓
┌───────────────┐
│ AI GENERATION │
└───────┬───────┘
        ↓
┌───────────────┐
│  TRANSLATION  │
└───────┬───────┘
        ↓
┌───────────────┐
│   DELIVERY    │
└───────┬───────┘
        ↓
┌───────────────┐
│   TRACKING    │
└───────┬───────┘
        ↓
┌───────────────┐
│   ANALYTICS   │
└───────────────┘
````

---

# ✨ Core Features

<table>
<tr>
<td width="50%">

### 🤖 AI Content Generation

Generate communication content using AI.

* Brief content
* Standard content
* Detailed content
* Informative tone
* Formal tone
* Urgent tone
* Friendly tone

</td>

<td width="50%">

### 🌍 Multilingual Communication

Create communication for diverse Indian audiences.

**Supported languages include:**

English • Hindi • Telugu • Tamil • Kannada • Malayalam • Marathi • Bengali • Gujarati • Punjabi • Odia • Urdu

</td>
</tr>

<tr>
<td width="50%">

### 🎯 Smart Audience Targeting

Build targeted audiences using:

* State / UT
* District
* City
* Language
* Occupation
* Organization
* Campaign attributes

</td>

<td width="50%">

### 📢 Campaign Management

Manage the complete campaign lifecycle:

* Content
* Audience
* Languages
* Priority
* Channels
* Scheduling
* Delivery
* Analytics

</td>
</tr>

<tr>
<td width="50%">

### 📡 Delivery Tracking

Track communication from queue to engagement.

```text
QUEUED
  ↓
PROCESSING
  ↓
SENT
  ↓
DELIVERED
  ↓
READ
  ↓
CLICKED
```

</td>

<td width="50%">

### 📊 Engagement Analytics

Monitor communication performance through:

* Delivery KPIs
* Delivery funnel
* Recipient status
* Channel analytics
* Language analytics
* Engagement events
* Failures & retries

</td>
</tr>
</table>

---

# 🌐 Multilingual AI

GovComm AI integrates **AI4Bharat IndicTrans2** for Indian-language translation.

Dynamic campaign placeholders are preserved during translation:

```text
{{name}}
{{location}}
{{date}}
{{message}}
```

This enables personalized multilingual communication without breaking campaign templates.

---

# 🏗️ System Architecture

```text
                         ┌─────────────────────────┐
                         │      REACT + VITE        │
                         │        FRONTEND          │
                         └────────────┬────────────┘
                                      │
                              REST API / JWT
                                      │
                                      ▼
                         ┌─────────────────────────┐
                         │       DJANGO REST        │
                         │      CORE BACKEND        │
                         └────────────┬────────────┘
                                      │
                    ┌─────────────────┴─────────────────┐
                    │                                   │
                    ▼                                   ▼
          ┌──────────────────┐               ┌──────────────────┐
          │    POSTGRESQL    │               │     FASTAPI      │
          │     DATABASE     │               │    AI SERVICE    │
          └──────────────────┘               └────────┬─────────┘
                                                       │
                                              ┌────────┴────────┐
                                              │                 │
                                              ▼                 ▼
                                           GROQ          INDIC TRANS2
                                              │                 │
                                              └────────┬────────┘
                                                       ▼
                                             AI + TRANSLATION
                                                       │
                                                       ▼
                                            DELIVERY & TRACKING
                                                       │
                                                       ▼
                                                 ANALYTICS
```

---

# 🛠️ Technology Stack

<div align="center">

| Layer             | Technology                         |
| :---------------- | :--------------------------------- |
| 🎨 Frontend       | **React + Vite**                   |
| ⚙️ Backend        | **Django + Django REST Framework** |
| 🤖 AI Service     | **FastAPI**                        |
| 🗄️ Database      | **PostgreSQL**                     |
| 🔐 Authentication | **JWT**                            |
| 🧠 AI Generation  | **Groq**                           |
| 🌍 Translation    | **AI4Bharat IndicTrans2**          |
| 🔗 Communication  | **REST APIs**                      |
| 📊 Tracking       | **Delivery Logs & Events**         |

</div>

---

# 📁 Project Structure

```text
AI-Multilingual-Mass-Communication-Platform/
│
├── 📂 backend/
│   └── Django REST API
│
├── 📂 ai-service/
│   └── FastAPI AI & Translation Service
│
├── 📂 frontend/
│   └── React + Vite Application
│
├── 📂 docs/
│   └── Project Documentation
│
├── 📂 scratch/
│   └── Development Resources
│
├── 📄 .env.example
├── 📄 .gitignore
├── ▶️ start_all.bat
├── ⏹️ stop_all.bat
└── 📖 README.md
```

---

# ⚡ Quick Start

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/lokeshboddu006/AI-Multilingual-Mass-Communication-Platform.git

cd AI-Multilingual-Mass-Communication-Platform
```

### 2️⃣ Install Dependencies

```bash
pip install -r backend/requirements.txt

pip install -r ai-service/requirements.txt

cd frontend
npm install
cd ..
```

### 3️⃣ Configure Environment

Configure the required environment variables using the provided `.env.example` files.

### 4️⃣ Start the Platform

```text
Frontend     → http://localhost:5173
Backend      → http://127.0.0.1:8000
AI Service   → http://127.0.0.1:8001
```

For local development, the repository also provides:

```text
▶ start_all.bat
⏹ stop_all.bat
```

---

# 🔄 Complete Communication Workflow

```text
                  👤 RECIPIENT
                       │
                       ▼
                🎯 AUDIENCE
                 TARGETING
                       │
                       ▼
                📝 CAMPAIGN
                 CREATION
                       │
                       ▼
                🤖 AI CONTENT
                GENERATION
                       │
                       ▼
                🌍 LANGUAGE
                TRANSLATION
                       │
                       ▼
                📡 CHANNEL
                 SELECTION
                       │
                       ▼
                🚀 DELIVERY
                       │
                       ▼
                📊 TRACKING
                       │
                       ▼
                📈 ANALYTICS
```

---

# 📡 Communication Channels

The architecture is designed around a provider-independent delivery layer.

```text
                    CAMPAIGN
                       │
                       ▼
                 DISPATCH ENGINE
                       │
            ┌──────────┼──────────┐
            ▼          ▼          ▼
          EMAIL       SMS      WHATSAPP
            │          │          │
            └──────────┼──────────┘
                       │
                 PUSH / WEB
                       │
                       ▼
                  DELIVERY
                       │
                       ▼
                    EVENTS
                       │
                       ▼
                  ANALYTICS
```

The architecture can be extended with production communication providers without changing the core campaign and tracking system.

---

# 💡 Example Use Case

## 🌪️ Emergency Awareness Campaign

Imagine a public-awareness campaign for an approaching cyclone.

```text
Create Campaign
       ↓
Select Affected Region
       ↓
Identify Target Audience
       ↓
Generate AI Message
       ↓
Translate into Required Languages
       ↓
Select Communication Channels
       ↓
Distribute
       ↓
Track Delivery
       ↓
Analyze Engagement
```

The same architecture can support health awareness, education, government schemes, public announcements, emergency notifications, and other large-scale communication scenarios.

---

# 🎯 Project Vision

> **Create the right message, reach the right audience, communicate in the right language, use the right channel, and understand what happens afterward.**

GovComm AI connects:

```text
CONTENT
   +
AUDIENCE
   +
LANGUAGE
   +
CHANNEL
   +
DELIVERY
   +
ENGAGEMENT
```

into one unified communication workflow.

---

# 🚀 Future-Ready Architecture

The platform is designed to support future integrations such as:

* 📧 Email providers
* 📱 SMS providers
* 💬 WhatsApp Business
* 🔔 Push notifications
* 🌐 Web communication
* 🔗 Provider webhooks
* ⚙️ Background processing
* 📊 Advanced analytics

---

# 📊 Project Status

<div align="center">

| Component                  |     Status     |
| :------------------------- | :------------: |
| React Frontend             |    🟢 Active   |
| Django REST Backend        |    🟢 Active   |
| FastAPI AI Service         |    🟢 Active   |
| PostgreSQL Architecture    |    🟢 Active   |
| AI Content Generation      |  🟢 Integrated |
| Indic Language Translation |  🟢 Integrated |
| Audience Management        | 🟢 Implemented |
| Campaign Management        | 🟢 Implemented |
| Delivery Architecture      | 🟢 Implemented |
| Analytics Architecture     | 🟢 Implemented |

</div>

---

# 🤝 Contributing

Contributions and improvements are welcome.

```bash
git checkout -b feature/your-feature

git add .

git commit -m "Add your feature"

git push origin feature/your-feature
```

Open a Pull Request once your changes are ready.

---

# 🌟 Support the Project

If you find **GovComm AI** interesting or useful:

⭐ Star the repository
🍴 Fork the project
🐛 Report issues
💡 Suggest improvements
🤝 Contribute

---

<div align="center">

# 🌐 GovComm AI

### AI-Powered Multilingual Mass Communication & Public Awareness Platform

<br>

**Create → Target → Generate → Translate → Distribute → Track → Analyze**

<br><br>

Built with

**React • Django • FastAPI • PostgreSQL • Groq • IndicTrans2**

<br><br>

⭐ **Star the repository if you like the project!**

</div>

<div align="center">

![GovComm AI Dashboard](docs/images/dashboard.png)

</div>

 
