# 🐍 Voice Changer with Python

<div align="center">

**A Jupyter Notebook for high-quality voice modulation, batch audio processing, and file analysis.**

![GitHub repo size](https://img.shields.io/github/repo-size/SakibAhmedShuva/Changing-voice-with-Pyhton?style=for-the-badge)
![GitHub issues](https://img.shields.io/github/issues/SakibAhmedShuva/Changing-voice-with-Pyhton?style=for-the-badge)
![GitHub License](https://img.shields.io/github/license/SakibAhmedShuva/Changing-voice-with-Pyhton?style=for-the-badge)

</div>

This project provides a complete, easy-to-use Jupyter Notebook (`voice_changer.ipynb`) that allows you to apply a chain of audio effects to change voices in your audio files. It's built for both single-file testing and batch processing of entire folders. Additionally, it includes a powerful analysis tool to generate statistics and visualizations for your audio library.

---

## ✨ Key Features

* **High-Quality Effects**: Apply pitch shifting, time stretching, reverb, chorus, and formant filtering.
* **Batch Processing**: Convert an entire folder of audio files (`.wav`, `.mp3`, etc.) in one run.
* **Audio Analysis**: Automatically calculate and visualize statistics for your audio files, including duration, file size, and distribution, using `pandas` and `matplotlib`.
* **Interactive Environment**: Uses `IPython.display` to play back original and modified audio directly within the notebook.
* **All-in-One Notebook**: From installation to processing and analysis, everything is managed within a single `.ipynb` file.

---

## 🚀 Getting Started

Follow these steps to get the project running on your local machine.

### Prerequisites

* Python 3.7+
* A tool to run Jupyter Notebooks (like JupyterLab, VS Code, or Google Colab).

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/SakibAhmedShuva/Changing-voice-with-Pyhton.git](https://github.com/SakibAhmedShuva/Changing-voice-with-Pyhton.git)
    cd Changing-voice-with-Pyhton
    ```
2.  **Open the Notebook:**
    Launch Jupyter and open the `voice_changer.ipynb` file.

3.  **Install Dependencies:**
    The first code cell in the notebook handles all installations for you. Simply run it to install all required libraries.
    ```python
    # This is the first cell in the notebook
    !pip install numpy soundfile pedalboard audiotsm ipython librosa pandas matplotlib seaborn
    ```

---

## ⚙️ How to Use

The notebook is divided into sections. Run the cells in order.

### 1. File & Folder Setup

Before you begin, place your source audio files in the `Audio/Original` directory. The notebook will automatically create this folder if it doesn't exist. The output will be saved to `Audio/converted_audio`.

```
Your-Project-Folder/
├── Audio/
│   ├── Original/
│   │   └── your_audio_file.wav  <-- Place source files here
│   └── converted_audio/
│       └── (Output files appear here)
└── voice_changer.ipynb
```

### 2. Batch Voice Changing

* Navigate to the **`# Batch`** section in the notebook.
* **Configure your parameters** (like `PITCH`, `SPEED`, `REVERB_WET_LEVEL`, etc.) inside the code cell to customize the effect.
* **Run the cell**. The script will process all audio files from the `Audio/Original` folder and save the results in `Audio/converted_audio`.

### 3. Audio Analysis

* Navigate to the **`# Analysis`** section.
* This part of the notebook will analyze the files in the `Audio/converted_audio` folder.
* **Run the cell** to generate a full statistical report and visualizations of your modified audio files.

---

## 🛠️ Tech Stack

* **Core Processing**: `pedalboard`, `audiotsm`, `soundfile`
* **Data Handling & Analysis**: `numpy`, `pandas`, `librosa`
* **Visualization**: `matplotlib`, `seaborn`
* **Environment**: Jupyter Notebook

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---
<p align="center">
  Made by Sakib Ahmed Shuva
</p>