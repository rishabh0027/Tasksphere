# 🚀 TaskSphere

## Intelligent Team Task & Collaboration Management Platform

**TaskSphere** is a full-stack team productivity and collaboration platform designed to centralize task management, team communication, project coordination, scheduling, file sharing, notifications, approvals, and organizational workflows within a single workspace.

The platform combines a responsive **React + Vite frontend**, a **Node.js + Express backend**, **MongoDB**, and **Socket.IO** for real-time communication. It also integrates services such as **Google Calendar, Cloudinary, email, scheduled reminders, voice-assisted task creation, audit logging, and PDF reporting**.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Why TaskSphere](#why-tasksphere)
- [Core Features](#core-features)
- [System Architecture](#system-architecture)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Authentication & Authorization](#authentication--authorization)
- [Real-Time Communication](#real-time-communication)
- [Task Management](#task-management)
- [Voice-to-Task Creation](#voice-to-task-creation)
- [Google Calendar Integration](#google-calendar-integration)
- [File Management](#file-management)
- [Notifications & Reminders](#notifications--reminders)
- [Chat & Collaboration](#chat--collaboration)
- [Reporting](#reporting)
- [API Structure](#api-structure)
- [Installation & Setup](#installation--setup)
- [Environment Variables](#environment-variables)
- [Testing](#testing)
- [Deployment](#deployment)
- [Future Enhancements](#future-enhancements)
- [Author](#author)

---

## 🎯 Overview

TaskSphere is designed to solve the problem of managing team productivity across multiple disconnected tools.

Instead of using separate applications for:

- Task management
- Team communication
- File sharing
- Project scheduling
- Notifications
- Calendar management
- Reporting
- Administrative workflows

TaskSphere brings these capabilities together into a **single collaborative workspace**.

---

## ✨ Core Features

### ✅ Task Management

- Create and edit tasks
- Assign tasks to individuals and teams
- Bulk task assignment
- Task priorities
- Status tracking
- Start and due dates
- Task comments
- Attachments
- Task history
- Task dependencies
- Task approvals
- Search and filtering
- Deadline monitoring
- Recurring tasks

### 📊 Multiple Task Views

TaskSphere provides multiple visualization modes:

- **List View**
- **Kanban Board**
- **Calendar View**
- **Gantt / Timeline View**

These views allow teams to select the workflow that best suits their project.

### 💬 Real-Time Collaboration

Powered by **Socket.IO**, TaskSphere supports:

- Direct messaging
- Group conversations
- Real-time notifications
- Mentions
- Read status
- Message editing
- Message deletion
- Pinned messages
- Task-related communication

### 📅 Calendar Integration

TaskSphere includes Google Calendar integration for:

- Connecting calendars
- Creating task events
- Updating task events
- Removing calendar events
- Synchronizing task deadlines

### 🎙️ Voice-to-Task Creation

Users can create tasks through voice input.

The system can extract information such as:

- Task title
- Priority
- Assignee
- Due date

Example:

```text
"Create a high priority task for Rishabh by Friday"
