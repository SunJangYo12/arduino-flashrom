Untuk penjelasan lengkap mengenai chip
ini bisa dilihat di file Dokumen.txt

# update v1.0
tersedia option buat manipulasi memori
seperti pembacaan per page dan
menulis perpage, untuk penggunaan bisa
menggunakan perintah serial ";bantuan;"<br>
Note:
versi ini belum memiliki fungsi upload/download

# update v1.1
Penambahan upload dan download isi memori
untuk bisa di manipulasi menggunakan
tools ghex atau yang lain<br>
1). Dependencies<br>
    $ sudo apt install flashrom

2). Compile & Flash<br>
      sudo -s<br>
      make mega2560<br>
 	  make flash-mega2560<br>
      flashrom -p serprog:dev=/dev/ttyUSB1:115200 <br>
      flashrom -p serprog:dev=/dev/ttyUSB1:115200 -r tenda.rom<br>
      flashrom -p serprog:dev=/dev/ttyUSB1:115200 -w tenda.rom<br>

NOTE: untuk pilihan board arduino bisa 
dilihat di file Makefile dan untuk saat 
ini saya menggunankan board mega2560
dengan pin sebagai berikut:
1) MISO pin 50
2) MOSI pin 51
3) SCK  pin 52
4) SS   pin 53