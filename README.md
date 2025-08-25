
# AI Calling - Gemini Phone Agent with Deepgram Transcription

This project implements a voice-based AI phone agent using Google Gemini generative AI and Deepgram speech-to-text APIs. The agent interacts with customers, queries a product inventory database, and converts replies to speech in real-time.

---

## Features

- Real-time speech transcription with Deepgram SDK  
- Conversational AI powered by Google Gemini 2.0 Flash model  
- Text-to-speech synthesis and playback of agent responses  
- SQL database queries to retrieve product inventory information  
- Professional phone agent persona tailored for customer service  

---

## Requirements

- Python 3.8 or higher  
- See `requirements.txt` for the required Python packages  

---

## Installation & Setup

1. Clone this repository:

   ```
   git clone https://github.com/pruthvideepam/ai-calling.git
   cd ai-calling
   ```

2. Install Python dependencies:

   ```
   pip install -r requirements.txt
   ```

3. Create a `.env` file in the root directory with your Google API key:

   ```
   GOOGLE_API_KEY=your_google_api_key_here
   ```

4. Ensure you have an audio input device (microphone) configured on your system.

---

## Usage

Run the main script to start the AI calling agent:

```
python Encode.py
```

The agent will:

- Load the product inventory from `Products.csv` into an in-memory SQLite database  
- Connect to the Deepgram live transcription and speech synthesis services  
- Start listening through the microphone and respond to customer queries in a conversational style  
- Synthesize agent responses to speech and play the audio in real time  

Press `Ctrl+C` to stop the recording and terminate the program.

---

## Git Commands to Push Local Changes to GitHub

If you modify or add files and want to push changes, use the following:

```
git add .
git commit -m "Your commit message"
git push -u origin main
```

(If the error `src refspec main does not match any` occurs, check your branch name with `git branch` and replace `main` with your actual branch like `master`.)

---

## Notes

- You need a valid Google Generative AI API key for the Gemini model access.  
- The script assumes a `Products.csv` file with product inventory in the following format:

  ```
  Product Name,Category,Brand,Price in Rupees,Stock,Description
  Cotton T-Shirt,Clothing,Essentials,299,150,Comfortable cotton t-shirt available in various colors and sizes
  ...
  ```

- The database and conversations are managed in-memory and reset each run.  

---


For questions or contributions, please open an issue or submit a pull request.
