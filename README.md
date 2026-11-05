# Fashion-MNIST Pattern Recognition Project

This project compares classical machine-learning pipelines for classifying the
10 categories of Fashion-MNIST clothing images. Each image is 28 × 28 pixels
and grayscale.

## Method and results

The experiment uses a stratified sample of 20,000 training images to compare
six approaches with stratified 3-fold cross-validation (random seed 42):

1. K-nearest neighbors on raw pixels
2. Linear SVM on raw pixels
3. PCA (100 components) and RBF SVM on raw pixels
4. HOG features and a linear SVM
5. HOG features, PCA (100 components), and a linear SVM
6. HOG features, PCA (100 components), and an RBF SVM

The best-performing cross-validation pipeline was HOG + PCA + RBF SVM, with
mean accuracy 0.8936 and mean macro-F1 0.8933. Evaluated once on the official
10,000-image test set, it achieved accuracy 0.8940 and macro-F1 0.8941.

## Project files

| File | Description |
| --- | --- |
| `PR_project.ipynb` | Google Colab notebook containing the data exploration, preprocessing, HOG feature extraction, model comparison, evaluation, and result generation. |
| `pr_project.py` | Python export of the project workflow. It includes Google Colab-specific commands; use the notebook to run the project in Colab. |
| `fashion_mnist_train.csv` | 60,000 Fashion-MNIST training examples. |
| `fashion_mnist_test.csv` | 10,000 official test examples. |
| `fashion_mnist_all.csv` | Combined dataset of 70,000 examples. |
| `fashion_mnist_results_bundle.zip` | Experiment settings and Excel workbooks with cross-validation fold results and summary, final metrics, test classification report, and test predictions. |
| `PR_Report_FFF.docx` | Project report describing the dataset, preprocessing, HOG/PCA features, classifiers, experimental protocol, evaluation, and discussion. |
| `PR_presentation_F.pptx` | Presentation of the methodology, model comparisons, results, confusion matrix, conclusions, and limitations. |
| `.gitattributes` | Configures Git LFS for the large training and combined CSV files. |

Each dataset CSV has 786 columns: the numeric label, class name, and 784 pixel
values.

## Download CSV files

The CSV files are also available through these Google Drive links:

1. [CSV file 1](https://drive.google.com/file/d/1FUq_pp1R03w5f5w7-luM2RUQ5UJDdo3p/view?usp=drive_link)
2. [CSV file 2](https://drive.google.com/file/d/1asHyqGE6SY07wFJb_diV_YFKv9yqecGm/view?usp=sharing)
3. [CSV file 3](https://drive.google.com/file/d/1PPMs4yO70nSWqRk6KCWdwXoHHhs0OvGn/view?usp=sharing)
4. [CSV file 4](https://drive.google.com/file/d/1vvpJmjGtMnRevJuMfxLFbw8kMY8Ix2PE/view?usp=sharing)

To make a file accessible to everyone, set its Google Drive sharing permission
to **Anyone with the link**.
