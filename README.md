# Chart Whisperer

**Chart Whisperer** is an AI-powered application that analyzes chart images, extracts data, and lets you ask questions about your charts using natural language.
![image](https://github.com/user-attachments/assets/8737066b-2b8a-4f31-89b2-ecf4c07383af)

## Features

- 📊 Chart Image Analysis: Upload images of charts and graphs to extract underlying data  
- 🔍 Data Extraction: Automatically identify titles, headers, and data points from images  
- 💬 Natural Language Querying: Ask questions about your charts in plain English  
- 🤖 Local LLM Integration: Connect to your local Ollama instance for privacy-focused AI processing  
- 📈 Chart Visualization: Preview extracted data in clean, formatted tables  
- 📥 CSV Export: Download extracted chart data as CSV files  
- 🎤 Voice Commands: Use speech recognition for hands-free interaction  

## Tech Stack

### Frontend

- React with TypeScript  
- Vite for fast builds and development  
- Tailwind CSS for styling  
- shadcn/ui for UI components  
- Framer Motion for animations  
- Sonner for toast notifications  

### Backend

- Flask for the API server  
- Ollama for local LLM integration  
- Pix2Struct for chart image analysis  

## Installation

### Prerequisites

- Node.js and npm  
- Python 3.8 or higher  
- Ollama installed locally (for LLM features)  

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
Backend Setup
bash
Copy
Edit
cd backend
pip install -r requirements.txt
python app.py
```
Backend will run at http://localhost:5000

Usage
1. Upload a chart image

2. View extracted table data

3. Ask questions about the data

Export to CSV

API Endpoints:-
GET /status – Check if the backend is running

GET /models – List available Ollama models

POST /extract – Extract data from a chart image

POST /question – Ask a question about the extracted data

Sample API Usage
bash
Copy
Edit
# Extract data
```
curl -X POST http://localhost:5000/extract -F "image=@chart.png"
```
# Ask a question
```
curl -X POST http://localhost:5000/question -H "Content-Type: application/json" \
-d '{"question": "What is the highest value?", "data": {...}}'
```
Demo Mode
No backend? Try demo mode using sample data.

System Requirements
Modern web browser (Chrome, Firefox, Safari, Edge)

8GB RAM recommended for Ollama models

GPU improves image analysis performance

Contributing
Contributions are welcome!

bash
Copy
Edit
# Fork the repository
```
git clone https://github.com/AP4549/chart-whisperer.git
```

# Create a feature branch
git checkout -b feature/amazing-feature

# Commit your changes
```
git commit -m "Add some amazing feature"
```
# Push and open a PR
```
git push origin feature/amazing-feature
```
License
This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgments
Powered by Ollama

Uses Pix2Struct
