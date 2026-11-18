# Tugas Docker Minggu 9: Kontainerisasi Halaman Profil

Proyek ini berisi halaman profil saya yang dibungkus menjadi image Docker dan dijalankan sebagai container memakai nginx. Halaman berisi nama, NIM, tiga keahlian atau hobi, dan satu kalimat tentang container.

- Nama: Theresia Payung Allo
- NIM: 202557201015

## Cara Build

Jalankan perintah ini di dalam folder proyek untuk membuat image dari Dockerfile:

```
docker build -t profil-theresiapayungallo:1.0 .
docker images
```

Opsi `-t` memberi nama dan tag pada image. Tanda titik di akhir berarti folder saat ini dipakai sebagai build context.

## Cara Run

Jalankan image sebagai container di port 8082:

```
docker run -d --name profil-theresiapayungallo -p 8082:80 profil-theresiapayungallo:1.0
docker ps
```

Opsi `-d` menjalankan container di latar belakang, `--name` memberi nama container, dan `-p 8082:80` meneruskan port 8082 di komputer ke port 80 di container.

Setelah itu buka http://localhost:8082 di browser.

## Screenshot

Halaman profil di browser:

![Halaman profil](screenshot-browser.png)

Terminal setelah `docker ps` dan `docker images`:

![Terminal](screenshot-terminal.png)
