# Interest_Based_Content_Recommendation
Hybrid recommender using embeddings + features to predict engagement.


## Description:
This project recommend posts acording to person's preferences, using a Multilayer Perceptron to recommend top 3 posts.


## Table of Contents
- [Components](#components)
- [Procedure](#procedure)
- [Security](#security)
- [Results](#results)
- [Conclusions](#conclusions)

## Components 
The project uses different models and libraries to work properly:
  - **Whisper**: Used to get the text from the user's audio.
  - **Llama 3.2 Instruct**: Used to translate the text and detect the original language.
  - **gTTS**: Used to generate audio from the translated text. By default, it uses an English accent.
  - **Gradio**: Used to build the user interface. It works on both web and mobile.
 
## Procedure

### 1. Voice Input. 
- The user can upload an audio file or record using a microphone.
- The audio is saved in `.wav` format and sent to the processing modules.

### 2. Text Extraction.
- The audio is processed using Whisper, which returns the spoken text with high accuracy.
- The extracted text is sent to the next modules for translation and voice generation.

### 3. Translation and Language Detection.
- The text is sent to the Llama 3.2 Instruct model with a specific role and instruction.
- The model returns the translated text and also detects the original language.
- Both tasks use the Hugging Face API.

### 4. Voice Generation 
- The translated text is sent to the module that converts it into audio using gTTS.

## Security
- User information is never stored at any point, all data is deleted after the process.
- The data sent to the Llama model via API is not saved by the model and is automatically deleted after a few minutes.
- No personal data is required, collected, stored, or shared during the use of this app.

## Results
- A functional prototype was successfully created.
- Generative AI models were used for the main tasks.
- A user interface was built to show how the system works.

## Conclusions
- The app runs on CPU, which limits performance. Using GPU would give better results.
- The app takes time at the beginning because Whisper processes the audio locally, without an API.
- If an API was used for transcription, the process would be faster and the output quality would improve.
- In the part where text is converted to audio, a generative AI model was not used because it took too long to produce the output. That’s why other methods were chosen instead.
- I am aware that some models offer better performance for medical terminology, but for this demo, I prioritized functionality using tools I already knew and had experience with.
