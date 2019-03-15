# SoalShift_modul2_F7

Nomor 1
Elen mempunyai pekerjaan pada studio sebagai fotografer. Suatu hari ada seorang klien yang bernama
Kusuma yang meminta untuk mengubah nama file yang memiliki ekstensi .png menjadi
“[namafile]_grey.png”. Karena jumlah file yang diberikan Kusuma tidak manusiawi, maka Elen meminta
bantuan kalian untuk membuat suatu program C yang dapat mengubah nama secara otomatis dan
diletakkan pada direktori /home/[user]/modul2/gambar.
Catatan : Tidak boleh menggunakan crontab.
Jawab : Langkah pertama adalah kita harus membuat kondisi yang menerima bahwa file tersebut adalah
.png, selanjutnya kita simpan path direktori yang ingin dituju, lalu kita gabungkan path direktori tersebut
dengan nama file, selanjutnya kita gabungkan dengan “_grey” sesuai permintaan soal, lalu kita rename
dengan menggunakan exec argumen mv (move);

Nomor 2
Pada suatu hari Kusuma dicampakkan oleh Elen karena Elen dimenangkan oleh orang lain. Semua
kenangan tentang Elen berada pada file bernama “elen.ku” pada direktori “hatiku”. Karena sedih
berkepanjangan, tugas kalian sebagai teman Kusuma adalah membantunya untuk menghapus semua
kenangan tentang Elen dengan membuat program C yang bisa mendeteksi owner dan group dan
menghapus file “elen.ku” setiap 3 detik dengan syarat ketika owner dan grupnya menjadi “www-data”.
Ternyata kamu memiliki kendala karena permission pada file “elen.ku”. Jadi, ubahlah permissionnya
menjadi 777. Setelah kenangan tentang Elen terhapus, maka Kusuma bisa move on.
Catatan: Tidak boleh menggunakan crontab
Jawab :
Langkah pertama, kita simpan path direktori file elen.ku, lalu kita simpan nama owner dan group yang
ingin kita deteksi, setelah itu gunakan stat and struct untuk mendapatkan password dan group agar kita
bisa membandingkannya dengan yang ingin kita deteksi, jika saat dibandingkan sama dengan nama
yang kita simpan tadi, maka delete file elenku, dari direktori path yang sudah disimpan.

Nomor 3

Nomor 4

Nomor 5
Kerjakan poin a dan b di bawah:
1. Buatlah program c untuk mencatat log setiap menit dari file log pada syslog ke
/home/[user]/log/[dd:MM:yyyy-hh:mm]/log#.log
Ket:
• Per 30 menit membuat folder /[dd:MM:yyyy-hh:mm]
• Per menit memasukkan log#.log ke dalam folder tersebut
‘#’ : increment per menit. Mulai dari 1

2. Buatlah program c untuk menghentikan program di atas.
NB: Dilarang menggunakan crontab dan tidak memakai argumen ketika menjalankan program.
Jawab:
Langkah pertama, kita simpan path direktori ke string, lalu simpan juga waktu dan tanggal di string,
kemudian buat direktori dari string waktu dan tanggal yang sudah disimpan tadi, lalu gabungkan string
path direktori dengan string direktori yang sudah dibuat, tambahkan “/log” dengan strcat, karena
permintaan soal nama file log#.log, masuk ke looping kita buka file syslog dengan fopen “r” lalu kita tulis
file syslog tersebut di file yang diinginkan, menggunakan looping fgetc dan fputc sampai end of file, close
file syslog dan reset path agar dapat membuat increment file selanjutnya.
