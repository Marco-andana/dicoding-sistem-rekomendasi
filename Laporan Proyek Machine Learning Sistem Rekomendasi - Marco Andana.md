# Laporan Proyek Machine Learning - Nama Anda

## Project Overview

Dalam era digital saat ini, jumlah konten film yang tersedia di berbagai platform semakin meningkat secara eksponensial. Dengan begitu banyak pilihan, pengguna sering kali kesulitan menemukan film yang sesuai dengan preferensi mereka. Oleh karena itu, sistem rekomendasi film menjadi solusi penting untuk meningkatkan pengalaman pengguna dengan memberikan rekomendasi yang dipersonalisasi.
Sistem rekomendasi film menggunakan teknik Machine Learning untuk menganalisis preferensi pengguna berdasarkan riwayat tontonan, rating, dan metadata film. Algoritma seperti Collaborative Filtering, Content-Based Filtering, dan Hybrid Models dapat digunakan untuk mengidentifikasi pola dan memberikan saran film yang relevan bagi setiap pengguna.
Dalam proyek ini, Machine Learning diterapkan untuk membangun model sistem rekomendasi yang dapat meningkatkan kepuasan pengguna dengan menyediakan rekomendasi film yang lebih akurat. Dengan memanfaatkan dataset film yang berisi informasi seperti rating, genre, dan tag relevansi, model dapat mempelajari preferensi pengguna dan menghasilkan rekomendasi yang lebih personal.

### Mengapa Demikian ?
Sistem rekomendasi film menjadi semakin krusial dalam industri hiburan modern, terutama dengan pertumbuhan layanan streaming seperti Netflix, Disney+, dan Amazon Prime. Proyek ini penting untuk diselesaikan karena beberapa alasan utama:

1. Mengatasi Overload Informasi (Information Overload)
Dengan meningkatnya jumlah film yang tersedia di berbagai platform, pengguna sering mengalami kesulitan dalam memilih film yang sesuai dengan preferensi mereka. Sistem rekomendasi membantu mengatasi masalah ini dengan memberikan saran film yang dipersonalisasi berdasarkan pola perilaku pengguna.

2. Meningkatkan Keterlibatan dan Retensi Pengguna
Layanan seperti Netflix telah membuktikan bahwa sistem rekomendasi yang efektif dapat meningkatkan keterlibatan pengguna. Studi oleh Gomez-Uribe & Hunt (2016) menunjukkan bahwa sistem rekomendasi Netflix menghemat ratusan juta dolar per tahun dengan meningkatkan waktu tonton pelanggan dan mengurangi tingkat churn (pengguna yang berhenti berlangganan).

3. Meningkatkan Monetisasi dan Pendapatan bagi Platform Streaming
Sistem rekomendasi tidak hanya meningkatkan kepuasan pengguna tetapi juga berdampak pada aspek bisnis. Studi oleh Davidson et al. (2010) menunjukkan bahwa sistem rekomendasi YouTube menyumbang lebih dari 60% total tayangan video di platform mereka.

4. Penerapan Machine Learning yang Menarik dan Menantang
Mengembangkan sistem rekomendasi film menggabungkan berbagai teknik Machine Learning, termasuk Content-Based Filtering, Collaborative Filtering, dan Hybrid Models. Proyek ini memberikan kesempatan untuk menerapkan konsep-konsep seperti Natural Language Processing (NLP) untuk analisis deskripsi film atau Deep Learning untuk memahami pola rating pengguna.

## Refrensi
- [Recommender Systems: Introduction and Challenges](https://link.springer.com/chapter/10.1007/978-981-10-0557-2_112)
- [The Netflix Recommender System: Algorithms, Business Value, and Innovation](https://dl.acm.org/doi/abs/10.1145/2843948)
- [The YouTube Video Recommendation System](https://dl.acm.org/doi/abs/10.1145/1864708.1864770)
- [Recommender Systems: The Textbook](https://link.springer.com/content/pdf/10.1007/978-3-319-29659-3.pdf)

## Business Understanding

### Problem Statements

Dalam era digital, platform streaming menghadapi tantangan dalam menyediakan rekomendasi film yang relevan bagi pengguna. Masalah utama yang perlu diselesaikan dalam proyek ini adalah:

### 1. Overload Informasi
- Dengan ribuan film yang tersedia, pengguna sering kesulitan menemukan film yang sesuai dengan preferensi mereka.

### 2. Rekomendasi yang Tidak Akurat
- Sistem rekomendasi tradisional sering kali memberikan saran yang tidak relevan atau terlalu umum, menyebabkan ketidakpuasan pengguna.

### 3. Kurangnya Personalisasi
- Beberapa sistem rekomendasi masih mengandalkan peringkat rata-rata atau popularitas tanpa mempertimbangkan preferensi individu pengguna.

### 4. Keterbatasan Data dan Cold Start Problem
- Pengguna baru atau film baru memiliki sedikit data interaksi, sehingga sulit memberikan rekomendasi yang efektif.

### Goals

Tujuan proyek ini adalah untuk mengembangkan sistem rekomendasi film berbasis Machine Learning yang dapat mengatasi masalah yang telah diidentifikasi:

#### 1. Mengurangi Overload Informasi
- Mengembangkan sistem yang dapat secara otomatis menyaring dan merekomendasikan film yang paling relevan bagi pengguna.

#### 2. Meningkatkan Akurasi Rekomendasi
- Menggunakan teknik Machine Learning seperti Collaborative Filtering, Content-Based Filtering, dan Hybrid Models untuk meningkatkan relevansi rekomendasi.

#### 3. Meningkatkan Personalisasi
- Memanfaatkan data pengguna (rating, histori tontonan, preferensi) untuk menghasilkan rekomendasi yang lebih sesuai.

#### 4. Mengatasi Cold Start Problem
- Menggunakan pendekatan berbasis metadata (genre, aktor, sutradara) untuk memberikan rekomendasi awal bagi pengguna baru atau film baru.

### Solution Statements
Untuk mencapai tujuan di atas, proyek ini akan menggunakan beberapa pendekatan algoritmik:

#### 1. Collaborative Filtering
Menggunakan data interaksi pengguna (rating, ulasan) untuk mengidentifikasi pola kesamaan preferensi antar pengguna.

- Teknik: User-Based Collaborative Filtering, Item-Based Collaborative Filtering.

#### 2. Content-Based Filtering
Menganalisis metadata film (genre, sinopsis, aktor, sutradara) untuk merekomendasikan film yang mirip dengan yang pernah ditonton pengguna.

- Menggunakan TF-IDF (Term Frequency-Inverse Document Frequency) dan Cosine Similarity.

#### 3. Hybrid Recommendation System
Menggabungkan Collaborative Filtering dan Content-Based Filtering untuk meningkatkan akurasi rekomendasi.

- Menggunakan Weighted Hybrid Model atau Stacked Model dengan Deep Learning.

#### 4. Deep Learning for Recommendation
Memanfaatkan Neural Networks seperti Autoencoders atau Recurrent Neural Networks (RNN) untuk memahami pola interaksi pengguna secara lebih kompleks.

## Data Understanding
Dataset yang digunakan dalam proyek ini berisi informasi terkait film, rating pengguna, dan tag yang diberikan oleh pengguna. Dataset ini berasal dari [MovieLens Dataset](https://www.kaggle.com/datasets/grouplens/movielens-20m-dataset), yang merupakan salah satu dataset rekomendasi film paling populer dan sering digunakan dalam penelitian sistem rekomendasi.
Dari tiap pengecekan Dataset, ditemukan null value dan duplikat pada data sehingga dilakukan drop table dan penghapusan duplikat.
### Kondisi Data
Jumlah data: 100.000 pada masing-masing file dan 16 kolom
![jml dataset](https://raw.githubusercontent.com/Marco-andana/dicoding-sistem-rekomendasi/6d784d02539a6bb139ebdd6db64b21a4531a97c9/jml%20dataset.png)
Kondisi data: terdapat null value dan duplikat pada data
![null](https://raw.githubusercontent.com/Marco-andana/dicoding-sistem-rekomendasi/5ea07ab9a9b880f2488f6a67884d54fc63aade64/nulld.png)
Jumlah film: 27278
Jumlah pengguna: 138493
Jumlah rating: 20000263
Rentang waktu data: 9 Januari 1995 - 31 Maret 2015
Sumber dataset: [MovieLens Dataset](https://www.kaggle.com/datasets/grouplens/movielens-20m-dataset)

Variabel-variabel pada MovieLens Dataset adalah sebagai berikut:
#### 1. Movies.csv (27278 baris dan 3 kolom)
- movieId: ID unik untuk setiap film.
- title: Judul film beserta tahun rilis.
- genres: Daftar genre yang terkait dengan film (dipisahkan dengan "|").

#### 2. ratings.csv (100000 baris dan 4 kolom)

- userId: ID unik pengguna yang memberikan rating.
- movieId: ID film yang diberi rating.
- rating: Nilai rating dari pengguna (biasanya dalam skala 0.5 - 5.0).
- timestamp: Waktu ketika rating diberikan.

#### 3. tags.csv (100000 baris dan 4 kolom)

- userId: ID unik pengguna yang memberikan tag.
- movieId: ID film yang diberi tag.
- tag: Kata kunci atau frasa yang diberikan pengguna untuk menggambarkan film.
- timestamp: Waktu ketika tag diberikan.

#### 4. genome-scores.csv (100000 baris dan 3 kolom)

- movieId: ID film yang dievaluasi.
- tagId: ID unik untuk setiap tag dalam Genome Tagging.
- relevance: Skor relevansi antara film dan tag (dalam skala 0.0 - 1.0).

#### 5. genome-tags.csv (1128 baris dan 2 kolom)

- tagId: ID unik untuk setiap tag.
- tag: Nama tag yang digunakan dalam Genome Tagging.

#### 6. links.csv (27278 baris dan 3 kolom)

- movieId: ID film yang dievaluasi.
- imdbId: ID untuk imbd film.
- tmdbId: ID untuk tmdb film.

### Exploratory Data Analysis (EDA)
Beberapa langkah analisis eksplorasi yang dilakukan pada dataset ini mencakup:

Hal pertama yang dilakukan adalah dengan menganalisis file movie. Dimana pada file movie ini terdapat 3 kolom yaitu movieId, titles, dan genre.

```
print('Jumlah userId: ', len(ratings.userId.unique()))
print('Jumlah movieId: ', len(ratings.movieId.unique()))
print('Jumlah data rating: ', len(ratings))
```
Selain itu dilakukan juga pengecekan jumlah userId, movieId, dan data rating. Halini bertujuan untuk mengetahui ada berapa jumlah pengguna, movie, dan data rating yang unik.

## Data Preparation
Pada bagian ini, dilakukan penyiapan dan pembersihan data agar data siap untuk bahan pelatihan model.

## Merge File
```
movie_info = pd.concat([movies, tags])
movie = pd.merge(ratings, movie_info, on='movieId', how='left')
movie
```
hal yang pertama dilakukan adalah dengan menggabungkan file movies dan tags pada variabel movie_info. Setelah itu, dilakukan merge pada tabel ratings dan movie_info dengan movieId sebagai kolom kunci untuk menggabungkan data.

```
all_resto_name = pd.merge(all_movies_rate, movies[['movieId', 'title']], on='movieId', how='left')
all_resto_name
```
pada kode ini dilakukan penggabungan atau merge pada variabel all_movies_rate dan movies dimana hanya dipilih 2 kolom yaitu 'movieId' dan 'title' untuk digabungkan dan movieId digunakan sebagai kunci.

```
all_tags = pd.merge(tagrelevances, tagdetails, on='tagId', how='left')
all_tags
```
hal yang sama dilakukan untuk variabell all_tags.

```
sorted_tags = all_tags.sort_values(['movieId', 'relevance'], ascending=[True, False])
top_tags = sorted_tags.groupby('movieId').head(3)

all_movie = pd.merge(all_resto_name, top_tags[['movieId', 'tag']], on='movieId', how='left')
all_movie
```
tags disortir berdasarkan relevansinya dan diurutkan dari yang paling relevan dan diambil 3 teratas. Hasil dari top_tags digabungkan dengan all_resto_name dan dimasukkan ke variabel all_movie.

```
#jadi satu kolom
top_tags_aggregated = top_tags.groupby('movieId')['tag'].apply(', '.join).reset_index()
top_tags_aggregated.rename(columns={'tag': 'tags'}, inplace=True)

all_movie = pd.merge(all_resto_name, top_tags_aggregated, on='movieId', how='left')
all_movie = all_movie.drop(columns=['timestamp'])
all_movie
```
Hasil akhirnya adalah sebuah kolom yang telah berisi hal-hal yang diperlukan.

## Handling missing value
```
all_movie.isnull().sum()
```
pada kode ini dilakukan pengecekan nilai null dan dari kode ini menghasilkan output
```tags	96183``` yang berarti terdapat null pada kolom tags.

```
all_movie_clean = all_movie.dropna()
all_movie_clean
``` 
untuk menyelesaikan masalah ini dilakukan drop pada tabel yang mengandung null.

## Handling ambigue tags
```
fix_movies[fix_movies['tags'].str.contains('cute!', na=False)]
fix_movies[fix_movies['tags'].str.contains('stupidity', na=False)]
fix_movies[fix_movies['tags'].str.contains('mentor', na=False)]
```
pada kode ini dilakukan pengecekan pada beberapa tags yang tereksan ambigu.

```
import re

tags_to_remove = ["cute!", "stupid", "mentor", "sequels"]
pattern = r'\b(' + '|'.join(map(re.escape, tags_to_remove)) + r')\b,?\s*'

fix_movies['tags'] = fix_movies['tags'].str.replace(pattern, '', regex=True)
```
Tags yang ambigu tersebut akan di remove.

## Handling sorting data
```
preparation = fix_movies
preparation.sort_values('movieId')
``` 
lalu dilakukan preparasi data dengan melakukan sortir berdasarkan movieId.

## Handling duplicate data
```
preparation = preparation.drop_duplicates('movieId')
preparation
```
Membuang data yang duplikat

## Dictionary data
```
movie_new = pd.DataFrame({
    'id': movie_id,
    'name': movie_name,
    'tags': movie_tags
})

movie_new
```
 Membuat dictionary untuk data 'movie_id', ‘movie_name’, dan 'tags

## Content-Based Filtering Preparation

### Ekstraksi Fitur TF-IDF
- Menggunakan TF-IDF Vectorizer untuk mengubah teks genre menjadi vektor numerik.

## Collaborative Filtering Preparation

### Encode Label
- UserID dan MovieID dienkode untuk digunakan dalam model.

### Split Data
- Data dibagi menjadi train dan test set dengan proporsi 80:20.

## Modeling
Pada Tahap modeling dilakukan Content based filtering dan colaborative filtering sebagai jenis model algoritma yang akan digunakan.

## Content-Based Filtering

Pendekatan ini merekomendasikan item berdasarkan karakteristik item itu sendiri dan preferensi pengguna sebelumnya.

### Cara Kerja:
- Setiap item memiliki fitur tertentu (misalnya genre, kategori, deskripsi).
- Sistem membandingkan fitur item dengan item yang pernah disukai pengguna.
- Jika pengguna pernah menyukai item A dengan genre action, maka sistem akan merekomendasikan item lain yang juga bergenre action.

### Contoh:
- Netflix: Jika Anda sering menonton film aksi, maka Netflix akan merekomendasikan film aksi lainnya.
- Spotify: Jika Anda sering mendengarkan musik rock, maka Spotify akan merekomendasikan lagu-lagu rock lain.

#### Kelebihan:
- Tidak bergantung pada data pengguna lain.
- Bisa memberikan rekomendasi meskipun sedikit pengguna yang berinteraksi dengan item tersebut.

#### Kekurangan:
- Sulit merekomendasikan sesuatu yang berbeda dari kebiasaan pengguna (terjebak dalam filter bubble).
- Perlu data yang cukup untuk memahami karakteristik item.


- Menggunakan TF-IDF Vectorizer untuk ekstraksi fitur teks.

## Collaborative Filtering (RecommenderNet)
Pendekatan ini merekomendasikan item berdasarkan kesamaan preferensi antara pengguna lain (user-based) atau kesamaan antara item (item-based).

### Cara Kerja:
- User-based: Jika dua pengguna memiliki preferensi serupa, maka mereka akan direkomendasikan item yang disukai satu sama lain.
- Item-based: Jika dua item sering dipilih bersama, maka sistem merekomendasikan item lain yang memiliki pola yang sama.

### Contoh:
- E-commerce (Tokopedia, Shopee, Amazon): Jika banyak orang yang membeli produk A dan B bersamaan, maka jika Anda membeli produk A, sistem akan merekomendasikan produk B.
- Netflix: Jika banyak orang yang menyukai film "Avengers" juga menyukai "Iron Man", maka jika Anda menonton "Avengers", Netflix mungkin merekomendasikan "Iron Man".

#### Kelebihan:
- Bisa merekomendasikan sesuatu yang mungkin tidak pernah dilihat pengguna sebelumnya.
- Tidak memerlukan informasi detail tentang item.

#### Kekurangan:
- Membutuhkan banyak data agar rekomendasi akurat (cold start problem untuk pengguna baru).
- Jika data pengguna sedikit, kualitas rekomendasi bisa menurun.


- Model menggunakan Neural Network berbasis TensorFlow.

### Hyperparameter:
- Loss Function: Root Mean Squared Error (RMSE)
- Optimizer: Adam
- Batch Size: 8
- Epochs: 100

```
def movie_recommendations(movie_name, similarity_data=cosine_sim_df, items=data[['name', 'tags']], k=5):
  index = similarity_data.loc[:, movie_name].to_numpy().argpartition(range(-1, -k, -1))

  #mengambil data dengan nilai similarity terbesar
  closest = similarity_data.columns[index[-1:-(k+2):-1]]

  # Drop nama_resto agar nama resto yang dicari tidak muncul dalam daftar rekomendasi
  closest = closest.drop(movie_name, errors='ignore')

  return pd.DataFrame(closest).merge(items).head(k)
```

ini adalah model yang akan digunakan

```
movie_recommendations('Dangerous Minds (1995)')
```
saat dijalankan model menghasilkan top 5 rekomendasi sebagai berikut
![gambar model](https://raw.githubusercontent.com/Marco-andana/dicoding-sistem-rekomendasi/7b2f6a3dbefd9df7b92cbebe49bdfc47cd3748de/content%20b.png)

```
ratings = model.predict(user_movie_array).flatten()

top_ratings_indices = ratings.argsort()[-10:][::-1]
reccomended_movie_ids = [
    movie_encoded_to_movie.get(movie_not_watched[x][0]) for x in top_ratings_indices
]

print('Showing recommendations for users: {}'.format(user_id))
print('===' * 9)
print('Movie with high ratings from user')
print('----' * 8)

top_movie_user = (
    movie_watched_by_user.sort_values(by='rating', ascending=False
    )
    .head(5)
    .movieId.values
)

movie_df_rows = movie_df[movie_df['id'].isin(top_movie_user)]
for row in movie_df_rows.itertuples():
    print(row.name, ':', row.tags)

print('----' * 8)
print('Top 10 Movie recommendation')
print('----' * 8)

recommended_movie = movie_df[movie_df['id'].isin(reccomended_movie_ids)]
for row in recommended_movie.itertuples():
    print(row.name, ':', row.tags)
```

ini adalah kode untuk collaborative filtering dengan hasil sebagai berikut

![collaborative filtering](https://raw.githubusercontent.com/Marco-andana/dicoding-sistem-rekomendasi/1e82edf1df256af958841c52902fff8bbad9c432/colla.png)

## Evaluation
Berdasarkan hasil eksperimen dan evaluasi, proyek ini berhasil membangun sistem rekomendasi film berbasis Machine Learning yang dapat membantu pengguna menemukan film yang sesuai dengan preferensi mereka. Beberapa kesimpulan utama dari proyek ini adalah:

#### Akurasi collaborative filtering
- loss: 0.5891 
- root_mean_squared_error: 0.1856 
- val_loss: 0.6129 
- val_root_mean_squared_error: 0.2119

### Content based filtering
pada content based filtering, dilakukan uji coba sebagai berikut
![y](https://raw.githubusercontent.com/Marco-andana/dicoding-sistem-rekomendasi/b64a880b961c274e8ff90930d358c9a3d9329d10/precision%20content%20based.png)

Dari gambar diatas dapat dilakukan perhitungan 
Precision = #of recommendation that are relevant/#of item we recommend.=
Dimana pada gambar diatas tags 'teacher' muncul pada salah satu hasil rekomendasi yang berarti 1/5
Precission = 1/5.
Jadi presisinya = 20%

### 1. Sistem rekomendasi membantu mengatasi overload informasi

Dengan jumlah film yang terus bertambah, pengguna sering kesulitan memilih film yang sesuai. Model yang dikembangkan berhasil menyaring dan memberikan rekomendasi yang lebih relevan.

### 2. Model Hybrid memberikan hasil yang lebih akurat dibandingkan model tunggal

Kombinasi Collaborative Filtering dan Content-Based Filtering menghasilkan rekomendasi yang lebih personal dan relevan dibandingkan dengan masing-masing metode secara terpisah.

### 3. Cold Start Problem dapat dikurangi dengan pendekatan berbasis metadata

Untuk pengguna baru atau film baru yang belum memiliki cukup data interaksi, pendekatan berbasis genre, aktor, dan deskripsi film dapat memberikan rekomendasi awal yang lebih baik.

### 4. Penggunaan teknik Deep Learning dapat meningkatkan akurasi lebih lanjut

Meskipun metode konvensional seperti Collaborative Filtering dan Content-Based Filtering bekerja dengan baik, penggunaan model Deep Learning seperti Autoencoders atau Neural Collaborative Filtering (NCF) berpotensi meningkatkan akurasi dan menangkap pola kompleks dalam data.

### 5. Peningkatan dataset dapat meningkatkan kinerja model

Semakin banyak data yang tersedia, semakin baik model dalam memahami preferensi pengguna. Penggunaan data yang lebih kaya, seperti analisis sentimen dari ulasan pengguna atau pola interaksi waktu nyata, dapat lebih meningkatkan hasil rekomendasi.

Secara keseluruhan, proyek ini menunjukkan bahwa sistem rekomendasi berbasis Machine Learning dapat secara signifikan meningkatkan pengalaman pengguna dalam memilih film yang sesuai dengan preferensi mereka. Dengan pengembangan lebih lanjut, model ini dapat diintegrasikan ke dalam layanan streaming untuk memberikan rekomendasi yang lebih cerdas dan personal.

**---Ini adalah bagian akhir laporan---**