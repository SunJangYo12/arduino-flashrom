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
      Edit Makefile line 34 SERIAL_DEV ?= /dev/ttyUSB... example ttyUSB1
      Edit Makefile line 112 ttyUSB... example ttyUSB1
      make mega2560<br>
 	  sudo make flash-mega2560<br>
      sudo flashrom -p serprog:dev=/dev/ttyUSB1:115200 <br>
      sudo flashrom -p serprog:dev=/dev/ttyUSB1:115200 -r tenda.rom<br>
      sudo flashrom -p serprog:dev=/dev/ttyUSB1:115200 -w tenda.rom<br>

NOTE: untuk pilihan board arduino bisa 
dilihat di file Makefile dan untuk saat 
ini saya menggunankan board mega2560
dan rom winbond 25Q64JVSIQ dengan pin sebagai berikut:
1) MISO (pin 2) arduino pin 50
2) MOSI (pin 5) arduino pin 51
3) SCK (pin 6) arduino pin 52
4) SS (pin 1)  arduino pin 53
