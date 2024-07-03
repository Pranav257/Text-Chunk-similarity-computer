 
# Text Analysis for Education

This Python script is designed to assist educators and researchers in analyzing textual responses from students compared to a teacher's model answers. It leverages Natural Language Processing (NLP) to extract key phrases from both student and teacher responses and provides various metrics to assess the similarity between them.

## Features

- **Key Phrase Extraction**: Utilizes spaCy to identify and extract key phrases from both questions and answers.
- **Phrase Comparison**: Removes common phrases found in the question from the responses to focus on unique content.
- **Similarity Metrics**:
  - **Jaccard Similarity**: Calculates the Jaccard index to quantify the overlap between the sets of key phrases from teacher and student answers.
  - **Semantic Similarity**: Uses sentence transformers to calculate semantic similarity scores between the teacher's and student's key phrases.
  
## Requirements

Before running this script, ensure you have the following installed:
- Python 3.x
- pandas
- spaCy
- sentence-transformers

You can install the necessary libraries with the following commands:

```bash
pip install pandas spacy sentence-transformers
python -m spacy download en_core_web_sm
```

## Usage

1. **Data Preparation**: Ensure your Excel file is formatted correctly with columns for 'Question', 'Teacher Answer', and 'Student Answer'.
2. **Configuration**: Modify the `file_path` variable to point to your specific Excel file location.
3. **Running the Script**: Execute the script in your environment. The script will output the results in JSON format, displaying the extracted key phrases and similarity scores.

## Example Output

```json
[
    {
        "Question": "What is the capital of France?",
        "Teacher_Keyphrases_Excluding_Question": ["Paris"],
        "Student_Keyphrases_Excluding_Question": ["Paris"],
        "Similarity_Score": 1.0
    }
]
```

This output provides a structured view of the analysis, making it easy to integrate with other tools or reports.

## Contributions

Contributions to this project are welcome. You can enhance the functionality, improve the UI, or suggest new features by opening an issue or a pull request on the project repository.

 
