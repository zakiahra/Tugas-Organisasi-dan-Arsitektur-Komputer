# Tugas Organisasi dan Arsitektur Komputer
## 1. Jelaskan Struktur Antar Hubungan dan Beri Contohnya?
Struktur antar Hubungan bisa disebut sebagai sistem BUS, jadi BUS adalah sebuah subsistem yang mentransfer data atau listrik antar komponen komputer di dalam sebuah komputer atau antar komputer.Pada sistem komputer, bus ini termasuk perangkat internal, kecepatan pengiriman informasi melalui bus ini dilakukan dengan kecepatan tinggi.
Contoh :
- PCI ( Pheripheral Component Interconnect )
   bus yang didesain untuk menangani beberapa perangkat keras. PCI juga adalah suatu bandwidth tinggi yang populer, prosesor independent bus itu dapat berfungsi sebagai bus mezzenine atau bus periferal. Standar bus PCI ini dikembangkan oleh konsorsium PCI Special Interest Group yang dibentuk oleh Intel Corporation dan beberapa perusahaan lainnya, pada tahun 1992. Tujuan dibentuknya bus ini adalah untuk menggantikan Bus ISA/EISA yang sebelumnya digunakan dalam komputer IBM PC atau kompatibelnya.
- USB ( Universal Serial Bus )
      USB merupakan suatu teknologi yang memungkinkan kita untuk menghubungkan alat eksternal (peripheral) seperti scanner, printer, mouse, papan ketik (keyboard), alat penyimpan data (zip drive), flash disk, kamera digital atau perangkat lainnya ke komputer kita. USB sangat mendukung transfer data sebesar 12 Mbps ( juta bit per detik). Komputer (PC) saat ini, umumnya sudah memiliki port USB. Biasanya disediakan minimal 2 port. Jika dibandingkan dengan paralel port dan serial port, penggunaan port USB lebih mudah dalam penggunaannya.
- BUS PCI
   Bus yang tidak tergantung prosesor dan berfungsi sebagai bus mezzanine atau bus peripheral. Standar PCI adalah 64 saluran data pada kecepatan 33MHz, laju transfer data 263 MB per detik atau 2,112 Gbps. Keunggulan PCI tidak hanya pada kecepatannya saja tetapi murah dengan keping yang sedikit.
- BUS ISA ( Industry Standart Architecture )
   Industri computer personal lainnya merespon perkembangan ini dengan mengadopsi standarnya sendiri, bus ISA, yang pada dasarnya adalah bus PC/AT yang beroperasi pada 8,33 MHz. Keuntungannya adalah bahwa pendekatan ini tetap mempertahankan kompatibilitas dengan mesin-mesin dan kartu-kartu yang ada.

## 2. Bila terlalu banyak modul atau perangkat dihubungkan pada bus maka akan terjadi penurunan kinerja, sebutkan penyebabnya?
Bila terlalu banyak modul atau perangkat dihubungkan pada bus maka akan terjadi penurunan kinerja, yang disebabkan oleh :
- Semakin besar delay propagasi untuk mengkoordinasikan penggunaan bus. 
- Antrian penggunaan bus semakin panjang.
- Dimungkinkan habisnya kapasitas transfer bus sehingga memperlambat data.
Antisipasi dan solusi persoalan di atas adalah penggunaan bus jamak yang hierarkis. Modul – modul dikalasifikasikan berdasarkan kebutuhan terhadap lebar dan kecepatan bus. Bus biasanya terdiri atas bus lokal, bus sistem, dan bus ekspansi.

## 3. Umumnya perangkat berprioritas paling rendah memiliki waktu tunggu rata-rata yang paling singkat. Dengan dasar ini biasanya CPU diberi perioritas tertinggi pada SBI. Sebutkan alasan perangkat berprioritas 16 memiliki waktu tunggu rata-rata paling rendah ? Di bawah kondisi Seperti apa keadaan diatas tidak berlaku ?
Lintasan bagi perpindahan data antar modul. Secara kolektif lintasan tersebut disebut bus data.  Umumnya jumlah saluran terkait dengan panjang word, misalnya 8, 16, 32 saluran. Jalur-jalur data adalah dua arah (bidirectional). CPU dapat membaca dan mengirim data dari/ke memori atau port. Banyak perangkat pada sistem yang dicantolkan ke bus data tapi hanya satu perangkat pada satu saat yang dapat memakainya. Untuk mengatur ini, perangkat harus mempunyai tiga state  (tristate) agar dapat dipasang pada bus data.

Secara umum, perangkat dengan prioritas rendah memiliki waktu tunggu rata-rata yang lebih rendah dibandingkan dengan yang lainnya karena pendekatan antrian yang dilakukan oleh SBI (Sistem Berbasis Interrupt). Dalam SBI, perangkat atau proses dengan prioritas lebih tinggi diberikan 'hak' pertama untuk memproses kerjaan, sementara perangkat atau proses dengan prioritas yang lebih rendah harus menunggu. Kondisi ini tidak berlaku apabila terjadi overrun buffer, yaitu ketika data masuk melebihi kapasitas buffer dan tidak dapat diproses oleh perangkat, yang mengakibatkan delay waktu tanggap dan meningkatkan waktu tunggu rata-rata.

Proses-peroses dalam sistem berbasis interrupt (SBI) dilayani berdasarkan prioritas. Tugas atau perangkat dengan prioritas tertinggi akan mendapat waktu CPU terlebih dahulu dibandingkan yang lain. Alasannya adalah agar CPU dapat merespons dan menyelesaikan interrupt secepat mungkin, hal ini memberikan insentif bagi prioritas interrupt yang lebih tinggi. Oleh karenanya umumnya perangkat berprioritas paling rendah memiliki waktu tunggu rata-rata yang paling pendek.

Namun pada kondisi bahaya yang dikenal gleap atau overrun buffer (yaitu ketika data masuk terlalu cepat dan buffer tidak memadai untuk menyimpannya), perangkat bisa mengalami tardiness, dengan kata lain waktu tanggap penyelesaian dari proses tersebut menjadi terlambat dan waktu tunggu rata-rata pun meningkat. Hal ini akan mengganggu prioritas dasar SBI yang seharusnya semenjak awal dimiliki oleh proses dengan prioritas


### sumber dan referensi
- https://tecnomasi.blogspot.com/2015/12/jawaban-organisasi-arsitektur-komputer.html
- https://123dok.com/document/zg65782q-bab-sistem-bus-organisasi-komputer.html#:~:text=Bila%20terlalu%20banyak%20modul%20atau%20perangkat%20dihubungkan%20pada,penggunaan%20bus.%20%E2%80%A2%20Antrian%20penggunaan%20bus%20semakin%20panjang.
- https://www.questionai.com/questions-sz1AD1Tn3j/content-3-umumnya-perangkat-berprioritas-paling-rendah

