# Handwritten Text Recognition

A **handwritten text recognition (HTR)** system developed as a graduation project at Helwan University. The application combines a React frontend with a Flask backend and a trained recognition model to convert handwritten images into digital text.

## Key Features

- Upload handwritten images from the web interface
- Image preprocessing with OpenCV
- Handwritten text inference through the recognition model
- Confidence score returned by the backend
- Post-processing and text correction with SymSpell
- REST endpoint for image-to-text conversion
- React frontend connected to the Flask API

## Tech Stack

**Frontend**
- React 18
- Axios
- Bootstrap / React-Bootstrap
- React Icons

**Backend & ML**
- Python
- Flask
- TensorFlow
- OpenCV
- NumPy
- SymSpell

## Architecture

```text
React Frontend
      ↓
Flask REST API
      ↓
Image Preprocessing
      ↓
HTR Model Inference
      ↓
Text Correction
      ↓
Recognized Text + Confidence
```

## Project Structure

```text
Handwritten-Text-Recognition/
├── frontend/
│   └── src/
├── backend/
│   ├── flask/
│   │   ├── app.py
│   │   ├── htr_module.py
│   │   └── model/
│   └── requirements.txt
└── README.md
```

## Run Locally

### Backend

```bash
cd backend
pip install -r requirements.txt
cd flask
python app.py
```

### Frontend

Open another terminal:

```bash
cd frontend
npm install
npm start
```

The frontend runs on **http://localhost:3000** by default.

## API

```http
POST /convert
```

Upload an image using the `image` form field. The API returns recognized text, confidence, and corrected text.

## Author

**Eslam Ayman**  
Helwan University — 2024
