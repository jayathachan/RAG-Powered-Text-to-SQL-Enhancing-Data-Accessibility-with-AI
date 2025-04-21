
# RAG-Powered-Text-to-SQL-Enhancing-Data-Accessibility-with-AI<img width="651" alt="Screenshot 2025-04-20 at 11 53 49 PM" src="https://github.com/user-attachments/assets/69576a01-4791-4d71-8b60-9829ce773266" />


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
   pip install -r chatbotapp/requirements.txt
5. Add your api key, hugging face token and database path(sqlite database path)
   Create a .env file in chatbotapp/ and add:
   ```bash
   OPENAI_API_KEY=your_openai_api_key_here
   HUGGINGFACE_API_TOKEN=your_huggingface_token_here
   DATABASE_PATH=path/to/your/database.db
6. To run the streamlit application
   ```bash
   streamlit run Q-A_app/app.py


