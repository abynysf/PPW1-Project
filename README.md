**Tugas Project Akhir Praktikum Pemrograman Web 1**

Nama : Muhammad Abyan Farras Yusuf
NIM : 22/506156/SV/22088

import file "portfolio.sql" ke phpmyadmin lalu jalankan ke "localhost/portfolio/"

**WEBSITE PROFIL DIRI**

Website profil diri atau portfolio bertujuan untuk mempresentasikan identitas dan karya seseorang secara online. Website profil diri akan memberikan ruang untuk menggambarkan keahlian, pengalaman kerja, dan pendidikan individu. Hal ini membantu klien untuk memperlihatkan kompetensinya kepada pengunjung dan calon klien atau perekrut.

**Beberapa permasalahan yang di-cover oleh website profil diri meliputi:**

1. Jangkauan yang lebih luas: Dengan memiliki website profil diri, klien dapat mencapai audiens yang lebih besar daripada hanya mengandalkan saluran-saluran pemasaran atau komunikasi tradisional. Potensial perekrut, klien, atau kolektor seni dapat menemukan dan mengevaluasi klien dengan lebih mudah melalui pencarian online.
2. Branding personal: Website profil diri memberikan klien kesempatan untuk membangun citra dan merek personal mereka. Desain yang unik, gaya visual yang konsisten, dan pesan yang jelas akan membantu menciptakan identitas yang kuat bagi klien.
3. Referensi dan testimoni: Website profil diri dapat mencantumkan referensi atau testimoni dari klien atau klien sebelumnya, memberikan bukti nyata tentang kemampuan dan kualitas pekerjaan klien. Hal ini dapat membangun kepercayaan dan membantu mengamankan proyek atau kesempatan baru.
4. Pembaruan konten: Website profil diri dapat diperbarui secara teratur dengan informasi terbaru, proyek-proyek terkini, atau prestasi baru. Dengan demikian, klien dapat menjaga relevansi dan memberikan informasi yang up-to-date kepada pengunjung.

**Kriteria Penilaian**

===========================================================================

**1. Desain :**
- Menggunakan navigation bar untuk memudahkan pengguna untuk melakukan navigasi
- Desain yang konsisten
- tipografi yang jelas

```
<nav id="navbar" class="navbar">
  <ul>
    <li><a class="nav-link active" href="#header">Home</a></li>
    <li><a class="nav-link" href="#about">About</a></li>
    <li><a class="nav-link" href="#resume">Resume</a></li>
    <li><a class="nav-link" href="#services">Services</a></li>
    <li><a class="nav-link" href="#portfolio">Portfolio</a></li>
    <li><a class="nav-link" href="#contact">Contact</a></li>
  </ul>
  <i class="bi bi-list mobile-nav-toggle"></i>
</nav><!-- .navbar -->
```
===========================================================================

**2. Website bersifat responsif untuk mobile, tablet dan desktop :**

```
<!-- ======= About Me ======= -->
    <div class="about-me container">

      <div class="section-title">
        <h2>About</h2>
        <p>Learn more about me</p>
      </div>

      <div class="row">
        <div class="col-lg-4" data-aos="fade-right">
          <img src="assets/img/me.png" class="img-fluid" alt="">
        </div>
        <div class="col-lg-8 pt-4 pt-lg-0 content" data-aos="fade-left">
          <h3><?php echo $data['title']?></h3>
          <p class="fst-italic">
            <?=$data['slogan']?>
          </p>st
          <div class="row">
            <div class="col-lg-6">
              <ul>
                <li><i class="bi bi-chevron-right"></i> <strong>Birthday:</strong> <span><?php echo date('d M Y', strtotime($data['birthday']))?></span></li>
                <li><i class="bi bi-chevron-right"></i> <strong>Website:</strong> <span><a style="color: white;" href="<?=$data['website']?>" target="_blank"><?=$data['website']?></a></span></li>
                <li><i class="bi bi-chevron-right"></i> <strong>Phone:</strong> <span><a style="color: white;" href="tel:<?=$data['phone']?>"><?=$data['phone']?></a></span></li>
                <li><i class="bi bi-chevron-right"></i> <strong>City:</strong> <span><?=$data['city']?></span></li>
                <li><i class="bi bi-chevron-right"></i> <strong>Age:</strong> <span><?=$data['age']?></span></li>
              </ul>
            </div>
            <div class="col-lg-6">
              <ul>
                <li><i class="bi bi-chevron-right"></i> <strong>Degree:</strong> <span><?=$data['degree']?></span></li>
                <li><i class="bi bi-chevron-right"></i> <strong>Certification:</strong> <span><?=$data['certification']?></span></li>
                <li><i class="bi bi-chevron-right"></i> <strong>Email:</strong> <span><a style="color: white;" href="mailto:<?=$data['email']?>"><?=$data['email']?></a></span></li>
                <li><i class="bi bi-chevron-right"></i> <rong>Freelance:</rong> <span>
                  <?php 
                  if($data['freelance'] == 1){
                    echo "Available";
                  }
                  else{
                    echo "Not Available";
                  }
                  ?>

                </span></li>
              </ul>
            </div>
          </div>
        </div>
      </div>
```

Penjelasan :

a) Media Query untuk Layar Lebar (Large Screens):

- Digunakan kelas "col-lg-*" pada elemen kolom (col-lg-4 dan col-lg-8) untuk mengatur tata letak pada layar yang lebar, seperti desktop atau laptop.
- Angka "" pada kelas "col-lg-" menunjukkan jumlah kolom yang akan digunakan oleh elemen dalam grid, di mana nilai tersebut dapat berkisar antara 1 hingga 12.
- Dalam kode di atas, kelas "col-lg-4" digunakan untuk mengatur tata letak gambar (img) dengan menggunakan 4 kolom di dalam grid, sedangkan kelas "col-lg-8" digunakan untuk mengatur tata letak konten dengan menggunakan 8 kolom di dalam grid.

b) Responsif terhadap Layar Lebar yang Lebih Kecil:

- Dalam konteks kode tersebut, ketika ukuran layar menjadi lebih kecil dari ukuran layar lebar (large screens), Bootstrap secara otomatis akan menyesuaikan tata letak elemen-elemen tersebut.
- Pada kasus ini, elemen gambar (img) dan konten (content) akan secara otomatis mengikuti tata letak default Bootstrap yang responsif untuk layar yang lebih kecil.

c) Responsif terhadap Layar Mobile:

- Pada layar mobile atau perangkat dengan ukuran layar yang sangat kecil, Bootstrap akan mengatur ulang tata letak elemen secara otomatis untuk memastikan keterbacaan dan tampilan yang baik.
- Dalam kode di atas, menggunakan kelas "img-fluid" pada elemen gambar (img) untuk memastikan gambar menyesuaikan ukuran kontainer dan tidak terlalu memanjang atau membesar secara tidak wajar pada layar mobile.

===========================================================================

**3. Direct feedback ke pengguna website :**

```
      <?php
        if(isset($_POST['send_message'])){
          global $con;
          $name = mysqli_real_escape_string($con, $_POST['name']);
          $email = mysqli_real_escape_string($con, $_POST['email']);
          $subject = mysqli_real_escape_string($con, $_POST['subject']);
          $message = mysqli_real_escape_string($con, $_POST['message']);

          $contact = "INSERT INTO `contact` (`name`, `email`, `subject`, `message`) VALUES ('$name', '$email', '$subject', '$message')";
          mysqli_query($con, $contact);

          if (mysqli_affected_rows($con) > 0) {
            echo "<p class='text-success'>Message sent successfully!</p>";
          } else {
            echo "<p class='text-danger'>Failed to send message. Please try again later.</p>";
          }
        }
      ?>
```
Penjelasan :

- Setelah pengguna mengirimkan datanya, mulai line 128 akan ada notifikasi yang muncul untuk memberitahu pengguna apakah data yang dimasukkan sudah terdata ke database atau tidak.
  
===========================================================================

**4. Konten dinamis dari database :**

```
  <!-- ======= Portfolio Section ======= -->
  <section id="portfolio" class="portfolio">
    <div class="container">

      <div class="section-title">
        <h2>Portfolio</h2>
        <p>My Works</p>
      </div>

      <div class="row">
        <div class="col-lg-12 d-flex justify-content-center">
          <ul id="portfolio-flters">
            <li data-filter="*" class="filter-active">All</li>
            <?php
              $cat_list = "SELECT * FROM `category`";
              $cat_result = mysqli_query($con, $cat_list);
              if($cat_result -> num_rows > 0){
                while($cat_data = $cat_result -> fetch_assoc()){
                  ?>
                  <li data-filter=".<?php echo $cat_data['name']?>"><?php echo $cat_data['name']?></li>
                  <?php
                }
              }
            ?>
          </ul>
        </div>
      </div>

      <div class="row portfolio-container">
        <?php
          $portfolio = "SELECT * FROM `portfolio`";
          $portfolio_result = mysqli_query($con, $portfolio);

          if($portfolio_result -> num_rows > 0){
            while($portfolio_data = $portfolio_result->fetch_assoc()){
              $category = $portfolio_data['category'];
                $category_sql = "SELECT * FROM `category` WHERE `category`.`id`='$category'";
                $category_result = mysqli_query($con, $category_sql);
                $category_data = mysqli_fetch_assoc($category_result);
              ?>
                <div class="col-lg-4 col-md-6 portfolio-item <?=$category_data['name']?>">
                  <div class="portfolio-wrap">
                    <img src="<?=$portfolio_data['image']?>" class="img-fluid" alt="">
                    <div class="portfolio-info">
                      <h4><?=$portfolio_data['title']?></h4>
                      <p><?=$category_data['name']?></p>
                      <div class="portfolio-links">
                        <a href="<?=$portfolio_data['image']?>" data-gallery="portfolioGallery" class="portfolio-lightbox" title="<?php echo $portfolio_data['title']?>"><i class="bx bx-plus"></i></a>
                        <a href="portfolio-details.php?id=<?php echo $portfolio_data['id']?>" data-gallery="portfolioDetailsGallery" data-glightbox="type: external" class="portfolio-details-lightbox" title="Portfolio Details"><i class="bx bx-link"></i></a>
                      </div>
                    </div>
                  </div>
                </div>
              <?php
            }
          }
          else{
            echo "NO Portfolio Found.";
          }
        ?>
      </div>

    </div>
  </section><!-- End Portfolio Section -->
```
Penjelasan :

- Kode di atas menggambarkan bagian dari halaman web yang menampilkan konten dinamis dari database. Khususnya, bagian ini terkait dengan menampilkan portfolio
  
```
$cat_list = "SELECT * FROM `category`";
$cat_result = mysqli_query($con, $cat_list);
```

- Query ini mengambil semua kategori yang tersedia dari tabel "category" dalam database. Hasil query disimpan dalam variabel $cat_result.

```
if($cat_result -> num_rows > 0){
  while($cat_data = $cat_result -> fetch_assoc()){

```
- Loop ini mengecek apakah ada kategori yang ditemukan dalam hasil query. Jika ada, maka akan dilakukan iterasi melalui setiap baris data menggunakan fungsi fetch_assoc(). Setiap baris data disimpan dalam variabel $cat_data.

```
<li data-filter=".<?php echo $cat_data['name']?>"><?php echo $cat_data['name']?></li>
```

- Bagian ini mencetak elemen ```<li>``` untuk setiap kategori yang ditemukan dalam database. Nilai dari atribut data-filter digunakan untuk menyaring portofolio berdasarkan kategori saat pengguna memilih opsi filter. Nilai dari kategori ditampilkan sebagai teks di dalam elemen ```<li>```.
