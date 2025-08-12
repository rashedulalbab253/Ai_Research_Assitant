# Multi Agent Research Assistant

A modular, multi-agent research pipeline powered by [CrewAI](https://github.com/joaomdmoura/crewAI). This project automates topic research, data analysis, and report generation—each handled by a specialist AI agent for efficiency, structure, and extensibility.

---

## 🚀 Features

- **Automated, multi-step research workflow**  
- **Specialist agents** for research, analysis, and writing  
- **Configurable via environment variables**  
- **Extensible:** add or modify agents/tasks easily  
- **Markdown outputs** for research, analysis, and final report  

---

## 🗂️ Project Structure

```
.
├── agents/
│   ├── research_specialist.py   # Research agent
│   ├── data_analyst.py         # Analyst agent
│   └── content_writer.py       # Content writer agent
├── tasks/
│   ├── research_task.py        # Research task
│   ├── analysis_task.py        # Analysis task
│   └── writing_task.py         # Writing/report task
├── crew.py                     # Crew & pipeline assembly
├── main.py                     # Main entrypoint
├── env_template.txt            # Environment variable template
└── README.md                   # Project documentation
```

---

## ⚙️ Setup & Usage

### 1. Clone the Repository

```sh
git clone https://github.com/yourusername/yourrepo.git
cd yourrepo
```

### 2. Install Dependencies

```sh
pip install -r requirements.txt
```

### 3. Configure Environment Variables

- Copy the template and insert your API keys:
  ```sh
  cp env_template.txt .env
  ```
- Edit `.env` with your actual keys and LLM preferences.

### 4. Run the Project

```sh
python main.py
```
- The default topic is `"AI Agents"`. Change it in `main.py` for your own research.

---

## 🛠️ Customization

- **Change topic:**  
  Edit the `topic` in `main.py` or modify the script for CLI input.

- **Add/modify agents or tasks:**  
  - Place new agents in `agents/`
  - Place new tasks in `tasks/`
  - Register them in `crew.py`

- **Tune LLM and temperature:**  
  Adjust per-agent LLM and temperature in your `.env` file.

---

## 📄 Output

- `research_findings.md` — Collected research
- `analysis_report.md` — Analytical review
- `final_report.md` — Polished, comprehensive report

---

## 🔑 Environment Variables

See `env_template.txt` for all required variables. Example:

```text
GROQ_API_KEY=your-groq-api-key-here
SERPER_API_KEY=your-serper-api-key-here
RESEARCH_AGENT_LLM=groq/llama-3.3-70b-versatile
RESEARCH_AGENT_TEMPERATURE=0.1
...
```

---

## 🏗️ Built With

- [CrewAI](https://github.com/joaomdmoura/crewAI)
- Python 3.9+

---

## 🤝 Credits

Project by [rashedulalbab253](https://github.com/rashedulalbab253)

---

*Feel free to use, extend, and contribute!*
