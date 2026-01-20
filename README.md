# 🖼️➡️🇧🇩 Image-to-Bangla Caption Generation (ViT + Transformer)

This project focuses on generating **Bangla natural language captions from images** using a modern **Vision–Language Encoder–Decoder architecture**.

Most image captioning research is heavily **English-centric**, while Bangla (spoken by **230M+** people) has limited high-quality vision–language resources. This work aims to improve Bangla caption generation by using stronger visual representation learning and better cross-modal alignment. fileciteturn1file0

---

## ✨ Key Highlights

- ✅ Bangla Image Captioning (Vision → Language)
- ✅ **Vision Transformer (ViT)** image encoder
- ✅ **Transformer** text decoder
- ✅ **Gated Cross-Attention Fusion (CAF)** for better vision–language alignment
- ✅ Trained and tested on a Bangla caption dataset (BNLIT)

---

## 🧠 Model Architecture

### **Encoder**
- **Vision Transformer (ViT)**
- Splits an image into patches → converts them into tokens
- Self-attention learns **global context from early layers** fileciteturn1file0

### **Fusion Module**
- **Gated Cross-Attention Fusion (CAF)**
- Refines visual tokens and balances raw vs contextualized features fileciteturn1file0

### **Decoder**
- **Transformer Decoder**
- Uses cross-attention over visual tokens to generate Bangla caption tokens fileciteturn1file0

---

## 📌 Dataset Used

This project uses the **Bangla Natural Language Image to Text (BNLIT)** dataset:

- **8,743 images**
- **Bangladesh perspective images**
- **1 Bangla caption per image**
- Preprocessed image sizes:
  - **224×224**
  - **500×375**
- Includes a CNN feature file: `features.pkl`

🔗 Dataset link (Mendeley Data):  
https://data.mendeley.com/datasets/ws3r82gnm8/4

---

## 📂 Project Files

Main notebook in this project:

- `ViT.ipynb` *(training + evaluation + caption generation)*

---

## ⚙️ Requirements

Recommended Python version:
- **Python 3.8+**

Install common dependencies:

```bash
pip install numpy pandas matplotlib pillow tqdm scikit-learn torch torchvision transformers
```

*(If your notebook uses TensorFlow/Keras instead, install those libraries accordingly.)*

---

## ▶️ How to Run

### ✅ Option 1: Run Notebook

1. Clone the repository:
   ```bash
   git clone <your-repo-link>
   cd <your-repo-folder>
   ```

2. Download the dataset from Mendeley and place it in your project directory.

3. Open the notebook:
   ```bash
   jupyter notebook ViT.ipynb
   ```

4. Run all cells to:
   - load images + captions  
   - preprocess tokens  
   - train the model  
   - generate Bangla captions  

---

## 📊 Motivation

Bangla captioning is still challenging because:

- Most datasets/models are optimized for English
- Bangla datasets are smaller and often limited in caption diversity
- CNN-based encoders may lose global context by collapsing features into a single vector fileciteturn1file0

This project addresses these gaps using a **ViT-based encoder** and improved attention fusion.

---

## ✅ Expected Outcome

- Better global image understanding using ViT tokens  
- Improved alignment between **image regions ↔ Bangla words**
- More natural and context-aware Bangla captions fileciteturn1file0

---

## 👨‍💻 Author

**Hasin Almas Sifat**  
📧 Email: hasin.almas.sifat@gmail.com  
🔗 LinkedIn: https://www.linkedin.com/in/hasin-almas-sifat/  
💻 GitHub: https://github.com/almassifat  

---

## ⭐ Support

If you find this project helpful:
- ⭐ Star the repo  
- 🍴 Fork it  
- 🧠 Share feedback / improvements  
