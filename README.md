🧹 Text-Cleaning API
A lightweight and efficient FastAPI based tool designed for text preprocessing. This API helps you clean noisy text by removing unwanted symbols, handling extra whitespaces, and normalizing newlines—making it perfect for NLP tasks or general data cleaning.
✨ Features
Clean All Mode: Automatically removes symbols, normalizes spaces, removes newlines, and converts text to lowercase in one go.
Custom Mode: Fine-grained control to toggle specific cleaning operations based on your needs.
RapidAPI Compatible: Includes necessary CORS middleware and header support for seamless integration with RapidAPI.
Fast & Reliable: Built with FastAPI for high performance and easy scalability.
🚀 Getting Started
1. Clone the Repository
git clone https://github.com/Makhal-Architect/text-cleaning-APi.git
cd text-cleaning-APi
2. Install Dependencies
Make sure you have Python installed, then run:
pip install fastapi uvicorn

3. Run the Server
uvicorn main:app --reload
The API will be available at http://127.0.0.1:8000.
🛠 API Documentation
Endpoint: /process
Method: POST
Request Body Parameters:
Parameter Type Description
input_text String The raw text you want to clean.
clean_all Boolean If true, applies all cleaning rules automatically.
remove_space_newline Boolean Removes tabs, newlines, and extra spaces (Custom mode).
remove_symbols Boolean Removes all non-alphanumeric characters (Custom mode).
to_lowercase Boolean Converts

Example Request (JSON):
{
  "input_text": "Hello @World!!! \n This is   FastAPI.",
  "clean_all": false,
  "remove_space_newline": true,
  "remove_symbols": true,
  "to_lowercase": true
}
Example Response:
{
  "status": "complete",
  "mode": "custom",
  "result": "hello world this is fastapi"
}
📂 Project Structure
main.py - The core FastAPI application logic.
.gitignore - Pre-configured to keep your repo clean from Python junk files.
README.md - Documentation for the project.
