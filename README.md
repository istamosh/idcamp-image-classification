# IDCamp Image Classification

An image classification project using CIFAR-10 built in Jupyter Notebook with TensorFlow.

## Setup

This project uses `uv` for dependency management.

```bash
uv sync
```

## Workflow

1. Install dependencies with `uv sync`.
2. Open `main.ipynb`.
3. Run the notebook cells in order:
   - load/cache CIFAR-10 data
   - train the baseline and improved CNN models
   - evaluate the results
   - export the trained model

## Exported Model Formats

After running the export section, the trained model is saved in:

- `saved_model/` — TensorFlow SavedModel
- `tflite/` — TensorFlow Lite model and labels
- `tfjs_model/` — TensorFlow.js model files

## Folder Structure

```text
idcamp-image-classification/
├── data/
│   ├── cache/
│   └── raw/
├── saved_model/
│   ├── saved_model.pb
│   └── variables/
├── tflite/
│   ├── model.tflite
│   └── label.txt
├── tfjs_model/
│   ├── group1-shard1of1.bin
│   └── model.json
├── main.ipynb
├── pyproject.toml
├── uv.lock
└── README.md
```

## Notes

- `data/` is gitignored and stores the raw dataset plus cache files.
- Re-run the final export cell if you retrain the model.
- Use `uv lock` / `uv sync` to keep the environment reproducible across machines.
