# Intelligent-News-Summarization-and-Analysis-system
The implementation integrates NewsAPI, OpenAI GPT API (via LangChain for simplified prompt management), FastAPI for API handling, and other essential libraries for processing, caching, and managing the pipeline

Description : 
This project is a Python-based system that fetches news articles, processes them using a Large Language Model (LLM), and provides intelligent insights. It leverages open-source libraries like FastAPI, LangChain, and BeautifulSoup for efficient data handling, API integration, and article analysis. It also integrates Docker for deployment and caching for optimized performance.

## Features

- **News Article Fetching**: Uses NewsAPI to fetch articles based on search queries.
- **Article Preprocessing**: Cleans and preprocesses article text to prepare it for analysis.
- **LLM Integration**: Summarizes articles, extracts key points, analyzes sentiment, and classifies topics using OpenAI's GPT API.
- **Analysis Module**: Tracks trending topics and generates topic clusters.
- **API Endpoints**: Provides FastAPI endpoints to access summarized data and insights.
- **Caching and Rate Limiting**: Implements caching for improved performance.
- **Docker Configuration**: Dockerized application for easy deployment.
- **Unit Tests**: Basic unit tests included for article processing.

## Setup Instructions

### 1. Prerequisites

- Python 3.9+
- Docker (for containerized deployment)
- NewsAPI API Key (for fetching news)
- OpenAI API Key (for LLM integration via LangChain)

### 2. Clone the Repository

```bash
git clone https://github.com/yourusername/news-summarization-analysis.git
cd news-summarization-analysis


3. Install Dependencies
Using requirements.txt
pip install -r requirements.txt


4. Environment Variables
Set up your API keys in the environment. You can set them directly in your shell:
export NEWS_API_KEY='your_newsapi_key'
export OPENAI_API_KEY='your_openai_key'


5. Run the API Locally
To start the FastAPI server locally:
uvicorn main:app --reload --host 0.0.0.0 --port 8000


6. Run Unit Tests
pytest test_script.py


7. Docker Setup
To build and run the Docker container:

Build the Docker image:
docker build -t news_summarization .

Run the Docker container:
docker run -p 8000:8000 news_summarization

The API will be available at http://localhost:8000



