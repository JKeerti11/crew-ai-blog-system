

# CrewAI Blog Automation System

A multi-agent AI automation system built with CrewAI and Google Gemini.  
This project demonstrates how specialized AI agents can collaborate to research and generate high-quality technical blog content automatically.

---

## Overview

This system uses two AI agents working sequentially:

1. A Research Agent that analyzes emerging trends in a given topic.
2. A Writer Agent that transforms research findings into a structured blog article.

The workflow is orchestrated using CrewAI with a sequential process, ensuring that research output feeds directly into the writing stage.

---

## Architecture

The system consists of:

- **LLM Provider**: Google Gemini (`gemini-1.5-flash`)
- **Framework**: CrewAI
- **Agents**:
  - Senior Researcher
  - Writer
- **Execution Mode**: Sequential process
- **Output Format**: Markdown blog post

Workflow:

Input Topic → Research Agent → Writer Agent → Markdown Blog Output

---

## Project Structure

```

.
├── agents.py        # Agent definitions
├── tasks.py         # Task definitions
├── crew.py          # Crew orchestration and execution
├── requirements.txt
└── README.md

````

---

## Features

- Role-based AI agents with defined goals and backstories
- Task delegation and structured collaboration
- Automatic research and blog generation
- Markdown output file creation
- Environment-based API key management
- Extensible multi-agent architecture

---

## Requirements

- Python 3.9+
- Google Gemini API Key
- pip

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/your-repository-name.git
cd your-repository-name
````

Install dependencies:

```bash
pip install -r requirements.txt
```

Create a `.env` file in the root directory:

```
GOOGLE_API_KEY=your_api_key_here
```

---

## Usage

Run the project:

```bash
python crew.py
```

By default, the topic is set inside `crew.py`.
You can modify the topic input inside:

```python
crew.kickoff(inputs={'topic': 'AI in healthcare'})
```

The generated blog post will be saved as:

```
new-blog-post.md
```

---

## Customization

You can extend the system by:

* Adding more specialized agents
* Introducing additional tasks
* Switching to parallel execution
* Integrating vector databases for long-term memory
* Connecting to external APIs for real-time data
* Deploying as a web service

---

## Security Note

Do not commit your `.env` file or API keys.

Add this to your `.gitignore`:

```
.env
__pycache__/
*.pyc
```

---

## Example Use Cases

* Automated technical blogging
* Market research automation
* Industry trend analysis
* AI newsroom pipelines
* Content generation workflows

---

## License

Specify your preferred license here (MIT, Apache 2.0, etc.).

---

## Acknowledgments

* CrewAI Framework
* Google Gemini API
* Python ecosystem contributors

##Output
<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/78ec4bdf-2547-4989-a74f-7c5932673279" />
---

