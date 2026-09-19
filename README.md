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

## 🚀 Cara Menjalankan (*How to Run*)
1. *Clone* repositori ini ke dalam *local machine* atau buka langsung menggunakan Google Colab.
   ```bash
   git clone [https://github.com/username-kamu/visualisasi-geospasial-indonesia.git](https://github.com/username-kamu/visualisasi-geospasial-indonesia.git)
