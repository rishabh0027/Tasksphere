🚀 TaskSphere

## Intelligent Team Task & Collaboration Management Platform

TaskSphere is a full-stack team productivity and collaboration platform designed to bring **task management, team communication, project coordination, scheduling, file sharing, notifications, approvals, and reporting** into a single workspace.

The platform is built with a modern **React + Vite frontend**, **Node.js + Express backend**, **MongoDB database**, and **Socket.IO real-time communication layer**.

It also includes integrations and utilities for **Google Calendar, Cloudinary, voice-assisted task creation, scheduled reminders, audit logging, login activity tracking, and PDF reporting**.


# 📋 Table of Contents

- [Overview](#-overview)
- [Why TaskSphere](#-why-tasksphere)
- [Core Features](#-core-features)
- [Task Management](#-task-management)
- [Task Views](#-task-views)
- [Team Collaboration](#-team-collaboration)
- [Real-Time Communication](#-real-time-communication)
- [Voice-to-Task Creation](#-voice-to-task-creation)
- [Google Calendar Integration](#-google-calendar-integration)
- [File Management](#-file-management)
- [Notifications & Reminders](#-notifications--reminders)
- [Announcements](#-announcements)
- [Groups & Departments](#-groups--departments)
- [Approvals & Workflows](#-approvals--workflows)
- [Dashboard & Reporting](#-dashboard--reporting)
- [Audit & Login Activity](#-audit--login-activity)
- [Authentication & Authorization](#-authentication--authorization)
- [System Architecture](#-system-architecture)
- [Technology Stack](#-technology-stack)
- [Project Structure](#-project-structure)
- [API Structure](#-api-structure)
- [Environment Variables](#-environment-variables)
- [Installation](#-installation)
- [Running the Application](#-running-the-application)
- [Testing](#-testing)
- [Production Build](#-production-build)
- [Deployment](#-deployment)
- [Security](#-security)
- [Development Workflow](#-development-workflow)
- [Future Enhancements](#-future-enhancements)
- [Author](#-author)
- [License](#-license)


# 🎯 Overview

Modern teams often use separate applications for task tracking, communication, file sharing, scheduling, announcements, reporting, and employee management.

TaskSphere aims to simplify this workflow by providing these capabilities through a unified platform.

With TaskSphere, users can:

- Create and manage tasks
- Assign work to individuals or teams
- Track deadlines and progress
- Collaborate through real-time chat
- Share files and manage file versions
- Receive task and system notifications
- Manage groups and departments
- Connect tasks with Google Calendar
- Create tasks using voice input
- Manage announcements
- Track approvals
- Monitor login activity
- Review audit records
- Generate PDF reports

The application is designed around a modular full-stack architecture that separates the frontend, backend, database, real-time communication, and external service integrations.

---

# 💡 Why TaskSphere?

TaskSphere focuses on four major areas of productivity.

### 📌 Centralized Task Management

Keep tasks, priorities, deadlines, assignments, comments, files, and history in one place.

### 🤝 Team Collaboration

Enable employees and teams to communicate through real-time messaging, mentions, announcements, notifications, and shared files.

### 📊 Better Visibility

Use dashboards, multiple task views, activity records, and reports to understand project and team progress.

### ⚙️ Automation

Reduce repetitive work through reminders, scheduled jobs, calendar integration, and voice-assisted task creation.

---

# ✨ Core Features

## ✅ Task Management

TaskSphere provides a complete task lifecycle management system.

### Task Operations

- Create tasks
- Edit tasks
- Delete tasks
- Assign tasks
- Bulk task assignment
- Bulk task creation
- Update task status
- Set task priority
- Set start and due dates
- Add task descriptions
- Add task comments
- Add attachments
- Search tasks
- Filter tasks
- Track task history
- Manage task dependencies
- Support recurring tasks
- Track overdue tasks
- Support task approval workflows

---

# 📊 Task Views

TaskSphere provides multiple ways to visualize work.

### 📋 List View

A structured view for reviewing tasks with filtering and sorting capabilities.

### 🗂️ Kanban View

A board-based workflow for visually moving tasks between different statuses.

### 📅 Calendar View

A date-oriented view for monitoring scheduled tasks and deadlines.

### 📈 Gantt / Timeline View

A timeline-oriented visualization for understanding task duration, scheduling, and dependencies.

---

# 👥 Team Collaboration

TaskSphere is designed for collaborative team environments.

Users can work together through:

- Group management
- Department organization
- Task assignment
- Task comments
- Mentions
- Direct messaging
- Group chat
- Announcements
- Notifications
- File sharing
- Approvals
- Activity tracking

This allows teams to keep communication and work execution within the same platform.

---

# 💬 Real-Time Communication

TaskSphere uses **Socket.IO** for real-time communication between connected users.

### Supported capabilities

- Direct messaging
- Group messaging
- Real-time message delivery
- Message editing
- Message deletion
- Message pinning
- Read status
- User mentions
- Chat room management
- Real-time notifications

### Real-Time Flow

```text
┌──────────────┐
│   Client A   │
└──────┬───────┘
       │
       │ Socket Event
       ▼
┌─────────────────────┐
│  TaskSphere Server  │
│      Socket.IO      │
└──────────┬──────────┘
           │
           │ Broadcast / Event
           ▼
┌──────────────┐
│   Client B   │
└──────────────┘
````

This allows users to receive collaboration updates without manually refreshing the application.

---

# 🎙️ Voice-to-Task Creation

TaskSphere includes a voice-assisted task workflow.

The platform contains a transcript parsing utility that can extract structured information from natural language.

The parser can identify:

* Task title
* Priority
* Assignee
* Due date

### Example

A spoken instruction such as:

```text
Create a high priority task for Rishabh and finish it by Friday.
```

can be interpreted into structured information:

```text
Task Title  : Finish task
Priority    : High
Assignee    : Rishabh
Due Date    : Friday
```

The generated values can then be used in the task creation workflow.

---

# 📅 Google Calendar Integration

TaskSphere includes Google Calendar integration utilities.

Users can connect their Google Calendar and synchronize task-related events.

### Supported workflows

* Google OAuth authorization
* Authorization callback handling
* Token management
* Calendar connection status
* Calendar disconnection
* Create calendar events
* Update calendar events
* Delete calendar events

### Calendar Workflow

```text
Task Created
     │
     ▼
Task contains scheduling information
     │
     ▼
Google Calendar integration
     │
     ▼
Calendar Event
     │
     ▼
Task deadline synchronized
```

---

# 📁 File Management

TaskSphere supports file uploads and cloud-based file management.

The backend uses **Multer** for handling uploads and **Cloudinary** for cloud storage.

### File capabilities

* Upload files
* Store file metadata
* Associate files with tasks
* Share files
* Retrieve files
* Delete files
* Maintain file versions

The presence of a dedicated `FileVersion` model allows the application to support file version tracking.

---

# 🔔 Notifications & Reminders

TaskSphere includes a notification system for important workspace events.

Users can receive notifications related to:

* Task assignments
* Task updates
* Mentions
* Comments
* Collaboration events
* Announcements
* Deadlines
* Reminders

The backend also includes scheduled task processing using **node-cron**.

This enables recurring background operations such as reminder processing.


# 📢 Announcements

Authorized users can create and manage announcements for teams or organizations.

### Announcement capabilities

* Create announcements
* Edit announcements
* Delete announcements
* Pin announcements
* Archive announcements
* Track read status
* View announcement statistics
* Attach supporting files

Announcements provide a centralized channel for communicating important organizational information.

---

# 👨‍👩‍👧‍👦 Groups & Departments

TaskSphere provides organizational structures through groups and departments.

## Groups

Group functionality includes:

* Group creation
* Group updates
* Group deletion
* Member management
* Group-specific tasks
* Group communication

## Departments

Department functionality helps organize users according to organizational structure and responsibilities.

---

# ✅ Approvals & Workflows

TaskSphere supports structured approval workflows for tasks and organizational operations.

Approval functionality allows users to move work through controlled stages where authorization or review is required.

This provides greater accountability and visibility compared with unstructured task updates.

---

# 📊 Dashboard & Reporting

TaskSphere provides dashboard functionality for monitoring work and operational activity.

### Dashboard information can include

* Total tasks
* Pending tasks
* Completed tasks
* In-progress tasks
* Overdue tasks
* Upcoming deadlines
* Team activity
* Notifications
* Productivity information

---

## 📄 PDF Reporting

The frontend includes PDF report generation using:

```text
jsPDF
jsPDF-AutoTable
```

This allows application data to be transformed into structured reports containing tables and summary information.

---

# 🕵️ Audit & Login Activity

TaskSphere includes dedicated functionality for monitoring application activity.

## Audit Logging

Important actions can be recorded for:

* Accountability
* Administrative review
* Troubleshooting
* Change tracking
* Operational monitoring

## Login Activity

The platform also includes login activity management for tracking account access events.

This can help administrators review authentication activity and investigate unusual access patterns.

---

# 🔐 Authentication & Authorization

TaskSphere uses token-based authentication and backend authorization middleware.

### Authentication technologies

* JWT
* bcryptjs
* Google authentication support
* Express middleware

### Authentication Flow

```text
User
  │
  ▼
Login / Google Authentication
  │
  ▼
Backend Credential Validation
  │
  ▼
JWT / Authenticated Session
  │
  ▼
Protected API Request
  │
  ▼
Authentication Middleware
  │
  ▼
Authorization / Role Check
  │
  ▼
Controller
  │
  ▼
Database
```

Passwords are protected using bcrypt-based hashing.

Protected resources are validated through backend authentication middleware.

---

# 🏗️ System Architecture

TaskSphere follows a client-server architecture.

```text
                         ┌────────────────────────┐
                         │       TaskSphere       │
                         │      Web Client        │
                         └───────────┬────────────┘
                                     │
                          HTTP / REST│WebSocket
                                     │
                    ┌────────────────┴────────────────┐
                    │                                 │
             ┌──────▼───────┐                 ┌──────▼───────┐
             │    React     │                 │   Socket.IO  │
             │   Frontend   │                 │ Real-Time    │
             │    + Vite    │                 │ Communication│
             └──────┬───────┘                 └──────┬───────┘
                    │                                │
                    └──────────────┬─────────────────┘
                                   │
                              REST APIs
                                   │
                         ┌─────────▼─────────┐
                         │ Node.js + Express │
                         │      Backend      │
                         └─────────┬─────────┘
                                   │
              ┌────────────────────┼────────────────────┐
              │                    │                    │
       ┌──────▼──────┐     ┌──────▼───────┐     ┌──────▼───────┐
       │   MongoDB   │     │  Cloudinary  │     │ External APIs│
       │   Database  │     │ File Storage │     │ Google / etc.│
       └─────────────┘     └──────────────┘     └──────────────┘
```

---

# 🛠️ Technology Stack

## Frontend

| Technology        | Purpose                       |
| ----------------- | ----------------------------- |
| React 18          | User interface                |
| Vite              | Development and build tooling |
| React Router      | Client-side routing           |
| Tailwind CSS      | Styling                       |
| Axios             | REST API communication        |
| Socket.IO Client  | Real-time communication       |
| Lucide React      | UI icons                      |
| React Hot Toast   | Notifications                 |
| Day.js            | Date and time handling        |
| @hello-pangea/dnd | Drag-and-drop functionality   |
| jsPDF             | PDF generation                |
| jsPDF-AutoTable   | PDF table generation          |

---

## Backend

| Technology          | Purpose                      |
| ------------------- | ---------------------------- |
| Node.js             | Server runtime               |
| Express.js          | REST API framework           |
| MongoDB             | Database                     |
| Mongoose            | MongoDB object modeling      |
| JWT                 | Authentication               |
| bcryptjs            | Password hashing             |
| Socket.IO           | Real-time communication      |
| Cloudinary          | Cloud file/image storage     |
| Multer              | File upload processing       |
| Nodemailer          | Email functionality          |
| Google APIs         | Calendar integration         |
| Google Auth Library | Google authentication        |
| node-cron           | Scheduled jobs               |
| Stripe              | Payment integration support  |
| Razorpay            | Payment integration support  |
| UUID                | Unique identifier generation |
| Validator           | Data validation              |

---

## Development & Testing

| Technology     | Purpose                     |
| -------------- | --------------------------- |
| Git            | Version control             |
| GitHub         | Source code hosting         |
| Docker         | Containerized development   |
| Docker Compose | Local service orchestration |
| Jest           | Testing                     |
| Supertest      | API testing                 |
| Nodemon        | Development server          |
| ESLint         | Code quality                |

---

# 📂 Project Structure

```text
TaskSphere/
│
├── backend/
│   ├── src/
│   │   ├── config/
│   │   │   ├── cloudinary.js
│   │   │   ├── db.js
│   │   │   └── taskFileUpload.js
│   │   │
│   │   ├── controllers/
│   │   ├── middleware/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── tests/
│   │   └── utils/
│   │
│   ├── server.js
│   └── package.json
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── context/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   ├── App.css
│   │   ├── index.css
│   │   └── main.jsx
│   │
│   ├── vite.config.js
│   └── package.json
│
├── docker-compose.yml
├── verify-setup.js
├── package.json
├── package-lock.json
└── README.md
```

---

# 🔌 API Structure

The backend is organized into modular REST API routes.

## Authentication

```text
/api/auth
```

Handles authentication-related functionality such as:

* Login
* Logout
* Google authentication
* Session/user retrieval

---

## Users

```text
/api/users
```

Supports:

* User registration
* User retrieval
* User profile management
* User administration
* Password-related workflows
* Account activation
* Bulk user operations

---

## Tasks

```text
/api/tasks
```

Supports:

* Task creation
* Task retrieval
* Task updates
* Task deletion
* Bulk creation
* Bulk assignment
* Status updates
* Comments
* History
* Search
* Statistics
* Voice parsing
* Scheduler-related operations

---

## Chat

```text
/api/chat
```

Supports:

* Chat room management
* Message retrieval
* Sending messages
* Message editing
* Message deletion
* Message pinning
* Read status
* Room member management
* Mentions

---

## Groups

```text
/api/groups
```

Supports:

* Group creation
* Group retrieval
* Group updates
* Group deletion
* Membership management

---

## Departments

```text
/api/departments
```

Supports department-level organizational management.

---

## Notifications

```text
/api/notifications
```

Handles user notifications and notification-related workflows.

---

## Announcements

```text
/api/announcements
```

Supports announcement creation, editing, deletion, pinning, archiving, attachments, and read tracking.

---

## Calendar

```text
/api/calendar
```

Supports Google Calendar authentication and synchronization.

---

## Files

```text
/api/files
```

Handles file uploads, retrieval, sharing, and file-related operations.

---

## Settings

```text
/api/settings
```

Provides application configuration and system settings functionality.

---

## Login Activity

```text
/api/login-activity
```

Provides access to login activity and authentication records.

---

# 🔐 Environment Variables

TaskSphere uses environment variables for sensitive credentials and runtime configuration.

Create:

```text
backend/.env
```

A typical configuration may include:

```env
PORT=5000

MONGODB_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret

CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GOOGLE_REDIRECT_URI=your_google_redirect_uri

STRIPE_SECRET_KEY=your_stripe_secret_key

RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret

SMTP_USER=your_email
SMTP_PASS=your_email_password
```

The exact variable names and values should match the configuration expected by your current project implementation.

> **Never commit real credentials, API keys, tokens, or passwords to GitHub.**

For public repositories, use placeholder `.env.example` files instead.

---

# 🚀 Installation

## Prerequisites

Before running TaskSphere locally, install:

* Node.js
* npm
* Git
* Docker Desktop
* MongoDB or Docker-based MongoDB

---

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/rishabh0027/Tasksphere.git

cd Tasksphere
```

---

## 2️⃣ Install Dependencies

Install the dependencies for the project:

```bash
npm run install-all
```

This installs the dependencies required by the workspace and its applications.

---

## 3️⃣ Configure Environment Variables

Create the required environment files.

For example:

```text
backend/.env
frontend/.env
```

Add the necessary configuration values and service credentials.

---

# 🐳 Database Setup with Docker

TaskSphere includes a Docker Compose configuration for local database development.

Start the database:

```bash
npm run db:up
```

Stop the database:

```bash
npm run db:down
```

---

# 🌱 Database Seeding

Where configured, initial or demonstration data can be seeded using:

```bash
npm run seed
```

---

# ▶️ Running the Application

## Start Frontend + Backend Together

From the project root:

```bash
npm run dev
```

This starts the configured frontend and backend development processes.

---

## Start Frontend Separately

```bash
cd frontend

npm run dev
```

---

## Start Backend Separately

```bash
cd backend

npm run dev
```

---

# ❤️ Backend Health Check

When the backend is running, a health/status endpoint is available for checking service availability.

Typical local backend URL:

```text
http://localhost:5000
```

Health endpoint:

```text
http://localhost:5000/health
```

The health check can be used to verify application and database availability.

---

# 🧪 Testing

The backend includes automated testing support using:

* Jest
* Supertest

Run the project tests:

```bash
npm test
```

Or from the backend directory:

```bash
cd backend

npm test
```

Tests can be used to validate API behavior and backend functionality.

---

# 🔍 Setup Verification

TaskSphere includes a verification utility.

Run:

```bash
node verify-setup.js
```

This can help validate important local development requirements and backend configuration.

---

# 📦 Production Build

## Frontend

Build the React application:

```bash
cd frontend

npm run build
```

Preview the generated production build:

```bash
npm run preview
```

---

## Backend

Start the production backend using the configured start script:

```bash
cd backend

npm start
```

---

# ☁️ Deployment

TaskSphere includes deployment configuration suitable for modern hosting platforms.

Before deploying, configure the production environment for:

* MongoDB
* JWT
* Cloudinary
* Google OAuth
* Google Calendar
* SMTP
* Payment providers
* CORS
* Frontend API URL

After deployment, verify:

* User authentication
* Database connectivity
* Task creation
* Task assignment
* Task updates
* Real-time communication
* File uploads
* Notifications
* Calendar synchronization
* Scheduled reminders
* Reporting

---

# 🛡️ Security

TaskSphere implements several security-oriented practices.

### Authentication

* JWT-based authentication
* Password hashing using bcryptjs
* Google authentication support

### Authorization

* Protected routes
* Authentication middleware
* Role-based access control

### API Security

* Request validation
* Controlled file upload routes
* CORS configuration
* Environment-based secret management

### Production Recommendations

Before deploying publicly:

* Use HTTPS
* Rotate production secrets regularly
* Configure production CORS carefully
* Never expose private API keys
* Store secrets in hosting-platform environment variables
* Restrict database access
* Validate uploaded files
* Maintain dependency updates

---

# 🔄 Development Workflow

A typical TaskSphere workflow looks like this:

```text
                    ┌──────────────────┐
                    │      Login       │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │    Dashboard     │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │   Create Task    │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ Assign / Schedule│
                    └────────┬─────────┘
                             │
                             ▼
             ┌───────────────┴────────────────┐
             │                                │
             ▼                                ▼
      ┌──────────────┐                ┌───────────────┐
      │ Task Views   │                │ Team Chat     │
      │ Kanban/List  │                │ Notifications │
      │ Calendar/Gantt│               │ File Sharing  │
      └──────┬───────┘                └───────┬───────┘
             │                                │
             └───────────────┬────────────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │  Update Status   │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ Activity / Audit │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │     Reports      │
                    └──────────────────┘
```

---

# 🧠 Engineering Highlights

TaskSphere demonstrates practical implementation of:

* Full-stack JavaScript development
* React component architecture
* REST API development
* MongoDB data modeling
* Authentication and authorization
* JWT-based security
* Real-time WebSocket communication
* Context-based frontend state management
* Cloud file storage
* OAuth integration
* Google Calendar integration
* Background task scheduling
* Voice transcript parsing
* PDF report generation
* API testing
* Docker-based local development
* Modular backend architecture
* Role-based application workflows

---

# 🚧 Future Enhancements

Potential improvements for future versions include:

### 📊 Advanced Analytics

* Team productivity metrics
* Project performance analytics
* Task completion trends
* Resource utilization dashboards

### 🤖 Intelligent Automation

* AI-based task prioritization
* Intelligent deadline prediction
* Automated task categorization
* Smart productivity recommendations

### 📱 Mobile Experience

* Progressive Web App
* Dedicated Android/iOS application
* Push notifications
* Mobile-first task management

### 🔎 Search

* Advanced global search
* Full-text task search
* User search
* File search
* Conversation search

### 🔄 Integrations

* Slack
* Microsoft Teams
* Trello
* GitHub
* Microsoft Outlook
* Additional calendar providers

### ⚙️ DevOps

* CI/CD pipeline
* Automated testing
* Monitoring
* Error tracking
* Performance analytics

---

# 👨‍💻 Author

## Rishabh Singh

**B.Tech Computer Science Engineering**
**Specialization: Artificial Intelligence & Data Science**

### GitHub

https://github.com/rishabh0027

### LinkedIn

https://www.linkedin.com/in/rishabh-singh-r2004/

---

# 📄 License

This project is currently intended for **educational, portfolio, and software engineering demonstration purposes**.

---

# ⭐ Support

If you find TaskSphere useful or interesting, consider giving the repository a ⭐ on GitHub.

---

<div align="center">

### TaskSphere

**Plan. Collaborate. Execute.**

Built with React, Node.js, Express, MongoDB, and Socket.IO.

</div>
```
