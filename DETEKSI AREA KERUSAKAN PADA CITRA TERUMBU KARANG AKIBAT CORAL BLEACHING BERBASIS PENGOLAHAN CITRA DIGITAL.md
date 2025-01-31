# **DETEKSI AREA KERUSAKAN PADA CITRA TERUMBU KARANG AKIBAT CORAL BLEACHING BERBASIS PENGOLAHAN CITRA DIGITAL**
# **Nama: Alma Choerunisa, Muhammad Ilman Maulana Hasan**  
# **NPM: 2206083, 2206118**
**Institut Teknologi Garut, Jawa Barat, Indonesia**

**2206083@itg.ac.id**

**2206118@itg.ac.id**

## **1. Pendahuluan**  
### **1.1 Latar Belakang**  
Terumbu karang adalah ekosistem laut yang memiliki peran penting dalam menjaga keseimbangan kehidupan laut. Namun, pemanasan global dan aktivitas manusia menyebabkan pemutihan karang (*coral bleaching*), yaitu kondisi di mana karang kehilangan alga simbionnya akibat stres lingkungan. Proses ini dapat menyebabkan kematian karang secara massal jika tidak segera ditangani.  

Pemantauan terumbu karang secara manual memerlukan waktu dan tenaga yang besar. Oleh karena itu, metode berbasis pengolahan citra digital menjadi solusi yang efektif untuk mendeteksi area pemutihan dengan cepat dan akurat.  

### **1.2 Penelitian atau Teori Terkait**  
Penelitian sebelumnya telah membahas penggunaan berbagai teknik pengolahan citra, seperti segmentasi berbasis warna dan analisis morfologi, dalam mendeteksi area pemutihan karang. Studi oleh **Smith et al. (2020)** menunjukkan bahwa pemrosesan citra digital dapat memberikan estimasi area bleaching dengan akurasi tinggi. Teknik pengolahan citra berbasis HSV (Hue, Saturation, Value) sering digunakan untuk mendeteksi warna putih sebagai indikasi pemutihan.  

### **1.3 Tujuan Tugas**  
Proyek ini bertujuan untuk:  
- Mengembangkan sistem deteksi otomatis untuk mengidentifikasi area bleaching pada citra terumbu karang.  
- Menggunakan pengolahan citra digital untuk menghitung persentase area yang mengalami pemutihan.  
- Memvisualisasikan hasil deteksi bleaching agar dapat digunakan untuk pemantauan ekosistem laut.  

---

## **2. Metode**  
### **2.1 Langkah-langkah yang Dilakukan**  
1. **Pengumpulan Dataset**  
   - Dataset berisi gambar terumbu karang yang diambil dari berbagai sumber.  
2. **Pra-Pemrosesan Citra**  
   - Konversi citra ke format RGB.  
   - Konversi ke HSV untuk mendeteksi warna putih sebagai indikasi bleaching.  
3. **Segmentasi Area Bleaching**  
   - Menerapkan batas nilai HSV untuk mengekstrak area putih.  
   - Menggunakan operasi morfologi untuk menghilangkan noise.  
4. **Perhitungan Persentase Bleaching**  
   - Menghitung jumlah piksel yang terdeteksi sebagai bleaching.  
   - Menghitung rasio terhadap total piksel gambar.  
5. **Visualisasi Hasil**  
   - Menampilkan gambar asli, area bleaching, dan hasil pasca-morfologi.  

### **2.2 Visualisasi Model**  
#### **Tahap - tahap dan deskirpsi model**  
Berikut adalah tahapan pemrosesan citra yang dilakukan:  

| **Tahap** | **Deskripsi** |
|-----------|-------------|
| **1. Input Gambar** | Gambar terumbu karang dimasukkan ke dalam sistem |
| **2. Konversi ke RGB** | Mengubah format gambar ke RGB untuk analisis warna |
| **3. Konversi ke HSV** | Mengubah format gambar ke HSV untuk segmentasi warna |
| **4. Deteksi Warna Putih** | Menerapkan thresholding pada kanal HSV untuk mengekstrak area putih |
| **5. Operasi Morfologi** | Menghilangkan noise dengan operasi morfologi (closing & opening) |
| **6. Perhitungan Persentase** | Menghitung jumlah piksel bleaching dibandingkan total piksel |
| **7. Visualisasi Hasil** | Menampilkan gambar hasil deteksi bleaching |

---

## **3. Hasil**  
Eksperimen dilakukan pada dataset citra terumbu karang. Berikut hasil yang diperoleh:  

### **Contoh hasil analisis untuk salah satu gambar:**  

| Nama Gambar  | Citra Input (RGB) | Mask Area Bleaching | Citra Hasil Morfologi | Persentase Bleaching |
|-------------|----------------|-----------------|-----------------|---------------------|
| **koral1.jpg** | ![koralori](https://github.com/user-attachments/assets/60588c7a-a703-435a-9c49-f25c3f9ae7e2) | ![koral](https://github.com/user-attachments/assets/94c92fc1-1194-4ced-bd50-e5cd1af56b32) | ![korall](https://github.com/user-attachments/assets/c1c85192-e034-4d35-b2eb-cd3820df3245) | **02.09%** |
| **koral2.jpg** | ![image](https://github.com/user-attachments/assets/f09027a6-9350-4d49-b333-5edc12ed3f81) | ![image](https://github.com/user-attachments/assets/91b3d9c2-2d94-4c7b-99fa-c78cf04459a0) | ![image](https://github.com/user-attachments/assets/2166dcf5-9388-46eb-b829-a05e507d26e1) | **21.55%** |
| **koral3.jpg** | ![image](https://github.com/user-attachments/assets/d94ae16e-b975-4976-aadd-9908e1b7a40a) | ![image](https://github.com/user-attachments/assets/b7105190-f771-487e-b606-81c53cf5c099) | ![image](https://github.com/user-attachments/assets/a723cae9-805e-45c4-8360-80e62baf3cfd) | **05.37%** |
| **koral4.jpg** | ![image](https://github.com/user-attachments/assets/a35e8009-e215-45ad-b3d9-bfe5df978b0c) | ![image](https://github.com/user-attachments/assets/bd610395-a8ae-4a9c-98cb-e90b6946b2ba) | ![image](https://github.com/user-attachments/assets/a2da9465-d74e-47d9-b7f5-d40585dd22b5) | **01.08%** |
| **koral1.jpg** | ![image](https://github.com/user-attachments/assets/fabefc58-54a8-40da-9e72-83dc68136524) | ![image](https://github.com/user-attachments/assets/18415a19-9a27-4d25-b2f7-57563ad9c9e9) | ![image](https://github.com/user-attachments/assets/42b2aa5c-9472-4aac-916e-74450220f534) | **05.22%** |

Dari hasil di atas, gambar **"koral2.jpg"** memiliki tingkat bleaching tertinggi, yang menandakan bahwa area tersebut mengalami kerusakan paling parah.  

---

## **4. Kesimpulan**  
### **4.1 Ringkasan Temuan**  
- Sistem berbasis pengolahan citra digital berhasil mendeteksi area bleaching dengan akurat.  
- Pendekatan berbasis HSV efektif dalam mengidentifikasi area putih pada citra terumbu karang.  
- Operasi morfologi meningkatkan akurasi deteksi dengan mengurangi noise pada hasil segmentasi.  

### **4.2 Batasan Pekerjaan**  
- Dataset yang digunakan masih terbatas dan perlu diperluas untuk meningkatkan akurasi model.  
- Kondisi pencahayaan dan kualitas gambar mempengaruhi hasil deteksi.  
- Warna putih yang bukan bagian dari bleaching dapat terdeteksi sebagai false positive.  

### **4.3 Rekomendasi untuk Pekerjaan di Masa Depan**  
- Menggunakan teknik deep learning untuk meningkatkan akurasi deteksi.  
- Menambahkan fitur deteksi warna lain seperti hijau dan coklat untuk membedakan antara bleaching dan karang sehat.  
- Mengembangkan aplikasi berbasis web atau mobile untuk memudahkan pemantauan terumbu karang secara real-time.  
