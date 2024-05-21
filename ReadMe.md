**WhatsApp Chat Analyzer**
=====================================


Welcome to the WhatsApp Chat Analyzer, a containerized FastAPI project that leverages Large Language Models (LLMs) to analyze and summarize WhatsApp chats, providing valuable insights on relationships.

**Getting Started**
-------------------

To get started with this project, follow these steps:
1.  **Clone the repository**: Run `git clone https://github.com/your-username/whatsapp-chat-analyzer.git`
2.  **Create a `.env` file**: Copy the `.env.template` file and create a new file named `.env`. Fill in your environment variables accordingly.
    * Set `MAIL_USER=`, `MAIL_PASS=`, `MAIL_SENDER=`, `MAIL_HOST=`, and `MAIL_PORT=` to configure email settings (this is needed to be able to receive the results).
    * Set `HF_TOKEN` and make sure you have access to the tokenizer of your chosen model. (e.g. for LLAMA3, you can get access [here](https://huggingface.co/meta-llama/Meta-Llama-3-8B))
    * Set `TOKENIZERS_PARALLELISM=false` to control tokenization parallelism.
    * Set `OLLAMA_URL="http://localhost:11434/api/generate"` to specify the URL where OLLAMA should be run.
    * Set `MODEL_NAME="llama3"` to specify the name of the model you want to use for analysis. Supported models are 
      * `llama3` (default, performs best according to our tests)
      * `dolphin-2.6-mixtral-8x7b`
      * `mistralai/Mixtral-8x7B-Instruct-v0.1`
      * `Qwen1.5-32B-Chat`
3.  **Start the Docker container**: Run `docker-compose up` to start the containerized FastAPI application.

**About this project**
-------------------

The WhatsApp Chat Analyzer is designed to help users gain insights into their relationships by analyzing WhatsApp chats. The project uses a pre-trained LLM to summarize conversations and identify key themes, relationship and chronological progression. This information can be used to improve communication, resolve conflicts, or simply better understand the dynamics of a relationship.

**Key features**
-----------------

*  **Conversational analysis**: Leverage an LLM to analyze WhatsApp chat logs and generate summaries.
*  **Insight generation**: Identify key themes, relationship progression, and chronological trends in conversations.
*  **Relationship insights**: Provide actionable recommendations for improving communication and strengthening relationships. (coming soon, maybe ;) )

**Technical details**
--------------------

This project is built using:
- FastAPI: A modern Python web framework for building APIs.
- Docker: Containerization for easy deployment and management.
- LLMs (Large Language Models): Utilize pre-trained models for natural language processing tasks. In specific, this project uses OLLAMA (big shoutout to the team at [OLLAMA](https://ollama.com/).)
