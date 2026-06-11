# Weed Detection YOLO

This repository contains code and config for a YOLO-based weed detection project.

## Dataset (excluded)

The `crop_weed_dataset` directory is intentionally excluded from the repository (see `.gitignore`).
This keeps the Git history small and avoids committing large image/model files (~256MB currently).

To use the project locally, provide the dataset at the repository root with the following structure:

- crop_weed_dataset/
  - images/
    - data/        (original images)
    - train/
    - valid/
    - test/
  - labels/

Options to obtain the dataset:

1. Download or copy the dataset into `crop_weed_dataset`.

2. Track dataset in Git (not recommended for large files):

```bash
git add -f crop_weed_dataset
git commit -m "Add dataset"
git push
```

3. Use Git LFS (recommended for large files):

```bash
brew install git-lfs   # macOS
git lfs install
git lfs track "*.jpg" "*.png" "*.pt"
git add .gitattributes
git add crop_weed_dataset
git commit -m "Add dataset via LFS"
git push
```

If you want, I can help enable Git LFS and add the dataset to the remote.

## Next steps

- Add a `README` or dataset download link if the dataset is hosted elsewhere.
- Add LICENSE, examples, or CI as needed.
