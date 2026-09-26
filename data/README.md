# Dataset Berita Politik Indonesia

## Sumber Dataset

Dataset yang digunakan dalam tugas Analisis Big Data adalah **Indonesian Political News Clean**.

Sumber dataset:
https://huggingface.co/datasets/ardimardiana/indonesian-political-news-clean

Dataset berisi kumpulan berita politik berbahasa Indonesia yang telah melalui proses pembersihan dan deduplikasi.

## Informasi Dataset

| Informasi    | Keterangan                      |
| ------------ | ------------------------------- |
| Nama Dataset | Indonesian Political News Clean |
| Sumber       | Hugging Face                    |
| Bahasa       | Bahasa Indonesia                |
| Format       | Parquet                         |
| Jumlah File  | 22 file                         |
| Jumlah Baris | Lebih dari 1 juta baris         |
| Jumlah Kolom | 15                              |
| Lisensi      | CC-BY-SA-4.0                    |
| DOI          | 10.57967/hf/9063                |

## Struktur Dataset

Dataset memiliki 15 atribut:

| Kolom           | Keterangan                                  |
| --------------- | ------------------------------------------- |
| `id`            | Identitas data berita                       |
| `news_title`    | Judul berita                                |
| `news_source`   | Sumber berita                               |
| `news_author`   | Penulis berita                              |
| `news_hostname` | Domain sumber berita                        |
| `news_date`     | Tanggal publikasi berita                    |
| `news_text`     | Isi berita                                  |
| `news_tags`     | Tag berita                                  |
| `news_kabkot`   | Kabupaten/kota yang berkaitan dengan berita |
| `news_intent`   | Informasi intent berita                     |
| `news_image`    | Informasi gambar berita                     |
| `update_date`   | Waktu pembaruan data                        |
| `create_date`   | Waktu pembuatan data                        |
| `news_guid`     | GUID berita                                 |
| `news_raw_data` | Data mentah berita                          |

## Pembagian File

Dataset tersedia dalam 22 file Parquet:

```text
train-00000-of-00022.parquet
train-00001-of-00022.parquet
train-00002-of-00022.parquet
...
train-00021-of-00022.parquet
```

Seluruh file ditempatkan pada folder `data/`.

## Cara Mendapatkan Dataset

Dataset dapat diunduh melalui halaman resmi Hugging Face:

https://huggingface.co/datasets/ardimardiana/indonesian-political-news-clean

Pada halaman tersebut, file Parquet tersedia pada bagian **Data files**.

Setelah seluruh file diunduh, letakkan file Parquet di folder:

```text
data/
```

## Penggunaan Dataset

Dataset digunakan sebagai data utama untuk tugas Analisis Big Data. Pada tahap awal, dataset dilakukan profiling menggunakan **Polars** dengan pendekatan **Lazy Evaluation**.

Profiling meliputi pemeriksaan:

* jumlah baris dan kolom;
* struktur dan tipe data;
* missing value;
* data duplikat;
* sumber berita;
* wilayah kabupaten/kota;
* rentang tanggal;
* karakteristik panjang teks.

Dataset tidak disertakan dalam repository Git karena memiliki ukuran yang besar. File dataset dapat diperoleh melalui sumber resmi yang tercantum di atas.

## Referensi Dataset

Mardiana, A., & Fauzan, B. (2026). *Indonesian Political News Clean*. Hugging Face. DOI: 10.57967/hf/9063.
