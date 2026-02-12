# AI-Generated Podcast Audio Files

This directory should contain 3 podcast audio files (~3 minutes each):

## Required Files

| Filename | Duration | Topic |
|----------|----------|-------|
| `vienna-circle-intro.mp3` | 3:12 | The Vienna Circle: A Scientific Worldview |
| `wittgenstein-ladder.mp3` | 3:08 | Wittgenstein's Ladder: The Limits of Language |
| `plato-to-frege.mp3` | 2:54 | From Plato to Frege: 2000 Years of Logic |

## Generation Options

### Option 1: NotebookLM (Recommended)
1. Go to [notebooklm.google.com](https://notebooklm.google.com)
2. Create a new notebook
3. Add source text about each topic (Wikipedia articles, Stanford Encyclopedia excerpts)
4. Click "Generate Audio Overview" to create a ~3 min podcast-style discussion
5. Download and rename the audio files

### Option 2: ElevenLabs
1. Write scripts for each episode (500-600 words each)
2. Use [elevenlabs.io](https://elevenlabs.io) to generate speech
3. Export as MP3

### Option 3: OpenAI Text-to-Speech
```python
from openai import OpenAI
client = OpenAI()

response = client.audio.speech.create(
    model="tts-1-hd",
    voice="onyx",
    input="Your script here..."
)
response.stream_to_file("vienna-circle-intro.mp3")
```

## Sample Scripts

### Episode 1: The Vienna Circle (3:12)
Discuss: Schlick's Thursday evening seminars, rejection of metaphysics, verification principle, connection to Russell and Wittgenstein, the manifesto "Wissenschaftliche Weltauffassung"

### Episode 2: Wittgenstein's Ladder (3:08)  
Discuss: The Tractatus structure (7 propositions), picture theory of meaning, logical atomism, "throwing away the ladder," the mystical and silence

### Episode 3: From Plato to Frege (2:54)
Discuss: Plato's Forms and dialectic, Aristotle's syllogistic, Leibniz's dream of a calculus, Frege's Begriffsschrift, the birth of modern logic
