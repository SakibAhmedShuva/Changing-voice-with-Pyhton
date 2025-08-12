# 🐍 Python Voice Changer

A versatile Python script to modify audio files with a range of high-quality effects like pitch shifting, time stretching, reverb, and formant filtering. This tool is designed for batch processing, allowing you to convert an entire folder of audio files with a single command.

![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg) ![Python Version](https://img.shields.io/badge/python-3.7+-brightgreen.svg)

---

## 🌟 Key Features

* **Pitch Shifting**: Make voices higher or lower without changing the speed.
* **Time Stretching**: Change the speed of the audio without affecting the pitch.
* **Formant Filtering**: A high-pass filter to make voices sound "smaller" or more cartoonish.
* **Reverb**: Add a sense of space and environment to the audio.
* **Chorus**: Create a thicker, richer sound with a subtle doubling effect.
* **Batch Processing**: Automatically processes all supported audio files (`.wav`, `.mp3`, `.flac`, etc.) in a specified folder.

---

## ⚙️ Setup and Installation

Follow these steps to get the project running on your local machine.

### 1. Prerequisites

* **Python 3.7+**
* **pip** (Python package installer)

### 2. Clone the Repository

Clone this repository to your local machine using Git:
```bash
git clone [https://github.com/SakibAhmedShuva/Changing-voice-with-Pyhton.git](https://github.com/SakibAhmedShuva/Changing-voice-with-Pyhton.git)
cd Changing-voice-with-Pyhton
```

### 3. Set Up a Virtual Environment (Recommended)

It's best practice to create a virtual environment to manage project dependencies.

* **On macOS / Linux:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```
* **On Windows:**
    ```bash
    python -m venv venv
    .\venv\Scripts\activate
    ```

### 4. Install Dependencies

Install all the required Python libraries using the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

---

## 🚀 How to Use

Using the script is straightforward. Just configure your folders and parameters, then run it.

### Step 1: Prepare Your Audio Files

Create a folder structure as shown below. Place all your source audio files into the `Original` directory.

```
Your-Project-Folder/
├── Audio/
│   ├── Original/
│   │   └── your_audio_1.wav  <-- Place your source files here
│   │   └── another_sound.mp3
│   └── converted_audio/
│       └── (Output files will appear here)
├── voice_changer_script.py  <-- The main script
└── requirements.txt
```
*Note: The script will automatically create the `converted_audio` folder if it doesn't exist.*

### Step 2: Configure the Parameters

Open the Python script (`voice_changer_script.py` or similar) and edit the parameters section to customize your desired voice effect.

```python
# ===-===-===-===-===-===-===-===-===-===-===-===-===-===
# --- 1. EDIT YOUR PARAMETERS HERE ---
#
# PITCH: Higher value means a higher pitch (e.g., 2.0 is one octave higher).
PITCH = 1.25
#
# SPEED: Higher value means faster audio (1.0 is original speed).
SPEED = 1.0
#
# FORMANT: Removes low frequencies to sound "smaller". Good values are 0.1 to 0.8.
#          Set to 0 to disable.
FORMANT_SHIFT = 0.8
#
# REVERB: Adds a sense of space. Good values are 0.1 to 0.3.
#         Set to 0 to disable.
REVERB_WET_LEVEL = 0.1
#
# CHORUS: Adds a subtle doubling effect. Good values are 0.2 to 0.5.
#         Set to 0 to disable.
CHORUS_MIX = 0.05
#
# ===-===-===-===-===-===-===-===-===-===-===-===-===-===
# --- 2. DEFINE YOUR FOLDERS HERE ---

# Define the path to the folder containing your original audio files
input_folder = r".\Audio\Original"

# Define the path for the output folder where converted files will be saved
output_folder = r".\Audio\converted_audio"
```

### Step 3: Run the Script

Execute the script from your terminal. It will find all audio files in the `input_folder`, process them with your chosen effects, and save them to the `output_folder`.

```bash
python voice_changer_script.py
```

You'll see progress messages in the console, and your converted files will be ready in the output folder once the script finishes.

---

## 🔧 Understanding the Parameters

* **`PITCH` (float)**: A multiplier for the frequency. `1.0` is the original pitch. `2.0` is one octave higher, and `0.5` is one octave lower.
* **`SPEED` (float)**: A multiplier for the playback speed. `1.0` is the original speed. `1.5` is 50% faster, and `0.75` is 25% slower.
* **`FORMANT_SHIFT` (float)**: This controls a high-pass filter, measured in kHz. By cutting off low frequencies, it can simulate a smaller vocal tract, making a voice sound "smaller" or higher-pitched in a different way than the main pitch shifter. A value of `0.8` (800 Hz) is a good starting point for a "kid" or "chipmunk" effect. Set to `0` to disable.
* **`REVERB_WET_LEVEL` (float)**: The amount of reverberation (echo) to add. This is a "wet/dry" mix, where `0.0` is no reverb and `1.0` is only the reverb signal. A small value like `0.1` or `0.2` adds a nice sense of space.
* **`CHORUS_MIX` (float)**: Controls the mix of the chorus effect, which creates a shimmering, doubling sound. `0.0` means no chorus, while `0.5` is an equal mix of original and chorus signals.

---

## 🛠️ Libraries Used

This project relies on several fantastic open-source libraries:

* [**Pedalboard**](https://github.com/spotify/pedalboard): For high-quality, real-time audio effects like pitch shifting, reverb, and chorus.
* [**audiotsm**](https://github.com/Muges/audiotsm): For high-quality time-stretching without altering the pitch, using the WSOLA algorithm.
* [**SoundFile**](https://github.com/bastibe/python-soundfile): For reading and writing virtually any audio format.
* [**NumPy**](https://numpy.org/): For efficient numerical operations on audio arrays.

---

## 📜 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.