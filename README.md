# AI-Powered Conversational Agent

This project implements an advanced AI-powered conversational agent with capabilities including document retrieval, web search, and image generation. The agent utilizes long-term memory, performs document analysis, and generates adaptive responses using Large Language Models (LLMs) and vector databases.

## Features

- Natural language conversation with context-aware responses
- Document retrieval and analysis for informed answers
- Web search integration for up-to-date information
- Image generation based on user requests
- Long-term memory storage and retrieval
- Adaptive response generation using LLMs
- Modular architecture for easy extensibility

## Prerequisites

- Python 3.8+
- pip (Python package manager)

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/ai-powered-agent.git
   cd ai-powered-agent
   ```

2. Create a virtual environment (optional but recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

4. Set up environment variables:
   - Copy the `.env.example` file to `.env`
   - Fill in the required API keys and configuration values in the `.env` file

## Configuration

Edit the `.env` file to configure the following:

- API keys (OpenAI, Google Search, Tavily)
- LLM model and temperature
- Embeddings model
- Vector store directory
- URLs for document loading
- Logging level

## Usage

### Running the Chat Interface

To start the conversational agent with a command-line interface:

```
python chat.py
```

### Running the Gradio Web Interface

To launch the Gradio web interface for the agent:

```
python gradio_chat.py
```

## Project Structure

- `chat.py`: Main script for the command-line chat interface
- `gradio_chat.py`: Gradio web interface for the chat
- `config.py`: Configuration and environment variable management
- `chains.py`: LangChain chain definitions and utility functions
- `document_loader.py`: Functions for loading and processing documents
- `evaluation.py`: Evaluation metrics and dataset creation
- `graph.py`: Workflow graph definition using LangGraph
- `graph_functions.py`: Functions used in the workflow graph
- `graph_state.py`: State management for the workflow graph
- `memory_utils.py`: Long-term and short-term memory management
- `prompts.py`: Prompt templates for various agent tasks
- `scraping_utils.py`: Web scraping utilities
- `tools.py`: Custom tools for web search and other functionalities

## Extending the Agent

To add new capabilities to the agent:

1. Implement new functions in `graph_functions.py`
2. Add new prompt templates in `prompts.py` if needed
3. Update the workflow graph in `graph.py` to incorporate new functions
4. Modify `chat.py` or `gradio_chat.py` to expose new features in the interface

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
