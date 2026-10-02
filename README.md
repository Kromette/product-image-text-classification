# Product Image & Text Classification

Feasibility study for the **automatic categorization of e-commerce products** using product descriptions and images.

The project investigates whether text and image features can be used to automatically group products belonging to the same categories, as a first step towards automating product categorization for an e-commerce marketplace.

## Overview

This project was conducted for a fictional e-commerce marketplace where sellers manually assign categories to their products when listing them.

The objective was to assess the feasibility of an automated categorization system based on two complementary sources of information:

* **Product descriptions**
* **Product images**

Rather than building a supervised classification model, the project focuses on an initial **unsupervised feasibility study**. Different text and image feature extraction approaches are compared, followed by dimensionality reduction and clustering to determine whether products from the same category naturally group together.

## Objectives

The project aims to:

* Preprocess product descriptions and images.
* Extract meaningful features from text using several representation approaches.
* Extract features from product images using traditional computer vision and transfer learning.
* Reduce high-dimensional feature spaces to two dimensions for visualization.
* Apply clustering techniques to the extracted representations.
* Compare the resulting clusters with the known product categories.
* Assess whether the extracted features are sufficiently informative to support automatic product categorization.

## Methodology

### 1. Text preprocessing and feature extraction

Several approaches are explored to represent product descriptions numerically:

* **Bag-of-Words** with simple word counts
* **TF-IDF**
* **Word2Vec** / classical word or sentence embeddings
* **BERT**
* **Universal Sentence Encoder (USE)**

The resulting representations are analyzed and compared to assess how well the different approaches capture similarities between product categories.

### 2. Image preprocessing and feature extraction

Product images are processed using two complementary approaches:

* A traditional local feature extraction method based on **SIFT, ORB or SURF**
* **CNN Transfer Learning** to obtain higher-level image representations

These approaches are used to investigate whether visual information alone can help distinguish between product categories.

### 3. Dimensionality reduction

Because the extracted text and image features can have hundreds or thousands of dimensions, dimensionality reduction techniques are applied to obtain two-dimensional representations.

The resulting projections are visualized to investigate:

* The structure of the feature space
* Similarities between products
* Separation between known product categories
* Potential relationships between categories

### 4. Clustering

Unsupervised clustering is then applied to the extracted features.

The clusters are compared with the **true product categories** using quantitative similarity measures to assess whether products belonging to the same category tend to be grouped together.

The combination of visual analysis and quantitative evaluation provides evidence for assessing the feasibility of automatic product categorization.

## Results

The project compares different representations of both textual and visual information and evaluates their ability to recover the underlying product categories.

The analysis includes:

* 2D visualizations of the reduced feature spaces
* Cluster visualizations
* Comparison between clusters and known categories
* Quantitative similarity measurements
* Comparison of text-based and image-based representations

The detailed experiments and results are available in the notebooks.

## Repository Structure

```text
.
├── notebooks/
│   ├── 01_text_features.ipynb
│   ├── 02_image_features.ipynb
│
├── presentation/
│   └── project_presentation.pdf
│
├── README.md
└── requirements.txt
```

## Tools & methods

**Python** · **Pandas** · **NumPy** · **Scikit-learn** · **TensorFlow / Keras** · **OpenCV** · **NLTK** · **Jupyter Notebook** · NLP · Bag-of-Words · TF-IDF · Word embeddings · BERT · Universal Sentence Encoder · Computer vision · CNN Transfer Learning · Dimensionality reduction · Clustering · Data visualization

## Context

This project was completed as part of the **Data Scientist training program at OpenClassrooms**.

The project focuses on an initial feasibility study rather than the development of a production classification system. The objective was to determine whether the information extracted from product descriptions and images could effectively reveal the underlying product categories through unsupervised methods.
