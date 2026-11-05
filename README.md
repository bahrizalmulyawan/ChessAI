# Chess AI Lab

**Dokumentasi Bahasa Indonesia dan English Documentation**

---

# 🇮🇩 Bahasa Indonesia

## Deskripsi

**Chess AI Lab** adalah prototipe permainan catur berbasis HTML, CSS, dan JavaScript. Aplikasi ini menyediakan mode pertandingan **Manusia vs AI** dan **AI vs AI**, serta beberapa profil model AI untuk eksperimen pemilihan langkah.

Aplikasi berjalan langsung di browser tanpa instalasi dependensi atau server khusus.

## Fitur

- Papan catur 8 × 8 dengan bidak putih dan hitam.
- Pemilihan bidak dan kotak tujuan melalui klik atau tap.
- Sorotan kotak tujuan yang tersedia untuk langkah bidak yang dipilih.
- Mode **Manusia vs AI** dan **AI vs AI**.
- Pilihan profil model: **Perceptron**, **CNN**, **SNN**, dan **Triple**.
- Riwayat pergerakan bidak dengan koordinat dan panah, misalnya `♙ E2 → E4`.
- Sorotan langkah terakhir dan visualisasi arah perpindahan bidak.
- Panel visualisasi neuron, output neuron, statistik, dan catatan simulasi.
- Penyimpanan data AI pada `localStorage` browser.
- Ekspor data ke `memory.json` dan `learn.json`, serta impor `memory.json`.

## Cara Menjalankan

1. Unduh file `chess_ai_lab_catur_revisi.html`.
2. Buka file tersebut menggunakan browser modern, seperti Chrome, Firefox, Edge, atau Safari.
3. Aplikasi dapat langsung digunakan. Tidak diperlukan proses build, package manager, atau koneksi internet.

Simpan `README.md` dan file HTML di folder proyek yang sama agar dokumentasi mudah ditemukan.

## Cara Bermain

### Manusia vs AI

1. Pilih mode **Manusia vs AI**.
2. Klik **Mulai**.
3. Pilih salah satu bidak putih.
4. Pilih kotak tujuan yang disorot.
5. AI akan merespons dengan langkah hitam.

### AI vs AI

1. Pilih mode **AI vs AI**.
2. Tentukan model untuk sisi putih dan hitam melalui pilihan model yang tersedia.
3. Klik **Mulai** untuk menjalankan pertandingan otomatis.
4. Gunakan **Jeda** untuk menghentikan sementara pertandingan.
5. Gunakan **Reset skor** untuk mengatur ulang papan dan statistik pertandingan.

### Riwayat Pergerakan Bidak

Setiap langkah dicatat pada panel **History pergerakan bidak**. Riwayat menampilkan koordinat petak awal dan tujuan menggunakan simbol panah, contohnya `♙ E2 → E4`. Visualisasi pergerakan menampilkan perpindahan terakhir.

## Model AI dan Penyimpanan

Aplikasi menyediakan profil **Perceptron**, **CNN**, **SNN**, dan **Triple**. Profil tersebut memengaruhi pemilihan kandidat langkah AI. Mesin pemilihan langkah menggunakan pencarian minimax sederhana dan evaluasi material.

Data bobot dan statistik model disimpan pada penyimpanan lokal browser (`localStorage`).

Fitur ekspor menghasilkan dua file:

- `memory.json` — bobot dan parameter model.
- `learn.json` — ringkasan statistik pembelajaran.

Gunakan tombol **Impor memory.json** untuk memuat file memory yang sesuai dengan versi dan struktur model aplikasi.

## Batasan Implementasi

- Aplikasi ini merupakan prototipe eksperimen, bukan mesin catur kompetitif.
- Aturan khusus **rokade** dan **en passant** belum diimplementasikan.
- Promosi pion saat ini otomatis menjadi ratu.
- Panel neuron dan beberapa metrik pembelajaran merupakan visualisasi eksperimental dari kerangka proyek. Visualisasi tersebut tidak membuktikan bahwa seluruh model neural telah dilatih atau mengevaluasi posisi catur secara penuh.
- Hasil pemilihan langkah AI dapat bervariasi karena terdapat unsur acak dalam pemilihan kandidat.

## Struktur Proyek

```text
project/
├── chess_ai_lab_catur_revisi.html   # File aplikasi utama
└── README.md                        # Dokumentasi proyek
```

## Teknologi

- HTML5
- CSS3
- JavaScript (Vanilla)
- HTML Canvas API
- Browser `localStorage` dan Blob API untuk penyimpanan serta ekspor data

## Kredit

**Author:** BAHRIZAL HELMI MULYAWAN

---

# 🇬🇧 English

## Description

**Chess AI Lab** is a chess game prototype built with HTML, CSS, and JavaScript. It provides **Human vs AI** and **AI vs AI** match modes, along with several AI model profiles for move-selection experiments.

The application runs directly in a web browser. No dependency installation or dedicated server is required.

## Features

- 8 × 8 chessboard with white and black pieces.
- Select pieces and destination squares by clicking or tapping.
- Highlights available destination squares for the selected piece.
- **Human vs AI** and **AI vs AI** game modes.
- AI model profiles: **Perceptron**, **CNN**, **SNN**, and **Triple**.
- Piece movement history with square coordinates and an arrow, for example `♙ E2 → E4`.
- Highlights the latest move and visualizes the piece's movement direction.
- Neuron visualization, neuron output, statistics, and simulation log panels.
- Saves AI data in the browser's `localStorage`.
- Exports data to `memory.json` and `learn.json`, and imports `memory.json`.

## Getting Started

1. Download `chess_ai_lab_catur_revisi.html`.
2. Open the file in a modern browser such as Chrome, Firefox, Edge, or Safari.
3. The application is ready to use. No build process, package manager, or internet connection is required.

Keep `README.md` and the HTML file in the same project folder for convenient documentation access.

## How to Play

### Human vs AI

1. Select **Human vs AI** mode.
2. Click **Start**.
3. Select one of the white pieces.
4. Select one of the highlighted destination squares.
5. The AI will respond by making a move with the black pieces.

### AI vs AI

1. Select **AI vs AI** mode.
2. Choose the model for the white and black sides using the available model selectors.
3. Click **Start** to run the match automatically.
4. Use **Pause** to temporarily stop the match.
5. Use **Reset Score** to reset the board and match statistics.

### Piece Movement History

Every move is recorded in the **History pergerakan bidak** panel. The history displays the starting and destination squares using an arrow, for example `♙ E2 → E4`. The movement visualization shows the latest piece movement.

## AI Models and Data Storage

The application provides **Perceptron**, **CNN**, **SNN**, and **Triple** profiles. These profiles affect how the AI selects candidate moves. The move-selection engine uses a simple minimax search and material evaluation.

Model weights and statistics are stored in the browser's local storage (`localStorage`).

The export feature generates two files:

- `memory.json` — model weights and parameters.
- `learn.json` — a summary of learning statistics.

Use the **Impor memory.json** button to load a memory file that matches the application's version and model structure.

## Implementation Limitations

- This is an experimental prototype, not a competitive chess engine.
- Special chess rules for **castling** and **en passant** have not been implemented.
- Pawn promotion currently converts the pawn automatically into a queen.
- The neuron panel and some learning metrics are experimental visualizations retained from the project framework. They should not be interpreted as proof that every neural model has been trained or fully evaluates chess positions.
- AI move selection may vary because candidate selection includes a random element.

## Project Structure

```text
project/
├── chess_ai_lab_catur_revisi.html   # Main application file
└── README.md                        # Project documentation
```

## Technologies

- HTML5
- CSS3
- Vanilla JavaScript
- HTML Canvas API
- Browser `localStorage` and Blob API for data storage and export

## Credits

**Author:** BAHRIZAL HELMI MULYAWAN
