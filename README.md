# Klasifikasi Sinyal EKG pada penyakit Kardiovaskular Menggunakan CNN berbasis arsitektur VGG16
Repository ini berisi implementasi deep learning menggunakan transfer learning dengan arsitektur VGG16 untuk klasifikasi gambar EKG pasien jantung. Proyek ini memanfaatkan dataset dari Institut Kardiologi Ch. Pervaiz Elahi, Pakistan.

![Gambar Elektrokardiogram](https://faste.id/wp-content/uploads/2023/01/sinus-heart-rhythm-on-electrocardiogram-1024x683.jpg)

## Tujuan Penelitian
- Melakukan klasifikasi sinyal EKG menggunakan arsitektur VGG16 yang dimodifikasi untuk mendeteksi dan membedakan sinyal dengan akurasi tinggi.
- Mengevaluasi efektivitas model VGG16 dalam menangani karakteristik unik sinyal EKG, termasuk kemampuan ekstraksi fitur spasial melalui lapisan convolusi.
- Menganalisis pengaruh variasi hyperparameter, seperti learning rate, dropout, dan optimizer, terhadap performa model dalam hal akurasi, loss, dan kemampuan generalisasi.
- Mengidentifikasi konfigurasi hyperparameter terbaik yang dapat meningkatkan performa model dalam klasifikasi sinyal EKG.
- Menyediakan model deep learning yang lebih efisien dan akurat untuk membantu analisis sinyal EKG dalam aplikasi medis.

## Dataset 
Pada penelitian ini, dataset yang digunakan adalah Dataset Gambar EKG Pasien Jantung. Dataset gambar EKG ini merupakan koleksi data elektrokardiogram (EKG) dari pasien jantung yang dibuat di bawah naungan Ch. Pervaiz Elahi Institute of Cardiology di Multan, Pakistan, dengan tujuan untuk mendukung penelitian ilmiah dalam deteksi dan diagnosis penyakit kardiovaskular. Dataset ini terdiri dari empat kelas, namun dalam penelitian ini hanya dua kelas yang digunakan, yaitu Normal dan Abnormal, yang masing-masing menggambarkan kondisi EKG pasien tanpa gangguan jantung dan dengan gangguan jantung. Dataset ini disediakan oleh Ch. Pervaiz Elahi Institute of Cardiology dan berkolaborasi dengan University of Management and Technology, serta termasuk dalam kategori Cardiac Care dan ECG Database, yang bertujuan untuk membantu pengembangan metode deteksi otomatis penyakit jantung melalui analisis data EKG.

link sumber dataset : (https://data.mendeley.com/datasets/gwbz3fsgp8/2)

link drive dataset : (https://drive.google.com/drive/folders/1xuZaobn3d-7V8qZ3SMXu2mQ9yJufYkaM?usp=sharing)

## Tujuan Penelitian
Pada penelitian ini, digunakan model Convolutional Neural Network (CNN) berbasis arsitektur VGG16 yang telah terlatih sebelumnya dengan bobot dari dataset ImageNet. Model VGG16 dipilih karena kemampuannya dalam mengekstraksi fitur spasial secara mendalam melalui 13 lapisan convolusi dan 3 lapisan fully connected. Untuk menyesuaikan dengan karakteristik sinyal EKG, lapisan fully connected terakhir dihapus (include_top=False) dan digantikan dengan lapisan yang dirancang khusus, meliputi flatten layer, dense layer dengan 128 neuron dan aktivasi ReLU, serta output layer dengan 1 neuron dan aktivasi sigmoid untuk klasifikasi biner. Selain itu, dilakukan fine-tuning dengan membekukan sebagian besar lapisan awal model, sehingga hanya lapisan-lapisan terakhir yang dilatih ulang menggunakan data EKG.

![Gambar Arsitektur VGG16](https://raw.githubusercontent.com/Masterx-AI/VGG-16_Implemenation/main/VGG16.png)

## Anggota Kelompok
- Deodry Siahaan (121450151) - [Github] (https://github.com/deodrysiahaan)
- Salwa Amelia Salsabila (121450023) - [Github] (https://github.com/Aameliasalsabila)
- Audrey Ribka D. Manihuruk (121450103) - [Github] (https://github.com/audreyribkaa)
- Yosia Letare Banurea (121450149) - [Github] (https://github.com/YosiaBanurea)
- Deyvan Loxeval (121450148) - [Github] (https://github.com/deyvanloxefal)
