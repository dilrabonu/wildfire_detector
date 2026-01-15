# Wildfire Image Detector & Chat Assistant 🔥💬

A deep learning project that combines wildfire image classification with a chatbot-style interface using RAG and GPT-4 for interactive wildfire information.

# 🔍 Objective

This project aims to:

Detect whether an uploaded image shows signs of wildfire (fire/no_fire).

Allow users to chat and ask questions related to wildfire safety, causes, prevention, etc.

It combines Computer Vision and Natural Language Processing to assist in wildfire detection and public education.

📂 Dataset

# 🔥 Image Classification

Source: Kaggle wildfire dataset

Samples: ~1900 images (balanced classes: fire and no_fire)

Format: RGB images of varying sizes

📄 RAG Document Corpus

Sources: FEMA, UNICEF, and other public wildfire safety documents

Processing:

Split into 200-word chunks

Embedded using OpenAI

Stored in vector FAISS DB

Retrieved using cosine similarity

You will find full list of documents with their original links below.

# 🧠 Methodology

1. 🔬 Image Classification

Baseline Model: Custom CNN (ReLU, MaxPooling, Dropout)

Advanced Model: EfficientNetB0 (transfer learning from ImageNet)

Evaluation: Accuracy, Precision, Recall, F1-Score, Confusion Matrix

Tools: PyTorch, torchvision, OpenCV

2. 🖥 Web Interface

Framework: Streamlit

Features:

Upload an image → Get fire/no_fire prediction

Textbox → Ask questions and get AI-generated answers

3. 🧾 Conversational Agent (RAG + GPT-4)

Retrieval-Augmented Generation using LangChain

Use cases:

Wildfire prevention tips

Climate and fire correlation

Document-based factual Q&A

# 🚀 Installation

To run this project locally:

🔹 1. Clone the repository

git clone https://github.com/ukhalilov/wildfire-detector.git

cd wildfire-detector

🔹 2. Install dependencies

Make sure you have Python 3.8+ installed. Then install required packages:

pip install streamlit torch torchvision Pillow python-dotenv langchain langchain-community langchain-openai faiss-cpu typing-extensions

🔹 3. Add Your own OPENAI API KEY

You need to create .env in the same directory and write your own OPENAI API KEY in the following way: OPENAI_API_KEY=replace_this_with_your_key

🔹 3. Run the application

Start the app using:

streamlit run wildfire_detector.py

🧪 How to Use the App

Once the app is running, here’s how to interact with it:

🔥 Left Side – Wildfire Detection

Upload an Image On the left panel, click on "Browse Files" or Drag and drop files and upload a photo (formats supported: JPG, JPEG, PNG, BMP, TIFF, TIF). The maximum filesize of each image is 200MB.

Preview Your Image

After uploading, the image will appear below the upload button.

Click "Analyze for Wildfire"

Press the "🔍 Analyze for Wildfire" button under the image.

If fire is detected: You’ll see “🔥 Fire Detected!”

If not: You’ll see “✅ No Fire Detected.”

A confidence score will also be shown.

<img width="545" height="659" alt="image" src="https://github.com/user-attachments/assets/e8ac919a-699b-48c2-88c6-2427f13d2173" />



<img width="550" height="853" alt="image" src="https://github.com/user-attachments/assets/2590aedd-b934-4f9d-879d-cede4a56f386" />



# 👥 Authors

Dilrabo Khidirova

Abdumutalib Begmuratov

Ulugbek Khalilov
