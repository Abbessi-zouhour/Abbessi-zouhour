<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=28&pause=1000&color=00C4CC&center=true&vCenter=true&width=700&lines=Hey+%F0%9F%91%8B+I'm+Zouhour+Abbassi;AI+Engineer+%7C+Builder+%7C+Problem+Solver;I+turn+data+into+decisions;...and+models+into+products" alt="Typing SVG" />
</h1>

<p align="center">
  <em>I build AI systems that actually do something — trading bots, medical classifiers, recruitment engines, real-time monitors.</em><br/>
  <em>From raw data to deployed product, end to end.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Based%20in-Tunis%2C%20Tunisia-00C4CC?style=flat-square"/>
  <img src="https://img.shields.io/badge/Degree-M.Sc.%20Digital%20Technologies%20for%20Healthcare-8A2BE2?style=flat-square"/>
  <img src="https://komarev.com/ghpvc/?username=Abbessi-zouhour&style=flat-square&color=00C4CC"/>
</p>

---

## 🧬 Who I Am

I'm an **AI Engineer** specializing in building systems that go beyond the notebook — production-ready pipelines, deployed APIs, and full-stack applications where AI is a first-class citizen, not an afterthought.

My background spans **biomedical deep learning**, **NLP & LLM integration**, **computer vision**, and **full-stack development**. I've trained models on pharmaceutical datasets, built real-time trading bots with AI decision layers, and shipped recruitment platforms used by real teams.

I care about three things: **clean architecture**, **grounded AI** (models that answer from data, not hallucinations), and **shipping things that work**.

- 🎓 M.Sc. in Digital Technologies for Healthcare — ISIMS Sfax (DAAD Tunisia–Germany)
- 🔬 CNNs · U-Net · Transformers · RAG · LLM integration · real-time systems
- 📫 **abbassizouhour2001@gmail.com** · [LinkedIn](https://linkedin.com/in/zouhour-abbassi) · [GitHub](https://github.com/Abbessi-zouhour)

---

## 🛠️ Tech Stack

<table>
<tr>
<td valign="top" width="33%">

**AI / ML / DL**
```
PyTorch · TensorFlow · Keras
scikit-learn · XGBoost
Hugging Face · LangChain
OpenCV · RDKit · DeepChem
Groq · OpenAI API
```

</td>
<td valign="top" width="33%">

**Backend & APIs**
```
FastAPI · Flask · Laravel
Node.js · SQLAlchemy · Alembic
Pydantic · JWT · Uvicorn
REST · WebSocket
```

</td>
<td valign="top" width="33%">

**Frontend & Mobile**
```
Next.js · React · TypeScript
Streamlit · Flutter
Axios · Tailwind
```

</td>
</tr>
<tr>
<td valign="top">

**Databases**
```
PostgreSQL · MySQL
MongoDB · Supabase
Firebase
```

</td>
<td valign="top">

**Languages**
```
Python · TypeScript
JavaScript · PHP · Dart · SQL
```

</td>
<td valign="top">

**Tooling**
```
Git · GitHub · Postman
Ruff · Black · pre-commit
Docker (learning)
```

</td>
</tr>
</table>

---

## 🚀 Featured Projects

> *Each project is a real, deployed or deployable system — not a tutorial clone.*

---

### 📈 [TradePilot AI](https://github.com/Abbessi-zouhour/tradepilot-ai) — Full-Stack Crypto Trading Bot Platform

> *Live prices. Real strategies. 7 AI features. Zero real money at risk.*

A production-grade paper trading platform built from scratch — **FastAPI backend + Next.js frontend + PostgreSQL**, with a Binance WebSocket price feed and a complete AI layer powered by Groq.

**What makes it interesting:**

- Streams live BTC/ETH/SOL/BNB/XRP prices via Binance WebSocket and runs EMA cross signals automatically every tick
- Full strategy lifecycle: create → backtest → paper trade manually or automatically → monitor risk → close positions
- Hard risk limits enforced on **every** trade path (manual and automated) via a centralized `OrderManager`
- **7 distinct AI features**, all grounded in the trader's real live data — never model hallucination:

```
💬 Chat Assistant      → Q&A about your portfolio using live equity, PnL, and EMA trends
📊 Backtest Analyzer   → explains WHY a backtest performed as it did + suggests adjustments
🧠 Portfolio Advisor   → reviews concentration risk, diversification, asset correlation
🏗️ Strategy Builder   → plain English → structured JSON strategy → pre-fills creation form
📸 Chart Reader        → upload a TradingView screenshot → AI reads trend & patterns
📰 News Summarizer     → live CoinDesk RSS → summarized + connected to your actual holdings
🛡️ Auto-Trade Filter  → inline execution gate: approves/blocks signals before they fire,
                         fails CLOSED on any error, every decision logged + auditable
```

The AI filter is the most consequential piece: it sits **inside** the trade execution pipeline, not as an advisory panel. If the LLM call errors or returns malformed JSON, the trade is blocked — not silently allowed through.

`FastAPI` `Next.js` `PostgreSQL` `SQLAlchemy` `Groq` `Binance WebSocket` `TypeScript` `Pydantic` `JWT`

---

### 🤖 [TalentBridge](https://github.com/Abbessi-zouhour/cold-email-generation-tool) — AI-Powered Recruitment Intelligence Platform

> *One dashboard. Every recruitment workflow. AI throughout.*

A full recruitment platform built for real agency use — not a demo, a working product deployed on Streamlit Cloud and connected to a live Supabase/PostgreSQL database with role-based access control.

**What it covers end to end:**

- **CV Parser** → extracts skills, experience, and candidate data from uploaded resumes
- **ATS Scorer** → evaluates candidate fit against a job description with a structured score
- **AI Candidate Ranker** → automatically ranks a shortlist by skills, experience, and ATS compatibility
- **AI Assistant** → recruitment-focused chatbot that answers questions about candidates, jobs, and hiring decisions
- **Email Generator** → outreach, interview invitations, rejections, offer letters — one click
- **Interview Scheduler** → reminder emails + AI-generated question sets per role
- **Recruitment CRM** → companies, clients, contacts, relationships — all tracked
- **Activity Logs** → every user action (create/edit/delete/AI call) recorded and visible to admins
- **PDF Reports** → export pipeline analytics and candidate metrics on demand

`Python` `Streamlit` `Supabase` `PostgreSQL` `LangChain` `Llama 3.3 70B` `Groq` `SMTP` `RBAC`

---

### 🧪 Drug–Excipient Compatibility & Solubility Prediction

> *ROC-AUC ≈ 0.97 on a problem pharmaceutical scientists spend weeks solving manually.*

A DNN + Transformer pipeline that predicts whether a drug and excipient are chemically compatible, and whether a compound will be soluble — inputs to formulation decisions that normally require wet-lab experiments.

- Molecular feature extraction with **RDKit** and **DeepChem**
- **ChemBERTa** fine-tuned on SMILES strings for molecular representation
- Deployed as a **FastAPI** inference endpoint

`PyTorch` `ChemBERTa` `RDKit` `DeepChem` `FastAPI` `Transformers`

---

### 🎗️ Breast Cancer Detection on Mammograms

> *92% classification accuracy. Segmentation + classification in one pipeline.*

End-to-end pipeline: **Deep U-Net** segments the region of interest from raw mammogram images, then a fine-tuned **VGG16** classifies benign vs. malignant. Deployed as a Flask API for radiologist review.

`TensorFlow` `Keras` `U-Net` `VGG16` `OpenCV` `Flask`

---

### 🏥 Cardiovascular Health Monitoring

> *Real-time vitals from a wearable sensor, streamed to a mobile app.*

Mobile application for elderly cardiac monitoring — integrates a **Polar H10** chest sensor over BLE, streams heart rate data in real time, and triggers alerts on anomalies. Full backend in Node.js with Firebase + MongoDB.

`Flutter` `Firebase` `MongoDB` `Node.js` `Polar H10` `BLE`

---

### 👁️ Real-Time Object Detection System

> *94% accuracy. Runs live.*

Custom real-time object detection pipeline built on PyTorch, optimized for low-latency inference on a live video stream via OpenCV.

`Python` `PyTorch` `OpenCV`

---

### 🏢 HR & Payroll Management System

> *Full-stack internal tool for employee lifecycle and payroll automation.*

Complete HR platform: employee onboarding, contract management, leave tracking, payroll calculation, and reporting — built with Laravel and a MySQL backend, with a JavaScript frontend for analytics dashboards.

`Laravel` `MySQL` `JavaScript` `PHP`

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Abbessi-zouhour&show_icons=true&theme=radical&hide_border=true&count_private=true" height="165"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Abbessi-zouhour&layout=compact&theme=radical&hide_border=true" height="165"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Abbessi-zouhour&theme=radical&hide_border=true" height="165"/>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Abbessi-zouhour&theme=react-dark&hide_border=true" />
</p>

---

## 🌐 Let's Connect

<p align="center">
<a href="https://linkedin.com/in/zouhour-abbassi">
  <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>
<a href="mailto:abbassizouhour2001@gmail.com">
  <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>
<a href="https://github.com/Abbessi-zouhour">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>
</p>

<p align="center">
  <em>Open to AI engineering roles, research collaborations, and interesting problems.</em><br/>
  <em>If you're building something ambitious, let's talk.</em>
</p>
