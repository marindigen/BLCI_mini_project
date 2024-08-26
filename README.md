# Brain Like Computing and Intelligence - MiniProject

## Overview

This repository contains the code and resources used for the MiniProject as part of the NX-414 course on Brain Like Computing and Intelligence. The project explores the use of both task-driven and data-driven approaches to model and predict neural firing rates based on image datasets. The main objective was to compare different modeling techniques, including linear models, PCA-based dimensionality reduction, and Convolutional Neural Networks (CNNs), to determine their efficacy in predicting neuronal activity.

## Project Structure

- **`week6/`**: Contains the ipynb notebook corresponding to neural activity predictions using the task-driven approach. This allows network to develop representations that resemble the ones of the biological brain. Contains the implementations of the various models used, including Ridge Regression, PCA-based models, and ResNet50 pre-trained and randomly initialised architectures. The folder also contains saved activations of layers.
- **`week7.ipynb`**: Contains the ipynb notebook corresponding to neural activity predictions using the data-driven approach. Explores simple optimised for the data CNN architecture with 2-3 convolutional layers.
- **`week9/`**: Includes the ipynb notebook with experiments with different architecture models and co-training network that contains the best performing ResNet50 model on images of objects and neural data to classify the images. The folder also includes activations of different pre-trained CNNs.
- **`test/`**: Contains the best model's performance on test data.
- **`MiniProject_report_final.pdf`**: Contains the final project report and any supplementary documentation.

## Models and Methodologies

### Task-Driven Approach

- **Ridge Regression**: Implemented with PCA-based dimensionality reduction using activations from layers of pre-trained models like ResNet50 and VGG19. The Ridge Regression model trained on PCA activations from ResNet50 showed the highest explained variance of 0.406 and a correlation of 0.628 on the validation set.

### Data-Driven Approach

- **Convolutional Neural Networks (CNNs)**: Several CNN architectures were explored, with variations in the number of layers, batch sizes, and hyperparameters like learning rate and weight decay. The best-performing CNN model had three layers, a batch size of 32, and a learning rate of 0.001. However, its performance was lower compared to the task-driven approach, with an explained variance of 0.2100.

### Experimentation and Results

- Various models were tested, including linear models and more complex neural networks. The results showed that simpler linear models with PCA-based features from pre-trained networks performed better in predicting neural firing rates compared to more complex CNNs. The final Ridge Regression model with ResNet50 PCA features was the best performer.

## Key Findings

- **Best Model**: Ridge Regression using PCA activations from ResNet50, with a mean explained variance of 0.406 and a correlation of 0.628.
- **CNN Performance**: Although CNNs were optimized through hyperparameter tuning, they did not outperform simpler linear models in this task.
- **Importance of Pre-trained Models**: Utilizing activations from pre-trained models like ResNet50 and VGG19 significantly improved the performance of the Ridge Regression models.

## Installation

To run the code in this repository, follow these steps:

Clone the repository:
   ```bash
   git clone https://github.com/username/project-repo.git
   ```

## Usage

- **Data Preparation**: Place your datasets in the `data/` directory. Ensure that the datasets are in the correct format as expected by the scripts.
- **Training Models**: Use the scripts provided in the `scripts/` directory to train the models and generate predictions. Modify the parameters in the scripts as needed for your experiments.
- **Evaluation**: Results will be saved in the `results/` directory, and performance metrics will be displayed.

## Contributions

Feel free to submit pull requests or report issues. Any contributions that improve the models or add new features are welcome.

## References

- Majaj, Najib J., et al. "Simple Learned Weighted Sums of Inferior Temporal Neuronal Firing Rates Accurately Predict Human Core Object Recognition Performance." The Journal of Neuroscience 35.39 (2015): 13402-13418. DOI: [10.1523/JNEUROSCI.5181-14.2015](https://doi.org/10.1523/JNEUROSCI.5181-14.2015).

For more detailed information, please refer to the final report available in the `report/` directory.

---

This README provides an overview of the project and instructions on how to use the repository. Please refer to the documentation and comments in the code for further details.
