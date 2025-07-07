# Voice Cursor 🎤

A powerful AI-powered voice-controlled coding assistant that allows you to interact with your development environment using natural speech. Built with cutting-edge technologies including OpenAI GPT-4, LangGraph, and speech recognition.

## ✨ Features

- **Voice-Controlled Coding**: Execute commands and get coding assistance through natural speech
- **AI-Powered Assistance**: Leverages OpenAI GPT-4 for intelligent code generation and problem-solving
- **Real-time Speech Recognition**: Uses Google's speech recognition API for accurate voice input
- **Persistent Conversations**: Maintains conversation context using MongoDB checkpoints
- **Tool Integration**: Can execute system commands and provide real-time feedback
- **Docker Support**: Easy deployment with Docker Compose

## 🏗️ Architecture

This project combines several advanced technologies:

- **Speech Recognition**: Google Speech Recognition API for voice input processing
- **AI Model**: OpenAI GPT-4 for intelligent responses and code generation
- **Workflow Engine**: LangGraph for managing conversation flows and tool execution
- **Persistence**: MongoDB for storing conversation checkpoints and state
- **Tool System**: Custom tools for executing system commands

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- Docker and Docker Compose
- OpenAI API key
- Microphone access

### Installation

1. **Clone the repository**

   ```bash
   git clone <your-repo-url>
   cd voice-cursor
   ```

2. **Set up environment variables**

   ```bash
   cp .env.example .env
   ```

   Edit `.env` and add your OpenAI API key:

   ```
   OPENAI_API_KEY=your_openai_api_key_here
   ```

3. **Start MongoDB using Docker**

   ```bash
   docker-compose up -d
   ```

4. **Install Python dependencies**

   ```bash
   pip install -r requirements.txt
   ```

5. **Run the application**

   ```bash
   python -m app.main
   ```

## 🎯 Usage

1. **Start the application** - The system will initialize and wait for voice input
2. **Speak your request** - Clearly state what you want to do (e.g., "Create a new Python file", "List all files in the current directory")
3. **Listen for response** - The AI will process your request and execute the appropriate actions
4. **Follow up** - Continue the conversation naturally with follow-up questions or requests

### Example Interactions

- "Create a new Python file called hello.py"
- "What files are in the current directory?"
- "Help me debug this error"
- "Write a function to calculate fibonacci numbers"

## 🛠️ Technical Details

### Project Structure

```
voice-cursor/
├── app/
│   ├── main.py          # Main application entry point
│   └── graph.py         # LangGraph workflow definition
├── docker-compose.yml   # MongoDB service configuration
├── requirements.txt     # Python dependencies
└── README.md           # This file
```

### Key Components

- **`main.py`**: Handles speech recognition, audio processing, and orchestrates the conversation flow
- **`graph.py`**: Defines the LangGraph workflow with chatbot and tool execution nodes
- **Docker Compose**: Manages MongoDB instance for conversation persistence

### Dependencies

- **Core AI**: `openai`, `langchain`, `langgraph`
- **Speech**: `SpeechRecognition`, `PyAudio`
- **Database**: `pymongo`, `motor`
- **Utilities**: `python-dotenv`, `pydantic`

## 🔧 Configuration

### Environment Variables

- `OPENAI_API_KEY`: Your OpenAI API key (required)
- `MONGODB_URI`: MongoDB connection string (defaults to localhost)

### Customization

You can modify the system prompt in `app/graph.py` to customize the AI assistant's behavior and capabilities.

## 🐳 Docker Deployment

For production deployment, you can use Docker:

```bash
# Build and run with Docker Compose
docker-compose up --build
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- OpenAI for providing the GPT-4 API
- LangChain and LangGraph teams for the workflow framework
- Google Speech Recognition for voice processing capabilities

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/yourusername/voice-cursor/issues) page
2. Create a new issue with detailed information about your problem
3. Include your operating system, Python version, and any error messages

---

**Built with ❤️ using cutting-edge AI technologies**
