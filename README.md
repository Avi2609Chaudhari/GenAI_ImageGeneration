# 🎨 Text-to-Image Generation using CLIP & VQGAN (Custom Multimodal Model)

This project focuses on **generating images from text prompts** using a combination of **CLIP** (for text–image semantic understanding) and **VQGAN / Taming Transformer** (for generating high-quality images).  
The entire system works **offline without any API keys**, making it fully open-source and customizable.

> ⚡ **Recommended Hardware:** This project is optimized for running on an **NVIDIA T4 GPU** (such as Google Colab T4).  
Running on CPU is possible but extremely slow.

---

## ⚙️ Features
- Generate images from user prompts using custom multimodal architecture  
- Works completely **offline**, no API key required  
- Combines the power of:  
  - 🧠 **CLIP (Text–Image similarity model)**  
  - 🖼️ **VQGAN (Image generator using discrete latent space)**  
- Customizable generation settings (iterations, learning rate, augmentations)  
- Notebook-based interface for easy experimentation  
- **Optimized for GPU (T4 recommended)** to significantly speed up image generation  

---

## 🤖 Models Used
- **CLIP (Contrastive Language–Image Pretraining)**  
  - Used to evaluate how well an image matches the text prompt  
- **VQGAN (Vector Quantized GAN)**  
  - Generates high-quality images from learned latent codes  
- **Taming Transformers**  
  - Framework enabling transformer-based image generation  
- **Optimization Loop**  
  - Iteratively updates the latent representation to satisfy CLIP’s guidance  

---

## 🧠 Workflow
- **Model Loading:** Load CLIP + VQGAN weights locally  
- **Latent Initialization:** Start with a random latent representation  
- **Optimization:**  
  - Decode image using VQGAN  
  - Evaluate similarity score using CLIP  
  - Backpropagate loss to update latent vector  
- **Image Generation:** Best-matching images are produced after iterations  
- **User Interaction:** Modify prompt, sampling steps, resolution, etc.  

---

## 🖥️ Tech Stack
- **Programming Language:** Python  
- **Environment:** Google Colab  
- **Hardware:**  
  - ⚡ **NVIDIA T4 GPU (Recommended)**  
  - CUDA-enabled environment for faster execution  
- **Libraries:**  
  - PyTorch  
  - CLIP  
  - Taming Transformers  
  - Pillow  
  - NumPy  
  - OmegaConf  

---
