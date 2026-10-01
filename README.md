# AI Academic Summarizer & Quiz Generator

An AI-powered study assistant that converts academic PDFs into concise summaries, interactive flashcards, and self-assessment quizzes.

## Hackathon

**VORTEX 2K26 – Global AI Innovation Hackathon**
**Platform:** Unstop

## Problem Statement

College and engineering students spend significant time going through lengthy lecture slides, lab manuals, and textbook PDFs while preparing for examinations. Manually creating notes, flashcards, and practice questions makes revision slower and reduces the time available for active recall and self-assessment.

This project provides an interactive web application where students can upload academic documents and use AI to generate structured summaries, flashcards, and quizzes for faster and more focused revision.

## Features

### Core Features

* 📄 **PDF Upload & Parsing**

  * Upload lecture slides, lab manuals, and textbook chapters.
  * Extract and process document text for AI analysis.

* 📝 **AI Summary Generator**

  * Generates concise, structured, high-yield summaries.
  * Highlights important concepts and topics.

* 🃏 **Flashcard Generator**

  * Creates topic-based question-and-answer flashcards.
  * Designed for quick revision and active recall.

* 🧠 **AI Quiz Generator**

  * Generates MCQs and short-answer questions directly from uploaded content.
  * Supports configurable quiz lengths such as 5, 10, or 15 questions.
  * Supports different difficulty levels.

* 📊 **Interactive Quiz & Feedback**

  * Real-time score tracking.
  * Instant feedback after answering questions.
  * AI-generated explanations for incorrect answers.

### Advanced Features

* 📈 **Weak Spot Analytics**

  * Tracks quiz performance across topics.
  * Identifies areas that require additional revision.

* 📥 **Study Guide Export**

  * Export summaries, flashcards, and quiz review material as PDFs.
  * Useful for offline revision.

## Technology Stack

| Layer             | Technology          | Purpose                            |
| ----------------- | ------------------- | ---------------------------------- |
| Frontend          | React.js + Vite     | Web application interface          |
| Styling           | Tailwind CSS        | Responsive UI                      |
| API Communication | Axios / Fetch API   | Frontend-backend communication     |
| Backend           | Python + FastAPI    | REST API and application logic     |
| PDF Processing    | PyPDF2 / pdfplumber | PDF text extraction                |
| AI                | Groq API + Llama 3  | Summaries, flashcards, and quizzes |
| Database          | PostgreSQL          | Application and performance data   |
| Database Platform | Supabase            | Managed PostgreSQL                 |
| Frontend Hosting  | Vercel              | Frontend deployment                |
| Backend Hosting   | Render              | Backend deployment                 |

## System Architecture

```text
                 ┌─────────────────────┐
                 │       Student       │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   React + Vite      │
                 │   Tailwind CSS      │
                 └──────────┬──────────┘
                            │
                       REST API
                            │
                            ▼
                 ┌─────────────────────┐
                 │      FastAPI        │
                 │      Backend        │
                 └──────┬──────┬───────┘
                        │      │
              ┌─────────┘      └──────────┐
              ▼                           ▼
     ┌─────────────────┐          ┌─────────────────┐
     │ PDF Processing  │          │    Groq AI      │
     │ PyPDF2/pdfplumber│         │    Llama 3      │
     └────────┬────────┘          └────────┬────────┘
              │                            │
              └────────────┬───────────────┘
                           ▼
                  ┌─────────────────┐
                  │   PostgreSQL    │
                  │    / Supabase   │
                  └─────────────────┘
```

## Project Workflow

```text
Upload PDF
    ↓
Extract Document Text
    ↓
Clean & Process Content
    ↓
Send Content to AI Pipeline
    ↓
Generate
 ┌───────────────┬───────────────┬───────────────┐
 │   Summary     │  Flashcards   │     Quiz      │
 └───────────────┴───────────────┴───────────────┘
    ↓
Display Results
    ↓
Track Quiz Performance
    ↓
Identify Weak Topics
```

## Team

| Member             | Role                        | Responsibilities                                                                |
| ------------------ | --------------------------- | ------------------------------------------------------------------------------- |
| **Anjankumar B H** | Frontend / Full-Stack Lead  | React application, UI components, API integration, state management, deployment |
| **Aditthya S S**   | Backend / AI Pipeline Lead  | FastAPI, PDF processing, Groq integration, database, backend deployment         |
| **B M Shubhank**   | UI/UX, Product & Pitch Lead | Figma designs, UX, pitch deck, demo video, presentation                         |

## Development Plan

### Phase 1 — Hours 0–6

* Define application architecture.
* Establish API contracts.
* Create initial Figma wireframes.
* Set up GitHub repository and development environments.

### Phase 2 — Hours 6–20

* Implement PDF processing pipeline.
* Integrate Groq AI.
* Develop summary and flashcard generation.
* Build React interface and quiz components.

### Phase 3 — Hours 20–28

* Connect frontend and backend.
* Implement end-to-end document processing.
* Test quiz generation and scoring.
* Fix integration and UI issues.

### Phase 4 — Hours 28–36

* Deploy frontend to Vercel.
* Deploy backend to Render.
* Perform final testing.
* Finalize pitch deck and demo video.
* Prepare hackathon submission.

## Expected Output

The completed application will allow students to:

1. Upload an academic PDF.
2. Extract and process its content.
3. Generate concise AI-powered summaries.
4. Create interactive study flashcards.
5. Generate customizable practice quizzes.
6. Receive immediate quiz feedback.
7. Track performance by topic.
8. Export study material for offline revision.

## Repository Structure

```text
ai-academic-summarizer/
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
│
├── backend/
│   ├── app/
│   ├── requirements.txt
│   └── ...
│
├── docs/
│   ├── architecture/
│   └── ...
│
├── README.md
└── .gitignore
```

## Future Improvements

* Support for additional document formats.
* Personalized question generation based on previous performance.
* More detailed learning analytics.
* Subject/topic-based study plans.
* Improved document chunking for very large PDFs.
* Additional AI-generated learning resources.

## Project Status

🚧 **Hackathon Project — In Development**

Built as part of **VORTEX 2K26 – Global AI Innovation Hackathon**.
