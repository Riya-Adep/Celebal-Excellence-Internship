# **Week 6 Assignment | Deep Learning Internship – Celebal Technologies**
## 🧹 MNIST Image Denoising using Convolutional Autoencoders
---
A **Convolutional Denoising Autoencoder** is implemented using the **MNIST Handwritten Digit Dataset** to reconstruct clean images from noisy inputs. The model learns compact latent representations through an encoder and reconstructs high-quality denoised images using a decoder.

This project demonstrates the complete deep learning workflow, including data preprocessing, noise generation, model building, training, evaluation, and image reconstruction.

---

# 🧠 What is a Denoising Autoencoder?

A **Denoising Autoencoder (DAE)** is a neural network that learns to recover clean data from corrupted inputs.

Instead of memorizing the input, the network learns meaningful compressed representations (latent features) that preserve important information while filtering out unwanted noise.

The architecture consists of two major components:

### 🔹 Encoder
- Extracts important visual features.
- Compresses the input image into a lower-dimensional latent representation.
- Learns edges, curves, and digit structures.

### 🔹 Decoder
- Reconstructs the original clean image.
- Restores spatial information.
- Removes noise while preserving the handwritten digit.

---

# 📂 Dataset Information

**Dataset:** MNIST Handwritten Digits

The MNIST dataset is one of the most widely used benchmark datasets for computer vision and deep learning tasks.

| Property | Value |
|----------|-------|
| Training Images | 60,000 |
| Testing Images | 10,000 |
| Image Size | 28 × 28 |
| Color Format | Grayscale |

Before training:

- Images were normalized to pixel values between **0 and 1**.
- Artificial **Gaussian Noise** was added to create noisy input images.
- The original clean images were used as target outputs.

---

# 🏗 Model Architecture

The proposed model is a **Convolutional Denoising Autoencoder**.

## Encoder

```text
Input Image (28×28×1)
        │
        ▼
Conv2D (32 Filters, ReLU)
        │
MaxPooling2D
        │
Conv2D (64 Filters, ReLU)
        │
MaxPooling2D
        │
Conv2D (128 Filters, ReLU)
        │
Latent Representation
```

## Decoder

```text
Latent Representation
        │
        ▼
Conv2D (128 Filters, ReLU)
        │
UpSampling2D
        │
Conv2D (64 Filters, ReLU)
        │
UpSampling2D
        │
Conv2D (32 Filters, ReLU)
        │
Conv2D (1 Filter, Sigmoid)
        │
Reconstructed Image (28×28×1)
```

The encoder progressively compresses the image while extracting meaningful features. The decoder restores the original spatial dimensions and reconstructs a clean image from the compressed representation.

---

# ⚙️ Training Configuration

| Parameter | Value |
|-----------|-------|
| Optimizer | Adam |
| Loss Function | Binary Crossentropy |
| Batch Size | 128 |
| Early Stopping | Enabled |
| Noise Type | Gaussian Noise |
| Noise Factor | 0.5 |

---

# 📊 Model Performance

| Metric | Value |
|---------|-------|
| Training Epochs | 8 |
| Reconstruction Error (MSE) | **0.009138** |

---

# 📷 Original vs Noisy Images

Artificial Gaussian noise was added to the clean MNIST images to generate the noisy inputs used during training.

<img width="1184" height="497" alt="image" src="https://github.com/user-attachments/assets/12ecad0e-c075-42c1-8a67-1a5f6157f4e2" />


---

# 🏗 Model Architecture Visualization

The following figure illustrates the complete architecture of the Convolutional Denoising Autoencoder.


<img width="570" height="1765" alt="image" src="https://github.com/user-attachments/assets/c90763cd-83a9-4c5a-83bb-2e90e11ec65f" />

---

# 📉 Training Performance

The graph below illustrates the variation of **training loss** and **validation loss** during training.

The model converged successfully, and **Early Stopping** restored the best-performing model after **8 epochs**, preventing unnecessary training.


<img width="717" height="470" alt="image" src="https://github.com/user-attachments/assets/f30d6996-5158-40aa-a3b6-1c866709d599" />


---

# ✨ Image Reconstruction Results

The figure below compares:

- Original Image
- Noisy Image
- Reconstructed (Denoised) Image

The trained autoencoder successfully removes Gaussian noise while preserving the overall digit structure.


<img width="1468" height="891" alt="image" src="https://github.com/user-attachments/assets/65519c60-484d-4eca-96df-abe7376b151b" />


---

# 📌 Observations

- Successfully implemented a Convolutional Denoising Autoencoder for handwritten digit reconstruction.
- The encoder learned meaningful latent representations from noisy images.
- The decoder effectively reconstructed clean images while preserving digit structures.
- Training loss decreased consistently, while validation loss remained stable, indicating good generalization.
- Early Stopping automatically terminated training after **8 epochs**, restoring the best-performing model.
- The reconstruction error (**MSE = 0.009138**) demonstrates that the reconstructed images closely resemble the original clean images.
- The model effectively removed Gaussian noise without significantly distorting the handwritten digits.

---

# ⚠️ Challenges

- Selecting an appropriate noise factor without making reconstruction excessively difficult.
- Preserving fine image details while removing Gaussian noise.
- Balancing model complexity with reconstruction performance.
- Preventing overfitting using Early Stopping.

---

# 🚀 Future Improvements

- Compare Binary Crossentropy with Mean Squared Error (MSE).
- Train with different Gaussian noise levels.
- Implement a Variational Autoencoder (VAE).
- Compare Dense and Convolutional Autoencoders.
- Evaluate reconstruction quality using **PSNR** and **SSIM**.
- Experiment with deeper encoder-decoder architectures.

---

# ▶️ How to Run

## Clone the Repository

```bash
git clone https://github.com/<your-username>/<repository-name>.git
```

## Install Dependencies

```bash
pip install tensorflow numpy matplotlib pandas scikit-learn pillow
```

## Run the Notebook

Open:

```text
Week6_Riya_Adep.ipynb
```

using:

- Jupyter Notebook
- Google Colab
- VS Code

Run all cells sequentially.

---

# 📚 Key Learning Outcomes

- Understanding Autoencoders and Denoising Autoencoders
- Encoder–Decoder Architecture
- Latent Space Representation
- Image Reconstruction
- Gaussian Noise Generation
- Convolutional Neural Networks
- Early Stopping
- Binary Crossentropy Loss
- Model Evaluation using Mean Squared Error (MSE)

---

# 👩‍💻 Author

**Riya Adep**

MCA Student  
Deep Learning Internship – Celebal Technologies
