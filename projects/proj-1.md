---
title: EEG Neural Data ML Comparison for BCI Product
excerpt: Evaluating PCA, ICA, and VAE for high-dimensional EEG classification
---

<img src= "/assets/brain-8825819_1280.jpg" alt="Brain Illustration" width="300">


**Problem:**  
Brain–Computer Interfaces (BCIs) are an emerging technology that enable computers to interpret neural signals, allowing users to interact with machines using brain activity alone.

Beyond their scientific appeal, BCIs have strong commercial and product potential across gaming, assistive technology, and biomedical devices. EEG-based BCIs are particularly compelling because they are non-invasive, relying on wearable sensors rather than surgical implants, making them far more realistic for consumer-facing products.

Here, I evaluate how different dimensionality reduction techniques impact classification performance and computational respources on high-dimensional EEG time-series data (BCI Competition IV-2a dataset, motor imagery task).

**Approach:**  
- Preprocessing: Bandpass filtering (7–30 Hz), artifact removal, epoching  
- Dimensionality reduction: PCA, ICA, Variational Autoencoder (VAE), or control group (no DR applied)
- Classification: SVM (binary: Left vs Right hand)  
- Evaluation: Accuracy, F1-score, inference time  

![Overview Flow Chart](https://github.com/bellasteinbeck/EEG-Motor-Imagery-Binary-Classification/raw/main/figures/overview_flow_chart.png)

**Results:**  
- ICA achieved the highest accuracy (73.1%) and F1-score (~0.8)  
- PCA offered no improvement over raw data  
- VAE underperformed due to dataset size and hyperparameters  

![Classification Results](https://github.com/bellasteinbeck/EEG-Motor-Imagery-Binary-Classification/raw/main/figures/final_radar_chart_compare.png)

**Tools:** Python, Numpy/Pandas, MNE, Scikit-learn, PyTorch/TensorFlow, Matplotlib/Seaborn, Jupyter Notebooks  

**Takeaway:** ICA provides the best balance of accuracy, interpretability, and robustness for practical EEG-based BCIs.

[View GitHub Repository](https://github.com/bellasteinbeck/EEG-Motor-Imagery-Binary-Classification)
