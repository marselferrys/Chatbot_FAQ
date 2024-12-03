# Chatbot FAQ Asrama ITERA

Proyek ini bertujuan untuk membangun *chatbot* FAQ (Frequently Asked Questions) bagi Asrama ITERA dengan menggunakan dua algoritma pembelajaran mesin, yaitu Long Short-Term Memory (LSTM) dan Naive Bayes. Proyek ini dilakukan sebagai bagian dari tugas besar mata kuliah **Pengolahan Bahasa Alami (Natural Language Processing)**. 

### **Tujuan**
Mengevaluasi kinerja algoritma **LSTM** dan **Naive Bayes** dalam menjawab pertanyaan berbasis *dataset* FAQ mahasiswa, dengan fokus pada akurasi, presisi, *recall*, dan F1-score untuk menentukan algoritma yang paling sesuai untuk implementasi.

---

## **Tahapan Proyek**
Proyek ini menggunakan pendekatan CRISP-DM (*Cross Industry Standard Process for Data Mining*) yang mencakup beberapa tahap berikut:

1. **Business Understanding**  
   Merancang chatbot FAQ untuk menjawab pertanyaan yang sering diajukan mahasiswa terkait Asrama ITERA. Dataset diambil dari situs web resmi asrama ITERA: [https://asrama.itera.ac.id/](https://asrama.itera.ac.id/).

2. **Data Understanding**  
   Mengumpulkan dataset berbasis pertanyaan umum yang diekstraksi dan diolah dari data asrama.

3. **Data Preparation**  
   Melakukan *preprocessing* pada dataset menggunakan teknik:
   - *Case folding*
   - *Filtering*
   - *Tokenization*
   - *Stopword removal*
   - *Stemming*

4. **Modeling**  
   Dua algoritma digunakan untuk membangun *chatbot*:
   - **LSTM** menggunakan arsitektur Bidirectional LSTM.
   - **Naive Bayes** menggunakan model berbasis *TF-IDF vectorizer*.

5. **Evaluation**  
   Model dievaluasi berdasarkan metrik: 
   - Akurasi
   - Presisi
   - *Recall*
   - F1-Score

6. **Deployment**  
   Menggunakan **Streamlit** untuk membuat antarmuka demo prototipe *chatbot*.

---

## **Teknologi yang Digunakan**
- **Bahasa Pemrograman**: Python
- **Pustaka**: 
  - TensorFlow
  - scikit-learn
  - pandas, numpy
  - Streamlit

---

## **Struktur Proyek**
```plaintext
Chatbot_FAQ/
├── Folder_LSTM/
│   ├── BILSTM_model.h5            # Model Bidirectional LSTM
│   ├── CHATBOT_LSTM.ipynb         # Notebook untuk pelatihan dan pengujian LSTM
│   ├── label_encoder.pickle       # Label encoder
│   ├── max_sequence_length.txt    # Panjang maksimum urutan input
│   ├── tokenizer.pickle           # Tokenizer untuk preprocessing teks
│
├── Folder_Naive_Bayes/
│   ├── CHATBOT_NAIVE_BAYES.ipynb  # Notebook untuk pelatihan dan pengujian Naive Bayes
│   ├── label_encoder.pkl          # Label encoder
│   ├── naive_bayes_model.pkl      # Model Naive Bayes
│   ├── tfidf_vectorizer.pkl       # TF-IDF Vectorizer
│
├── README.md                      # Dokumentasi proyek
├── requirements.txt               # Daftar pustaka yang diperlukan
└── app.py                         # aplikasi streamlit
