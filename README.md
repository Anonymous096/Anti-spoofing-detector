# Spoofing Detection Project

This project implements a spoofing detection system using computer vision and deep learning techniques. It utilizes YOLOv8 for object detection and MediaPipe for facial feature extraction.

## Project Structure

```
.
├── dataset/           # Directory containing the dataset
        └── all
        └── DataCollect
        └── Fake
        └── Real
        └── Split data # It will be created after running split_dta.py
├── model/            # Directory for storing trained models
├── runs/             # Directory for storing training runs and results
├── data_collect.py   # Script for collecting and processing data
├── main.py          # Main application script
├── split_data.py    # Script for splitting dataset into train/val/test
├── train.py         # Script for training the model
└── requirements.txt # Project dependencies
```

## Requirements

- Python 3.x
- ultralytics (YOLOv8)
- mediapipe
- opencv-python

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd spoofing
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

## Usage

### Data Collection

Run the data collection script to gather and process data:

```bash
python data_collect.py
```

NOTE: In data_collect.py it will capture real or fake images on the basis of ID and 0 is for fake and 1 is for real, while collecting the data change it accordingly and after collecting real cut all the images and paste it in dataset/real folder and do the same for fake, DataCollect should be empty it should only collect while running the script. Take same number of images from both real and fake and put it in dataset/all folder to split it and train it

### Data Splitting

Split the dataset into training, validation, and test sets:

```bash
python split_data.py
```

### Training

Train the model using the prepared dataset:

```bash
python train.py
```

### Running the Application

Start the main application:

```bash
python main.py
```

## Model

The project uses YOLOv8 (yolov8n.pt) as the base model for object detection. The model is fine-tuned for spoofing detection tasks.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

[MIT](https://choosealicense.com/licenses/mit/)

## Acknowledgments

- YOLOv8 by Ultralytics
- MediaPipe by Google
