
# Project Overview: EmojiWave Project: Real-Time Hand Gesture Recognition with Emoji Feedback
This project was built during an 8-day sprint in the Saudi Digital Academy’s Data Science Bootcamp, in partnership with Le Wagon.

It detects hand gestures from a webcam or uploaded image, predicts the gesture using a custom-trained CNN model, and displays the corresponding emoji on-screen using Streamlit.

Our project is an intelligent interactive system that recognizes hand gestures in real-time using a camera and instantly displays the corresponding emoji—no touch or voice required.

# Why This Project Matters
Interacting with machines should be natural, inclusive, and touchless when needed. Our system offers an alternative interaction model that is not only fun, but potentially life changing for users with accessibility needs, presenters, and more.

# My Team
- Noura Alzahrani
- Norah Alharbi
- Amal Alahmadi
- Yousif Alnasser

# Tech Stack
- Python
- TensorFlow
- OpenCV
- Streamlit
- Jupyter / Google Colab
- Docker
- VS Code

#Challenges & Solutions
#1. Low Accuracy with Camera Input
- Problem: Model failed to predict correctly using real-time camera images.
- Cause: Camera input looked different from training data.
- Solution: Built 3 separate preprocessing pipelines for:
  - Training data
  - Uploaded images
  - Webcam frames

#2.Choosing the Right Model
- We tested both pretrained and custom models.
- Our best-performing model was built from scratch, reaching 99% accuracy after tuning.

#3.Time Constraints
- Project duration: 8 days only.
- Each team member worked on specific tasks with high coordination.

#Features
- Upload an image OR use your webcam live
- Real-time emoji overlay based on predicted gesture
- Fun, personal experience
- Portable deployment via Docker

# Future Enhancements
- Assign functionality to gestures (volume, slides, etc.)
- Transparent/no UI mode
- Multi-user recognition
- Wider gesture/emotion recognition

# Project Structure

EmojiWave/
├── __pycache__/                # Compiled Python files for faster loading
├── fast.py                     # FastAPI application for serving the model
├── model.py                    # Contains the model architecture
├── preprocess.py               # Data preprocessing functions
├── notebooks/                  # Jupyter notebooks for experiments
│   ├── final_model_acc99.h5    # Final trained model with 99% accuracy
│   ├── Baseline_Model.ipynb    # Notebook for baseline model training
│   ├── EDA.ipynb               # Exploratory Data Analysis notebook
│   ├── PreProcess.ipynb        # Notebook for data preprocessing
│   ├── Best_Model.ipynb        # Notebook for fine-tuning the best model
│   └── plots/                  # Directory for storing plots
│       ├── baseline_model.jpeg  # Visualization of baseline model results
│       └── best_model.jpeg      # Visualization of best model results
├── streamlit_app/              # Directory for Streamlit application
│   ├── pages/                  # Subdirectory for app pages
│   ├── EmojiWave-unscreen-1.gif # GIF for the application
│   └── Home.py                 # Main home page of the Streamlit app
├── requirements.txt            # List of project dependencies
├── .gitignore                  # Files and directories to be ignored by Git
└── README.md                   # This README file

# How to Run
1. Clone the repo
2. Install requirements
3. Launch Streamlit:
```bash
streamlit run app.py
