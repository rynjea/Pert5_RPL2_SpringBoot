# Data Mahasiswa Menggunakan SpringBoot
Spring Boot adalah framework Java berbasis Spring yang memudahkan pembuatan
aplikasi dengan konfigurasi otomatis (auto configuration), struktur standar, dan
dependensi yang sudah dikelola, sehingga developer bisa fokus pada logika aplikasi
tanpa repot mengatur konfigurasi manual.

Untuk langkah langkahnya kurang lebih sama seperti pertemuan sebelumnya, tetapi
untuk penjelasan kodenya seperti ini:
Program tersebut adalah aplikasi Spring Boot berbasis console yang terhubung ke
database MySQL untuk mengelola data mahasiswa. ModelMahasiswa adalah kelas
entity yang mewakili tabel mahasiswa di database, di dalamnya terdapat field seperti
npm, nama, semester, dan ipk dengan anotasi JPA seperti @Entity, @Table, @Id,
dan @GeneratedValue agar Hibernate dapat memetakan objek ke tabel.
MahasiswaRepository merupakan interface yang mewarisi JpaRepository, sehingga
otomatis menyediakan fungsi CRUD tanpa perlu menulis SQL.
MahasiswaController berperan sebagai pengelola logika aplikasi—menampilkan
menu, menampilkan seluruh data mahasiswa dari database menggunakan findAll(),
menambah data mahasiswa dengan save(), serta mengetes koneksi database. Kelas
utama Pertemuan5SpringBootApplication menjalankan aplikasi Spring Boot dan
memanggil menu melalui CommandLineRunner. Konfigurasi koneksi database
berada pada application.properties yang menyimpan URL MySQL, username,
password, serta pengaturan Hibernate (ddl-auto=update). Dependensi seperti Spring
Data JPA, Spring Web, dan MySQL Connector didefinisikan di pom.xml, sehingga
project dapat berjalan, terhubung ke database, dan melakukan CRUD menggunakan
Spring Boot. Secara keseluruhan, aplikasi ini adalah contoh penerapan Spring +
Hibernate berbasis console tanpa UI web, namun sudah mengikuti standar arsitektur
Spring (Entity, Repository, Controller).
