# Style Transfer using TensorFlow

## Overview
This project applies style transfer to images using a convolutional neural network (CNN) in TensorFlow. The goal is to generate a new image that combines the content of one image with the artistic style of another image.

## Requirements
- Python 3.x
- TensorFlow 2.x
- Matplotlib
- Google Colab (optional, for running the notebook)

## Setup
1. Mount Google Drive to access images.
2. Set the paths for the content image and style image.

```python
from google.colab import drive
drive.mount('/content/drive')
```

3. Define the content and style image paths.

```python
content_path = ('/content/drive/My Drive/dog.jpg')
style_path = ('/content/drive/My Drive/style.jpg')
```

## Code Breakdown
1. **Image Loading**: Load the images (content and style) and preprocess them.
    - Resize images to fit the neural network.
    - Normalize image pixel values to [0, 1] range.

2. **Model Setup**: 
    - Use pre-trained neural networks for feature extraction.
    - Implement a function to extract features from both the content and style images.

3. **Style Transfer Function**: 
    - Define a loss function that combines content loss and style loss.
    - Use optimization techniques to adjust the generated image iteratively to match the desired style and content.

4. **Output**: Display the generated image, which combines the content of the first image and the style of the second image.

## Usage
After setting up the notebook, run each cell sequentially. The output will be a styled image that blends content and style as per the model's training.

### Example Usage:
1. Load the content and style images.
2. Set the model parameters for style transfer.
3. Optimize the generated image to minimize the loss.
4. Display the final result.

```python
plt.imshow(generated_img[0])
```

## License
This project is open source and available under the MIT License.
