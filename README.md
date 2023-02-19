# Tugas PWEB (CV dengan HTML)

## Identitas
| Name           | NRP        | Kelas     |
| ---            | ---        | ----------|
| Rayssa Ravelia | 5025211219 |Probstat A |

Pada CV yang saya buat terdapat beberapa bagian file yakni CSS, JS, images, dan HTML. Berikut ini adalah penjelasan detailnya:

## CSS
CSS merupakan bahasa yang digunakan untuk membuat desain dokumen HTML. Terdapat 3 file yang saya gunakan yaitu:
- aos.css

`AOS (animated on scroll)` merupakan library animasi pada CSS dan JavaScript yang memungkinkan elemen halaman web untuk dianimasikan saat pengguna scroll ke bawah atau ke atas halaman. 
Untuk menggunakan AOS, pertama-tama kita perlu menambahkan file `JavaScript dan CSS` dari library AOS ke dalam halaman web kita. Kemudian kita dapat menambahkan kelas CSS yang disediakan oleh AOS ke elemen yang ingin `dianimasikan`. Kita juga dapat mengatur opsi dan parameter animasi AOS menggunakan atribut data yang disediakan oleh AOS.

- bootstrap.min.css

File `bootstrap.min.css` adalah salah satu file inti dari Bootstrap. File ini berisi kumpulan `gaya CSS` yang diperlukan untuk membuat tampilan dan layout website yang sesuai dengan gaya Bootstrap.
Dengan menggunakan Bootstrap, saya dapat `menghemat waktu` dan upaya dalam mengembangkan website, karena mereka tidak perlu membuat gaya CSS dan komponen UI dari awal.

- main.css

File `main.css` merupakan file yang sangat penting dalam pengembangan website karena memungkinkan untuk `mengontrol dan menyesuaika` tampilan website secara keseluruhan. Dalam file ini, saya membuat aturan gaya yang spesifik untuk website mereka dan menghasilkan tampilan yang konsisten dan menarik untuk pengguna. Hal-hal yang saya atur adalah `warna dan jenis font, tata letak, efek visual, dan responsivitas`.

## JS
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

## Images
Terdapat 3 foto dengan format `jpg` yang saya gunakan dalam CV ini, yaitu:
- cc-bg.jpg

digunakan untuk background header CV

- map.jpg

digunakan untuk background footer CV

- rayssa,jpg

digunakan untuk foto pribadi pada CV

## HTML
