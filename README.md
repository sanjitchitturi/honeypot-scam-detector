# Agentic Honeypot for Scam Detection

An AI powered honeypot system designed to detect scam messages and autonomously engage scammers using believable victim personas. The system extracts actionable intelligence while maintaining conversation realism and contextual continuity.

---

## Overview

This project simulates real victims to interact with potential scammers after detecting fraudulent intent. It enables intelligence gathering such as contact details, financial identifiers, and malicious links, which can be used for analysis, reporting, or research.

---

## Features

- Advanced scam detection powered by Claude AI  
- Multiple victim personas for realistic engagement  
- Intelligence extraction including:
  - Phone numbers  
  - Bank account details  
  - UPI IDs  
  - URLs and phishing links  
- Conversation memory and context tracking  
- Secure API key authentication  
- Real time scam analysis  

---

## API Endpoints

### GET `/test`

Validation endpoint used to confirm authentication and service availability.

**Headers**

```
x-api-key: your_api_key
```

**Response**

Authentication confirmation message.

---

### POST `/api/honeypot/analyze`

Primary analysis and engagement endpoint.

**Headers**

```
x-api-key: your_api_key
```

**Request Body**

```json
{
  "message": "Congratulations! You won $10000",
  "conversation_id": "conv_123"
}
```

**Functionality**

- Detects scam indicators in the message  
- Generates persona driven responses  
- Maintains conversation context  
- Extracts intelligence where possible  

---

## Environment Variables

| Variable | Description |
|---------|-------------|
| `ANTHROPIC_API_KEY` | Claude API key |
| `HONEYPOT_API_KEY` | API authentication key (default: `hackathon_secret_key_12345`) |

---

## Local Development

Install dependencies and run locally:

```bash
pip install -r requirements.txt
export ANTHROPIC_API_KEY="your_key"
python main.py
```

---

## Deployment

The service can be deployed on any Python compatible hosting platform such as:

- Render  
- Railway  
- Other cloud or VPS environments  

Ensure environment variables are configured in the deployment platform.

---

## Use Cases

- Scam research and intelligence gathering  
- Fraud pattern analysis  
- Security experimentation and red teaming  
- Awareness and educational demonstrations  

---

## Repository Metadata

- Language: Python  
- Status: Active development  
- Releases: None published  
- Packages: None published  

---

## Disclaimer

This project is intended for research, security testing, and educational purposes only. Ensure compliance with local laws and platform policies when deploying or operating honeypot systems.
