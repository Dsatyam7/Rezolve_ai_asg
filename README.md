# Rezolve_ai_asg

# FastAPI Text Processing API

**Overview**

This is a simple RESTful API built with FastAPI that processes text using Azure OpenAI's gpt-4o. The API provides functionalities such as:

Summarizing input text

Extracting keywords

Performing sentiment analysis

Retrieving the history of processed texts

Features

Uses Azure OpenAI's GPT model for text processing

RESTful endpoints for text processing and history retrieval

Input validation using Pydantic models

Modular structure for scalability

Installation

Prerequisites

Python 3.8+

Azure OpenAI API Key

**Setup**

1. Clone the repository
2. Setup a virtual env.
3. Install the dependencies from requirements.txt.
4. Setup your environment variables in .env.base file.(If you are using OpenAI instead of AzureOpenAI, you may have to change the function names and response structures a bit as well).
5. Run the application: uvicorn main:app --reload

# API Endpoints

**Process Text**

Endpoint: POST /process
Request Body:
{
  "text": "Your text here"
}

Response:
{
  "summary": "Summarized text...",
  "sentiment": "Positive/Negative/Neutral",
  "keywords": ["keyword1", "keyword2"]
}

**Get Processing History**

Endpoint: GET /history
Response:
{
  "history": [
    {
      "summary": "Summarized text...",
      "sentiment": "Positive",
      "keywords": ["keyword1", "keyword2"]
    }
  ]
}
