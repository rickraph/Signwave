# Speech-to-Sign-language Translator

**An application which takes in live speech or audio recording as input, converts it into text, and displays the relevant Indian Sign Language (ISL) images or GIFs.**

- Front-end using EasyGUI.
- Speech input through a microphone using PyAudio.
- Speech recognition using Google Speech API and Sphinx (for offline use).
- Text preprocessing using NLP.
- Dictionary-based Machine Translation.

---

## Features

1. **Live Speech Recognition:**
   - Captures speech through a microphone.
   - Recognizes spoken words using Google Speech API (online) and Sphinx (offline).

2. **Indian Sign Language (ISL) Conversion:**
   - Displays ISL GIFs for recognized sentences.
   - Converts each character of unrecognized sentences to ISL alphabet images.

3. **Simple GUI Interface:**
   - Intuitive interface to start live voice capture or exit the program.

4. **Add New Sentences:**
   - Users can add new sentences to the vocabulary along with their corresponding GIFs.

---

## Objective

**This Audio-to-Sign Language converter aims to:**

- Provide information access and services to deaf people in Indian Sign Language (ISL).
- Develop a scalable project that can be extended to capture the entire ISL vocabulary through manual and non-manual signs.

This project bridges the communication gap between hearing-impaired individuals and others by translating live speech into ISL, enabling effective communication.

---

## Prerequisites

Ensure you have the following installed:

- Python 3.x
- Required Python Libraries:
  ```bash
  pip install speechrecognition easygui numpy matplotlib pillow opencv-python
  ```
- Microphone for live voice input.
- A folder structure for assets:
  ```
  ISL_Gifs/      # Folder containing GIFs for predefined sentences.
  letters/       # Folder containing images for each alphabet (e.g., a.jpg, b.jpg, ...).
  sentences.txt  # Text file containing predefined sentences (one per line).
  signlang.png   # Image used for the GUI interface.
  ```

---

## Folder Structure

```
.
├── main.py            # The main Python script.
├── ISL_Gifs/          # Folder containing GIFs for predefined sentences.
├── letters/           # Folder containing alphabet images (a.jpg, b.jpg, ...).
├── sentences.txt      # Text file containing predefined sentences.
├── signlang.png       # Image for the GUI interface.
```

---

## How to Run

1. Open the terminal in the project directory.
2. Run the main Python script:
   ```bash
   python main.py
   ```
3. The application interface appears on the screen.
4. Hit the **Record** button to start capturing speech input.
5. The speech is processed, and the respective ISL outputs are displayed.
6. To exit the application using speech, say **goodbye**.

---

## Algorithm

**Audio-to-Sign Language Translator Workflow:**

1. **Start.**
2. **Capture Speech:**
   - Calibrate the energy threshold for ambient noise levels.
   - Listen to speech using a microphone.
3. **Recognize Speech:**
   - Convert speech to text.
   - Preprocess text by converting it to lowercase.
4. **Process Text:**
   - If the detected text is "goodbye," exit the program.
   - If the detected text matches a predefined sentence in the dictionary, display the corresponding GIF.
   - If the text is not in the dictionary, display the ISL alphabets for each character of the text.
5. **Repeat:** Continue the process until the user ends the speech or exits the program.
6. **Handle Errors:** If no speech is detected, display an error message: "Could not listen."

---

## Adding New Sentences

To expand the vocabulary:

1. Choose the option **Add new sentence** when prompted in the program.
2. Enter the new sentence and the corresponding GIF filename (without the `.gif` extension).
3. Place the corresponding GIF in the `ISL_Gifs/` folder.

The new sentence will now be recognized and displayed when spoken.

---

## Acknowledgments

- **Google Speech API and Sphinx:** For speech-to-text conversion.
- **Matplotlib & OpenCV:** For displaying images and GIFs.
- **EasyGUI:** For creating a simple GUI interface.

---

## Contributing

Contributions are welcome! If you have suggestions for improving the project or adding new features, feel free to open an issue or submit a pull request.

---
