# Visualisasi Data Lanjut: Analisis Geospasial Demografi Indonesia 🇮🇩

Repositori ini berisi proyek analisis dan visualisasi data spasial (geospasial) tingkat provinsi di Indonesia. Proyek ini bertujuan untuk memetakan data pernikahan menggunakan pemodelan poligon dari file *Shapefile* (SHP).

## 🎯 Tujuan Proyek
* **Eksplorasi Data Spasial:** Membaca dan memproses data geografis Indonesia menggunakan format SHP.
* **Visualisasi Demografi:** Memetakan metrik kependudukan ke dalam representasi visual yang mudah dipahami.
* **Otomatisasi & Pemrosesan:** Menggabungkan dan membersihkan atribut data spasial dengan Pandas dan GeoPandas untuk kebutuhan *business intelligence* atau pelaporan analitik.

## 🛠️ Teknologi & Library
Proyek ini dibangun di atas ekosistem Python untuk *Data Science* dan pemetaan:
* **GeoPandas & Pandas:** Membaca *Shapefile* (`WADMPR1.shp`), memanipulasi *GeoDataFrame*, dan memproses atribut tabular.
* **Geoplot & Cartopy:** Membuat visualisasi peta tingkat lanjut yang presisi.
* **Matplotlib & Seaborn:** Mengatur tata letak visual dan skema warna.
* **Mapclassify:** Melakukan klasifikasi data spasial untuk pewarnaan peta (*choropleth*).

## 📂 Dataset
Data yang digunakan bertumpu pada *Shapefile* wilayah administrasi provinsi Indonesia (`WADMPR1.shp`). Atribut utama yang dieksplorasi meliputi:
* `Jumlah_Pen`: Total populasi per provinsi.
* `Kepadatan_`: Kepadatan penduduk per kilometer persegi.
* `Laju_Pertu`: Laju pertumbuhan penduduk.
* `Rasio_Jeni`: Rasio jenis kelamin.
* `AREA_KM2`: Luas wilayah provinsi.
* **`Provinsi`**: Nama wilayah tingkat provinsi di Indonesia (contoh: Aceh, Bali), berfungsi sebagai label dan *identifier*.
* **`geometry`**: Berisi data spasial dengan format *MULTIPOLYGON* yang mendefinisikan koordinat dan batas geografis (poligon) masing-masing provinsi. Kolom ini mutlak diperlukan oleh GeoPandas untuk merender bentuk wilayah di atas peta.
* **`Nikah`**: Nilai numerik yang merepresentasikan total angka pernikahan yang tercatat di provinsi tersebut. Kolom ini merupakan metrik utama yang akan menentukan gradasi warna (intensitas) pada visualisasi peta *choropleth*.

## 📈 Analisis Mendalam (*In-Depth Analysis*)

Berdasarkan pemrosesan data spasial dan visualisasi metrik demografi tingkat provinsi di Indonesia, terdapat beberapa wawasan strategis yang dapat ditarik:

<img width="1570" height="543" alt="pernikahan-indonesia" src="https://github.com/user-attachments/assets/8e2eed2b-2b53-4853-8fb7-a655c2da7ee6" />

###1. Konsentrasi Ekstrem di Pulau Jawa
Angka pernikahan tertinggi, yang ditandai dengan warna kuning (> 100 Ribu pernikahan), secara eksklusif berpusat di provinsi-provinsi utama Pulau Jawa, khususnya Jawa Barat, Jawa Tengah, dan Jawa Timur. Hal ini sejalan dengan status Jawa sebagai pusat populasi terbesar di Indonesia. Tingginya angka pembentukan keluarga baru di area ini menjadikannya pasar paling potensial dan padat untuk sektor industri yang menargetkan keluarga muda, seperti perumahan (KPR), ritel barang rumah tangga, dan layanan kesehatan ibu dan anak.

### 2. Transisi Menengah di Sumatra, Kalimantan, dan Sulawesi (Kategori 10 Ribu - 100 Ribu)
Sebagian besar wilayah Sumatra dan Pulau Sulawesi berada pada rentang warna biru tua (10-25 Ribu) hingga toska (25-50 Ribu). Terdapat pula beberapa wilayah transisi dengan warna hijau muda (50-100 Ribu) yang berbatasan langsung dengan area populasi tinggi di Jawa. Angka ini merepresentasikan wilayah dengan basis demografi menengah yang stabil, yang secara analitik sering mewakili pasar sekunder (secondary markets) yang sedang berkembang di luar pulau Jawa. Sebagian besar Pulau Kalimantan juga berada di rentang biru tua (10-25 Ribu).

### 3. Angka Rendah di Indonesia Timur (Kategori < 10 Ribu)
Wilayah bagian timur Indonesia, termasuk Kepulauan Maluku dan seluruh regional Papua, didominasi oleh warna ungu pekat yang menandakan angka pernikahan di bawah 10 ribu. Angka yang rendah di area ini berkorelasi langsung dengan kepadatan penduduk yang lebih minim serta luasnya sebaran geografis di wilayah tersebut.

### Visualisasi spasial ini menegaskan bahwa metrik jumlah pernikahan berbanding lurus dengan peta kepadatan penduduk. Dalam konteks business intelligence atau pemodelan data strategis, peta ini tidak hanya menunjukkan rekapitulasi peristiwa demografis di tahun 2024, tetapi juga secara efektif memetakan letak kepadatan permintaan konsumen baru. Strategi rantai pasok (supply chain) atau integrasi dasbor analitik dapat menggunakan landasan spasial seperti ini untuk menentukan prioritas distribusi produk khusus keluarga, dengan memfokuskan penetrasi pada zona kuning dan hijau
