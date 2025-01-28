# Agentic Data Analysis

An AI-powered data analysis agent built with LangGraph that can perform intelligent analysis on your datasets. This project demonstrates advanced LangGraph techniques and provides an interactive Streamlit dashboard for data exploration.



## Features

- 📊 Interactive Streamlit dashboard
- 🤖 AI-powered data analysis using GPT-4
- 📈 Automated visualization generation
- 💬 Natural language query interface
- 📁 Support for multiple CSV datasets
- 🔍 Detailed data exploration capabilities

## Prerequisites

- Windows 10 or higher
- Python 3.8 or higher
- OpenAI API key
- Git for Windows (for cloning the repository)

## Installation

1. Clone the repository:
   - Open Command Prompt or PowerShell
   - Navigate to your desired directory
```powershell
git clone https://github.com/CinderZhang/AgenticDataAnalysis.git
cd AgenticDataAnalysis
```

2. Create and activate a virtual environment (recommended):
```powershell
python -m venv venv
.\venv\Scripts\activate
```

3. Install required packages:
```powershell
pip install -r requirements.txt
```

## Configuration

### Setting up API Keys (Important!)

1. Create a `.env` file:
   - Right-click in the project folder
   - Select "New" > "Text Document"
   - Name it `.env` (make sure to include the dot)
   - If Windows hides file extensions, you might need to name it `.env.`
   - Remove any `.txt` extension if present

2. Add your OpenAI API key to the `.env` file:
   - Open `.env` with a text editor (like Notepad)
   - Add this line:
```plaintext
OPENAI_API_KEY=your-api-key-here
```

⚠️ **Security Notes**:
- Never commit your `.env` file to version control
- Keep your API keys private and secure
- The `.env` file is already included in `.gitignore`
- Don't hardcode API keys in your Python files

## Usage

1. Start the Streamlit dashboard:
```powershell
streamlit run data_analysis_streamlit_app.py --server.maxUploadSize 2000
```

2. Upload your dataset(s):
   - You can use the sample dataset from [Kaggle](https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets/data)
   - Or upload your own CSV files
   - Multiple files can be uploaded and analyzed together

3. Interact with your data:
   - Use natural language to ask questions about your data
   - Generate visualizations automatically
   - Explore relationships between different datasets

## Sample Dataset

For testing, you can use the transactions fraud dataset from Kaggle:
[Transactions Fraud Dataset](https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets/data)

## Project Structure

```
AgenticDataAnalysis/
├── data_analysis_streamlit_app.py  # Main Streamlit application
├── Pages/                          # Application pages and components
│   ├── backend.py                  # Backend logic
│   ├── graph/                      # LangGraph components
│   └── prompts/                    # System prompts
├── uploads/                        # Uploaded datasets (gitignored)
├── images/                         # Generated visualizations
├── requirements.txt                # Python dependencies
└── .env                           # Environment variables (gitignored)
```

## Troubleshooting

Common issues and solutions:

1. **API Key Issues**:
   - Make sure `.env` file doesn't have a `.txt` extension
   - Verify the API key is on a single line without quotes
   - Check that `python-dotenv` is installed
   - Verify the API key is valid and has sufficient credits

2. **File Upload Issues**:
   - Maximum file size is set to 2000MB
   - Only CSV files are supported
   - Check file permissions in the uploads directory

3. **Windows-Specific Issues**:
   - If you get "command not found", make sure Python is in your PATH
   - If virtual environment doesn't activate, run `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser` in PowerShell
   - For permission errors, try running Command Prompt as Administrator

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License.
