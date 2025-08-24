# Biogin X - Facial Recognition Authentication System

## Work Team

- **Scrum Master**: Juan Manuel Cabrera
- **Development Leader**: Mariano Chun
- **Developers**: Mariano Chun, Francisco Barrientos, Matías Daniel Nissero, Fernando Iván Antúnez
- **Tester**: Agustina Camila Hirschfeld
- **Functional Analysts**: Adrián Gustavo Verón

## Mission

Provide reliable, secure, and high-quality products, ensuring that the user feels comfortable and confident when using the Biogin X authentication system.

## Scope

The project includes:

- User registration using facial recognition.
- Authentication process through facial image comparison.
- Intuitive user interface.
- Security and privacy of biometric data.
- Tolerance to variations in lighting conditions, viewing angles, and facial expressions.
- Access logging and update capability.

## Introduction
Biogin X is a simple and secure mobile application designed to quickly authenticate users through facial recognition. This system is implemented to improve security and efficiency in accessing facilities such as universities.

## Main Screen

### 1. Log in with facial recognition (Security)
This option is intended for security personnel in charge of authenticating students, faculty, and other users entering the university. Authentication is carried out through facial recognition and requires the person to be previously registered in the database.

### 2. Log in with facial recognition (HR)
This module is intended for human resources staff, who have the ability to register new users in the database. For registration, the user’s corresponding data, their role (student, faculty, etc.), and three photos are entered. Subsequently, a facial encoding is generated through the face detection API.

### 3. Log in with DNI
This option is used when there is no Internet connection. First, the security officer’s DNI is scanned, then users previously registered can be validated using a local database with authorized DNIs.

### 4. Log in with facial recognition (Managerial)
This module allows users with a managerial role to configure an email address to receive reports and set the days on which the algorithm will be trained with photos of new people.

### 5. Log in with facial recognition (Admin)
This view allows switching the main database in case it is not available. The main options are Firebase and Back4apps.

## API Functionality

The facial recognition API is developed in Python using Adam Geitgey’s ‘face_recognition’ library. It allows training the model and performing facial recognition through the camera.

- **Model Training**: Receives a training request with three images of the new person. It uses the HOG (Histogram of Oriented Gradients) method to process the images and generate a facial feature vector.
- **Facial Recognition**: At the time of authentication, the API receives a POST recognition request and returns the DNI associated with the face or an “unknown” message if the person is not registered.

The API is hosted on the PythonAnywhere website.

## Database

Biogin X uses Firebase for cloud database management, which allows better organization and the ability to execute server-side functions.

## Project Objectives

- **Efficiency**: Optimize battery, memory, and processor usage.
- **Usability**: Provide an easy-to-use interface for users with different levels of experience.
- **Security**: Comply with biometric data privacy regulations.
- **Performance**: Ensure acceptable response times in the facial authentication process.
