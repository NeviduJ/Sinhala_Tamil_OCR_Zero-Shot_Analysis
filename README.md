# Zero-Shot Analysis of OCR Engines for Sinhala and Tamil

This study presents a comparative analysis of the zero-shot performance of six distinct OCR engines on two LRLs: Sinhala and Tamil. The selected engines include both commercial and open-source systems, aiming to evaluate the strengths of each category. The Cloud Vision API, Surya, Document AI, and Tesseract were evaluated for both Sinhala and Tamil, while Subasa OCR and EasyOCR were examined for only one language due to their limitations. The performance of these systems was rigorously analysed using five measurement techniques to assess accuracy at both the character and word levels. According to the findings, Surya delivered the best performance for Sinhala across all metrics, with a WER of 2.61%. Conversely, Document AI excelled across all metrics for Tamil, highlighted by a very low CER of 0.78%.

## Tamil Text Image Dataset

In addition to the above analysis, we also introduce a novel synthetic Tamil OCR benchmarking dataset.

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

## Citation

```json
@article{jayatilleke2025zero,
  title={Zero-shot OCR Accuracy of Low-Resourced Languages: A Comparative Analysis on Sinhala and Tamil},
  author={Jayatilleke, Nevidu and de Silva, Nisansa},
  journal={arXiv preprint arXiv:2507.18264},
  year={2025}
}
```
