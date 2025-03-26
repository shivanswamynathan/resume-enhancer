# AI Resume Enhancer

An intelligent application that enhances resumes using AI to match them with job descriptions, improve content, and generate professionally formatted PDFs.

## Features

- **Resume Analysis**: Extract key information from uploaded resumes
- **Job Description Matching**: Compare resumes against job descriptions to identify gaps
- **Content Enhancement**: AI-powered suggestions to improve resume content
- **PDF Generation**: Create professionally formatted PDF resumes

## Tech Stack

- **Backend**: Python, Flask
- **AI**: OpenAI API
- **PDF Generation**: Yaml
- **Containerization**: Docker

## Prerequisites

- Python 3.11+
- Docker (for containerized deployment)
- OpenAI API key
- Yaml (for PDF generation)

## Getting Started

### Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ai-resume-enhancer.git
   cd ai-resume-enhancer
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file with your environment variables:
   ```
   OPENAI_API_KEY=your_openai_api_key
   MODEL_NAME=openai
   DEBUG=True
   ```

5. Run the application:
   ```bash
   python app.py
   ```

### Docker Deployment

1. Build the Docker image:
   ```bash
   docker build -t resume-enhancer .
   ```

2. Run the container:
   ```bash
   docker run -p 5000:5000 -e OPENAI_API_KEY=your_key_here resume-enhancer
   ```

   Or with an environment file:
   ```bash
   docker run -p 5000:5000 --env-file .env resume-enhancer
   ```

## API Endpoints


```
POST /process-resume
```

## Configuration

The application can be configured using environment variables:

| Variable | Description | Default |
|----------|-------------|---------|
| `OPENAI_API_KEY` | OpenAI API key | - |
| `MODEL_NAME` | AI model to use | `openai` |

