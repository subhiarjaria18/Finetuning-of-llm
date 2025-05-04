# Finetuning-of-llm
multi modal

# 🔧 Fine-Tuning IDEFICS 9B on Pokémon Go Cards

This project demonstrates fine-tuning the **IDEFICS 9B** vision-language model on a custom **Pokémon Go card dataset** to enhance its performance in **visual question answering (VQA)**.

---

## 🧠 Why Fine-Tune?

The base IDEFICS model is trained for general multimodal tasks. Fine-tuning it on Pokémon Go cards helps the model:

- Better understand **card-specific layouts and designs**
- Accurately answer **questions related to card content**
- Adapt to **domain-specific vocabulary** and formats

---

## 🛠️ How It Was Done

- ✅ **Model**: [IDEFICS 9B](https://huggingface.co/HuggingFaceM4/idefics-9b)
- ⚙️ **Fine-Tuning Method**: [PEFT (LoRA)](https://github.com/huggingface/peft)
- 📉 **Quantization**: 4-bit using `bitsandbytes`
- 💾 **Platform**: Google Colab
- 📚 **Frameworks**:
  - Hugging Face Transformers
  - PEFT
  - Datasets
  - Torch + CUDA

---

## 📁 Dataset Format

Each example includes:
```json
{
  "image": "path/to/image.jpg",
  "question": "What is the Pokémon's attack power?",
  "answer": "120"
}
