# Speech TTS and Grammar Correction - Installation Guide

## Features Added
- **Text-to-Speech**: After you stop the microphone, the detected speech is read back using Edge TTS with a natural voice
- **Grammar Correction**: Automatic grammar correction using a simple rule-based system (no Java required!)
- **Corrected Speech Playback**: If corrections are made, the corrected sentence is also read aloud

## Installation Steps

1. **Install Required Packages**
   ```bash
   cd "d:\Projects 2025\SpeechWebsite\SpeechAnalysis"
   pip install edge-tts
   ```

2. **Run the Django Server**
   ```bash
   python manage.py runserver
   ```

3. **Test the Feature**
   - Navigate to the speech page
   - Click the microphone button to start recording
   - Speak something (try with or without grammar mistakes)
   - Click the microphone again to stop
   - The system will:
     1. Play back what you said
     2. Check for grammar mistakes
     3. If mistakes found, play the corrected version

## Libraries Used

### edge-tts
- **Free**: No API key required
- **Natural Voices**: Uses Microsoft Edge's text-to-speech engine
- **Offline-capable**: After initial download, works without internet
- **No Java Required**: Pure Python implementation

### Simple Grammar Correction
- **Built-in**: No external dependencies or Java required
- **Fast**: Instant corrections using regex patterns
- **Free**: Completely free, no API keys
- **Fixes Common Issues**:
  - Capitalization
  - Subject-verb agreement (I is → I am, they is → they are)
  - Common contractions (dont → don't, Im → I'm)
  - Article corrections (a apple → an apple)
  - Missing punctuation

## Voice Configuration

The current voice is set to `en-US-AriaNeural` (natural female voice).

You can change it in [views.py](App/views.py) by modifying:
```python
voice = "en-US-AriaNeural"
```

Other natural voices:
- `en-US-GuyNeural` - Male voice
- `en-US-JennyNeural` - Female voice
- `en-GB-SoniaNeural` - British female
- `en-GB-RyanNeural` - British male

## How It Works

1. When you stop recording, the last detected speech is sent to `/api/process-speech-tts/`
2. The backend:
   - Applies grammar corrections using regex patterns
   - Generates audio for the original text
   - If corrections exist, generates audio for corrected text
3. The frontend:
   - Plays the original audio
   - If corrections exist, shows "Grammar corrected version:" and plays corrected audio
   - Adds the corrected text to the transcript with a ✓ mark

## Troubleshooting

If you get import errors:
```bash
pip install --upgrade edge-tts
```

If TTS doesn't work:
- Check your internet connection (needed for first-time voice download)
- Check browser console for errors
- Ensure microphone permissions are granted

## Example Corrections

The system can fix:
- "I is going" → "I am going."
- "they is here" → "they are here."
- "dont know" → "don't know."
- "im ready" → "I'm ready."
- "a apple" → "an apple."
- Missing punctuation at end of sentences

