# LLM Chat Application

A simple, standalone web-based chat interface for LLMs using the Cerebras API. Built with vanilla JavaScript, HTML, and CSS.

## Features

- **Clean, Modern Interface**: Intuitive chat UI similar to popular platforms like ChatGPT and Claude
- **Cerebras API Integration**: Access to GPT OSS 120B LLM model through a single interface
- **Rich Text Support**: Markdown rendering and code syntax highlighting
- **File Upload**: Add context to your prompts by uploading text files
- **Streaming Responses**: See model responses in real-time as they're generated
- **Conversation Management**: Save, load, export, and import conversations
- **Advanced Settings**: Fine-tune model parameters like `temperature`, `top_p`, and more
- **Persistence**: Chat history stored in `localStorage` for data preservation
- **Mobile Responsive**: Works well on desktop, tablet, and mobile devices

## Getting Started

### Prerequisites

- A Cerebras API key (sign up at [cloud.cerebras.ai](https://cloud.cerebras.ai))
- A modern web browser (Chrome, Firefox, Safari, Edge)
- A web server (optional for local development)

### Installation

1. Clone this repository:
   ```
   git clone https://github.com/SuperGamer474/cerebras-web.git
   ```

2. Navigate to the project directory:
   ```
   cd cerebras-web
   ```

3. Open the `index.html` file in your browser or serve it with a local server

For a simple local server, you can use Python:
```
# Python 3
python -m http.server

# Python 2
python -m SimpleHTTPServer
```

Then access the application at `http://localhost:8000`.

### Usage

1. Type your message in the input field at the bottom of the screen
2. (Optional) Upload text files by clicking the paperclip icon
3. Press Enter or click the send button to submit your message
4. View the model's response as it streams in real-time

## The Model

The application supports the 'GPT OSS 120B' model from Cerebras.

## Advanced Settings

The application provides numerous settings to customize model behavior:

- **Temperature**: Controls randomness (0.0 to 2.0)
- **Top P**: Controls diversity via nucleus sampling (0.0 to 1.0)
- **Top K**: Limits choice to K top tokens (0 or above)
- **Frequency Penalty**: Reduces repetition based on frequency in input (-2.0 to 2.0)
- **Presence Penalty**: Reduces repetition regardless of frequency (-2.0 to 2.0)
- **Repetition Penalty**: Reduces repetition based on token probability (0.0 to 2.0)
- **Min P**: Minimum probability relative to most likely token (0.0 to 1.0)
- **Top A**: Dynamic Top-P based on highest probability token (0.0 to 1.0)
- **Seed**: For deterministic responses
- **Max Tokens**: Maximum number of tokens to generate
- **Logprobs**: Return log probabilities of output tokens
- **Top Logprobs**: Number of most likely tokens to return at each position
- **Streaming**: Stream the response as it's generated
- **Reasoning Tokens**: Controls the amount of reasoning (thinking) tokens the model uses

## File Upload Support

The application supports uploading text-based files to provide context for your prompts. Supported file types include:

- Plain text (.txt)
- Markdown (.md)
- Code files (.js, .html, .css, .py, etc.)
- Data files (.json, .csv, etc.)

When you upload a file, its content will be appended to your prompt in a structured format.

## Managing Conversations

- **Export Chat**: Save the current conversation as a JSON file
- **Import Chat**: Load a previously exported conversation
- **Delete Chat**: Remove the current conversation from history

## Keyboard Shortcuts

- **Enter**: Send message
- **Shift+Enter**: Newline in message
- **Ctrl+N** / **Cmd+N**: New chat


All data is stored locally in your browser using `localStorage`. Your API key is stored in `sessionStorage` and is only valid for the current session.

## Security Note

This application handles API keys directly in the browser, which carries security risks as it exposes your API key to anyone inspecting the page's source code or network requests. This implementation is intended for personal use only.

## License

This project is licensed under the MIT License.

## Acknowledgments

- Cerebras API for providing access to the LLM model
- **josephgodwinkimani** for the original openrouter-web code
- Bootstrap team for the responsive design framework
- Any & all the open-source libraries used in this project

