# Multiple PDF Chatbot 🤖📄

[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)](https://streamlit.io/)
[![LangChain](https://img.shields.io/badge/LangChain-00A67D?style=for-the-badge)](https://python.langchain.com/)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21F?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/)

An AI-powered chatbot that lets you ask questions about your PDF and DOCX documents using natural language processing.

![Demo Screenshot](demo.png) <!-- Replace with your actual demo image -->

## Features ✨

- Upload and process multiple PDF/DOCX files simultaneously
- Natural language question answering
- Conversation history and context awareness
- Powered by HuggingFace's Flan-T5 model
- Local FAISS vector storage for efficient searching
- Simple Streamlit web interface

## Prerequisites 🛠️

- Python 3.8+
- Git
- HuggingFace account (for API token)

## Installation ⚙️

1. Clone the repository:
```bash
git clone https://github.com/himanshu9470/Multiple-PDF-chatbot-.git
cd Multiple-PDF-chatbot-

2. Set up virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create `.env` file (from the template):
```bash
cp .env.example .env
```

5. Add your HuggingFace token to `.env`:
```env
HUGGINGFACEHUB_API_TOKEN=your_token_here
```

## Usage 🚀

1. Run the application:
```bash
streamlit run app.py
```

2. In your browser:
- Upload PDF/DOCX files using the sidebar
- Click "Process" to analyze documents
- Ask questions in the chat interface

## Configuration ⚙️

Customize in `app.py`:
- `chunk_size` and `chunk_overlap` in `get_text_chunks()`
- LLM parameters (temperature, max_length)
- Change model by modifying `model_name` in `get_conversation_chain()`

## Project Structure 📂

```
Multiple-PDF-chatbot-/
├── app.py                # Main application
├── requirements.txt      # Dependencies
├── .env.example          # Environment template
├── .gitignore           # Ignored files
└── README.md            # This file
```

## Troubleshooting 🐛

- **API errors**: Verify your HuggingFace token in `.env`
- **Memory issues**: Reduce `chunk_size` in `app.py`
- **Slow performance**: Try smaller model like "google/flan-t5-small"
- **Secret scanning**: Never commit actual tokens, use `.env.example`

## Contributing 🤝

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License 📜

MIT License - see [LICENSE](LICENSE) for details.

---

**Note**: Always keep your `.env` file private and never commit API tokens to version control.
```

### Additional Files You Should Create:

1. **requirements.txt** (include all dependencies):
```
streamlit
langchain
PyPDF2
python-docx
faiss-cpu
huggingface-hub
git-filter-repo
python-dotenv
```

2. **.env.example**:
```
HUGGINGFACEHUB_API_TOKEN=your_token_here
```

3. **.gitignore**:
```
.env
__pycache__/
*.pyc
*.pdf
*.docx
venv/
```
