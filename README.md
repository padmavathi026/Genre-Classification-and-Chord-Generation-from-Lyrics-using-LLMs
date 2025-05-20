
<h1>🎶 Genre Classification and Chord Generation from Lyrics using LLMs</h1>

<h2>Description</h2>
This project explores how Large Language Models (LLMs) can be used to generate chord progressions from song lyrics, and classify genre and emotion—bridging Natural Language Processing (NLP) and music composition.

<h3>🧠 Project Overview</h3>
Using a combination of pre-trained and fine-tuned models, the project performs:

- 🎼 Genre Classification (BERT)

- 🎭 Emotion Detection (VADER Sentiment)

- 🎹 Chord Generation (GPT-2 fine-tuned)

- 📈 Evaluation using Falcon-7B (LLM) and human ratings

- 🔉 Audio Output rendered from predicted chords

<h4>📁 Dataset Summary</h4>

| Dataset            | Description                                                             |
| ------------------ | ----------------------------------------------------------------------- |
| Lyrics Dataset     | 273 cleaned song lyrics used for genre and emotion prediction           |
| Musixmatch         | Lyrics with emotional tags and metadata for validation                  |
| Million Songs      | Metadata like title, tempo, year—used for mapping and trend analysis    |
| Chordonomicon      | Real-world chord sequences used to fine-tune GPT-2 for chord generation |


<h5>🔧 Tools & Libraries </h5>

- 🤖 Transformers (HuggingFace) – BERT, GPT-2

- 🎯 VADER – Sentiment scoring

- 🎵 pretty_midi – MIDI to .wav rendering

- 📊 Seaborn, Matplotlib – Visualizations

- 📡 Falcon-7B – For LLM-based evaluation

- 🧠 Scikit-learn – Model utilities

<h6> ⚙️ Methodology </h6>

- 1. Genre Classification
Preprocessed lyrics → Tokenized → BERT fine-tuned for Pop, Rock, Hip-hop labels

Important for stylistic guidance in chord generation.

- 2. Emotion Detection
Used VADER to assign polarity: Positive, Neutral, Negative

Emotion impacted chord selection (e.g., minor for sad lyrics)

- 3. Chord Generation
GPT-2 fine-tuned on Chordonomicon sequences

Prompted with lyric + genre + emotion

Post-processed to clean formatting and validate chords

<h7> 📊 Evaluation </h7>

- <b>LLM-Based Evaluation (Falcon-7B)</b>
Prompted with lyrics + chords

Rated on a scale of 1–10 (Avg. Score: 8/10)

Explained alignment with emotion and flow

- <b>Human Evaluation</b>
5 volunteers rated the audio (generated from chords) on a scale of 1–5

Average Score: 4.4/5

Confirmed positive reception and alignment with lyrical theme

<h8> 🔉 Output Sample </h8>

- Lyric Input:
"When the night falls and the stars light the sky."

- Generated Chords:
Bb F C Bb F C Bb F C Bb F C B

- Audio Output:
Saved as output_music.wav (available in this repo)

<h8>Results Summary</h8>

| Component            | Model Used        | Key Results                  |
| -------------------- | ----------------- | ---------------------------- |
| Genre Classification | BERT              | Accurate genre labeling      |
| Emotion Detection    | VADER             | Clear Positive/Negative tags |
| Chord Generation     | GPT-2 (tuned)     | Realistic and mood-matching  |
| Evaluation           | Falcon-7B + Human | Avg. Score: 8/10 & 4.4/5     |
