GovComm AI

<p align="center">

<strong>{=html}AI-Powered Multilingual Mass Communication & Public
Awareness Platform</strong>{=html}

</p>

<p align="center">

Create • Target • Generate • Translate • Distribute • Track • Analyze

</p>

Overview

GovComm AI is a full-stack communication management platform for
creating, targeting, translating, distributing, and monitoring
public-awareness campaigns across multiple Indian languages and
communication channels.

The platform brings the complete communication lifecycle into one
workspace:

Recipients
    ↓
Audience Segmentation
    ↓
Campaign Creation
    ↓
AI Content Generation
    ↓
Indian-Language Translation
    ↓
Channel Selection
    ↓
Delivery
    ↓
Live Tracking
    ↓
Engagement Analytics

Core Capabilities

AI Content Generation

Generate communication content directly inside the platform with:

Brief

Standard

Detailed

Content can be generated for different communication scenarios and
tones, including:

Informative

Formal

Urgent

Friendly

Multilingual Communication

The platform supports multilingual communication across:

English

Hindi

Telugu

Tamil

Kannada

Malayalam

Marathi

Bengali

Gujarati

Punjabi

Odia

Urdu

Indian-language translation is integrated through AI4Bharat
IndicTrans2.

Campaign placeholders such as {{name}}, {{location}}, {{date}},
and {{message}} are preserved during translation.

Audience & Recipient Management

Create targeted audiences using recipient attributes such as:

State / Union Territory

District

City

Preferred language

Occupation / category

Organization

Other campaign-specific attributes

The recipient directory maintains structured communication information
including contact details, language and geographic context.

Campaign Management

Campaigns combine:

Content

Audience

Priority

Languages

Channels

Scheduling

Delivery tracking

Templates & Content Library

Reusable templates and content allow frequently used public-awareness
communications to be created consistently and efficiently.

Live Delivery & Tracking

The delivery layer supports a complete lifecycle:

QUEUED
   ↓
PROCESSING
   ↓
SENT
   ↓
DELIVERED
   ↓
READ / OPENED
   ↓
CLICKED

Failure handling:

FAILED
   ↓
RETRYING
   ↓
PROCESSING
   ↓
SENT / DELIVERED

Tracking includes:

Delivery KPIs

Delivery funnel

Recipient-level status

Channel analytics

Language analytics

Event timestamps

Failures

Retries

Engagement events

Architecture

                         ┌─────────────────────┐
                         │    React + Vite     │
                         │     Frontend        │
                         └──────────┬──────────┘
                                    │
                             REST / Authentication
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │     Django REST     │
                         │   Core Application  │
                         └───────┬───────┬─────┘
                                 │       │
                       Database  │       │ AI
                                 │       ▼
                                 │ ┌───────────────┐
                                 │ │    FastAPI    │
                                 │ │  AI Service   │
                                 │ └───────┬───────┘
                                 │         │
                                 │    ┌────┴────┐
                                 │    │         │
                                 │   Groq   IndicTrans2
                                 │
                                 ▼
                         ┌─────────────────────┐
                         │     PostgreSQL      │
                         │   Primary Database  │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │ Delivery & Tracking │
                         │ Events + Analytics  │
                         └─────────────────────┘

Technology Stack

Layer                   Technology

Frontend                React + Vite
Core Backend            Django + Django REST Framework
AI Service              FastAPI
Primary Database        PostgreSQL
Development Database    SQLite support
Authentication          JWT
AI Generation           Groq
Translation             AI4Bharat IndicTrans2
API                     REST
Delivery Architecture   Provider abstraction
Tracking                DeliveryLog + DeliveryEvent
Channels                Email, SMS, WhatsApp, Push, Web
Development             VS Code / Antigravity IDE

Authentication note: If Firebase Authentication / Google OAuth is
enabled in the current deployment, it can be used as the identity
layer alongside the existing JWT-protected API architecture. Keep
provider-specific configuration in environment variables and never
commit credentials.

Authentication & Security

The platform provides an authenticated workspace for communication
administrators and creators.

The authentication architecture is designed around:

User Identity
     ↓
Authenticated Session
     ↓
JWT-Protected API
     ↓
Profile / Permissions
     ↓
Campaign Workspace

Security considerations include:

Secure password hashing through the backend authentication system

JWT-protected API endpoints

Role-aware authorization

Environment-based secret management

No credentials committed to source control

API validation

Delivery-event idempotency

Controlled placeholder handling

For production deployment, configure HTTPS, secure token/cookie
policies, rate limiting, secret management and verified provider
webhooks.

Database

PostgreSQL is the primary relational database for the platform.

It stores structured application data including:

Users and profiles

Recipients

Audiences

Campaigns

Templates

Content

Delivery records

Delivery events

Tracking information

The Django ORM and migration system provide schema management and
relational integrity.

AI Service

The AI layer is separated from the core Django application through a
dedicated FastAPI service.

React
  ↓
Django REST
  ↓
FastAPI AI Service
  ├── Content Generation
  └── Translation

This separation keeps AI functionality modular and allows the AI layer
to evolve independently from the core application.

The AI generation layer uses the configured LLM provider, while
Indian-language translation is handled through the IndicTrans2
integration.

Delivery Architecture

The delivery system is provider-independent.

Campaign
   ↓
Dispatch Engine
   ↓
Channel Interface
   ├── Email
   ├── SMS
   ├── WhatsApp
   ├── Push
   └── Web
   ↓
Provider
   ↓
Delivery Event
   ↓
Database
   ↓
Analytics

This architecture allows production communication providers to be
connected through channel adapters without rewriting the core delivery
tracking system.

The delivery layer includes:

Dispatch engine

Provider abstraction

Delivery logs

Delivery events

Retry handling

Webhook-ready event processing

Idempotency

Campaign analytics

Delivery Events

The platform tracks communication events such as:

MESSAGE_QUEUED
MESSAGE_SENT
MESSAGE_DELIVERED
MESSAGE_READ
MESSAGE_CLICKED
MESSAGE_FAILED
MESSAGE_RETRIED
MESSAGE_CANCELLED

Provider event identifiers can be used to prevent duplicate events from
incorrectly affecting analytics.

India Geography

The platform includes reusable geographic targeting for India with:

State / Union Territory
        ↓
District
        ↓
City / Location

The same geography structure can be reused across:

Recipient management

Audience creation

Campaign targeting

Profile information

Project Structure

project-root/
│
├── backend/
│   ├── api/
│   │   ├── delivery/
│   │   │   ├── providers/
│   │   │   └── services/
│   │   ├── migrations/
│   │   ├── services/
│   │   └── tests/
│   ├── manage.py
│   └── ...
│
├── ai-service/
│   ├── providers/
│   ├── services/
│   ├── config.py
│   ├── main.py
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   │   ├── api/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── context/
│   │   └── App.jsx
│   ├── package.json
│   └── ...
│
└── README.md

Local Development

Requirements

Python 3.12+

Node.js

npm

PostgreSQL

Git

Backend

python -m venv backend_venv

Windows

backend_venv\Scriptsctivate

Install dependencies:

pip install -r backend/requirements.txt

Run migrations:

cd backend
python manage.py migrate

Start Django:

python manage.py runserver 127.0.0.1:8000

AI Service

cd ai-service
pip install -r requirements.txt

Configure environment variables in .env.

Example:

GROQ_API_KEY=your_key_here
GEMINI_API_KEY=your_key_here
AI_SERVICE_URL=http://127.0.0.1:8001

Start FastAPI:

uvicorn main:app --host 127.0.0.1 --port 8001

Frontend

cd frontend
npm install
npm run dev

Local Services

Service              URL

React + Vite         http://localhost:5173
Django REST API      http://127.0.0.1:8000
FastAPI AI Service   http://127.0.0.1:8001
AI Health Check      http://127.0.0.1:8001/health

Testing

Backend validation:

python manage.py check

Run backend tests:

python manage.py test

Delivery tests:

python manage.py test api.tests.test_delivery

Frontend production build:

npm run build

Example Workflow

A public-awareness campaign can follow this lifecycle:

1. Authenticate
        ↓
2. Manage Recipients
        ↓
3. Build Audience
        ↓
4. Generate Content
        ↓
5. Translate Content
        ↓
6. Create Campaign
        ↓
7. Select Channels
        ↓
8. Dispatch
        ↓
9. Track Delivery
        ↓
10. Analyze Engagement

Example

A cyclone-awareness campaign can be created, targeted to relevant
geographic audiences, generated using AI, translated into required
Indian languages, prepared for multiple channels, and then monitored
through the delivery dashboard.

Production Integration Roadmap

The architecture is designed to support production integrations such as:

Email delivery providers

Indian SMS providers

WhatsApp Business

Firebase Cloud Messaging

Production webhook endpoints

Background job processing

Advanced monitoring

Production analytics

Provider credentials should always be stored through secure
environment/secret management.

Project Vision

GovComm AI is built around one simple principle:

Create the right message, reach the right audience, communicate in
the right language, use the right channel, and understand what happens
afterward.

The platform connects:

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

into one unified communication workflow.

Project

GovComm AI
AI-Powered Multilingual Mass Communication & Public Awareness
Management Platform

Repository

lokeshboddu006-AI-Multilingual-Mass-Communication-Platform

Create → Target → Generate → Translate → Distribute → Track → Analyze#   l o k e s h b o d d u 0 0 6 - A I - M u l t i l i n g u a l - M a s s - C o m m u n i c a t i o n - P l a t f o r m  
 #   l o k e s h b o d d u 0 0 6 - A I - M u l t i l i n g u a l - M a s s - C o m m u n i c a t i o n - P l a t f o r m  
 