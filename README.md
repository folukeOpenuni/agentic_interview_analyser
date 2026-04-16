# agentic_interview_analyser

---

### 🎯 Project Title

**Agentic AI Interview Analyzer**

---

### 📌 Description

An **agentic AI system** that analyzes a job interview transcript and provides structured, actionable feedback to help users improve their interview performance.

The system will:

* Extract **questions asked** by the interviewer
* Identify **answers given** by the candidate
* Evaluate the **quality and correctness** of responses
* Provide **constructive feedback and improvements**
* Suggest **better sample answers**

This will simulate a personalized interview coach powered by LLM agents.

---

### 🚀 Objectives

* Help users **understand how well they performed** in an interview
* Provide **clear, structured feedback** instead of vague suggestions
* Demonstrate **agentic AI workflows (multi-step reasoning, evaluation, critique)**

---

### 🧠 Core Features

#### 1. Transcript Ingestion

* Accept input as:

  * Raw text
  * Uploaded file (TXT/PDF)
* Optional: Speech-to-text integration (future scope)

---

#### 2. Question & Answer Extraction Agent

* Parse transcript into:

  * Interviewer questions
  * Candidate answers
* Handle messy or unstructured conversations

---

#### 3. Evaluation Agent

For each Q&A pair:

* Determine:

  * **Relevance** of the answer
  * **Correctness** (if technical/knowledge-based)
  * **Clarity & structure**
* Assign a **score (e.g., 1–10)**

---

#### 4. Feedback & Improvement Agent

* Highlight:

  * Missing points
  * Weak explanations
  * Communication issues
* Suggest:

  * **Improved version of the answer**
  * **Key points that should have been included**

---

#### 5. Output Formatter

Return structured output like:

```
Question 1:
"What is REST API?"

Your Answer:
"..."

Evaluation:
- Correctness: 7/10
- Clarity: 6/10

Feedback:
- Missed explanation of statelessness
- Example was weak

Improved Answer:
"A REST API is..."
```

---

### ⚙️ Technical Approach

#### Architecture 

* **Frontend**: Angular/React or Streamlit chatbot UI
* **Backend**: Python (FastAPI or Flask)
* **LLM**: Local model via Ollama and ChatGPT when deployed
* **Agent Framework**:

  * Option 1: LangChain Agents
  * Option 2: Custom agent orchestration 

---

#### Agent Flow

1. **Parser Agent** → splits transcript into Q&A
2. **Evaluator Agent** → scores answers
3. **Critic Agent** → identifies weaknesses
4. **Improver Agent** → rewrites better answers
5. **Coordinator Agent** → orchestrates flow

---

### 📊 Success Criteria

* Accurately extracts ≥80% of Q&A pairs
* Provides **clear, non-generic feedback**
* Generates **useful improved answers**

---

### 🔥 Stretch Goals

* Domain-aware evaluation (e.g., software engineering vs HR questions)
* STAR method detection for behavioral questions
* Voice input + real-time feedback
* Scoring dashboard (visual analytics)
* Fine-tuned evaluation prompts per job role

---

### ⚠️ Challenges / Risks

* Transcript parsing can be messy
* LLM hallucination when judging “correctness”
* Maintaining consistent evaluation criteria
* Latency with multi-agent pipelines

---


### System Design Diagram
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/141dd9d1-087a-4ece-9088-5ff0c9c42e0c" />


