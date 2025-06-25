# ECO Smart Hub

Eco Smart Hub is a centralized, eco-friendly web application developed using Python Flask. It offers four key features that help users manage waste, track energy consumption, and locate recycling centers efficiently.

## Main Interface

The main dashboard is developed using:
- Python Flask (with Blueprints for modular routing)
- HTML, CSS, JavaScript

This interface links to the four core features of the application.

## Features

### 1. Waste Management Chatbot

An AI-powered chatbot designed specifically to answer questions about waste management.

- Model Used: qwen3-30b-a3b via OpenRouter API
- Technologies: Python Flask, HTML, CSS, JavaScript
- Functionality:
  - Requires selecting a waste type (e.g., plastic, glass, food).
  - Displays suggested questions based on the selected waste type.
  - Users can ask a custom question (only if it is related to waste).
  - Answers are generated using the AI model through the OpenRouter API.

### 2. Waste Classification Model

A computer vision model that predicts the type of waste from an uploaded image.

- Model Used: MobileNetV2 pretrained on ImageNet
- Technologies: Python Flask, HTML, CSS, JavaScript
- Functionality:
  - Supports classification of 20–22 different waste categories.
  - If the model's confidence is below 75%, the prediction is not shown.
  - Users can upload an image and view the classification result through a simple UI.

### 3. Recycling Center Locator

Helps users find nearby dumping yards, waste disposal areas, or recycling centers.

- API Used: Google Maps API
- Technologies: Python Flask, HTML, CSS, JavaScript
- Functionality:
  - Users can manually enter a location or use the "Use My Location" option.
  - Displays nearby facilities on an interactive map.

### 4. Energy Tracker

A tool for tracking electricity usage and receiving AI-based suggestions for optimization.

- Model Used for Suggestions: qwen3-30b-a3b via OpenRouter API
- Technologies: Python Flask, HTML, CSS, JavaScript
- Functionality:
  - Users enter appliance wattage, usage hours per day, and usage days per month.
  - Displays a graph showing energy consumption.
  - Provides smart suggestions to reduce electricity usage.
  - Data can be exported in CSV or JSON format.

## How to Run the Project

1. Clone the repository:

   bash
   git clone https://github.com/DhruthiCHegde/EcoSmart-Hub
   cd eco-smart-hub
   

2. Install dependencies:

   bash
   pip install -r requirements.txt
   

3. Run the application:

   bash
   python app.py
  

4. Open your browser and navigate to:

   http://127.0.0.1:5000
   

## Tech Stack

- Backend: Python Flask (with Blueprints)
- Frontend: HTML, CSS, JavaScript
- AI Models: Qwen3-30b-a3b via OpenRouter API, MobileNetV2
- APIs: Google Maps API, OpenRouter API

## Project Structure (Simplified)


eco-smart-hub/
├── app.py
├── /static/
├── /templates/
├── /blueprints/
│   ├── chatbot/
│   ├── classifier/
│   ├── locator/
│   └── energy_tracker/
├── requirements.txt
└── README.md


## Acknowledgements

- OpenRouter AI for AI-based chatbot and energy suggestions
- Google Maps API for recycling center data
- TensorFlow/Keras for image classification model

## Future Improvements

- Add user authentication
- Store chatbot query history
- Improve visualization of classification confidence
- Add user-generated recycling center reviews or contributions
