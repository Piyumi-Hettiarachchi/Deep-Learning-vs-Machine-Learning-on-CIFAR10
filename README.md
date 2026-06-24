# Deep-Learning-vs-Machine-Learning-on-CIFAR10
Comparative study of Deep Learning and Classical Machine Learning for CIFAR-10 image classification using ResNet-18 and RBF SVM with comprehensive performance evaluation.

This project presents a comparative study between Deep Learning and Classical Machine Learning approaches for image classification on the CIFAR-10 dataset.

Two different approaches were implemented and evaluated:

- Deep Learning using ResNet-18
- Classical Machine Learning using RBF Support Vector Machine (SVM)

The objective was to investigate the strengths and limitations of both approaches and determine which method performs better for multi-class image classification.

---

## Dataset

The project uses the CIFAR-10 dataset, which consists of 60,000 colour images across 10 classes:

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

The dataset was divided into:

- Training set: 45,000 images
- Validation set: 5,000 images
- Test set: 10,000 images

All experiments used identical data splits to ensure a fair comparison. :contentReference[oaicite:1]{index=1}

---

## Objectives

- Compare Deep Learning and Classical Machine Learning performance.
- Evaluate model effectiveness using multiple metrics.
- Investigate per-class performance differences.
- Analyse strengths and limitations of each approach.

---

## Models Implemented

### Deep Learning Model

- Architecture: ResNet-18 CNN
- Framework: PyTorch
- Transfer Learning using ImageNet pre-trained weights

### Machine Learning Model

- Algorithm: RBF Support Vector Machine (SVM)
- Feature Extraction:
  - HOG
  - HSV Colour Histogram
  - LBP
- Dimensionality Reduction:
  - PCA (95% variance retained)

---

## Technologies Used

- Python
- PyTorch
- Scikit-learn
- NumPy
- Pandas
- Matplotlib
- OpenCV
- Jupyter Notebook

---

## Evaluation Metrics

Models were evaluated using:

- Accuracy
- Macro Precision
- Macro Recall
- Macro F1 Score
- Weighted F1 Score
- Confusion Matrix

Macro F1 Score was selected as the primary evaluation metric because it provides a balanced assessment across all classes. 

---

## Results

| Metric | ResNet-18 | RBF SVM |
|---------|-----------|---------|
| Accuracy | 94.39% | 65.55% |
| Macro Precision | 94.40% | 65.54% |
| Macro Recall | 94.39% | 65.55% |
| Macro F1 Score | 94.39% | 65.51% |

ResNet-18 significantly outperformed the RBF SVM across all evaluation metrics. The Deep Learning model achieved a Macro F1 Score of 94.39%, while the Machine Learning model achieved 65.51%.

---

## Key Findings

- Deep Learning achieved substantially higher classification performance.
- ResNet-18 maintained consistently strong performance across all classes.
- Classical Machine Learning performed competitively on structured classes such as automobiles and trucks.
- Hand-crafted features struggled with visually similar classes such as cats and dogs
- Deep Learning is the preferred approach when sufficient computational resources are available. 

---

## Project Structure

```text
Deep-Learning-vs-Machine-Learning-on-CIFAR10/
│
├── development_DL.ipynb
├── development_ML.ipynb
├── appendix.pdf
├── README.md

```

---

Open Jupyter Notebook:

```bash
jupyter notebook
```

Run:

```text
development_DL.ipynb
```

or

```text
development_ML.ipynb
```

---

## Future Improvements

- Explore Vision Transformers (ViT)
- Investigate additional feature extraction methods
- Perform extensive hyperparameter optimisation
- Evaluate larger image datasets

## License

This project was developed for educational purposes as part of the COS80027 Machine Learning unit at Swinburne University of Technology.
