Pegal Linux V2 (Garuda Rani Edition)

Sistem operasi kustom berbasis Arch Linux — dirancang khusus untuk produktivitas Engineering & IoT. Ringan, estetis, dan siap pakai.

✨ Fitur Utama

🛠️ Engineering Ready: Dilengkapi pre-installed tools: VS Code, Arduino IDE, Wireshark, Git, dll.

🎨 Visual Identity: Boot Splash kustom (Plymouth Aregression V2), GRUB Theme, dan Desktop Sweet-Dark.

⚡ Performa Tinggi: Menggunakan Kernel Linux Zen untuk responsivitas maksimal.

🛡️ Keamanan Data: Sistem Snapshot BTRFS terintegrasi untuk pemulihan instan dari menu boot.

📟 Terminal Kustom: Integrasi Fastfetch dengan logo ASCII art khusus & MOTD statis.

🚀 Instalasi & Penggunaan

Sebelum mulai: pastikan Anda memiliki USB Flashdrive (min. 8GB) dan software flash (Rufus/Balena Etcher).

Persiapan

Unduh file ISO terbaru dari tab Releases.

Flash ke USB drive menggunakan Rufus/Etcher.

Boot PC melalui USB (mode UEFI direkomendasikan).

Pasca Instalasi (Opsional — untuk paket tambahan)

Clone repositori ini:

git clone [https://github.com/Rhyred/Pegal-Linux-V2.git](https://github.com/Rhyred/Pegal-Linux-V2.git)
cd Pegal-Linux-V2


Jalankan script installer otomatis:

chmod +x install-apps.sh
./install-apps.sh


Script akan otomatis menginstal paket-paket engineering tambahan via paru / pacman.

📁 Struktur Repositori (singkat)

pegal-linux-v2/
├── assets/             # Aset gambar (Logo, Wallpaper, Icon)
├── scripts/            # Script otomatisasi (install-apps.sh)
├── configs/            # File konfigurasi sistem (GRUB, Plymouth, Fastfetch)
├── packages.list       # Daftar paket aplikasi pre-installed
├── Manual_OS.pdf       # Panduan pengguna lengkap
└── README.md           # Dokumentasi ini


🎯 Cara Kerjanya (ringkas)

Booting: Sistem memuat kernel Zen dengan tema Plymouth kustom via Dracut.

Login: Masuk melalui SDDM dengan tema yang selaras.

Desktop: Lingkungan KDE Plasma yang sudah dikonfigurasi untuk workflow engineering.

Recovery: Jika terjadi error, gunakan menu "Garuda Linux Snapshots" di GRUB untuk rollback.

🔧 Konfigurasi Kustom

Tambahkan/Edit file konfigurasi berikut jika perlu:

Terminal (Fastfetch)

Lokasi: ~/.config/fastfetch/config.jsonc

// Contoh mengganti warna logo
"logo": {
    "source": "~/.config/fastfetch/logo.txt",
    "color": { "1": "cyan", "2": "white" }
}


Boot Splash (Plymouth)

Lokasi Tema: /usr/share/plymouth/themes/aregression_v2/

Untuk menerapkan perubahan tema:

sudo plymouth-set-default-theme <nama_tema>
sudo dracut -f --regenerate-all --force


📊 Spesifikasi Minimum

Processor: 64-bit Dual Core

RAM: 4 GB (8 GB direkomendasikan)

Storage: 30 GB ruang kosong

GPU: Mendukung OpenGL 3.3+

👥 Tim Pengembang

Tim Pegal Linux — Mahasiswa Informatika ITENAS:

[Nama Kamu/Rhyred] — Lead Developer & System Architect

[Nama Anggota 2] — UI/UX Designer

[Nama Anggota 3] — Documentation

[Nama Anggota 4] — Testing & QA

[Nama Anggota 5] — Asset Manager

Made with ❤️ and ☕ by Rhyred using Arch Linux