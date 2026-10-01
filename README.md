# qurio-cron

Penjadwal gratis buat Qurio (repo publik = menit GitHub Actions gratis).

Workflow `.github/workflows/tick.yml` manggil `https://orbitalid.site/qurio/app/api/cron/tick` tiap ±5 menit:
- kirim pengingat ayat pagi ke member yang jam pengingatnya udah lewat (maks 1x/hari per member)
- cek order Scalev lunas yang belum dapat lisensi Qurio, lalu terbitin + kirim email

Nggak ada secret di sini. Jadwal GitHub bisa telat beberapa menit, itu normal.
Ada langkah keepalive mingguan supaya jadwal nggak dimatiin GitHub waktu repo sepi.

Kode app ada di repo privat `orbitalid/qurio-app`.
