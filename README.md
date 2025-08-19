# 🎵 Combining Graph Neural Network with Attention Mechanism in Sequence-Based Music Recommendation System  

Repositori ini merupakan bagian dari **Tugas Akhir** dengan judul:  
**Penggabungan Graph Neural Network dengan Attention Mechanism dalam Sistem Rekomendasi Musik Berbasis Urutan**  
(*Combining Graph Neural Network with Attention Mechanism in Sequence-Based Music Recommendation System*).  

---

## 📖 Ringkasan Penelitian  

Penelitian ini berfokus pada pengembangan **sistem rekomendasi musik berbasis urutan** dengan mengombinasikan **Graph Neural Network (GNN)** dan **Attention Mechanism**.  

- **GNN** digunakan untuk membentuk pola urutan berdasarkan keterkaitan antar node (lagu, artis, album).  
- **Attention Mechanism** membantu menangkap preferensi **jangka pendek (short-term)**.  
- Preferensi **jangka panjang (long-term)** dan **dinamis (dynamic preference)** juga dipertimbangkan dalam model.  
- Model ini merupakan pengembangan dari **Graph-Based Attentive Sequential Model (GASM)** dengan penyesuaian untuk dataset berskala lebih besar.  

---

## 📂 Dataset  

Dataset yang digunakan adalah **Music4All**, yang berisi informasi interaksi pengguna dengan musik dalam jumlah besar, mencakup:  
- Metadata lagu (judul, artis, album).  
- Riwayat interaksi pengguna (urutan pemutaran lagu).  

---

## 🎯 Kontribusi Penelitian  

1. Mengadaptasi model **GASM** untuk diterapkan pada dataset skala besar.  
2. Mengombinasikan **Graph Neural Network + Attention Mechanism** untuk menangkap preferensi pengguna secara lebih akurat.  
3. Melakukan **evaluasi ekstensif** melalui:  
   - Perbandingan skenario model.  
   - Hyperparameter tuning.  
   - Benchmarking terhadap baseline model rekomendasi.  

---

## 🛠️ Metodologi Singkat  

1. **Preprocessing Data**  
   - Pembentukan metadata dan historis mendengarkan.
   - Seleksi data untuk memadatkan data
   - Pembentukan sequence berdasarkan interaksi pengguna.  

2. **Modeling**  
   - Representasi graph dari interaksi musik.  
   - Penerapan GNN untuk sequence modeling.  
   - Penambahan Attention Mechanism untuk preferensi short-term.
   - Preferensi lainnya dibentuk dengan long-term dan dynamic.

3. **Evaluasi**  
   - Digunakan metrik seperti **Hitrate@K dan MRR@K**.
   - Skenario model untuk mengetahui pengaruh preferensi pada hasil rekomendasi
   - Hyperparameter tuning untuk mengetahui parameter yang optimal.
   - Perbandingan hasil dengan baseline model rekomendasi.  
git clone https://github.com/username/nama-repo.git
cd nama-repo
