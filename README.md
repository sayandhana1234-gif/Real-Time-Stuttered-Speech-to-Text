# Real-Time Stuttered Speech-to-Text Conversion Using Machine Learning and MLP

An AI-driven assistive speech system designed to convert stuttered speech into fluent, readable text using machine learning, speech recognition and natural language processing techniques.

## Project Overview

This project focuses on developing a real-time speech-to-text conversion system to assist individuals with stuttered speech. It uses machine learning and natural language processing techniques to identify speech disfluencies, process spoken input and generate more readable text while preserving the intended meaning.

The system, named **Emotion-Aware Assistive Speech Generator (EASG)**, integrates speech acquisition, disfluency detection, automatic speech recognition and NLP-based text correction into a unified workflow.

The application provides a web-based interface developed using Django and supports microphone input, audio uploads, speech transcription and corrected text generation.

## Key Features

- Speech input through a microphone or audio upload.
- Audio preprocessing and feature extraction.
- Machine learning-based speech disfluency analysis.
- Detection of repetitions, prolongations, blocks and interjections.
- Speech-to-text conversion.
- NLP-based text correction and refinement.
- Text-to-speech functionality.
- Web-based user interface.
- Interactive communication support.
- User-specific speech pattern personalization.

## Technologies Used

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Web Framework | Django |
| Machine Learning | TensorFlow, MLP |
| Contextual Modeling | BERT |
| Speech Recognition | Wav2Vec2 |
| Natural Language Processing | NLTK |
| Audio Processing | MFCC, Spectrogram |
| Text-to-Speech | Edge TTS, gTTS |
| Generative AI | Google Gemini API |
| Frontend | HTML, CSS, JavaScript |
| Database | SQLite |
| Computer Vision | OpenCV |
| Communication | REST APIs, Socket Programming |

## System Workflow

1. **Speech Input:** Users record speech through a microphone or upload an audio file.
2. **Audio Preprocessing:** The input audio undergoes preprocessing and feature extraction using techniques such as MFCC and spectrogram analysis.
3. **Disfluency Detection:** Machine learning models identify speech disfluencies, including repetitions, prolongations, blocks and interjections.
4. **Speech Recognition:** Wav2Vec2 processes the speech and generates an initial transcript.
5. **Text Correction:** NLP techniques are applied to refine the transcript, remove unnecessary repetitions and improve grammatical readability.
6. **Output Generation:** The corrected text is displayed through the web interface and can be converted into speech using text-to-speech functionality.

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

### 1. Clone the Repository

```bash
git clone https://github.com/sayandhana1234-gif/Real-Time-Stuttered-Speech-to-Text.git
```

### 2. Navigate to the Project Directory

```bash
cd Real-Time-Stuttered-Speech-to-Text
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the project root directory and configure the following variables:

```env
DJANGO_SECRET_KEY=your_django_secret_key
GEMINI_API_KEY=your_gemini_api_key
```

Use your own private API keys. Never upload the `.env` file to GitHub.

### 5. Run Database Migrations

```bash
python manage.py migrate
```

### 6. Start the Development Server

```bash
python manage.py runserver
```

Open the application in your browser:

http://127.0.0.1:8000/

## Project Objective

The primary objective is to explore how artificial intelligence, machine learning and speech-processing technologies can support individuals with speech disfluencies by improving the readability and usability of speech-generated text.

The system aims to provide an accessible assistive communication approach by integrating speech recognition, disfluency detection and text correction.

## Experimental Results

The research evaluates the proposed framework using speech disfluency detection and transcription-related performance metrics.

A relative Word Error Rate (WER) reduction of approximately **56%** was reported after applying the proposed fluency correction pipeline.

The research also includes F1-score comparisons and ROC curve analysis to evaluate disfluency detection performance.

*Note: These figures represent the results reported in the research paper.*

## Research Publication

**Research Title:** Real-Time Stuttered Speech-to-Text Conversion Using Machine Learning and MLP

**Project Name:** Emotion-Aware Assistive Speech Generator (EASG)

**Conference:** ICTEST-2026

**Presentation:** Government Model Engineering College, Kochi, Kerala, July 2026.

## Authors

This work was developed as a group academic project.

1. Dr. Sarika S
2. Ms. Aaliya M Ismail
3. Mr. Akshay S
4. Mr. Arjun S
5. Ms. Sayandhana KS

**Department:** Artificial Intelligence and Data Science

**Institution:** Adi Shankara Institute of Engineering and Technology, Kalady, Ernakulam, Kerala, India.

## My Contribution

My primary contribution to this group project focused on dataset processing and preparation for the speech disfluency analysis workflow.

- Worked on processing and preparing speech datasets for model development.
- Assisted in organizing and preparing audio data for further analysis.
- Contributed to preparing speech data used in identifying disfluencies such as repetitions, prolongations, blocks and interjections.
- Supported the project through dataset-related activities.

## Future Enhancements

- Support for additional languages.
- Offline functionality without requiring an internet connection.
  
## Acknowledgment

We express our sincere gratitude to the faculty of Adi Shankara Institute of Engineering and Technology for their guidance, encouragement and support throughout the project.

---

**Repository:** [Real-Time Stuttered Speech-to-Text Conversion Using Machine Learning and MLP](https://github.com/sayandhana1234-gif/Real-Time-Stuttered-Speech-to-Text)
