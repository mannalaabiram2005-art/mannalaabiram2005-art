<div align="center">

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=22&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&width=700&lines=Mannala+Abiram+%7C+AI+Engineer+(LLM+%26+RAG);Agentic+RAG+%C2%B7+LangChain+%C2%B7+FastAPI+%C2%B7+FAISS+%C2%B7+ChromaDB;Shipping+full-stack+GenAI+apps+end+to+end;Open+to+AI+Engineer+%26+LLM+Application+Developer+roles" alt="Typing SVG" />
</a>

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://abi-portfolio-smb5.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abirammannala)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:abirammannala@gmail.com)
[![Resume](https://img.shields.io/badge/Resume-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/14TRTlkustqs5eCR3ssIBkB9e4ykDRrIC/view?usp=drive_link)

![Open to Work](https://img.shields.io/badge/Open%20to-AI%20Engineer%20%7C%20LLM%20Applications%20%7C%20GenAI-2ea44f?style=flat-square)
![Graduating](https://img.shields.io/badge/B.Tech%20CS-2026-58A6FF?style=flat-square)
![Location](https://img.shields.io/badge/Based%20in-India-orange?style=flat-square)
![Profile Views](https://komarev.com/ghpvc/?username=mannalaabiram2005-art&label=Profile%20Views&color=58A6FF&style=flat-square)

</div>

---

## 👋 About Me

I'm **Mannala Abiram**, a B.Tech Computer Science graduate (2026) who builds **LLM applications, RAG pipelines and tool-calling agents**, and wraps them in real **FastAPI backends and React frontends**. I care about the full path from raw documents to a working product: ingestion, retrieval, orchestration, API, UI and measurement.

- 🔭 **Built:** [InsightAI](https://github.com/mannalaabiram2005-art/InsightAI), an agentic RAG app with persistent multi-turn memory, and [AI Resume Shortlister](https://github.com/mannalaabiram2005-art/AI_RESUME_SHORTLISTER), a semantic resume-ranking engine.
- 🌱 **Learning next:** Model Context Protocol (MCP), RAG evaluation (RAGAS, DeepEval), multi-agent patterns, pgvector and Docker-based deployment.
- 🎯 **Looking for:** AI Engineer, LLM Application Developer, Generative AI Engineer and internship roles.
- 💬 **Ask me about:** RAG pipelines, chunking and retrieval tuning, LangChain agents, vector search, FastAPI backend design.
- 📫 **Reach me:** [abirammannala@gmail.com](mailto:abirammannala@gmail.com) · [LinkedIn](https://www.linkedin.com/in/abirammannala)

---

## 📊 Results at a Glance

| Project | Measured outcome |
|---|---|
| 🤖 **InsightAI** | Answer accuracy raised **90% → 95%** on an internal test set by tuning chunk size and top-5 retrieval; **~2 s** average response across 20 documents |
| 🧾 **AI Resume Shortlister** | **200 resumes screened in 65 s** (vs. an estimated 2–3 hours manually); **80%** agreement with manual shortlisting; **95%** extraction accuracy |
| 🏥 **MediQ** | **5 REST endpoints** load-tested with **500 concurrent users** at **~1 s** average response; JWT auth with **4 user roles** |

<sub>Figures come from my own test sets and samples (internal test set, 200 labeled resumes, load test), as described in each project README and on my resume.</sub>

---

## 🚀 Featured Projects

### 🤖 [InsightAI](https://github.com/mannalaabiram2005-art/InsightAI) — Full-Stack Agentic RAG Application
Multi-turn question answering over uploaded **PDF, TXT and Markdown** files. A LangChain agent decides between **document retrieval** and **real-time web search**, then returns grounded answers with Llama 3.1 running on Groq.

`Python` `LangChain` `FastAPI` `Groq (Llama 3.1)` `ChromaDB` `Hugging Face Embeddings` `SQLAlchemy` `SQLite` `React` `Vite` `Tailwind CSS`

```mermaid
flowchart LR
    A[Upload PDF / TXT / MD] --> B[Parse and chunk]
    B --> C[HF embeddings]
    C --> D[(ChromaDB)]
    U[User question] --> G{LangChain agent}
    G -->|document question| D
    G -->|needs fresh info| W[Web search]
    D --> L[Llama 3.1 on Groq]
    W --> L
    L --> R[Grounded answer]
    R --> M[(SQLite chat memory)]
    M --> G
```

- Ingestion and retrieval pipeline with a persistent vector store; chunk size and top-k tuned to lift accuracy from 90% to 95%.
- Persistent chat memory (SQLite + SQLAlchemy) for context-aware conversations across sessions.
- React + Vite + Tailwind interface built end to end.

### 🧾 [AI Resume Shortlister](https://github.com/mannalaabiram2005-art/AI_RESUME_SHORTLISTER) — Recruitment Automation
Parses bulk PDF resumes and ranks candidates against a job description with **Sentence Transformers embeddings and FAISS similarity search**, using a configurable relevance threshold.

`Python` `LangChain` `Sentence Transformers` `FAISS` `FastAPI` `Streamlit`

```mermaid
flowchart LR
    subgraph Ingest["Resume ingestion"]
        A["Bulk PDF resumes"] --> B["Text parsing"]
        B --> C["Profile extraction<br/>name, email, phone, skills"]
        B --> D["Sentence Transformers<br/>embeddings"]
        D --> E[("FAISS index")]
    end
    subgraph Match["Matching"]
        J["Job description"] --> K["Sentence Transformers<br/>embedding"]
        K --> S{"FAISS similarity search"}
        E --> S
        S --> T["Relevance threshold"]
    end
    T --> R["Ranked candidates"]
    C --> R
    R --> API["FastAPI endpoints"]
    R --> UI["Streamlit dashboard"]
```

- Extracts names, emails, phone numbers and skills into structured, recruiter-ready results.
- Streamlit dashboard and FastAPI endpoints to view ranked candidates and screening output.

### 🏥 [MediQ](https://github.com/mannalaabiram2005-art/Smart_Appointment) — Full-Stack Healthcare Management System
Doctor discovery, appointment booking and digital health records with a responsive React interface.

`React.js` `FastAPI` `PostgreSQL` `SQLAlchemy` `JWT`

```mermaid
flowchart LR
    U["Patient / Doctor / Admin / Pharmacist"] --> FE["React.js frontend<br/>responsive UI"]
    FE -->|"REST + JWT"| AUTH{"JWT auth and<br/>role-based access"}
    subgraph BE["FastAPI backend"]
        AUTH --> RT["Routes"]
        RT --> SV["Services"]
        SV --> DM["Data models"]
    end
    DM --> ORM["SQLAlchemy"]
    ORM --> DB[("PostgreSQL")]
    SV -.-> F1["Doctor discovery"]
    SV -.-> F2["Appointment booking"]
    SV -.-> F3["Digital health records"]
```

- JWT authentication and role-based authorization for patients, doctors, administrators and pharmacists.
- Backend structured into routes, services and data-model layers for maintainability.

### 🌐 [Portfolio](https://abi-portfolio-smb5.vercel.app/)
Responsive personal site with project case studies, deployed on Vercel.

---

## 🧠 What I Work On

| Area | What I've actually built with |
|---|---|
| 🔎 **RAG** | Document parsing, chunking, embeddings, top-k retrieval tuning, grounded answers |
| 🤖 **Agents** | ReAct-style tool-calling agents (LangChain) that route between retrieval and web search |
| 🗂️ **Vector search** | FAISS, ChromaDB |
| ⚙️ **Backend** | FastAPI, REST API design, JWT auth, SQLAlchemy, PostgreSQL, SQLite |
| 🖥️ **Frontend** | React, Vite, Tailwind CSS, Streamlit |
| 🧾 **Applied NLP** | Resume parsing, entity extraction, semantic ranking |

---

## 🛠️ Tech Stack

<table>
<tr>
<td><b>Languages</b></td>
<td>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" title="Python" alt="Python" width="40" height="40"/>&nbsp;
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" title="JavaScript" alt="JavaScript" width="40" height="40"/>&nbsp;
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg" title="SQL" alt="SQL" width="40" height="40"/>&nbsp;
</td>
</tr>
<tr>
<td><b>LLM &amp; AI</b></td>
<td>
<img src="https://api.iconify.design/simple-icons/langchain.svg?color=%231C3C3C" title="LangChain" alt="LangChain" width="40" height="40"/>&nbsp;
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/scikitlearn/scikitlearn-original.svg" title="scikit-learn" alt="scikit-learn" width="40" height="40"/>&nbsp;
<img src="https://cdn.simpleicons.org/huggingface" title="Hugging Face" alt="Hugging Face" width="40" height="40"/>&nbsp;
</td>
</tr>
<tr>
<td><b>Backend &amp; APIs</b></td>
<td>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/fastapi/fastapi-original.svg" title="FastAPI" alt="FastAPI" width="40" height="40"/>&nbsp;
<img src="https://cdn.simpleicons.org/swagger/85EA2D" title="REST API" alt="REST API" width="40" height="40"/>&nbsp;
<img src="https://cdn.simpleicons.org/jsonwebtokens" title="JWT" alt="JWT" width="40" height="40"/>&nbsp;
</td>
</tr>
<tr>
<td><b>Frontend</b></td>
<td>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" title="React" alt="React" width="40" height="40"/>&nbsp;
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vitejs/vitejs-original.svg" title="Vite" alt="Vite" width="40" height="40"/>&nbsp;
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/tailwindcss/tailwindcss-original.svg" title="Tailwind CSS" alt="Tailwind CSS" width="40" height="40"/>&nbsp;
<img src="https://cdn.simpleicons.org/streamlit" title="Streamlit" alt="Streamlit" width="40" height="40"/>&nbsp;
</td>
</tr>
<tr>
<td><b>Data &amp; Vector DBs</b></td>
<td>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg" title="PostgreSQL" alt="PostgreSQL" width="40" height="40"/>&nbsp;
<img src="https://www.vectorlogo.zone/logos/sqlite/sqlite-icon.svg" title="SQLite" alt="SQLite" width="40" height="40"/>&nbsp;
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pandas/pandas-original.svg" title="Pandas" alt="Pandas" width="40" height="40"/>&nbsp;
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/numpy/numpy-original.svg" title="NumPy" alt="NumPy" width="40" height="40"/>&nbsp;
</td>
</tr>
<tr>
<td><b>Tools</b></td>
<td>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/git/git-original.svg" title="Git" alt="Git" width="40" height="40"/>&nbsp;
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/github/github-original.svg" title="GitHub" alt="GitHub" width="40" height="40"/>&nbsp;
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg" title="Docker (basic)" alt="Docker" width="40" height="40"/>&nbsp;
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/jupyter/jupyter-original.svg" title="Jupyter" alt="Jupyter" width="40" height="40"/>&nbsp;
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" title="Linux" alt="Linux" width="40" height="40"/>&nbsp;
</td>
</tr>
</table>

**Also:** Groq (Llama 3.1) · Sentence Transformers · FAISS · ChromaDB · SQLAlchemy · Prompt Engineering · Conversational Memory

---

## 📈 GitHub Activity

<div align="center">

![Stats](https://github-readme-stats.vercel.app/api?username=mannalaabiram2005-art&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=mannalaabiram2005-art&layout=compact&theme=tokyonight&hide_border=true)

</div>

---

## 🎓 Education & Learning

**B.Tech, Computer Science** — Anantha Lakshmi Institute of Technology & Sciences, JNTU Anantapur (2026)
**Certifications:** Artificial Intelligence Fundamentals (IBM) · Data Analysis & Decision Making (NPTEL)

**Learning roadmap**

- [x] LangChain agents and tool calling
- [x] FAISS and ChromaDB vector search
- [x] FastAPI backends with JWT auth
- [ ] LangGraph state machines
- [ ] Model Context Protocol (MCP) integrations
- [ ] LLM evaluation (RAGAS, DeepEval)
- [ ] Multi-agent orchestration
- [ ] pgvector and Docker-based AI service deployment

## 🎯 2026 Goals

- 📌 Join a team as an AI Engineer / LLM Application Developer
- 📌 Add an evaluation harness (RAGAS) to InsightAI and publish the results
- 📌 Write up lessons from tuning RAG retrieval
- 📌 Contribute to an open-source RAG or agent project

---

## 🤝 Let's Connect

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abirammannala)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:abirammannala@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://abi-portfolio-smb5.vercel.app/)
[![Resume](https://img.shields.io/badge/Resume-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/14TRTlkustqs5eCR3ssIBkB9e4ykDRrIC/view?usp=drive_link)

<sub>⭐ If my work is useful or interesting, a star on the repos is appreciated. Thanks for visiting!</sub>

</div>
