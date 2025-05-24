---
language:
- ta
tags:
- tamil
- text
- images
- ocr
task_categories:
- image-to-text
---

# Tamil Text Image Dataset

This dataset contains images of Tamil text generated from 6 different fonts:

- Hind_Madurai
- Noto_Serif_Tamil
- Kavivanar
- Noto_Sans_Tamil
- Pavanam
- Anek_Tamil

## Dataset Description

The dataset consists of images of Tamil text, with each image containing a single line of Tamil text. The text is derived from Opus OpenSubtitles. The images were generated using a variety of popular Tamil fonts to enhance diversity for tasks like OCR.

## Structure

The dataset has the following structure:

```json
DatasetDict({
    data: Dataset({
        features: ['image', 'text'],
        num_rows: 7000
    })
})
```
## How to Use the Dataset

You can easily load this dataset using the `datasets` library:

```python
from datasets import load_dataset

# Load the dataset
dataset = load_dataset("Nevidu/tamil_synthetic_ocr")

# Access the first example
first_example = dataset['data'][0] 

# Get the image and text
image = first_example['image']
text = first_example['text']

print(f"Text: {text}")
# image.show() # To display the image (requires libraries like Pillow)
```
