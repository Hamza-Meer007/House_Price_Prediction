# 🏠 Bangalore Home Price Prediction

A machine learning web application that predicts home prices in Bangalore based on location, square footage, number of bedrooms (BHK), and bathrooms. The project uses a trained scikit-learn model with a Flask backend API and a responsive HTML/CSS/JavaScript frontend.

## 🌟 Features

- **Real-time Price Prediction**: Get instant home price estimates based on your inputs
- **Location-based Analysis**: Covers multiple areas across Bangalore
- **User-friendly Interface**: Clean and intuitive web interface
- **Machine Learning Model**: Built using scikit-learn with data preprocessing and outlier removal
- **RESTful API**: Flask-based backend with CORS support

## 🛠️ Technology Stack

- **Backend**: Python, Flask, scikit-learn, NumPy
- **Frontend**: HTML5, CSS3, JavaScript, jQuery
- **Machine Learning**: Linear Regression model trained on Bangalore housing data
- **Data Processing**: Pandas, feature engineering, outlier detection

## 📋 Prerequisites

Before running this project, make sure you have:

- Python 3.7 or higher installed
- A modern web browser
- Live Server extension (for VS Code) or any local server setup

## 🚀 Installation & Setup

### Step 1: Install Dependencies

First, install the required Python packages:

```bash
pip install -r requirements.txt
```

The requirements include:

- Flask (web framework)
- numpy (numerical computations)
- scikit-learn (machine learning)

### Step 2: Start the Backend Server

Navigate to the server folder and run the Flask application:

```bash
cd server
python server.py
```

You should see output similar to:

```
Starting Python Flask Server For Home Price Prediction...
 * Running on http://127.0.0.1:5000
 * Debug mode: on
```

### Step 3: Launch the Frontend

1. Navigate to the `client` folder
2. Open `app.html` with Live Server (if using VS Code) or any local server
3. If using Live Server in VS Code:
   - Right-click on `app.html`
   - Select "Open with Live Server"

Alternatively, you can open `app.html` directly in your browser, but using a local server is recommended for best performance.

## 🎯 How to Use

1. **Enter Area**: Input the total area in square feet
2. **Select BHK**: Choose the number of bedrooms (1-5)
3. **Select Bathrooms**: Choose the number of bathrooms (1-5)
4. **Choose Location**: Select from available Bangalore locations
5. **Get Prediction**: Click "Estimate Price" to get the predicted price in Lakhs

   # Preview

   ![Bangalore Home Price Prediction](BHP_website.PNG)

## 📊 Model Information

The machine learning model was trained on Bangalore housing data with the following features:

- **Data Cleaning**: Handled missing values and inconsistent data formats
- **Feature Engineering**: Extracted BHK from size, calculated price per sqft
- **Outlier Removal**: Removed properties with unusual price per sqft ratios
- **Location Encoding**: One-hot encoded location features
- **Model**: Linear Regression for price prediction

## 📁 Project Structure

```
House Price Prediction/
├── client/
│   ├── app.html          # Main frontend interface
│   ├── app.css           # Styling
│   └── app.js            # Frontend JavaScript logic
├── server/
│   ├── server.py         # Flask backend server
│   ├── util.py           # Utility functions for ML model
│   └── artifacts/        # Trained model and data files
├── model/
│   ├── banglore_home_prices_final.ipynb  # Model training notebook
│   └── *.csv             # Training datasets
├── requirements.txt      # Python dependencies
└── README.md            # This file
```

## 🔧 API Endpoints

- **GET** `/get_location_names` - Returns available location names
- **POST** `/predict_home_price` - Predicts home price based on input parameters

## 🤝 Contributing

Feel free to fork this project and submit pull requests for any improvements!

## 📝 License

This project is open source and available under the MIT License.

---

**Note**: Make sure both the Flask server (Step 2) and the frontend (Step 3) are running simultaneously for the application to work properly. The frontend communicates with the backend API to get price predictions.
