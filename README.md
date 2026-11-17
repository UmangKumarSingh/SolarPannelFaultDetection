Solar Panel Fault Detection with Deep Learning (Image Classification)
Overview
This project is an example from the AI for Energy Solutions course at MIT that I taught in January 2025. It showcases how deep learning and image classification can be applied to energy infrastructure monitoring.

The system is a web application that detects and classifies faults in solar panels, capable of analyzing:

Clean panels
Physical damage
Electrical damage
The project is designed to be accessible, beginning with a no-code approach using Google Teachable Machine, and optionally extending to coding and deployment for students looking to delve deeper into development.

https://teachablemachine.withgoogle.com/models/6ip1rASfF/

Screen Shot 2025-01-15 at 9 55 15 AM
Project Highlights
Beginner-Friendly: No-Code Model Training
Google Teachable Machine makes training an image classification model simple and intuitive.
No prior coding knowledge is required.
Learn to create a powerful AI model with just a few clicks.
Optional Advanced: Coding & Deployment
For students interested in exploring coding and deployment:

Use Python to process data and deploy a real-world application.
Build a web app with Streamlit to make the model user-friendly.
Enhance functionality with batch processing, CSV downloads, and more.
What You'll Learn
This project teaches students to:

No-Code Training:
Train an image classifier using Google Teachable Machine.
Optional Coding Section:
Deploy the trained model in a Python-based web app.
Use Streamlit for a professional, user-friendly interface.
Practical Applications:
Analyze single images or batches for energy monitoring tasks.
Expand capabilities to other types of energy infrastructure.
Features
No-Code: Train a model without programming.
Single & Batch Processing: Analyze one or many images.
Real-Time Results: Confidence scores for multiple classifications.
Web Interface: Interactive and accessible, powered by Streamlit.
Deployment Ready: Preconfigured for easy deployment.
Future Directions
Integrating drone imagery for automated inspections.
Expanding to other renewable energy systems (e.g., wind turbines).
Mobile app development for field use.
Getting Started
Prepare Your Dataset

To follow along with this tutorial, you can download images from this Kaggle solar panel dataset: https://www.kaggle.com/datasets/pythonafroz/solar-panel-images. Unzip the files. OR
Collect ~50+ images per category. You could find a dataset through a website like Kaggle or create your own dataset.
Ensure diverse conditions (lighting, angles, distances)
Include both positive and negative examples
Label your images consistently
Train Using Google Teachable Machine

Visit Teachable Machine
Create a new Image Project
Upload your images for each class and name each class
Screen Shot 2025-01-10 at 8 16 43 PM
Set training parameters:
Epochs: 50 (adjust based on performance)
Batch Size: 16
Learning Rate: 0.001
Screen Shot 2025-01-10 at 8 31 25 PM
Train the model
Test it with other images
Export it to the web by clicking Export, then Upload. Feel free to test the web link and share it with your friends.
Congratulations, you have created an image classification deep learning model project!
Screen Shot 2025-01-15 at 9 42 50 AM
Optional: Follow the instructions in the repository below to:

Build a Python-based app using Streamlit.
Customize features for advanced use cases.
Optional Project: Code and Deploy
This project was created as an example project for the AI for Energy Solutions course that I taught at MIT in January 2025. It demonstrates how deep learning and image classification can be applied to real-world energy infrastructure monitoring.

The system is a deep learning-powered web application that detects and classifies faults in solar panels using transfer learning and image classification. It can analyze both single images and batch process multiple images to identify three conditions:

Clean panels
Physical damage
Electrical damage
Live Demo

This project was partly inspired by AIAnytime's Waste Classifier project and adapted its initial codebase from their waste classification system.

Screen Shot 2025-01-10 at 9 48 39 PM Screen Shot 2025-01-10 at 10 11 50 PM Screen Shot 2025-01-10 at 9 49 29 PM
This implementation shows students how to:

Train a custom image classification model using Google Teachable Machine
Deploy a deep learning model in a user-friendly web interface
Process both single and batch images for real-world applications
Handle multiple classification categories with confidence scoring
Features
Single image analysis with detailed confidence scores
Batch processing capability for multiple panels
Real-time analysis with progress tracking
Downloadable results in CSV format
User-friendly interface built with Streamlit
High accuracy classification using TensorFlow Lite
Tech Stack
Python
TensorFlow Lite
Streamlit
Google Teachable Machine
PIL (Python Imaging Library)
Pandas
NumPy
Model Training
The model was trained using Google Teachable Machine with:

50+ images for each condition
Three classification categories
Image augmentation for better generalization
Transfer learning using MobileNet architecture
Setup and Installation
Export Model from Teachable Machine
Export the model as TensorFlow Lite.

Screen Shot 2025-01-10 at 9 36 39 PM
Local Development
Clone the repository:
git clone https://github.com/jtwirly/solarpanelfaultdetection/
cd solarpanelfaultdetection
Install required packages:
pip install -r requirements.txt
Run the application locally:
streamlit run app.py
Streamlit Cloud Deployment
Fork the repository to your GitHub account

Visit Streamlit Share and sign in with your GitHub account

Click "New app" and select:

Repository: solarpanelfaultdetection
Branch: main
Main file path: app.py
Click "Deploy"

Your app will be available at: https://[your-username]-solarpanelfaultdetection-streamlit-app.streamlit.app or whatever you choose to set the URL as.

Note: The repository already includes:

converted_model.tflite (TensorFlow Lite model) - or use your own (exported from Teachable Machine)
labels.txt (Class labels)
requirements.txt (Dependencies)
No additional configuration is needed for deployment.

Usage
Single Image Analysis
Select the "Single Image Analysis" tab
Upload a solar panel image
Click "Analyze Image"
View the results showing:
Panel condition
Confidence score
Detailed probability breakdown
Batch Analysis
Select the "Batch Analysis" tab
Upload multiple solar panel images
Click "Analyze All Images"
Monitor the progress bar
View summary statistics and detailed results
Download results as CSV if needed
Model Performance
The current model achieves:

High confidence scores for clean panels (typically >90%)
Accurate classification of physical damage patterns
Reliable identification of electrical faults
Fast inference time suitable for real-time analysis
Future Enhancements
Integration with drone imagery systems
Time series analysis for degradation tracking
Automated report generation
Geographic mapping of panel conditions
Mobile app development
Customizing the Project
This project can be adapted for various energy infrastructure monitoring applications. Check otherideas.txt for a comprehensive list of potential adaptations. You can also modify the Streamlit code to suit your needs, using Claude or otherwise to generate the code or writing it yourself.

Modify the Code

Update labels.txt with your categories:
0 YourClass1
1 YourClass2
2 YourClass3
Rename your model to converted_model.tflite
Adjust the display messages in app.py:
def format_condition(condition):
    """Format condition text for display"""
    if condition == "YourClass1":
        return "Your Display Text 1"
    elif condition == "YourClass2":
        return "Your Display Text 2"
    return condition
Customize the Interface

Modify the code in app.py (you can use Claude or ChatGPT to help if desired)
Modify the title and descriptions
Adjust confidence thresholds if needed
Add custom metrics relevant to your use case
Update the results display format
Best Practices for Adaptation
Data Collection

Use real-world examples
Include various environmental conditions
Consider seasonal variations
Document image sources and conditions
Model Training

Start with default parameters
Experiment with learning rates
Monitor for overfitting
Validate with test images
Testing & Validation

Use a separate test dataset
Verify performance across all categories
Test edge cases
Document accuracy metrics
Deployment Considerations

Update requirements.txt if needed
Test thoroughly before deployment
Consider scalability
Document any special requirements
Example Adaptation (Wind Turbine)
# Example labels.txt for wind turbine inspection
0 Normal
1 BladeDamage
2 IceAccumulation
3 Corrosion

# Example condition formatting
def format_condition(condition):
    conditions = {
        "Normal": "✅ Normal Operation",
        "BladeDamage": "🚨 Blade Damage Detected",
        "IceAccumulation": "❄️ Ice Accumulation",
        "Corrosion": "⚠️ Corrosion Detected"
    }
    return conditions.get(condition, condition)
Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

License
MIT

Acknowledgments
Original inspiration: AIAnytime's Waste Classifier
Thanks to Google Teachable Machine for making ML model training accessible
