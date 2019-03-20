<ol>
	<b>
	<li>Pendahuluan</li>
	</b>
		<ol>
			 <b>1.1 Tujuan</b><br>
			 <ol>
			 	Tujuan dalam membuat dokumen SSD(Software Design Description) ini adalah untuk menjelaskan langkh-langkah desain dan proses-proses dalam pembuatan sistem aplikasi yang akan diterapkan pada aplikasi simulasi management proyek RPL dan juga memberi definisi kebutuhan untuk sistem spesifikasi kebutuhan fungsional.<br>
			 </ol>
			 <b>1.2 Ruang Lingkup</b><br>
			 <ol>
			 	Ruang lingkup SDD ini adalah penjelasan mengenai aplikasi simulasi management proyek RPL berbasis dekstop, ruang lingkup system ini mencakup informasi mengenai antarmuka dari system tersebut.<br>
			 </ol>
			 <b>1.3 Definisi, Akronim, dan Singkatan</b><br>
			 <ol>
			 	 Dalam penulisan dokumen pembuatan projek ini yang mungkin akan sulit di pahami berikut ini:<br>
			 	 SSD artinya Software Design Description<br>
			 	 OOP artinya Object Oriented Programmung<br>
			 	 User artinya untuk pengguna system<br>
			 </ol>
		</ol>
	<b>
	<li>Referensi</li>
	</b>
	<ol>
		a. Modul KULIAH RPL 7 DOKUMEN SDD <br>
		b. Contoh Software Design Document (SDD) Moch. Bambang Sulistio<br>
	</ol>
	 <b>
	<li>Deskripsi Dekomposisi</li>
	</b>
	<ol>
		<b>3.1 Dekomposisi Modul</b><br>
		<ol>
			Kebutuhan fungsional (Functional Requirements) ini adalah kebutuhan utama yang diharapkan dari sistem ini, yang terkait langsung dengan sistem ini. Kebutuhan fungsional dari sistem ini adalah sebagai berikut: <br>
			<li>Pencatatan Hak Akses</li>
			<li>Pencatatan Nama aplikasi , Nama Kategori dan Nama Client </li>
			<li>Pencatatan Target Waktu , Jumlah Orang dan Biaya Aplikasi</li>
			Spesifikasi yang diharapkan pada Pencatatan Hak Akses:<br>
		<ul>
			<li>Membedakan antara user dan admin dalam hak ases</li>
			<li>Sistem dapat memproses secara otomatis jika kita terdaftar dalam admin memiliki hak ases penuh dan sebaliknya juka terdaftar dalam user tidak memiliki hak ases penuh</li>
		</ul>
			Spesifikasi yang diharapkan pada Pencatatan Target Waktu , Jumlah Orang dan Biaya Aplikasi :<br>
		<ul>
			<li>Sistem dapat memproses secara otomatis target waktu aplikasi yang akan di buat dalam sebuah project</li>
			<li>Sistem dapat memproses secara otomatis jumlah orang dalam sebuah project</li>
			<li>Sistem dapat memproses secara otomatis biaya dalam sebuah aplikasi yang akan di buat</li>
		</ul>
		</ol>
	<b>3.2 Dekomposisi Proses Konkuren</b><br> 
	<ol> Konkurensi adalah proses-proses (lebih dari satu proses) yang terjadi pada saat bersamaan. Konkurensi merupakan landasan umum perancangan sistem operasi. 
	Proses-proses disebut konkuren jika proses-proses berada pada saat yang sama. Pada proses-proses konkuren yang berinteraksi mempunyai beberapa masalah yang harus diselesaikan:<br></ol>
	  <ol> 
		<li>Mutual Exclusion</li> 
		<li>Sinkronisasi</li> 
		<li>Deadlock</li> 
		<li>Startvation</li>
	  </ol> 
 			Pada sistem dengan banyak proses (kongkuren), terdapat 2 katagori interaksi, yaitu: <br>
 		<ol> 
			<li>Proses-proses Saling Tidak Peduli (Independen).
			Proses-proses ini tidak dimaksudkan untuk bekerja untukmencapai tujuan tertentu. Pada multiprogramming dengan proses-proses independen, dapat berupa batch atau sesi interaktif, atau campuran keduanya.</li>
			<li>Proses-proses Saling Mempedulikan Secara Tidak Langsung. Proses-proses tidak perlu saling mempedulikan identitas proses-proses lain, tapi sama-sama mengakses objek tertentu, seperti buffer masukan/keluaran. Proses-proses itu perlu bekerja sama (cooperation) dalam memakai bersama objek tertentu.</li>
			<li>Proses-proses konkuren mengharuskan beberapa hal yang harus ditangani, antara lain:<br></li> 
			  <ol>
				a. Sistem operasi harus mengetahui proses-proses yang aktif<br>
				b. Sistem operasi harus mengalokasikan dan mendealokasikan beragam sumber daya untuk tiap proses aktif. Sumber daya yang harus dikelola, 
				antara lain:<br>
				  <ol>
					<li>Waktu pemroses.</li>
					<li>Memori.</li> 
					<li>Berkas-berkas.</li> 
					<li>Perangkat I/O</li>
				  </ol>
				c. Sistem operasi harus memproteksi data dan sumber daya fisik masingmasing proses dari gangguan proses-proses lain.<br>
				d. Hasil-hasil proses harus independen terhadap kecepatan relatif prosesproses lain dimana eksekusi dilakukan.<br>
			  </ol>
		</ol>
	<b>3.3 Dekomposisi Data</b><br>
		<ol>
			Bagian ini akan menjelaskan struktur data. Table yang terbentuk ada 2 (Dua)
		dengan nama masing masing tablenya adalah sebagai berikut : <br>
			<oL>
				<li>Tabel karyawan</li>
				<li>Tabel hitung_cost</li>
			</oL>
			Penjelasan fungsi dari masing masing tabel akan dijelaskan pada bagian berikut ini : <br>
			Tabel admin, digunakan untuk menyimpan informasi Admin, dimana Admin ini dapat mengolah sebuah aplikasi dengan penuh seperti mengedit, simpan, hapus dan update. <br>
			<img src="data.jpg" align="center" width="150" height="150"><br>
			Tabel hitung, digunakan untuk menyimpan hasil efroth, durasi waktu, jumlah orang dan gaji setiap karyawan yang bekerja dalam sebuah project aplikasi.<br>
			<img src="proyek.jpg" width="150" height="150">
			<br>
			<center>Tabel 2 Hitung Proyek </center>
		</ol>
	</ol>
		<b>
	<li>Deskripsi ketergantungan (dependency)</li></b>
	<ol>
		<b>4.1 Dekomposisi Modul</b><br>
			<ol>
				Ketika merancang sebuah Dependensi Inter-modul sistem, dapat dirancang dengan dua cara yang luas dan cara pertama adalah untuk merancang sistem yang lengkap dengan menggunakan sistem yang ada diketahui dan mengimplementasikan fitur baru yang diperlukan untuk meningkatkan efektivitas sistem dan mengujinya di kondisi nyata. Cara alternatif akan merancang sistem dan biasanya karena biaya untuk menyiapkan antarmuka antara modul. Modul dari siaran berita Sistem SCC tergantung pada penyebaran informasi. Ini antar-modul dari penelitian ini adalah tampilan dari pengumuman dan itu termasuk database sistem. Kemudian seluruh informasi yang telah dimasukkan akan disimpan dalam database, yang berasal dari proses input sampai pengumuman menampilkan ke monitor lain.<br>
			</ol>
		<b>4.2 Keterkaitan inter proses</b><br>
			<ol>
				Proses yang dilakukan oleh pengguna dalam melakukan pemesanan proyek aplikasi akan mempengaruhi beberapa proses lainya seperti penentuan value, dan penjadwalan. Juga data akan tersimpan sebagai riwayat proses pemesanan.<br>
			</ol>
		<b>4.3 Keterkaitan data</b><br>
		<ol>
		Dependensi data didasarkan pada pengguna. Mereka adalah orang yang akan memverifikasi atau menyetujui pengumuman antri.<br>
	</ol>
</ol>


