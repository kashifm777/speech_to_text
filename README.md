## Speech-to-Text Django App with AssemblyAI

This repository provides a user-friendly Django application for converting audio files into text transcripts. It integrates with AssemblyAI, a powerful speech recognition API, to deliver accurate results.

**Features:**

- **Simple File Upload:** Users can easily upload their audio files using a web form.
- **AssemblyAI Integration:** Leverages AssemblyAI's API for efficient and reliable speech-to-text transcription.
- **Clear Transcript Display:** The transcribed text is displayed prominently on the application's interface.
- **Error Handling:** In case of errors during upload or transcription, informative messages are provided to the user.

**Requirements:**

- Python 3.x
- Django (tested with version 3.x)
- assemblyai library (`pip install assemblyai`)
- A valid AssemblyAI API key (obtainable from your AssemblyAI account)

**Getting Started:**

1. **Clone or download this repository.**
2. **Create a virtual environment:** It's recommended to create a virtual environment to isolate the project's dependencies. You can use tools like `venv` or `virtualenv`.
3. **Install dependencies:** Activate the virtual environment and run `pip install -r requirements.txt` to install the required libraries.
4. **Configure AssemblyAI API Key:** Create a file named `.env` in your project's root directory and add the line `ASSEMBLYAI_API_KEY=<your_api_key>`, replacing `<your_api_key>` with your actual AssemblyAI API key.
5. **Set up your Django project:** If you haven't already, create a Django project and configure it according to the Django documentation.
6. **Add the app:**
    - Copy the `transcription` directory (containing `views.py` and `index.html`) to your project's `apps` directory.
    - Add `'transcription'` to your `INSTALLED_APPS` setting in your Django project's `settings.py` file.
7. **Run migrations:** Execute `python manage.py makemigrations` and then `python manage.py migrate` to apply database migrations (if applicable).
8. **Start the development server:** Run `python manage.py runserver` to launch the Django development server. You can usually access the app at http://127.0.0.1:8000/ by default.

**How it Works:**

1. Visit the application in your web browser.
2. Click "Choose File" and select the audio file you want to transcribe. Ensure the file format is supported by AssemblyAI (check the AssemblyAI documentation for details).
3. Click the "Upload" button.
4. If the upload is successful and transcription completes without errors, the app will display the transcribed text on the page.
5. In case of errors during upload or transcription, an informative message will be displayed.

**Further Enhancements:**

- Implement progress indicators to visually inform users about upload and transcription progress.
- Add support for different audio formats beyond the default supported by AssemblyAI.
- Integrate audio playback functionality, allowing users to verify the audio file before uploading.
- Explore advanced features provided by the AssemblyAI API, such as diarization for identifying different speakers in the audio.

**Disclaimer:**

This application serves as a starting point for speech-to-text functionality using Django and AssemblyAI. You may need to adapt it to your specific needs and data formats. Refer to the AssemblyAI documentation for detailed information on their API and supported features.

This repository provides a convenient way to build and deploy your own speech-to-text application. With customization and further enhancements, you can create a valuable tool for transcribing audio content.