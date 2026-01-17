# Colab Image Upscaler Projects

Repositori ini berisi tiga notebook Google Colab untuk melakukan upscaling gambar menggunakan teknologi AI yang berbeda. Pilih notebook yang sesuai dengan kebutuhan Anda.

---

## 1. Real-ESRGAN Upscaler (`upsize.ipynb`)

Notebook ini menggunakan **Real-ESRGAN** dengan model `x2plus`. Sangat cepat dan cocok untuk upscaling umum (foto, anime, ilustrasi).

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dpk4212/Colab/blob/main/upsize.ipynb)

### 📋 Fitur Utama

- **Kecepatan Tinggi**: Proses upscaling sangat cepat.
- **Skala 2x**: Menggandakan resolusi gambar.
- **Otomasi**: Otomatis memindahkan file asli ke folder `done` setelah selesai.

### ⚙️ Konfigurasi Path (Google Drive)

Secara default, skrip ini menggunakan folder berikut di Google Drive Anda:

- **Input**: `/content/drive/MyDrive/source` (Simpan gambar yang ingin di-upscale di sini)
- **Output**: `/content/drive/MyDrive/result` (Hasil gambar akan muncul di sini)
- **Selesai**: `/content/drive/MyDrive/done` (File asli dipindahkan ke sini setelah sukses)

### 🛠️ Cara Mengubah Pengaturan

Anda dapat mengubah pengaturan berikut di dalam kode (Sel 3):

1.  **Format Input/Output**:
    - Ubah nama folder di variabel:
      ```python
      input_folder_name = "source"
      output_folder_name = "result"
      ```

2.  **Kualitas Gambar**:
    - Atur kualitas kompresi JPG (1-95) pada variabel:
      ```python
      jpg_quality = 95
      ```

---

## 2. Real-ESRGAN 4x Upscaler (`upsize4x.ipynb`)

Notebook ini menggunakan **Real-ESRGAN** dengan model `x4plus`. Cocok untuk memperbesar gambar lebih ekstrem (4x lipat).

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dpk4212/Colab/blob/main/upsize4x.ipynb)

### 📋 Fitur Utama

- **Skala 4x**: Memperbesar resolusi gambar hingga 4 kali lipat dengan detail tinggi.
- **Model RealESRGAN_x4plus**: Varian standar yang kuat untuk berbagai jenis gambar.
- **Otomasi**: Sama seperti versi 2x, file otomatis dipindahkan setelah selesai.

### ⚙️ Konfigurasi Path (Google Drive)

Secara default, skrip ini menggunakan folder yang sama dengan versi 2x:

- **Input**: `/content/drive/MyDrive/source`
- **Output**: `/content/drive/MyDrive/result`

---

## 3. HAT (Hybrid Attention Transformer) Upscaler (`upsizeHAT.ipynb`)

Notebook ini menggunakan **HAT** dengan model `Real_HAT_GAN_sharper`. Memberikan hasil yang **sangat tajam dan detail**, ideal untuk restorasi foto berkualitas tinggi.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dpk4212/Colab/blob/main/upsizeHAT.ipynb)

### 📋 Fitur Utama

- **Kualitas Premium**: Detail tekstur yang jauh lebih baik daripada Real-ESRGAN.
- **Auto-Move Background**: Menggunakan script latar belakang untuk memindahkan file ke Drive secara real-time.
- **Konfigurasi Tile**: Dioptimalkan dengan tile size 256 untuk keseimbangan kecepatan dan memori GPU.

### ⚙️ Konfigurasi Path (Google Drive)

Secara default, skrip ini menggunakan folder berikut:

- **Input**: `/content/drive/MyDrive/hatsource` (Simpan gambar di sini)
- **Output**: `/content/drive/MyDrive/hatoutput` (Hasil akan disalin ke sini)

### 🛠️ Cara Mengubah Pengaturan

Anda dapat mengubah pengaturan berikut di dalam kode:

1.  **Folder Input/Output** (Sel 1):

    ```python
    input_folder = '/content/drive/MyDrive/hatsource'
    output_folder_drive = '/content/drive/MyDrive/hatoutput'
    ```

2.  **Detail Konfigurasi** (Sel 3):
    - Skrip otomatis menyuntikkan konfigurasi `tile_size: 256` untuk performa stabil di Colab T4.
    - Model yang digunakan adalah `Real_HAT_GAN_sharper.pth`.

---

## 📝 Cara Penggunaan Singkat

1.  Klik tombol **Open in Colab** pada notebook yang diinginkan.
2.  Hubungkan ke Google Drive saat diminta (Mount Drive).
3.  Pastikan Anda telah membuat folder input di Google Drive dan mengisinya dengan gambar.
4.  Jalankan sel secara berurutan (Play button).
5.  Tunggu proses selesai dan cek folder output di Google Drive Anda.
