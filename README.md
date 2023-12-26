# Quote Analyzer Web App

## Project Overview

Quote Analyzer is a Python-based web application that fetches quotes from an Azure SQL Database, performs sentiment analysis and text summarization using Azure AI Services, and displays the analyzed results sequentially on the UI, allowing users to interact with and analyze different quotes.

## Objective

The objective of this project is to develop a web application that demonstrates the integration of Azure Services for natural language processing tasks. The application will:

- Utilize Azure SQL Database to store and manage quotes with a structured data model.
- Employ Azure AI Service - Language Service to perform sentiment analysis and text summarization on the quotes.
- Provide a simple and user-friendly interface to display the quotes and the analysis results.

## Functionality

### Key features of the web application:

- **Quote Display**: Fetches and displays one quote at a time from the Azure SQL Database on the user interface.
- **Sentiment Analysis**: Analyzes the sentiment of each displayed quote using Azure AI Service and displays the sentiment result (e.g., Positive, Negative, Neutral).
- **Text Summary**: Generates a text summary of the quote using Azure AI Service and displays it on the UI.
- **New Quote Button**: Allows users to view and analyze different quotes sequentially by fetching a new quote from the database upon clicking the "New" button.

## Technology Stack

### Backend:

- Python
- Flask framework

### Database:

- Azure SQL Database

### Frontend:

- HTML
- CSS
- JavaScript

### Azure Services:

- Azure AI Language Service

## How to Run

### Prerequisites:

- Python 3.8 or higher
- Flask 2.0.1 or higher
- Azure SQL Database with a quotes table (schema provided below)
- Azure AI Service - Language Service with valid subscription key and endpoint URL

### Environment Variables:

- `AZURE_SQL_CONNECTION_STRING`: Connection string for the Azure SQL Database
- `AZURE_TEXT_ANALYTICS_KEY`: Subscription key for the Azure AI Service - Language Service
- `AZURE_TEXT_ANALYTICS_ENDPOINT`: Endpoint URL for the Azure AI Service - Language Service

### Steps:

1. Clone the repository or download the source code.
2. Install dependencies: `pip install -r requirements.txt`
3. Run the app: `flask run`
4. Access the UI: [http://localhost:5000/](http://localhost:5000/)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Additional Information

### Azure SQL Database Table Schema:

| Column | Type          | Description           |
|--------|---------------|-----------------------|
| id     | int           | Unique identifier     |
| text   | nvarchar(max) | Text of the quote     |
| author | nvarchar(100) | Name of the quote author |

