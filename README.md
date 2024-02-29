# Chat Your PDF - Jupyter Notebook

This is a Jupyter Notebook version of the [Redis Chatbot for Azure OpenaAI](https://github.com/alexvasseur/redis-chatbot-azureopenai) Streamlit app.

It allows you to execute the code step by step and to examine intermediate artifacts, such as the text chunks used for generating the embeddings.

## Prerequisites

- Python 3.11
- An execution environment for Jupyter Notebook. I find that [Anaconda](https://www.anaconda.com/download) works best
- Python requirements installed: `pip install -r requirements.txt`

## Runnning the Notebook

Copy file `env.example` to `.env` and change values to reflect your environment. Note that by default the notebook is configured for a locally running Redis Stack on port 6379 - change the value of `REDIS_URL` in the cell below `Apply Config` if you want to connect to a Redis Docker container (`REDIS_URL`) or a Redis Enterprise instance on Azure (`AZURE_REDIS_URL`).
