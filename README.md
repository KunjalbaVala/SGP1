# TensorFlow Object Detection and Object Counting

## Overview
This project uses a pretrained TensorFlow object detection model to detect objects in a customized dataset and count the number of each detected object. The model is fine-tuned to achieve better accuracy on the specific dataset provided.

## Installation

### Prerequisites
- Python 3.8+
- TensorFlow 2.4+
- Other dependencies listed in `setup.py`

### Installation Steps
1. **Clone the repository:**
    ```bash
    git clone https://github.com/KunjalbaVala/SGP1.git
    cd your-repo
    ```

2. **Create and activate a virtual environment:**
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows use `env\Scripts\activate`
    ```

3. **Install the required packages:**
    ```bash
    pip install -r setup.py
    ```

## Usage

### Running the Model
To run the object detection model on an image and count detected objects, use the following command:
```bash
python detect_from_image_count_objects.py --image_path /path/to/image.jpg
```

### Examples
- **Example 1:** Detecting objects in a sample image.
    ```bash
    python detect_from_image.py --image_path samples/image1.jpg
    ```

- **Example 2:** Batch processing multiple images.
    ```bash
    python detect_from_image.py --image_dir samples/
    ```

## Dataset

### Dataset Information
The dataset used for this project includes a customized collection of images labeled with the objects of interest and is downloaded from kaggle.

### Data Preparation
1. **Organize the dataset**: Ensure your images and annotations are in the correct format. The structure should look like this:
    ```
    dataset/
    ├── images/
    │   ├── image1.jpg
    │   ├── image2.jpg
    │   └── ...
    └── annotations/
        ├── image1.xml
        ├── image2.xml
        └── ...
    ```

2. **Convert annotations to TensorFlow format**: Use a script to convert XML annotations to TensorFlow's TFRecord format if necessary.
In this project I have converted all the xml files to csv format, to do so you can go through `xml_to_csv.py` and proceed further.


## Results

We wil get the following kind of output for the trained model.

### Object Counts
- **Image 1**: 3 apples, 2 oranges
- **Image 2**: 1 apple, 4 bananas


## Contact
For questions, please contact me at kunjalbavala@gmail.com

