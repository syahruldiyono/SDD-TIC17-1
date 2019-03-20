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