# DLAssigment2
# Hindi Transliteration using Sequence-to-Sequence Model (PyTorch)

This project implements a sequence-to-sequence (seq2seq) model for transliterating Latin-script Hindi words into Devanagari script using PyTorch.

It includes:
- A character-level encoder-decoder architecture (GRU, LSTM, or RNN).
- Teacher forcing during training.
- Greedy decoding during inference.
- Accuracy evaluation and sample predictions.

---

## 📁 File Structure

- `DLassignment2.ipynb`: Jupyter notebook with full implementation.
- `hi.translit.sampled.dev.tsv`: Validation data (3-column TSV file: Devanagari, Latin, frequency).

---

## 🧠 Model Overview

The model consists of:
- **Encoder**: Converts input Latin characters to hidden states.
- **Decoder**: Generates Devanagari characters one by one.
- **Training loop**: Includes gradient clipping and optional teacher forcing.
- **Evaluation**: Measures character-level accuracy.
- **Prediction**: Uses greedy decoding to generate sequences.

---

## 🔧 Requirements

Install dependencies with pip:

```bash
pip install torch numpy
🗃️ Data Format
The input .tsv file should have lines in the format:

php-template
Copy
Edit
<devanagari_word>    <latin_word>    <frequency>
Each line is duplicated based on frequency for training balance.

🚀 How to Run
Place the validation file at: /content/hi.translit.sampled.dev.tsv

Open DLassignment2.ipynb in Jupyter or Google Colab.

Run all cells to:

Load and preprocess data

Train the model (if training code is added)

View predictions

✅ Sample Output
yaml
Copy
Edit
Input: namaste | Target: नमस्ते | Predicted: नमस्ते
Input: dilli   | Target: दिल्ली | Predicted: दिल्ली
...
✍️ Author
Add your name and contact info here.

📜 License
You can add a license like MIT, Apache, etc. depending on your use case.

yaml
Copy
Edit

---

Let me know if you want me to generate the actual file for download or customize it for something like LSTM
# 🎤 GPT-2 Lyric Generator (Fine-tuned on Khalid & Lady Gaga)

This project fine-tunes OpenAI's GPT-2 model to generate lyrics in the style of Khalid and Lady Gaga using Hugging Face's `transformers` and `datasets` libraries.

---

## 🧠 Project Overview

We:
- Collected lyrics from Khalid and Lady Gaga.
- Cleaned and prepared the data for training.
- Fine-tuned a pre-trained GPT-2 language model.
- Used the model to generate lyrics based on a given prompt.

---

## 🗂️ Files

- `DLassignment2.ipynb`: Main notebook containing code for data preprocessing, training, and generation.
- `Khalid_chintu.csv`, `LadyGaga_chintu.csv`: Source CSV files with lyrics.
- `lyrics_dataset.txt`: Cleaned and combined dataset used for training.
- `./gpt2-lyrics/`: Folder where fine-tuned model checkpoints are saved.

---

## 🔧 Setup

### Install dependencies

```bash
pip install transformers datasets pandas


📄 Data Format
Each CSV file should have a Lyric column, e.g.:

csv
Copy
Edit
Lyric
I remember those nights when...
Cause baby you're a firework...
🧼 Data Cleaning
Lyrics are:

Lowercased and stripped of smart quotes.

Non-ASCII characters and special symbols are removed.

Combined into a .txt format for language model training.

🚀 Training the Model
The script uses GPT2LMHeadModel for language modeling.

The Trainer API is used for efficient training.

Training runs for 3 epochs with batch size 2 (can be modified).

python
Copy
Edit
trainer.train()
🎶 Generate Lyrics
Use the fine-tuned model to generate lyrics:

python
Copy
Edit
generator("I remember those nights when", max_length=100)[0]["generated_text"]
Example output:

css
Copy
Edit
I remember those nights when I was so lost in the dark,
Waiting on a spark...
📍 Notes
The tokenizer's pad token is set to eos_token to avoid padding errors.

Use GPU (if available) for faster training (cuda).

This model is best for fun/creative generation, not production.

✍️ Author
Add your name and contact/email here.

📜 License
You may add an open-source license (MIT, Apache 2.0, etc.)

yaml
Copy
Edit

---

Let me know if you'd like me to:
- Combine this with the Question 1 README.
- Export both README files.
- Add badges, demo images, or Colab links for a more complete GitHub project look.
