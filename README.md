# Muscle AI: Rekomendasi Jenis Latihan Gym 🏋️‍♂️💪

## Anggota Kelompok 3C 👥
- **Alif Naufal Fachrian** - 2209106108
- **Gerry Hasrom** - 2209106094
- **Muhammad Rizky Putra Pratama** - 2209106102
- **Zaky Syuhada** - 2209106073

## Deskripsi Proyek 📝
**Muscle AI** adalah aplikasi yang memberikan rekomendasi jenis latihan gym berdasarkan input kalori yang ingin dibakar dan jenis latihan yang dipilih. Jenis latihan yang tersedia meliputi:

- **Cardio** 🏃‍♂️
- **HIIT (High-Intensity Interval Training)** 🔥
- **Strength** 🏋️‍♀️
- **Yoga** 🧘‍♂️

Semakin banyak kalori yang ingin dibakar, semakin banyak latihan yang akan direkomendasikan. Pengguna dapat memilih latihan yang sesuai dengan tujuan mereka.

## Tujuan Aplikasi 🎯
Aplikasi **Muscle AI** bertujuan untuk membantu pengguna menentukan latihan gym yang sesuai berdasarkan jumlah kalori yang ingin dibakar dan jenis latihan yang dipilih. Dengan menggunakan metode **Deep Neural Network (DNN)**, model ini telah mencapai **akurasi MAE sebesar 78.5643**. Backend menggunakan **Django**, terintegrasi dengan aplikasi **Flutter** melalui endpoint yang diuji menggunakan **Postman**.

## Teknologi yang Digunakan 🖥️
- **Backend**: Django 🐍
- **Frontend**: Flutter 📱
- **Model**: Deep Neural Network (DNN) 🧠
- **Endpoint Testing**: Postman 🚀

## Kendala yang Dihadapi ⚠️
- **80%**: Masalah terkait endpoint Django dengan aplikasi Flutter, terutama terkait pembatasan akses **CORS** dan domain local tunnel.
- **10%**: Integrasi dengan model **Gemini API**.
- **5%**: Kendala pada controller bagian prediksi.
- **3%**: Penyesuaian tampilan antarmuka pengguna (UI).
- **2%**: Kendala motivasi (rasa malas wkwk) 😅.

## Cara Menjalankan Program ⚙️

### Persiapan
1. **Install dependencies Flutter**:
   - Jalankan `flutter pub get` terlebih dahulu.

2. **Menjalankan Server Django**:
   - Aktifkan environment dengan command:  
     `conda activate pakbmobile`
   - Jalankan server Django dengan command:  
     `python manage.py runserver`
   - Periksa output pada terminal, pastikan server berjalan pada `http://127.0.0.1:8000/`.

3. **Menjalankan Local Tunnel**:
   - Install **LocalTunnel** menggunakan command:  
     `npm install -g localtunnel`
   - Jalankan LocalTunnel dengan command:  
     `lt --port 8000 --subdomain gerry`
   - Jika domain tidak tersedia, ganti subdomain dan sesuaikan di **settings.py** serta endpoint di aplikasi Flutter.

4. **Pengujian Endpoint di Postman**:
   - Gunakan endpoint: `https://gerry.loca.lt/api/predict/` dengan metode **POST**.
   - Tambahkan header berikut:
     - `Content-Type`: `application/json`
     - `User-Agent`: `FlutterApp`
     - `bypass-tunnel-reminder`: `true`
   - Kode 200 menunjukkan berhasil, sedangkan kode 502 menandakan masalah server LocalTunnel.

5. **Menjalankan Aplikasi Flutter**:
   - Buka **main.dart** dan jalankan aplikasi menggunakan debugging atau tanpa debugging.
   - Jalankan aplikasi Flutter dengan command:  
     `flutter run`
   - Disarankan untuk menggunakan **Microsoft Edge** untuk hasil terbaik.

## Cara Menggunakan Aplikasi 🧑‍💻

1. **Registrasi Akun**: Buat akun baru di aplikasi.
2. **Login Akun**: Masuk dengan akun yang sudah didaftarkan.
3. **Masukkan Data Pribadi**: Isi data diri pengguna.
4. **Halaman Train**: Masukkan jumlah kalori yang ingin dibakar dan pilih jenis latihan yang sesuai.
5. **Add to Workout**: Pilih latihan untuk ditambahkan ke halaman **Workout** dan ikuti langkah-langkah dari **Gemini** untuk instruksi lebih lanjut.

---

## Informasi Kontak 📧

**GitHub Collaborators**:
- **Alif Naufal Fachrian**: [alnfl29](https://github.com/alnfl29)
- **Gerry Hasrom**: [GerryHasrom](https://github.com/GerryHasrom)
- **Muhammad Rizky Putra Pratama**: [tamaaja](https://github.com/tamaaja)
- **Zaky Syuhada**: [jisNOTmyname](https://github.com/jisNOTmyname)

**Email**:
- **Alif Naufal Fachrian**: aliffbatasa29@gmail.com
- **Gerry Hasrom**: gerryhasrom25@gmail.com
- **Muhammad Rizky Putra Pratama**: rizkyputra1206@gmail.com
- **Zaky Syuhada**: Zaonly881@gmail.com

## Catatan 📌
- Pastikan server Django berjalan dengan baik dan endpoint sudah diatur dengan benar di aplikasi Flutter.
- Untuk masalah terkait LocalTunnel, pastikan subdomain yang digunakan sudah valid dan sesuai dengan pengaturan pada **settings.py**.
- Gunakan Postman untuk memverifikasi endpoint dan pastikan aplikasi berfungsi dengan baik di semua tahap.
- Jika Gemini tidak memberikan respons, tapi bisa melakukan predict ganti api key, bisa aja karena api sudah habis credit harian.

Selamat mencoba, semoga aplikasi **Muscle AI** dapat membantu Anda mencapai tujuan fitness Anda! 🏆
