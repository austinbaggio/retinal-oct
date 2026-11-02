# Retinal OCT

Workspace for retinal disease classification on optical coherence tomography (OCT) images.

## Dataset

[Retinal OCT Image Classification - C8](https://www.kaggle.com/datasets/obulisainaren/retinal-oct-c8) by Obuli Sai Naren (version 3), stored in [`data/`](data/). It has 24,000 JPEG images of varying dimensions, in 8 balanced classes.

| Class    | Condition                         | `train` | `val` | `test` | Total  |
|----------|-----------------------------------|---------|-------|--------|--------|
| `AMD`    | Age-related macular degeneration  | 2,300   | 350   | 350    | 3,000  |
| `CNV`    | Choroidal neovascularization      | 2,300   | 350   | 350    | 3,000  |
| `CSR`    | Central serous retinopathy        | 2,300   | 350   | 350    | 3,000  |
| `DME`    | Diabetic macular edema            | 2,300   | 350   | 350    | 3,000  |
| `DR`     | Diabetic retinopathy              | 2,300   | 350   | 350    | 3,000  |
| `DRUSEN` | Drusen                            | 2,300   | 350   | 350    | 3,000  |
| `MH`     | Macular hole                      | 2,300   | 350   | 350    | 3,000  |
| `NORMAL` | No abnormalities                  | 2,300   | 350   | 350    | 3,000  |
| **Total**|                                   | **18,400** | **2,800** | **2,800** | **24,000** |

```
data/
├── train/<class>/<class>_train_<n>.jpg
├── val/<class>/<class>_val_<n>.jpg
├── test/<class>/<class>_test_<n>.jpg
├── KAGGLE_README.md    # the publisher's original README
└── LICENSE             # CC BY-NC-SA 4.0
```

Images are unchanged from the Kaggle download. Only the folder layout differs: `RetinalOCT_Dataset/RetinalOCT_Dataset/` became `data/`.

### Notes on using the data

- The publisher's README says the split is 75/15/15, but the actual split is about 76.7/11.7/11.7.
- The publisher says the images were compiled from multiple sources and augmented with cropping, padding and horizontal flipping. It doesn't say whether augmentation happened before splitting, so check for near-duplicates across splits before trusting test scores.

## License and citation

The dataset in `data/` is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/), as published on Kaggle: non-commercial use only, with attribution, and derivatives must use the same license. The full text is in [`data/LICENSE`](data/LICENSE).

> Obuli Sai Naren. (2021). *Retinal OCT Image Classification - C8* [Data set]. Kaggle. https://doi.org/10.34740/KAGGLE/DSV/2736749
