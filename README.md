# Document Q&A Chatbot with LangChain and Gemini

An intelligent document chatbot that leverages Google's Gemini AI and LangChain to provide accurate answers from your PDF documents. Built with modern AI tools including Chroma vector store for efficient document retrieval.

## Features

- PDF document loading and processing
- Text embedding using Google's Gemini AI
- Vector storage with Chroma DB
- Interactive chat interface using Gradio
- Question-answering capabilities using LangChain

## Prerequisites

- Python 3.12+
- Google AI Studio API key for Gemini
- PDF documents to process

## Setup

1. Clone the repository
2. Create a virtual environment:
```bash
python -m venv langchain_env
source langchain_env/bin/activate  # On Windows: .\langchain_env\Scripts\activate
```

3. Install dependencies:
```bash
pip install langchain langchain-google-genai langchain-community langchain-chroma chromadb gradio python-dotenv
```

4. Create a `.env` file in the project root:
```
GEMINI_API_KEY=your_api_key_here
```

## Project Structure

```
.
├── documents/         # Place your PDF files here
├── chroma_data/      # Vector store data
├── chatbot.ipynb     # Main notebook with implementation
├── .env             # Environment variables
└── README.md
```

## Usage

1. Place your PDF documents in the `documents/` directory
2. Run the Jupyter notebook:
```bash
jupyter notebook chatbot.ipynb
```

3. Execute the cells in order to:
   - Load and process documents
   - Initialize the vector store
   - Start the chat interface

4. Access the chat interface at the provided local URL

## How it Works

1. Documents are loaded and split into chunks
2. Text chunks are embedded using Gemini's embedding model
3. Embeddings are stored in Chroma vector store
4. User questions are processed through a retrieval chain
5. Relevant context is retrieved and used to generate answers
6. Responses are presented through a Gradio chat interface

## License

MIT

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.