# Table Structure Detection and CSV Extraction

This repository provides a pipeline to detect table structures from images stored on Google Drive and extract the content into CSV files. It uses the **Microsoft Table Transformer** model for structure detection and **PaddleOCR** for text extraction.

## Features
- **Table Detection:** Detects rows, columns, and headers in tables.
- **Text Extraction:** Extracts cell content using OCR.
- **CSV Export:** Saves table data into CSV format.
- **Visualization:** Outputs images with detected row and column bounding boxes.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Dhushan27/table-structure-detection.git
   cd table-structure-detection
    ```
2. Install dependencies:
    ```bash
    %pip install transformers
    %pip install pillow huggingface_hub
    %pip install timm
    %pip install matplotlib
    %pip install paddlepaddle paddleocr
    ```

3. Mount Google Drive to access data:
   ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```
4. Download the Table Transformer model:
    ```python
    from transformers import TableTransformerForObjectDetection
    model_structure = TableTransformerForObjectDetection.from_pretrained("microsoft/table-transformer-structure-recognition")
    ```

## Example Workflow

1. Detect table structure from images stored in Google Drive.
2. Extract rows, columns, and cells using bounding boxes.
3. Perform OCR on the cells and export results to CSV.

## Improvements

- **Detection Accuracy:** Enhance images or fine-tune the model for better results.
- **Table Alignment:** Improve post-processing to align rows and columns more accurately.