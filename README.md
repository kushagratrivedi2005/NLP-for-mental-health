# NLP-for-mental-health
# Mental Health Analysis Web Application

A Flask-based web application that performs comprehensive analysis of mental health-related text inputs using various NLP models and machine learning techniques. The application provides sentiment analysis, keyword extraction, concern classification, and intensity scoring for mental health-related text.

## Features

- **Emotion Classification**: Analyzes the emotional content of text using RoBERTa-based sentiment analysis
- **Keyword Extraction**: Identifies key phrases and topics using KeyBERT
- **Concern Classification**: Categorizes mental health concerns using TF-IDF and Logistic Regression
- **Category Classification**: Zero-shot classification using BART for specific mental health categories
- **Intensity Scoring**: Predicts the intensity of mental health concerns
- **Visualization**: Tracks and visualizes sentiment analysis trends over time

## Prerequisites

- Python 3.7+
- Flask
- PyTorch
- Transformers
- scikit-learn
- pandas
- KeyBERT
- matplotlib

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/mental-health-analyzer.git
cd mental-health-analyzer
```

2. Install the required packages:
```bash
pip install -r requirements.txt
```

3. Download the required model files:
- cardiffnlp/twitter-roberta-base-sentiment
- microsoft/BiomedNLP-PubMedBERT-base-uncased-abstract-fulltext
- facebook/bart-large-mnli

## Usage

1. Start the Flask application:
```bash
python app.py
```

2. Navigate to `http://localhost:5000` in your web browser
3. Enter text in the provided form to analyze mental health-related content
4. View the analysis results including:
   - Emotional polarity
   - Extracted keywords
   - Concern classification
   - Category prediction
   - Intensity score

## Data Storage

The application stores analysis results in a `data.txt` file with the following format:
```
User Input, Polarity, Extracted Concern, Category, Category Confidence, Intensity
```

## Supported Categories

The application can classify text into the following mental health categories:
- Health Anxiety
- Eating Disorder
- Anxiety
- Depression
- Insomnia
- Stress
- Positive Outlook
- Career Confusion

## Technical Details

### Models Used
- **Sentiment Analysis**: cardiffnlp/twitter-roberta-base-sentiment
- **Medical Classification**: microsoft/BiomedNLP-PubMedBERT
- **Zero-shot Classification**: facebook/bart-large-mnli
- **Keyword Extraction**: KeyBERT
- **Custom trained models**: TF-IDF vectorizer with Logistic Regression for concern classification

### GPU Support
The application automatically utilizes GPU acceleration when available, falling back to CPU processing when GPU is not present.

## Visualization

The application includes a timeline visualization showing:
- Polarity trends
- Intensity scores
- Category confidence levels

Access the visualization at `/plot.png` after submitting entries.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License

Copyright (c) [2024] [Kushagra Trivedi]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


## Acknowledgments

- Hugging Face for providing pre-trained models
- KeyBERT for keyword extraction capabilities
- Flask community for the web framework

## Note

This application is intended for research and demonstration purposes only. It should not be used as a substitute for professional mental health advice or diagnosis.
