# Speech Recognition: From Voice to Text and Back


## 📌 Project Overview

This project explores the complete **Automatic Speech Recognition (ASR) and Text-to-Speech (TTS) pipeline** using audio containing speech disruptions associated with stuttering. It demonstrates how speech signals are processed, converted into meaningful features, transcribed into text, evaluated for recognition accuracy, and converted back into speech.

The implementation uses Python in Google Colab and pretrained speech recognition models to analyze real-world audio.

## 🎯 Objectives

- Analyze speech signals using waveform visualization.
- Extract and visualize Log-Mel spectral features.
- Understand the architecture of an ASR system.
- Explore Connectionist Temporal Classification (CTC) decoding.
- Generate speech transcripts using Wav2Vec2 and Whisper.
- Compare ASR outputs using Word Error Rate (WER).
- Convert recognized text back into speech using Text-to-Speech.
- Understand the challenges of recognizing speech containing disfluencies.

## 🔄 System Pipeline

**Speech → Feature Extraction → Log-Mel Spectrum → ASR → CTC → Text → TTS → Speech**

1. **Speech Input:** Load an audio recording containing speech and possible stuttering.
2. **Feature Extraction:** Process the audio into numerical representations useful for speech analysis.
3. **Log-Mel Spectrum:** Visualize how speech energy varies across time and frequency.
4. **Automatic Speech Recognition:** Generate text using pretrained speech recognition models.
5. **CTC Decoding:** Understand how a CTC-based model converts frame-level predictions into a text sequence.
6. **Text Output:** Obtain and examine the recognized transcripts.
7. **WER Evaluation:** Compare model predictions against a reference transcript.
8. **Text-to-Speech:** Generate speech from text using a TTS system.

## 🛠️ Technologies Used

- Python
- Google Colab and Jupyter Notebook
- PyTorch
- Hugging Face Transformers
- Wav2Vec2 (`facebook/wav2vec2-base-960h`)
- Whisper (`openai/whisper-base`)
- Librosa and Matplotlib
- JiWER for Word Error Rate evaluation
- gTTS for Text-to-Speech

## 🧠 ASR Models

### 1. Wav2Vec2

Wav2Vec2 is a pretrained speech recognition model that processes audio representations and predicts speech tokens. The CTC-based model converts these predictions into a text transcript.

### 2. Whisper

Whisper is a pretrained speech recognition model used to generate a second transcript from the same audio. Comparing its output with Wav2Vec2 helps illustrate differences in recognition behavior.

## 📊 Evaluation

The project examines recognition output using Word Error Rate (WER).

**Formula:**

WER = (S + D + I) / N

Where:
- **S:** Number of substitutions
- **D:** Number of deletions
- **I:** Number of insertions
- **N:** Number of words in the reference transcript

A lower WER indicates better agreement with the reference transcript. Reliable evaluation requires a reference transcript checked against the original audio. If an ASR-generated transcript is used as the reference, the result is provisional rather than ground-truth WER.

## 🔊 Text-to-Speech

The recognized text is passed to a TTS system to generate speech audio. This demonstrates the reverse direction of the pipeline, from written text back to synthesized speech.

## 📁 Repository Contents

- `Speech_Recognition_Unit_3.ipynb` — Google Colab notebook containing the implementation, visualizations, ASR inference, evaluation, and TTS workflow.
- `README.md` — Project overview and instructions.

## ▶️ How to Run

1. Open the notebook in Google Colab.
2. Run the setup and dependency installation cells.
3. Download and load the audio using the provided notebook code.
4. Execute the waveform and Log-Mel spectrogram analysis.
5. Run the Wav2Vec2 and Whisper transcription sections.
6. Review the ASR architecture and CTC explanation.
7. Provide a verified reference transcript for WER evaluation, where available.
8. Run the TTS section and listen to the generated audio.

**Note:** The first run may take time because pretrained models and audio files must be downloaded. CPU execution can be slower than GPU execution.

## 📚 Audio Source

The activity uses the podcast recording *Paying It Forward – Male Episode 1*, featuring Alan Badmington discussing his experiences with stuttering.

- [Podcast source page](https://stutterrockstar.com/2011/06/02/paying-it-forward-episode-1/)
- [Direct audio file](https://stutterrockstar.files.wordpress.com/2011/05/male-episode-1-with-alan1.mp3)

The notebook processes a selected portion of the recording for analysis. Speech disruptions in the selected segment should be verified by listening to the audio.

## 📌 Learning Outcomes

By completing this activity, the learner gains practical experience with audio preprocessing, spectral visualization, pretrained ASR models, CTC-based transcription, recognition evaluation, and speech synthesis.

## ⚠️ Limitations

Recognition performance may be affected by stuttering, pronunciation variations, pauses, background noise, and model limitations. The models are pretrained and are not specifically fine-tuned for stuttering. Recognition results should therefore be interpreted as an experimental comparison rather than a clinical assessment.

## 👨‍💻 Project Type

Academic coursework — Speech Recognition, Unit 3.
