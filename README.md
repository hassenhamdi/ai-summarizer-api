# AI-Powered Content Summarizer API

This project is a simple Flask-based RESTful API that summarizes text content using the Google Gemini API.

## Requirements

*   Python 3.6+
*   A Google Gemini API key

## Setup

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/hassenhamdi/ai-summarizer-api/
    cd ai-summarizer-api
    ```

2.  **Create a virtual environment:**

    ```bash
    python3 -m venv .venv
    ```

3.  **Activate the virtual environment:**

    ```bash
    source .venv/bin/activate
    ```

4.  **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

5.  **Create a `.env` file:**

    Create a file named `.env` in the project root directory and add your Gemini API key:

    ```
    GOOGLE_API_KEY=YOUR_GEMINI_API_KEY
    ```

    Replace `YOUR_GEMINI_API_KEY` with your actual Gemini API key.

## Running the API

1.  **Activate the virtual environment:**

    ```bash
    source .venv/bin/activate
    ```

2.  **Run the Flask application:**

    ```bash
    flask run
    ```

    The API will run on `http://127.0.0.1:5000/`.

## API Endpoint

### `POST /summarize`

Summarizes the provided text content using the Gemini API.

**Request Body:**

```json
{
    "text": "Your text content here to be summarized."
}
```

**Response Body (Success):**

```json
{
    "summary": "The summarized text."
}
```

**Response Body (Error):**

```json
{
    "error": "Error message."
}
```

## Example Usage (using curl)

```bash
curl -X POST -H "Content-Type: application/json" -d '{"text": "This is a test sentence that I want to be summarized."}' http://127.0.0.1:5000/summarize
```

## Project Structure

```
ai-summarizer-api/
├── .env
├── .gitignore
├── app.py
├── requirements.txt
└── README.md
```

This project demonstrates the following skills:

*   Designing and building a RESTful API with Flask.
*   Integrating a third-party LLM API (Gemini).
*   Working with JSON data.
*   Using environment variables for sensitive information.
*   Managing dependencies with `requirements.txt`.
*   Using Git for version control.
*   Providing documentation with README.md.

## Development Notes

This project was developed with the assistance of an AI agent, reflecting a "vibe coding" approach and the capabilities of agentic AI in software development, for testing purpose.
