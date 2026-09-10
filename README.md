# 📘 OCR Dictionary App

### Intelligent Image-to-Text Dictionary with Translation & Pronunciation

An AI-powered web application that extracts text from images using **Optical Character Recognition (OCR)**, provides **language translation**, and generates **pronunciation audio** to help users understand unfamiliar words and phrases.

The application combines a **FastAPI backend** with a lightweight **HTML, CSS, and JavaScript frontend** to provide a simple and interactive learning experience.

---

## 🌟 Overview

The **OCR Dictionary App** allows users to upload an image containing text and automatically:

1. 📷 Extract text from the image using OCR
2. 🔍 Identify the detected words or text
3. 🌍 Translate the extracted text into another language
4. 🔊 Generate pronunciation audio
5. 🖥️ Display the results through a simple web interface

It is designed to be useful for **language learners, students, travelers, and users who want to quickly understand text found in images**.

---

## ✨ Features

* 📷 **Image Upload**
  Upload images containing words, sentences, signs, documents, or other readable text.

* 🔍 **Optical Character Recognition**
  Uses **Tesseract OCR** to extract text from uploaded images.

* 🌍 **Text Translation**
  Translate the extracted text into a supported target language.

* 🔊 **Pronunciation Support**
  Generate audio pronunciation for translated or detected text.

* ⚡ **FastAPI REST API**
  Provides a lightweight and efficient backend for processing requests.

* 🖥️ **Interactive Web Interface**
  Simple frontend built using HTML, CSS, and JavaScript.

* 🔐 **CORS Support**
  Enables secure communication between the frontend and backend during development and deployment.

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │       User          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Web Frontend      │
                    │   HTML/CSS/JS        │
                    └──────────┬──────────┘
                               │
                         Image Upload
                               │
                               ▼
                    ┌─────────────────────┐
                    │   FastAPI Backend   │
                    └──────────┬──────────┘
                               │
                ┌──────────────┼──────────────┐
                │              │              │
                ▼              ▼              ▼
        ┌────────────┐  ┌────────────┐  ┌────────────┐
        │ Tesseract │  │ Translation│  │Pronunciation│
        │    OCR     │  │   Service  │  │   Service   │
        └─────┬──────┘  └─────┬──────┘  └──────┬─────┘
              │               │                │
              └───────────────┼────────────────┘
                              ▼
                    ┌─────────────────────┐
                    │  Processed Result   │
                    │ Text + Translation  │
                    │ + Pronunciation     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │       User          │
                    └─────────────────────┘
```

---

## 🛠️ Tech Stack

### Backend

* **Python**
* **FastAPI**
* **Tesseract OCR**
* OCR/image processing libraries
* REST API
* CORS middleware

### Frontend

* **HTML5**
* **CSS3**
* **JavaScript**

### Core Technologies

| Technology    | Purpose                     |
| ------------- | --------------------------- |
| Python        | Backend development         |
| FastAPI       | REST API and server         |
| Tesseract OCR | Text extraction from images |
| JavaScript    | Frontend interaction        |
| HTML          | Web page structure          |
| CSS           | User interface styling      |

---

## 📂 Project Structure

```text
OCR-Dictionary-App/
│
├── backend/
│   ├── ...
│   └── ...
│
├── frontend/
│   ├── ...
│   └── ...
│
├── .gitignore
│
└── README.md
```

> The `backend` directory contains the FastAPI application and OCR-related processing, while the `frontend` directory contains the web interface.

---

## 🔄 Application Workflow

### Step 1 — Upload Image

The user selects an image containing the text they want to understand.

### Step 2 — OCR Processing

The image is sent to the backend, where **Tesseract OCR** detects and extracts the text.

### Step 3 — Text Processing

The extracted text is cleaned and prepared for further processing.

### Step 4 — Translation

The detected text can be translated into the user's preferred language.

### Step 5 — Pronunciation

The application generates pronunciation audio to help the user learn how the translated text is spoken.

### Step 6 — Display Results

The frontend displays the extracted text, translation, and pronunciation options to the user.

---

## 🚀 Getting Started

### Prerequisites

Make sure the following are installed:

* Python 3.9+
* Tesseract OCR
* Git

---

### 1. Clone the Repository

```bash
git clone https://github.com/Shalini-d-13/OCR-Dictionary-App.git
cd OCR-Dictionary-App
```

---

### 2. Set Up the Backend

Navigate to the backend directory:

```bash
cd backend
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment.

**Windows:**

```bash
venv\Scripts\activate
```

**Linux / macOS:**

```bash
source venv/bin/activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

### 3. Install Tesseract OCR

Tesseract must be installed separately because it is an external OCR engine.

After installation, make sure the Tesseract executable is available to the backend configuration.

---

### 4. Start the Backend

From the backend directory, run:

```bash
uvicorn main:app --reload
```

The API will normally be available at:

```text
http://127.0.0.1:8000
```

FastAPI also provides interactive API documentation at:

```text
http://127.0.0.1:8000/docs
```

---

### 5. Run the Frontend

Open the frontend files in a browser or serve the frontend using a local development server.

Make sure the frontend API configuration points to the running FastAPI backend.

---

## 🧪 Example Use Case

Imagine a user sees an unfamiliar word on a sign or in a book.

```text
              Image
                │
                ▼
          ┌───────────┐
          │    OCR    │
          └─────┬─────┘
                │
                ▼
         Extracted Text
                │
                ▼
          Translation
                │
                ▼
         Pronunciation
                │
                ▼
       Learning Result
```

The user can therefore understand the **written text, translated meaning, and pronunciation** without manually typing the word.

---

## 🎯 Applications

The project can be useful for:

* 📚 Language learning
* 🎓 Student learning assistance
* 🌍 Travel and tourism
* 📖 Reading foreign-language material
* 🪧 Understanding text from signs
* 📝 Quick text extraction from images
* 🔊 Pronunciation practice

---

## 🔮 Future Enhancements

Possible improvements include:

* 📱 Mobile application support
* 🌐 Support for more languages
* 🧠 Improved OCR accuracy for complex images
* ✍️ Handwritten text recognition
* 📄 PDF/document OCR
* 🔊 Multiple pronunciation accents
* 📜 Translation history
* ⭐ Save frequently used words
* 📊 Vocabulary learning and progress tracking
* 🎙️ Speech-based word lookup
* 📴 Offline OCR support

---

## 🔒 Security & Performance Considerations

* CORS is configured to allow frontend-backend communication.
* Uploaded images should be validated before processing.
* File-size and file-type restrictions can be added for production deployment.
* Temporary uploaded files should be securely handled and removed after processing.
* API authentication can be introduced for production use.

---

## 📸 Screenshots

Add screenshots of the application here to make the repository more attractive.

```text
### Home Page

[ Add screenshot here ]

### OCR Result

[ Add screenshot here ]

### Translation & Pronunciation

[ Add screenshot here ]
```

---

## 📌 Project Highlights

* ✅ Image-to-text conversion using OCR
* ✅ RESTful backend using FastAPI
* ✅ Translation functionality
* ✅ Pronunciation generation
* ✅ Lightweight web interface
* ✅ Modular frontend and backend architecture
* ✅ Useful for language learning and accessibility

---

## 👩‍💻 Author

**Shalini D**

GitHub: [Shalini-d-13](https://github.com/Shalini-d-13)

---

## 📄 License

This project is intended for educational and development purposes.

If a specific open-source license is added to the repository, this section should be updated accordingly.
