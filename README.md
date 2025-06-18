# Evaluasi Estetika Lanskap Kampus IPB Darmaga menggunakan BLIP

Repositori ini berisi kode dan data pendukung untuk penelitian tugas akhir berjudul "Evaluasi Estetika Lanskap Kampus IPB Darmaga menggunakan Bootstrapped Language-Image Pre-training (BLIP)". Penelitian ini dilakukan di Departemen Arsitektur Lanskap, Fakultas Pertanian, Institut Pertanian Bogor.

## 📄 Abstrak
Estetika visual adalah komponen penting dari pengalaman lanskap, meliputi elemen-elemen seperti warna, pola, dan tekstur yang memengaruhi kenyamanan dan daya tarik spasial. Lanskap Kampus IPB Dramaga memainkan peran strategis dalam mendukung keberlanjutan ekologis dan akademis. Namun, metode evaluasi estetika konvensional seringkali kurang objektif. Penelitian ini bertujuan untuk mengevaluasi estetika lanskap kampus melalui integrasi Visitor Employed Photography (VEP) dan Bootstrapped Language-Image Pre-training (BLIP). Sebanyak 1.086 foto dikumpulkan dari 31 mahasiswa peserta dan dianalisis menggunakan BLIP untuk menghasilkan deskripsi tekstual otomatis. Teks yang dihasilkan kemudian diproses menggunakan NVivo untuk mengekstrak 13 kata kunci dominan, yang selanjutnya diinterpretasikan menggunakan content analysis. Analisis ini mengidentifikasi elemen visual utama yang terkait dengan persepsi positif dan negatif, yang kemudian diinterpretasikan melalui prinsip-prinsip desain lanskap untuk menghasilkan rekomendasi desain yang meningkatkan harmoni spasial, ritme visual, dan estetika fungsional.

## ⚙️ Metodologi
Penelitian ini menggunakan kerangka kerja integratif yang menggabungkan persepsi manusia dengan analisis AI:

Pengumpulan Data (VEP): 31 partisipan dari kalangan mahasiswa IPB diminta untuk mengambil foto di sepanjang rute yang telah ditentukan di dalam Kampus IPB Darmaga, lalu mengkategorikannya sebagai "Menarik" atau "Tidak Menarik".

Ekstraksi Fitur Visual (BLIP): Sebanyak 1.086 foto yang valid dianalisis menggunakan model BLIP (salesforce/blip-image-captioning-large) untuk menghasilkan caption atau deskripsi tekstual dalam bahasa Inggris secara otomatis untuk setiap gambar.

Analisis Konten: Seluruh caption yang dihasilkan kemudian dianalisis menggunakan perangkat lunak NVivo untuk mengidentifikasi 13 kata kunci elemen visual yang paling dominan.

Interpretasi & Rekomendasi: Kata kunci dan asosiasinya diinterpretasikan berdasarkan prinsip-prinsip desain lanskap untuk merumuskan rekomendasi pengembangan.

## 📂 Struktur Repositori
.
├── code/
│   └── blip_caption_generator.ipynb   # Kode utama untuk menghasilkan caption dari gambar
├── data/
│   ├── photos/                        # Folder berisi foto-foto VEP (disarankan tidak di-upload jika privat)
│   └── output_captions.csv            # Contoh file CSV hasil luaran dari kode
├── paper/
│   └── Tugas_Akhir_Lengkap.pdf        # Dokumen PDF tugas akhir
└── README.md                          # File yang sedang Anda baca

 ## 🛠️ Instalasi
Untuk menjalankan kode dalam repositori ini, Anda perlu menginstal beberapa pustaka Python. Pastikan Anda memiliki Python 3.x terpasang.

pip install torch
pip install transformers
pip install Pillow

## 🚀 Cara Menjalankan Kode
Siapkan Data:

Buat sebuah folder (misalnya images_to_process).

Letakkan semua file gambar (format .jpg, .jpeg, .png) yang ingin Anda proses ke dalam folder tersebut.

Jalankan Script:

Buka file code/blip_caption_generator.ipynb menggunakan Jupyter Notebook atau JupyterLab.

Ubah path folder input (input_folder) dan nama file output (output_file) sesuai dengan kebutuhan Anda di dalam sel kode.

Jalankan semua sel kode secara berurutan.

Lihat Hasil:

Setelah proses selesai, sebuah file .csv akan dibuat (misalnya captions_result.csv).

File ini akan berisi dua kolom: filename (nama file gambar) dan caption (deskripsi yang dihasilkan oleh BLIP).

## 💡 Hasil Utama
Analisis menghasilkan 13 kata kunci elemen lanskap yang paling dominan, yaitu: Bench, Building, Forest, Garden, House, Lawn, Leaf, Park, Path, Plant, Road/Street, dan Sign. Analisis lebih lanjut menunjukkan bahwa persepsi estetika sangat bergantung pada konteks, keteraturan, dan perawatan, di mana elemen seperti Bench dan House yang terintegrasi baik cenderung dinilai positif, sementara Path yang tidak terawat dipersepsikan negatif.

## ✍️ Sitasi
Jika Anda menggunakan kode atau temuan dari penelitian ini dalam pekerjaan Anda, mohon sitasi karya berikut:

Fisabila, D. F. (2025). Evaluasi Estetika Lanskap Kampus IPB Darmaga menggunakan Bootstrapped Language-Image Pre-training (BLIP) (Tugas Akhir). Institut Pertanian Bogor: Bogor, Indonesia.

## ⚖️ Lisensi
Proyek ini dilisensikan di bawah Lisensi MIT. Lihat file LICENSE untuk detail lebih lanjut.
