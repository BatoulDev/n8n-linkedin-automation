# n8n LinkedIn Automation 

This project is an end-to-end **LinkedIn content automation workflow** built with **n8n**, combining AI text generation, AI image generation, human approval, and automated publishing.

It is designed to help individuals or organizations create high-quality LinkedIn posts efficiently while keeping full human control over approvals.

---

## Features

-  **Airtable Trigger**
  - Starts automatically when a record status is set to **Ready**

- **AI Content Generation**
  - Uses OpenAI (GPT-4) to generate professional LinkedIn posts
  - Enforces:
    - Exactly 3 sentences
    - Strong hook
    - Clear explanation
    - Call-to-action
    - No emojis

- **Human Approval Workflow**
  - Sends generated text via Gmail
  - Classifies response as **Approved** or **Rejected**
  - Regenerates content if rejected

-  **AI Image Generation**
  - Uses Replicate API to generate a professional illustration
  - Stores the image URL in Airtable
  - Requires separate approval for the image

-  **Airtable Sync**
  - Updates:
    - Generated text
    - Approved image
    - Status tracking

- **LinkedIn Publishing**
  - Automatically publishes the approved post with image
  - Supports posting as **Person** or **Organization**

---

##  Workflow Overview

1. Airtable record marked as **Ready**
2. AI generates LinkedIn post text
3. Email approval sent
4. Text classified (Approved / Rejected)
5. AI image generated
6. Image approval sent
7. Final post published to LinkedIn

---

## Tech Stack

- **n8n**
- **OpenAI (GPT-4)**
- **Replicate API**
- **Airtable**
- **Gmail API**
- **LinkedIn API**

---

##  Security Notes

> ⚠️ No API keys or secrets are stored in this repository.

All credentials (OpenAI, Airtable, Gmail, Replicate, LinkedIn) must be added **inside n8n Credentials**, not in code.





##  Setup Instructions

1. Import the JSON file into **n8n**
2. Create credentials in n8n for:
   - Airtable
   - OpenAI
   - Gmail
   - Replicate
   - LinkedIn
3. Update Airtable Base & Table IDs
4. Activate the workflow

---

##  Use Cases

- Personal branding on LinkedIn
- Company content automation
- AI-assisted social media workflows
- Approval-based publishing systems

---

## Author

**Batoul Abdulrahman**  
Full Stack Developer & Automation Engineer  

---

##  Future Improvements

- Hashtag generation
- Scheduling posts
- Multi-language support
- Analytics & engagement tracking


