# Rocket-3-FP

# Stage 1 (EDA)
Business Insight
Insights
Berdasarkan plots yang telah dianalisa, dapat diketahui insights berupa:

1. Terdapat tiga fitur yang mempengaruhi kuat churn rate, yaitu Tenure, CashbackAmount dan Complain.
2. Laptop & Accessory merupakan kategori dengan pencarian terbanyak oleh para customer.
3. Banyak terjadinya churn di kategori Mobile Phone, meskipun dengan adanya promo cashback.
4. Adanya churn pada feedback SatisfactionScore yang disertai complain, meskipun score nya sudah baik.
5. Semakin banyak OrderCount customer dengan coupon yang digunakan, semakin rentan untuk terjadi churn.
Rekomendasi bisnis

Berdasarkan insight-insight diatas, untuk mengurangi churn, perusahaan dapat melakukan hal-hal berikut:

1. Melakukan engagement untuk menarik kembali customer sudah lama tidak aktif.
2. Pengadaan promo cashback yang lebih banyak lagi, sehingga dapat menarik engagement dari para customer.
3. Memberikan rekomendasi produk sesuai kategori yang terpopuler berdasarkan minat customer sebelumnya, sehingga dapat menarik minat customer untuk melakukan pembelian.
4. Menyediakan platform saluran complain/feedback yang lebih terintegrasi dan mudah dibaca oleh perusahaan.
5. Memberikan coupon/voucher untuk mengatasi complain.
6. Meninjau dan menyesuaikan kembali coupon yang diberikan pada customer yang memiliki jumlah order banyak agar dapat memenuhi kepuasan customer.

# Stage 2 (Data Pre-process)
Data Cleansing
Pertama kita cek apakah ada data yang kosong dan duplicate.
1. Untuk mengecek data yang kosong, menggunakan df.isna()sum. Dari hasil tersebut ditemukan bahwa ada data yang null di ganti dengan median dan mean.
2. Untuk mengecek data yang duplicate, menggunakan df.duplicates(. Dari hasil tersebut ditemukan bahwa tidak ada data yang duplicate.

Handle Missing Value
1. Untuk kolom Tenure, Ware House to Home, Hour Spend On App,Coupon Used, Order Count, dan Day Since Last Order di ganti dengan median.
2. Untuk kolom Order Amount Hike From last Year di ganti dengan mean.

Feature Transformation
1. Pada feature HourSpendApp, Number of device registered, satisfaction score, number of address, order amount hike from last year, day since order, cashback amount distribusi data pada feature tersebut adalah normal.
2. Pada feature couponused dan ordercount distribusi feature tersebut mengalami skew / tidak normal.
3. Pada feature dengan distribusi normal dan tidak normal tersebut dilakukan scaling.

Feature Encoding

Feature Encoding untuk proses mengubah kolom dengan feature categorical menjadi feature numeric.

Handle Class Imbalance

Feature Encoding untuk proses mengubah feature categorical menjadi feature numeric karena saat membuat permodelan, model hanya dapat menggunakan feature categorical.

Feature Engineering

Feature Selection

Pada dataset yang kami gunakan tidak ada penambahan feature dikarenakan seluruh feature digunakan untuk modelling dan tidak ada yang di drop.

Feature Extraction

Membuat satu feature baru, yaitu average churn.

Feature Tambahan
1. Age = untuk mengetahui persebaran umur yang lebih banyak churn.
2. Product recommendation = untuk dapat mengukur kategori mana yang dapat ditawari promo.
3. Product review = menggali ulasan customer sehingga dapat membantu keputusan pembelian bagi customer berikutnya.
4. Call-to-action = memberikan informasi baru tentang produk-produk atau promo sehingga dapat menarik perhatian customer.
