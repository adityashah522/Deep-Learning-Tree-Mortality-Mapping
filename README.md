# Deep-Learning-Tree-Mortality-Mapping
# Tree Death Detection: Deep Learning for Forestry Analysis

This repository contains a Jupyter Notebook designed for detecting tree mortality using high-resolution satellite or aerial imagery. The project utilizes a **U-Net** deep learning architecture for semantic segmentation, identifying dead or dying trees from multi-spectral raster data.

## Project Overview

The goal of this project is to automate the detection of tree death to aid in forestry management, wildfire risk assessment, and ecological monitoring. The notebook demonstrates a full end-to-end workflow, including:

* **Data Preparation**: Loading and preprocessing multi-band `.tif` raster files.
* **Model Architecture**: Implementing a U-Net model optimized for segmentation.
* **Training & Evaluation**: Training the model on labeled data and evaluating performance using metrics like F1-score, Precision, Recall, and Accuracy.

## Features

* **Google Colab Integration**: Optimized for use with Google Drive for data storage and retrieval.
* **Raster Data Processing**: Specifically designed to handle geospatial data using libraries like `rasterio` and `tifffile`.
* **Automated Metrics**: Detailed global evaluation outputs to measure model performance across study areas.

## Prerequisites & Installation

To run the notebook, you will need a Python environment with the following dependencies:

```bash
pip install rasterio numpy imageio pandas tqdm matplotlib scikit-learn tifffile

```

The notebook also requires access to **Google Colab** if you intend to use the integrated Google Drive mounting feature.

## Getting Started

1. **Clone the Repository**:
```bash
git clone https://github.com/your-username/tree-death-detection.git

```


2. **Upload to Colab**: Open the `.ipynb` file in Google Colab.
3. **Mount Google Drive**: Ensure your data is stored in your Drive. The default path in the notebook is `/content/drive/MyDrive/Tree_Mortality`.
4. **Run the Cells**: Execute the cells sequentially to install dependencies, load data, and start the training/evaluation process.

## Data Structure

The notebook expects training data to be organized in a specific directory structure:

* `Training/`: Contains high-resolution `.tif` imagery (e.g., `studyarea77.tif`).
* `Results/`: Location where global evaluation text files and model checkpoints are saved.

## Evaluation Results

The model outputs a global evaluation report including:

* **F1-Score**: Balancing precision and recall for dead tree detection.
* **Precision & Recall**: Measuring the accuracy of positive detections.
* **Accuracy**: Overall classification success rate.

Results are automatically saved to a text file in the results directory (e.g., `global_eval_checkpoint.txt`).

## License

This project is licensed under the MIT License - see the LICENSE file for details.
