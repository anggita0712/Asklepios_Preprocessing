# Final Project

Data source : https://www.kaggle.com/prachi13/customer-analytics

## Kelompok 3 : "Asklepios"
#### Anggota : 
- Awalsyah Rinanto Putra
- Fathah Oscar
- M Rizky Septiansyah
- Hermawan Febrianto
- Devi Puji Ayuningsih
- Anggita Citanegara Lubis
    
    
## Descriptive Statistics
A. Semua tipe data dan nama kolom serta isinya sudah sesuai <br>
B. Tidak ada kolom yang memiliki missing value <br>
C. Jika dilihat dari nilai max, variabel Purchases dan Discount kemungkinan memiliki nilai outlier


## Univariate Analysis
![kde](https://user-images.githubusercontent.com/116422996/198684631-8a1a8358-6737-4c38-bcf1-718f90170ae7.jpg)
![categorical](https://user-images.githubusercontent.com/116422996/198685064-87b541a2-a02c-4db9-b465-63e3da6d04a8.jpg)

#### Hasil Observasi  <br>
- Variabel Purchases dan Discount memiliki outlier dan membentuk pola positively Skewed
- Variabel Cost memiliki distribusi yang paling mendekati distribusi normal
- Warehouse block yang paling banyak digunakan adalah Warehouse F
- Shipment mode yang dominan adalah pengiriman dengan kapal
- Jumlah sampel yang mengalami keterlambatan pengiriman lebih banyak


## Multivariate Analysis
![heatmap](https://user-images.githubusercontent.com/116422996/198685212-05e9cebb-2b61-4105-99de-bff76598b4cf.jpg)

#### Hasil Observasi  <br>
A. Feature yang paling relevan dan harus dipertahankan adalah feature Discount dan Weight <br>
B. Feature yang memiliki korelasi antar feature adalah 
- Weight terhadap Calls
- Weight terhadap Discount
- Cost terhadap Calls


## Business Insight and Recommendation
- Untuk pembelian produk dengan discount diatas 10% banyak mengalami keterlambatan pengiriman. <br>
Dalam hal ini pihak e-commerce perlu memberikan notifikasi keterlambatan pengiriman kepada customer ketika melakukan pembelian dengan menggunakan discount yang besar yang memungkinkan produk yang dipesan tidak terkirim tepat waktu.
- Barang dengan berat 2-4 Kg terkonfirmasi mengalami keterlambatan pengiriman. <br>
Dalam hal ini, pihak e-commerce perlu memberikan notifikasi keterlambatan pengiriman kepada customer yang membeli produk di rentang berat produk 2-4 kg sebelum customer melakukan transaksi.
- Semakin banyak customer care calls yang terjadi maka tingkat keterlambatan pengiriman semakin menurun <br>
Berdasarkan data jumlah keterlambatan pengiriman menurun dengan meningkatnya jumlah telepon yang diterima oleh customer care.
Perusahaan perlu mencari informasi mengenai isi telepon customer kepada customer care (siapa penelpon, isi telepon), sehingga bisa menentukan korelasi dengan jumlah keterlambatan pengiriman.

Rekomendasi dengan Asumsi: 
1. Bila di asumsikan bahwa pelanggan menelpon untuk melakukan konfirmasi pemesanan, maka bisa dilakukan proses konfirmasi pemesanan dari pelanggan memberikan pengingat kepada penjual untuk segera melakukan konfirmasi ketersediaan barang dan kesiapaan pengiriman kepada bagian pengiriman atau kurir. (bisa dengan aplikasi atau ditambahkan pada petugas tertentu).
2. Bila di asumsikan bahwa penjual menelpon untuk melakukan konfirmasi kesediaan pesanan dan barang siap di kirim, maka bisa dilakukan proses otomatisasi saat penjual konfirmasi kesediaan barang, langsung barang disiapkan untuk di kirim pada hari yang sama dan mengirimkan konfirmasi untuk kurir mengirimkan.

## Data Pre-Processing
### Data Cleansing
- Dilakukan handle outliers pada feature Discount yang menghasilkan 8604 baris data
- Dilakukan standardization/normalization pada tiga feature yaitu: Cost, Discount dan Weight dikarenakan memiliki nilai variance dan standard deviation yang tinggi
- Merubah nilai kategorik menjadi numerik pada feature Gender dan Importance menggunakan Label Encoding, dan menggunakan One Hots Encoding pada feature Warehouse dan Shipment
- Proportion of minority >40% sehingga tidak perlu dilakukan handle class imbalance

### Feature Engineering
- Menghapus feature ID, Warehouse dan Shipment
- Feature yang bisa ditambahkan : waktu pengiriman, alamat customer, alamat warehouse, musim/cuaca, kapasitas pengiriman per-hari, dan traffic route
Footer
