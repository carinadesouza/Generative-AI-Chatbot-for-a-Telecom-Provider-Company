# Generative AI Chatbot — Telecom Customer Support

> 🥈 **2nd Best Project — MIT ADT University** (selected from 2,000+ submissions)

A customer support chatbot built for telecom providers, powered by a Large Language Model through the OpenRouter API. The system handles common support queries automatically — data plans, billing, SIM activation, network issues — using structured prompt engineering to keep responses accurate and on-topic.

Built as an academic project exploring how Generative AI can reduce support workload without sacrificing response quality.

---

## The problem it solves

Telecom support teams deal with the same questions hundreds of times a day. Most of them have clear, consistent answers. This chatbot handles that layer — freeing up human agents for cases that actually need them.

It covers:
- Data plan queries and usage issues
- SIM activation and number porting
- Network troubleshooting
- Billing and payment questions
- Service upgrades and plan changes

---

## How it works

The user sends a message through the web interface. The Flask backend receives it, wraps it in a structured prompt that constrains the model to act as a telecom support agent, and sends it to the OpenRouter API. The response comes back, gets processed, and is returned to the user. Every interaction — along with any feedback the user submits — is logged for evaluation.

```
User message
     ↓
Flask API
     ↓
Prompt engineering layer
     ↓
OpenRouter LLM
     ↓
Response processing
     ↓
User + feedback logger
```

The prompt engineering layer is what keeps the model focused. Without it, LLMs tend to go off-script. The structured prompts define the chatbot's persona, scope, and response style — so it behaves like a support agent, not a general assistant.

---

## Tech stack

| | |
|---|---|
| Language | Python |
| Backend | Flask |
| LLM | OpenRouter API |
| Frontend | HTML (Jinja2 templates) |
| Data | JSON |
| Dev tools | Git |

---

## Project structure

```
Generative-AI-Chatbot-for-a-Telecom-Provider-Company/
├── main.py              # Flask app — routes, LLM integration, feedback logging
├── data/                # Telecom knowledge base / training context
├── templates/           # HTML frontend templates
├── requirements.txt
└── .gitignore
```

---

## Getting started

**Prerequisites:** Python 3.8+, an [OpenRouter API key](https://openrouter.ai)

```bash
# Clone the repo
git clone https://github.com/carinadesouza/Generative-AI-Chatbot-for-a-Telecom-Provider-Company.git
cd Generative-AI-Chatbot-for-a-Telecom-Provider-Company

# Create virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Add your API key
echo "OPENROUTER_API_KEY=your_key_here" > .env
```

```bash
# Run the app
python main.py
```

App runs at `http://localhost:5000`

---

## API endpoints

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/chat` | Send a message, receive an AI response |
| `POST` | `/feedback` | Submit feedback on a response |

### Example

```bash
curl -X POST http://localhost:5000/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "How do I activate my new SIM card?"}'
```

```json
{
  "response": "To activate your SIM, insert it into your device and restart...",
  "session_id": "abc123",
  "status": "success"
}
```

---

## Feedback and evaluation

Every chatbot response can be rated by the user. That feedback is stored in JSON and used to:

- Track which query types the model handles well vs. poorly
- Identify gaps in the prompt engineering
- Guide iterative improvements to response quality

It's a simple loop: deploy → collect feedback → improve prompts → redeploy.

---

## What I built

This was a collaborative project. My contributions:

- Designed and built the Flask backend architecture
- Integrated the OpenRouter LLM API
- Wrote the prompt engineering strategies that keep the model on-topic
- Built the RESTful request–response workflow
- Designed the feedback logging and evaluation system
- Implemented API error handling for reliability

---

## Roadmap

- [ ] Conversation memory for multi-turn dialogue
- [ ] Intent classification before LLM generation
- [ ] Analytics dashboard for response quality monitoring
- [ ] Expanded telecom dataset coverage
- [ ] Production deployment

---

## Recognition

Selected as **2nd best project at MIT ADT University** out of over 2,000 submissions, recognised for technical depth and real-world applicability of Generative AI in an enterprise support context.

---

## Authors

**Carina Desouza** — [github.com/carinadesouza](https://github.com/carinadesouza)  
**Rohit Nanda Naik** — system design, use case analysis, performance evaluation

---

## License

Academic project. Please get in touch before reusing or distributing.
