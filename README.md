# Image Inquiry Simulation for PET/FIRST Test Exam

![Introduction](https://github.com/user-attachments/assets/eedf427f-d59d-4bcb-a7e3-24beada35dfe)


## Overview
This project is designed to simulate an oral section for a PET/FIRST exam using a chatbot. The chatbot guides users in describing a color photograph, helping them practice their skills for the exam. The project integrates object detection, image captioning, and grammatical correction tools to provide a realistic and engaging practice environment.

### Key Features:
- **Image Selection and Processing**: Upload images from the user's device or from a URL.
- **Object Detection**: Detects objects in the image using the YOLOv8 model.
- **Image Captioning**: Describes the contents of the image using the ViT-GPT2 model.
- **Grammatical Feedback**: Identifies and corrects grammatical errors in user responses using Gramformer.
- **Conversational Flow**: Provides questions and feedback, simulating the PET/FIRST oral exam.

---

## Components

### 1. **Object Detection**: 
Uses YOLOv8 for object detection to identify objects in the uploaded image. This allows the chatbot to generate questions related to the objects found in the image.

### 2. **Image Captioning**: 
Generates captions for the image using the ViT-GPT2 model, a combination of Vision Transformers and GPT-2, trained on the COCO dataset. This helps provide a description of the image to guide the conversation.

### 3. **Grammar Check**: 
Uses the Gramformer library to detect and correct grammatical mistakes in the user’s responses. This feedback helps improve language accuracy.

### 4. **POS Tagging and Tokenization**: 
Breaks down user responses into parts of speech for more accurate evaluation of grammar and syntax.

---

## Models Used

**Download pre-trained models:**
   - [YOLOv8 model](https://ultralytics.com/)
   - [ViT-GPT2 model](https://huggingface.co/)
   - [Gramformer library](https://github.com/PrithivirajDamodaran/Gramformer)

---

## Conversation Flow

### 1. Image Loading and Processing:
The chatbot loads and processes the image to detect objects and generate a caption.

**Image display**: A preview of the image is shown to the user.

![Image Preview](https://github.com/user-attachments/assets/1dc5c1c0-a0b7-4eb6-b5e3-ad3669c13d14) 

### 2. User Interaction:
The chatbot asks questions about the objects detected in the image.

Based on the user's responses, the chatbot provides feedback, including any grammatical corrections if necessary.

**Example conversation:**
![Example Corrections](https://github.com/user-attachments/assets/b4fc3f89-482c-43d1-9a4e-513692d51044)


The chatbot also asks for a description of the image.

**Example final question:**
![Final Question](https://github.com/user-attachments/assets/659c9ad1-b7e5-46de-8444-72883883f2bb)


---

## Evaluation

The chatbot evaluates user responses based on:

- **Correctness**: How accurate the answer is.
- **Length**: Longer answers (more than 5 words) earn more points.
- **Grammar**: Points are deducted for grammatical errors.
- **Final Score**: The chatbot calculates a final score based on the user's responses and provides feedback.

---

## Acknowledgments

- **YOLOv8**: Ultralytics for the object detection model.
- **ViT-GPT2**: Vision Transformers and GPT-2 for image captioning.
- **Gramformer**: Library for grammar correction.
- **NLTK**: Natural Language Toolkit for POS tagging and tokenization.



