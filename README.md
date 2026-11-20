# Real-Time Stuttered Speech-to-Text Conversion Using Machine Learning and MLP

## Project Overview

This project focuses on developing a real-time speech-to-text conversion system designed to assist individuals with stuttered speech. It uses machine learning and natural language processing techniques to identify speech disfluencies and generate more readable text.

The application provides a web-based interface developed using Django.

## Key Features

- Speech input through microphone or audio upload.
- Speech preprocessing and feature extraction.
- Machine learning-based speech analysis.
- Detection of speech disfluencies such as repetitions, prolongations and blocks.
- Speech-to-text conversion.
- Text correction and refinement.
- Text-to-speech functionality.
- Web-based user interface.

## Technologies Used

- **Programming Language:** Python
- **Web Framework:** Django
- **Machine Learning:** TensorFlow, MLP
- **Speech Recognition:** Wav2Vec2
- **Natural Language Processing:** BERT, NLTK
- **Audio Processing:** MFCC, Spectrogram
- **Text-to-Speech:** Edge TTS
- **Generative AI:** Google Gemini API
- **Frontend:** HTML, CSS, JavaScript
- **Database:** SQLite

## Project Structure

```text
SpeechAnalysis/
│
├── App/
│   ├── views.py
│   ├── models.py
│   ├── consumers.py
│   ├── admin.py
│   └── routing.py
│
├── SpeechAnalysis/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── manage.py
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/sayandhana1234-gif/Real-Time-Stuttered-Speech-to-Text.git
```

### 2. Navigate to the project folder

```bash
cd SpeechAnalysis
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root and configure:

```env
DJANGO_SECRET_KEY=your_django_secret_key
GEMINI_API_KEY=your_gemini_api_key
```

Use your own private API keys. Never upload the `.env` file to GitHub.

### 5. Run database migrations

```bash
python manage.py migrate
```

### 6. Start the development server

```bash
python manage.py runserver
```

Open the application at:

http://127.0.0.1:8000/

## Project Objective

The objective is to explore how machine learning and speech-processing technologies can support people with speech disfluencies by improving the readability and usability of speech-generated text.

## Author

Sayandhana KS

B.Tech Computer Science and Engineering (Artificial Intelligence)