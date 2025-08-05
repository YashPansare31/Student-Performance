# Student Exam Performance Prediction

A Flask web application that predicts student performance scores based on demographic and test preparation data using machine learning.

## 🎯 Overview

This project leverages machine learning to predict student exam performance based on various factors including gender, parental level of education, lunch type, test preparation course completion, and previous test scores. The application provides an intuitive web interface for easy data input and real-time predictions.

## ✨ Features

- **Interactive Web Interface**: User-friendly forms for inputting student demographics and test data
- **Real-time Predictions**: Instant performance score predictions using trained ML models
- **Data Preprocessing**: Automatic feature scaling and preprocessing pipeline
- **Modular Architecture**: Clean, maintainable code structure with separate pipeline components
- **Responsive Design**: Works seamlessly across different devices and screen sizes

## 🏗️ Project Structure
```
student-performance-prediction/
├── .ebextensions/
├── artifacts/
│   ├── data.csv
│   ├── model.pkl
│   ├── proprocessor.pkl
│   ├── test.csv
│   └── train.csv
├── catboost_info/
│   ├── learn/
│   ├── catboost_training.json
│   ├── learn_error.tsv
│   └── time_left.tsv
├── notebook/
│   ├── data/
│   ├── EDA_STUDENT_PERFORMANCE.ipynb
│   └── MODEL_TRAINING.ipynb
├── src/
│   ├── components/
│   │   ├── __init__.py
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   ├── pipeline/
│   │   ├── __init__.py
│   │   ├── predict_pipeline.py
│   │   └── train_pipeline.py
│   ├── __init__.py
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
├── templates/
│   ├── index.html
│   └── home.html
├── .gitignore
├── app.py
├── README.md
├── requirements.txt
└── setup.py
```
## 🚀 Quick Start

### Prerequisites

- Python 3.7 or higher
- pip (Python package installer)
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd student-exam-performance-prediction
   ```

2. **Create a virtual environment**
   ```bash
   # Create virtual environment
   python -m venv venv
   
   # Activate virtual environment
   # On Windows:
   venv\Scripts\activate
   
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   python app.py
   ```

5. **Access the application**
   
   Open your web browser and navigate to Home Page:
   ```
   http://localhost:5000
   ```

   To Predict Marks:
    ```
    http://localhost:5000/predictdata
    ```

## 📊 How to Use

1. **Navigate to the Home Page**: Click on the "Go to Home Page" button from the landing page
2. **Fill in Student Details**: 
   - Select gender
   - Choose parental level of education
   - Select lunch type (standard/free or reduced)
   - Indicate test preparation course completion
   - Enter reading and writing scores
3. **Get Prediction**: Submit the form to receive the predicted math score
4. **View Results**: The predicted performance score will be displayed on the same page

## 🛠️ Technical Details

### Core Components

- **CustomData Class**: Handles data transformation and validation
- **PredictPipeline Class**: Manages the ML prediction workflow
- **Flask Routes**: Handle web requests and responses
- **HTML Templates**: Provide the user interface

### Machine Learning Pipeline

1. **Data Collection**: User inputs are collected through web forms
2. **Preprocessing**: Features are scaled and transformed using saved preprocessors
3. **Prediction**: Trained ML model generates performance predictions
4. **Output**: Results are displayed in a user-friendly format

## 📦 Dependencies

- **Flask**: Web framework for the application
- **NumPy**: Numerical computing library
- **Pandas**: Data manipulation and analysis
- **Scikit-learn**: Machine learning library
- **Dill**: Extended pickle functionality for model serialization

*See `requirements.txt` for complete dependency list with versions.*

## 🔧 Configuration

The application runs on:
- **Host**: 127.0.0.1 (accessible from any IP)
- **Port**: 5000
- **Debug Mode**: Enabled for development

## 📈 Model Performance

The machine learning model has been trained on student performance data and achieves reliable predictions for academic outcomes based on the input features.

## 🚀 Deployment

### Local Development
Follow the installation steps above for local development.

### Production Deployment
For production deployment, consider:
- Setting `debug=False` in app.py
- Using a production WSGI server like Gunicorn
- Implementing proper error handling and logging
- Adding environment-specific configurations

## 🔮 Future Enhancements

- [ ] **User Authentication**: Add login/registration functionality
- [ ] **Data Visualization**: Include charts and graphs for better insights
- [ ] **Model Retraining**: Implement automated model updates
- [ ] **API Endpoints**: Create REST API for programmatic access
- [ ] **Database Integration**: Store predictions and user data
- [ ] **Cloud Deployment**: Deploy on AWS, GCP, or Azure
- [ ] **CI/CD Pipeline**: Automated testing and deployment
- [ ] **Mobile App**: Develop companion mobile application

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

If you encounter any issues or have questions:
- Open an issue on GitHub
- Check the documentation
- Review the code comments for implementation details

## 🙏 Acknowledgments

- Thanks to the contributors of the libraries used in this project
- Educational datasets that made this project possible
- The open-source community for continuous inspiration

---
