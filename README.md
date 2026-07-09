# 📋 Smart To-Do List using n8n, WhatsApp & OpenAI

## Overview

This project is an AI-powered **Smart To-Do List** built using **n8n**, **WhatsApp Cloud API**, **OpenAI Chat Model**, **AI Agent**, and **Google Sheets**. It allows users to manage their daily tasks directly through WhatsApp using natural language commands.

The workflow is fully automated using n8n. Incoming WhatsApp messages are captured through the **WhatsApp On Message** node and forwarded to an **AI Agent** connected to the **OpenAI Chat Model**. The AI Agent understands the user's intent and automatically performs the requested action by interacting with Google Sheets. Users can create new tasks, retrieve existing tasks, update task details, or delete completed tasks without manually accessing the spreadsheet. Once the requested operation is completed, the workflow automatically sends a confirmation or the requested information back to the user through WhatsApp.

This project demonstrates how conversational AI can simplify everyday task management by combining workflow automation, natural language processing, and cloud-based data storage into a single intelligent system.

---

## Features

- 💬 Manage tasks directly through WhatsApp
- 🤖 AI-powered task management using the OpenAI Chat Model
- ➕ Create new tasks using natural language
- 📋 View all existing tasks
- ✏️ Update task details
- ❌ Delete completed or unnecessary tasks
- 📊 Store and manage tasks in Google Sheets
- ⚡ Fully automated workflow using n8n
- 🔌 REST API integration between WhatsApp, OpenAI, and Google Sheets
- 🚀 Easily scalable with additional AI tools and integrations

---

## Workflow

```text
User
   │
   ▼
WhatsApp Message
   │
   ▼
WhatsApp Trigger (On Message)
   │
   ▼
AI Agent
   │
   ▼
OpenAI Chat Model
   │
   ▼
Determine User Intent
   │
   ├───────────────┬───────────────┬───────────────┐
   ▼               ▼               ▼               ▼
Create Task     Get Tasks     Update Task     Delete Task
   │               │               │               │
   └───────────────┴───────────────┴───────────────┘
                   │
                   ▼
             Google Sheets
                   │
                   ▼
         WhatsApp Send Message
                   │
                   ▼
                  User
```

---

## Tech Stack

- **n8n** – Workflow Automation
- **WhatsApp Cloud API** – Receive and send WhatsApp messages
- **OpenAI Chat Model** – AI-powered natural language understanding
- **AI Agent** – Interprets user requests and executes the appropriate tool
- **Google Sheets** – Stores and manages task records
- **REST APIs** – Enables communication between WhatsApp, OpenAI, Google Sheets, and n8n

---

## How It Works

1. A user sends a message to the WhatsApp chatbot describing a task-related request.
2. The **WhatsApp On Message** node receives the incoming message.
3. The message is passed to the **AI Agent**.
4. The AI Agent sends the request to the **OpenAI Chat Model** to understand the user's intent.
5. Based on the detected intent, the AI Agent automatically selects one of the available tools:
   - **Create Task** – Adds a new task to Google Sheets.
   - **Get Tasks** – Retrieves existing tasks from Google Sheets.
   - **Update Task** – Modifies an existing task.
   - **Delete Task** – Removes a task from Google Sheets.
6. After the requested operation is completed, the AI Agent generates a response.
7. The **WhatsApp Send Message** node sends the confirmation or requested information back to the user.

---

## Example Commands

```text
Add a task to complete the project by Friday.

Create a reminder to call the client tomorrow.

Show all my pending tasks.

Update task 3 to "Submit assignment before 8 PM."

Delete task number 5.

What tasks do I have today?
```

---

## Learning Outcomes

This project demonstrates:

- Workflow automation using n8n
- AI Agent implementation
- OpenAI Chat Model integration
- WhatsApp Cloud API integration
- Google Sheets CRUD operations
- REST API communication
- Conversational AI development
- Intelligent tool calling with AI Agents
- End-to-end task management automation

---

## Future Enhancements

- 🧠 Conversation memory for contextual interactions
- ⏰ Automatic task reminders via WhatsApp
- 📅 Google Calendar integration
- ⭐ Task priorities and labels
- 👥 Multi-user support
- 📊 Task completion analytics dashboard
- 🔔 Daily task summary notifications
- ☁️ Database integration with MySQL, PostgreSQL, or MongoDB
- 📱 Web dashboard for task management
- 🎤 Voice command support

---

## License

This project is created for educational purposes and portfolio demonstration. Feel free to fork, modify, and extend the workflow to build your own AI-powered Smart To-Do List application.
