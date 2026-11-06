# AutoClean AI: Autonomous Multi-Agent Data Engineering Pipeline

AutoClean AI is a production-grade, autonomous multi-agent pipeline designed to automate the ingestion, cleaning, validation, and visualization of messy tabular CSV datasets. By deploying a collaborative ecosystem of specialized LLM agents operating within strict governance guardrails, it eliminates fragile scripting and manual wrangling while maintaining critical human-in-the-loop oversight.

---

## Key Features

- **5-Agent Collaborative Loop:** Specialized agents split responsibilities across profiling, strategy planning, execution, validation, and dashboard creation.
- **Human-in-the-Loop Governance:** Mandatory approval checkpoints pause execution for high-risk data modifications (e.g., column drops) while low-risk imputations are auto-approved.
- **Circuit Breaker Retry Mechanism:** An automated feedback loop re-routes failed validations back to the planner with a maximum 3-attempt circuit breaker.
- **Interactive Web Canvas:** Live simulation dashboard for real-time control over LLM cost tiers, confidence thresholds, and outlier sensitivities.

---

## 🏗️ System Architecture

1. **Agent 1 (Data Inspector & Profiler):** Profiles metadata, missing values, and statistical distributions to generate diagnostic JSON reports without exceeding token limits.
2. **Agent 2 (Remediation Planner):** Formulates step-by-step Pandas transformation strategies and assigns operational risk tags.
3. **Agent 3 (Code Executor):** Translates approved plans into clean, vectorized Python Pandas code and executes safe sandbox transformations.
4. **Agent 4 (Governance Validator):** Audits post-execution data integrity against defect reports, enforcing a 3-attempt circuit breaker loop back to the planner if anomalies persist.
5. **Agent 5 (Dashboard Generator):** Produces self-contained Streamlit and Plotly application scripts with dynamic distribution charts and direct export options.

---

## 🛠️ Tech Stack

- **Core Logic & Orchestration:** Python 3.10+, Pandas, LangChain, Pydantic
- **LLM Engine:** OpenAI GPT-4o / GPT-4o-mini
- **Dashboard & UI:** Streamlit, Plotly, HTML5, CSS3, JavaScript

---

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/autoclean-multiagent-pipeline.git](https://github.com/your-username/autoclean-multiagent-pipeline.git)
cd autoclean-multiagent-pipeline
