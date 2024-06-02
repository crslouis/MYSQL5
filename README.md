## Profil
| Variable | Isi |
| -------- | --- |
| **Nama** | CARLOS LOUIS FERNANDO |
| **NIM** | 312310458 |
| **Kelas** | TI.23.A5 |
| **Mata Kuliah** | Basis data |

# Soal Latihan Praktikum 

![alt text](screenshoot/T1.png)

![alt text](screenshoot/T3.png)

![alt text](screenshoot/T4.png)

![alt text](screenshoot/T5.png)

# Tabel mahasiswa
![alt text](screenshoot/H1.png)

# Tabel dosen
![alt text](screenshoot/H2.png)

# Tabel matakuliah
![alt text](screenshoot/H3.png)

# Tabel jadwal mengajar
![alt text](screenshoot/H4.png)

# Tabel Krsmahasiwa
![alt text](screenshoot/H5.png)

## Latihan

- Lakukan join table Mahasiswa dan Dosen.
- Lakukan join tabel Matakuliah dan Dosen.
- Lakukan join table JadwalMengajar, Dosen, dan Matakuliah.
- Lakukan join tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen.

## Buat Script SQL JOIN Table berdasarkan skema data diatas.

- Lakukan join table Mahasiswa dan Dosen.
![alt text](screenshoot/J1.png)
```
SELECT m.nim, m.nama, m.jk, d.nama AS 'Dosen PA'
FROM mahasiswa m
JOIN dosen d ON m.kd_ds = d.kd_ds;
```
- join
![alt text](screenshoot/J2.png)
```
SELECT Mahasiswa.nim, Mahasiswa.nama, Mahasiswa.jk, Dosen.nama AS "Dosen PA"
FROM Mahasiswa LEFT JOIN Dosen ON Dosen.kd_ds = Mahasiswa.kd_ds;
```

- Lakukan join tabel Matakuliah dan Dosen
![alt text](screenshoot/J3.png)
```
SELECT Matakuliah.kd_mk, Matakuliah.nama AS "Nama Matakuliah", Matakuliah.sks, Dosen.nama AS "Nama Dosen Pengampu"
FROM JadwalMengajar
LEFT JOIN Matakuliah ON JadwalMengajar.kd_mk = Matakuliah.kd_mk
LEFT JOIN Dosen ON JadwalMengajar.kd_ds = Dosen.kd_ds;

```
- Lakukan join table JadwalMengajar, Dosen, dan Matakuliah
![alt text](screenshoot/J4.png)
```
SELECT jm.kd_mk, mk.nama, mk.sks, d.nama AS 'Dosen Pengampu'
FROM jadwalmengajar jm
JOIN dosen d ON jm.kd_ds = d.kd_ds
JOIN matakuliah mk ON jm.kd_mk = mk.kd_mk;
```
-  join tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen
![alt text](screenshoot/J5.png)
```
SELECT km.kd_mk, mk.nama, mk.sks, d.nama AS 'Dosen Pengampu', jm.hari, jm.jam, jm.ruang
FROM krsmahasiswa km
JOIN mahasiswa m ON km.nim = m.nim
JOIN matakuliah mk ON km.kd_mk = mk.kd_mk
JOIN jadwalmengajar jm ON km.kd_mk = jm.kd_mk AND km.kd_ds = jm.kd_ds
JOIN dosen d ON jm.kd_ds = d.kd_ds;
```

### Buat laporan praktikum yang berisi, langkah-langkah praktikum beserta screenshot yang sudah dilakukan dalam bentuk dokumen.

## SELESAI <img align="center" alt="Ikhsan-Python" height="40" width="45" src="https://em-content.zobj.net/source/microsoft-teams/337/student_1f9d1-200d-1f393.png"> <img align="center" alt="Ikhsan-Python" height="40" width="45" src="https://em-content.zobj.net/thumbs/160/twitter/348/flag-indonesia_1f1ee-1f1e9.png">

