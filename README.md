# Video Agent

A powerful AI agent system for video processing and analysis, built with multimodal capabilities.

## Demo

[Video Agent Demo] = https://youtu.be/Tf463Nc4D-I


<p align="center">
  <img src="https://github.com/danial-shehroz-khan/video-agent/blob/master/whole%20system%20diagram-32e86eeb-d01a-43b5-ad5f-c6cbbeb103f3.png" width="800" />
</p>

Second component - API, Stateful agents and MCP Clients


<p align="center">
  <img src="https://github.com/danial-shehroz-khan/video-agent/blob/master/Second%20component%20-%20API%2C%20Stateful%20agents%20and%20MCP%20Clients.png" width="800" />
</p>

## Features

- **Video Processing**: Advanced video analysis and processing capabilities
- **Multimodal AI**: Handles text, images, audio, and video inputs
- **MCP Integration**: Model Context Protocol for seamless AI tool integration
- **Modern UI**: React-based user interface with real-time chat
- **API Backend**: FastAPI-powered backend with Groq integration

## Architecture

The system consists of three main components:

1. **MCP Server** (`kubrick-mcp`) - Handles video processing and AI tools
2. **API Server** (`kubrick-api`) - FastAPI backend with AI agents
3. **UI** (`kubrick-ui`) - React frontend interface

## Quick Start

### Prerequisites

- Docker and Docker Compose
- Python 3.12+ with uv package manager
- API keys for OpenAI, Groq, and Opik

### Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/video-agent.git
cd video-agent
```

2. Set up environment variables:
   - Create `.env` files in `kubrick-mcp/` and `kubrick-api/` directories
   - Add your API keys (OpenAI, Groq, Opik)

3. Start the system:
```bash
docker compose up --build -d
```

### Access Points

- **Main UI**: http://localhost:3000
- **API Documentation**: http://localhost:8080/docs
- **MCP Server**: http://localhost:9090

## Configuration

### Environment Variables

**For kubrick-mcp/.env:**
```env
OPENAI_API_KEY=your_openai_api_key_here
OPIK_API_KEY=your_opik_api_key_here
OPIK_WORKSPACE=default
OPIK_PROJECT=kubrick-mcp
```

**For kubrick-api/.env:**
```env
GROQ_API_KEY=your_groq_api_key_here
OPIK_API_KEY=your_opik_api_key_here
OPIK_WORKSPACE=default
OPIK_PROJECT=kubrick-api
```

## Usage

1. Open http://localhost:3000 in your browser
2. Upload a video or use the sample video
3. Ask questions about the video content
4. The AI agent will analyze and respond with insights

## Development

### Running Components Individually

**MCP Server:**
```bash
cd kubrick-mcp
make start-kubrick-mcp
```

**API Server:**
```bash
cd kubrick-api
make start-kubrick-api
```

**UI (Development):**
```bash
cd kubrick-ui
npm install
npm run dev
```

## License

This project is open source and available under the MIT License.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
