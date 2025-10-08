🎬 Review Sentiment Analysis
A web application that analyzes movie reviews and classifies them as positive or negative using a deep learning model trained on the IMDB dataset.


📊 Model Performance
Test Accuracy: about 86%

Test Loss: 0.36(imdb_model11_2_final.keras) and 0.5(imdb_model(5).keras)

Model Type: LSTM Neural Network

Training Data: IMDB Movie Reviews (25,000 training samples)

The model achieves solid performance in sentiment classification, correctly identifying review sentiment in approximately 86% of cases.



🚀 How to Use the App
1. Access the Application
The app opens with a text area where you can enter movie reviews

2. Submit a Review
Type or paste a movie review in the text area

Click the "Submit" button to analyze the sentiment

3. View Results
The app will display whether the review is Positive or Negative



4. Analyze Multiple Reviews
After seeing results, click "Want to try next" to analyze another review

The form will reappear for continuous usage


🛠️ Technical Details
Model Architecture

Sequential([
    Embedding(25000, 4, input_length=300),
    LSTM(32, return_sequences=True),
    LSTM(32),
    Dense(1, activation='sigmoid')
])

Features
Vocabulary: Top 25,000 most frequent words from IMDB dataset

Sequence Length: 300 words (padded/truncated)

Preprocessing: Automatic text cleaning and tokenization

Real-time Analysis: Instant sentiment classification



📁 Project Structure
review-sentiment-analysis/
├── app.py                 # Main Streamlit application
├── loading_modelandrunning.py  # Model loading and prediction script
├── imdb_model (5).keras   # Pre-trained model file
└── README.md             # This file

🔧 Installation & Setup

Prerequisites
Python 3.8+
Streamlit
TensorFlow/Keras
NumPy

Quick Start
Clone the repository
git clone <repository-url>
cd review-sentiment-analysis

Install dependencies
pip install streamlit tensorflow numpy

Run the application
streamlit run app.py

Open your browser
The app will automatically open at http://localhost:8501

💡 Example Usage
Positive Review Example:
"a movie about time, patience and loyalty."

Output: The review is positive

Negative Review Example:
"I was very disappointed with this movie. The plot was predictable and the characters were poorly developed."

Output: The review is negative

🎯 Use Cases
Movie Critics: Quickly analyze review sentiment

Production Studios: Monitor audience reception

Film Students: Learn about sentiment analysis applications

Researchers: Experiment with NLP classification

⚠️ Limitations
Trained specifically on movie reviews

May not perform as well on other types of text

Limited to English language

Binary classification (positive/negative only)

🔮 Future Enhancements
Confidence scores for predictions

Support for multiple languages

Fine-grained sentiment (very positive, neutral, etc.)

Batch processing of multiple reviews

Export results functionality

📊 Model Training Details
Dataset: IMDB Movie Reviews

Training Samples: 25,000

Validation Samples: 25,000

Vocabulary Size: 25,000 words

Epochs: 10

Batch Size: 32

🤝 Contributing
Contributions are welcome! Please feel free to submit pull requests or open issues for suggestions and improvements.

📄 License

This project is open source and available under the MIT License.




