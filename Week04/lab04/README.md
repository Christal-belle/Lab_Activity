1. Yang salah: Row, Row tidak memberi batas lebar ke Text, jadi Text memanjang lurus sampai keluar layar. Solusinya: bungkus Text dengan Expanded dan beri maxLines dengan ellipsis.

2. Angka 150 hanya cocok untuk satu layar. Di layar yang lebih kecil, teks yang lebih panjang, atau font yang lebih besar, errornya akan muncul lagi. Yang benar adalah ruang yang tersedia ditentukan oleh parent, bukan angka.

3. Yang gagal: test 7 (500 item, lazy). shrinkWrap: true membuat semua 500 item dibangun sekaligus. Kalau data dari API jumlahnya banyak, aplikasi jadi lambat dan berat.

4. MediaQuery hanya tahu ukuran layar, LayoutBuilder tahu ruang yang diberikan ke widget. Jadi LayoutBuilder lebih tepat karena layout menyesuaikan dengan ruang yang benar-benar ada.

5. Karena layar harus aman untuk data apa pun, kalau data kosong membuat aplikasi crash, layar tidak tampil sama sekali. Jadi data kosong juga harus dirancang, sama seperti ukuran layar.