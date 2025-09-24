# 🚀 Agentic AI Project Environment Setup Guide

This repository contains all the projects and required dependencies developed throughout a comprehensive Agentic AI course. By following the steps below, you can set up a development environment to run all projects seamlessly on your local machine.

## ✅ Prerequisites

Before you begin, please ensure you have the following installed on your system:

1.  **Git:** Required to clone the repository. [Git Installation Guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
2.  **Python (Version 3.10 - 3.12):** The projects are compatible with these Python versions. [Python Installation Guide](https://www.python.org/downloads/)
3.  **uv:** A fast and modern Python package manager.
    *   If you don't have `uv` installed, you can easily install it by running the following command in your terminal:
        ```bash
        curl -LsSf https://astral.sh/uv/install.sh | sh
        ```
4.  **Docker Desktop:** Required for some projects (e.g., running n8n, safe code execution in AutoGen). [Docker Desktop Installation Guide](https://docs.docker.com/desktop/)

---

## ⚙️ Setup Instructions

### Step 1: Clone the Project to Your Machine

Open your terminal and run the following command to download a copy of the project to your computer:

```bash
git clone https://github.com/ridvanyigit/agents.git
```

### Step 2: Navigate to the Project Directory

Once the download is complete, move into the project folder:

```bash
cd agents
```

### Step 3: Install the Virtual Environment and Packages

Now, we will install all the necessary Python libraries for the project with a single command.

```bash
uv sync
```

✨ **What does this command do?**
> The `uv sync` command reads the `pyproject.toml` and `uv.lock` files within the project. These files contain a complete list of all required libraries and their **exact versions**. `uv` automatically creates a virtual environment (the `.venv` folder) based on this list and installs all the packages into it. This process guarantees that the project runs in an environment **identical** to the one used during development, ensuring perfect reproducibility.

---

## 🔑 Configuring API Keys

The projects require API keys from services like OpenAI, Serper, LangSmith, etc., to function correctly.

1.  In the root directory of the project (inside the `agents/` folder), create a new file named **`.env`**.
2.  Copy the template below, paste it into your new `.env` file, and replace the placeholder values within the quotes with your own API keys.

```
# LangSmith (for tracing)
LANGCHAIN_TRACING_V2="true"
LANGCHAIN_API_KEY="ls__..."

# Models
OPENAI_API_KEY="sk-..."
DEEPSEEK_API_KEY="..."
GOOGLE_API_KEY="..."
GROQ_API_KEY="..."
OPENROUTER_API_KEY="..."
```
> **Important:** Thanks to the `.gitignore` file, your `.env` file will **never** be uploaded to GitHub. This keeps your API keys secure.

---

## ▶️ Running a Project

Congratulations! The setup is complete. You can now run any of the projects from the course. For example, to launch the user interface for the Week 6 Capstone project, run:

```bash
uv run PATH/YOUR/FOLDER/app.py
```

You are now ready to explore the world of Agentic AI
