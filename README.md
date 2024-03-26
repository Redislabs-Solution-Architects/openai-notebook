# Chat Your PDF - Jupyter Notebook

This repo contains Jupyter Notebook versions of the [Redis Chatbot for Azure OpenaAI](https://github.com/alexvasseur/redis-chatbot-azureopenai) Streamlit app, adapted to use "pure" OpenAI.

You can execute the code step by step and to examine intermediate artifacts, such as the text chunks used for generating the embeddings.

## Local Notebook (playground_openai.ipynb)

### Prerequisites

- Python 3.11
- An execution environment for Jupyter Notebook. I find that [Anaconda](https://www.anaconda.com/download) works best
- Python requirements installed: `pip install -r requirements.txt`

### Runnning the Notebook

Copy file `env.example` to `.env` and change values to reflect your environment. Note that by default the notebook is configured for a locally running Redis Stack on port 6379 - change the value of `REDIS_URL` in the cell below `Apply Config` if you want to connect to a Redis Docker container (`REDIS_URL`) or a Redis Enterprise instance on Azure (`AZURE_REDIS_URL`).

## Colab Notebook (playground_openai_colab.ipynb)

### Prerequisites

- A Redis database with a public URL, for example a fixed subscription in Redis Cloud. This database must include the Search module.

Your Colab environment needs to have four secrets set:

- `openai_api_key` - your OpenAI API key
- `redis_password` - the password for the default user in your Redis database
- `redis_host` - the host component of your Redis database, for example `redis-13713.c1.eu-west-1-3.ec2.cloud.redislabs.com`
- `redis_port` - the port of your Redis database, for example `13713`

### Runnning the Notebook

Click on the image below and enable your notebook for Colab secrets when prompted.

[<img src="https://github.com/Redislabs-Solution-Architects/openai-notebook/assets/116373419/1328a378-bc45-4d4c-956f-051cf9658819">](https://colab.research.google.com/github/Redislabs-Solution-Architects/openai-notebook/blob/main/playground_openai_colab.ipynb)
