**Real-Time Cricket Shot Classification and Automated Commentary**

**Purpose**
A system that processes live cricket video, identifies the shot being played, and generates instant, human-like commentary. Built for analytics, broadcasters, and interactive cricket applications.

**Core Function**
The pipeline ingests video frames, applies a CNN–LSTM model to classify the shot type, then constructs a text commentary snippet matched to the predicted class.

**Technical Structure**
CNN extracts spatial features from each frame. LSTM captures the temporal sequence across frames. Post-processing resolves frame-level predictions into a stable shot label. A lightweight app layer renders predictions and commentary.

**Model Details**
Trained on curated cricket footage. Optimized for multi-class shot recognition. Outputs categories such as cover drive, pull, sweep, cut, lofted shots, and defensive strokes.

**Application Layer**
A Streamlit interface provides real-time playback, shot detection, probability scores, and auto-generated commentary lines. Designed for single-video uploads and future extension to live streams.

**Repository Layout**
`src/core` contains inference, preprocessing, and postprocessing.
`src/app` contains UI logic.
`models` stores serialized weights.
`notebooks` holds exploratory training notebooks.
`tests` includes minimal verification scripts.

**Usage**
Install dependencies, place model files, run the Streamlit app, upload a cricket clip. The system displays classification and commentary in real time.

**Intended Extensions**
Live-feed integration, richer shot taxonomy, multilingual commentary, and performance tuning through improved datasets.
