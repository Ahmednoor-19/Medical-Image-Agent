# Medical Image Agent 🩺🔬

An AI-powered medical image analysis tool that provides detailed diagnostic insights from various medical imaging modalities.

## Overview

Medical Image Agent leverages advanced AI models to analyze medical images (X-ray, MRI, CT, Ultrasound, etc.) and provides structured reports with diagnostic assessments, patient-friendly explanations, and relevant research context. This Streamlit-based application makes sophisticated medical image analysis accessible with just a few clicks.

## Features

- **Multi-Modal Support**: Analyze X-rays, MRI, CT scans, Ultrasound images, and more
- **Comprehensive Reports**: Get structured analysis including:
  - Image type and regional identification
  - Key findings and abnormalities
  - Diagnostic assessment with confidence levels
  - Patient-friendly explanations
  - Research context with supporting literature
- **User-Friendly Interface**: Simple upload-and-analyze workflow
- **Research Integration**: Automatically searches for relevant medical literature

## Installation

### Prerequisites

- Python 3.8+
- pip package manager

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Medical-Image-Agent.git
   cd Medical-Image-Agent
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up your Google API key:
   - Get a Gemini API key from Google AI Studio
   - Set it as an environment variable or directly in the app.py file

## Usage

1. Start the application:
   ```bash
   streamlit run app.py
   ```

2. Open your web browser and navigate to the displayed URL (typically http://localhost:8501)

3. Upload a medical image using the file uploader in the sidebar

4. Click "Analyze Image" to process the image

5. Review the comprehensive analysis report

## Dependencies

- Streamlit: Web application framework
- PIL (Pillow): Image processing
- Agno: AI agent framework
- Google Gemini: AI model for image analysis
- DuckDuckGo Tools: For medical literature search

## Configuration

The application uses the Gemini 2.0 Flash model. You can modify the model or other parameters in the `app.py` file:

```python
medical_agent = Agent(
    model=Gemini(id="gemini-2.0-flash-exp"),
    tools=[DuckDuckGoTools()],
    markdown=True
)
```
