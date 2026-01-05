# Stock Impact AI Analyst

This project provides a simple web application that uses Google's Gemini AI to analyze news articles and extract their potential impact on publicly traded stocks. Users can paste news content, and the AI generates a structured, easy-to-understand report covering key financial and market-related insights.

## Features

*   **AI-Powered News Analysis:** Leverages Google's Gemini-2.5-flash model for intelligent text analysis.
*   **Stock-Focused Insights:** Specifically designed to identify and explain impacts relevant to stock performance, company valuation, and investor sentiment.
*   **Structured JSON Output:** The AI's response is formatted into a clean JSON object, making it easy for the frontend to parse and display.
*   **Key Data Points:** Extracts information on:
    *   Company mentioned & Ticker Symbol
    *   Market Summary
    *   Investor Sentiment & Stock Impact Magnitude
    *   Affected Financial/Operational Metrics (e.g., Revenue, Profit Margins)
    *   Short-term Stock Reaction
    *   Long-term Stock Outlook
    *   Risk Factors Highlighted
    *   Peer Impact
    *   Relevant Jargon Explanations
*   **User-Friendly Interface:** A clean, responsive HTML frontend to input news and display the analysis.
*   **Error Handling:** Robust error handling for missing API keys, invalid news input, and issues with the AI API.

## How it Works

The application consists of two main parts:

1.  **`app.py` (Flask Backend):**
    *   A Flask web server that exposes a `/analyze` endpoint.
    *   Receives news text via a POST request from the frontend.
    *   Constructs a highly specific prompt for the Gemini AI, requesting a JSON output focused on stock impact.
    *   Sends the prompt to the Gemini API using the `requests` library.
    *   Parses the AI's response, stripping any markdown formatting (like ` ```json `) to ensure valid JSON.
    *   Returns the structured JSON analysis to the frontend.
    *   Requires a `GEMINI_API_KEY` loaded from a `.env` file.

2.  **`index.html` (Frontend):**
    *   An HTML page with a textarea for news input and a button to trigger analysis.
    *   Uses JavaScript to send the news text to the Flask backend.
    *   Displays a loading indicator while the AI processes the request.
    *   Parses the JSON response from the backend.
    *   Dynamically renders the analysis results into a clean, categorized dashboard format.

## Setup and Installation

### Prerequisites

*   Python 3.7+
*   A Google Cloud Project with the Gemini API enabled.
*   A Gemini API Key.

### Steps

1.  **Clone the Repository (or create files manually):**
    ```bash
    # If you have a git repo
    git clone <your-repo-url>
    cd stock-impact-ai-analyst
    ```
    If creating manually, ensure `app.py` is in the root and `index.html` is inside a `templates` directory:
    ```
    .
    ├── app.py
    └── templates/
        └── index.html
    ```

2.  **Install Python Dependencies:**
    ```bash
    pip install Flask Flask-Cors python-dotenv requests
    ```

3.  **Create a `.env` file:**
    In the same directory as `app.py`, create a file named `.env` and add your Gemini API Key:
    ```
    GEMINI_API_KEY=YOUR_GEMINI_API_KEY_HERE
    ```
    Replace `YOUR_GEMINI_API_KEY_HERE` with your actual key obtained from Google AI Studio or Google Cloud.

4.  **Run the Flask Backend:**
    ```bash
    python app.py
    ```
    You should see output similar to: `Server starting at http://localhost:8080`

5.  **Access the Frontend:**
    Open your web browser and navigate to `http://localhost:8080`.

## Usage

1.  **Paste News:** In the web interface, paste a news article or snippet into the provided text area.
2.  **Analyze:** Click the "Analyze Financial Data" button.
3.  **View Report:** The AI will process the news, and a structured report detailing its stock market impact will appear on the page.

## Technologies Used

*   **Backend:** Python, Flask
*   **Frontend:** HTML, CSS, JavaScript
*   **AI:** Google Gemini-2.5-flash API
*   **Dependency Management:** `python-dotenv` (for environment variables), `requests` (for HTTP requests)

---