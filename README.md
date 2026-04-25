# 🚀 TalentBridge AI

TalentBridge AI is a full-stack Next.js application that evaluates **real skill proficiency** (not just resume claims), conducts adaptive assessments, and generates **personalized learning plans**.

---

## ✨ Features

* 🎨 Light glassmorphism UI with soft gradient background
* 📄 Upload support for `PDF`, `DOCX`, `TXT`, `JPG`, `PNG`, `JPEG`
* 📝 Textarea fallback for resume and job description
* ⚡ Automatic file parsing via `/api/parse`
* 🧠 Skill extraction and matching (`matched`, `missing`, `weak`)
* 💬 Conversational assessment with progress tracking
* 📊 AI-based evaluation with weighted scoring
* 📈 Results dashboard including:

  * Skill score progress bars
  * Missing & weak skill gap analysis
  * 7–14 day personalized learning plan
  * Curated learning resources

---
## 🧠 How It Works
1. Extract skills from resume & job description
2. Match required vs existing skills
3. Assess skills via AI-generated questions
4. Score answers (knowledge, clarity, confidence)
5. Identify weak/missing skills
6. Generate personalized learning plan

## 📌 Sample Input
Resume: React Developer with basic Node.js  
JD: Full Stack Developer (React, Node, Docker)

## 📌 Output
- Matched: React
- Missing: Docker
- Weak: Node.js

Learning Plan:
- Learn Docker basics (3 days)
- Improve Node.js APIs (4 days)

## 🔄 Navigation Flow

`Input Page → Skill Match → Assessment Chat → Results Dashboard`

---

## 🛠 Tech Stack

* Next.js (App Router, TypeScript)
* Tailwind CSS
* Node.js Route Handlers
* Groq SDK (`groq-sdk`)
* Zod
* pdf-parse (PDF parsing)
* mammoth (DOCX parsing)

---

## 🔌 API Endpoints

* `POST /api/parse`
* `POST /api/analyze-skills`
* `POST /api/generate-questions`
* `POST /api/evaluate`
* `POST /api/generate-learning-plan`

### Response Format

```json
{ "success": true, "data": {} }
```

or

```json
{ "success": false, "error": "message", "details": "optional" }
```

---

## ⚙️ Local Setup

1. Install dependencies:

```bash
npm install
```

2. Create `.env.local`:

```env
GROQ_API_KEY=your_groq_api_key_here
GROQ_MODEL=llama-3.3-70b-versatile
```

3. Start development server:

```bash
npm run dev
```

4. Open:

```
http://localhost:3000
```

---

## 🌐 Live Demo

👉 https://talentbridge-ai-2026-bo7z9c4p5-shravyas-projects-2786a280.vercel.app/

---

## 🧠 What Makes It Smart

* Goes beyond resume keywords
* Evaluates **actual understanding via questions**
* Identifies **real skill gaps**
* Suggests **adjacent, realistic learning paths**

---

## 👩‍💻 Author

**Shravya Palegarthuli**

---

## 📌 Note

* Image parsing is currently preview-only (no OCR)
* Designed as a hackathon-ready prototype with real-world extensibility

---
