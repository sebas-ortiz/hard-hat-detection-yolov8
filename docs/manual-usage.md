# Manual Usage

## Purpose

This document explains how to use the notebook, either to train the model from scratch or to run inference with the included trained model.

## Files Used

- `hard_hat_detection_yolov8.ipynb` — main notebook
- `models/helmet.pt` — trained model
- `requirements.txt` — dependencies
- `examples/sample_input.jpg` — sample image
- `examples/sample_prediction.jpg` — sample prediction

## Requirements

- Python 3.10+
- Google Colab or Jupyter Notebook
- Internet connection for dataset download
- Libraries listed in `requirements.txt`

## Installation

```bash
pip install -r requirements.txt
```

## Option A — Train from scratch

1. Open `hard_hat_detection_yolov8.ipynb` in Google Colab.
2. Run the installation cells.
3. Download the dataset using your own Roboflow API key.
4. Create the 1000-image subset.
5. Generate the `data.yaml` file.
6. Load YOLOv8n.
7. Run training.
8. Validate the model and review the generated plots.

## Option B — Run inference with the included model

1. Open `hard_hat_detection_yolov8.ipynb` in Google Colab.
2. Load `models/helmet.pt`.
3. Upload or select an input image.
4. Run the inference cells.
5. Review the generated prediction with bounding boxes and labels.

## Expected Outputs

The notebook can generate:

- training curves
- confusion matrix
- label distribution plots
- prediction images
- validation metrics such as precision, recall, and mAP

## Troubleshooting

### Dataset download fails
Check the Roboflow workspace, project version, internet connection, and API key.

### Training is too slow
Use a GPU runtime in Google Colab and reduce dataset size or epochs if necessary.

### Inference fails
Check that `helmet.pt` is loaded correctly and the image path is valid.

### Missing dependencies
Run the installation cells again or install packages from `requirements.txt`.

## Notes

- Do not upload API keys.
- Do not upload the full dataset.
- Do not upload temporary Colab files.
- Keep only the notebook, the trained model, the main artifacts, and sample outputs in the repository.
