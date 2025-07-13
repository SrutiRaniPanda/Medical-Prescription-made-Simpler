# 🩺 Medical Prescription Reader & Simplifier

A Python-based tool to **automatically read handwritten or scanned medical prescriptions**, extract essential medical details, and **convert them into simple, patient-friendly instructions** — especially for elderly, rural, or non-English speakers.

---

## 🧭 Project Goal

To simplify the often complex format of prescriptions by:
- Automatically extracting medicine names, dosages, and timings
- Interpreting medical shorthand (e.g., "1-0-1", "SOS")
- Providing output in clear, understandable, and multilingual format

---

## 🔄 Workflow

```text
1. Upload Prescription (Image/Text)
          ↓
2. OCR (Tesseract-based)
          ↓
3. Text Cleaning & Preprocessing
          ↓
4. NLP Analysis (NER + Regex)
          ↓
5. Plain Language Conversion
          ↓
6. Multilingual Output (Hindi, Marathi, etc.)
          ↓
7. Display/Download Summary
````
## 🧪 Key Components Implemented

### 🔍 OCR Processing

* Preprocessing: grayscale, thresholding, noise reduction
* Optimized **Tesseract OCR** for medical handwriting and scanned images

### 💬 NLP Analysis

* Regex-based detection of dosage patterns (e.g., `1-0-1`)
* Named Entity Recognition for drug names
* Abbreviation handling: OD, BD, SOS, etc.

### 🗣 Plain Language Conversion

* Shorthand → Full sentence (e.g., "1-0-1 after food" → "Take 1 tablet in the morning and 1 at night after meals")

### 🌐 Multilingual Support

* Supports **11 Indian languages** using `googletrans`
* Ideal for **non-English speaking patients**

### 📤 Download & Share

* **PDF reports** with clear formatting
* **Text files** for mobile compatibility
* Share via WhatsApp for easy access

### ✅ Enhanced User Experience

* Prompts for patient name and language
* Progress indicators during processing
* Auto-downloads reports in Colab

---

## 💻 How to Use in Google Colab

1. Open Google Colab

2. Paste the full code in a new notebook

3. Run the cell — it will:

   * Install dependencies
   * Set up Tesseract OCR
   * Launch the processor

4. Upload your prescription image

5. Enter patient details + language preference

6. Automatically download the simplified report

---

## 🛠 Setup Instructions (for local use)

### 🔧 Install Dependencies

```bash
pip install streamlit opencv-python pillow pytesseract spacy googletrans==4.0.0-rc1 pandas reportlab
python -m spacy download en_core_web_sm
```

### 🔧 Install Tesseract OCR

* **Windows**: [Download here](https://github.com/tesseract-ocr/tesseract/releases)
* **Linux**: `sudo apt-get install tesseract-ocr`
* **Mac**: `brew install tesseract`

### ▶️ Run Script

```bash
streamlit run prescription_reader.py
```

---

## 📦 Advanced Capabilities

* ✅ Regex for `1-0-1`, `2x daily`, `OD`, `SOS`, `TID`, `HS`, etc.
* ✅ Preprocessing pipeline (denoising, thresholding)
* ✅ 40+ Medical abbreviations handled
* ✅ Multilingual translation via `googletrans`
* ✅ PDF/text export with patient details

---

## 🧑‍💻 Author

**Sruti Rani Panda**
B.Tech, ECE | NIT Goa
[GitHub Profile](https://github.com/SrutiRaniPanda)


```
