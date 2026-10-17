# Tukang Cerita Terbalik

Game puzzle cerita berbahasa Indonesia. Pemain melihat akhir cerita terlebih dahulu, lalu menyusun kartu kejadian secara mundur hingga menemukan titik awal.

**[Mainkan demo](https://tukang-serita-terbalik.netlify.app)**

## Fitur

- Lima level bertema Indonesia: Warung, Kos-kosan, Angkot, Pasar, Pesantren.
- Kartu kejadian diacak, dengan urutan benar dan kartu jebakan.
- Gulung Balik maksimal tiga kali per permainan untuk membatalkan langkah.
- Skor satu sampai tiga bintang berdasarkan kesalahan.
- Rekor bintang terbaik per level disimpan di localStorage. Game tetap berjalan jika penyimpanan browser tidak tersedia.
- Bagikan hasil melalui tombol WhatsApp; pengunjung meninjau dan mengirim pesan sendiri.
- Tampilan scrapbook yang menyesuaikan layar HP dan komputer, dengan ilustrasi serta font lokal.

## Teknologi

HTML, CSS, dan JavaScript murni, tanpa framework, backend, atau proses build. Data cerita tertanam sebagai JSON dalam blok script ber-ID `level-data` di `index.html`.

## Menjalankan

Unduh atau clone repository, lalu buka `index.html` di browser modern. Pertahankan folder `assets/` di sebelahnya. Untuk perilaku penyimpanan yang konsisten, jalankan melalui server statis lokal atau hosting web.

Gambar dan font tersedia lokal sehingga permainan tidak memerlukan CDN. Berbagi hasil melalui WhatsApp memerlukan koneksi internet. Progres tersimpan per browser dan alamat situs; tidak tersinkron antarperangkat dan dapat hilang jika data browser dibersihkan.

## Struktur

`index.html` — tampilan, logika permainan, dan data lima level.  
`assets/` — lima ilustrasi WebP, font Caveat, dan lisensi font.

## Menambah cerita

Edit array `levels` di blok JSON. Setiap level memiliki ID unik, tema, judul, kalimat akhir, daftar kartu, rantai urutan benar, dan lokasi gambar. Rantai disimpan dari awal ke akhir; pemain memilihnya dari akhir ke awal. Implementasi saat ini memakai satu rantai valid per level.

## Deploy

Unggah `index.html` dan folder `assets/` ke hosting statis seperti Netlify. Tidak diperlukan perintah build. Jika alamat demo berubah, perbarui URL pada fungsi `whatsappMessage` dan tautan demo di README ini.

## Proses pengembangan

Proyek pribadi Alfa Tabi Mawarid, dikembangkan melalui arahan konsep, permintaan fitur, dan iterasi bersama asisten AI. Kode dan ilustrasi dibuat dengan bantuan AI.

## Catatan validasi

Pada percakapan pengembangan, kedua versi (HTML mandiri dan folder) dilaporkan lulus pengujian offline lima level, pemuatan gambar/font, penyelesaian rantai, simpan rekor, serta format berbagi WhatsApp. Pengemasan repository ini memeriksa ulang sintaks JavaScript dan kelengkapan referensi aset; tidak menjalankan ulang pengujian browser tersebut.

## Font dan lisensi

Font Caveat disertakan dalam bentuk subset WOFF2. Lisensi SIL Open Font License tersedia di [assets/OFL.txt](assets/OFL.txt). Repository ini belum menetapkan lisensi terpisah untuk kode dan ilustrasi game.
