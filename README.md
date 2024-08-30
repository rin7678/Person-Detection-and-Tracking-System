
# Person Detection and Tracking System

This project is designed to detect and track people (specifically children and therapists) in videos. It assigns a unique ID to each person, tracks them as they move, and keeps track of them even if they leave and re-enter the frame. The final result is a video showing each person with their unique ID.

## Table of Contents
- [Installation](#installation)
- [How to Use](#how-to-use)
- [Files in the Project](#files-in-the-project)
- [How It Works](#how-it-works)
- [Features](#features)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Installation

### What You Need
- Python 3.x installed on your computer
- pip (a tool to install Python packages)

### Installing the Required Packages
To install everything you need, run this command:

```bash
pip install -r requirements.txt
```

Or you can install the packages one by one:

```bash
pip install deep-sort-realtime ultralytics opencv-python torch torchvision torchaudio filterpy
```

## How to Use

1. **Download the project:**
    ```bash
    git clone <your-repository-link>
    cd <your-repository-name>
    ```

2. **Run the code:**
    Open the Jupyter Notebook file `Right_code.ipynb` and run the code cells in order. The code will:
    - Use a pre-trained model to detect people in the video.
    - Track the people throughout the video.
    - Save the video with each person labeled by a unique ID.

3. **Input Video:**
    - Place the video you want to process in the same folder as the notebook, or update the video path in the notebook.

4. **Output Video:**
    - The processed video will be saved as `output.avi` in the current folder.

## Files in the Project

```bash
.
├── Right_code.ipynb        # The main code in a Jupyter Notebook
├── requirements.txt        # List of Python packages you need
└── README.md               # This file
```

## How It Works

This project uses a model called YOLO (You Only Look Once) to detect people in the video. Then it uses another tool called Deep SORT (Simple Online and Realtime Tracking) to keep track of each person as they move, even if they disappear from the frame and come back later.

### Kalman Filter:
A Kalman Filter is used to predict and update the positions of people in the video. It helps in keeping the tracking smooth, even when people are partially hidden.

## Features

- **Person Detection:** Detects children and therapists in the video.
- **Unique ID:** Assigns a unique ID to each person and tracks them.
- **Re-Entry Tracking:** Tracks people even if they leave and come back into the frame.
- **Post-Occlusion Tracking:** Continues tracking people even if they get partially hidden.

## Results

The final result is a video (`output.avi`) that shows each person with their unique ID.

## Contributing

If you want to help improve this project, you can fork the repository and make your changes. Pull requests are welcome!

## License

This project is under the MIT License. You can find more details in the [LICENSE](LICENSE) file.
