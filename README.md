# rag-demo
rag-demo is a project that uses RAG (Retrieval Augmented Generation) to answer questions about a document. It uses LangFuse to evaluate the model's performance.

## Features

## Prerequisites

- Python 3.7+
- API keys for OpenAI  and LangFuse (for running evaluation on datasets)

## Installation and Setup

1. **Clone the Repository**:
   ```sh
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Create a Virtual Environment**:
   ```sh
   python -m venv .venv
   source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
   ```

3. **Install Dependencies**:
   ```sh
   pip install -r requirements.txt
   ```

## Configuration

1. **API Keys**: 
   - Copy the `.env.sample` file and rename it to `.env`
   - Replace the placeholder values with your actual API keys and Runpod endpoints
   - Note: Runpod keys are optional


## Running the Application

1. **Activate the Virtual Environment** (if not already activated):
   ```sh
   source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
   ```

2. **DOCUMENT RAG + LLM**:
    - Place the data you want to use in the data folder
    - Run `python3 rag_email.ipynb` to run the application

3. **GMAIL RAG  + LLM**:
   - Create a project in Google Cloud
   - Go to APIs & Services -> Library, search for Gmail, and enable it, Use external if you're using a Gmail account
   - Add scope, search for gmail, and choose "gmail.readonly"

   - Go to APIs & Services -> Credentials, create a new OAuth 2.0 Client ID and download the credentials JSON file
   - Copy credentials.json to the new project folder,
   - Run `pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib`
   - Run `python3 rag_email.ipynb` to run the application

3. **Evaluation**:
   - Run `python3 generate_dataset.py` to generate a dataset of questions and answers from the document and upload it to LangFuse
   - Run `python3 evaluate_rag.py` to evaluate the model's performance against the dataset
## Contributing

Contributions are welcome! Please open an issue or submit a pull request with your proposed changes.

## License

This project is licensed under the MIT License.

## Contact

For any questions or inquiries, please contact the project maintainer, abhinav.tekumalla@gmail.com