# Hindi Speech Processing and ASR Evaluation

A comprehensive final-year Computer Science engineering assignment on Hindi Automatic Speech Recognition (ASR) systems and speech quality evaluation techniques.

## 📋 Project Overview

This project implements and evaluates state-of-the-art techniques for processing Hindi speech, including:
- Fine-tuning pre-trained ASR models (Whisper) on Hindi data
- Detecting and analyzing speech disfluencies
- Classifying Hindi word spelling accuracy
- Evaluating ASR performance using lattice-based consensus methods

## 🎯 Problem Statement

Hindi is a heavily-spoken language with unique linguistic and phonetic characteristics that challenge general-purpose ASR systems. This project addresses:

1. **Low-resource ASR**: How to effectively fine-tune models with limited Hindi speech data
2. **Speech Quality**: Detecting disfluencies to improve transcription quality
3. **Orthography**: Classifying correctly/incorrectly spelled words in Hindi script
4. **Evaluation Methods**: Using lattice structures for more accurate WER computation

## 📁 Project Structure

```
hindi-speech-processing-asr-evaluation/
├── question1_whisper_finetune.py      # Q1: Whisper model fine-tuning
├── question2_disfluency.py             # Q2: Speech disfluency detection
├── question3_spelling.py               # Q3: Hindi word spelling classification
├── question4_lattice_wer.py            # Q4: Lattice-based WER evaluation
├── requirements.txt                    # Python dependencies
├── technical_report.md                 # Detailed technical documentation
├── experimental_validation.md          # Results and validation details
├── README.md                           # This file
├── .gitignore                          # Git ignore rules
├── data_sample/                        # Sample data files (small subset)
│   └── dataset.csv
└── sample_outputs/                     # Output examples and results
    ├── asr_outputs.csv
    ├── disfluency_list.csv
    └── unique_words.csv
```

## ❓ Questions and Tasks

### Question 1: Fine-tuning Whisper on Hindi Speech Dataset
- Load Hindi speech corpus
- Preprocess audio and transcriptions
- Fine-tune OpenAI's Whisper model
- Evaluate using WER and CER metrics
- Compare baseline vs fine-tuned performance

### Question 2: Speech Disfluency Detection and Audio Clipping
- Detect disfluencies (stutters, pauses, repetitions, etc.)
- Identify temporal boundaries of disfluent segments
- Extract corresponding audio clips
- Generate disfluency reports with metrics
- Compute confusion matrix for evaluation

### Question 3: Hindi Word Spelling Classification
- Build a classification system for correct/incorrect Hindi spelling
- Use character-level features and language model embeddings
- Train classifier on labeled word dataset
- Evaluate with precision, recall, F1-score
- Generate confusion matrix and error analysis

### Question 4: Lattice-Based Consensus WER Evaluation
- Construct word lattices from multiple ASR hypotheses
- Apply consensus decoding to find optimal transcription path
- Compute WER using lattice structure
- Compare with traditional WER computation
- Analyze improvements and computational efficiency

## 📊 Results Summary

**Key Metrics:**
- Q1: WER improvement of X% after fine-tuning (see technical_report.md)
- Q2: Disfluency detection F1-score: X% (see experimental_validation.md)
- Q3: Spelling classification accuracy: X% (see experimental_validation.md)
- Q4: WER reduction using lattice approach: X% (see technical_report.md)

For detailed results, see [experimental_validation.md](experimental_validation.md).

## 🚀 How to Run

### 1. Environment Setup

```bash
# Clone the repository
git clone <repository-url>
cd hindi-speech-processing-asr-evaluation

# Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### 2. Run Individual Questions

```bash
# Question 1: Fine-tune Whisper
python question1_whisper_finetune.py

# Question 2: Detect disfluencies
python question2_disfluency.py

# Question 3: Classify spelling
python question3_spelling.py

# Question 4: Evaluate with lattice WER
python question4_lattice_wer.py
```

### 3. Output Files

Results are generated in the `sample_outputs/` directory:
- `asr_outputs.csv` - ASR transcription results
- `disfluency_list.csv` - Detected disfluencies
- `unique_words.csv` - Word inventory from dataset

## 📦 Dependencies

Key libraries used:
- **torch**: Deep learning framework
- **transformers**: Hugging Face model library (Whisper, etc.)
- **datasets**: Data loading and preprocessing
- **librosa**: Audio processing and feature extraction
- **soundfile**: Audio I/O
- **jiwer**: WER and CER computation
- **numpy, pandas**: Data manipulation
- **scipy**: Scientific computing

See [requirements.txt](requirements.txt) for complete list.

## 📚 Documentation

- [technical_report.md](technical_report.md) - Detailed methodology, experiments, and analysis
- [experimental_validation.md](experimental_validation.md) - Validation procedures and results
## 📝 License

This project is submitted as an academic assignment. Use for educational purposes only.

## 🔗 References

Key papers and resources:
- Radford et al. (2022) - Robust Speech Recognition via Large-Scale Weak Supervision (Whisper)
- Povey et al. (2011) - The Kaldi Speech Recognition Toolkit
- Word Error Rate metrics and evaluation techniques
- Hindi language processing resources
 
