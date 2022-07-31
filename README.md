# Prediksi Harga Saham

Repo ini berisi kodingan python yang digunakan dalam skripsi.
Data yang digunakan ukurannya yang cukup besar maka tidak diupload di github. Data tersebut bisa diakses di [google drive](https://drive.google.com/drive/folders/15HNIiolMJg2EfiUVa6vB1_LB0ZeFB6dP?usp=sharing)


## Tools yang digunakan

Dalam proses pengerjaan skripsi ini menggunakan `Conda` sebagai package managernya, sehingga agar mempermudah untuk menjalankan kodingan yang ada silahkan install terlebih dahulu [`Conda`](https://docs.conda.io/en/latest/) di laptopmu. Setelah itu buka terminal dan jalankan perintah berikut 

```cmd
conda create --name <env> --file requirements.txt
conda activate <env>
```

Ubah `<env>` dengan nama environment yang kamu inginkan. Untuk melihat library yang digunakan silahkan lihat pada `requirements.txt`


## File dan Folder Kodingan

Berikut beberapa notebook yang ada pada repo ini dan disarankan untuk dijalankan secara berurutan.

1. `Scraping.ipynb`, notebook ini berisi kodingan untuk melakukan scraping data berita secara incremental. Akan dilakukan pengecekan pada data yang ada untuk mengetahui kapan terakhir melakukan scraping kemudian setelah itu akan dilakukan scraping dari tanggal tersebut sampai kapan notebook ini dijalankan. Sebelum menjalankan notebook ini pastikan folder `data` sudah diisi berdasarkan data yang ada di [google drive](https://drive.google.com/drive/folders/15HNIiolMJg2EfiUVa6vB1_LB0ZeFB6dP?usp=sharing)
2. `Translator.ipynb`, notebook ini berisi kodingan untuk melakukan translate data berita dari bahasa Indonesia ke bahasa Inggris. Hasil dari translatenya disimpan di `data/translate.txt`
3. `PerbandinganMetodeSentiment.ipynb`, notebook ini berisi perbandingan beberapa metode sentimen analisis berbasi lexical based. Hasil dari analisis ini yang menentukan model sentiment yang akan digunakanan.
4. `Sentimen.ipynb`, notebook ini berisi sentimen analisis menggunakan VADER. Sentimen skor yang diperoleh akan disimpan `data/data_vader.json`.
5. `HyperparameterOptimization.ipynb`, notebook ini berisi penerapan hyperparameter optimization menggunakan Bayesian Optimization dengan package Keras Tuner. Hasil dari setiap percobaan akan disimpan dalam folder `model`. Untuk setiap hyperparameter yang dijalankan akan disimpan hasil evaluasi dari pemodelan yang dilakukan beserta modelnya. Telah dicoba 40,000 hyperparameter sehingga folder `model` memiliki ukuran yang besar. Folder `model` yang ada pada google drive telah dihapus file modelnya sehingga yang ada hanya hasil evaluasi dari modelnya.
6. `PerbandinganKombinasiVariabel.ipynb`, setiap hyperparameter terbaik untuk setiap kombinasi variabel dilatih lagi pada 60 fold forward validation, dan notebook ini melakukan hal tersebut. Hasilnya disimpan pada folder `kombinasi_variabel`
7. `TestingData.ipynb`, model terbaik dari proses perbandingan kombinasi variabel akan dievaluasi pada data testing mulai dari Januari-Maret 2022. Proses tersebut dilakukan pada notebook ini. Hasilnya disimpan pada folder `testing_data`
8. `Analisis.ipynb`, notebook ini berisi kodingan untuk menjawab tujuan 1-4 dari penelitian ini. Hasil yang dijabarkan pada bab 4 diperoleh dari hasil olahan yang ada di notebook ini

Selain itu terdapat juga beberapa folder

1. `helpers`, folder ini berisi Class yang dipakai di beberapa notebook. Tujuannya agar pendefinisian Class nya hanya dilakukan disatu tempat sehingga tidak susah jika ada perubahan.
2. `scraping_history`, folder ini berisi kodingan untuk melakukan scraping data berita dari tahun 2004. Silahkan cek `README.md` untuk detailnya
3. Folder yang tidak ada pada repo ini karena ukurannya sangat besar. Silahkan download folder tersebut beserta isinya di [google drive](https://drive.google.com/drive/folders/15HNIiolMJg2EfiUVa6vB1_LB0ZeFB6dP?usp=sharing)


Repo ini juga bisa diperoleh di [Github](https://github.com/ekoptra/skripsi). *Thank you for visiting my repo!*

**Best Regards, Eko Putra Wahyuddin!**
