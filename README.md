# Sat-question-bank-to-csv


# SAT Question Processor

This tool allows you to extract questions from an SAT PDF and process them using GPT-4. The questions are formatted into a structured JSON format, which can then be downloaded as a CSV file.

## Features

- **PDF Upload**: Upload an SAT PDF file to extract questions.
- **GPT-4 Processing**: Utilizes GPT-4 to analyze and structure the extracted content into JSON format.
- **CSV Export**: Processed questions can be downloaded as a CSV file.

## Requirements

Before using this app, you will need:

1. **API Key**: An OpenAI API key to access GPT-4 (you can get it from [OpenAI](https://platform.openai.com/signup)).
2. **Python Libraries**:
   - `streamlit` - For creating the interactive web interface.
   - `PyPDF2` - For extracting text from the uploaded PDF.
   - `requests` - To make API requests to GPT-4.
   - `pandas` - For managing and exporting the processed data.
   
   You can install the required libraries with the following command:

   ```bash
   pip install streamlit PyPDF2 requests pandas
   ```

## How to Run

### Step 1: Clone the Repository
Clone this repository to your local machine.

```bash
git clone https://github.com/yourusername/sat-question-processor.git
cd sat-question-processor
```

### Step 2: Set Up the Environment
Make sure you've installed the necessary Python libraries (as listed in the **Requirements** section).

### Step 3: Run the App
Run the app using Streamlit:

```bash
streamlit run app.py
```

This will launch the app in your web browser.

### Step 4: Enter API Key
Once the app is running, you'll need to enter your OpenAI API key to access GPT-4. You can obtain this key by signing up at [OpenAI's platform](https://platform.openai.com/signup).

### Step 5: Upload PDF
Upload your SAT PDF file. The tool will automatically process the document and extract the questions. It will then analyze the content using GPT-4 and present it in a structured format.

### Step 6: Download Processed Data
Once the processing is complete, you can download the questions in CSV format. This CSV will include:
- **Question ID**
- **Question Text**
- **Options (A, B, C, D, E)**
- **Correct Answer**
- **Rationale**
- **Test**
- **Domain**
- **Skill**
- **Difficulty**

## Example JSON Output

The extracted and processed questions are formatted in the following JSON structure:

```json
{
  "questions": [
    {
      "question_id": "6ed4qc",
      "question_text": "The human brain is primed to recognize faces—so much so that, due to a perceptual tendency called pareidolia, ______ will even find faces in clouds, wooden doors, pieces of fruit, and other faceless inanimate objects.",
      "options": [
        {"label": "A", "text": "she"},
        {"label": "B", "text": "they"},
        {"label": "C", "text": "it"},
        {"label": "D", "text": "those"}
      ],
      "correct_answer": "C",
      "rationale": "Choice C is the best answer. 'It' is a singular pronoun used to stand in for objects.",
      "test": "Reading and Writing",
      "domain": "Standard English Conventions",
      "skill": "Form, Structure and Tense",
      "difficulty": "Medium"
    }
  ]
}
```

## Troubleshooting

If you encounter any issues, consider the following:
- **Invalid API Key**: Ensure your OpenAI API key is correctly entered.
- **PDF Issues**: The tool processes text from PDFs, so make sure the document is not encrypted or contains images instead of text.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
