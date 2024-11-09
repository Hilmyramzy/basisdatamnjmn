HILMY SYADDAD RAMZY NURFAUZAN

312210162

TI22A1

===============================================================================

1. Jelaskan perbedaan antara data dan informasi. Berikan contoh bagaimana data dapat diubah menjadi informasi yang berguna dalam konteks sistem basis data.
   Perbedaan antara Data dan Informasi:

Data adalah sekumpulan fakta mentah yang tidak memiliki makna tersendiri. Data biasanya berupa angka, karakter, atau simbol yang tidak terstruktur dan belum diproses, sehingga kurang berguna bagi pengambilan keputusan. Contoh data mentah dapat berupa angka-angka seperti 123, 456, 789.

Informasi adalah hasil dari pengolahan data yang sudah terstruktur dan memiliki makna dalam konteks tertentu. Informasi adalah data yang telah diinterpretasikan, sehingga memiliki nilai untuk mendukung pengambilan keputusan.

Contoh Konversi Data menjadi Informasi dalam Basis Data: Misalkan dalam suatu sistem basis data mahasiswa, terdapat data mentah seperti berikut:

{NIM: "A123", Nilai: 80}, {NIM: "B456", Nilai: 90}, {NIM: "C789", Nilai: 70}

Data ini hanyalah sekumpulan angka dan kode mahasiswa yang belum memiliki makna. Namun, setelah diolah menjadi informasi, data tersebut bisa dijadikan laporan peringkat mahasiswa atau statistik nilai rata-rata dalam satu mata kuliah

2.  Sebuah universitas ingin menyimpan informasi tentang mahasiswa dan mata kuliah yang mereka ambil. Identifikasi entitas dan atribut yang relevan dalam sistem ini. Buat tabel sederhana yang mencakup entitas dan atribut yang diperlukan.
   Entitas dan Atribut:
Entitas: Mahasiswa
![d1c3c856-0a6c-4fc3-8fe5-e3463a23da29](https://github.com/user-attachments/assets/6fc457ce-8e77-40fc-9355-b4f9761fbda9)

Atribut:
NIM (Nomor Induk Mahasiswa)
Nama
Tanggal_Lahir
Alamat
Jurusan
Entitas: Mata_Kuliah


Atribut:
Kode_MataKuliah
Nama_MataKuliah
SKS (Satuan Kredit Semester)
Entitas: Registrasi (menyimpan data hubungan antara mahasiswa dan mata kuliah yang mereka ambil)


Atribut:
ID_Registrasi
NIM
Kode_MataKuliah
Nilai


Tabel Sederhana yang Mencakup Entitas dan Atribut:
Entitas	Atribut

Mahasiswa	NIM, Nama, Tanggal_Lahir, Alamat, Jurusan
Mata_Kuliah	Kode_MataKuliah, Nama_MataKuliah, SKS
Registrasi	ID_Registrasi, NIM, Kode_MataKuliah, Nilai

Penjelasan:

Tabel Mahasiswa menyimpan data mahasiswa.

Tabel Mata_Kuliah menyimpan data mata kuliah yang ditawarkan universitas.

Tabel Registrasi menghubungkan Mahasiswa dengan Mata_Kuliah,
menyimpan data mata kuliah apa saja yang diambil setiap mahasiswa dan berisi nilai yang diperoleh mahasiswa di setiap mata kuliah tersebut.

3.  Pada sistem perpustakaan, terdapat entitas Buku dan entitas Anggota. Jelaskan bagaimana relasi antar entitas ini bisa dibangun dalam basis data. Gambarkan relasi antar entitas tersebut dalam bentuk diagram ER (Entity-Relationship).

   Pembentukan Relasi
   ![d1c3c856-0a6c-4fc3-8fe5-e3463a23da29](https://github.com/user-attachments/assets/b337a99e-d763-4342-9565-a6b6e0594f4d)

Entitas Buku:

Menyimpan informasi tentang buku yang ada di perpustakaan.

Atribut: ISBN, Judul, Pengarang, Penerbit.

Entitas Anggota:

Menyimpan data anggota perpustakaan yang memiliki hak untuk meminjam buku.

Atribut: ID_Anggota, Nama, Alamat, Nomor_Telepon.

Entitas Peminjaman:

Menghubungkan entitas Buku dan Anggota. Entitas ini digunakan untuk menyimpan data peminjaman, sehingga memungkinkan pencatatan buku mana yang dipinjam oleh anggota tertentu, kapan dipinjam, dan kapan harus dikembalikan.

Atribut: ID_Peminjaman, ID_Anggota, ISBN, Tanggal_Pinjam, Tanggal_Kembali.

Relasi Antar Entitas

Relasi antara Anggota dan Buku melalui Peminjaman adalah relasi many-to-many (banyak ke banyak), karena:

Seorang anggota dapat meminjam banyak buku.

Sebuah buku bisa dipinjam oleh beberapa anggota pada waktu yang berbeda.

4.  Dalam suatu sistem penjualan online, terdapat entitas Pelanggan dan entitas Pesanan. Diskusikan kemungkinan kardinalitas dan participation constraint yang dapat berlaku antara entitas Pelanggan dan Pesanan. Berikan contoh yang sesuai dalam diagram ER.

   Dalam sistem penjualan online, relasi antara Pelanggan dan Pesanan memiliki karakteristik sebagai berikut:
   ![d1c3c856-0a6c-4fc3-8fe5-e3463a23da29](https://github.com/user-attachments/assets/26fbeba1-6d80-470d-93ee-5c69076eb5f7)


Kardinalitas

Setiap Pelanggan dapat membuat lebih dari satu Pesanan (relasi one-to-many, 1
), karena seorang pelanggan dapat membeli beberapa produk di waktu yang berbeda.

Setiap Pesanan harus dibuat oleh satu Pelanggan (relasi many-to-one, N:1), karena pesanan tidak dapat dilakukan tanpa adanya pelanggan.

   Participation Constraint
   
Mandatory Participation pada entitas Pesanan: Setiap Pesanan wajib terhubung ke satu Pelanggan karena pesanan tidak dapat ada tanpa pelanggan yang membuatnya.

Optional Participation pada entitas Pelanggan: Seorang Pelanggan mungkin belum pernah membuat Pesanan; misalnya, pelanggan yang baru mendaftar belum tentu langsung melakukan pembelian.

Penjelasan Diagram ER

Dalam diagram tersebut, satu Pelanggan dapat memiliki banyak Pesanan, dan setiap Pesanan terkait dengan satu Pelanggan yang melakukan pesanan. Ini adalah relasi umum dalam sistem penjualan online, yang memungkinkan pelanggan memiliki beberapa pesanan di waktu yang berbeda.




================================================================================================
![Untitled Diagram](https://github.com/user-attachments/assets/b36c2fad-6c03-483c-8fc0-73e09cad943e)

[1728093458726_basis+data+5.docx](https://github.com/user-attachments/files/17515058/1728093458726_basis%2Bdata%2B5.docx)
[Untitled Diagram.drawio.pdf](https://github.com/user-attachments/files/17515341/Untitled.Diagram.drawio.pdf)
