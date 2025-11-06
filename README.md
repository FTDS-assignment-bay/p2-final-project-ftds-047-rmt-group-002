# 💼 SkillMatch

<div style="text-align: center;">
    <img src="logo.png" alt="SkillMatch Preview" width="500">
</div>

Lagi bingung cari kerja yang cocok sama kemampuanmu? Tenang, kamu nggak sendiri!  

Di **SkillMatch**, kamu bisa menemukan pekerjaan yang pas banget sama skill dan minatmu. Nggak perlu scroll ratusan lowongan, tinggal tunjukin keahlianmu, dan biar kami bantu temuin kerjaan yang paling cocok buat kamu.  

✨ Temukan pekerjaan yang sesuai dengan skillmu di sini!

---

## 🌐 Try it Online

Coba aplikasi **SkillMatch** secara langsung di browser kamu:  
[🔗 Akses SkillMatch](https://huggingface.co/spaces/Annisa123/job_recomendation)

---

## 🎯 Problem Background

💡 Banyak pencari kerja memiliki keahlian luar biasa, namun sering kali kesulitan menemukan pekerjaan yang benar-benar sesuai dengan kemampuan mereka.
Melalui SkillMatch, sistem rekomendasi berbasis AI yang memanfaatkan Natural Language Processing (NLP) dan TF-IDF, pengguna dapat menemukan lowongan yang paling relevan dengan keterampilan mereka.

🌍 SkillMatch hadir sebagai jembatan antara skill dan opportunity, dengan menganalisis deskripsi pekerjaan dari berbagai industri untuk membantu setiap individu menemukan pekerjaan yang sesuai dengan potensinya.

---

## 🚀 Project Output

✨ **SkillMatch** menghasilkan sistem rekomendasi pekerjaan interaktif berbasis web yang mampu:  

- Menganalisis kemampuan pengguna dan mencocokkannya dengan deskripsi pekerjaan yang relevan.  
- Mengukur tingkat kemiripan antara input pengguna dan lowongan kerja menggunakan Cosine Similarity.  
- Memberikan hasil rekomendasi beserta tautan pekerjaan asli dari LinkedIn.  
- Melakukan analisis topik pekerjaan menggunakan FASTopic Clustering untuk mengelompokkan jenis pekerjaan berdasarkan pola teks.  

---

## 📊 Data Overview

**Deskripsi singkat:**  
Dataset berisi kumpulan lowongan pekerjaan hasil scraping dari **LinkedIn**, mencakup:  

- Nama perusahaan  
- Lokasi  
- Posisi pekerjaan  
- Deskripsi pekerjaan  
- URL sumber lowongan  

| No | Kolom             | Deskripsi                   |
|----|-----------------|----------------------------|
| 1  | company_name     | Nama perusahaan            |
| 2  | job_location     | Domisili Perusahaan        |
| 3  | job_title        | Posisi pekerjaan           |
| 4  | job_description  | Deskripsi pekerjaan        |
| 5  | job_url          | Tautan ke halaman lowongan |

**Langkah Preprocessing:**  
1. Menghapus duplikat dan nilai kosong  
2. Menyaring data berbahasa Inggris  
3. Membersihkan teks (case folding, stopwords removal, lemmatization)  
4. Mengubah teks menjadi representasi numerik menggunakan **TF-IDF Vectorizer**

---

## ⚙️ Methodology

Proyek ini menggunakan pendekatan berbasis **Content-Based Filtering** melalui **Machine Learning (NLP)**.  

**Langkah-langkah utama:**  
1. **Web Scraping** – Mengambil data dari LinkedIn menggunakan Selenium  
2. **Data Validation** – Menggunakan *Great Expectations* untuk menjaga kualitas data  
3. **Text Preprocessing** – Pembersihan dan normalisasi teks deskripsi pekerjaan  
4. **TF-IDF Vectorization** – Mengubah teks menjadi bentuk numerik  
5. **Cosine Similarity** – Mengukur tingkat kesamaan antara skill pengguna dan deskripsi pekerjaan  
6. **FASTopic Clustering** – Mengelompokkan pekerjaan berdasarkan topik  
7. **Web Deployment** – Implementasi sistem rekomendasi dalam aplikasi web interaktif

---

## 🧩 Tech Stack

**💻 Bahasa Pemrograman & Tools:**  
- Python  
- Jupyter Notebook  
- Streamlit (untuk web app)  

**📚 Library Utama:**  
- `pandas`, `numpy` – Manipulasi data  
- `nltk`, `re`, `string` – Preprocessing teks  
- `scikit-learn` – TF-IDF & Cosine Similarity  
- `matplotlib`, `seaborn`, `WordCloud` – Visualisasi  
- `FASTopic` – Topic Clustering  
- `Great Expectations` – Validasi data

---

## 🎨 Future Improvement
- Integrasi model BERT/Sentence Transformers untuk rekomendasi yang lebih kontekstual dan akurat.
- Analisis keterampilan otomatis dari CV/resume pengguna untuk mempermudah input skill.
- Dashboard interaktif untuk visualisasi tren pekerjaan, misal: job demand per industri, skill populer.
- Pengembangan mobile-friendly UI agar bisa diakses dari smartphone dengan nyaman.
- Sistem feedback pengguna untuk meningkatkan akurasi rekomendasi (misal thumbs up/down pada rekomendasi pekerjaan).
- Keamanan & privasi data – implementasi enkripsi dan anonymisasi data pengguna.
- Multi-language support – menambahkan dukungan bahasa Indonesia atau bahasa lain agar lebih inklusif.

---

## 📚 Reference

- LinkedIn Job Portal – Cek lowongan langsung di [LinkedIn Jobs](https://www.linkedin.com/jobs)  
- scikit-learn Docs – Panduan TF-IDF & Cosine Similarity di [scikit-learn Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html)  
- Great Expectations – Framework buat validasi data, liat di [Great Expectations Docs](https://docs.greatexpectations.io/docs/home/)  
- FASTopic – Untuk clustering topik pekerjaan, info lengkap di [FASTopic PyPI](https://pypi.org/project/fastopic/) 

---

## 🌟 Contributors

| Name       | LinkedIn |
|------------|----------|
| Annisa Herliansyah | [🔗 Connect](https://www.linkedin.com/in/annisa-herliansyah-1a8257287/) |
| Aqib Abdul Aziz | [🔗 Connect](https://www.linkedin.com/in/aqib-az/) |
| Muhammad Alwi Rifqi | [🔗 Connect](https://www.linkedin.com/in/m-alwirifqi/) |
| Wesley Hakim | [🔗 Connect](https://www.linkedin.com/in/wesley-hakim/) |
---
## 📝 Berikan Masukan Anda
Silakan klik tautan berikut:  
[💬 Isi Formulir Feedback](https://forms.gle/aJnEeBsktNnLJBrL9)  

Terima kasih telah mencoba **SkillMatch**! 😊  
Setiap saran dan masukan Anda akan sangat berarti bagi pengembangan SkillMatch ke depannya. Terima kasih atas partisipasinya. 🙏✨

---

> ✨ *“Membantu setiap individu menemukan pekerjaan yang sesuai dengan potensinya.”*  
> 🛠️ Built with love by **Group 2** - **RMT047** for data-driven solutions.