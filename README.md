# PWeb_Tugas1_5025211219

## Identitas
| Name           | NRP        | Kelas     | Tahun Ajaran      |
| ---            | ---        | ----------|---                |
| Rayssa Ravelia | 5025211219 |PWEB A     | 2022/2023 (Genap) |

Link deploy [web](https://rayrednet.github.io/)

Pada CV yang saya buat terdapat beberapa bagian file yakni CSS, JS, images, dan HTML. Berikut ini adalah penjelasan detailnya:

## A. CSS
CSS merupakan bahasa yang digunakan untuk membuat desain dokumen HTML. Terdapat 3 file yang saya gunakan yaitu:
- aos.css

`AOS (animated on scroll)` merupakan library animasi pada CSS dan JavaScript yang memungkinkan elemen halaman web untuk dianimasikan saat pengguna scroll ke bawah atau ke atas halaman. 
Untuk menggunakan AOS, pertama-tama kita perlu menambahkan file `JavaScript dan CSS` dari library AOS ke dalam halaman web kita. Kemudian kita dapat menambahkan kelas CSS yang disediakan oleh AOS ke elemen yang ingin `dianimasikan`. Kita juga dapat mengatur opsi dan parameter animasi AOS menggunakan atribut data yang disediakan oleh AOS.

- bootstrap.min.css

File `bootstrap.min.css` adalah salah satu file inti dari Bootstrap. File ini berisi kumpulan `gaya CSS` yang diperlukan untuk membuat tampilan dan layout website yang sesuai dengan gaya Bootstrap.
Dengan menggunakan Bootstrap, saya dapat `menghemat waktu` dan upaya dalam mengembangkan website, karena mereka tidak perlu membuat gaya CSS dan komponen UI dari awal.

- main.css

File `main.css` merupakan file yang sangat penting dalam pengembangan website karena memungkinkan untuk `mengontrol dan menyesuaika` tampilan website secara keseluruhan. Dalam file ini, saya membuat aturan gaya yang spesifik untuk website mereka dan menghasilkan tampilan yang konsisten dan menarik untuk pengguna. Hal-hal yang saya atur adalah `warna dan jenis font, tata letak, efek visual, dan responsivitas`.

## B. JS
File JS digunakan untuk pustaka JavaScript. Terdapat 3 bagian JS yang digunakan:

### Core
Di dalam folder ini ada 3 file yang digunakan:

- bootstrap.min.js

`Bootstrap.min.js` adalah file JavaScript yang termasuk dalam Bootstrap, dan berfungsi untuk mengaktifkan berbagai fitur interaktif pada elemen HTML, seperti navigasi yang responsif, dialog modal, dropdown, jendela geser (carousel), tooltip, dan masih banyak lagi.

- jquery.3.2.1.min.js

`File jquery-3.2.1.min.js` adalah file JavaScript yang berisi kode sumber dari pustaka jQuery versi 3.2.1 yang telah di-minifikasi untuk mengurangi ukuran file dan mempercepat proses pengunduhan pada halaman web.

Beberapa `fungsi` dari jquery-3.2.1 yaitu: manipulasi elemen HTML, animasi, Ajax, menagani event, dan meningkatkan cross-browser compability

- popper.min.js

File popper.min.js adalah file JavaScript yang berisi kode sumber dari pustaka `Popper.js` yang telah di-minifikasi untuk mengurangi ukuran file dan mempercepat proses pengunduhan pada halaman web. 

Beberapa `fungsi` pooper.min.js yaitu menempatkan elemen HTML, menciptakan efek interaktif, meningkatkan user experience, memperbaiki kesalahan dalam peningkatan elemen HTML.

### Plugins
Terdapat 4 file yang digunakan yaitu:
- bootstrap-datepicker.js

`Bootstrap Datepicker` adalah plugin JavaScript yang memperluas kemampuan kerangka kerja Bootstrap dengan menambahkan `kalender` yang dapat dipilih pada elemen input tanggal. File bootstrap-datepicker.js adalah file JavaScript yang berisi kode sumber dari plugin Bootstrap Datepicker.

- bootstrap-switch.js

`Bootstrap Switch` adalah plugin JavaScript yang memperluas kemampuan kerangka kerja Bootstrap dengan menambahkan `kontrol switch (saklar)` yang dapat dipilih pada elemen input. File bootstrap-switch.js adalah file JavaScript yang berisi kode sumber dari plugin Bootstrap Switch

- jquery.sharre.js

`jQuery Sharre` adalah plugin JavaScript yang memperluas kemampuan kerangka kerja jQuery dengan menambahkan tombol berbagi `(share button)` untuk berbagai platform media sosial seperti Facebook, Twitter, dan Google+. File jquery.sharre.js adalah file JavaScript yang berisi kode sumber dari plugin jQuery Sharre.

- nouislider.js

`Nouislider` adalah plugin JavaScript yang memperluas kemampuan kerangka kerja JavaScript dengan menambahkan `kontrol geser` (slider) interaktif yang dapat disesuaikan dan dapat digunakan untuk berbagai tujuan seperti rentang harga, waktu, atau pengaturan kustom lainnya. File nouislider.js adalah file JavaScript yang berisi kode sumber dari plugin Nouislider.

### Main

File `main.js` adalah file JavaScript yang sering digunakan sebagai file utama untuk mengatur perilaku dan tampilan pada halaman web. File ini berisi kode sumber untuk mengatur interaksi dan dinamika pada halaman web yang berkaitan dengan fungsi-fungsi seperti tampilan, animasi, validasi input, dan lain sebagainya.

Untuk animasi scroll dijalankan sekali
```ruby
$(document).ready(function() {
  AOS.init( {
    // once: true  
  }); // initialize animate on scroll library
});
```
Animasi scroll untuk link dengan hashes
```ruby
$('a.smooth-scroll')
.click(function(event) {
  // On-page links
  if (
    location.pathname.replace(/^\//, '') == this.pathname.replace(/^\//, '') 
    && 
    location.hostname == this.hostname
  ) {
    // Figure out element to scroll to
    var target = $(this.hash);
    target = target.length ? target : $('[name=' + this.hash.slice(1) + ']');
    // Does a scroll target exist?
    if (target.length) {
      // Only prevent default if animation is actually gonna happen
      event.preventDefault();
      $('html, body').animate({
        scrollTop: target.offset().top
      }, 1000, function() {
        // Callback after animation
        // Must change focus!
        var $target = $(target);
        $target.focus();
        if ($target.is(":focus")) { // Checking if the target was focused
          return false;
        } else {
          $target.attr('tabindex','-1'); // Adding tabindex for elements not focusable
          $target.focus(); // Set focus again
        };
      });
    }
  }
});
```

## C. Images
Terdapat 3 foto dengan format `jpg` yang saya gunakan dalam CV ini, yaitu:
- cc-bg.jpg

digunakan untuk background header CV

- map.jpg

digunakan untuk background footer CV

- rayssa.jpg

digunakan untuk foto pribadi pada CV

## D. HTML

File `index.html` adalah file utama pada sebuah proyek web yang berisi `markup untuk menampilkan konten` pada halaman web. File ini adalah halaman web yang pertama kali diakses oleh pengguna ketika membuka situs web, dan berisi struktur HTML yang mengatur konten halaman web.

### Bagian Head
Pada bagian head digunakan judul halaman web dan juga sidebar web
```Ruby
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Curriculum Vitae</title>
    <link href="https://fonts.googleapis.com/css?family=Montserrat:400,700,200" rel="stylesheet">
    <link href="https://maxcdn.bootstrapcdn.com/font-awesome/latest/css/font-awesome.min.css" rel="stylesheet">
    <link href="css/aos.css?ver=1.1.0" rel="stylesheet">
    <link href="css/bootstrap.min.css?ver=1.1.0" rel="stylesheet">
    <link href="css/main.css?ver=1.1.0" rel="stylesheet">
    <noscript>
      <style type="text/css">
        [data-aos] {
            opacity: 1 !important;
            transform: translate(0) scale(1) !important;
        }
      </style>
    </noscript>
  </head>
  <body id="top">
    <header>
      <div class="profile-page sidebar-collapse">
        <nav class="navbar navbar-expand-lg fixed-top navbar-transparent bg-primary" color-on-scroll="400">
          <div class="container">
            <div class="navbar-translate"><a class="navbar-brand" href="#" rel="tooltip">Curriculum Vitae</a>
              <button class="navbar-toggler navbar-toggler" type="button" data-toggle="collapse" data-target="#navigation" aria-controls="navigation" aria-expanded="false" aria-label="Toggle navigation"><span class="navbar-toggler-bar bar1"></span><span class="navbar-toggler-bar bar2"></span><span class="navbar-toggler-bar bar3"></span></button>
            </div>
            <div class="collapse navbar-collapse justify-content-end" id="navigation">
              <ul class="navbar-nav">
                <li class="nav-item"><a class="nav-link smooth-scroll" href="#about">About</a></li>
                <li class="nav-item"><a class="nav-link smooth-scroll" href="#skill">Skills</a></li>
                <li class="nav-item"><a class="nav-link smooth-scroll" href="#experience">Experience</a></li>
                <li class="nav-item"><a class="nav-link smooth-scroll" href="#contact">Contact</a></li>
              </ul>
            </div>
          </div>
        </nav>
      </div>
    </header>
```
### Bagian Body
Pada bagian ini digunakan untuk profile page yang berisi informasi umum pada CV
```Ruby
    <div class="page-content">
      <div>
<div class="profile-page">
  <div class="wrapper">
    <div class="page-header page-header-small" filter-color="purple">
      <div class="page-header-image" data-parallax="true" style="background-image: url('images/cc-bg.jpg')"></div>
      <div class="container">
        <div class="content-center">
          <div class="cc-profile-image"><a href="#"><img src="images/rayssa.jpg" alt="Image"/></a></div>
          <div class="h2 title">Rayssa Ravelia</div>
          <p class="category text-white">Tech Enthusiast, Computer Science Student</p><a class="btn btn-primary smooth-scroll mr-2" href="#contact" data-aos="zoom-in" data-aos-anchor="data-aos-anchor">Hire Me</a><a class="btn btn-primary" href="#" data-aos="zoom-in" data-aos-anchor="data-aos-anchor">Download CV</a>
        </div>
      </div>
      <div class="section">
        <div class="container">
          <div class="button-container"><a class="btn btn-default btn-round btn-lg btn-icon" href="https://www.facebook.com/rayssa.ravelia" rel="tooltip" title="Follow me on Facebook"><i class="fa fa-facebook"></i></a><a class="btn btn-default btn-round btn-lg btn-icon" href="https://twitter.com/yeayray" rel="tooltip" title="Follow me on Twitter"><i class="fa fa-twitter"></i></a><a class="btn btn-default btn-round btn-lg btn-icon" href="https://mail.google.com/mail/u/rayssaravelia12@gmail.com/#compose" rel="tooltip" title="Follow me on Google+"><i class="fa fa-google-plus"></i></a><a class="btn btn-default btn-round btn-lg btn-icon" href="https://www.instagram.com/dat_rayssa/" rel="tooltip" title="Follow me on Instagram"><i class="fa fa-instagram"></i></a></div>
        </div>
      </div>
    </div>
  </div>
</div>
<div class="section" id="about">
  <div class="container">
    <div class="card" data-aos="fade-up" data-aos-offset="10">
      <div class="row">
        <div class="col-lg-6 col-md-12">
          <div class="card-body">
            <div class="h4 mt-0 title">About</div>
            <p>Hello! I am Rayssa Ravelia. An enthusiastic learner with highly motivated energy that eager to learn new technologies and methodologies.</p>
            <p>Always willing to innovate new things that can improve the existing technology. Fluent in Bahasa Indonesia and English with excellent communication and interpersonal skills. A fast learner with strong time management and multi-tasking skills. </p>
          </div>
        </div>
        <div class="col-lg-6 col-md-12">
          <div class="card-body">
            <div class="h4 mt-0 title">Basic Information</div>
            <div class="row">
              <div class="col-sm-4"><strong class="text-uppercase">Age:</strong></div>
              <div class="col-sm-8">20</div>
            </div>
            <div class="row mt-3">
              <div class="col-sm-4"><strong class="text-uppercase">Email:</strong></div>
              <div class="col-sm-8">rayssaravelia12@gmailcom</div>
            </div>
            <div class="row mt-3">
              <div class="col-sm-4"><strong class="text-uppercase">Address:</strong></div>
              <div class="col-sm-8">Indonesia</div>
            </div>
            <div class="row mt-3">
              <div class="col-sm-4"><strong class="text-uppercase">Language:</strong></div>
              <div class="col-sm-8">Bahasa Indonesia, English, Chinese</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```
Pada bagian ini digunakan untuk menampilkan skill yang saya miliki pada CV
```Ruby
<div class="section" id="skill">
  <div class="container">
    <div class="h4 text-center mb-4 title">Key Skills & Characteristics</div>
    <div class="card" data-aos="fade-up" data-aos-anchor-placement="top-bottom">
      <div class="card-body">
        <div class="row">
          <div class="col-md-6">
            <div class="progress-container progress-primary"><span class="progress-badge">C and C++</span>
              <div class="progress">
                <div class="progress-bar progress-bar-primary" data-aos="progress-full" data-aos-offset="10" data-aos-duration="2000" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 80%;"></div><span class="progress-value">80%</span>
              </div>
            </div>
          </div>
          <div class="col-md-6">
            <div class="progress-container progress-primary"><span class="progress-badge">Java</span>
              <div class="progress">
                <div class="progress-bar progress-bar-primary" data-aos="progress-full" data-aos-offset="10" data-aos-duration="2000" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 75%;"></div><span class="progress-value">75%</span>
              </div>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-md-6">
            <div class="progress-container progress-primary"><span class="progress-badge">UI/UX</span>
              <div class="progress">
                <div class="progress-bar progress-bar-primary" data-aos="progress-full" data-aos-offset="10" data-aos-duration="2000" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 60%;"></div><span class="progress-value">60%</span>
              </div>
            </div>
          </div>
          <div class="col-md-6">
            <div class="progress-container progress-primary"><span class="progress-badge">Work under pressure</span>
              <div class="progress">
                <div class="progress-bar progress-bar-primary" data-aos="progress-full" data-aos-offset="10" data-aos-duration="2000" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 60%;"></div><span class="progress-value">60%</span>
              </div>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-md-6">
            <div class="progress-container progress-primary"><span class="progress-badge">Critical thinking</span>
              <div class="progress">
                <div class="progress-bar progress-bar-primary" data-aos="progress-full" data-aos-offset="10" data-aos-duration="2000" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 75%;"></div><span class="progress-value">75%</span>
              </div>
            </div>
          </div>
          <div class="col-md-6">
            <div class="progress-container progress-primary"><span class="progress-badge">Photoshop</span>
              <div class="progress">
                <div class="progress-bar progress-bar-primary" data-aos="progress-full" data-aos-offset="10" data-aos-duration="2000" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 70%;"></div><span class="progress-value">70%</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</div>
```

Selanjutnya saya menampilkan section pengalaman yang saya miliki
```ruby
<div class="section" id="experience">
  <div class="container cc-experience">
    <div class="h4 text-center mb-4 title">Work Experience</div>
    <div class="card">
      <div class="row">
        <div class="col-md-3 bg-primary" data-aos="fade-right" data-aos-offset="50" data-aos-duration="500">
          <div class="card-body cc-experience-header">
            <p>August 2021 - January 2022</p>
            <div class="h5">Ini Lho ITS!2022</div>
          </div>
        </div>
        <div class="col-md-9" data-aos="fade-left" data-aos-offset="50" data-aos-duration="500">
          <div class="card-body">
            <div class="h5">UI/UX Designer</div>
            <p>An event was held by Sepuluh Nopember Institute of Technology Student Body (BEM ITS) to introduce ITS to the public. Accomplishments: Collaborated with developer teams and successfully designed the website UI according to the ILITS 2022 theme. </p>
          </div>
        </div>
      </div>
    </div>
    <div class="card">
      <div class="row">
        <div class="col-md-3 bg-primary" data-aos="fade-right" data-aos-offset="50" data-aos-duration="500">
          <div class="card-body cc-experience-header">
            <p>July 2018 - August 2019</p>
            <div class="h5">REDS</div>
          </div>
        </div>
        <div class="col-md-9" data-aos="fade-left" data-aos-offset="50" data-aos-duration="500">
          <div class="card-body">
            <div class="h5">1st Speaker Debate Club</div>
            <p>A society runs by SMA Regina Pacis Bogor aims to develop English oracy skills, expand confidence, and become more aware of current world status quo . Accomplishments: Managed to deliver great arguments and speeches, developed confidence and competence in public speaking and discourse </p>
          </div>
        </div>
      </div>
    </div>
    <div class="card">
      <div class="row">
        <div class="col-md-3 bg-primary" data-aos="fade-right" data-aos-offset="50" data-aos-duration="500">
          <div class="card-body cc-experience-header">
            <p>August 2019 - January 2021</p>
            <div class="h5">NSEC</div>
          </div>
        </div>
        <div class="col-md-9" data-aos="fade-left" data-aos-offset="50" data-aos-duration="500">
          <div class="card-body">
            <div class="h5">Head of CS Divison</div>
            <p>A community for high school students runs by SMA Regina Pacis Bogor that aims to develop scientific thinking by learning and participating in the scientific competition. Accomplishments: Coordinated with National Science and Engineering Competition (NSEC) for the event preparation, supervised and led computer science division members to participate in the scientific competition that focuses on computer science </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

Pada bagian ini saya menampilkan historis pendidikan saya
```ruby
<div class="section">
  <div class="container cc-education">
    <div class="h4 text-center mb-4 title">Education</div>
    <div class="card">
      <div class="row">
        <div class="col-md-3 bg-primary" data-aos="fade-right" data-aos-offset="50" data-aos-duration="500">
          <div class="card-body cc-education-header">
            <p>2021 - present</p>
            <div class="h5">Bachelor's Degree</div>
          </div>
        </div>
        <div class="col-md-9" data-aos="fade-left" data-aos-offset="50" data-aos-duration="500">
          <div class="card-body">
            <div class="h5">Informatics Engineering</div>
            <p class="category">Sepuluh Nopember Institute of Technology</p>
            <p>Current GPA : 3.92 / 4.00</p>
          </div>
        </div>
      </div>
    </div>
    <div class="card">
      <div class="row">
        <div class="col-md-3 bg-primary" data-aos="fade-right" data-aos-offset="50" data-aos-duration="500">
          <div class="card-body cc-education-header">
            <p>2018 - 2021</p>
            <div class="h5">High School</div>
          </div>
        </div>
        <div class="col-md-9" data-aos="fade-left" data-aos-offset="50" data-aos-duration="500">
          <div class="card-body">
            <div class="h5">Science and Mathematics</div>
            <p class="category">SMA Regina Pacis Bogor</p>
            <p>Final Grade : 94.7 / 100</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</div>
```
Di bagian ini saya menampilkan informasi kontak saya
```Ruby
<div class="section" id="contact">
  <div class="cc-contact-information" style="background-image: url('images/map.jpg')">
    <div class="container">
      <div class="cc-contact">
        <div class="row">
          <div class="col-md-9">
            <div class="card mb-0" data-aos="zoom-in">
              <div class="h4 text-center title">Contact Me</div>
              <div class="row">
                <div class="col-md-6">
                  <div class="card-body">
                    <form action="https://formspree.io/f/mrgvqpgd" method="POST">
                      <div class="p pb-3"><strong>Feel free to contact me </strong></div>
                      <div class="row mb-3">
                        <div class="col">
                          <div class="input-group"><span class="input-group-addon"><i class="fa fa-user-circle"></i></span>
                            <input class="form-control" type="text" name="name" placeholder="Name" required="required"/>
                          </div>
                        </div>
                      </div>
                      <div class="row mb-3">
                        <div class="col">
                          <div class="input-group"><span class="input-group-addon"><i class="fa fa-file-text"></i></span>
                            <input class="form-control" type="text" name="Subject" placeholder="Subject" required="required"/>
                          </div>
                        </div>
                      </div>
                      <div class="row mb-3">
                        <div class="col">
                          <div class="input-group"><span class="input-group-addon"><i class="fa fa-envelope"></i></span>
                            <input class="form-control" type="email" name="_replyto" placeholder="E-mail" required="required"/>
                          </div>
                        </div>
                      </div>
                      <div class="row mb-3">
                        <div class="col">
                          <div class="form-group">
                            <textarea class="form-control" name="message" placeholder="Your Message" required="required"></textarea>
                          </div>
                        </div>
                      </div>
                      <div class="row">
                        <div class="col">
                          <button class="btn btn-primary" type="submit">Send</button>
                        </div>
                      </div>
                    </form>
                  </div>
                </div>
                <div class="col-md-6">
                  <div class="card-body">
                    <p class="mb-0"><strong>Address </strong></p>
                    <p class="pb-2">Indonesia</p>
                    <p class="mb-0"><strong>Email</strong></p>
                    <p>rayssaravelia12@gmail.com</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  ```
  
 Bagian terakhir saya menampilkan footer yang berisi sosial media dan copyright
 ```ruby
 </div></div>
    </div>
    <footer class="footer">
      <div class="container text-center"><a class="cc-facebook btn btn-link" href="https://www.facebook.com/rayssa.ravelia"><i class="fa fa-facebook fa-2x " aria-hidden="true"></i></a><a class="cc-twitter btn btn-link " href="https://twitter.com/yeayray"><i class="fa fa-twitter fa-2x " aria-hidden="true"></i></a><a class="cc-google-plus btn btn-link" href="https://mail.google.com/mail/u/rayssaravelia12@gmail.com/#compose"><i class="fa fa-google-plus fa-2x" aria-hidden="true"></i></a><a class="cc-instagram btn btn-link" href="https://www.instagram.com/dat_rayssa/"><i class="fa fa-instagram fa-2x " aria-hidden="true"></i></a></div>
      <div class="h4 title text-center">Rayssa Ravelia</div>
      <div class="text-center text-muted">
        <p>&copy; All rights reserved.<br>@2023</p>
      </div>
    </footer>
    <script src="js/core/jquery.3.2.1.min.js?ver=1.1.0"></script>
    <script src="js/core/popper.min.js?ver=1.1.0"></script>
    <script src="js/core/bootstrap.min.js?ver=1.1.0"></script>
    <script src="js/now-ui-kit.js?ver=1.1.0"></script>
    <script src="js/aos.js?ver=1.1.0"></script>
    <script src="scripts/main.js?ver=1.1.0"></script>
  </body>
</html>
```
