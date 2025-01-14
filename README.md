# Pemrograman Orientasi Objek

| UAS          | PEMROGRAMAN ORIENTASI OBJEK |
|--------------|-----------------|
| NAMA :       | Aaqilah Aathirah Sutisna| 
| NIM  :       | 312310621  | 
| Kelas  :     | TI.23.A6  | 

# Latihan OOP
![Latihan](https://github.com/user-attachments/assets/fd45527c-74c2-4175-8b21-920d88888c2d)

# Struktur
![Struktur](https://github.com/user-attachments/assets/3a97259f-9b3f-46a1-b4f3-f073242068e8)

Penjelasan :
1. clasess : Digunakan untuk output dari proses build.
2. controller : Menyimpan kelas-kelas yang bertanggung jawab untuk logika kontrol, yaitu mengatur aliran data antara model (data) dan view (tampilan).
3. model :  Menyimpan kelas-kelas yang merepresentasikan data atau entitas dalam aplikasi. Contohnya bisa berupa kelas seperti Mahasiswa atau Nilai.
4. view : Berisi kelas atau file yang mengatur tampilan antarmuka pengguna (UI). Bisa berupa teks pada konsol atau GUI berbasis Java seperti Swing atau JavaFX.

# Configurasi database di Mysql
mysql -uroot

``CREATE DATABASE akademik;``

``USE akademik;``

``CREATE TABLE mahasiswa (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nim VARCHAR(20) NOT NULL UNIQUE,
    nama VARCHAR(100) NOT NULL,
    jurusan VARCHAR(50) NOT NULL,
    angkatan VARCHAR(100) NOT NULL
);``

``CREATE TABLE nilai (
    id INT PRIMARY KEY AUTO_INCREMENT,
    mahasiswa_id INT NOT NULL,
    mata_kuliah VARCHAR(100) NOT NULL,
    semester INT NOT NULL,
    nilai CHAR(2),
    FOREIGN KEY (mahasiswa_id) REFERENCES mahasiswa(id)
    ON DELETE CASCADE
);``
