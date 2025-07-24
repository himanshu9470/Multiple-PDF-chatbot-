```markdown
# Multiple PDF Chatbot 📄💬

[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)](https://streamlit.io/)
[![LangChain](https://img.shields.io/badge/LangChain-00A67D?style=for-the-badge)](https://python.langchain.com/)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21F?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/)

A conversational AI chatbot that can answer questions about your PDF and DOCX documents using natural language processing.

![Demo GIF](demo.gif) <!-- You can add a demo GIF later -->

## Features ✨

- Upload and process multiple PDF/DOCX files simultaneously
- Chat interface for natural language questions
- Context-aware conversations with memory
- Uses state-of-the-art Flan-T5 LLM from HuggingFace
- Local vector storage with FAISS for efficient document retrieval
- Streamlit web interface for easy interaction

## Prerequisites 🛠️

- Python 3.8+
- Git
- HuggingFace account (for API token)

## Installation ⚙️

1. Clone the repository:
```bash
git clone https://github.com/himanshu9470/Multiple-PDF-chatbot-.git
cd Multiple-PDF-chatbot-
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file and add your HuggingFace token:
```env
HUGGINGFACEHUB_API_TOKEN=your_token_here
```

## Usage 🚀

1. Run the Streamlit app:
```bash
streamlit run app.py
```

2. Upload your PDF/DOCX files using the sidebar

3. Click "Process" to analyze your documents

4. Start chatting with your documents in the main interface

## Configuration ⚙️

You can modify these parameters in `app.py`:
- `chunk_size` and `chunk_overlap` in `get_text_chunks()`
- LLM parameters (temperature, max_length) in `get_conversation_chain()`
- Different HuggingFace models by changing `model_name`

## Project Structure 📂

```
Multiple-PDF-chatbot-/
├── app.py                # Main application code
├── requirements.txt      # Python dependencies
├── .env.example          # Environment variables template
├── .gitignore           # Specifies untracked files
└── README.md            # This file
```

## Troubleshooting 🐛

- **Error loading HuggingFace model**: Ensure you have a valid API token in `.env`
- **Memory issues**: Reduce chunk size in `get_text_chunks()`
- **Slow performance**: Try a smaller model like "google/flan-t5-small"

## Contributing 🤝

Contributions are welcome! Please open an issue or submit a pull request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License 📜

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments 🙏

- [LangChain](https://python.langchain.com/) for the NLP framework
- [HuggingFace](https://huggingface.co/) for the Flan-T5 model
- [Streamlit](https://streamlit.io/) for the web interface
```

To complete your repository, you should also:

1. Add a `requirements.txt` file with all dependencies
2. Create a `.env.example` file (without your actual token)
3. Add a LICENSE file (MIT recommended for open source)
4. Create a demo GIF showing the app in action