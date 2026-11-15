# Malaria Detection Using Convolutional Neural Networks

## Project Overview

Malaria is a potentially life-threatening disease caused by parasites transmitted through infected mosquitoes. Early detection plays an important role in effective treatment.

This project explores the use of **convolutional neural networks (CNNs)** and deep learning to classify microscopic red blood cell images into two categories:

- **Parasitized:** Red blood cells infected with malaria parasites.
- **Uninfected:** Red blood cells without visible malaria parasites.

The objective was to investigate different deep learning approaches, compare their performance, and identify an effective model for image-based malaria classification.

## Project Objectives

- Explore and understand the characteristics of microscopic red blood cell images.
- Prepare and preprocess images for deep learning.
- Develop and compare multiple CNN architectures.
- Evaluate the impact of different activation functions and batch normalization.
- Investigate whether data augmentation improves model performance.
- Compare a custom CNN against a pretrained VGG16 model.

## Dataset

The project uses a collection of microscopic red blood cell images divided into two classes: parasitized and uninfected.

The dataset contains variations in cell orientation, shape, size, and appearance, making it a useful application for computer vision and image classification.

The images were organized into training and testing directories and processed for use in the neural network models.

## Exploratory Data Analysis & Image Preprocessing

Initial exploration focused on understanding the image data and identifying characteristics that could influence classification performance.

Preprocessing techniques explored included:

- Resizing images to 128 × 128 pixels.
- Normalizing pixel values.
- HSV color space conversion.
- Gaussian blurring.
- Preparing image datasets for TensorFlow/Keras.

The exploration also highlighted the variation in cell orientation and appearance, which informed the use of data augmentation during model development.

## Model Development

Several neural network architectures and techniques were explored to compare their impact on classification performance.

| Model | Description |
|---|---|
| Baseline CNN | Initial convolutional neural network used as a performance baseline. |
| Model 1 | Deeper CNN architecture incorporating ELU activation. |
| Model 2 | Introduced batch normalization and LeakyReLU activation. |
| Model 3 | Built on Model 2 by incorporating data augmentation. |
| VGG16 | Transfer learning experiment using an ImageNet-pretrained VGG16 model. |

### Data Augmentation

Data augmentation was introduced to help the model account for variations in cell orientation, position, and scale.

The augmentation techniques used included:

- Random flipping
- Random rotation
- Random zoom
- Random translation

### Transfer Learning

A pretrained VGG16 architecture was also explored using ImageNet weights. Its convolutional base was frozen while the model was adapted for the binary classification task.

This provided a comparison between a custom-built CNN and a model based on an established pretrained architecture.

## Model Results & Evaluation

The strongest-performing model in the original experiments was **Model 3**, which combined convolutional layers, batch normalization, LeakyReLU activation, and data augmentation.

The notebook reported the following results:

| Metric | Model 3 |
|---|---:|
| Validation Accuracy | 97.4% |
| Validation Loss | 0.106 |
| False Positive Rate | 2.69% |
| False Negative Rate | 2.46% |

The model comparisons also indicated that incorporating batch normalization and LeakyReLU activation improved performance over the earlier CNN architectures. Adding data augmentation produced the strongest reported validation results.

## Key Findings & Conclusion

The experiments demonstrated the value of combining architectural improvements with data augmentation when classifying microscopic cell images.

Some of the most important findings were:

- Batch normalization and LeakyReLU activation improved the performance of the custom CNN.
- Data augmentation helped address variations in image orientation, position, and scale.
- Model 3 achieved the strongest reported validation performance among the architectures explored.
- VGG16 provided a useful comparison between transfer learning and a custom-built CNN.

Overall, this project provided practical experience applying deep learning to a computer vision problem and evaluating how different model design choices influence classification performance.

## Future Improvements

Potential areas for further development include:

- Experimenting with additional CNN architectures.
- Optimizing hyperparameters and learning rates.
- Exploring additional pretrained models.
- Applying Grad-CAM to better understand which image regions influence model predictions.
- Investigating model deployment for image classification.

## Tools & Technologies

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- OpenCV
- Matplotlib
- Seaborn
- Scikit-learn
- Pillow
- Jupyter Notebook

## Disclaimer

This project was developed for educational and machine learning experimentation purposes. It is not a clinically validated diagnostic tool and should not be used to diagnose malaria or guide medical treatment.

---

**Project Category:** Data Science | Deep Learning | Computer Vision
