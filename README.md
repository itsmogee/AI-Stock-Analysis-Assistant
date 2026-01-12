# AI Stock Analysis Assistant

An AI-powered tool for intelligent stock market analysis using real-time data and conversational AI insights.

## Features

- Real-time stock price retrieval
- Historical price data analysis with date ranges
- Company balance sheet information
- Stock news aggregation
- AI-powered conversational analysis with streaming responses
- CORS-enabled API for seamless frontend integration

## Tech Stack

- **Backend**: FastAPI, Python 3.14+, LangChain, OpenAI API integration, yfinance, uvicorn
- **Frontend**: React 19, TypeScript, Vite, @crayonai/react-ui, @thesysai/genui-sdk

## Installation

1. **Prerequisites**: Python 3.14+, Node.js, npm/yarn

2. **Backend Setup**:
   - Navigate to `backend/` directory
   - Install dependencies: `uv sync` (or `pip install -r requirements.txt` if uv not available)
   - Create `.env` file with required API keys (e.g., OPENAI_API_KEY)

3. **Frontend Setup**:
   - Navigate to `frontend/` directory
   - Install dependencies: `npm install`
   - Start development server: `npm run dev`

## Usage

- Start backend: `python main.py` (runs on port 8888)
- Start frontend: `npm run dev` (runs on port 5173)
- Access the application at `http://localhost:5173`
- Enter stock tickers for analysis, receive AI-powered insights

## API Reference

- **Endpoint**: `POST /api/chat`

- **Request Body**:
  ```json
  {
    "prompt": {
      "content": "Analyze AAPL stock",
      "id": "unique-id",
      "role": "user"
    },
    "threadId": "conversation-thread",
    "responseId": "response-id"
  }
  ```

- **Response**: Server-sent events stream with AI analysis

## AI Model Capabilities & Limitations

- **Capabilities**: Provides intelligent stock analysis by combining real-time market data (prices, historical trends, balance sheets, news) with conversational AI reasoning. Supports natural language queries about stocks and can perform comparative analysis.

- **Limitations**: Analysis is based on available yfinance data and news sources, which may have delays or incomplete information. AI responses are generated conversationally but should not be considered financial advice. API rate limits and data availability can affect response quality.

## Project Structure

```
├── backend/          # FastAPI server with AI agent
├── frontend/         # React/TypeScript client
├── .gitignore        # Git ignore rules
├── .python-version   # Python version specification
└── README.md         # This file
```