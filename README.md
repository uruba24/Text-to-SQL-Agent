# Text-to-SQL Agent

## Overview
The **Text-to-SQL Agent** is an AI-powered application that translates natural language queries into SQL statements, allowing users to interact with a MySQL database without writing SQL manually. The agent is built using LangChain, OpenAI’s GPT-3.5 Turbo, and Python.

## Features
- **Natural Language Query Processing** – Convert text queries into SQL.
- **Real-time SQL Execution** – Execute generated queries on a MySQL database.
- **Error Handling & Query Validation** – Prevent invalid SQL execution.
- **Interactive Web UI** – Deployed with Streamlit for user-friendly interaction.
- **Multi-Table Query Support** – Handles joins and aggregations.

## Installation
### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- MySQL Database
- pip package manager

### Step 1: Clone the Repository
```bash
 git clone https://github.com/your-username/text-to-sql-agent.git
 cd text-to-sql-agent
```

### Step 2: Set Up a Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Configure Database Connection
Edit `config.py` with your MySQL credentials:
```python
db_user = "your_username"
db_password = "your_password"
db_host = "your_host"
db_name = "your_database"
```

### Step 5: Set OpenAI API Key
Export your OpenAI API key:
```bash
export OPENAI_API_KEY='your-api-key'
```
On Windows (PowerShell):
```powershell
$env:OPENAI_API_KEY="your-api-key"
```

### Step 6: Run the Application
```bash
python app.py
```
For Streamlit UI:
```bash
streamlit run app.py
```

## Usage
- **Ask Questions** – Type natural language queries (e.g., *“Find the top 5 products with the highest sales”*).
- **View Results** – The app converts text to SQL and displays results.
- **History & Logs** – Track executed queries and responses.

## API Endpoints
| Method | Endpoint | Description |
|--------|------------|-------------|
| POST | `/query` | Process natural language input and return SQL result |
| GET | `/history` | Retrieve previous queries and results |

## Troubleshooting
- **Database Connection Error?** Ensure MySQL is running and credentials are correct.
- **Incorrect SQL Output?** Improve query accuracy by fine-tuning prompts.
- **OpenAI API Issues?** Check API key validity and usage limits.

## Future Enhancements
- Support for PostgreSQL, SQLite.
- Advanced AI fine-tuning for better SQL accuracy.
- Data visualization for query results.

## Contributing
Feel free to fork the repo, create a new branch, and submit a pull request!

## License
This project is licensed under the MIT License.

