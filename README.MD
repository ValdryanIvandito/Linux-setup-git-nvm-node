# Panduan Setup Linux Ubuntu untuk Developer Pemula

Berikut ini adalah panduan yang sangat mudah diikuti oleh teman-teman peserta bootcamp yang sedang belajar Linux pertama kali. Ikuti langkah-langkah di bawah ini untuk menginstal **Git**, **NVM**, **NodeJS**, **VSCode**, **Slack**, dan **Zoom Workspace**.

---

## Persyaratan

Panduan ini diperuntukkan bagi teman-teman yang sudah berhasil menginstal sistem operasi Linux berbasis **Debian** seperti contohnya **Ubuntu**, **Linux Mint**, dan **AnduinOS**.

---

## Langkah - Langkah

> ⚠️ **PETUNJUK PENTING: HARAP DIBACA DENGAN SAKSAMA!**

- *Copy & paste* semua perintah-perintah di bawah ini.
- Walaupun belum mengerti, **tidak masalah** — teman-teman bisa mempelajarinya nanti dengan *googling* tanya *AI* atau eksplorasi mandiri.
- Setiap menggunakan perintah **sudo**, teman-teman akan diminta memasukkan **password admin** yang telah teman-teman buat ketika pertamakali menginstal Linux.

---

### Step-1: Buka Terminal

**Terminal** adalah aplikasi berbasis teks yang digunakan untuk menjalankan perintah di sistem operasi Linux.

Dengan terminal, kita bisa:
- Menginstal aplikasi
- Mengelola file
- Menjalankan program

**Cara membuka terminal:**
- Tekan `Ctrl + Alt + T`
- Atau cari **"Terminal"** di menu aplikasi

---

### Step-2: Update Daftar Paket Aplikasi

```bash
sudo apt update
```

Perintah ini digunakan untuk **memperbarui daftar repository aplikasi** agar sistem mengetahui versi terbaru dari paket yang tersedia.

> *(Petunjuk: Ketika menggunakan sudo, teman-teman diminta untuk memasukkan password admin yang dibuat saat instalasi Linux.)*

---

### Step-3: Instalasi Curl

```bash
sudo apt install curl
```

**Curl** adalah tools yang digunakan untuk mengambil data dari internet melalui terminal (misalnya untuk download script atau API).

Setelah proses selesai, verifikasi instalasi:

```bash
curl --version
```

> *(Petunjuk: Jika berhasil, terminal akan menampilkan versi curl. Jika belum muncul, tutup terminal lalu buka kembali dan jalankan ulang perintah tersebut.)*

---

### Step-4: Instalasi Git

```bash
sudo apt install git
```

**Git** adalah sistem *version control* yang digunakan untuk mengelola perubahan kode dan kolaborasi dalam pengembangan software.

Verifikasi instalasi:

```bash
git --version
```

> *(Petunjuk: Jika berhasil, akan muncul versi Git. Jika belum, restart terminal dan coba lagi.)*

---

### Step-5: Instalasi NVM

Pada langkah ini kita akan menggunakan **curl** untuk menginstal **NVM (Node Version Manager)**.

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

> *(Catatan: Versi `v0.39.7` adalah versi stabil saat ini. Silakan cek versi terbaru di GitHub jika diperlukan.)*

**NVM** digunakan untuk:
- Menginstal Node.js
- Mengelola banyak versi Node.js dalam satu komputer

Setelah instalasi selesai, jalankan:

```bash
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

Perintah ini memastikan **NVM aktif di sesi terminal saat ini**.

Verifikasi instalasi:

```bash
nvm --version
```

> *(Petunjuk: Jika berhasil, akan muncul versi NVM.)*

---

### Step-6: Instalasi NodeJS

**Node.js** adalah runtime JavaScript yang digunakan untuk menjalankan JavaScript di luar browser.

Install Node.js menggunakan NVM:

```bash
nvm install 24.14.1
```

Verifikasi instalasi:

```bash
node --version
```

> *(Petunjuk: Jika berhasil, akan muncul versi Node.js.)*

> 💡 *Saran:* Sangat dianjurkan untuk mempelajari perintah-perintah NVM seperti:
> - `nvm list`
> - `nvm use`
> - `nvm install <version>`

---

### Step-7: Instalasi VSCode, Slack, dan Zoom

Silakan download terlebih dahulu ketiga installer berikut ini:

[Link Download VScode](https://code.visualstudio.com/thank-you?dv=linux64_deb)
[LInk Download Slack](https://slack.com/downloads/instructions/linux?ddl=1&build=deb)
[Link Download Zoom](https://zoom.us/download?os=linux)

(Petunjuk: Ketika klik Link Download Zoom akan diarahkan kesebuah halaman download scroll kebawah pilh linux type Ubuntu lalu klik Download)

Setelah ketiga instaler sudah di download mari kita masuk ke folder Downloads melalui terminal. Buka kembali terminal, lalu ketikan perintah berikut untuk memastikan posisi teman-teman sedang berada di (/home/'nama_user'):

```bash
pwd
```
Setelah itu akan muncul contoh hasil seperti ini: 
/home/ivandito

Kemudian kita cek lagi ada folder apa saja, ketikan perintah berikut:

```bash
ls
```

Setelah itu akan muncul contoh hasil seperti ini: 
Desktop    Downloads  Music     Public     Videos
Documents  KodingUp   Pictures  Templates

Kemudian kita akan masuk ke folder Downloads, karena ketiga instaler yang telah kita download berada disitu, ketikan perintah berikut:

```bash
cd Downloads
```

Sekarang lokasi teman-teman harusnya berada di (/home/'nama_user'/Downloads) Kemudian kita cek lagi untuk memastikan apakah ketiga installer itu ada di folder Download, ketikan perintah berikut:

```bash
ls
```

Setelah itu akan muncul contoh hasil seperti ini: 
code_1.114.0-1775036290_amd64.deb  zoom_amd64.deb
slack-desktop-4.47.69-amd64.deb

(Petunjuk: Semua instaler aplikasi Linux berbasis Debian seperti Ubuntu memiliki extention .deb)

Akhirnya ketiga instaler sudah berhasil teman-teman download, mari kita selesaikan tahap terakhir instalasi. Jalankan perintah instalasi berikut ini satu per satu. 

(Petunjuk: Pastikan lokasi teman-teman berada di /home/'nama_user'/Downloads menggunakan perintah pwd)

Instalasi VSCode

```bash
sudo apt install ./code_1.114.0-1775036290_amd64.deb
```

Instalasi Slack

```bash
sudo apt install ./slack-desktop-4.47.69-amd64.deb
```

Instalasi Zoom

```bash
sudo apt install ./zoom_amd64.deb
```

---

## Verifikasi Semua Instalasi

Jalankan perintah berikut:

```bash
git --version
nvm --version
node --version
```

Contoh output:
```
git version 2.xx.x
0.xx.x
vxx.xx.x
```

> *(Catatan: Versi bisa berbeda, itu normal.)*

Untuk aplikasi GUI seperti:
- **VSCode**
- **Slack**
- **Zoom**

Silakan buka melalui **Application Menu**.

---

## 🎉 Selamat!

**CONGRATULATIONS!** 🎉  
Teman-teman telah berhasil menginstal dan menyiapkan environment dasar untuk menjadi seorang developer.

Terus semangat belajar dan eksplorasi! 🚀

---

## Author

**Valdryan Ivandito**  
Peserta **KodingUp Batch-2**
 