# Full-dataset-and-MLP-model-for-X-ray-dose-estimation

##  Overview

This repository contains a **full dataset of 5,606 chest X-ray images** sampled from the NIH ChestX-ray14 dataset along with **physics-based features** extracted from each image. The dataset is designed for **AI-driven radiation dose estimation, image quality assessment, and deep learning benchmarking**.

Additionally, the repository includes a **trained MLP model** for dose estimation and example notebooks demonstrating how to train, evaluate, and visualize results.



##  Dataset

* **Images:** 5,606 chest X-ray images
* **Features extracted per image:**

  * Noise variance (`noise_var`)
  * Sharpness (`sharpness`)
  * Entropy (`entropy`)
  * Mean intensity (`mean_intensity`)
  * Standard deviation of intensity (`std_intensity`)
* **Dose simulation parameters:** `scale` and `noise_std`
* **License:** CC BY-SA 4.0
* **Resolution:** Original X-ray resolution (varies)

**Purpose:**
This dataset provides a controlled environment for studying how X-ray image features change under different dose levels, supporting research in medical imaging, dose optimization, and AI enhancement methods.



##  Example Features 

| noise_var | sharpness | entropy | mean_intensity | std_intensity | image            | scale | noise_std |
| --------- | --------- | ------- | -------------- | ------------- | ---------------- | ----- | --------- |
| 128.95    | 5.95      | 7.07    | 0.544          | 0.152         | 00006199_010.png | 1.0   | 0.005     |
| 579.18    | 18.70     | 6.82    | 0.435          | 0.123         | 00006199_010.png | 0.8   | 0.020     |
| 2087.36   | 36.35     | 6.59    | 0.327          | 0.099         | 00006199_010.png | 0.6   | 0.040     |

---

##  Model Training & Results

* **Model:** Multi-Layer Perceptron (MLP) trained on physics-based features
* **Training Loss Progression:**

```
Epoch 0, Train Loss=0.5306
Epoch 5, Train Loss=0.0269
Epoch 10, Train Loss=0.0109
...
Epoch 95, Train Loss=0.0030
Test MSE: 0.0019266045
```

* **Performance Metrics on Test Set:**

  * R² Score: 0.928
  * MAE: 0.0357
  * RMSE: 0.0439

* **Visualizations included:**

  * Scatter plots (e.g., noise variance vs dose scale)
  * Feature correlation heatmaps



##  How to Use

1. **Clone the repository**

```bash
git clone https://github.com/your-username/Full-dataset-and-MLP-model-for-X-ray-dose-estimation.git
cd Full-dataset-and-MLP-model-for-X-ray-dose-estimation
```

2. **Open the example notebook**

* `x-ray-dose-simulation-mlp-full.ipynb`
* It contains step-by-step instructions for:

  * Loading dataset and features
  * Training MLP model
  * Evaluating model performance
  * Visualizing results

3. **Train your own model or evaluate**

* Modify the notebook to adjust MLP architecture, train/test split, or hyperparameters.



## Potential Use Cases

* **Dose estimation models:** Predict X-ray radiation dose from features or images
* **Image quality assessment:** Analyze noise, sharpness, and entropy
* **Denoising/enhancement research:** Benchmark algorithms on low-dose X-ray images
* **Medical physics education:** Demonstrate dose effects on image quality
* **Deep learning preprocessing:** Lightweight dataset for regression model prototyping



##  References

* NIH ChestX-ray14 Dataset: [Link](https://www.kaggle.com/datasets/nih-chest-xrays/sample)
* Physics-based feature extraction methods (Noise, Sharpness, Entropy)



##  License

This repository is licensed under **CC BY-SA 4.0**. You are free to use, share, and adapt the dataset and code with proper attribution.
