
# RAG-Powered-Text-to-SQL-Enhancing-Data-Accessibility-with-AI <img width="651" alt="Screenshot 2025-04-20 at 11 53 49 PM" src="https://github.com/user-attachments/assets/69576a01-4791-4d71-8b60-9829ce773266" />
This project aims to make basketball analytics more accessible by empowering non-technical users to interact with complex NBA datasets using natural language. By fine-tuning an open-source LLM to translate English questions into accurate SQL queries, the system provides fact-based, grounded insights without requiring SQL knowledge.

## Project Highlights

- **Custom Dataset Pipeline**: Developed an orchestration workflow to clean, augment, and synthesize Text-to-SQL query pairs, enhancing model generalization and fine-tuning quality. 
- **Data Preprocessing**: Leveraged FAISS-based semantic retrieval to enrich queries and used Unsloth for efficient tokenization and LoRA-based fine-tuning. 
- **Baseline Comparisons**: Benchmarked against multiple models including N-Gram, Seq2Seq LSTM, and pre-trained Mistral and LLaMA.
- **LLM Fine-Tuning**: Fine-tuned a LLaMA 3.2B-Instruct model using a domain-specific NBA dataset via Unsloth, applying 5-bit quantization for GPU efficiency. 
- **Evaluation Metrics**: Assessed output quality using ROUGE-1, ROUGE-L, BLEU, and BERTScore to capture syntactic and semantic fidelity.
- **Chatbot Interface**: Implemented a Streamlit + LangChain-based chatbot to allow intuitive natural language interaction with the NBA database.
- **Local Deployment**: Deployed the quantized LLM locally using Ollama, with public access enabled through Ngrok for easy testing and demonstrations.

# To run the Q-A_app locally
1. Clone the repository to your local machine:
   ```bash
   git clone <repository-url>
   cd RAG-Powered-Text-to-SQL-Enhancing-Data-Accessibility-with-AI
2. Switch to the Chatbot branch
   ```bash
   git checkout Q-A_app
3. Create and Set up your Environment
   ```bash
   python -m venv venv
   source venv/bin/activate
4. Install the packages using `requirements.txt`
   ```bash
   pip install -r Q-A_app/requirements.txt
5. Add your api key, hugging face token and database path(sqlite database path)
   Create a .env file in Q-A_app/ and add:
   ```bash
   OPENAI_API_KEY=your_openai_api_key_here
   HUGGINGFACE_API_TOKEN=your_huggingface_token_here
   DATABASE_PATH=path/to/your/database.db
6. To run the streamlit application
   ```bash
   streamlit run Q-A_app/app.py


