# Ghana Sign Language (GSL) Translator 🚧

This repository contains an ongoing project developing a real-time Ghana Sign Language (GSL) translator aimed at improving communication between deaf or hard-of-hearing individuals and hearing communities in Ghana, particularly in healthcare and public accessibility contexts.

## Project Status
🚧 **Work in Progress**  
The project is actively under development. The focus is on experimentation, system design, and iterative improvement rather than delivering a finished product.

## System Overview
The GSL Translator is designed as a multi-stage AI pipeline:
Camera Input
→
Exported Teachable Machine Model
→
Word-Level Predictions (in app)
→
Timing & Buffering Logic
→
Sentence Construction Pipeline
→
Text / Speech Output
### 1. Sign Recognition
- Uses **Google Teachable Machine** to train a computer vision model that classifies individual GSL hand signs.
- Sign selection is informed by the [Ayele Foundation GSL Dictionary](https://www.ayelefoundation.org/gsl/).
- The trained model is exported and used in the application to produce **word-level predictions** in real time.

### 2. Timing and Buffering Logic
- Ensures that detected signs are **held long enough** to count as a word.
- Prevents repeated detections of the same sign.
- Detects pauses to signal sentence boundaries.

### 3. Sentence Construction
- Accumulated word outputs are processed through an AI pipeline.
- Combines rule-based logic and language-model techniques to **approximate GSL grammatical patterns** and convert sequences into clear English sentences.

## Tools and Technologies
- Google Teachable Machine (computer vision training)  
- Python / JavaScript for pipeline logic and app  
- Real-time webcam input  
- Language models for sentence construction (experimental)

## Limitations
- Currently supports only **basic signs and short phrases**.  
- Facial expressions and non-manual markers are not modeled.  
- Full linguistic translation of GSL grammar is outside the current scope.

## Future Work
- Expand the sign vocabulary  
- Improve timing stability and word confirmation  
- Refine sentence construction for better grammatical accuracy  
- Explore speech output for accessibility  
- Investigate sequence-based models for longer phrases

## Disclaimer
This is an educational and exploratory prototype, not a substitute for professional sign language interpreters.
