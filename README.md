<div align=center>

# Probability And Statistics - ANOVA (Analysis of Variance)

## Kelompok 11

|    NRP     |      Name               |
| :--------: | :---------------------: |
| 5025221038 |Rafli Syahputra Pane     |
| 5025221052 | M. Syarif Hidayatullah  |
| 5025221101 | Lalu Aldo Wadagraprana  |
| 5025221174 | Aloyisius deDeo Darmo S.|


</div>

# 📊 Introduction to ANOVA (Analysis of Variance)

Analisis Variansi (ANOVA) merupakan uji statistik yang sangat penting dan banyak digunakan dalam berbagai bidang penelitian, termasuk di antaranya kedokteran dan pertanian. Dalam artikel ini, kita akan membahas kapan ANOVA digunakan, gagasan dasar di balik ANOVA (yakni bagaimana variansi digunakan untuk menarik kesimpulan tentang rata-rata kelompok), serta ANOVA satu arah (one-way ANOVA). 


---

## 🔍 Apa itu ANOVA?

**ANOVA** (Analysis of Variance) adalah metode statistik untuk menguji **perbedaan rata-rata** dari dua atau lebih kelompok. Kalau kamu hanya punya dua kelompok, cukup gunakan t-test. Tapi kalau tiga atau lebih? Nah, saat itulah ANOVA jadi metode utama.

---

## 🎯 Kapan Menggunakan ANOVA?

Jika kamu sedang membaca artikel ini, kemungkinan besar kamu sudah cukup familiar dengan konsep pengujian hipotesis dan uji t (t-test). Namun, jika konsep-konsep tersebut masih terasa baru, jangan khawatir—kamu akan memahaminya seiring kita menggali lebih dalam dalam artikel ini.

Uji t memang cocok digunakan untuk membandingkan rata-rata dua kelompok. Tapi, bagaimana jika kamu memiliki tiga kelompok atau lebih? Nah, di sinilah Analisis Variansi (ANOVA) menjadi alat yang sangat diperlukan.

Bayangkan kamu adalah seorang peneliti medis dan sedang menguji tiga jenis obat berbeda—sebut saja A, B, dan C—untuk menangani suatu penyakit, misalnya penyakit XYZ. Sekarang, kamu ingin mengetahui apakah ada perbedaan nyata dalam efektivitas ketiga obat tersebut terhadap penyakit XYZ. Apa yang harus kamu lakukan? Kamu harus menggunakan ANOVA.
Kalau hanya ada dua jenis obat, misalnya A dan B, maka uji t sudah cukup. Tapi ketika ada lebih dari dua kelompok yang ingin dibandingkan, maka pilihan yang tepat adalah ANOVA.

Gunakan ANOVA saat ingin membandingkan rata-rata dari lebih dari dua populasi.

Gunakan juga ANOVA jika ingin membandingkan populasi yang masing-masing memiliki beberapa level atau subkelompok.

![pic1](https://github.com/user-attachments/assets/62bc7216-b833-40f4-95cf-6ecbc4a77163)

Di sini, x̄₁, x̄₂, x̄₃ adalah rata-rata dari sampel a, b, dan c.

Setiap sampel memiliki rata-rata dan distribusinya sendiri.

Yang ingin kita cari tahu adalah:

- Apakah semua rata-rata sampel tersebut berasal dari populasi yang sama?
- Apakah salah satu rata-rata berbeda sangat jauh dari dua lainnya sehingga kemungkinan besar tidak berasal dari populasi yang sama?
- Atau, apakah ketiga rata-rata itu sangat berbeda sehingga tampak berasal dari populasi yang berbeda-beda?

Dengan kata lain, kita sedang membahas **jarak relatif antar rata-rata** tersebut.

Mungkin kamu bertanya-tanya, *kenapa disebut analisis variansi (analysis of variance)* kalau sebenarnya kita ingin membuat keputusan tentang rata-rata? Nanti kamu akan memahami jawabannya.

Untuk sekarang, mari kita fokus pada **jarak antar rata-rata**.

Berdasarkan ilustrasi dan penjelasan sebelumnya, anggap kita memiliki tiga sampel (a, b, dan c) dengan rata-rata masing-masing x̄₁, x̄₂, x̄₃.

Jika seluruh data dari ketiga sampel tersebut kita gabungkan menjadi satu, maka kita akan membentuk sebuah **distribusi gabungan** yang lebih besar.

Distribusi ini kira-kira akan terlihat seperti gambar yang ditunjukkan berikutnya.

![pic2](https://github.com/user-attachments/assets/b83882ff-2cb6-4773-82a8-c33d4f663c1f)

Kurva distribusi besar yang berada di belakang distribusi dari ketiga sampel tersebut merupakan **populasi gabungan** yang terbentuk dari penggabungan semua data dari sampel a, b, dan c.

Garis putus-putus di tengah menunjukkan **rata-rata dari populasi gabungan** tersebut.

![pic3](https://github.com/user-attachments/assets/35a722b3-3998-40d4-b86a-50deb6dbdd1f)

Sekarang, perhatikan gambar di atas (Gambar 3). **Rata-rata dari sampel pertama (x̄₁)** hampir tepat berada di atas **garis putus-putus**, yang merupakan rata-rata populasi gabungan.

Garis merah di bawah x̄₂ menunjukkan **jarak antara rata-rata sampel b (x̄₂)** dan rata-rata populasi (garis putus-putus).

Sementara itu, garis merah di atas distribusi berwarna hijau menunjukkan **jarak antara x̄₃ dan garis putus-putus**, yaitu rata-rata dari populasi besar yang terbentuk dari penggabungan ketiga sampel.

![pic4](https://github.com/user-attachments/assets/52d20cb6-23b9-4d3b-9e30-fda5b47c89d7)

Pada gambar ini, terlihat bahwa **rata-rata dari salah satu sampel (grafik berwarna hijau)** berada **cukup jauh dari garis putus-putus**, yang mengindikasikan bahwa sampel tersebut **kemungkinan besar tidak berasal dari populasi gabungan** tersebut.

Di sisi lain, **x̄₂ tidak terlalu jauh dari garis putus-putus**, sehingga masih memungkinkan berasal dari populasi yang sama.

![pic5](https://github.com/user-attachments/assets/3e7b08ad-9938-4cd3-9dff-65c1940d0d52)

Pada gambar ini, baik **x̄₂ maupun x̄₃** terlihat **terlalu jauh dari garis putus-putus**, sedangkan **x̄₁ tepat berada di atas garis tersebut**.

Dari situ, bisa dikatakan bahwa **x̄₂ dan x̄₃ tampaknya berasal dari distribusi populasi mereka masing-masing**, sementara **x̄₁ kemungkinan besar berasal dari populasi gabungan** (ditandai oleh garis biru dan garis putus-putus di latar belakang).

Dengan kata lain, **semakin jauh rata-rata sampel dari rata-rata populasi (di latar belakang)**, maka semakin besar kemungkinan bahwa sampel tersebut **berasal dari populasi yang berbeda**.

---

### 🧪 Hipotesis Nol (Null Hypothesis)

Dalam jenis permasalahan seperti ini, hipotesis nol yang diuji adalah:
```
H₀: μ₁ = μ₂ = μ₃
```
Artinya, rata-rata dari ketiga populasi yang diuji dianggap **sama** — atau dengan kata lain, **tidak ada perbedaan signifikan** di antara kelompok-kelompok tersebut.


Apakah ketiga rata-rata sampel tersebut berasal dari **populasi yang sama**?  
Itulah inti dari hipotesis nol yang diuji dalam ANOVA.

(Ingat: **rata-rata sampel adalah estimasi titik (point estimate)** dari rata-rata populasi.)

Jadi, **hipotesis nol (H₀)** secara tidak langsung menyatakan bahwa **ketiga rata-rata sampel tersebut berasal dari populasi yang sama**.

Yang diuji bukan apakah nilai rata-ratanya **sama persis**, tapi apakah mereka **berasal dari sumber populasi yang sama**.

---

### 🔁 ANOVA sebagai Rasio Variabilitas

Maka, pada akhirnya ANOVA adalah **rasio dari variabilitas antar kelompok terhadap variabilitas dalam kelompok**.


F = (Variabilitas Antar Kelompok) / (Variabilitas Dalam Kelompok)

### Variabilitas Antar dan Dalam Kelompok

**Variabilitas antar kelompok** menggambarkan **jarak atau perbedaan antara rata-rata tiap sampel dengan rata-rata gabungan** (ditunjukkan oleh garis putus-putus pada gambar sebelumnya).

Seperti yang terlihat di ilustrasi, semakin besar jarak antara rata-rata sampel dengan rata-rata populasi gabungan, maka **tingkat tumpang tindih antar distribusi makin kecil**. Artinya, distribusi sampel semakin menjauh dari distribusi populasi utama (populasi yang terbentuk dari penggabungan ketiga sampel).

---

Sekarang, mari kita bahas tentang **variabilitas dalam kelompok**.  
Perhatikan gambar di bawah ini (yang dimaksud pada artikel aslinya).

![pic6](https://github.com/user-attachments/assets/19571e3f-1e97-48f9-8aba-daac58d81c23)

Bandingkan **penyebaran data (spread)** dari sampel-sampel pada dua gambar tersebut.

![pic7](https://github.com/user-attachments/assets/845895b3-4a5f-4db8-8560-963848dc7a2f)

Gambar pertama menunjukkan penyebaran yang relatif **sempit** dalam tiap kelompok, sedangkan gambar kedua menunjukkan **penyebaran yang lebih lebar**, artinya **variansi dalam kelompok meningkat**.

Semakin besar penyebaran dalam kelompok, semakin sulit untuk melihat perbedaan antar kelompok secara signifikan, karena data masing-masing kelompok menjadi semakin tumpang tindih.

Varians seperti ini, yang terjadi **di dalam masing-masing kelompok**, disebut sebagai **variabilitas dalam kelompok (within-group variability)**.

Sebelumnya, kita sudah bahas tentang **variabilitas antar kelompok**, yaitu perbedaan antara rata-rata tiap sampel dengan rata-rata populasi gabungan.

---

![pic8](https://github.com/user-attachments/assets/f556fdd9-7780-455d-8815-8ea630b16548)

Pada grafik ini, **garis-garis pada bagian pembilang (numerator)** mewakili **jarak antara rata-rata masing-masing sampel dengan rata-rata populasi gabungan**.

Sementara itu, **garis-garis pada bagian penyebut (denominator)** menunjukkan **penyebaran (variansi) dari masing-masing sampel itu sendiri**.

Jadi secara sederhana, **rasio ANOVA** bisa dipahami sebagai:

> **Jarak antar rata-rata** (antar kelompok)  
> dibagi dengan  
> **penyebaran dalam tiap kelompok**.

### Rumus Statistik F dalam ANOVA

F-statistic = Variance Between Groups / Variance Within Groups  
            = MSB / MSW

![image](https://github.com/user-attachments/assets/30dad886-dae4-495b-8887-2200091a4353)

Keterangan:
- **MSB** = Mean Square Between (varians antar kelompok)
- **MSW** = Mean Square Within (varians dalam kelompok)

Jadi, nilai F menunjukkan **seberapa besar variasi antar kelompok dibandingkan dengan variasi dalam kelompok**.
Semakin besar nilai F, semakin besar kemungkinan bahwa **setidaknya satu kelompok berbeda signifikan** dari yang lain.

Karena ANOVA merupakan **rasio dari variansi**, maka perhitungannya mengikuti **distribusi F (F-distribution)**.

Jika **variabilitas antar rata-rata** (pada pembilang) **jauh lebih besar** dibandingkan dengan **variabilitas dalam kelompok** (pada penyebut), maka **nilai F akan jauh lebih besar dari 1**.

Dalam kasus seperti itu, kemungkinan besar **sampel-sampel tersebut tidak berasal dari populasi yang sama**, sehingga kita dapat **menolak hipotesis nol** yang menyatakan bahwa semua rata-rata adalah sama.

Jadi secara sederhana, **ANOVA adalah rasio variabilitas antar kelompok terhadap variabilitas dalam kelompok**.

![pic9](https://github.com/user-attachments/assets/a363a6ca-e543-4203-958f-f4445847cfe4)

### Tiga Kondisi Umum Rasio Variabilitas dalam ANOVA

Perbandingan:

**Variabilitas Antar Kelompok**  / **Variabilitas Dalam Kelompok**

---

1. **Jika rasionya besar:**

**besar** / **kecil**

- Variabilitas antar kelompok: **besar**
- Variabilitas dalam kelompok: **kecil**

**Interpretasi:** Tolak H₀ (ada perbedaan yang signifikan antar rata-rata kelompok)

---

2. **Jika rasionya kecil:**

**kecil** / **kecil**

- Variabilitas antar kelompok: **kecil**
- Variabilitas dalam kelompok: **kecil**

**Interpretasi:** Jangan tolak H₀ (tidak ada bukti cukup bahwa kelompok berbeda)

---

3. **Jika rasionya sedang (intermediate):**

**similar** / **similarl**

- Variabilitas antar kelompok: **mirip**
- Variabilitas dalam kelompok: **mirip**

**Interpretasi:** Gagal menolak H₀ (tidak ada cukup bukti untuk menyimpulkan perbedaan)

---

### 🧪 Contoh Kasus: One-Way ANOVA

Sekarang, mari kita masuk ke jenis pertama dari ANOVA, yaitu **One-Way ANOVA**.

Sebagai contoh, misalkan ada **tiga jenis pakan** yang diberikan kepada sapi:

- 7 ekor sapi diberi **Pakan A**  
- 7 ekor sapi diberi **Pakan B**  
- 7 ekor sapi diberi **Pakan C**

Tujuannya adalah untuk mengetahui apakah terdapat **perbedaan hasil produksi susu** di antara ketiga kelompok tersebut.

Pertanyaan ini akan kita jawab menggunakan **one-way ANOVA**.

![image](https://github.com/user-attachments/assets/b8d91923-757f-4478-a7ac-1e8e70f78431)

Pada tabel di atas, kita memiliki **data observasi untuk masing-masing jenis pakan**, dan di bagian bawah terdapat **rata-rata (mean) untuk setiap kelompok**.

Sekarang, mari kita hitung **rata-rata gabungan (grand mean/G)**, yaitu rata-rata dari semua observasi yang digabungkan dari ketiga kelompok tersebut.

Hasilnya: **G = 74.52**

Kalau kita lihat rata-rata produksi susu dari masing-masing pakan, terlihat bahwa **Pakan A memiliki nilai yang relatif tidak normal** dibandingkan dengan Pakan B dan C.

---

Karena ANOVA adalah **analisis variasi**, maka kita perlu mengulas secara singkat konsep **varians**.

### 📏 Apa itu Varians?

**Varians** adalah **rata-rata dari selisih kuadrat antara tiap data dan rata-ratanya**.

Langkah-langkah menghitung varians:
1. Hitung jarak tiap data ke rata-ratanya.
2. Kuadratkan jarak tersebut.
3. Jumlahkan semua hasil kuadratnya.
4. Bagi dengan jumlah data untuk mendapatkan rata-rata dari kuadrat selisih tersebut.

---

**Rumus varians sampel (sample variance):**

```plaintext
s² = Σ (xᵢ − x̄)² / (n − 1)
```
![image](https://github.com/user-attachments/assets/446ca84f-60f1-476e-bbc4-37e50877b0f8)

xᵢ  = nilai data ke-i
x̄ = rata-rata sampel
n = jumlah data

Jika kita mengabaikan penyebut (denominator) dari rumus varians (karena hanya ingin menghitung jumlah total variasi), kita mendapatkan **Sum of Squares (SS)**, yaitu:

```plaintext
SS = Σᵢ₌₁ⁿ (xᵢ − x̄)²
```
![image](https://github.com/user-attachments/assets/06504cbf-eda1-4c8e-8430-bdaedc45a1e7)

### 🧮 Tiga Jenis Sum of Squares dalam One-Way ANOVA

Dalam ANOVA, khususnya **one-way ANOVA**, kita menggunakan **tiga jenis sum of squares (SS)** utama:

1. **SST** — *Total Sum of Squares*  
   → Mengukur **total variasi** dalam seluruh data.

2. **SSC** — *Sum of Squares Between Groups (Columns)*  
   → Mengukur **variasi antar kelompok** (perbedaan rata-rata antar grup).

3. **SSE** — *Sum of Squares Error (Within Groups)*  
   → Mengukur **variasi dalam kelompok** (penyebaran data dalam setiap grup).

---

Hubungannya dirumuskan sebagai:

```plaintext
SST = SSC + SSE
```

### 🔢 Cara Menghitung Total Sum of Squares (SST)

Untuk menghitung **SST (Total Sum of Squares)**, ikuti langkah-langkah berikut:

1. **Ambil selisih antara setiap nilai data (Xᵢ) dari semua grup** dengan **rata-rata keseluruhan (grand mean, G)**:  
   ```plaintext
   Xᵢ − G
   ```

2. Kuadratkan semua selisih tersebut:
  ```
  (Xᵢ − G)²
  ```
3. Jumlahkan seluruh hasil kuadratnya:
  ```
  SST = Σ (Xᵢ − G)²
  ```
📌 **Keterangan:**

- **N** = Jumlah total observasi dari semua kelompok  
- **Xᵢ** = Setiap nilai data individu  
- **G** = Grand mean (rata-rata keseluruhan dari semua data)

Jadi, **SST = Σ (Xᵢ − G)²** digunakan untuk mengukur **total variasi** seluruh data terhadap grand mean.

---

### 📘 Cara Menghitung SSC (Sum of Squares Between Groups)

**SSC** mengukur variasi **antar kelompok** (misalnya antar jenis pakan). Berikut langkah-langkah menghitungnya:

1. **Hitung selisih antara rata-rata setiap kelompok dengan grand mean (G):**
```plaintext
Deviasiᵢ = x̄ᵢ − X̄
```
2. Kuadratkan setiap deviasi:
```plaintext
Deviasi Kuadratᵢ = (x̄ᵢ − X̄)²

```

3. Kalikan hasil kuadrat dengan jumlah sampel dalam kelompok tersebut:
```plaintext
Deviasi Kuadrat Tertimbangᵢ = nᵢ × (x̄ᵢ − X̄)²

```

4. Jumlahkan semua hasil dari langkah 3 untuk mendapatkan nilai SSC:
```plaintext
SSC = Σ (nᵢ × (x̄ᵢ − X̄)²), untuk i = 1 sampai k
```

📌 Keterangan:

x̄ᵢ = rata-rata dari kelompok ke-i

X̄ = grand mean (rata-rata keseluruhan)

nᵢ = jumlah data dalam kelompok ke-i

k = jumlah total kelompok

---

![pic10](https://github.com/user-attachments/assets/6f54f733-25c3-42bb-b911-5cd2bed02928)

Di sini, **garis merah menunjukkan jarak antara rata-rata kelompok (x̄) dengan grand mean (G)**.

Seperti yang sudah kita bahas sebelumnya, saat **jarak antara rata-rata kelompok dan grand mean semakin besar**, maka kemungkinan besar memang **terdapat perbedaan yang signifikan antar kelompok**.

Nah, dalam bagian perhitungan **SSC (Sum of Squares Between Groups)**, kita menggunakan **perbedaan antara rata-rata tiap kelompok dengan grand mean** untuk mengukur **variabilitas antar kelompok**.

📌 Jadi sekarang, **kita akan berpindah fokus ke SSE (Sum of Squares Error)**, yaitu **variabilitas dalam kelompok** — yang memperhitungkan seberapa jauh masing-masing data menyimpang dari rata-rata kelompoknya sendiri.


### Langkah-langkah Menghitung SSE:

1. **Hitung selisih antara setiap data dengan rata-rata kolomnya (rata-rata tiap kelompok):**
```plaintext
Deviasiᵢⱼ = xᵢⱼ − x̄ⱼ
```
Di mana:

xᵢⱼ adalah nilai ke-i dalam kelompok ke-j

x̄ⱼ adalah rata-rata dari kelompok ke-j
```
Contohnya:
  - "Selisih antara setiap data di Feed A dengan rata-rata Feed A"
  - "Lalu selisih setiap data di Feed B dengan rata-rata Feed B, dan seterusnya"
```
2. Kuadratkan setiap deviasi tersebut:
```plaintext
(xᵢⱼ − x̄ⱼ)²
```
```
Dalam kasus kita, total ada 21 deviasi (karena 3 kelompok × 7 observasi).
```
3. Jumlahkan semua deviasi kuadrat tersebut untuk mendapatkan SSE:

![image](https://github.com/user-attachments/assets/4761a287-d650-4714-a514-8b04d8dc14ce)

Keterangan:

p = jumlah kelompok (pakan), dalam contoh ini: 3

n = jumlah observasi per kelompok, dalam contoh ini: 7

x̄ⱼ = rata-rata kelompok ke-j

xᵢⱼ = nilai ke-i dalam kelompok ke-j

### Penjelasan Sederhana SSE

Secara sederhana, **SSE (Sum of Squares Error)** mengukur **variabilitas dalam setiap kelompok (kolom)**.

Dengan kata lain, SSE merepresentasikan **kesalahan (error)** atau **variabilitas yang tidak dapat dijelaskan** oleh perbedaan antar kelompok.

Semakin besar nilai SSE, artinya data dalam tiap kelompok **tidak konsisten terhadap rata-rata kelompoknya sendiri**.

![pic11](https://github.com/user-attachments/assets/32fb4a8f-7222-4c44-94c3-edc059ca3bf5)

### Tabel One-Way ANOVA

Berikut adalah bentuk umum dari tabel ANOVA satu arah:

| Sumber Variasi        | Sum of Squares (SS)                                  | Derajat Bebas (df) | Mean Square (MS)       | F-ratio             |
|-----------------------|------------------------------------------------------|---------------------|------------------------|---------------------|
| **Antar Kelompok (SSC)** | SSC = Σ nᵢ × (x̄ᵢ − G)²                              | k − 1               | MSC = SSC / (k − 1)     | F = MSC / MSE        |
| **Dalam Kelompok (SSE)** | SSE = Σ (xᵢⱼ − x̄ⱼ)²                                | N − k               | MSE = SSE / (N − k)     |                     |
| **Total (SST)**        | SST = Σ (xᵢⱼ − X̄)²                                   | N − 1               |                        |                     |

---

### Penjelasan Komponen:

- **SSC**: Sum of Squares Between Groups  
- **SSE**: Sum of Squares Within Groups  
- **SST**: Total Sum of Squares (SST = SSC + SSE)

- **k**: Jumlah kelompok (group/treatment)  
- **N**: Jumlah total observasi

- **MSC**: Mean Square Between Groups = SSC / (k − 1)  
- **MSE**: Mean Square Within Groups = SSE / (N − k)

- **F**: Rasio F (F-statistic) = MSC / MSE

Tabel ini digunakan untuk melakukan uji F dalam ANOVA dan menentukan apakah terdapat **perbedaan signifikan antar rata-rata kelompok**.

### Nilai k, N, dan Derajat Bebas (Degrees of Freedom)

Dalam kasus kita:

- **k = 3** → karena ada tiga kelompok pakan: Feed A, Feed B, dan Feed C  
- **N = 27** → karena setiap kelompok memiliki 7 observasi: 3 × 7 = 21

---

### Derajat Bebas (Degrees of Freedom)

- **df antar kelompok (df groups)**  
  ```plaintext
  df_groups = k − 1 = 3 − 1 = 2
  ```
- **df dalam kelompok (df error)**
  ```
  df_error = N − k = 27 − 3 = 24
  ```
- **df total**
  ```
  df_total = N − 1 = 27 − 1 = 26
  ```

Derajat bebas ini akan digunakan untuk menghitung Mean Square (MS) dan F-statistic pada tabel ANOVA.

![image](https://github.com/user-attachments/assets/52f5532c-8c76-4b1a-b0d8-a9975a1ca73c)

Terakhir, nilai F-ratio dihitung dengan membagi MSC (Mean Square Between) dengan MSE (Mean Square Error). Bandingkan nilai F yang telah dihitung dengan nilai F dari tabel. Jika nilai F hitung lebih besar dari nilai F tabel, maka tolak hipotesis nol dan simpulkan bahwa terdapat perbedaan yang signifikan pada rata-rata kelompok, setidaknya di salah satu pasangan kelompok.

---

## 📊 Tabel ANOVA

| Sumber Variasi        | df  | SS       | MS      | F     |
|-----------------------|-----|----------|---------|-------|
| Antarkelompok (SSC)   | 2   | 88.87    | 44.33   | 0.28  |
| Dalam kelompok (SSE)  | 18  | 2812.57  | 156.25  |       |
| Total (SST)           | 20  | 2901.24  |         |       |

---

## 📏 Rumus F-Ratio

F = MSC / MSE = 44.33 / 156.25 ≈ 0.28

Sekarang mari kita bandingkan nilai **F hitung** dalam kasus kita, yaitu **0.28**, dengan nilai **F tabel**.  
(Dalam software statistik, nilai F kritis biasanya langsung disediakan.)

Untuk permasalahan ini, nilai **F kritis (tabel)** adalah **3.55**, yang **lebih besar** dari nilai F hitung kita (**0.28**).

---

## 🔍 Interpretasi

- Nilai F hitung: 0.28
- Bandingkan dengan nilai F tabel (pada df = 2 dan 18)
- Karena F hitung < F tabel → **Gagal menolak H₀**

---

### Kesimpulan

Karena **F hitung < F tabel**, maka kita **gagal menolak hipotesis nol (H₀)**.

Artinya, **tidak terdapat perbedaan yang signifikan** pada **rata-rata hasil produksi susu** berdasarkan jenis pakan yang diberikan.

Dengan kata lain, **pakan A, B, dan C tidak menunjukkan perbedaan nyata dalam pengaruhnya terhadap hasil produksi susu sapi**.

---

## 🧾 One-Way ANOVA: Asumsi Dasar

Agar hasil dari One-Way ANOVA valid dan dapat diandalkan, beberapa asumsi statistik berikut **harus dipenuhi**:

1. **Normalitas**  
   Setiap sampel berasal dari **populasi yang terdistribusi normal**.

2. **Varians yang Sama (Homogenitas Varians)**  
   Varians dari populasi tempat sampel diambil **harus sama**.  
   Kamu bisa menggunakan **Uji Bartlett** untuk menguji asumsi ini.

3. **Independensi**  
   Observasi antar kelompok harus **independen**, dan observasi dalam kelompok diperoleh dari **sampel acak**.

---

📌 **Ingat!**  
Untuk menerapkan One-Way ANOVA:
- Diperlukan **satu variabel kategorik** (sebagai variabel bebas) dengan **lebih dari dua level** — dalam kasus kita: **jenis pakan**.
- Dan satu **variabel kontinu** sebagai variabel terikat — dalam kasus kita: **hasil produksi susu (yield)**.

---

## 🔁 Rekap: Kenapa Kita Analisis Variansi?

Mari kita kembali ke pertanyaan inti: *“Kenapa kita menganalisis variansi untuk mengetahui apakah rata-rata kelompok berbeda?”*

Fokus pada bagian: **"rata-rata yang berbeda"**  
→ Perbedaan rata-rata **secara eksplisit melibatkan variasi antar rata-rata**.

- Kalau **tidak ada variasi antar rata-rata**, maka mereka **tidak mungkin berbeda**, bukan?
- Sebaliknya, semakin besar perbedaan antar rata-rata, maka **semakin besar variasi yang muncul**.

🧠 **ANOVA dan uji F** digunakan untuk menilai **besarnya variasi antar rata-rata kelompok** dengan mempertimbangkan **variasi dalam kelompok**, guna menentukan apakah perbedaan tersebut **signifikan secara statistik**.

---

🎯 Dengan kata lain, **semakin besar perbandingan antara variabilitas antar kelompok dan dalam kelompok**, semakin besar kemungkinan bahwa **perbedaan rata-rata yang diamati bukanlah kebetulan**.

---

## 📄 Referensi

Shrajankumar. (2023). *Introduction To ANOVA For Beginners*. Medium.
GitHub: [github.com/ShrajanKumar](https://github.com/ShrajanKumar)

<div align=center>

# TERIMA KASIH

</div>
