# 🦅 Pegal Linux V2

## 🚀 Jalankan Secara Lokal

## 📖 Tentang Proyek

**Pegal Linux V2** adalah distribusi Linux hasil kustomisasi dari **Garuda Linux (Arch)** yang dirancang khusus untuk kebutuhan **Engineering** dan  **Internet of Things (IoT)** .

Proyek ini bertujuan untuk menyediakan lingkungan kerja yang siap pakai ( *out-of-the-box* ) dengan antarmuka yang modern, performa tinggi berkat kernel  **Linux Zen** , dan keamanan data terjamin melalui sistem snapshot  **BTRFS** .

## ✨ Fitur Utama

### 🛠️ Engineering Ready

Dilengkapi dengan *pre-installed tools* untuk produktivitas coding dan hardware:

* **Development:** Visual Studio Code, Arduino IDE, Git.
* **Networking:** Wireshark, Nmap, PuTTY, Net-tools.
* **Multimedia:** OBS Studio, VLC Media Player, GIMP.

### 🎨 Visual Identity (Branding)

* **Boot Splash:** Tema Plymouth kustom **"Aregression V2"** yang elegan.
* **Bootloader:** GRUB Menu dengan *background* kustom dan manajemen *entry* yang rapi.
* **Desktop:** KDE Plasma dengan tema **Sweet-Dark** (Neon/Cyberpunk) + Icon BeautyLine.
* **Terminal:** Integrasi **Fastfetch** dengan Logo ASCII Art Kustom & MOTD Statis.

### 🛡️ Keamanan & Stabilitas

* **Snapshot BTRFS:** Fitur *Time Travel* yang memungkinkan pemulihan sistem instan dari menu GRUB jika terjadi kerusakan ( *Kernel Panic* ).
* **Kernel Zen:** Dioptimalkan untuk responsivitas desktop dan gaming/multimedia.

## 🚀 Instalasi & Penggunaan

### Prasyarat

* USB Flashdrive (Min. 8GB).
* Software Flash (Rufus/Balena Etcher).
* Sistem dengan dukungan UEFI (Direkomendasikan).

## 🚀 Instalasi & Penggunaan

### Prasyarat

* USB Flashdrive (Min. 8GB).
* Software Flash (Rufus/Balena Etcher).
* Sistem dengan dukungan UEFI (Direkomendasikan).

### Cara Install Aplikasi Tambahan

Gunakan script otomatis yang telah kami sediakan untuk menginstal paket-paket esensial pasca-instalasi.

1. **Clone Repository ini:**
   ```
   git clone [https://github.com/Rhyred/Pegal-Linux-V2.git](https://github.com/Rhyred/Pegal-Linux-V2.git)
   cd Pegal-Linux-V2
   ```
2. **Jalankan Script Installer:**
   ```
   chmod +x install-apps.sh
   ./install-apps.sh
   ```
3. **Manual Install (via Paru):**
   ```
   paru -S <nama_paket>
   # Contoh: paru -S visual-studio-code-bin
   ```

### Cara Mengganti Tema Boot (Plymouth)

Jika ingin mengubah tema boot splash, gunakan perintah berikut (Wajib Rebuild Dracut):

```
sudo plymouth-set-default-theme <nama_tema>
sudo dracut -f --regenerate-all --force
```

## 📸 Tangkapan Layar

| **Boot Splash**   | **Desktop Environment** |
| ----------------------- | ----------------------------- |
|                         |                               |
| *Tema Aregression V2* | *KDE Plasma Sweet-Dark*     |

| **Terminal (Fastfetch)** | **GRUB Menu**   |
| ------------------------------ | --------------------- |
|                                |                       |
| *Custom ASCII Art*           | *Custom Background* |

> *Catatan: Ganti placeholder di atas dengan link gambar asli dari screenshot Anda.*

## 📂 Struktur Repositori

```
.
├── 📂 assets/              # Aset gambar (Logo, Wallpaper, Icon)
├── 📂 scripts/             # Script instalasi & konfigurasi otomatis
│   └── install-apps.sh     # Script installer aplikasi
├── 📂 configs/             # File konfigurasi sistem (Backup)
│   ├── grub                # Config /etc/default/grub
│   ├── plymouth            # Config tema plymouth
│   └── fastfetch           # Config jsonc & logo ascii
├── packages.list           # Daftar paket aplikasi
├── Manual_OS.pdf           # Panduan Pengguna Lengkap
└── README.md               # Dokumentasi Proyek
```

## 👥 Kredit & Tim Pengembang

Proyek ini dikembangkan sebagai tugas besar mata kuliah  **Sistem Operasi - ITENAS Bandung** .

**Tim Pengembang:**

* **Robi Rizki Permana**- *Lead Developer & System Architect*
* **Aditya Luthfi** - *UI/UX Designer*
* **Akbar Dhika A** - *Documentation & Testing*
* **Buga Nesha A** - *Research & Asset Manager*
* **Dila Amelisa S** - Donatur 

**Special Thanks to:**

* [Garuda Linux Team](https://garudalinux.org/ "null") - Untuk basis OS yang luar biasa.
* [Arch Linux Community](https://archlinux.org/ "null") - Untuk dokumentasi Wiki yang lengkap.
* **Dosen Pengampu:** Diash Firdaus S.Kom M.T

---

Made with ❤️ and ☕ by Mas Agan using Arch Linux