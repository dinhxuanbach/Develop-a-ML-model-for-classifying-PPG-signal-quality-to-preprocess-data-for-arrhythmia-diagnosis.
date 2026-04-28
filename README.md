# Develop-a-ML-model-for-classifying-PPG-signal-quality-to-preprocess-data-for-arrhythmia-diagnosis.
# ECG Signal Steganography & Watermarking (MIT-BIH)

This project implements the encoding and embedding of secure information (watermarking/steganography) into electrocardiogram (ECG) signals using the MIT-BIH Arrhythmia Database. The project combines digital signal processing and cryptography techniques to protect patient information.

## 🚀 Key Features

1. **Biomedical Signal Processing:** Reads and processes V1 lead ECG signals from the MIT-BIH dataset.

2. **Signal Quality Index (SQI):** Evaluates signal quality (noise level, saturation, SNR) before data embedding.

3. **Cryptography:** - Generates a multi-dimensional security key based on patient ID, patient name, and system hardware information (Node, Processor, Machine).

- Encrypt data using **AES (Advanced Encryption Standard)** with `MODE_EAX`.

4. **Steganography:**

- Apply the Fast Walsh-Hadamard Transform (FWHT) to the ECG signal.

- Define the multidimensional space and embed the encoded data bits into the FWHT coefficients.

- Reconstruct the watermarked signal using the inverse transform (IFWHT).

## 🛠 System Requirements (Dependencies)

Ensure you have installed Python 3.x and the following libraries:

```bash
pip install numpy pandas matplotlib scipy sympy
pip install key-generator pycryptodome
