# Face Detection and Recognition using DeepFace (FACE SEEKER)

This project leverages the [DeepFace](https://github.com/serengil/deepface) library to perform face detection and recognition. The repository demonstrates how to query an image and find matching faces from a specified image database.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Results](#results)
- [Contributing](#contributing)
- [Owner](#Owner)

## Overview
This project utilizes the DeepFace library to find and display images from a database that match a given query image. It includes:
- A function to detect faces in a database and return matching image paths.
- A visualization tool using Matplotlib to display the query image alongside matching results.

## Features
- **Face Verification**: Verify if two images are of the same person.
- **Face Detection**: Search for matching faces in a given image database.
- **Visualization**: Display the query image and matched images using Matplotlib.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Ritikyadav1/face-detection-deepface.git
   cd face-detection-deepface
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure you have the `DeepFace` library installed:
   ```bash
   pip install deepface
   ```

## Usage
1. Prepare an image database by storing images in a folder (e.g., `/content/database`).

2. Run the script to detect and visualize results:
   ```python
   python main.py
   ```

3. Modify the `image_path` and `db_path` variables in the script as needed to test with different images.

### Code Snippets
#### Face Detection Function
```python
def detect_faces(image_path, db_path):
    dfs = DeepFace.find(img_path=image_path, db_path=db_path)
    data = dfs[0]
    imgs = data['identity'].tolist()
    return imgs
```

#### Visualization Example
```python
import matplotlib.pyplot as plt

# Display the query and found images
plt.figure(figsize=(10, 5))
plt.imshow(query_img)
plt.title('Query Image')
plt.axis('off')
```

## Dependencies
- Python 3.x
- [DeepFace](https://github.com/serengil/deepface)
- Matplotlib
- OpenCV
- TensorFlow

## Results
This project outputs a list of image paths matching the query and displays them using Matplotlib. The detected images are shown side-by-side with the original query image for easy comparison.

## Contributing
Contributions are welcome! Please fork the repository, make your changes, and submit a pull request.

## Owner
RITIK YADAV 

