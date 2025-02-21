# AI Language Tutor using a Jetson Orin Nano Super

## Table of Contents 
- [Problem Statement](#problem-statement)
- [Solution](#solution)
- [Approach](#approach)
- [Features](#features)
- [Software Stack](#software-stack)
- [Hardware Requirements](#hardware-requirements)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

## Problem Statement

Learning a new language can be challenging, especially when the main methods of practice involve reading or typing on a device. Without real-time feedback of pronunciation, it’s easy to simply memorize phrases or go through the motions without truly knowing if incorrect habits are being developed. This approach can be discouraging when they attempt to use what they have learned in real-world conversations, only to have their mistakes pointed out by others.

## Solution

Our project aims to create a simple yet interactive approach to language learning. Imagine a system where users can practice speaking a new language using a device and receive immediate feedback. This device will automatically update their progress in a web application, enabling them to track development and share achievements with others. By focusing on speaking rather than passive learning, users can benefit from an effective and engaging approach to language learning

## Approach

The development of this project will leverage software optimized for Jetson Orin Nano, pre-trained language models that may be fine-tuned, and frontend and backend components from a previous project. The system consists of several key components that interact to create an engaging AI language-learning tutor.

### Jetson Orin Nano Super

The Jetson Orin Nano Super paired with I/O devices such as a microphone and speaker, will serve as the interface for user interaction. It will process voice input and generate speech output using pretrained models and generative AI.

### Full-Stack Web Application

The full-stack web application will serve as an interactive platform, enabling users to track their progress using Google Charts JS for dynamic data visualization. Users will be able to create accounts by using general information (e.g., name, email, password), and select a language to learn.

Additionally, users can share their progress through a timeline feature, where they can create posts, interact with others via comments and likes. The language courses will be stored in a database and made accessible through API endpoints in JSON format.

Additional features, such as language practice through typing exercises and quizzes on the platform, are in consideration and will be implemented if time permits.

### API Communication Between Jetson Orin Nano Super and Web Application

The Jetson Orin Nano Super will interact with the web application through API calls. Using a course/section identification number, it will retrieve the requested content for the section the user is currently on. This interaction will be facilitated through voice commands, which will be processed to call the appropriate function.

### Backend Data Retrieval and Storage

When an API call for a course is received, the backend will utilize CRUD operations to query a local database and retrieve the requested data. The retrieved content will then be formatted as JSON and sent to the Jetson Orin Nano Super, which will process the data for speech output to the user.

### Speech Processing with NVIDIA Riva

The system will leverage NVIDIA’s Riva software for speech-to-text (STT) and text-to-speech (TTS) processing. Additionally, we will use Riva’s pre-trained models for speech recognition. If time permits, these models will be fine-tuned
using NVIDIA’s TAO Toolkik (Train, Adapt, Optimize) to enhance speech recognition for users with heavier accents. This would be specific to one language, as time would not permit to train for multiple languages.

### Generative AI for Error Feedback

After the speech-to-text process is completed, the generated string will be compared to the expected string from the course. If a mistake is detected, generative AI will provide feedback by identifying mispronounced words and offer corrective guidance. A prompt will be generated using the mispronounced word(s), instructing the AI to assist with pronunciation while also providing definitions and examples sentences demonstrating their usage in different contexts. The lesson will continue only after the correct input is detected. The exact implementation of generative AI integration is still under consideration and will require further research as the project progresses.

## Features

## Software Stack

## Hardware Requirements

## Installation

## Usage

## API Endpoints

## Contributing
1. Fork the repository
2. Clone your forked repository to your local machine:
   ```bash
      git clone https://github.com/your-username/AI-Language-Tutor.git
   ```
   - Replace **your-username** with GitHub username
3. Navigate into the project directory:
   ```bash
      cd AI-Language-Tutor
   ```
4. Sync your forked repository with the main repository:
   ```bsh
      git remote add upstream https://github.com/bryan-melo/AI-Language-Tutor.git
   ```
5. Create a new branch for your changes:
   ```bash
     git checkout -b branch-name
   ```
6. Commit your changes:
   ```bash
     git commit -m "Message describing changes"
   ```
7. Push changes to your branch:
   ```bash
     git push origin branch-name 
   ```
8. Open a Pull Request (PR)
