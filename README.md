# AI-Powered-Portable-Health-Screening-Kiosk-for-Smart-Rural-Healthcare-Monitoring
AI-powered healthcare kiosk built with Python, Flask, and SQLite for multilingual symptom assessment, disease prediction, and patient record management. Uses ensemble machine learning with 92% accuracy and SHAP-based explainable AI. Includes automated health report generation and a user-friendly web interface for accessible healthcare monitoring.
🏥 AI-Powered Portable Health Screening Kiosk

Smart Rural Healthcare Monitoring using AI, Machine Learning & Explainable AI

An AI-powered multilingual healthcare screening kiosk designed to provide accessible preliminary health assessment for rural and underserved communities.

The system combines Google Gemini AI, XGBoost, SHAP Explainable AI, Flask, and SQLite to analyze patient symptoms, predict possible diseases, explain predictions, generate health reports, and maintain patient records.

«⚠️ Disclaimer: This project is an academic/prototype healthcare decision-support system. It is not intended to replace professional medical diagnosis or treatment.»

---

📌 Project Overview

Healthcare accessibility remains a major challenge in rural areas because of limited medical infrastructure, shortage of healthcare professionals, language barriers, and limited health awareness.

This project proposes a portable healthcare kiosk that allows users to:

- Register their basic information
- Select their preferred language
- Enter symptoms using text or voice
- Interact with an AI-powered symptom analysis system
- Receive a preliminary disease prediction
- View prediction confidence
- Understand important contributing symptoms using SHAP
- Generate a downloadable PDF health report
- Store consultation history
- View healthcare analytics through a dashboard

The system supports multilingual interaction, including English, Hindi, and Kannada.

---

✨ Key Features

👤 Patient Registration

- Patient profile creation
- Name, age, gender and mobile number
- Patient ID generation
- Patient history management

🌐 Multilingual Interface

Supports interaction in:

- 🇬🇧 English
- 🇮🇳 Hindi
- 🇮🇳 Kannada

The system is designed to make healthcare screening more accessible to users with different linguistic and literacy backgrounds.

🎙️ Voice & Text Symptom Input

Users can describe their symptoms using:

- Text input
- Voice input
- Speech-to-text processing

The interface uses browser-based speech capabilities for voice interaction.

🤖 AI Symptom Analysis

Google Gemini AI is used to process natural-language symptom descriptions and extract structured information such as:

- Symptoms
- Severity
- Duration
- Frequency
- Affected body parts
- Additional medical information

🧠 Disease Prediction

An XGBoost classifier processes engineered symptom features and predicts the most probable disease category.

The project considers diseases including:

- Common Cold
- Influenza
- Gastroenteritis
- Malaria
- Tuberculosis
- Asthma
- Allergy
- Dengue

🔍 Explainable AI

SHAP (SHapley Additive exPlanations) is used to explain the model's predictions.

The system identifies:

- Important symptoms
- Feature contribution
- Positive/negative influence
- Relative feature importance

This helps make the ML prediction more understandable.

📄 Automated Health Reports

The system generates PDF reports containing information such as:

- Patient details
- Symptoms
- Predicted disease
- Confidence score
- Severity
- Precautionary measures
- Suggested medication information
- Specialist consultation guidance

🗄️ Patient Record Management

Patient and consultation information is stored using SQLite.

The database maintains:

- Patient details
- Consultation history
- Symptoms
- Prediction results
- Confidence scores
- SHAP explanations
- Generated reports

📊 Analytics Dashboard

The dashboard provides visualizations for:

- Total patients
- Consultation statistics
- Disease distribution
- Demographic information
- Healthcare trends

📱 Report Delivery

The proposed system also supports report delivery through the WhatsApp Cloud API.

---

🏗️ System Architecture

The system follows a modular architecture consisting of:

                    ┌─────────────────────────┐
                    │       Patient/User      │
                    └────────────┬────────────┘
                                 │
                     Voice / Text Input
                                 │
                                 ▼
              ┌─────────────────────────────────┐
              │       Presentation Layer        │
              │ HTML • CSS • JavaScript         │
              │ Bootstrap • Web Speech API      │
              └───────────────┬─────────────────┘
                              │
                              ▼
              ┌─────────────────────────────────┐
              │        Application Layer        │
              │             Flask               │
              │ Registration • Sessions • APIs  │
              └───────────────┬─────────────────┘
                              │
                              ▼
              ┌─────────────────────────────────┐
              │            AI Layer             │
              │                                 │
              │  Google Gemini → NLP/Symptoms   │
              │          ↓                      │
              │  Feature Engineering            │
              │          ↓                      │
              │  XGBoost → Disease Prediction  │
              │          ↓                      │
              │  SHAP → Explanation             │
              └───────────────┬─────────────────┘
                              │
                              ▼
              ┌─────────────────────────────────┐
              │          Data Layer             │
              │            SQLite               │
              │ Patient Records • Consultations│
              │ Reports • System Logs           │
              └───────────────┬─────────────────┘
                              │
                ┌─────────────┴─────────────┐
                ▼                           ▼
        ┌───────────────┐           ┌───────────────┐
        │ PDF Report    │           │   Dashboard   │
        │ Generation    │           │  & Analytics  │
        └───────────────┘           └───────────────┘

The project report describes the architecture in terms of presentation, application, AI/ML, and data layers.

---

🔄 System Workflow

Patient Registration
        ↓
Language Selection
        ↓
Symptom Input
(Voice / Text)
        ↓
Gemini AI
        ↓
Structured Symptom Extraction
        ↓
Feature Engineering
        ↓
XGBoost Disease Prediction
        ↓
Confidence Score
        ↓
SHAP Explanation
        ↓
Health Assessment
        ↓
PDF Report Generation
        ↓
Database Storage
        ↓
Dashboard / Report Delivery

---

🛠️ Technology Stack

Category| Technology
Programming Language| Python 3.11+
Backend| Flask
Frontend| HTML5, CSS3, JavaScript
UI Framework| Bootstrap 5
AI/NLP| Google Gemini AI
Machine Learning| XGBoost
Explainable AI| SHAP
Data Processing| Pandas, NumPy
Visualization| Plotly
Database| SQLite
ORM| SQLAlchemy
Voice Input| Web Speech API
Text-to-Speech| gTTS
PDF Generation| Python PDF generation libraries
Development Environment| Visual Studio Code

The project report specifies Python 3.11+, Flask, HTML5/CSS3/JavaScript, Bootstrap 5, SQLite, Gemini AI, XGBoost, Ensemble methods, and SHAP among the primary software technologies.

---

📁 Project Structure

AI-Healthcare-Kiosk/
│
├── app.py
├── requirements.txt
├── README.md
├── .env.example
│
├── models/
│   ├── xgboost_model.pkl
│   └── model_metadata.pkl
│
├── data/
│   └── dataset.csv
│
├── database/
│   └── healthcare.db
│
├── templates/
│   ├── index.html
│   ├── registration.html
│   ├── symptoms.html
│   ├── result.html
│   ├── report.html
│   └── dashboard.html
│
├── static/
│   ├── css/
│   ├── js/
│   └── images/
│
├── reports/
│   └── generated_reports/
│
└── utils/
    ├── prediction.py
    ├── gemini.py
    ├── shap_explainer.py
    └── report_generator.py

«Adjust the structure above to match the actual files in your GitHub repository.»

---

⚙️ Installation

1. Clone the repository

git clone https://github.com/YOUR_USERNAME/AI-Healthcare-Kiosk.git

2. Navigate to the project

cd AI-Healthcare-Kiosk

3. Create a virtual environment

python -m venv venv

4. Activate the virtual environment

Windows:

venv\Scripts\activate

Linux/macOS:

source venv/bin/activate

5. Install dependencies

pip install -r requirements.txt

---

🔐 Environment Variables

Create a ".env" file in the project root:

GEMINI_API_KEY=your_gemini_api_key

# Optional WhatsApp Cloud API configuration
WHATSAPP_ACCESS_TOKEN=your_access_token
WHATSAPP_PHONE_NUMBER_ID=your_phone_number_id

«Never commit API keys, passwords, tokens, database credentials, or other secrets to GitHub.»

Add ".env" to ".gitignore":

.env
venv/
_pycache_/
*.pyc
*.db
reports/generated_reports/

---

▶️ Running the Application

Start the Flask application:

python app.py

Then open:

http://127.0.0.1:5000

The application can then be accessed through the browser.

---

🧠 Machine Learning Pipeline

The ML pipeline consists of the following stages:

Raw Patient Symptoms
        ↓
Gemini AI Symptom Understanding
        ↓
Structured Medical Information
        ↓
Feature Engineering
        ↓
XGBoost Classifier
        ↓
Disease Probability
        ↓
Prediction
        ↓
SHAP Explanation

The project uses engineered features including symptom count, severity, duration, frequency, and patient age.

---

🔬 Explainable AI with SHAP

SHAP is used to explain how individual features contribute to the model prediction.

Example output:

Predicted Disease: Malaria

Important Factors:
✓ High fever
✓ Chills
✓ Fatigue
✓ Headache

Prediction Confidence:
85%

The SHAP module generates feature contribution values that can be presented through visual and textual explanations.

---

📊 Dashboard

The administrator dashboard can provide information such as:

- Total patient registrations
- Number of consultations
- Disease distribution
- Consultation trends
- Demographic statistics
- Recent consultations

This enables healthcare administrators to analyze collected information and monitor healthcare trends.

---

🧪 Testing

The system includes testing of major modules such as:

- Patient registration
- Language selection
- Symptom input
- Voice input
- Gemini AI integration
- Disease prediction
- SHAP explanation
- PDF generation
- Database operations
- Dashboard functionality
- Report delivery

The project report contains a dedicated system-testing chapter covering testing methodology, test cases, and test results.

---

🚀 Future Enhancements

Potential future improvements include:

- Integration with additional IoT health sensors
- Blood pressure monitoring
- Pulse oximetry
- Temperature monitoring
- Heart-rate monitoring
- More regional language support
- Improved offline functionality
- Cloud-based healthcare record synchronization
- Mobile application integration
- Advanced disease prediction models
- Integration with healthcare professionals
- Improved security and privacy mechanisms
- Deployment across multiple rural healthcare centers

---

🎯 Project Objectives

The major objectives of the project are:

1. Develop a multilingual, voice-enabled healthcare kiosk.
2. Integrate AI-powered symptom analysis.
3. Implement ML-based disease prediction.
4. Provide explainable AI using SHAP.
5. Generate automated healthcare reports.
6. Maintain patient records.
7. Provide real-time healthcare analytics.
8. Implement rule-based fallback functionality.
9. Develop an affordable and scalable rural healthcare screening solution.

---

📚 Research Foundation

The project builds upon research related to:

- Artificial Intelligence in healthcare
- AI-assisted rural healthcare
- Machine learning-based disease prediction
- Explainable AI
- XGBoost-based medical classification
- Symptom-based disease prediction
- AI-assisted remote healthcare

The project report includes a literature survey covering these areas.

---

👩‍💻 Author

Spandana Indira R

M.Tech – Artificial Intelligence and Data Science
MVJ College of Engineering, Bengaluru
2025–2026

Project Guide:
Prof. P. Bindu Madhavi
Assistant Professor
Department of Information Science & Engineering
MVJ College of Engineering, Bengaluru

---

📄 Academic Project

This project was developed as a Mini Project for the Master of Technology in Artificial Intelligence and Data Science at MVJ College of Engineering, Bengaluru.

---

⭐ If you find this project useful

If this project helps you understand AI, machine learning, explainable AI, or healthcare technology:

⭐ Star this repository
🍴 Fork the repository
💡 Feel free to explore and improve the project

---

⚠️ Medical Disclaimer

This software is an academic/prototype system intended for preliminary health screening and educational purposes.

The predictions generated by the system should not be considered a medical diagnosis. Users should consult qualified healthcare professionals for diagnosis, treatment, medication decisions, and emergency medical care.
