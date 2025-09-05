# Multimodal Finanicial Agent with Phidata

The system consists of:
1. A Web Search Agent: Retrieves the latest financial news.
2. A Finance AI Agent: Analyzes stocks, fundamentals, technical indicators, and recommendations.
3. A Multi-Agent Assistant: Combines both agents to provide enriched, structured analysis with sources and clarity.

## 1. Prerequisites

Ensure you have the following before proceeding:
1. Python 3.12 (or equivalent)
2. Basic knowledge of Python and APIs

API keys:
PHIDATA_API_KEY (from Phidata/Agno platform)
GROQ_API_KEY (for using Groq as your LLM provider)
OPENAI_API_KEY (for using openAI)

## Create Virtual Environment & Install Dependencies
conda create -p venv python=3.12
conda activate venv
pip install -r requirements.txt

## Tips:
1. Set up API keys correctly: Make sure your .env file contains valid PHIDATA_API_KEY and GROQ_API_KEY. The application won't work if these keys are missing or incorrect.
2. Test each agent individually before combining: Run web_search_agent and finance_agent separately to make sure they work as expected. This helps you catch issues early before creating a multi-agent assistant.
3. Install all required dependencies: Use a requirements.txt file and run pip install -r requirements.txt
4. Use clear and specific prompts: Agents work better when you ask direct questions. Avoid vague queries. For example, use “Analyze Apple stock for the past week” instead of “Tell me about Apple.”
5. Avoid hitting API rate limits: External APIs like Groq or yFinance may restrict how many times you can access them in a short period. Space out your requests during development and testing.
6. Check system performance and memory usage: Large models or multi-agent workflows can use a lot of memory. Running everything on limited hardware may cause crashes or delays.