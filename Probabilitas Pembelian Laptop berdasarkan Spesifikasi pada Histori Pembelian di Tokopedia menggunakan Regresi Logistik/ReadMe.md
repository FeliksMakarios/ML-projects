# Integrated Final Project #2
This is the result of an Integrated Final Project from two courses: Data Analytics, and Artificial Intelligence. This project is done in groups.

## Objectives
History Data pembelian dan data customer yang ada didalam database Tokopedia tentunya sangat banyak, ada banyak cara untuk mengolah data yang ada pada database Tokopedia. Spesifiksasi laptop akan digunakan sebagai fitur-fitur. Spesifikasi ini seperti merk, ukuran memori, prosesor, ukuran disk, harga, dan jumlah terjualnya. Regresi logistik akan digunakan untuk melihat besarnya nilai _r<sup>2</sup>_ dari setiap fitur. Fitur dengan nilai _r<sup>2</sup>_ tertinggi dianggap memiliki kemampuan yang tinggi dalam memberikan rekomendasi pembelian laptop. Sebagai hipotesis awal, fitur merk diasumsikan memiliki nilai _r<sup>2</sup>_ tertinggi. Sebuah pencarian laptop berdasarkan merk tertentu dianggap akan menampilkan rekomendasi laptop yang paling tepat dengan merujuk ke histori pembelian seluruh pengguna.

Tujuan penelitian ini adalah:
1)	Menentukan fitur yang tepat untuk digunakan dalam analisis probabilitas pembelian laptop
2)	Menentukan probabilitas pembelian laptop dengan merk tertentu menggunakan model regresi logistik

## Results

Berdasarkan hasil klasifikasi dengan pohon keputusan baik dengan ID3 ataupun Random Forest, terlihat dataset layak untuk digunakan dalam proses klasifikasi merk laptop dengan fitur-fitur spesifikasi lainnya. Model ID3 dan Random Forest yang dikembangkan memiliki akurasi yang sama sebesar 0,642 atau 64%. Hasil kedua model tersebut menunjukkan data input yang sama menghasilkan hasil klasifikasi yang sama.

Proses klusterisasi dimulai dengan melakukan Korelasi Pearson terhadap semua fitur. Dari hasil korelasi, ditemukan dua fitur yang memiliki tingkat korelasi yang cukup tinggi, yaitu `price_cat` dengan `memory_size`. Kedua fitur ini kemudian digunakan dalam proses klusterisasi untuk melihat jumlah kluster yang tepat yang memiliki karakteristik yang unik satu sama lain. Hasilnya terdapat tiga kluster dengan *Kluster 0* dan *Kluster 1* memiliki data terbanyak. Hasil klusterisasi menunjukkan bahwa laptop dengan ukuran memori yang tinggi akan sejalan dengan harga laptop yang semakin mahal pula. Jumlah data yang banyak pada Kluster menunjukkan harga laptop yang mahal dengan memori yang tinggi justru lebih diminati. Hal ini terlihat dari jumlah transaksi yang sangat tinggi diatas 50% dari total keseluruhan transaksi. Disusul dengan *Kluster 1* dengan rentang laptop yang lebih murah dan ukuran memori yang lebih kecil dari Kluster 0.

Hasil regresi logistik pada ketiga fitur (`price_cat`, `memory_size`, dan `merk_cat`) menunjukkan bahwa ketiganya dapat dibuat persamaan regresi logistiknya untuk menentukan probabilitas pembelian laptop. Namun, dari hasil perhitungan regresi, terlihat bahwa _r<sup>2</sup>_ untuk `price_cat` menghasilkan nilai yang terbesar yaitu 0,82. Sedangkan `merk_cat` memiliki nilai _r<sup>2</sup>_ sebesar 0.17 yang berarti bahwa `merk_cat` memberikan pengaruh yang sangat kecil terhadap probabilitas pembelian sebuah laptop. Dari hasil tersebut, `price_cat` memiliki pengaruh yang sangat tinggi dalam menentukan probabilitas pembelian sebuah laptop.

`price_cat` memiliki kemampuan yang tinggi dalam memberikan rekomendasi pembelian laptop.

## Conclusions
Hasil eksperimen yang dilakukan dalam penelitian ini menunjukkan bahwa *harga* merupakan faktor *paling berpengaruh* dalam pembelian laptop berdasarkan histori pembelian seluruh pengguna Tokopedia. Penelitian ini dapat memberikan rekomendasi agar Tokopedia dapat menggunakan data histori pembelian sebagai sarana dalam memberikan rekomendasi laptop yang paling tepat untuk pengguna berdasarkan rentang harga yang diinginkan pengguna. Ini juga dapat dijadikan referensi ketika sebuah brand ingin mempromosikan produknya lewat banner iklan atau hal lainnya.

Dalam prosesnya, ada banyak data yang dibuang karena dalam penulisan namanya tidak mencantumkan spesifikasi yang digunakan dalam penguraian untuk membuat fitur yang baru. Sehingga disarankan Tokopedia dapat membuat aturan penulisan yang seragam untuk penjualan laptop. Didalamnya terdapat merk, tipe, ukuran memori, ukuran disk, dan prosesor. Hal ini akan sangat membantu dalam mengeksplorasi dan menganalisis histori pembelian laptop dari setiap toko/merchant.

## Published Paper:
This research has not been published yet because it coincides with the design of our thesis proposal.

## Dataset:
https://www.kaggle.com/artakusuma/laptopecomercee
