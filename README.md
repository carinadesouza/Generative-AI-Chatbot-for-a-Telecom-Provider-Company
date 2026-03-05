# 📡 Generative AI Telecom Support Chatbot

> **🥈 Second Best Project — MIT ADT University** (Selected from 2000+ projects)

A Generative AI–powered customer support chatbot designed to automate telecom query handling using Large Language Models (LLMs). Built with a modular Flask backend, structured prompt engineering, and a feedback-driven evaluation system.

---

## 🚀 Overview

Customer support in the telecom industry is burdened by high volumes of repetitive queries. This project demonstrates how Generative AI can automate support interactions while maintaining accuracy, consistency, and scalability.

The chatbot handles telecom queries including:

- 📶 Data plan issues
- 📱 SIM activation
- 🔧 Network troubleshooting
- 💳 Billing inquiries
- ⬆️ Service upgrades

---

## 🧠 Key Features

| Feature | Description |
|---|---|
| 🤖 **LLM-Powered Responses** | Uses OpenRouter API to generate intelligent, context-aware answers |
| 🔗 **API-Based Architecture** | Modular Flask backend with RESTful request–response workflows |
| 🧩 **Prompt Engineering** | Structured prompts to control model behaviour and ensure consistent outputs |
| 📊 **Feedback Logging** | User feedback captured and stored for performance evaluation |
| ⚙️ **Error Handling** | Robust API error handling for stable, reliable chatbot behaviour |
| 📈 **Performance Monitoring** | Feedback data enables iterative improvement of responses |

---

## 🏗️ System Architecture

```
User Interface
      │
      ▼
Flask Backend API
      │
      ▼
Prompt Engineering Layer
      │
      ▼
OpenRouter LLM API
      │
      ▼
Response Processing
      │
      ▼
User Feedback Logging & Evaluation
```

---

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| **Language** | Python |
| **Backend Framework** | Flask |
| **LLM Integration** | OpenRouter API |
| **Data Handling** | JSON |
| **Logging** | Custom feedback storage system |
| **Dev Tools** | Git, Postman |

---

## ⚙️ Getting Started

### Prerequisites

- Python 3.8+
- An [OpenRouter API](https://openrouter.ai/) key

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/telecom-ai-chatbot.git
cd telecom-ai-chatbot

# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

```

### Configuration

Create a `.env` file in the root directory:

```env
OPENROUTER_API_KEY=your_api_key_here
```

### Run the Application

```bash
python app.py
```

The Flask server will start at `http://localhost:5000`.

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/chat` | Send a user query and receive an AI response |
| `POST` | `/feedback` | Submit feedback for a chatbot response |

### Example Request

```bash
curl -X POST http://localhost:5000/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "How do I activate my new SIM card?"}'
```

### Example Response

```json
{
  "response": "To activate your SIM card, please follow these steps...",
  "session_id": "abc123",
  "status": "success"
}
```

---

## 📊 Feedback & Evaluation Module

The feedback logging system captures user responses to chatbot outputs, enabling:

- ✅ Monitoring of response quality
- 🔍 Identification of incorrect or weak responses
- 🔄 Iterative improvement of prompt design

Feedback is stored in structured JSON format and can be used for offline analysis and model performance evaluation.

---

## 🔮 Future Improvements

- [ ] Conversation memory for multi-turn dialogue
- [ ] Intent classification layer before LLM generation
- [ ] Dashboard analytics for chatbot performance visualisation
- [ ] Expanded telecom dataset coverage
- [ ] Production deployment as a web application

---

## 👩‍💻 Team

  **Rohit Nanda Naik**
- Contributed to system design and use case analysis
- Evaluated chatbot performance and response quality
- Supported analysis of user feedback and system effectiveness

**Project Collaborator** **Carina Vima De Souza**
- Designed and implemented the Flask backend architecture
- Integrated the OpenRouter LLM API
- Developed structured prompt engineering strategies
- Implemented RESTful request–response workflows
- Designed the feedback logging and evaluation system
- Implemented API error handling and reliability mechanisms


---

## 🏆 Recognition

> 🥈 **Second Best Project — MIT ADT University**
> Selected from over 2,000 university projects for strong technical execution and real-world relevance in applying Generative AI to telecom customer support.

---

## 📄 License

This project is for academic purposes. Please contact the team before reuse or distribution.
