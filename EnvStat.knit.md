--- 
title: "Statistika Lingkungan Menggunakan R"
author: "Moh. Rosidi"
date: "2019-06-12"
knit: "bookdown::render_book"
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
colorlinks: yes
lof: yes
lot: yes
site: bookdown::bookdown_site
description: "Buku yang membahas penerapan R pada komputasi statistik di bidang Teknik Lingkungan"
cover-image: cover.png
apple-touch-icon: "Rosidi.png"
apple-touch-icon-size: 120
favicon: "Rosidi.png"
---



# Pengantar {-}



<style>
body{
text-align: justify}
</style>

Buku ini menyajikan penerapan program `R` dalam `Statistika Lingkungan`. Buku ini akan disajikan secara ringkas menggunakan sejumlah contoh kasus yang relevan dalam bidang lingkungan.

Penulis berharap buku ini dapat menjadi referensi sumber terbuka bagi mahasiswa yang ingin menggunakan `R` untuk kegiatan analisa data. Sehingga dapat mengurangi ketergantungan pada penggunaan aplikasi yang berlisensi.


<!--chapter:end:index.Rmd-->

# (PART\*) Bahasa Pemrograman R {-}

<style>
body{
text-align: justify}
</style>

# Mengenal Bahasa R 

Dewasa ini tersedia banyak sekali *software* yang dapat digunakan untuk membantu kita dalam melakukan analisa data. *software* yang digunakan dapat berupa *software* berbayar atau gratis.

`R` merupakan merupakan salah satu *software* gratis yang sangat populer di Indonesia. Kemudahan penggunaan serta banyaknya besarnya dukungan komunitas membuat `R` menjadi salah satu bahasa pemrograman paling populer di dunia.

Paket yang disediakan untuk analisis statistika juga sangat lengkap dan terus bertambah setiap saat. Hal ini membuat `R` banyak digunakan oleh para analis data.

Pada *chapter* ini penulis akan memperkenalkan kepada pembaca mengenai bahasa pemrograman `R`. Mulai dari sejarah, cara instalasi sampai dengan bagaimana kita memanfaatkan fitur dasar bantuan untuk menggali lebih jauh tentang fungsi-fungsi `R`.

## Sejarah R

`R` Merupakan bahasa yang digunakan dalam komputasi **statistik** yang pertama kali dikembangkan oleh **Ross Ihaka** dan **Robert Gentlement** di University of Auckland  New Zealand yang merupakan akronim dari nama depan kedua pembuatnya. Sebelum `R` dikenal ada `S` yang dikembangkan oleh **John Chambers** dan rekan-rekan dari **Bell Laboratories** yang memiliki fungsi yang sama untuk komputasi statistik. Hal yang membedakan antara keduanya adalah `R` merupakan sistem komputasi yang bersifat gratis.Logo `R` dapat dilihat pada Gambar \@ref(fig:Logo).

\begin{figure}

{\centering \includegraphics[width=0.4\linewidth]{r-icon} 

}

\caption{Logo R.}(\#fig:Logo)
\end{figure}

`R` dapat dibilang merupakan aplikasi sistem **statistik** yang kaya. Hal ini disebabkan banyak sekali paket yang dikembangkan oleh pengembang dan komunitas untuk keperluan analisa statistik seperti *linear regression*, *clustering*, *statistical test*, dll. Selain itu, `R` juga dapat ditambahkan paket-paket lain yang dapat meningkatkan fiturnya.

Sebagai sebuah bahasa pemrograman yang banyak digunakan untuk keperluan analisa data, `R` dapat dioperasikan pada berbagai sistem operasi pada komputer. Adapun sistem operasi yang didukung antara lain: `UNIX`, `Linux`, `Windows`, dan `MacOS`.


## Fitur dan Karakteristik R

`R` memiliki karakteristik yang berbeda dengan bahasa pemrograman lain seperti `C++`,`python`, dll. `R` memiliki aturan/sintaks yang berbeda dengan bahasa pemrograman yang lain yang membuatnya memiliki ciri khas tersendiri dibanding bahasa pemrograman yang lain.

Beberapa ciri dan fitur pada `R` antara lain:

1. **Bahasa `R` bersifat case sensitif**. maksudnya adalah dalam proses input `R` huruf besar dan kecil sangat diperhatikan. Sebagai contoh kita ingin melihat apakah objek A dan B pada sintaks berikut:

```r
A <- "Andi"
B <- "andi"

# cek kedua objek A dan B
A == B
```

```
## [1] FALSE
```

```r
# Kesimpulan : Kedua objek berbeda
```
2. **Segala sesuatu yang ada pada program `R` akan diangap sebagai objek**. konsep objek ini sama dengan bahasa pemrograma berbasis objek yang lain seperti `Java`, `C++`, `python`, dll.Perbedaannya adalah bahasa `R` relatif lebih sederhana dibandingkan bahasa pemrograman berbasis obejk yang lain.
3. **interpreted language atau script**. Bahasa `R` memungkinkan pengguna untuk melakukan kerja pada `R` tanpa perlu kompilasi kode program menjadi bahasa mesin.
4. Mendukung proses **loop**, **decision making**, dan menyediakan berbagai jenis **operstor** (aritmatika, logika, dll).
5. **Mendukung export dan import berbagai format file**, seperti:TXT, CSV, XLS, dll.
6. **Mudah ditingkatkan melalui penambahan fungsi atau paket**. Penambahan paket dapat dilakukan secara online melalui [CRAN](https://cran.r-project.org/) atau melalui sumber seperti [github](https://github.com/).
7. **Menyedikan berbagai fungsi untuk keperluan visualisasi data**. Visualisasi data pada `R` dapat menggunakan paket bawaan atau paket lain seperti `ggplo2`,`ggvis`, dll.

##  Kelebihan dan Kekurangan R

Selain karena `R` dapat digunakan secara gratis terdapat **kelebihan** lain yang ditawarkan, antara lain:

1. **Protability**. Penggunaan software dapat digunakan kapanpun tanpa terikat oleh masa berakhirnya lisensi.
2. **Multiplatform**. `R` bersifat *Multiplatform Operating Systems*, dimana *software* `R` lebih kompatibel dibanding *software* statistika lainnya. Hal in berdampak pada kemudahan dalam penyesuaian jika pengguna harus berpindah sistem operasi karena `R` baik pada sistem operasi seperti `windows` akan sama pengoperasiannya dengan yang ada di `Linux` (paket yang digunakan sama).
3. **General** dan **Cutting-edge**. Berbagai metode statistik baik metode klasik maupun baru telah diprogram kedalam `R`. Dengan demikian *software* ini dapat digunakan untuk analisis statistika dengan pendekatan klasik dan pendekatan modern.
4. **Programable**. Pengguna dapat memprogram metode baru atau mengembangakan modifikasi dari analisis statistika yang telah ada pada sistem `R`.
5. **Berbasis analisis matriks**. Bahasa `R` sangat baik digunakan untuk *programming* dengan basis matriks.
6. Fasiltas grafik yang lengkap.

Adapun kekurangan dari `R` antara lain:

1. **Point and Click GUI**. Interaksi utama dengan `R` bersifat *CLI* (*Command Line Interface*), walaupun saat ini telah dikembangkan paket yang memungkinkan kita berinteraksi dengan `R` menggunakan *GUI* (*Graphical User Interface*) sederhana menggunakan paket `R-Commander` yang memiliki fungsi yang terbatas. `R- Commander` sendiri merupakan *GUI* yang diciptakan dengan tujuan untuk keperluan pengajaran sehingga analisis statistik yang disediakan adalah yang klasik. Meskipun terbatas paket ini berguna jika kita membutuhkan analisis statistik sederhana dengan cara yang simpel.
2. **Missing statistical function**. Meskipun analisis statistika dalam `R` sudah cukup lengkap, namun tidak semua metode statistika telah diimplementasikan ke dalam `R`. Namun karena `R` merupakan *lingua franca* untuk keperluan komputasi statistika modern staan ini, dapat dikatakan ketersediaan fungsi tambahan dalam bentuk paket hanya masalah waktu saja.


##  RStudio

Aplikasi `R` pada dasarnya berbasis teks atau *command line* sehingga pengguna harus mengetikkan perintah-perintah tertentu dan harus hapal perintah-perintahnya. Setidaknya jika kita ingin melakukan kegiatan analisa data menggunakan `R` kita harus selalu siap dengan perintah-perintah yang hendak digunakan sehingga buku manual menjadi sesuatu yang wajib adasaat berkeja dengan `R`.

Kondisi ini sering kali membingunkan bagi pengguna pemula maupun pengguna mahir yang sudah terbiasa dengan aplikasi statistik lain seperti SAS, SPSS, Minitab, dll. Alasan itulah yang menyebabkan pengembang `R` membuat berbagai *frontend* untuk `R` yang berguna untuk memudahkan dalam pengoperasian `R`. 

`RStudio` merupakan salah satu bentuk *frontend* `R` yang cukup populer dan nyaman digunakan. Selain nyaman digunakan, `RStudio`  memungkinkan kita melakukan penulisan laporan menggunakan `Rmarkdown` atau `RNotebook` serta membuat berbagai bentuk project seperti shyni, dll. Pada `R` studio juga memungkinkan kita mengatur *working directory* tanpa perlu mengetikkan sintaks pada Commander, yang diperlukan hanya memilihnya di menu `RStudio`. Selain itu, kita juga dapat meng-import file berisikan data tanpa perlu mengetikkan pada Commander  dengan cara memilih pada menu `Environment`.

##  Menginstall R dan RStudio

Pada tutorial ini hanya akan dijelaskan bagaimana menginstal `R` dan `RStudio` pada sistem operasi `windows`. Sebelum memulai menginstal sebaiknya pembaca mengunduh terlebih dahulu *installer* [R](https://cran.r-project.org/bin/windows/base/) dan [RStudio](https://www.rstudio.com/products/rstudio/download/).

1. Jalankan proses pemasangan dengan meng-klik *installer* aplikasi `R` dan `RStudio`.
2. Ikuti langkah proses pemasangan aplikasi yang ditampilkan dengan klik `OK` atau `Next`.
3. Apabila pemasangan telah dilakukan, jalankan aplikasi yang telah terpasang untuk menguji jika aplikasi telah berjalan dengan baik.

Jendela aplikasi yang telah terpasang ditampilkan pada Gambar \@ref(fig:jendela-R) dan Gambar \@ref(fig:jendela-RStudio).

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{jendela_r} 

}

\caption{Jendela R.}(\#fig:jendela-R)
\end{figure}

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{jendela_rstudio} 

}

\caption{Jendela RStudio.}(\#fig:jendela-RStudio)
\end{figure}


> **Note: ** Sebaiknya install `R` terlebih dahulu sebelum `RStudio`

##  Working Directory

Setiap pengguna akan bekerja pada tempat khusus yang disebut sebagai *working directory*. *working directory* merupakan sebuah folder dimana `R` akan membaca dan menyimpan file kerja kita. Pada pengguna `windows`, *working directory* secara default pada saat pertama kali menginstall `R` terletak pada folder `c:\\Document`.

### Mengubah Lokasi Working Directory

Kita dapat mengubah lokasi *working directory* berdasarkan lokasi yang kita inginkan, misalnya letak data yang akan kita olah tidak ada pada folder default atau kita ingin pekerjaan kita terkait `R` dapat berlangsung pada satu folder khusus.

Berikut adalah cara mengubah *working directory* pada `R`.

1. Buatlah folder pada drive (kita bisa membuat folder pada selain drive c) dan namai dengan nama yang kalian inginkan. Pada tutorial ini penulis menggunakan nama folder `R`.
2. Jika pengguna menggunakan `RStudio`, pada menu `RStudio` pilih **Session > Set Working Directory > Chooses Directory**. Proses tersebut ditampilkan pada Gambar \@ref(fig:working)
3. Pilih folder yang telah dibuat pada step 1 sebagai *working directory.

> **Note: ** Data atau file yang hendak dibaca selama proses kerja pada `R` harus selalu diletakkan pada working directory. Jika tidak maka data atau file tidak akan terbaca.

Untuk mengecek apakah proses perubahan telah terjadi, kita dapat mengeceknya dengan menjalankan perintah berikut untuk melihat lokasi *working directory* kita yang baru.


```r
getwd()
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{working} 

}

\caption{Mengubah working directory.}(\#fig:working)
\end{figure}

Selain itu kita dapat mengubah *working directory* menggunakan perintah berikut:


```r
# Ubah working directori pada folder R
setwd("/Documents/R")
```

> **Note: ** Pada proses pengisian lokasi folder pastikan pemisah pada lokasi folder menggunakan tanda "/" bukan "\"

### Mengubah Lokasi Working Directory Default

Pada proses yang telah penulis jelaskan sebelumnya. Proses perubahan *working directory* hanya berlaku pada saat pekerjaan tersebut dilakukan. Setelah pekerjaan selesai dan kita menjalankan kembali `R` maka *working directory* akan kembali secara default pada working directory lama.

Untuk membuat lokasi default *working directory* pindah, kita dapat melakukannya dengan memilih pada menu: **Tools > Global options > pada "General" klik pada "Browse" dan pilih lokasi working directory yang diinginkan**. Proses tersebut ditampilkan pada Gambar \@ref(fig:default)

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{default} 

}

\caption{Merubah working directory melalui Global options.}(\#fig:default)
\end{figure}

## Fasilitas Help

Agar dapat menggunakan `R` dengan secara lebih baik, pengetahuan untuk mengakses fasilitas *help* in cukup penting untuk disampaikan. Adapun cara yang dapat digunakan adalah sebagai berikut.

### Mencari Help dari Suatu Perintah Tertentu

Untuk memperoleh bantuan terkait suatu perintah tertentu kita dapat menggunakan fungsi `help()`. Secara umum format yang digunakan adalah sebagai berikut:


```r
help(nama_perintah)
```

atau dapat juga menggunakan tanda tanya (?) pada awal `nama_perintah` seperti berikut:


```r
?nama_perintah
```

Misalkan kita kebingungan terkait bagaimana cara menuliskan perintah untuk menghitung rata-rata suatu vektor. Kita dapat mengetikkan perintah berikut untuk mengakses fasilitas *help*.


```r
help(mean)

#atau
?mean
```

Perintah tersebut akan memunculkan hasil berupa dokumentasi yang ditampilkan pada Gambar \@ref(fig:meandoc).

\begin{figure}

{\centering \includegraphics[width=0.5\linewidth]{meandoc} 

}

\caption{Jendela help dokumentasi fungsi mean().}(\#fig:meandoc)
\end{figure}

Keterangan pada jendela pada Gambar \@ref(fig:meandoc) adalah sebagia berikut:

1. Pada bagian jendela kiri atas jendela *help*, diberikan keterangan nama dari perintah yang sedang ditampilkan.
2. Selanjutnya, pada bagian atas dokumen, ditampilkan infomasi terkait nama perintah, dan nama *library* yang memuat perintah tersebut. Pada gambar diatas informasi terkait perintah dan nama *library* ditunjukkan pada teks `mean {base}` yang menunjukkan perintah `mean()` pada paket (*library*) *base* (paket bawaan `R`).
3. Setiap jendela *help* dari suatu perintah tertentu selanjutnya akan memuat bagian-bagian berikut:
- *Title*
- *Description* : deskripsi singkat tentang perintah.
- *Usage* : menampilkan sintaks perintah untuk penggunaan perintah tersebut.
- *Arguments* : keterangan mengenai *argument/input*yang diperlukan pada perintah tersebut.
- *Details* : keterangan lebih lengkap lengkap tentang perintah tersebut.
- *Value* : keterangan tentang *output* suatu perintah dapat diperoleh pada bagian ini.
- *Author(s)* : memberikan keterangan tentang *Author* dari perintah tersebut.
- *References* : seringkali referensi yang dapat digunakan untuk memperoleh keterangan lebih lanjut terhadap suatu perintah ditampilkan pada bagian ini.
- *See also*: bagian ini berisikan daftar perintah/fungsi yang berhubungan erat dengan perintah tersebut.
- *Example* : berisikan contoh-contoh penggunaan perintah tersebut.

Kita juga dapat melihat contoh penggunaan dari perintah tersebut. Untuk melakukannya kita dapat menggunakan fungsi `example()`. Fungsi tersebut akan menampilkan contoh kode penerapan dari fungsi yang kita inginkan. Secara sederhana fungsi tersebut dapat dituliskan sebagai berikut:


```r
example(nama_perintah)
```

Untuk mengetahui contoh kode fungsi `mean()`, ketikkan sintaks berikut:


```r
example(mean)
```

```
## 
## mean> x <- c(0:10, 50)
## 
## mean> xm <- mean(x)
## 
## mean> c(xm, mean(x, trim = 0.10))
## [1] 8.75 5.50
```

kita juga dapat mencoba kode yang dihasilkan pada console `R`. Berikut adalah contoh penerapannya:


```r
# Menghitung rata-rata bilangan 1 sampai 10 dan 50
# membuat vektor
x <- c(0:10, 50)

# Print
x
```

```
##  [1]  0  1  2  3  4  5  6  7  8  9 10 50
```

```r
# mean
mean(x)
```

```
## [1] 8.75
```

Pembaca dapat mencoba melakukanya sendiri dengan mengganti nilai yang telah ada serta mencoba contoh kode yang lain.

### General Help

Kita juga dapat membaca beberapa dokumen manual yang ada pada `R`. Untuk melakukannya jalankan perintah berikut:


```r
help.start()
```

Output yang dihasilkan berupa link pada sejumlah dokumen yang dapat kita klik. Tampilan halaman yang dihasilkan disajikan pada Gambar \@ref(fig:generalhelp).

\begin{figure}

{\centering \includegraphics[width=0.5\linewidth]{generalhelp} 

}

\caption{Jendela general help dokumentasi fungsi mean().}(\#fig:generalhelp)
\end{figure}

### Fasilitas Help Lainnya

Selain yang telah penulis sebutkan sebelumnya. Kita juga dapat memanfaatkan fasilitas *help* lainnya melalui fungsi `apropos()` dan `help.search()`.

`apropos ()`: mengembalikan daftar objek, berisi pola yang pembaca cari, dengan pencocokan sebagian. Ini berguna ketika pembaca tidak ingat persis nama fungsi yang akan digunakan. Berikut adalah contoh ketika penulis ingin mengetahui fungsi yang digunakan untuk menghitung median.


```r
apropos("med")
```

```
## [1] "elNamed"        "elNamed<-"      "median"        
## [4] "median.default" "medpolish"      "runmed"
```

*List* yang dihasilkan berupa fungsi-fungsi yang memiliki elemen kata "med". Berdasarkan pencaria tersebut penulis dapat mencoba menggunakan fungsi "median" untuk menghitung median.

`help.search ()` (sebagai alternatif ??): mencari dokumentasi yang cocok dengan karakter yang diberikan dengan cara yang berbeda. Ini mengembalikan daftar fungsi yang mengandung istilah yang pembaca cari dengan deskripsi singkat dari fungsi.

Berikut adalah contoh penerapan dari fungsi tersebut:


```r
help.search("mean")

# atau
??mean
```

*Output* yang dihasilkan akan tampak seperti pada Gambar \@ref(fig:helpsearch).

\begin{figure}

{\centering \includegraphics[width=0.5\linewidth]{helpsearch} 

}

\caption{Jendela help search dokumentasi fungsi mean().}(\#fig:helpsearch)
\end{figure}


## Referensi

1. Primartha, R. 2018. **Belajar Machine Learning Teori dan Praktik**. Penerbit Informatika : Bandung
2. Rosadi,D. 2016. **Analisis Statistika dengan R**. Gadjah Mada University Press: Yogyakarta
3. STHDA. Running RStudio and Setting Up Your Working Directory - Easy R Programming .<http://www.sthda.com/english/wiki/running-rstudio-and-setting-up-your-working-directory-easy-r-programming#set-your-working-directory>
4. STDHA. **Getting Help With Functions In R Programming**. <http://www.sthda.com/english/wiki/getting-help-with-functions-in-r-programming> .
5. Venables, W.N. Smith D.M. and R Core Team. 2018. **An Introduction to R**. R Manuals.

<!--chapter:end:01-mengenal-bahasa-r.Rmd-->

<style>
body{
text-align: justify}
</style>

# Dasar Pemrograman Menggunakan R

Pada *chapter* ini penulis hendak mengajak pembaca lebih familiar dengan sintaks atau perintah yang ada pada `R` yang akan membantu pembaca untuk melakukan pemrograman pada `R`. Pembaca akan mempelajari penggunaan operator dalam melakukan operasi pengolahan data pada `R`, jenis data yang ada pada `R`, sampai dengan bagaimana kita melakukan proses *decision making* menggunakan `R`. 

## Operator Aritmatika

Proses perhitungan akan ditangani oleh fungsi khusus. `R` akan memahami urutannya secara benar. Kecuali kita secara eksplisit menetapkan yang lain. Sebagai contoh jalankan sintaks berikut:


```r
2+4*2
```

```
## [1] 10
```

Bandingkan dengan sintaks berikut:


```r
(2+4)*2
```

```
## [1] 12
```

> `R` dapat digunakan sebagai kalkulator

Berdasarkan kedua hasil tersebut dapat disimpulkan bahwa ketika kita tidak menetapkan urutan perhitungan menggunakan tanda kurung, `R` akan secara otomatis akan menghitung terlebih dahulu perkalian atau pembangian. 

Operator aritmatika yang disediakan `R` disajikan pada Tabel \@ref(tab:oparitmatika):


**Simbol**     | **Keterangan**
---------------|--------------------------------------------------------------------------------------
+              | *Addition*, untuk operasi penjumlahan
-              | *Substraction*, untuk operasi pengurangan
*              | *Multiplication*, untuk operasi pembagian
/              | *Division*, untuk operasi pembagian
^              | *Eksponentiation*, untuk operasi pemangkatan
%%             | *Modulus*, Untuk mencari sisa pembagian
%/%            | *Integer*, Untuk mencari bilangan bulat hasil pembagian saja dan tanpa sisa pembagian

*: (\#tab:oparitmatika) Operator Aritmatika `R`.*

Untuk lebih memahaminya berikut contoh sintaks penerapan operator tersebut.


```r
# Addition
5+3
```

```
## [1] 8
```

```r
# Substraction
5-3
```

```
## [1] 2
```

```r
# Multiplication
5*3
```

```
## [1] 15
```

```r
# Division
5/3
```

```
## [1] 1.667
```

```r
# Eksponetiation
5^3
```

```
## [1] 125
```

```r
# Modulus
5%%3
```

```
## [1] 2
```

```r
# Integer
5%/%3
```

```
## [1] 1
```

> *Note: * Pada `R` tanda `#` berfungsi menambahkan keterangan untuk menjelaskan sebuah sintaks pada `R`.

## Fungsi Aritmetik

Selain fungsi operator aritmetik, pada `R` juga telah tersedia fungsi aritmetik yang lain seperti logaritmik, ekponensial, trigonometri, dll.

1. Logaritma dan eksponensial

Untuk contoh fungsi logaritmik dan eksponensial jalankan sintaks berikut:


```r
log2(8) # logaritma basis 2 untuk 8
```

```
## [1] 3
```

```r
log10(8) # logaritma basis 10 untuk 8
```

```
## [1] 0.9031
```

```r
exp(8) # eksponensial 8
```

```
## [1] 2981
```

2. Fungsi trigonometri

fungsi trigonometri yang ditampilkan seperti sin,cos, tan, dll.


```r
cos(x) # cos x
sin(x) # Sin x
tan(x) # Tan x
acos(x) # arc-cos x
asin(x) # arc-sin x
atan(x) #arc-tan x
```

> **Note: ** x dalam fungsi trigonometri memiliki satuan radian

Berikut adalah salah satu contoh penggunaannya:


```r
cos(pi)
```

```
## [1] -1
```


3. Fungsi matematik lainnya

Fungsi lainnya yang dapat digunakan adalah fungsi absolut, akar kuadrat, dll. Berikut adalah contoh sintaks penggunaan fungsi absolut dan akar kuadrat.


```r
abs(-2) # nilai absolut -2
```

```
## [1] 2
```

```r
sqrt(4) # akar kuadrat 4
```

```
## [1] 2
```

## Operator Relasi

Operator relasi digunakan untuk membandingkan satu objek dengan objek lainnya. Operator yang disediakan `R` disajikan pada Tabel \@ref(tab:oprelasi).

**Simbol**     | **Keterangan**           
---------------|---------------------------
">"            | Lebih besar dari
"<"            | Lebih Kecil dari
"=="           | Sama dengan
">="           | Lebih besar sama dengan
"<="           | Lebih kecil sama dengan
"!="           | Tidak sama dengan

: (\#tab:oprelasi) Operator Relasi `R`.

Berikut adalah penerapan operator pada tabel tersebut:


```r
x <- 34
y <- 35

# Operator >
x > y
```

```
## [1] FALSE
```

```r
# Operator <
x < y
```

```
## [1] TRUE
```

```r
# operator ==
x == y
```

```
## [1] FALSE
```

```r
# Operator >=
x >= y
```

```
## [1] FALSE
```

```r
# Operator <=
x <= y
```

```
## [1] TRUE
```

```r
# Operator !=
x != y
```

```
## [1] TRUE
```

## Operator Logika

Operator logika hanya berlaku pada vektor dengan tipe logical, numeric, atau complex. Semua angka bernilai 1 akan dianggap bernilai logika `TRUE`. Operator logika yang disediakan `R` dapat dilihat pada Tabel \@ref(tab:oplogika).

**Simbol**     | **Keterangan**           
---------------|----------------------------------
&&             | Operator logika AND
'||'           | Operator logika OR
!              | Opeartor logika NOT
&              | Operator logika AND element wise
'|'            | Operator logika OR element wise
 
: (\#tab:oplogika) Operator logika `R`.

Penerapannya terdapat pada sintaks berikut:


```r
v <- c(TRUE,TRUE, FALSE)
t <- c(FALSE,FALSE,FALSE)

# Operator &&
print(v&&t)
```

```
## [1] FALSE
```

```r
# Operator ||
print(v||t)
```

```
## [1] TRUE
```

```r
# Operator !
print(!v)
```

```
## [1] FALSE FALSE  TRUE
```

```r
# operator &
print(v&t)
```

```
## [1] FALSE FALSE FALSE
```

```r
# Operator |
print(v|t)
```

```
## [1]  TRUE  TRUE FALSE
```

> **Note: ** 
>
> operator & dan | akan mengecek logika tiap elemen pada vektor secara berpesangan (sesuai urutan dari kiri ke kanan). 
>
>Operator %% dan || hanya mengecek dari kiri ke kanan pada observasi pertama. Misal saat menggunakan && jika observasi pertama TRUE maka observasi pertama pada vektor lainnya akan dicek, namun jika observasi pertama FALSE maka proses akan segera dihentikan dan menghasilkan FALSE.

## Memasukkan Nilai Kedalam Variabel

Variabel pada `R` dapat digunakan untuk menyimpan nilai. Sebagai contoh jalankan sintaks berikut:


```r
# Harga sebuah lemon adalah 500 rupiah
lemon <- 500

# Atau
500 -> lemon

# dapat juga menggunakan tanda "="
lemon = 500
```

> **Note: **
>
> 1. `R` memungkinkan penggunaan <-,->, atau = sebagai perintah pengisi nilai variabel
>
> 2. `R` bersifat *case-sensitive*. Maksudnya adalah variabel Lemon tidak sama dengan lemon (Besar kecil huruf berpengaruh)

Untuk mengetahui nilai dari objek `lemon` kita dapat menggunakan fungsi `print()` atau mengetikkan nama objeknya secara langsung.


```r
# Menggunakan fungsi print()
print(lemon)
```

```
## [1] 500
```

```r
# Atau
lemon
```

```
## [1] 500
```

`R` akan menyimpan variabel `lemon` sebagai objek pada memori. Sehingga kita dapat melakukan operasi terhadap objek tersebut seperti mengalikannya atau menjumlahkannya dengan bilangan lain. Sebagai contoh jalankan sintaks berikut:


```r
# Operasi perkalian terhadap objek lemon
5*lemon
```

```
## [1] 2500
```

Kita dapat juga mengubah nilai dari objek `lemon` dengan cara menginput nilai baru terhadap objek yang sama. `R` secara otomatis akan menggatikan nilai sebelumnya. Untuk lebih memahaminya jalankan sintaks berikut:


```r
lemon <- 1000

# Print lemon
print(lemon)
```

```
## [1] 1000
```

Untuk lebih memahaminya berikut adalah sintaks untuk menghitung volume suatu objek.


```r
# Dimensi objek
panjang <- 10
lebar <- 5
tinggi <- 5

# Menghitung volume
volume <- panjang*lebar*tinggi

# Print objek volume
print(volume)
```

```
## [1] 250
```

Untuk mengetahui objek apa saja yang telah kita buat sepanjang artikel ini kita dapang menggunakan fungsi `ls()`.


```r
ls()
```

```
##  [1] "A"         "B"         "img1_path" "lebar"    
##  [5] "lemon"     "panjang"   "t"         "tinggi"   
##  [9] "v"         "volume"    "x"         "xm"       
## [13] "y"
```

> Kumpulan objek yang telah tersimpan dalam memori disebut sebagai **workspace**

Untuk menghapus objek pada memori kita dapat menggunakan fungsi `rm()`. Pada sintaks berikut penulis hendak menghapus objek `lemon` dan `volume`.


```r
# Menghapus objek lemon dan volume
rm(lemon, volume)

# Tampilkan kembali objek yang tersisa
ls()
```

```
##  [1] "A"         "B"         "img1_path" "lebar"    
##  [5] "panjang"   "t"         "tinggi"    "v"        
##  [9] "x"         "xm"        "y"
```

> **Note: ** Setiap variabel atau objek yang dibuat akan menempati sejumlah memori pada komputer sehingga jika kita bekerja dengan jumlah data yang banyak pastikan kita menghapus seluruh objek pada memori sebelum memulai kerja.

## Tipe dan Struktur Data

Data pada `R` dapat dikelompokan berdasarkan beberapa tipe. Tipe data pada `R` disajikan pada Tabel \@ref(tab:tipedata).

**Tipe Data**  | **Contoh**              | **Keterangan**
---------------|-------------------------|---------------------------------------------------------------------------------
Logical        | TRUE, FALSE             | Nilai Boolean
Numeric        | 12.3, 5, 999            | Segala jenis angka
Integer        | 23L, 97L, 3L            | Bilangan integer (bilangan bulat)
Complex        | 2i, 3i, 9i              | Bilangan kompleks
Character      | 'a', "b", "123"         | Karakter dan string
Factor         | 1, 0, "Merah"           | Dapat berupa numerik atau string (namun pada proses akan terbaca sebagai angka)
Raw            | Identik dengan "hello"  | Segala jenis data yang disimpan sebagai raw bytes

: (\#tab:tipedata) Tipe data `R`.

Sintaks berikut adalah contoh dari tipe data pada `R`. Untuk mengetahui tipa data suatu objek kita dapat menggunakan perintah `class()`


```r
# Logical
apel <- TRUE
class(apel)
```

```
## [1] "logical"
```

```r
# Numeric
x <- 2.3
class(x)
```

```
## [1] "numeric"
```

```r
# Integer
y <- 2L
class(y)
```

```
## [1] "integer"
```

```r
# Compleks
z <- 5+2i
class(z)
```

```
## [1] "complex"
```

```r
# string
w <- "saya"
class(w)
```

```
## [1] "character"
```

```r
# Raw
xy <- charToRaw("hello world")
class(xy)
```

```
## [1] "raw"
```

Keenam jenis data tersebut disebut sebagai tipe data atomik. Hal ini disebabkan karena hanya dapat menangani satu tipe data saja. Misalnya hanya numeric atau hanya integer.

Selain menggunakan fungsi `class()`, kita dapat pula menggunakan fungsi `is_numeric()`, `is.character()`, `is.logical()`, dan sebagainya berdasarkan jenis data apa yang ingin kita cek. Berbeda dengan fungsi `class()`, ouput yang dihasilkan pada fungsi seperti `is_numeric()` adalah nilai Boolean sehingga fungsi ini hanya digunakan untuk mengecek apakah jenis data pada objek sama seperti yang kita pikirkan. Sebagai contoh disajikan pada sintaks berikut:


```r
data <- 25

# Cek apakah objek berisi data numerik
is.numeric(data)
```

```
## [1] TRUE
```

```r
# Cek apakah objek adalah karakter
is.character(data)
```

```
## [1] FALSE
```

Kita juga dapat mengubah jenis data menjadi jenis lainnya seperti integer menjadi numerik atau sebaliknya. Fungsi yang digunakan adalah `as.numeric()` jika ingin mengubah suatu jenis data menjadi numerik. Fungsi lainnya juga dapat digunakan sesuai dengan kita ingin mengubah jenis data objek menjadi jenis data lainnya.


```r
# Integer
apel <- 2L

# Ubah menjadi numerik
as.numeric(apel)
```

```
## [1] 2
```

```r
# Cek
is.numeric(apel)
```

```
## [1] TRUE
```

```r
# Logical
nangka <- TRUE

# Ubah logical menjadi numeric
as.numeric(nangka)
```

```
## [1] 1
```

```r
# Karakter
minum <- "minum"

# ubah karakter menjadi numerik
as.numeric(minum)
```

```
## Warning: NAs introduced by coercion
```

```
## [1] NA
```

> **Note: ** Konversi karakter menjadi numerik akan menghasilkan output NA (*not available*). `R` tidak mengetahui bagaimana cara merubah karakter menjadi bentuk numerik.

Berdasarkan Tabel 2, vektor karakter dapat dibuat menggunakan tanda kurung baik *double quote* ("") maupun *single quote* ('').Jika pada teks yang kita tuliskan mengandung *quote* maka kita harus menghentikannya menggunakan tanda ( \ ). Sbegai contoh kita ingin menuliskan `**My friend's name is "Adi"**, pada sintaks akan dituliskan:


```r
'My friend\`s name is "Adi"'
```

```
## [1] "My friend`s name is \"Adi\""
```

```r
# Atau

"My friend's name \"Adi\""
```

```
## [1] "My friend's name \"Adi\""
```

Struktur data diklasifikasikan berdasarkan dimensi data dan tie data di dalamnya (homogen atau heterogen). Klasifikasi jenis data disajikan pada Tabel \@ref(tab:strukturdata).

**Dimensi**  | **Homogen**      | **Heterogen**
-------------|------------------|---------------
1d           | Atomik vektor    | List
2d           | Matriks          | Dataframe
nd           | Array            |               

: (\#tab:strukturdata) Struktur data `R`.

Berdasarkan Tabel tersebut dapat kita lihat bahwa objek terbagi atas dua buah struktur data yaitu homogen dan heterogen. Objek dengan struktur data homogen hanya dapat menyimpan satu tipe atau jenis data saja (numerik saja atau factor saja), sedangkan objek dengan struktur data heterogen akan dapat menyimpan berbagai jenis data. 

Berdasarkan daftar yang ada di Tabel \@ref(tab:strukturdata), kita tidak akan membahas struktur data Array pada buku ini. Struktur data tersebut lebih banyak digunakan untuk kepentingan akademis seperti membuat model matematis yang akan penulis bahas pada buku lain.

## Vektor

Vektor merupakan kombinasi berbagai nilai (numerik, karakter, logical, dan sebagainya berdasarkan jenis input data) pada objek yang sma. Pada contoh kasus berikut, pembaca akan memiliki sesuai jenis data input yaitu**vektor numerik**, **vector karakter**, **vektor logical**, dll.


### Membuat vektor

Vektor dibuat dengan menggunakan fungsi `c()`(concatenate) seperti yang disajikan pada sintaks berikut:


```r
# membuat vektor numerik
x <- c(3,3.5,4,7)
x # print vektor
```

```
## [1] 3.0 3.5 4.0 7.0
```

```r
# membuat vektor karakter
y <- c("Apel", "Jeruk", "Rambutan", "Salak")
y # print vektor
```

```
## [1] "Apel"     "Jeruk"    "Rambutan" "Salak"
```

```r
# membuat vektor logical
t <- c("TRUE", "FALSE", "TRUE")
t # print vektor
```

```
## [1] "TRUE"  "FALSE" "TRUE"
```

selain menginput nilai pada vektor, kita juga dapat memberi nama nilai setiap vektor menggunakan fungsi `names()`.


```r
# Membuat vektor jumlah buah yang dibeli
Jumlah <- c(5,5,6,7)
names(Jumlah) <- c("Apel", "Jeruk", "Rambutan", "Salak")

# Atau
Jumlah <- c(Apel=5, Jeruk=5, Rambutan=6, Salak=7)

# Print
Jumlah
```

```
##     Apel    Jeruk Rambutan    Salak 
##        5        5        6        7
```

> **Note: ** Vektor hanya dapat memuat satu buah jenis data. Vektor hanya dapat mengandung jenis data numerik saja, karakter saja, dll.

Untuk menentukan panjang sebuah vektor kita dapat menggunakan fungsi `lenght()`.


```r
length(Jumlah)
```

```
## [1] 4
```

### Missing Values

Seringkali nilai pada vektor kita tidak lengkap atau terdapat nilai yang hilang (*missing value*) pada vektor. *Missing value* pada `R` dilambangkan oleh `NA`(*not available*). Berikut adalah contoh vektor dengan *missing value*.


```r
Jumlah <- c(Apel=5, Jeruk=NA, Rambutan=6, Salak=7)
```

Untuk mengecek apakah dalam objek terdapat *missing value* dapat menggunakan fungsi `is.na()`. ouput dari fungsi tersebut adalah nilai Boolean. Jika terdapat *Missing value*, maka output yang dihasilkan akan memberikan nilai `TRUE`.


```r
is.na(Jumlah)
```

```
##     Apel    Jeruk Rambutan    Salak 
##    FALSE     TRUE    FALSE    FALSE
```

> **Note: **
> 
> Selain NA terdapat NaN (*not a number*) sebagai *missing value8*. Nilai tersebut muncul ketika fungsi matematika yang digunakan pada proses perhitungan tidak bekerja sebagaimana mestinya. Contoh: 0/0 = NaN
>
> `is.na()` juga akan menghasilkan nilai `TRUE` pada NaN. Untuk membedakannya dengan NA dapat digunakan fungsi `is.nan()`.

### Subset Pada Vektor

*Subseting vector* terdiri atas tiga jenis, yaitu: *positive indexing*, *Negative Indexing*, dan .

* **Positive indexing**: memilih elemen vektor berdasarkan posisinya (indeks) dalam kurung siku.


```r
# Subset vektor pada urutan kedua
Jumlah[2]
```

```
## Jeruk 
##    NA
```

```r
# Subset vektor pada urutan 2 dan 4
Jumlah[c(2, 4)]
```

```
## Jeruk Salak 
##    NA     7
```

Selain melalui urutan (indeks), kita juga dapat melakukan subset (membuat himpunan bagian) berdasarkan nama elemen vektornya.


```r
Jumlah["Jeruk"]
```

```
## Jeruk 
##    NA
```

> **Note: ** Indeks pada `R` dimulai dari 1. Sehingga kolom atau elemen pertama vektor dimulai dari [1]

* **Negative indexing**: mengecualikan (*exclude*) elemen vektor.


```r
# mengecualikan elemen vektor 2 dan 4
Jumlah[-c(2,4)]
```

```
##     Apel Rambutan 
##        5        6
```

```r
# mengecualikan elemen vektor 1 sampai 3
Jumlah[-c(1:3)]
```

```
## Salak 
##     7
```

* **Subset berdasarkan vektor logical**: Hanya, elemen-elemen yang nilai yang bersesuaian dalam vektor pemilihan bernilai TRUE, akan disimpan dalam subset.

> **Note: ** panjang vektor yang digunakan untuk subset harus sama.


```r
Jumlah <- c(Apel=5, Jeruk=NA, Rambutan=6, Salak=7)

# selecting vector
merah <- c(TRUE, FALSE, TRUE, FALSE)

# Subset
Jumlah[merah==TRUE]
```

```
##     Apel Rambutan 
##        5        6
```

```r
# Subset untuk elemen vektor bukan missing value
Jumlah[!is.na(Jumlah)]
```

```
##     Apel Rambutan    Salak 
##        5        6        7
```

### Operasi Matematis Menggunakan Vektor

Jika pembaca melakukan operasi dengan vektor, operasi akan diterapkan ke setiap elemen vektor. Contoh disediakan pada sintaks di bawah ini:


```r
pendapatan <- c(2000, 1800, 2500, 3000)
names(pendapatan) <- c("Andi", "Joni", "Lina", "Rani")
pendapatan
```

```
## Andi Joni Lina Rani 
## 2000 1800 2500 3000
```

```r
# Kalikan pendapatan dengan 3
pendapatan*3
```

```
## Andi Joni Lina Rani 
## 6000 5400 7500 9000
```

Seperti yang dapat dilihat, `R` mengalikan setiap elemen dengan bilangan pengali.

Kita juga dapat mengalikan vektor dengan vektor lainnya.Contohnya disajikan pada sintaks berikut:


```r
# membuat vektor dengan panjang sama dengan dengan vektor pendapatan
coefs <- c(2, 1.5, 1, 3)

# Mengalikan pendapatan dengan vektor coefs
pendapatan*coefs
```

```
## Andi Joni Lina Rani 
## 4000 2700 2500 9000
```

Berdasarkan sintaks tersebut dapat terlihat bahwa operasi matematik terhadap masing-masing vektor dapat berlangsung jika panjang vektornya sama.

Berikut adalah fungsi lain yang dapat digunakan pada operasi matematika vektor.


```r
max(x) # memperoleh nilai maksimum x
min(x) # memperoleh nilai minimum x
range(x) # memperoleh range vektor x
length(x) # memperoleh jumlah elemen vektor x
sum(x) # memperoleh total penjumlahan elemen vektor x
prod(x) # memeperoleh produk elemen vektor x
mean(x) # memperoleh nilai rata-rata seluruh elemen vektor x
sd(x) # standar deviasi vektor x
var(x) # varian vektor x
sort(x) # mengurutkan elemen vektor x dari yang terbesar
```

Contoh penggunaan fungsi tersebut disajikan beberapa pada sintaks berikut:


```r
# Menghitung range pendapatan
range(pendapatan)
```

```
## [1] 1800 3000
```

```r
# menghitung rata-rata dan standar deviasi pendapatan
mean(pendapatan)
```

```
## [1] 2325
```

```r
sd(pendapatan)
```

```
## [1] 537.7
```

## Matriks

Matriks seperti Excel sheet yang berisi banyak baris dan kolom (kumpulan bebrapa vektor). Matriks digunakan untuk menggabungkan vektor dengan tipe yang sama, yang bisa berupa numerik, karakter, atau logis. Matriks digunakan untuk menyimpan tabel data dalam R. Baris-baris matriks pada umumnya adalah individu / pengamatan dan kolom adalah variabel.

### Membuat matriks

Untuk membuat matriks kita dapat menggunakan fungsi `cbind()` atau `rbind()`. Berikut adalah contoh sintaks untuk membuat matriks.


```r
# membuat vektor numerik
col1 <- c(5, 6, 7, 8, 9)
col2 <- c(2, 4, 5, 9, 8)
col3 <- c(7, 3, 4, 8, 7)

# menggabungkan vektor berdasarkan kolom
my_data <- cbind(col1, col2, col3)
my_data
```

```
##      col1 col2 col3
## [1,]    5    2    7
## [2,]    6    4    3
## [3,]    7    5    4
## [4,]    8    9    8
## [5,]    9    8    7
```

```r
# Mengubah atau menambahkan nama baris
rownames(my_data) <- c("row1", "row2", "row3", "row4", "row5")
my_data
```

```
##      col1 col2 col3
## row1    5    2    7
## row2    6    4    3
## row3    7    5    4
## row4    8    9    8
## row5    9    8    7
```

> **Note: **
>
> + **cbind()**: menggabungkan objek `R` berdasarkan kolom
> + **rbind()**: menggabungkan objek `R` berdasarkan baris
> + **rownames()**: mengambil atau menetapkan nama-nama baris dari objek seperti-matriks
> + **colnames()**: mengambil atau menetapkan nama-nama kolom dari objek seperti-matriks

Kita dapat melakukan tranpose (merotasi matriks sehingga kolom menjadi baris dan sebaliknya) menggunakan fungsi `t()`. Berikut adalah contoh penerapannya:


```r
t(my_data)
```

```
##      row1 row2 row3 row4 row5
## col1    5    6    7    8    9
## col2    2    4    5    9    8
## col3    7    3    4    8    7
```

Selain melalui pembentukan sejumlah objek vektor, kita juga dapat membuat matriks menggunakan fungsi `matrix()`. Secara sederhana fungsi tersebut dapat dituliskan sebagai berikut:


```r
matrix(data = NA, nrow = 1, ncol = 1, byrow = FALSE,
       dimnames = NULL)
```

> **Note: **
>
> + **data**: vektor data opsional
> + **nrow**, **ncol**: jumlah baris dan kolom yang diinginkan, masing-masing.
> + **byrow**: nilai logis. Jika FALSE (default) matriks diisi oleh kolom, jika tidak, matriks diisi oleh baris.
> + **dimnames**: Daftar dua vektor yang memberikan nama baris dan kolom masing-masing.

Dalam kode `R` di bawah ini, data input memiliki panjang 6. Kita ingin membuat matriks dengan dua kolom. Kita tidak perlu menentukan jumlah baris (di sini `nrow = 3`). `R` akan menyimpulkan ini secara otomatis. Matriks diisi kolom demi kolom saat argumen `byrow = FALSE`. Jika kita ingin mengisi matriks dengan baris, gunakan `byrow = TRUE`. Berikut adalah contoh pembuatan matriks menggunakan fungsi `matrix()`.


```r
data <- matrix(
           data = c(1,2,3, 11,12,13), 
           nrow = 2, byrow = TRUE,
           dimnames = list(c("row1", "row2"), c("C.1", "C.2", "C.3"))
           )
data
```

```
##      C.1 C.2 C.3
## row1   1   2   3
## row2  11  12  13
```

Untuk mengetahui dimensi dari suatu matriks, kita dapat menggunakan fungsi `ncol()` untuk mengetahui jumlah kolom matriks dan `nrow()` untuk mengetahui jumlah baris pada matriks. Berikut adalah contoh penerapannya:


```r
# mengetahui jumlah kolom
ncol(my_data)
```

```
## [1] 3
```

```r
# mengetahui jumlah baris
nrow(my_data)
```

```
## [1] 5
```

Jika ingin memperoleh ringkasan terkait dimensi matriks kita juga dapat mengunakan fungsi `dim()` untuk mengetahui jumlah baris dan kolom matriks. Berikut adalah contoh penerapannya:


```r
dim(my_data) # jumlah baris dan kolom
```

```
## [1] 5 3
```

### Subset Pada Matriks

Sama dengan vektor, subset juga dapat dilakukan pada matriks. Bedanya subset dilakukan berdasarkan baris dan kolom pada matriks.

* **Memilih baris/kolom** berdasarkan pengindeksan positif

baris atau kolom dapat diseleksi menggunakan format `data[row, col]`. Cara selesi ini sama dengan vektor, bedanya kita harus menetukan baris dan kolom dari data yang akan kita pilih. Berikut adalah contoh penerapannya:


```r
# Pilih baris ke-2
my_data[2,]
```

```
## col1 col2 col3 
##    6    4    3
```

```r
# Pilih baris 2 sampai 4
my_data[2:4,]
```

```
##      col1 col2 col3
## row2    6    4    3
## row3    7    5    4
## row4    8    9    8
```

```r
# Pilih baris 2 dan 4
my_data[c(2,4),]
```

```
##      col1 col2 col3
## row2    6    4    3
## row4    8    9    8
```

```r
# Pilih baris 2 dan kolom 3
my_data[2, 3]
```

```
## [1] 3
```

* **Pilih berdasarkan nama baris/kolom**

Berikut adalah contoh subset berdasarkan nama baris atau kolom.


```r
# Pilih baris 1 dan kolom 3
my_data["row1","col3"]
```

```
## [1] 7
```

```r
# Pilih baris 1 sampai 4 dan kolom 3
baris <- c("row1","row2","row3")
my_data[baris, "col3"]
```

```
## row1 row2 row3 
##    7    3    4
```

* **Kecualikan baris/kolom** dengan pengindeksan negatif

Sama seperti vektor pengecualian data dapat dilakukan di matriks menggunakan pengindeksan negatif. Berikut cara melakukannya:


```r
# Kecualikan baris 2 dan 3 serta kolom 3
my_data[-c(2,3), -3]
```

```
##      col1 col2
## row1    5    2
## row4    8    9
## row5    9    8
```

* **Pilihan dengan logik**

Dalam kode `R` di bawah ini, misalkan kita ingin hanya menyimpan baris di mana col3> = 4:


```r
col3 <- my_data[, "col3"]
my_data[col3 >= 4, ]
```

```
##      col1 col2 col3
## row1    5    2    7
## row3    7    5    4
## row4    8    9    8
## row5    9    8    7
```

### Perhitungan Menggunakan Matriks
_
Kita juga dapat melakukan operasi matematika pada matriks. Pada operasi matematika pada matriks proses yang terjadi bisa lebih kompleks dibanding pada vektor, dimana kita dapat melakukan operasi untuk memperoleh gambaran data pada tiap kolom atau baris.

Berikut adalah contoh operasi matematika sederhana pada matriks:


```r
# mengalikan masing-masing elemen matriks dengan 2
my_data*2
```

```
##      col1 col2 col3
## row1   10    4   14
## row2   12    8    6
## row3   14   10    8
## row4   16   18   16
## row5   18   16   14
```

```r
# memperoleh nilai log basis 2 pada masing-masing elemen matriks
log2(my_data)
```

```
##       col1  col2  col3
## row1 2.322 1.000 2.807
## row2 2.585 2.000 1.585
## row3 2.807 2.322 2.000
## row4 3.000 3.170 3.000
## row5 3.170 3.000 2.807
```

Seperti yang telah penulis jelaskan sebelumnya, kita juga dapat melakukan operasi matematika untuk memperoleh hasil penjumlahan elemen pada tiap baris atau kolom dengan menggunakan fungsi `rowSums()` untuk baris dan `colSums()` untuk kolom.


```r
# Total pada tiap kolom
colSums(my_data)
```

```
## col1 col2 col3 
##   35   28   29
```

```r
# Total pada tiap baris
rowSums(my_data)
```

```
## row1 row2 row3 row4 row5 
##   14   13   16   25   24
```

Jika kita tertarik untuk mencari nilai rata-rata tiap baris arau kolom kita juga dapat menggunakan fungsi `rowMeans()` atau `colMeans()`. Berikut adalah contoh penerapannya:


```r
# Rata-rata tiap baris
rowMeans(my_data)
```

```
##  row1  row2  row3  row4  row5 
## 4.667 4.333 5.333 8.333 8.000
```

```r
# Rata-rata tiap kolom
colMeans(my_data)
```

```
## col1 col2 col3 
##  7.0  5.6  5.8
```

Kita juga dapat melakukan perhitungan statistika lainnya menggunakan fungsi `apply()`. Berikut adalah format sederhananya:




```r
apply(x, MARGIN, FUN)
```

> **Note: **
>
> * x : data matriks
> * MARGIN : Nilai yang dapat digunakan adalah 1 (untuk operasi pada baris) dan 2 (untuk operasi pada kolom)
> * FUN : fungsi yang diterapkan pada baris atau kolom

untuk mengetahui fungsi (`FUN`) apa saja yang dapat diterapkan pada fungsi `apply()` jalankan sintaks bantuan berikut:


```r
help(apply)
```

Berikut adalah contoh penerapannya:


```r
# Rata-rata pada tiap baris
apply(my_data, 1, mean)
```

```
##  row1  row2  row3  row4  row5 
## 4.667 4.333 5.333 8.333 8.000
```

```r
# Median pada tiap kolom
apply(my_data, 2, median)
```

```
## col1 col2 col3 
##    7    5    7
```

## Faktor

Dalam bahasa `R` , faktor merupakan verktor dengan level. Level disimpan sebagai `R` Character. Jika kita menggunakan SPSS maka factor ini akan sama dengan jenis data numerik atau ordinal.

Faktor merepresentasikan kategori atau grup pada data. Untuk membuat faktor pada `R`, kita dapat menggunakan fungsi `factor()`.

### Membuat Variabel Faktor

Berikut adalah contoh sintaks pembuatan variabel faktor.


```r
# membuat variabel faktor
faktor <- factor(c(1,2,1,2))
faktor
```

```
## [1] 1 2 1 2
## Levels: 1 2
```

Pada sintaks tersebut objek faktor terdiri atas dua buah kategori atau pada `R` disebut sebagai **factor levels**. Kita dapat mengecek factor levels menggunakan fungsi `levels()`.


```r
levels(faktor)
```

```
## [1] "1" "2"
```

Kita juga dapat memberikan label atau mengubah level pada faktor. Berikut adalah contoh bagaimana kita melakukannya:


```r
# Ubah level
levels(faktor) <- c("baik","tidak_baik")
faktor
```

```
## [1] baik       tidak_baik baik       tidak_baik
## Levels: baik tidak_baik
```

```r
# Ubah urutan level
faktor <- factor(faktor,
                 levels = c("tidak_baik","baik"))
faktor
```

```
## [1] baik       tidak_baik baik       tidak_baik
## Levels: tidak_baik baik
```

> **Note: **
>
> * Fungsi `is.factor()` dapat digunakan untuk mengecek apakah sebuah variabel adalah faktor. Hasil yang dimunculkan dapat berupa TRUE (jika faktor) atau FALSE (jika bukan)
> * Fungsi `as.factor()` dapat digunakan untuk merubah sebuah variabel menjadi faktor.


```r
# Cek jika objek faktor adalah faktor
is.factor(faktor)
```

```
## [1] TRUE
```

```r
# Cek jika objek Jumlah adalah faktor
is.factor(Jumlah)
```

```
## [1] FALSE
```

```r
# Ubah objek Jumlah menjadi faktor
as.factor(Jumlah)
```

```
##     Apel    Jeruk Rambutan    Salak 
##        5     <NA>        6        7 
## Levels: 5 6 7
```

### Perhitungan Menggunakan Faktor

Jika kita ingin mengetahui jumlah masing-masing observasi pada masing-masing faktor, kita dapat menggunakan fungsi `summary()`. Berikut adalah contoh penerapannya:


```r
summary(faktor)
```

```
## tidak_baik       baik 
##          2          2
```

Pada contoh perhitungan menggunakan vektor kita telah membuat objek `pendapatan`. Pada objek tersebut kita ingin menghitung nilai rata-rata pendapatan berdasarkan objek faktor. Untuk melakukannya kita dapat menggunakan fungsi `tapply()`.


```r
pendapatan
```

```
## Andi Joni Lina Rani 
## 2000 1800 2500 3000
```

```r
faktor
```

```
## [1] baik       tidak_baik baik       tidak_baik
## Levels: tidak_baik baik
```

```r
# Rata-rata pendapatan dan simpan sebagai objek dengan nama:
# mean_pendapatan
mean_pendapatan <- tapply(pendapatan, faktor, mean)
mean_pendapatan
```

```
## tidak_baik       baik 
##       2400       2250
```

```r
# Hitung ukuran/panjang masing-masing grup
tapply(pendapatan, faktor, length)
```

```
## tidak_baik       baik 
##          2          2
```

Untuk mengetahui jumlah masing-masing observasi masing-masing factor levels kita juga dapat menggunakan fungsi `table()`. Fungsi tersebut akan membuat frekuensi tabel pada masing-masing factor levels atau yang dikenal sebagai *contingency table*.


```r
table(faktor)
```

```
## faktor
## tidak_baik       baik 
##          2          2
```

```r
# Cross-tabulation antara
# faktor dan pendapatan
table(pendapatan, faktor)
```

```
##           faktor
## pendapatan tidak_baik baik
##       1800          1    0
##       2000          0    1
##       2500          0    1
##       3000          1    0
```

## Data Frames

Data frame merupakan kumpulan vektor dengan panjang sama atau dapat pula dikatan sebagai matriks yang memiliki kolom dengan jenis data yang berbeda-beda (numerik, karakter, logical). Pada data frame terdapat baris dan kolom. Baris disebut sebagai observasi, sedangkan kolom disebut sebagai variabel. Sehingga dapat dikatakan bahwa setiap observasi akan memiliki satu atau beberapa variabel.

### Membuat Data Frame

Data frame dapat dibuat menggunakan fungsi `data.frame()`. Berikut adalah contoh cara membuat data frame:


```r
# Membuat data frame
nama <- c("Andi","Rizal","Ani","Ina")
pendapatan <- c(1000, 2000, 3500, 500)
tinggi <- c(160, 155, 170, 146)
usia <- c(35, 40, 25, 27)
menikah <- c(TRUE, FALSE, TRUE, TRUE)

data_teman <- data.frame(nama = nama,
                         gaji = pendapatan,
                         tinggi = tinggi,
                         menikah = menikah)

data_teman
```

```
##    nama gaji tinggi menikah
## 1  Andi 1000    160    TRUE
## 2 Rizal 2000    155   FALSE
## 3   Ani 3500    170    TRUE
## 4   Ina  500    146    TRUE
```

Untuk mengecek apakah objek `data_teman` merupakan data frame, kita dapat menggunakan fungsi `is.data.frame()`. Jika hasilnya TRUE, maka objek tersebut adalah data frame. Berikut adalah contoh penerapannya:


```r
is.data.frame(data_teman)
```

```
## [1] TRUE
```

> **Note: ** untuk konversi objek menjadi data frame, kita dapat menjalankan fungsi `as.data.frame()`.

### Subset Pada Data Frame

Subset pada data frame sebenarnya tidak berbeda dengan subset pada matriks. Bedanya adalah kita juga bisa melakukan subset langsung terhadap nama variabel menggunakan dollar sign. Untuk lebih memahaminya berikut adalah jenis subset pada data frame.

* **Pengindeksan positif** menggunakan nama dan lokasi.


```r
# Subset menggunakan dollar sign
data_teman$nama
```

```
## [1] Andi  Rizal Ani   Ina  
## Levels: Andi Ani Ina Rizal
```

```r
# atau 
data_teman[, "nama"]
```

```
## [1] Andi  Rizal Ani   Ina  
## Levels: Andi Ani Ina Rizal
```

```r
# subset baris 1 sampai 3 serta kolom 1 dan 3
data_teman[1:3, c(1,3)]
```

```
##    nama tinggi
## 1  Andi    160
## 2 Rizal    155
## 3   Ani    170
```

* **Pengindeksan negatif**


```r
# Kecualikan kolom nama
data_teman[,-1]
```

```
##   gaji tinggi menikah
## 1 1000    160    TRUE
## 2 2000    155   FALSE
## 3 3500    170    TRUE
## 4  500    146    TRUE
```

* **Pengideksan berdasarkan karakteristik**

Kita ingin memilih data dengan kriteria teman yang telah menikah


```r
data_teman[data_teman$menikah==TRUE, ]
```

```
##   nama gaji tinggi menikah
## 1 Andi 1000    160    TRUE
## 3  Ani 3500    170    TRUE
## 4  Ina  500    146    TRUE
```

```r
# Tampilkan hanya kolom nama dan gaji untuk yang telah menikah
data_teman[data_teman$menikah==TRUE, 1:2]
```

```
##   nama gaji
## 1 Andi 1000
## 3  Ani 3500
## 4  Ina  500
```

kita juga dapat menggunakan fungsi `subset()` agar lebih mudah. Berikut adalah contoh penerapannya:

```r
# subset terhadap teman yang berusia >=30 tahun
subset(data_teman, usia>=30)
```

```
##    nama gaji tinggi menikah
## 1  Andi 1000    160    TRUE
## 2 Rizal 2000    155   FALSE
```

Opsi lain adalah menggunakan fungsi `attach()` dan `detach()`. Fungsi `attach()` mengambil data frame dan membuat kolomnya dapat diakses hanya dengan memberikan nama mereka.


```r
# attach data frame
attach(data_teman)
```

```
## The following objects are masked _by_ .GlobalEnv:
## 
##     menikah, nama, tinggi
```

```r
# ==== memulai data manipulation ====
data_teman[usia>=30]
```

```
##    nama gaji
## 1  Andi 1000
## 2 Rizal 2000
## 3   Ani 3500
## 4   Ina  500
```

```r
# ==== mengakhiri data manipulation ====
# detach data frame

detach(data_teman)
```

### Memperluas Data Frame

Kita dapat juga memperluas data frame dengan cara menambahkan variabel atau kolombaru pada data frame. Pada contoh kali ini penulis akan menambahkan kolom pendidikan terakhir pada objek `data_teman`. Berikut adalah sintaks yang digunakan.


```r
# membuat vektor pendidikan
pendidikan <- c("S1","S2","D3","D1")

# menambahkan variabel pendidikan pada data frame
data_teman$pendidikan <- pendidikan
```


```r
# atau
cbind(data_teman, pendidikan=pendidikan)
```


### Perhitungan Pada Data Frame

Perhitungan pada variabel numerik data frame pada dasarnya sama dengan perhitungan pada matriks. kita dapat menggunakan fungsi `rowSums()`, `colSums()`, `rowMeans()` dan `apply()`. Proses perhitungan dan manipulasi pada data frame akan dibahas pada sesi yang lain secara lebih detail.

## List

List adalah kumpulan objek yang diurutkan, yang dapat berupa vektor, matriks, data frame, dll. Dengan kata lain, daftar dapat berisi semua jenis objek `R`.

### Membuat List

List dapat dibuat menggunakan fungsi `list()`. Berikut disajikan contoh sebuah list sebuah keluarga:


```r
# Membuat list keluarga
keluarga <- list(
  ayah = "Budi",
  usia_ayah = 48,
  ibu  = "Ani",
  usia_ibu = "47",
  anak = c("Andi", "Adi"),
  usia_anak = c(15,10)
  )

# Print
keluarga
```

```
## $ayah
## [1] "Budi"
## 
## $usia_ayah
## [1] 48
## 
## $ibu
## [1] "Ani"
## 
## $usia_ibu
## [1] "47"
## 
## $anak
## [1] "Andi" "Adi" 
## 
## $usia_anak
## [1] 15 10
```

```r
# Nama elemen dalam list
names(keluarga)
```

```
## [1] "ayah"      "usia_ayah" "ibu"       "usia_ibu" 
## [5] "anak"      "usia_anak"
```

```r
# Jumlah elemen pada list
length(keluarga)
```

```
## [1] 6
```

### Subset List

Kita dapat memilih sebuah elemen pada list dengan menggunakan nama elemen atau indeks dari elemen tersebut. Berikut adalah contoh penerapannya:


```r
# Subset berdasarkan nama
# mengambil elemen usia_ayah
keluarga$usia_ayah
```

```
## [1] 48
```

```r
# Atau
keluarga[["usia_ayah"]]
```

```
## [1] 48
```

```r
# Subset berdasarkan indeks
keluarga[[2]]
```

```
## [1] 48
```

```r
# subset elemen pertama pada keluarga[[5]]
keluarga[[5]][1]
```

```
## [1] "Andi"
```

### Memperluas List

Kita juga dapat menambahkan elemen pada list yang telah kita buat. Pada contoh list sebelumnya penulis akan menambahkan elemen keluarga yang lain seperti berikut:


```r
# Menambahkan kakek dan nenek pada list
keluarga$kakek <- "Suprapto"
keluarga$nenek <- "Sri"

# Print
keluarga
```

```
## $ayah
## [1] "Budi"
## 
## $usia_ayah
## [1] 48
## 
## $ibu
## [1] "Ani"
## 
## $usia_ibu
## [1] "47"
## 
## $anak
## [1] "Andi" "Adi" 
## 
## $usia_anak
## [1] 15 10
## 
## $kakek
## [1] "Suprapto"
## 
## $nenek
## [1] "Sri"
```

Kita juga dapat menggabungkan beberapa list menjadi satu. Berikut adalah format sederhana bagaimana cara menggabungkan beberapa list menjadi satu:


```r
list_baru <- c(list_a, list_b, list_c, ...)
```

## Loop

*Loop* merupakan kode program yang berulang-ulang. *Loop* berguna saat kita ingin melakukan sebuah perintah yang perlu dijalankan berulang-ulang seperti melakukan perhitungan maupaun melakukan visualisasi terhadap banyak variabel secara serentak. Hal ini tentu saja membantu kita karena kita tidak perlu menulis sejumlah sintaks yang berulang-ulang. Kita hanya perlu mengatur *statement* berdasarkan hasil yang kita harapkan.

Pada `R` bentuk *loop* dapat bermacam-macam ("*for loop*","*while loop*", dll). `R` menyederhanakan bentuk *loop* ini dengan menyediakan sejumlah fungsi seperti `apply()`,`tapply()`, dll. Sehingga `loop` jarang sekali muncul dalam kode `R`. Sehingga `R` sering disebut sebagai *loopless loop*. 

Meski *loop* jarang muncul bukan berarti kita tidak akan melakukannya. Terkadang saat kita melakukan komputasi statistik atau matematik dan belum terdapat paket yang mendukung proses tersebut, sering kali kita akan membuat sintaks sendiri berdasarkan algoritma metode tersebut. Pada algoritma tersebut sering pula terdapat *loop* yang diperlukan selama proses perhitungan. Secara sederhana diagram umum loop ditampilkan pada Gambar \@ref(fig:loop)

\begin{figure}

{\centering \includegraphics[width=0.4\linewidth]{skema_loop} 

}

\caption{Diagram umum loop (sumber: Primartha, 2018).}(\#fig:loop)
\end{figure}

### For Loop

Mengulangi sebuah *statement* atau sekelompok *statement* sebanyak nilai yang ditentukan di awal. Jadi operasi akan terus dilakukan sampai dengan jumlah yang telah ditetapkan di awal atau dengan kata lain tes kondisi (Jika jumlah pengulangan telah cukup) hanya akan dilakukan di akhir. Secara sederhana bentuk dari *for loop* dapat dituliskan sebagai berikut:


```r
for (value in vector){
  statements
}
```


Berikut adalah contoh sintaks penerapan *for loop*:


```r
# Membuat vektor numerik
vektor <- c(1:5)

# loop 
for(i in vektor){
  print(i)
}
```

```
## [1] 1
## [1] 2
## [1] 3
## [1] 4
## [1] 5
```

*Loop* akan dimulai dari blok *statement for* sampai dengan  `print(i)`. Berdasarkan *loop* pada contoh tersebut, *loop* hanya dilakukan sebanyak 5 kali sesuai dengan jumlah vektor yang ada.

### While Loop

*While loop* merupakan loop yang digunakan ketika kita telah menetapkan *stop condition* sebelumnya. Blok *statement*/kode yang sama akan terus dijalankan sampai *stop condition* ini tercapai. *Stop condition* akan di cek sebelum melakukan proses *loop*. Berikut adalah pola dari *while loop* dapat dituliskan sebagai berikut:


```r
while (test_expression){
  statement
}
```

Berikut adalah contoh penerapan dari *while loop*:


```r
coba <- c("Contoh")
counter <- 1

# loop
while (counter<5){
  # print vektor
  print(coba)
  # tambahkan nilai counter sehingga proses terus berlangsung sampai counter = 5 
  counter <- counter + 1
}
```

```
## [1] "Contoh"
## [1] "Contoh"
## [1] "Contoh"
## [1] "Contoh"
```

*Loop* akan dimulai dari blok *statement while* sampai dengan *counter* <- 1. *Loop* hanya akan dilakukan sepanjang nilai *counter* < 5. 

### Repeat Loop

*Repeat loop* akan menjalankan *statement*/kode yang sama berulang-ulang hingga *stop condition* tercapai. Berikut adalah pola dari *repeat loop*.


```r
repeat {
  commands
  if(condition){
    break
  }
}
```

Berikut adalah contoh penerapan dari *repeat loop*:


```r
coba <- c("contoh")
counter <- 1
repeat {
  print(coba)
  counter <- counter + 1
  if(counter < 5){
break
  }
}
```

```
## [1] "contoh"
```

*Loop* akan dimulai dari blok *statement while* sampai dengan *break*. *Loop* hanya akan dilakukan sepanjang nilai *counter* < 5. Hasil yang diperoleh berbeda dengan *while loop*, dimana kita memperoleh 4 buah kata "contoh". Hal ini disebabkan karena *repeat loop* melakukan pengecekan *stop condition* tidak di awal loop seperti *while loop* sehingga berapapun nilainya, selama nilainya sesuai dengan *stop condition* maka *loop* akan dihentikan. Hal ini berbeda dengan *while loop* dimana proses dilakukan berulang-ulang sampai jumlahnya mendekati *stop condition*.

### Break

*Break* sebenarnya bukan bagian dari *loop*, namun sering digunakan dalam *loop*. *Break* dapat digunakan pada *loop* manakala dirasa perlu, yaitu saat kondisi yang disyaratkan pada *break* tercapai.

Berikut adalah contoh penerapan *break* pada beberapa jenis *loop*.


```r
# for loop
a = c(2,4,6,8,10,12,14)
for(i in a){
  if(i>8){
    break
  }
  print(i)
}
```

```
## [1] 2
## [1] 4
## [1] 6
## [1] 8
```

```r
# while loop
a = 2
b = 4
while(a<7){
  print(a)
  a = a +1
  if(b+a>10){
    break
  }
}
```

```
## [1] 2
## [1] 3
## [1] 4
## [1] 5
## [1] 6
```

```r
# repeat loop
a = 1
repeat{
  print(a)
  a = a+1
  if(a>6){
    break
  }
}
```

```
## [1] 1
## [1] 2
## [1] 3
## [1] 4
## [1] 5
## [1] 6
```

## Loop Menggunakan Apply Family Function

Penggunaan loop sangat membantu kita dalam melakukan proses perhitungan berulang. Namun, metode ini tidak cukup ringkas dalam penerapannya dan perlu penulisan sintaks yang cukup panjang untuk menyelesaikan sebuah kasus yang kita inginkan. Berikut adalah sebuah sintaks yang digunakan untuk menghitung nilai mean pada suatu dataset:


```r
# subset data iris
sub_iris <- iris[,-5]
# membuat vektor untuk menyimpan hasil loop
a <- rep(NA,4)
# loop
for(i in 1:length(sub_iris)){
  a[i]<-mean(sub_iris[,i])
}
# print
a
```

```
## [1] 5.843 3.057 3.758 1.199
```

```r
class(a) # cek kelas objek
```

```
## [1] "numeric"
```

Metode alternatif lain untuk melakukan loop suatu fungsi adalah dengan menggunakan Apply function family. Metode ini memungkinkan kita untuk melakukan loop suatu fungsi tanpa perlu menuliskan sintaks loop. Berikut adalah beberapa fungsi dari apply family yang nantinya akan sering kita gunakan:

- `apply()`: fungsi generik yang mengaplikasikan fungsi kepada kolom atau baris pada matriks atau secara lebih general aplikasi dilakukan pada dimensi untuk jenis data array.
- `lapply()`: fungsi apply yang bekerja pada jenis data list dan memberikan output berupa list juga.
- `sapply()`: bentuk sederhana dari lapply yang menghasilkan output berupa matriks atau vektor.
- `vapply()`: disebut juga *verified apply* (memungkinkan untuk menghasilkan output dengan jenis data yang telah ditentukan sebelumnya).
- `tapply()`: *tagged apply* dimana dimana tag menentukan subset dari data.

### Apply

Fungsi `apply()` bekerja dengan jenis data matrik atau array (jenis data homogen). Kita dapat melakukan spesifikasi apakah suatu fungsi hanya akan bekerja pada kolom saja, baris saja atau keduanya. Format fungsi ini adalah sebagai berikut:


```r
apply(X, MARGIN, FUN, ...)
```

> **Note: **
>
> - **X**: matriks atau array
> - **MARGIN**: menentukan bagaimana fungsi bekerja terhadap matriks atau array. Jika nilai yang diinputkan 1, maka fungsi akan bekerja pada masing-masing baris pada matriks. Jika nilainya 2, maka fungsi akan bekerja pada tiap kolom pada matriks.
> - **FUN**: fungsi yang akan digunakan. Fungsi yang dapat digunakan dapat berupa fungsi dasar matematika atau statistika, serta user define function.
> - **...**: opsional argumen pada fungsi yang digunakan.

Berikut adalah contoh bagaimana aplikasi fungsi tersebut pada matriks:


```r
## membuat matriks
x <- cbind(x1 = 3, x2 = c(4:1, 2:5))
x # print
```

```
##      x1 x2
## [1,]  3  4
## [2,]  3  3
## [3,]  3  2
## [4,]  3  1
## [5,]  3  2
## [6,]  3  3
## [7,]  3  4
## [8,]  3  5
```

```r
class(x) # cek kelas objek
```

```
## [1] "matrix"
```

```r
## menghitung mean masing-masing kolom
apply(x, MARGIN=2 ,FUN=mean, trim=0.2, na.rm=TRUE)
```

```
## x1 x2 
##  3  3
```

```r
## menghitung range nilai pada masing-masing baris
## menggunakan user define function
apply(x, MARGIN=1,
      FUN=function(x){
        max(x)-min(x)
      })
```

```
## [1] 1 0 1 2 1 0 1 2
```

### lapply

Fungsi ini melakukan loop fungsi terhadap input data berupa list. Output yang dihasilkan juga merupakan list dengan panjang list yang sama dengan yang diinputkan. Format yang digunakan adalah sebagai berikut:


```r
lapply(X, FUN, ...)
```

> **Note: **
>
> - **X**: vektor, data frame atau list
> - **FUN**: fungsi yang akan digunakan. Fungsi yang dapat digunakan dapat berupa fungsi dasar matematika atau statistika, serta user define function. Subset juga dimungkinkan pada fungsi ini.
> - **...**: opsional argumen pada fungsi yang digunakan.

Berikut adalah contoh penerapan fungsi lapply:


```r
## Membuat list
x <- list(a = 1:10, beta = exp(-3:3), logic = c(TRUE,FALSE,FALSE,TRUE))
x # print
```

```
## $a
##  [1]  1  2  3  4  5  6  7  8  9 10
## 
## $beta
## [1]  0.04979  0.13534  0.36788  1.00000  2.71828
## [6]  7.38906 20.08554
## 
## $logic
## [1]  TRUE FALSE FALSE  TRUE
```

```r
class(x) # cek kelas objek
```

```
## [1] "list"
```

```r
## Menghitung nilai mean pada masing-masing baris lits
lapply(x, FUN=mean)
```

```
## $a
## [1] 5.5
## 
## $beta
## [1] 4.535
## 
## $logic
## [1] 0.5
```

```r
## Menghitung mean tiap kolom dataset iris
lapply(iris, FUN=mean)
```

```
## Warning in mean.default(X[[i]], ...): argument is not
## numeric or logical: returning NA
```

```
## $Sepal.Length
## [1] 5.843
## 
## $Sepal.Width
## [1] 3.057
## 
## $Petal.Length
## [1] 3.758
## 
## $Petal.Width
## [1] 1.199
## 
## $Species
## [1] NA
```

```r
## Mengalikan elemen vektor dengan suatu nilai
y <- c(1:5)
lapply(y, FUN=function(x){x*5})
```

```
## [[1]]
## [1] 5
## 
## [[2]]
## [1] 10
## 
## [[3]]
## [1] 15
## 
## [[4]]
## [1] 20
## 
## [[5]]
## [1] 25
```

```r
## Mengubah output menjadi vektor
unlist(lapply(y, FUN=function(x){x*5}))
```

```
## [1]  5 10 15 20 25
```

### sapply

Fungsi `sapply()` merupakan bentuk lain dari fungsi `lapply()`. Perbedaanya terletak pada output default yang dihasilkan. Secara default `sapply()` menerima input utama berupa list (dapat pula dataframe atau vektor), namun tidak seperti `lapply()` jenis data output yang dihasilkan adalah vektor. Untuk mengubah output menjadi list perlu argumen tambahan berupa `simplify=FALSE`. Format fungsi tersebut adalah sebagai berikut:


```r
sapply(X, FUN, ..., simplify = TRUE, USE.NAMES = TRUE)
```

> **Note: **
>
> - **X**: vektor, data frame atau list
> - **FUN**: fungsi yang akan digunakan. Fungsi yang dapat digunakan dapat berupa fungsi dasar matematika atau statistika, serta user define function. Subset juga dimungkinkan pada fungsi ini.
> - **...**: opsional argumen pada fungsi yang digunakan.
> - **simplify**: logical. Jika nilainya TRUE maka output yang dihasilkan adalah bentuk sederhana dari vektor, matrix atau array.
> - **USE.NAMES**: jika list memiliki nama pada setiap elemennya, maka nama elemen tersebut akan secara default ditampilkan.

Berikut adalah contoh penerapannya:


```r
## membuat list
x <- list(a = 1:10, beta = exp(-3:3), logic = c(TRUE,FALSE,FALSE,TRUE))

## menghitung nilai mean setiap elemen
sapply(x, FUN=mean)
```

```
##     a  beta logic 
## 5.500 4.535 0.500
```

```r
## menghitung nilai mean dengan output list
sapply(x, FUN=mean, simplify=FALSE)
```

```
## $a
## [1] 5.5
## 
## $beta
## [1] 4.535
## 
## $logic
## [1] 0.5
```

```r
## summary objek dataframe
sapply(mtcars, FUN=summary)
```

```
##           mpg   cyl  disp    hp  drat    wt  qsec
## Min.    10.40 4.000  71.1  52.0 2.760 1.513 14.50
## 1st Qu. 15.43 4.000 120.8  96.5 3.080 2.581 16.89
## Median  19.20 6.000 196.3 123.0 3.695 3.325 17.71
## Mean    20.09 6.188 230.7 146.7 3.597 3.217 17.85
## 3rd Qu. 22.80 8.000 326.0 180.0 3.920 3.610 18.90
## Max.    33.90 8.000 472.0 335.0 4.930 5.424 22.90
##             vs     am  gear  carb
## Min.    0.0000 0.0000 3.000 1.000
## 1st Qu. 0.0000 0.0000 3.000 2.000
## Median  0.0000 0.0000 4.000 2.000
## Mean    0.4375 0.4062 3.688 2.812
## 3rd Qu. 1.0000 1.0000 4.000 4.000
## Max.    1.0000 1.0000 5.000 8.000
```

```r
## summary objek list
a <- list(mobil=mtcars, anggrek=iris)
sapply(a, FUN=summary)
```

```
## $mobil
##       mpg            cyl            disp      
##  Min.   :10.4   Min.   :4.00   Min.   : 71.1  
##  1st Qu.:15.4   1st Qu.:4.00   1st Qu.:120.8  
##  Median :19.2   Median :6.00   Median :196.3  
##  Mean   :20.1   Mean   :6.19   Mean   :230.7  
##  3rd Qu.:22.8   3rd Qu.:8.00   3rd Qu.:326.0  
##  Max.   :33.9   Max.   :8.00   Max.   :472.0  
##        hp             drat            wt      
##  Min.   : 52.0   Min.   :2.76   Min.   :1.51  
##  1st Qu.: 96.5   1st Qu.:3.08   1st Qu.:2.58  
##  Median :123.0   Median :3.69   Median :3.33  
##  Mean   :146.7   Mean   :3.60   Mean   :3.22  
##  3rd Qu.:180.0   3rd Qu.:3.92   3rd Qu.:3.61  
##  Max.   :335.0   Max.   :4.93   Max.   :5.42  
##       qsec            vs              am       
##  Min.   :14.5   Min.   :0.000   Min.   :0.000  
##  1st Qu.:16.9   1st Qu.:0.000   1st Qu.:0.000  
##  Median :17.7   Median :0.000   Median :0.000  
##  Mean   :17.8   Mean   :0.438   Mean   :0.406  
##  3rd Qu.:18.9   3rd Qu.:1.000   3rd Qu.:1.000  
##  Max.   :22.9   Max.   :1.000   Max.   :1.000  
##       gear           carb     
##  Min.   :3.00   Min.   :1.00  
##  1st Qu.:3.00   1st Qu.:2.00  
##  Median :4.00   Median :2.00  
##  Mean   :3.69   Mean   :2.81  
##  3rd Qu.:4.00   3rd Qu.:4.00  
##  Max.   :5.00   Max.   :8.00  
## 
## $anggrek
##   Sepal.Length   Sepal.Width    Petal.Length 
##  Min.   :4.30   Min.   :2.00   Min.   :1.00  
##  1st Qu.:5.10   1st Qu.:2.80   1st Qu.:1.60  
##  Median :5.80   Median :3.00   Median :4.35  
##  Mean   :5.84   Mean   :3.06   Mean   :3.76  
##  3rd Qu.:6.40   3rd Qu.:3.30   3rd Qu.:5.10  
##  Max.   :7.90   Max.   :4.40   Max.   :6.90  
##   Petal.Width        Species  
##  Min.   :0.1   setosa    :50  
##  1st Qu.:0.3   versicolor:50  
##  Median :1.3   virginica :50  
##  Mean   :1.2                  
##  3rd Qu.:1.8                  
##  Max.   :2.5
```

### vapply

Funsgi ini merupakan bentuk lain dari `sapply()`. Bedanya secara kecepatan proses fungsi ini lebih cepat dari `sapply()`. Hal yang menarik dari fungsi ini kita dapat menambahkan argumen `FUN.VALUE`. pada argumen ini kita memasukkan vektor berupa output fungsi yang diinginkan. Perbedaan lainnya adalah output yang dihasilkan hanya berupa matriks atau array. Format dari fungsi ini adalah sebagai berikut:


```r
vapply(X, FUN, FUN.VALUE, ..., USE.NAMES = TRUE)
```

> **Note: **
>
> - **X**: vektor, data frame atau list
> - **FUN**: fungsi yang akan digunakan. Fungsi yang dapat digunakan dapat berupa fungsi dasar matematika atau statistika, serta user define function. Subset juga dimungkinkan pada fungsi ini.
> - **FUN.VALUE**: vektor, template dari return value FUN.
> - **...**: opsional argumen pada fungsi yang digunakan.
> - **USE.NAMES**: jika list memiliki nama pada setiap elemennya, maka nama elemen tersebut akan secara default ditampilkan.

Berikut adalah contoh penerapannya:


```r
## membuat list
x <- sapply(3:9, seq)
x # print
```

```
## [[1]]
## [1] 1 2 3
## 
## [[2]]
## [1] 1 2 3 4
## 
## [[3]]
## [1] 1 2 3 4 5
## 
## [[4]]
## [1] 1 2 3 4 5 6
## 
## [[5]]
## [1] 1 2 3 4 5 6 7
## 
## [[6]]
## [1] 1 2 3 4 5 6 7 8
## 
## [[7]]
## [1] 1 2 3 4 5 6 7 8 9
```

```r
## membuat ringkasan data pada tiap elemen list
vapply(x, fivenum,
       c(Min. = 0, "1st Qu." = 0, 
         Median = 0, "3rd Qu." = 0, Max. = 0))
```

```
##         [,1] [,2] [,3] [,4] [,5] [,6] [,7]
## Min.     1.0  1.0    1  1.0  1.0  1.0    1
## 1st Qu.  1.5  1.5    2  2.0  2.5  2.5    3
## Median   2.0  2.5    3  3.5  4.0  4.5    5
## 3rd Qu.  2.5  3.5    4  5.0  5.5  6.5    7
## Max.     3.0  4.0    5  6.0  7.0  8.0    9
```

```r
## membuat ringkasan data pada tiap kolom dataframe
vapply(mtcars, summary,
       c(Min. = 0, "1st Qu." = 0, 
         Median = 0, "3rd Qu." = 0, Max. = 0, Mean=0))
```

```
##           mpg   cyl  disp    hp  drat    wt  qsec
## Min.    10.40 4.000  71.1  52.0 2.760 1.513 14.50
## 1st Qu. 15.43 4.000 120.8  96.5 3.080 2.581 16.89
## Median  19.20 6.000 196.3 123.0 3.695 3.325 17.71
## 3rd Qu. 20.09 6.188 230.7 146.7 3.597 3.217 17.85
## Max.    22.80 8.000 326.0 180.0 3.920 3.610 18.90
## Mean    33.90 8.000 472.0 335.0 4.930 5.424 22.90
##             vs     am  gear  carb
## Min.    0.0000 0.0000 3.000 1.000
## 1st Qu. 0.0000 0.0000 3.000 2.000
## Median  0.0000 0.0000 4.000 2.000
## 3rd Qu. 0.4375 0.4062 3.688 2.812
## Max.    1.0000 1.0000 4.000 4.000
## Mean    1.0000 1.0000 5.000 8.000
```

### tapply

Fungsi ini sangat berguna jika pembaca ingin menghitung suatu nilai misalnya mean berdasarkan grup data atau factor. Format fungsi ini adalah sebagi berikut:


```r
tapply(X, INDEX, FUN = NULL, ..., simplify = TRUE)
```

> **Note: **
>
> - **X**: vektor, data frame atau list
> - **INDEX**: list satu atau beberapa factor yang memiliki panjang sama dengan X.
> - **FUN**: fungsi yang akan digunakan. Fungsi yang dapat digunakan dapat berupa fungsi dasar matematika atau statistika, serta user define function. Subset juga dimungkinkan pada fungsi ini.
> - **...**: opsional argumen pada fungsi yang digunakan.
> - **simplify**: logical. Jika nilainya TRUE maka output yang dihasilkan adalah bentuk skalar.

Berikut adalah contoh penerapannya:


```r
## membuat tabel frekuensi
groups <- as.factor(rbinom(32, n = 5, prob = 0.4))

tapply(groups, groups, length)
```

```
##  7  9 11 15 
##  1  1  1  2
```

```r
# atau
table(groups)
```

```
## groups
##  7  9 11 15 
##  1  1  1  2
```

```r
## membuat tabel kontingensi
# menghitung jumlah breaks berdasarkan faktor jenis wool
# dan tensi level
tapply(X=warpbreaks$breaks, INDEX=warpbreaks[,-1], FUN=sum)
```

```
##     tension
## wool   L   M   H
##    A 401 216 221
##    B 254 259 169
```

```r
# menghitung mean panjang gigi babi hutan berdasarkan
# jenis suplemen dan dosisnya
tapply(ToothGrowth$len, ToothGrowth[,-1], mean)
```

```
##     dose
## supp   0.5     1     2
##   OJ 13.23 22.70 26.06
##   VC  7.98 16.77 26.14
```

```r
# menghitung mpg minimum berdasarkan jumlah silinder pada mobil
tapply(mtcars$mpg, mtcars$cyl, min, simplify=FALSE)
```

```
## $`4`
## [1] 21.4
## 
## $`6`
## [1] 17.8
## 
## $`8`
## [1] 10.4
```

## Loop Menggunakan map function pada Library `purrr`

Map function dari library `purrr` merupakan alternatif lain untuk melakukan looping selain dengan menggunakan for loop, while loop, atau apply family. Berbeda dengan metode tersebut, map function mempermudah proses kita dalam melakukan looping karena dapat diintegrasikan dengan fungsi-fungsi dari library `tidyverse` seperti `dplyr`, `tibble`, `tidyr`, dll, yang akan banyak penulis bahas pada Chapter selanjutnya. Selain itu, integrasi dengan library tersebut membuat setiap sintaks yang kita buat lebih mudah kita baca serta lebih cepat dalam prosesnya. 

Fungsi-fungsi yang tersedia berdasarkan jenis output yang kita inginkan. Berikut adalah fungsi-fungsi map family beserta output yang dihasilkan:

- `map()`: membuat output berupa list
- `map_lgl()`: membuat output berupa vektor logical
- `map_int()`: membuat output berupa vektor integer
- `map_dbl()`: membuat output berupa vektor double
- `map_chr()`: membuat output berupa vektor karakter

Berikut adalah format dari fungsi-fungsi tersebut:


```r
map(.x, .f, ...)

map_lgl(.x, .f, ...)

map_chr(.x, .f, ...)

map_int(.x, .f, ...)

map_dbl(.x, .f, ...)
```

> **Note: **
>
> - **.x**: list atau vaktor atomik.
> - **.f**: formula fungsi.
> - **...**: argumen tambahan dari fungsi.

Berikut adalah contoh dari penerapan fungsi-fungsi tersebut:


```r
library(purrr)
# list
map(.x=iris[,-5], .f=mean, na.rm=TRUE)
```

```
## $Sepal.Length
## [1] 5.843
## 
## $Sepal.Width
## [1] 3.057
## 
## $Petal.Length
## [1] 3.758
## 
## $Petal.Width
## [1] 1.199
```

```r
# vektor numerik
map_dbl(.x=iris[,-5], .f=mean, na.rm=TRUE)
```

```
## Sepal.Length  Sepal.Width Petal.Length  Petal.Width 
##        5.843        3.057        3.758        1.199
```

```r
# vektor integer
map_int(.x=iris[,-5], length)
```

```
## Sepal.Length  Sepal.Width Petal.Length  Petal.Width 
##          150          150          150          150
```

```r
# vektor logical
map_lgl(.x=iris, .f=is.double)
```

```
## Sepal.Length  Sepal.Width Petal.Length  Petal.Width 
##         TRUE         TRUE         TRUE         TRUE 
##      Species 
##        FALSE
```

```r
# vektor karakter
x <- c("Jakarta", "Bandung", "Surabaya")
map_chr(.x=x, .f=paste, "Kota")
```

```
## [1] "Jakarta Kota"  "Bandung Kota"  "Surabaya Kota"
```


## Decision Making

*Decicion Making* atau sering disebut sebagai *if then else statement* merupakan bentuk percabagan yang digunakan manakala kita ingin agar program dapat melakukan pengujian terhadap syarat kondisi tertentu. Pada Tabel \@ref(tab:percabangan) disajikan daftar percabangan yang digunakan pada `R`.

**Statement**          | **Keterangan**
-----------------------|--------------------------------------------------------------------------------------------------------------------------
*if statement*         | *if statement* hanya terdiri atas sebuah ekspresi *Boolean*, dan diikuti satu atau lebih *statement*
*if...else statement*  | *if else statement* terdiri atas beberapa buah ekspresi *Boolean*. Ekspressi *Boolean* berikutnya akan dijalankan jika ekspresi *Boolan  sebelumnya bernilai FALSE
*switch statement*     | *switch statement* digunakan untuk mengevaluasi sebuah variabel beberapa pilihan

: (\#tab:percabangan) Daftar percabangan pada `R`.

### if statement

Pola *if statement* disajikan pada Gambar \@ref(fig:ifstatement)

\begin{figure}

{\centering \includegraphics[width=0.4\linewidth]{ifstatement} 

}

\caption{Diagram if statement (sumber: Primartha, 2018).}(\#fig:ifstatement)
\end{figure}

Berikut adalah contoh penerapan *if statement*:


```r
x <- c(1:5)
if(is.vector(x)){
  print("x adalah sebuah vector")
}
```

```
## [1] "x adalah sebuah vector"
```


### if else statement

Pola dari *if else statement* disajikan pada Gambar \@ref(fig:ifelse)

\begin{figure}

{\centering \includegraphics[width=0.4\linewidth]{ifelse} 

}

\caption{Diagram if else statement (sumber: Primartha, 2018).}(\#fig:ifelse)
\end{figure}

Berikut adalah contoh penerapan *if else statement*:


```r
x <- c("Andi","Iwan", "Adi")
if("Rina" %in% x){
  print("Rina ditemukan")
} else if("Adi" %in% x){
  print("Adi ditemukan")
} else{
  print("tidak ada yang ditemukan")
}
```

```
## [1] "Adi ditemukan"
```


### switch statement

Pola dari *switch statement* disajikan pada Gambar \@ref(fig:switch)

\begin{figure}

{\centering \includegraphics[width=0.4\linewidth]{switch} 

}

\caption{Diagram switch statement (sumber: Primartha, 2018).}(\#fig:switch)
\end{figure}

Berikut adalah contoh penerapan *switch statement*:


```r
y = 3

x = switch(
  y,
  "Selamat Pagi",
  "Selamat Siang",
  "Selamat Sore",
  "Selamat Malam"
)

print(x)
```

```
## [1] "Selamat Sore"
```


## Fungsi

Fungsi merupakan sekumpulan instruksi atau *statement* yang dapat melakukan tugas khusus. Sebagai contoh fungsi perkalian untuk menyelesaikan operasi perkalian, fungsi pemangkatan hanya untuk operasi pemangkatan, dll.

Pada `R` terdapat 2 jenis fungsi, yaitu: *build in fuction* dan *user define function*. *build in fnction* merupakan fungsi bawaan `R` saat pertama kita menginstall `R`. Contohnya adalah `mean()`, `sum()`, `ls()`, `rm()`, dll. Sedangkan *user define fuction* merupakan fungsi-fungsi yang dibuat sendiri oleh pengguna.

Fungsi-fungsi buatan pengguna haruslah dideklarasikan (dibuat) terlebih dahulu sebelum dapat dijalankan. Pola pembentukan fungsi adalah sebagai berikut:


```r
function_name <- function(argument_1, argument_2, ...){
  function body
}
```

> **Note: **
>
> -  **function_name** : Nama dari fungsi `R`. `R` akan menyimpan fungsi tersebut sebagai objek
> -  **argument_1, argument_2,...** : *Argument* bersifat opsional (tidak wajib). *Argument* dapat digunakan untuk memberi inputan kepada fungsi
> -  **function body** : Merupakan inti dari fungsi. Fuction body dapat terdiri atas 0 statement (kosong) hingga banyak statement.
> -  **return** : Fungsi ada yang memiliki *output* atau *return value* ada juga yang tidak. Jika fungsi memiliki *return value* maka *return value* dapat diproses lebih lanjut

Berikut adalah contoh penerapan *user define function*:


```r
# Fungsi tanpa argument
bilang <- function(){
  print("Hello World!!")
}

# Print
bilang()
```

```
## [1] "Hello World!!"
```

```r
# Fungsi dengan argumen
tambah <- function(a,b){
  print(a+b)
}

# Print
tambah(5,3)
```

```
## [1] 8
```

```r
# Fungsi dengan return value
kali <- function(a,b){
  return(a*b)
}

# Print
kali(4,3)
```

```
## [1] 12
```


##Referensi

1. Primartha, R. 2018. **Belajar Machine Learning Teori dan Praktik**. Penerbit Informatika : Bandung.
2. Rosadi,D. 2016. **Analisis Statistika dengan R**. Gadjah Mada University Press: Yogyakarta.
3. STHDA. **Easy R Programming Basics**. <http://www.sthda.com/english/wiki/easy-r-programming-basics>
4. Venables, W.N. Smith D.M. and R Core Team. 2018. **An Introduction to R**. R Manuals.
5. The R Core Team. 2018. **R: A Language and Environment for Statistical Computing**. R Manuals.

<!--chapter:end:02-dasar-pemrograman-menggunakan-r.Rmd-->

<style>
body{
text-align: justify}
</style>

# Manajemen Data R

Data manajemen merupakan bagian penting dalam setiap proses analisa data. Proses import dan eksport data pada berbagai format penting untuk dipelajari. Selain itu, proses perapihan data sebelum analisa menjadi bagian yang harus ada pada awal proses analisa. Proses-proses tersebut akan kita ulas secara mendalam pada *chapter* ini.*Chapter* ini juga akan membahas bagaimana kita dapat melakukan sejumlah manipulasi data untuk memperoleh informasi lebih yang terkandung pada. 

Pada Chapter ini pembaca juga akan belajar bagaimana bekerja menggunakan `tidyverse`, sebuah paket yang berisi kumpulan library data science. Paket ini sangat berguna bagi pembaca khusunya pemula yang ingin bekerja dengan secara rapi dan mudah bersama `R`

## Tidyverse

`Tidyverse` merupakan kumpulan library yang dikhususkan bagi pengguna `R` yang ingin melakukan analisa data. Paket ini terdiri dari kumpulan berbagai library yang pada buku ini tidak akan dibahas seluruhnya. Library ini dari `tidyverse` antara lain:

1. **`ggplot2`**: library yang digunakan untuk membuat visualisasi data yang menarik yang didasarkan pada sistem *Grammar of Graphics*.
2. **`dplyr`**: berisi kumpulan fungsi yang digunakan untuk melakukan manipulasi pada data dengan nama fungsi dan output yang konsisten.
3. **`tidyr`**: library yang berisi kumpulan fungsi merapikan data atau membuat *pivot table* dari data.
4. **`readr`**: library yang berfungsi untuk membaca file format .csv, .txt, .tsv, dan .fwf.
5. **`purrr`**: library yang berguna untuk meningkatkan *fuctional programming* pada `R`. Fungsi ini telah penulis bahas secara garis besar pada Chapter 1.
6. **`tibble`**: library yang digunakan untuk mengubah dataframe menjadi format tibble (bentuk lain dataframe yang lebih konsisten).

Selain fungsi-fungsi tersebut, masih terdapat banyak fungsi lain yang ada seperti `stringr`, `forcats`, dll.

Untuk menginstall dan menjalankan library `tidyverse` jalankan sintaks berikut:


```r
install.packages("tidyverse")
```


```r
library(tidyverse)
```

```
## Registered S3 methods overwritten by 'ggplot2':
##   method         from 
##   [.quosures     rlang
##   c.quosures     rlang
##   print.quosures rlang
```

```
## -- Attaching packages ----------------------------------------------- tidyverse 1.2.1 --
```

```
## v ggplot2 3.1.1     v readr   1.3.1
## v tibble  2.1.3     v dplyr   0.8.1
## v tidyr   0.8.3     v stringr 1.4.0
## v ggplot2 3.1.1     v forcats 0.4.0
```

```
## -- Conflicts -------------------------------------------------- tidyverse_conflicts() --
## x dplyr::filter() masks stats::filter()
## x dplyr::lag()    masks stats::lag()
```

## Import File

Pada sesi bagian ini penulis akan menjelaskan cara mengimport file pada `R`. File yang diimport ke dalam `R` terdiri atas file yang sering digunakan pada saat akan melakukan analisis data, antara lain: TXT, CSv, Excel, SPSS, SAS, dan STATA.

Pada bagian ini akan dijelaskan pula bagaimana melakukan import data menggunakan library `readr` serta kelebihan dari metode import data yang digunakan. Berikut adalah cara mengimport data berbagai format pada `R`.

> **Note: ** Pastikan kita telah mengatur lokasi *working directory* pada tempat dimana lokasi file yang akan kita baca berada untuk mempermudah dalam melakukan import file.

### Import File Menggunakan Fungsi Bawaan R

Fungsi bawaan `R` secara umum hanya dapat membaca data dengan format TXT dan CSV. Pada `RStudio` fungsi ini bertambah dengan adanya library tambahan yang telah terinstall di `RStudio` untuk membaca file dengan format EXCEL, SPSS, SAS dan STATA.

Secara umum fungsi yang digunakan untuk membaca data dengan format tabel seperti TXT dan CSV adalah fungsi`read.table()`. Berikut adalah list fungsi dasar lainnya untuk membaca file dengan format TXT dan CSV pada `R`:

- **read.csv()**: untuk membaca file dengan format *comma separated value*(".csv").
- **read.csv2()**: varian yang digunakan jika pada file ".csv" yang akan dibaca mengandung koma (",") sebagai desimal dan semicolon (";") sebagai pemisah antar variabel atau kolom.
- **read.delim()**: untuk membaca file dengan format *tab-separated value*(".txt").
- **read.delim2()**: membaca file dengan format ".txt" dengan tanda koma (",") sebagai penujuk bilangan desimal.

Masing-masing fungsi diatas dapat dituliskan kedalam `R` dengan format sebagai berikut:


```r
# Membaca tabular data pada  R
read.table(file, header = FALSE, sep = "", dec = ".")
# Membaca"comma separated value" files (".csv")
read.csv(file, header = TRUE, sep = ",", dec = ".", ...)
# atau gunakan read.csv2 jika tanda desimal pada data adalah "," dan pemisah kolom adalah ";"
read.csv2(file, header = TRUE, sep = ";", dec = ",", ...)
# MembacaTAB delimited files
read.delim(file, header = TRUE, sep = "\t", dec = ".", ...)
read.delim2(file, header = TRUE, sep = "\t", dec = ",", ...)
```

> **Note: **
>
> - **file**: nama file diakhiri dengan format file (misal: "nama_file.txt") yang akan di import ke dalam file. Dapat pula diisi lokasi file tersebut berada, misal:(C:/Users/My PC/Documents/nama_file.txt atau .csv)
> - **sep**: pemisah antar kolom. "\t" digunakan untuk tab-delimited file.
> - **header**: nilai logik. jika TRUE, maka `read.table()` akan menganggap bahwa file yang akan dibaca pada baris pertama file merupakan header data. 
> - **dec**: karakter yang digunakan sebagai penunjuk desimal pada data.

Untuk info lebih lanjut terkait fungsi-fungsi tersebut dan contoh bagaimana menggunakannya, pembaca dapat mengakses fitur batuan dari fungsi tersebut menggunakan sintaks berikut:


```r
# mengakses menu bantuan
?read.table
?read.csv
?read.csv2
?read.delim
?read.delim2
```

Misalkan penulis memiliki data pada file bernama "mtcars.csv" dengan desimal berupa titik pada datanya. Penulsi ingin membaca file tersebut, maka penulis akan menuliskan sintaks berikut:


```r
data <- read.csv("mtcars.csv")
```

Secara default perintah tersebut akan membaca baris pertama data sebagai header serta data berupa karakter menjadi factor. Untuk mencegah agar data berupa karakter menjadi faktor, perintah tersebut dapat ditambahkan parameter `stringAsFactor = FALSE`.

Kita juga dapat memilih file yang akan kita baca secara interakti. Misal pada *working directory* terdapat beberapa file yang akan kita baca. Kita ingin melihat file dengan format tertentu yang hendak kita baca, namun kita malas mengecek file explorer pada windows. Untuk mengatasi masalah tersebut, kita dapat menggunakan fungsi `file.choose()` pada `R`. Fungsi tersebut akan menampilkan jendela windows explores sehingga kita dapat memilih file apa yang hendak dibaca. Berikut adalah contoh penerapannya:


```r
data <- read.csv(file.choose())
```

> **Note: ** pastikan format file yang dibaca sama dengan fungsi import yang digunakan.

Kita juga dapat membaca file dari internet. Untuk melakukannya kit hanya perlu meng-copy url file tersebut. Berikut adalah contoh file yang dibaca dari internet:


```r
# Membaca file dari internet
data <- read.delim("http://www.sthda.com/upload/boxplot_format.txt")

# mengecek 6 observasi awal
head(data)
```

```
##    Nom variable Group
## 1 IND1       10     A
## 2 IND2        7     A
## 3 IND3       20     A
## 4 IND4       14     A
## 5 IND5       14     A
## 6 IND6       12     A
```

### Membaca File CSV dan TXT Menggunakan Library readr

Pada bagian sebelumnya kita telah belajar bagaimana cara membaca file dengan format CSV dan TXT menggunakan paket dasar `R`. Pada bagian ini penulis akan menjelaskan bagaimana cara membaca file dengan format TXT dan CSV pada `R` menggunakan paket `readr`.

`readr` dikembangkan oleh Hadley Wickham. paket `readr` memberikan solusi cepat dan ramah untuk membaca delimited file ke dalam `R`.

Dibandingkan dengan paket dasar `R`, `readr` memiliki kelebihan sebagai berikut:

- Mampu membaca file 10x lebih cepat dibandingkan pada paket bawaan `R`.
- Menampilkan *progress bar* yang bermanfaat jika proses pemuatan berlangsung agak lama.
- semua fungsi bekerja dengan cara yang persis sama dengan paket bawaan `R`.

Untuk dapat menggunakan `readr`, kita perlu menginstall paketnya terlebih dahulu. Untuk melakukannya jalankan sintaks berikut:


```r
# Menginstall paket
install.packages("readr")

# Memuat paket
library(readr)
```

Berikut adalah format bebrapa fungsi yang dapat digunakan:


```r
# Fungsi umum (membaca TXT dan CSV) dapat juga membaca flat file dan tsv
read_delim(file, delim, col_names = TRUE)
# Membaca comma (",") separated values
read_csv(file, col_names = TRUE)
# Membaca semicolon (";") separated values
read_csv2(file, col_names = TRUE)
# Membaca tab separated values
read_tsv(file, col_names = TRUE)
```

> **Note: **
>
> - **file**: path file, koneksi atau raw vector. File yang berakhiran .gz, .bz2, .xz, atau .zip akan secara otomatis tidak terkompresi. File yang dimulai dengan "http: //", "https: //", "ftp: //", atau "ftps: //" akan diunduh secara otomatis. File gz jarak jauh juga dapat diunduh & didekompresi secara otomatis.
> - **delim**: karakter yang membatasi tiap nilai pada file.
> - **col_names**: nilai logik. Jika TRUE, maka baris pertama akan menjadi header.

Berikut adalah contoh bagaimana cara membaca file menggunakan fungsi pada paket `readr`:


```r
# Membaca file lokal
data <- read_csv("mtcars.csv")

# atau
data <- read_csv(file.choose())

# Membaca dari internet
data <- read_tsv("http://www.sthda.com/upload/boxplot_format.txt")
```

Kita juga dapat menspesifikasi jenis data pada kolom yang akan dibaca. Keuntungan dari penentuan jenis kolom (tipe data) akan memastikan data yang telah dibaca tidak salah berdasarkan jenis data pada masing-masing kolom.

Beberapa format jenis kolom yang tersedia pada `readr` adalah sebagi berikut:

- **col_integer()**: untuk menentukan integer (alias = "i").
- **col_double()**: untuk menentukan kolom sebagai jenis data double (alias = "d").
- **col_logical()**: untuk menentukan variabel logis (alias = "l").
- **col_character()**: meninggalkan string apa adanya.Tidak mengonversinya menjadi faktor (alias = "c").
- **col_factor()**: untuk menentukan variabel faktor (atau pengelompokan) (alias = "f")
- **col_skip()**: untuk mengabaikan kolom (alias = "-" atau "_")
- **col_date()** (alias = "D"), **col_datetime()** (alias = "T") dan **col_time()** ("t") untuk menentukan tanggal, waktu tanggal, dan waktu.

Berikut adalah contoh penerapannya:

```r
data <- read_csv("my_file.csv", col_types = cols(
  x = "i", # kolom integer
  treatment = "c" # kolom karakter/string
))
```

Untuk mempermudah pembaca dalam mempelajari materi ini, pembaca dapat melihat dokumentasi yang berisi perintah-perintah dasar pada paket ini di situs <https://readr.tidyverse.org/>. Selain itu, tersedia juga lembar *cheatsheet* yang berguna saat pembaca kebingungan dengan fungsi-fungsi yang ada namum pembaca tidak ingin membuka dokumentasi pada situs tersebut. *Cheatsheet dapat di unduh pada situs <https://rawgit.com/rstudio/cheatsheets/master/data-import.pdf>

### Import File Excel Pada R

Keunggulan penggunaan excel sebagai format penyimpan data adalah kita dapat menyimpan banyak data dan memisahkannya pada lembar (*sheet*) yang berbeda sebagai suatu data yang independen dibandingkan pembacaan pada file csv yang hanya berisikan satu tabel data saja tiap file.

Pada `R` kita dapat melakukan pembacaan file menggunakan berbagai macam cara seperti menggunakan paket bawaan `R` maupun menggunakan library yang perlu kita install. Berikut adalah beberapa cara membaca file excel pada `R`.

a. Mengkonversi terlebih dahulu satu sheet excel yang akan kita baca menjadi format ".csv" maupun ".txt" sehingga dapat dibaca seperti pada sub-bab 3.1.1.

b. Menyalin data dari excel dan mengimport data pada `R`.

Cara ini sedikit mirip dengan cara sebelumnya, dimana kita perlu membuka file excel dan melakukan **select** dan **copy** (ctrl+c) tabel data yang hendak dibaca. Data tersebut selanjutnya akan tersimpan pada **clipboard**.

Data yang telah tersalin selanjutnya diimport ke `R` dengan mengetikkan sintaks berikut:


```r
data <- read.table(file= "clipboard",
                   sep = "\t", header = TRUE)
```

Cara ini merupakan cara yang paling sering penulis gunakan. Kelemahan penggunaan cara ini adalah ketika kita melakukan proses **select** dan **copy** (ctrl+c) tabel yang jumlahnya sangat banyak dan terdapat teks-teks penjelasan terkait tabel data pada lembar kerja excel yang tidak ingin kita sertakan akan memakan waktu yang lebih lama pada proses **select**.

c. Mengimport data menggunakan library readxl.

Paket `readxl`, yang dikembangkan oleh Hadley Wickham, dapat digunakan untuk dengan mudah mengimpor file Excel (xls | xlsx) ke `R` tanpa ada ketergantungan eksternal.

Untuk dapat menggunakan library `readxl` kita harus menginstallnya terlebih dahulu menggunakan sintaks berikut:


```r
# Instal paket
install.packages("readxl")

# memuat paket
library(readxl)
```

Berikut adalah contoh cara mengimport data dengan format xls atau xlsx pada `R`.


```r
# Tentukan sheet dengan nama sheet pada file
data <- read_excel("my_file.xlsx", sheet = "data")

# Tentukan sheet berdasarkan indeks sheet
data <- read_excel("my_file.xlsx", sheet = 2) # membaca sheet ke-2
```

Dokumentasi dari library ini dapat diakses pada tautan <https://readxl.tidyverse.org/>. Pada tautan tersebut pembaca dapat membaca contoh kode dan kegunaan dari berbagai fungsi pada library `readxl`.

d. Mengimport data menggunakan library xlsx

Paket `xlsx`, solusi berbasis `java`, adalah salah satu paket `R` yang ampuh untuk membaca, menulis, dan memformat file Excel. Untuk dapat menggunakannya kita harus menginstall dan memuatnya terlebih dahulu. Berikut sintaks yang digunakan:


```r
# Menginstall paket
install.packages("xlsx")

# Memuat paket
library(xlsx)
```

Terdapat dua buah fungsi yang disediakan pada paket tersebut yaitu `read.xlsx()` dan `read.xlsx2()`. Perbedaan keduanya adalah `read.xlsx2()` digunakan pada file data dengan ukuran yang besar serta proses pembacaan data yang lebih cepat dibandingkan dengan `read.xlsx()`. Fromat yang digunakan untuk kedua fungsi tersebut disajikan sebagai berikut:


```r
read.xlsx(file, sheetIndex, header=TRUE)
read.xlsx2(file, sheetIndex, header=TRUE)
```

> **Note: **
>
> - **file**: nama atau lokasi file berada
> - **sheetIndex**: Indeks dari sheet yang hendak dibaca
> - **header**: nilai logik. Jika bernilai TRUE, maka baris pertama dari sheet menjadi header.

Berikut adalah contoh penggunaanya:


```r
data <- read.xlsx(file.choose(), 1) # membaca sheet 1
```

> **Note: ** kita juga dapat membaca file dari internet seperti pada sub-bab 3.1.1.

### Membaca File Dari Format Aplikasi Statistik

Untuk membaca file yang berasal dari format aplikasi statistik seperti SPSS, SAS, dan STATA kita perlu menginstal dan memuat paket-paket yang dibutuhkan sesuai dengan file yang akan kita install. Berikut adalah sintaks bagaimana cara mengimport file dari berbagai format aplikasi statistik.


```r
# membaca file SPSS
install.packages("Hmisc") # menginstall paket
library(Hmisc) # memuat paket
# simpan SPSS dataset pada transport format
get file='c:\mydata.sav'.
export outfile='c:\mydata.por'. 
data <- spss.get("c:\mydata.por", use.value.labels= TRUE) 
# use.value.labels digunakan untuk mengubah label menjadi factor


# membaca file SAS
install.packages("Hmisc") # menginstall paket
library(Hmisc) # memuat paket
# simpan SAS dataset pada transport format
libname out xport 'c:/mydata.xpt';
data out.mydata;
set sasuser.mydata;
run;
data <- sasxport.get("c:/mydata.xpt") 
# Variabel yang berupa karakter akan dikonversi menjadi factor


# membaca file STATA
install.packages("foreign") # menginstall paket
library(foreign) # memuat paket
data <- read.dta("c:/mydata.dta")
```

Library `haven` dari paket `tidyverse` juga dapat digunakan untuk membacadata dari ekstensi program-program tersebut. Fungsi yang tersedia antara lain:

1. `read_sas()`: membaca format file `.sas7bdat` + `.sas7bcat` dari **SAS**. Fungsi `read_xpt()` dapat digunakan untuk membaca SAS *transport files* (versi 5 dan versi 8).
2. `read_sav()`: membaca format file `.sav` dari **SPSS**. Untuk versi file yang lebih lama (`.por`), kita dapat menggunakan fungsi `read_por()`.
3. `read_dta()`: Membaca format file `.dta` dari **STATA** (berfungsi hingga versi 15).

Berikut adalah sintaks untuk mengistall, memuat, dan contoh penggunaan library `haven`:


```r
library(haven)

# SAS
read_sas("mtcars.sas7bdat")

# SPSS
read_sav("mtcars.sav")

# Stata
read_dta("mtcars.dta")
```

## Import Beberapa File Dalam Beberapa Baris Kode

Kita dapat melakukan import beberapa file kedalam `R` menggunakan beberapa baris kode. Pada contoh ini penulsi akan memberikan contoh bagaimana cara mengimport beberapa file csv yang sejenis kedalam `R`. 

Terlebih dahulu kita perlu memuat dua buah library untuk membantu proses ini yaitu `readr` (membaca file) dan `purrr` (melakukan iterasi). Berikut adalah sintaks untuk melakukannya:


```r
library(readr)
library(purrr)
```


Pada contoh kali ini data yang hendak penulis import adalah data `lelang kota bandung`. Penulis dapat mengunduh dataset yang dibutuhkan pada tahutan [berikut](https://github.com/mohrosidi/intro/tree/master/data-raw).

Untuk melakukan import, langkah pertama yang perlu kita lakukan adalah membuat list lokasi dari file yang akan kita import. Fungsi yang kita perlukan untuk membuat list ini adalah `list.files`. Format fungsi yang digunakan tersebut adalah sebagi berikut:


```r
list.files(path = ".", pattern = NULL, full.names = FALSE)
```

> **Note: **
>
> - **path**: path (jalur) lokasi file data berada.
> - **patern**: pola nama file yang hendak di import.
> - **full.names**: nilai logik. Jika TRUE, jalur direktori didahului dengan nama file untuk memberikan jalur file relatif. Jika FALSE, nama file (bukan path) dikembalikan.

File yang akan penulis import terletak di folder data pada *working directory*. Pada contoh ini penulis akan menggunakan path relatif (biasanya didahului oleh titik dan bukan lokasi drive yang digunakan) agar pemabaca juga dapat melakukannya sendiri. File yang akan di upload memiliki pola penamaan yang sama yaitu mengandung kata `lelang-bandung`. Berikut adalah sintaks untuk membuat list lokasi file akan di import.


```r
list <- list.files(path="./data", pattern="lelang-bandung", full.names=TRUE)

list
```

```
## [1] "./data/001_lelang-bandung_2013.csv"
## [2] "./data/002_lelang-bandung_2014.csv"
## [3] "./data/003_lelang-bandung_2015.csv"
## [4] "./data/004_lelang-bandung_2016.csv"
## [5] "./data/005_lelang-bandung_2017.csv"
```

Setelah lokasi file kita peroleh selanjutnya kita dapat melakukan import seluruh file sekaligus menggunakan metode iterasi.

### for loop

Cara pertama untuk melakukan import seluruh file adalah dengan menggunakan for loop. Untuk melakukannya kita terlebih dahulu perlu membuat list kosong yang kan menyimpan hasil loop yang kita lakukan. Untuk melakukannya kita perlu menggunakan fungsi `vector()`. Format fungsi tersebut adalah sebagi berikut:


```r
vector(mode = "logical", length = 0)
```

> **Note: **
>
> - **mode**: jenis file yang hendak dibuat.
> - **length**: panjang file yang hendak dibuat.

Berikut adalah sintaks yang digunakan:


```r
# print list lokasi file
list
```

```
## [1] "./data/001_lelang-bandung_2013.csv"
## [2] "./data/002_lelang-bandung_2014.csv"
## [3] "./data/003_lelang-bandung_2015.csv"
## [4] "./data/004_lelang-bandung_2016.csv"
## [5] "./data/005_lelang-bandung_2017.csv"
```

```r
# membuat list kosong
output_for <- vector(mode="list", length=length(list))

# for looop
for (i in seq_along(output_for)) {
  output_for[[i]] <- read_csv(list[[i]])
}
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_logical(),
##   tanggal_pembuatan = col_date(format = ""),
##   keterangan = col_logical(),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   keterangan = col_logical(),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   keterangan = col_logical(),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_double(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```r
# print hasil for loops
output_for
```

```
## [[1]]
## # A tibble: 680 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>       <lgl>    <date>          
##  1        5260 J5-Peningk~ NA       2013-02-19      
##  2      171260 B2-Peningk~ NA       2013-02-21      
##  3      374260 J126-Penin~ NA       2013-04-24      
##  4      452260 J140-Penin~ NA       2013-05-19      
##  5      521260 Belanja Mo~ NA       2013-05-20      
##  6      571260 Pengadaan ~ NA       2013-06-11      
##  7      727260 Pembanguna~ NA       2013-08-07      
##  8      628260 SS-06 Bang~ NA       2013-06-25      
##  9      772260 Belanja Mo~ NA       2013-08-13      
## 10      889260 PKP1-Penga~ NA       2013-09-18      
## # ... with 670 more rows, and 28 more variables:
## #   keterangan <lgl>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <lgl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
## 
## [[2]]
## # A tibble: 763 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>          <dbl> <date>          
##  1     1002260 Jasa Konsu~       NA 2014-02-21      
##  2     1003260 Jasa Konsu~   625017 2014-02-21      
##  3     1008260 Pengoperas~       NA 2014-03-03      
##  4     1007260 Pengoperas~       NA 2014-03-03      
##  5     1009260 Jasa Konsu~   792674 2014-03-10      
##  6     1013260 Kajian Mod~       NA 2014-03-12      
##  7     1014260 Belanja Pr~       NA 2014-03-14      
##  8     1016260 Jasa Tenag~       NA 2014-03-18      
##  9     1015260 Jasa Konsu~       NA 2014-03-18      
## 10     1017260 Jasa Tenag~       NA 2014-03-18      
## # ... with 753 more rows, and 28 more variables:
## #   keterangan <lgl>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <lgl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
## 
## [[3]]
## # A tibble: 638 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>          <dbl> <date>          
##  1     2161260 Belanja Ba~       NA 2015-01-06      
##  2     2164260 Pengadaan ~  2558197 2015-02-09      
##  3     2166260 Perawatan ~       NA 2015-02-10      
##  4     2165260 Perawatan ~       NA 2015-02-10      
##  5     2163260 "Pengadaan~  2837522 2015-02-12      
##  6     2173260 Peningkata~  3024560 2015-02-17      
##  7     2174260 Peningkata~  3024515 2015-02-17      
##  8     2178260 Peningkata~  3024663 2015-02-17      
##  9     2172260 Peningkata~  3024534 2015-02-17      
## 10     2167260 Peningkata~  3024431 2015-02-17      
## # ... with 628 more rows, and 28 more variables:
## #   keterangan <lgl>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <lgl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
## 
## [[4]]
## # A tibble: 785 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>          <dbl> <date>          
##  1     2994260 Belanja Ba~  5035789 2015-12-11      
##  2     2995260 Belanja Ja~  5026929 2015-12-11      
##  3     2996260 Belanja Ma~  5027086 2015-12-11      
##  4     2997260 Belanja Ja~  5027006 2015-12-11      
##  5     2998260 Belanja Ja~  5037194 2015-12-11      
##  6     2999260 Belanja Ja~  5037172 2015-12-11      
##  7     3000260 Belanja Ja~  5037210 2015-12-11      
##  8     3007260 Jasa Penga~  5054575 2015-12-11      
##  9     3013260 Penyediaan~  5057427 2015-12-11      
## 10     3014260 Pengadaan ~  5043143 2016-01-12      
## # ... with 775 more rows, and 28 more variables:
## #   keterangan <chr>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <lgl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
## 
## [[5]]
## # A tibble: 414 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>          <dbl> <date>          
##  1     4542260 Pengadaan ~ 11633430 2017-09-08      
##  2     4135260 Belanja Al~ 11005893 2017-05-03      
##  3     4244260 Belanja Ja~ 11367750 2017-06-09      
##  4     4462260 Belanja Ja~ 12437947 2017-08-11      
##  5     4393260 Belanja Ja~ 11999277 2017-07-27      
##  6     4231260 Belanja ja~ 12162438 2017-05-31      
##  7     4233260 Belanja ja~ 12156963 2017-05-31      
##  8     4234260 Belanja ja~ 12150139 2017-05-31      
##  9     4232260 Belanja ja~ 12150318 2017-05-31      
## 10     4238260 Belanja ja~ 12156804 2017-05-31      
## # ... with 404 more rows, and 28 more variables:
## #   keterangan <chr>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <dbl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
```

File kita inginkan telah kita import seluruhnya. Kita dapat membuat objek tunggal pada masing-masing dataset tersebut atau menggabungkannya menjadi satu dataset jika data tersebut merupakan data yang sama (menjelaskan hal yang sama). Misalkan kita ingin menyimpan dataset pertama kedalam objek dengan nama `list1`, kita dapat melakukan subset seperti berikut:


```r
list1 <- output_for[[1]]

# subset kolom 1 baris 1
list1[1,1]
```

```
## # A tibble: 1 x 1
##   kode_lelang
##         <dbl>
## 1        5260
```

Kita dapat juga menggabungkan list `output_for` menjadi satu data frame utuh menggunakan fungsi `rbind` (menggabungkan baris data) karena dataset pada list tersebut memiliki kolom yang sama. Untuk mengefisienkan proses tersebut atau agar kita tidak mengabungkannya satu-persatu kita dapat menggunakan fungsi `Reduce()`. Format fungsi tersebut adalah sebagai berikut:


```r
Reduce(f, x)
```

> **Note: **
>
> - **f**: fungsi yang digunakan.
> - **length**: objek (vektor, list, data frame, dan matriks) yang hendak dikenai fungsi.

Berikut adalah sintaks yang digunakan:


```r
df_for <- Reduce(f=rbind, x=output_for)

# print
df_for
```

```
## # A tibble: 3,280 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>          <dbl> <date>          
##  1        5260 J5-Peningk~       NA 2013-02-19      
##  2      171260 B2-Peningk~       NA 2013-02-21      
##  3      374260 J126-Penin~       NA 2013-04-24      
##  4      452260 J140-Penin~       NA 2013-05-19      
##  5      521260 Belanja Mo~       NA 2013-05-20      
##  6      571260 Pengadaan ~       NA 2013-06-11      
##  7      727260 Pembanguna~       NA 2013-08-07      
##  8      628260 SS-06 Bang~       NA 2013-06-25      
##  9      772260 Belanja Mo~       NA 2013-08-13      
## 10      889260 PKP1-Penga~       NA 2013-09-18      
## # ... with 3,270 more rows, and 28 more variables:
## #   keterangan <chr>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <dbl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
```

### Apply Family Function

Dibandingkan dengan metode for loops, metode ini menggunakan sedikit baris kolom. Pada metode sebelumnya kita perlu menuliskan iterasi for loop dengan beberapa baris kolom. Pada metode ini kita akan menggunakan sebuah fungsi untuk mengimport file yaitu `lapply()`. Fungsi ini telah kita bahas pada Chapter sebelumnya, dimana fungsi ini melakukan iterasi suatu fungsi terhadap objek input berupa list (dapat pula vektor atau data frame) dan menghasilkan output list. Berikut adalah sintaks yang digunakan untuk melakukan import data:


```r
# list lokasi berkas
list
```

```
## [1] "./data/001_lelang-bandung_2013.csv"
## [2] "./data/002_lelang-bandung_2014.csv"
## [3] "./data/003_lelang-bandung_2015.csv"
## [4] "./data/004_lelang-bandung_2016.csv"
## [5] "./data/005_lelang-bandung_2017.csv"
```

```r
# lapply function
output_lapply <- lapply(X=list, FUN=read_csv)
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_logical(),
##   tanggal_pembuatan = col_date(format = ""),
##   keterangan = col_logical(),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   keterangan = col_logical(),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   keterangan = col_logical(),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_double(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```r
# print
output_lapply
```

```
## [[1]]
## # A tibble: 680 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>       <lgl>    <date>          
##  1        5260 J5-Peningk~ NA       2013-02-19      
##  2      171260 B2-Peningk~ NA       2013-02-21      
##  3      374260 J126-Penin~ NA       2013-04-24      
##  4      452260 J140-Penin~ NA       2013-05-19      
##  5      521260 Belanja Mo~ NA       2013-05-20      
##  6      571260 Pengadaan ~ NA       2013-06-11      
##  7      727260 Pembanguna~ NA       2013-08-07      
##  8      628260 SS-06 Bang~ NA       2013-06-25      
##  9      772260 Belanja Mo~ NA       2013-08-13      
## 10      889260 PKP1-Penga~ NA       2013-09-18      
## # ... with 670 more rows, and 28 more variables:
## #   keterangan <lgl>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <lgl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
## 
## [[2]]
## # A tibble: 763 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>          <dbl> <date>          
##  1     1002260 Jasa Konsu~       NA 2014-02-21      
##  2     1003260 Jasa Konsu~   625017 2014-02-21      
##  3     1008260 Pengoperas~       NA 2014-03-03      
##  4     1007260 Pengoperas~       NA 2014-03-03      
##  5     1009260 Jasa Konsu~   792674 2014-03-10      
##  6     1013260 Kajian Mod~       NA 2014-03-12      
##  7     1014260 Belanja Pr~       NA 2014-03-14      
##  8     1016260 Jasa Tenag~       NA 2014-03-18      
##  9     1015260 Jasa Konsu~       NA 2014-03-18      
## 10     1017260 Jasa Tenag~       NA 2014-03-18      
## # ... with 753 more rows, and 28 more variables:
## #   keterangan <lgl>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <lgl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
## 
## [[3]]
## # A tibble: 638 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>          <dbl> <date>          
##  1     2161260 Belanja Ba~       NA 2015-01-06      
##  2     2164260 Pengadaan ~  2558197 2015-02-09      
##  3     2166260 Perawatan ~       NA 2015-02-10      
##  4     2165260 Perawatan ~       NA 2015-02-10      
##  5     2163260 "Pengadaan~  2837522 2015-02-12      
##  6     2173260 Peningkata~  3024560 2015-02-17      
##  7     2174260 Peningkata~  3024515 2015-02-17      
##  8     2178260 Peningkata~  3024663 2015-02-17      
##  9     2172260 Peningkata~  3024534 2015-02-17      
## 10     2167260 Peningkata~  3024431 2015-02-17      
## # ... with 628 more rows, and 28 more variables:
## #   keterangan <lgl>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <lgl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
## 
## [[4]]
## # A tibble: 785 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>          <dbl> <date>          
##  1     2994260 Belanja Ba~  5035789 2015-12-11      
##  2     2995260 Belanja Ja~  5026929 2015-12-11      
##  3     2996260 Belanja Ma~  5027086 2015-12-11      
##  4     2997260 Belanja Ja~  5027006 2015-12-11      
##  5     2998260 Belanja Ja~  5037194 2015-12-11      
##  6     2999260 Belanja Ja~  5037172 2015-12-11      
##  7     3000260 Belanja Ja~  5037210 2015-12-11      
##  8     3007260 Jasa Penga~  5054575 2015-12-11      
##  9     3013260 Penyediaan~  5057427 2015-12-11      
## 10     3014260 Pengadaan ~  5043143 2016-01-12      
## # ... with 775 more rows, and 28 more variables:
## #   keterangan <chr>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <lgl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
## 
## [[5]]
## # A tibble: 414 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>          <dbl> <date>          
##  1     4542260 Pengadaan ~ 11633430 2017-09-08      
##  2     4135260 Belanja Al~ 11005893 2017-05-03      
##  3     4244260 Belanja Ja~ 11367750 2017-06-09      
##  4     4462260 Belanja Ja~ 12437947 2017-08-11      
##  5     4393260 Belanja Ja~ 11999277 2017-07-27      
##  6     4231260 Belanja ja~ 12162438 2017-05-31      
##  7     4233260 Belanja ja~ 12156963 2017-05-31      
##  8     4234260 Belanja ja~ 12150139 2017-05-31      
##  9     4232260 Belanja ja~ 12150318 2017-05-31      
## 10     4238260 Belanja ja~ 12156804 2017-05-31      
## # ... with 404 more rows, and 28 more variables:
## #   keterangan <chr>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <dbl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
```

Seperti sebelumnya kita akan menggabungkan dataset pada list yang dihasilkan menggunakan fungsi `Reduce()`. Berikut adalah sintaks yang digunakan:


```r
df_lapply <- Reduce(rbind,output_lapply)

# print
head(df_lapply)

# cek apakah output for dan lapply seragam
identical(df_for, df_lapply)
```

### Map Family Function

Terakhir, Anda akan melakukan impor data dengan menggunakan keluarga `map` dari paket `purrr`. Adapun fungsi yang akan digunakan adalah `map_dfr`. Fungsi ini menerima input list berisi lokasi file berada. Fungsi ini selanjutnya membaca sekaligus menggabungkan file yang telah dibaca dengan menambahkan fungsi `read_csv`. File akan digabungkan berdasarkan baris. Untuk file yang ingi digabungkan secara menyamping (berdasarkan kolom) dapat menggunakan fungsi `map_dfc`. Struktur penulisan kode di keluarga `map` serupa dengan penulisan kode di keluarga `apply`, yaitu sebagai berikut:



```r
library(purrr) # aktifkan paket purrr
list
```

```
## [1] "./data/001_lelang-bandung_2013.csv"
## [2] "./data/002_lelang-bandung_2014.csv"
## [3] "./data/003_lelang-bandung_2015.csv"
## [4] "./data/004_lelang-bandung_2016.csv"
## [5] "./data/005_lelang-bandung_2017.csv"
```

```r
output_map <- map_dfr(list, read_csv)
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_logical(),
##   tanggal_pembuatan = col_date(format = ""),
##   keterangan = col_logical(),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   keterangan = col_logical(),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   keterangan = col_logical(),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_logical(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```
## Parsed with column specification:
## cols(
##   .default = col_character(),
##   kode_lelang = col_double(),
##   kode_rup = col_double(),
##   tanggal_pembuatan = col_date(format = ""),
##   tahun = col_double(),
##   pagu = col_double(),
##   hps = col_double(),
##   peserta_lelang = col_double(),
##   hasil_negosiasi = col_double(),
##   harga_penawaran = col_double(),
##   harga_terkoreksi = col_double()
## )
```

```
## See spec(...) for full column specifications.
```

```r
output_map
```

```
## # A tibble: 3,280 x 32
##    kode_lelang nama_lelang kode_rup tanggal_pembuat~
##          <dbl> <chr>          <dbl> <date>          
##  1        5260 J5-Peningk~       NA 2013-02-19      
##  2      171260 B2-Peningk~       NA 2013-02-21      
##  3      374260 J126-Penin~       NA 2013-04-24      
##  4      452260 J140-Penin~       NA 2013-05-19      
##  5      521260 Belanja Mo~       NA 2013-05-20      
##  6      571260 Pengadaan ~       NA 2013-06-11      
##  7      727260 Pembanguna~       NA 2013-08-07      
##  8      628260 SS-06 Bang~       NA 2013-06-25      
##  9      772260 Belanja Mo~       NA 2013-08-13      
## 10      889260 PKP1-Penga~       NA 2013-09-18      
## # ... with 3,270 more rows, and 28 more variables:
## #   keterangan <chr>, tahapan_lelang <chr>,
## #   instansi <chr>, satuan_kerja <chr>,
## #   kategori <chr>, metode_pengadaan <chr>,
## #   metode_kualifikasi <chr>, metode_dokumen <chr>,
## #   metode_evaluasi <chr>, tahun_anggaran <chr>,
## #   tahun <dbl>, pagu <dbl>, hps <dbl>,
## #   cara_pembayaran <chr>, pembebanan_ta <chr>,
## #   sumber_pendanaan <chr>, lokasi <chr>,
## #   kualifikasi_usaha <chr>, peserta_lelang <dbl>,
## #   agency <chr>, satker <chr>, nama_pemenang <chr>,
## #   alamat <chr>, npwp <chr>, hasil_negosiasi <dbl>,
## #   harga_penawaran <dbl>, harga_terkoreksi <dbl>,
## #   gagal_lelang <chr>
```

```r
class(output_map)
```

```
## [1] "spec_tbl_df" "tbl_df"      "tbl"        
## [4] "data.frame"
```


## Eksport File

Setelah kita melakukan analisa dan telah memperoleh hasil yang kita inginkan dan memperoleh data frame berupa hasil prediksi suatu model atau data yang telah dibersihakan, kita ingin melakukan pelaporan dalam bentuk file dengan format seperti EXCEL, CSV atau TXT. Untuk melakukannya kita perlu melakukan eksport data yang telah dihasilkan.

Pada bagian ini penulis akan menjelaskan bagaimana cara mengeksport data dari `R` kedalam format TXT, CSV, maupun EXCEL. Sebenarnya `R` memungkinkan untuk melakukan eksport dalam format lain seperti RDA maupun RDS yang tidak dibahas dalam buku ini karena berada diluar lingkup buku ini.

### Eksport Data Menjadi Format TXT dan CSV

Terdapat dua cara untuk melakukan ekport data dari `R` menjadi format TXT atau CSV, yaitu melalui paket dasar `R` maupun menggunakan library `readr`. Kedua cara tersebut memiliki sejumlah kemiripan dari segi fungsi, namun berbeda dari segi kecepatan eksport.

Fungsi dasar yang digunakan pada `R` untuk melakukan eksport file kedalam format TXT dan CSv adalah `write.tabel()`. Format umum yang digunakan adalah sebagai berikut:


```r
write.table(x, file, sep= " ", dec = ",",
            row.names = TRUE, col.names = TRUE)
```

> **Note: **
>
> - **x**: matriks atau data frame yang akan ditulis.
> - **file**: karakter yang menentukan nama file yang dihasilkan.
> - **sep**: string pemisah bidang atau kolom, mis., sep = “\ t” (untuk nilai yang dipisahkan tab).
> - **dec**: string yang akan digunakan sebagai pemisah desimal. Standarnya adalah “.”.
> - **row.names**: nilai logik yang menunjukkan apakah nama baris x harus ditulis bersama dengan x, atau vektor karakter nama baris yang akan ditulis.
> - **col.names**: baik nilai logik yang menunjukkan apakah nama kolom x harus ditulis bersama dengan x, atau vektor karakter nama kolom yang akan ditulis. Jika `col.names = NA` dan `row.names = TRUE` ditambahkan nama kolom kosong, yang merupakan konvensi yang digunakan untuk file CSV untuk dibaca oleh spreadsheet.

Selain menggunakan fungsi tersebut, untuk eksport ke dalam format CSV juga dapa menggunakan fungsi `write.csv()` atau `write.csv2()`. Berikut adalah format yang digunakan:


```r
write.csv(data, file="data.csv")
write.csv2(data, file="data.csv")
```

Secara penampakan kedua fungsi tersebut pada dasarnya sama dengan fungsi `write.table()`, bedanya adalah kedua fungsi tersebut spesifik digunakan untuk eksport file kedalam format CSV.

> **Note: **
> 
> - **write.csv()** menggunakan "." sebagai titik desimal serta "," sebagai pemisah antar kolom data.
> - **write.csv2()** menggunakan "," sebagai titik desimal serta ";" sebagai pemisah antar kolom data.

Misalkan kita ingin melakukan eksport data objek `mtcars` kedalam format CSV. Untuk melakukannya dapat dilakukan dengan sintaks berikut:


```r
write.csv(mtcars, file="mtcars.csv", row.names = FALSE)
```

> **Note: ** Hasil ekspoet ditampilkan pada *working directory*

Kita juga dapat menggunakan fungsi `write_delim()` dari library `readr` untuk melakukan eksport data kedalam format CSV atau TXT. Berdasarkan format file yang hendak dihasilkan kita juga dapat menggunakan fungsi `write_csv()` atau `write_tsv()`. Berikut adalah penjelasan terkait kedua fungsi tersebut:

- **write_csv()**: untuk mengeksport kedalam format CSV.
- **write_tsv()**: untuk mengeksport kedalam format TXT.

Format sederhana ketiga fungsi fungsi tersebut adalah sebagai berikut:


```r
# Fungsi umum
write_delim(x, path, delim = " ")
# Write comma (",") separated value files
write_csv(file, path)
# Write tab ("\t") separated value files
write_tsv(file, path)
```

> **Note: **
>
> - **x**: data frame yang akan ditulis
> - **path**: path ke file hasil (dapat berupa nama file disertai ekstensi file yang akan dibuat)
> - **delim**: Delimiter digunakan untuk memisahkan nilai. Harus karakter tunggal.

Berikut adalah contoh penerapan dari fungsi tersebut:


```r
# memuat mtcars data
data(mtcars)
library(readr)

# eksport mtcars menjadi tsv atau txt
write_tsv(mtcars, path = "mtcars.txt")

# eksport mycars menjadi csv
write_csv(mtcars, path = "mtcars.csv")
```

### Eksport Data Menjadi Format Excel

Untuk mengeksport data menjadi format EXCEL (".xls" atau ".xlsx") kita dapat menggunakan fungsi `write.xlsx()` dan `write.xlsx2()` dari library `xlsx`. Berikut adalah format sederhana yanga digunakan:


```r
write.xlsx(x, file, sheetName = "Sheet1", 
  col.names = TRUE, row.names = TRUE, append = FALSE)
write.xlsx2(x, file, sheetName = "Sheet1",
  col.names = TRUE, row.names = TRUE, append = FALSE)
```

> **Note: **
>
> - **x**: sebuah data frame untuk ditulis ke dalam worksheet.
> - **file**: path ke file output.
> - **sheetName**: string karakter yang digunakan untuk nama sheet.
> - **col.names, row.names**: nilai logik yang menentukan apakah nama kolom / nama baris x akan ditulis ke file.
> - **append**: nilai logis yang menunjukkan apakah x harus ditambahkan ke file yang ada.

Berikut adalah contoh penerapannya:


```r
library("xlsx")
# Menuliskan dataset pertama pada workbook
write.xlsx(USArrests, file = "myworkbook.xlsx",
      sheetName = "USA-ARRESTS", append = FALSE)
# Menambahkan dataset kedua pada workbook
write.xlsx(mtcars, file = "myworkbook.xlsx", 
           sheetName="MTCARS", append=TRUE)
# Menambahkan dataset kedua pada workbook
write.xlsx(iris, file = "myworkbook.xlsx",
           sheetName="IRIS", append=TRUE)
```

### Eksport File Dalam Format SAS, SPSS, dan STATA

Untuk memgeksport file dalam format seperti `.sas7bdat`, `.sav`, atau `.dta`, kita dapat menggunakan library `haven` dari paket `tidyverse`. Berikut adalah contoh sintaks untuk melakukannya:


```r
library(haven)

# SAS
write_sas(mtcars, "mtcars.sas7bdat")

# SPSS
write_sav(mtcars, "mtcars.sav")

# Stata
write_dta(mtcars, "mtcars.dta")
```


## Tibble Data Format

Tibble adalah data frame yang menyediakan metode print yang lebih bagus, berguna saat bekerja dengan kumpulan data besar. Pada bagian ini penulis akan menjelaskan penggunaan tibble sebagai alternatif kita dalam berinteraksi dengan data frame.

Untuk membuat tibble kita perlu menginstall dan memuat library `tibble` yang dikembangkan oleh **Hadley Wichham**. Berikut adalah sintaks yang digunakan:


```r
# menginstall paket
install.packages("tibble")

# memuat paket
library(tibble)
```

Dokumetasi library `tibble` dapat pembaca akses pada tautan <https://tibble.tidyverse.org/>. *Cheatsheet* library ini tersedia pada tautan <https://rawgit.com/rstudio/cheatsheets/master/data-import.pdf>.

### Membuat Tibble

Untuk dapat membuat tibble kita dapat melakukan konversi data frame yang sudah ada menjadi tibble menggunakan fungsi `as_tibble()`. Berikut adalah contoh bagaimana membuat tibble mengunakan data `iris`:





```r
# memuat data mtcars
data("iris")

# print
head(iris, 10)
```

```
##    Sepal.Length Sepal.Width Petal.Length Petal.Width
## 1           5.1         3.5          1.4         0.2
## 2           4.9         3.0          1.4         0.2
## 3           4.7         3.2          1.3         0.2
## 4           4.6         3.1          1.5         0.2
## 5           5.0         3.6          1.4         0.2
## 6           5.4         3.9          1.7         0.4
## 7           4.6         3.4          1.4         0.3
## 8           5.0         3.4          1.5         0.2
## 9           4.4         2.9          1.4         0.2
## 10          4.9         3.1          1.5         0.1
##    Species
## 1   setosa
## 2   setosa
## 3   setosa
## 4   setosa
## 5   setosa
## 6   setosa
## 7   setosa
## 8   setosa
## 9   setosa
## 10  setosa
```

```r
# konversi mtcars menjadi tibble
iris_tbl <- as_tibble(iris)

# print
iris_tbl
```

```
## # A tibble: 150 x 5
##    Sepal.Length Sepal.Width Petal.Length Petal.Width
##           <dbl>       <dbl>        <dbl>       <dbl>
##  1          5.1         3.5          1.4         0.2
##  2          4.9         3            1.4         0.2
##  3          4.7         3.2          1.3         0.2
##  4          4.6         3.1          1.5         0.2
##  5          5           3.6          1.4         0.2
##  6          5.4         3.9          1.7         0.4
##  7          4.6         3.4          1.4         0.3
##  8          5           3.4          1.5         0.2
##  9          4.4         2.9          1.4         0.2
## 10          4.9         3.1          1.5         0.1
## # ... with 140 more rows, and 1 more variable:
## #   Species <fct>
```

> **Note: ** Kita dapat mengkonversi tibble menjadi data frame menggunakan fungsi `as.data.frame()`

Secara default saat kita print tibble, maka akan dimunculkan 10 observasi pertama. Pada data frame biasa jika kita print data tersebut maka seluruh observasi akan ditampilkan.

Penggunaan tibble ini cenderung menguntungkan saat kita bekerja dengan jumlah data yang besar dan ingin mengecek observasi yang ada. Hal ini berbeda dengan data frame biasa dimana untuk mengecek observasi awal kita perlu menggunakan fungsi `head()` agar seluruh data tidak ditampilkan. Sehingga penggunaan tibble cenderung membuat proses analisa menjadi lebih rapi.

Kita juga dapat membuat tibble dari kumpulan sejumlah vektor menggunakan fungsi `tibble()`. `tibble()` akan secara otomatis mendaur ulang input dengan panjang 1 (variabel `y`), dan memungkinkan kita untuk merujuk ke variabel yang baru saja kita buat, seperti yang ditunjukkan pada sintaks berikut:


```r
tibble(
  x = 1:20,
  y = 1,
  z = 2*x+5*y
)
```

```
## # A tibble: 20 x 3
##        x     y     z
##    <int> <dbl> <dbl>
##  1     1     1     7
##  2     2     1     9
##  3     3     1    11
##  4     4     1    13
##  5     5     1    15
##  6     6     1    17
##  7     7     1    19
##  8     8     1    21
##  9     9     1    23
## 10    10     1    25
## 11    11     1    27
## 12    12     1    29
## 13    13     1    31
## 14    14     1    33
## 15    15     1    35
## 16    16     1    37
## 17    17     1    39
## 18    18     1    41
## 19    19     1    43
## 20    20     1    45
```

Jika pembaca telah mulai familiar dengan fungsi `data.frame()`, perlu diingat bahwa `tibble()` melakukan lebih sedikit: tidak pernah mengubah jenis input (mis., tidak pernah mengubah string menjadi faktor!), tidak pernah mengubah nama variabel, dan tidak pernah membuat nama baris seperti yang biasa terjadi saat kita menggunakan fungsi `data.frame()`.

Cara lain yang dapat digunakan untuk membuat tibble adalah dengan menggunakan fungsi `tribble()` yang merupakan singkatan dari *transposed tibble*. `tribble()` dikustomisasi untuk entri data dalam kode: judul kolom didefinisikan oleh rumus (yaitu, mereka mulai dengan ~), dan entri dipisahkan oleh koma. Hal ini memungkinkan untuk menata sejumlah kecil data dalam bentuk yang mudah dibaca. Berikut adalah contoh penerapannya:


```r
tribble(
  ~x, ~y, ~z,
  #--/--/----
  "a", 2, 5,
  "b", 5, 7
)
```

```
## # A tibble: 2 x 3
##   x         y     z
##   <chr> <dbl> <dbl>
## 1 a         2     5
## 2 b         5     7
```

Penambahahan komen (#--/--/----) dilakukan untuk memperjelas posisi dari header sehingga meminimalisir kesalahan dalam input data.

### Tibble vs Data Frame

terdapat dua buah perbedaan utama antara tibble dan data frame , yaitu: *printing* dan *subsetting*.

a. **Printing**

Tibbles memiliki metode print halus yang hanya menampilkan 10 baris pertama observasi, dan semua kolom yang sesuai dengan lebar layar. Ini membuatnya lebih mudah untuk bekerja dengan data besar. Selain namanya, setiap kolom melaporkan jenis datanya, fitur bagus yang dipinjam dari fungsi `str()`. Berikut adalah contohnya:


```r
tribble(
  ~x, ~y, ~z,
  #--/---/--------
  "a", 2.1, FALSE,
  "b", 5.5, TRUE
)
```

```
## # A tibble: 2 x 3
##   x         y z    
##   <chr> <dbl> <lgl>
## 1 a       2.1 FALSE
## 2 b       5.5 TRUE
```

Tibbles dirancang agar kita tidak secara sengaja menampilkan data yang sangat banyak saat melakukan perintah `print()`. Tetapi terkadang kita membutuhkan lebih banyak output daripada tampilan default. Ada beberapa opsi yang dapat membantu.

Pertama, kita dapat secara eksplisit melakukan print data frame dan mengontrol jumlah baris (n) dan lebar tampilan. `width = Inf` akan menampilkan semua kolom. Berikut adalah contoh penerapannya


```r
print(iris_tbl, n=15, width=Inf)
```

```
## # A tibble: 150 x 5
##    Sepal.Length Sepal.Width Petal.Length Petal.Width
##           <dbl>       <dbl>        <dbl>       <dbl>
##  1          5.1         3.5          1.4         0.2
##  2          4.9         3            1.4         0.2
##  3          4.7         3.2          1.3         0.2
##  4          4.6         3.1          1.5         0.2
##  5          5           3.6          1.4         0.2
##  6          5.4         3.9          1.7         0.4
##  7          4.6         3.4          1.4         0.3
##  8          5           3.4          1.5         0.2
##  9          4.4         2.9          1.4         0.2
## 10          4.9         3.1          1.5         0.1
## 11          5.4         3.7          1.5         0.2
## 12          4.8         3.4          1.6         0.2
## 13          4.8         3            1.4         0.1
## 14          4.3         3            1.1         0.1
## 15          5.8         4            1.2         0.2
##    Species
##    <fct>  
##  1 setosa 
##  2 setosa 
##  3 setosa 
##  4 setosa 
##  5 setosa 
##  6 setosa 
##  7 setosa 
##  8 setosa 
##  9 setosa 
## 10 setosa 
## 11 setosa 
## 12 setosa 
## 13 setosa 
## 14 setosa 
## 15 setosa 
## # ... with 135 more rows
```

Kita juga dapat mengontrol print default dengan melakukan pengaturan menggunakan fungsi `options()`. Berikut adalah contoh penerapannya:

- **options(tibble.print_max= n, tibble.print_min= m)**: jika terdapat lebih dari "m" baris, print hanya sejumlah "n" baris.
- **options(dplyr.print_min = Inf)**: untuk selalu menampilkan seluruh baris. Perlu diingat fungsi ini dapat digunakan saat kita telah memuat library `dplyr`.
- **options(tibble.width = Inf)**: menampilkan seluruh kolom tanpa mempedulikan lebar tampilan layar.

Cara terakhir untuk menampilkan seluruh observasi adalh dengan fungsi `view()`. Berikut adalah contoh penerapannya pada data `iris_tbl`:


```r
view(iris_tbl)
```

b. **Subsetting**

Sejauh ini semua alat yang kita pelajari telah bekerja dengan data frame yang lengkap. Jika kita ingin mengeluarkan variabel tunggal, kita memerlukan beberapa alat baru, dollar sign (`$`) dan [[. [[dapat mengekstraksi berdasarkan nama atau posisi; `$` hanya mengekstraksi berdasarkan nama. Berikut adalah contoh penerapannya:


```r
# print tibble
iris_tbl
```

```
## # A tibble: 150 x 5
##    Sepal.Length Sepal.Width Petal.Length Petal.Width
##           <dbl>       <dbl>        <dbl>       <dbl>
##  1          5.1         3.5          1.4         0.2
##  2          4.9         3            1.4         0.2
##  3          4.7         3.2          1.3         0.2
##  4          4.6         3.1          1.5         0.2
##  5          5           3.6          1.4         0.2
##  6          5.4         3.9          1.7         0.4
##  7          4.6         3.4          1.4         0.3
##  8          5           3.4          1.5         0.2
##  9          4.4         2.9          1.4         0.2
## 10          4.9         3.1          1.5         0.1
## # ... with 140 more rows, and 1 more variable:
## #   Species <fct>
```

```r
# subset berdasarkan nama kolom
iris_tbl$Sepal.Length
```

```
##   [1] 5.1 4.9 4.7 4.6 5.0 5.4 4.6 5.0 4.4 4.9 5.4 4.8
##  [13] 4.8 4.3 5.8 5.7 5.4 5.1 5.7 5.1 5.4 5.1 4.6 5.1
##  [25] 4.8 5.0 5.0 5.2 5.2 4.7 4.8 5.4 5.2 5.5 4.9 5.0
##  [37] 5.5 4.9 4.4 5.1 5.0 4.5 4.4 5.0 5.1 4.8 5.1 4.6
##  [49] 5.3 5.0 7.0 6.4 6.9 5.5 6.5 5.7 6.3 4.9 6.6 5.2
##  [61] 5.0 5.9 6.0 6.1 5.6 6.7 5.6 5.8 6.2 5.6 5.9 6.1
##  [73] 6.3 6.1 6.4 6.6 6.8 6.7 6.0 5.7 5.5 5.5 5.8 6.0
##  [85] 5.4 6.0 6.7 6.3 5.6 5.5 5.5 6.1 5.8 5.0 5.6 5.7
##  [97] 5.7 6.2 5.1 5.7 6.3 5.8 7.1 6.3 6.5 7.6 4.9 7.3
## [109] 6.7 7.2 6.5 6.4 6.8 5.7 5.8 6.4 6.5 7.7 7.7 6.0
## [121] 6.9 5.6 7.7 6.3 6.7 7.2 6.2 6.1 6.4 7.2 7.4 7.9
## [133] 6.4 6.3 6.1 7.7 6.3 6.4 6.0 6.9 6.7 6.9 5.8 6.8
## [145] 6.7 6.7 6.3 6.5 6.2 5.9
```

```r
#subset berdasarkan posisi
iris_tbl[[1]]
```

```
##   [1] 5.1 4.9 4.7 4.6 5.0 5.4 4.6 5.0 4.4 4.9 5.4 4.8
##  [13] 4.8 4.3 5.8 5.7 5.4 5.1 5.7 5.1 5.4 5.1 4.6 5.1
##  [25] 4.8 5.0 5.0 5.2 5.2 4.7 4.8 5.4 5.2 5.5 4.9 5.0
##  [37] 5.5 4.9 4.4 5.1 5.0 4.5 4.4 5.0 5.1 4.8 5.1 4.6
##  [49] 5.3 5.0 7.0 6.4 6.9 5.5 6.5 5.7 6.3 4.9 6.6 5.2
##  [61] 5.0 5.9 6.0 6.1 5.6 6.7 5.6 5.8 6.2 5.6 5.9 6.1
##  [73] 6.3 6.1 6.4 6.6 6.8 6.7 6.0 5.7 5.5 5.5 5.8 6.0
##  [85] 5.4 6.0 6.7 6.3 5.6 5.5 5.5 6.1 5.8 5.0 5.6 5.7
##  [97] 5.7 6.2 5.1 5.7 6.3 5.8 7.1 6.3 6.5 7.6 4.9 7.3
## [109] 6.7 7.2 6.5 6.4 6.8 5.7 5.8 6.4 6.5 7.7 7.7 6.0
## [121] 6.9 5.6 7.7 6.3 6.7 7.2 6.2 6.1 6.4 7.2 7.4 7.9
## [133] 6.4 6.3 6.1 7.7 6.3 6.4 6.0 6.9 6.7 6.9 5.8 6.8
## [145] 6.7 6.7 6.3 6.5 6.2 5.9
```

Dibandingkan dengan data frame, tibble lebih ketat: tibble tidak pernah melakukan *partial matching*, dan mereka akan menghasilkan peringatan jika kolom yang kita coba akses tidak ada.

## Merapikan Data

Sebelum memulai analisa terhadap data yang kita miliki, umumnya kita akan merapikan data yang akan kita gunakan. Tujuannya adalah agar data yang akan digunakan sudah siap untuk dilakukan analisa dengan software tertentu seperti `R`, dimana pada dataset perlu jelas antara variabel dan nilai (*value*), serta untuk mempermudah dalah memperoleh informasi pada data. Berikut adalah beberapa contoh dataset yang dapat pembaca cermati terkait manakah data yang telah rapi (*tidy data*) dan mana yang belum (*messy data*):


```r
table1                  
```

```
## # A tibble: 6 x 4
##   country      year  cases population
##   <chr>       <int>  <int>      <int>
## 1 Afghanistan  1999    745   19987071
## 2 Afghanistan  2000   2666   20595360
## 3 Brazil       1999  37737  172006362
## 4 Brazil       2000  80488  174504898
## 5 China        1999 212258 1272915272
## 6 China        2000 213766 1280428583
```

```r
table2                  
```

```
## # A tibble: 12 x 4
##    country      year type            count
##    <chr>       <int> <chr>           <int>
##  1 Afghanistan  1999 cases             745
##  2 Afghanistan  1999 population   19987071
##  3 Afghanistan  2000 cases            2666
##  4 Afghanistan  2000 population   20595360
##  5 Brazil       1999 cases           37737
##  6 Brazil       1999 population  172006362
##  7 Brazil       2000 cases           80488
##  8 Brazil       2000 population  174504898
##  9 China        1999 cases          212258
## 10 China        1999 population 1272915272
## 11 China        2000 cases          213766
## 12 China        2000 population 1280428583
```

```r
table3                  
```

```
## # A tibble: 6 x 3
##   country      year rate             
## * <chr>       <int> <chr>            
## 1 Afghanistan  1999 745/19987071     
## 2 Afghanistan  2000 2666/20595360    
## 3 Brazil       1999 37737/172006362  
## 4 Brazil       2000 80488/174504898  
## 5 China        1999 212258/1272915272
## 6 China        2000 213766/1280428583
```

```r
table4a                 
```

```
## # A tibble: 3 x 3
##   country     `1999` `2000`
## * <chr>        <int>  <int>
## 1 Afghanistan    745   2666
## 2 Brazil       37737  80488
## 3 China       212258 213766
```

```r
table4b                 
```

```
## # A tibble: 3 x 3
##   country         `1999`     `2000`
## * <chr>            <int>      <int>
## 1 Afghanistan   19987071   20595360
## 2 Brazil       172006362  174504898
## 3 China       1272915272 1280428583
```

```r
table5   
```

```
## # A tibble: 6 x 4
##   country     century year  rate             
## * <chr>       <chr>   <chr> <chr>            
## 1 Afghanistan 19      99    745/19987071     
## 2 Afghanistan 20      00    2666/20595360    
## 3 Brazil      19      99    37737/172006362  
## 4 Brazil      20      00    80488/174504898  
## 5 China       19      99    212258/1272915272
## 6 China       20      00    213766/1280428583
```


Sebelum kita melakukan analisa di dataset tersebut, kita harus tahu terlebih dahulu apa saja syarat suatu dataset dikatakan rapi (*tidy*). Berikut adalah syaratnya:

- Setiap variabel harus memiliki kolomnya sendiri
- Setiap observasi harus memiliki barisnya sendiri
- Setiap nilai berada pada sel tersendiri

Ketiga syarat tersebut saling berhubungan sehingga jika salah satu syarat tersebut tidak terpenuhi, maka dataset belum bisa dikatakan *tidy*. Ketiga syarat tersebut dapat divisualisasikan melalui Gambar \@ref(fig:tidy)

\begin{figure}

{\centering \includegraphics{tidy} 

}

\caption{Visualisasi 3 rule tidy data}(\#fig:tidy)
\end{figure}

Dengan menggunakan prinsip data *tidy* kita akan menganalisa data tersebut satu persatu. Berikut adalah analisa terkait data-data tesebut:

1. `table1` merupakan data yang telah *tidy*. Ketiga prinsip data *tidy* telah terpenuhi.
2. `table2` merupakan data yang belum *tidy* karena variabel tidak berada pada masing-masing kolomnya. Variabel `type` dapat dipecah lagi menjadi 2 kolom baru yaitu kolom  `cases` dan kolom `population`.
3. `table3` merupakan data yang belum *tidy*. Kolom `rate` berisikan rasio yang seharusnya berisi nilai hasil bagi kedua variabel. Dapat kita duga pembilang dari nilai rasio merupakan nilai variabel `cases`, sedangkan penyebutnya merupakan nilai dari variabel `population`. Agar *tidy* kolom `rate` perlu dipecah menjadi 2 kolom baru (2 variabel) yaitu `cases` dan `population` atau nilai yang ditampilkan pada kolom `rate` adalah hasil bagi kedua nilai (bukan pecahan).
4. `table4a` dan `table4b` masih belum *tidy*. Dua kolom yaitu kolom `1999` dan `2000` perlu dijadikan satu kolom yaitu kolom variabel `year`. Nilai dari kolom lama  selanjutnya digabung menjadi satu kolom, untuk `table4a` menjadi kolom `cases`, sedangkan `table4b` sebagai kolom `population`.
5. `table5` masih belum *tidy*. Agar data tersebut *tidy* maka kolom `century` dan `year` perlu digabung menjadi satu kolom (variabel) yaitu kolom `year`. Selain itu, kolom `rate juga perlu dijadikan satu atau 2 kolom seperti yang dilakukan pada poin 3.

Berdasarkan contoh-contoh tersebut pada pembahasan kali ini penulis akan menjelaskan bagaiman cara melakukan perapihan data menggunakan library `tidyr` dari paket `tidyverse`. Sebelum kita melakukannya berikut adalah sintaks untuk menginstall library `tidyr` secara terpisah dari paket `tidyverse` tersebut:


```r
# memasang paket
install.packages("tidyr")
```


```r
# memuat paket
library(tidyr)
```

### Gather

`gather()` merupakan fungsi yang digunakan untuk menggabungkan beberapa kolom menjadi satu kolom kunci (disebut juga sebagai *pivot long*. Secara sederhana fungsi tersebut dapat dituliskan dengan format sebagai berikut:


```r
gather(data, key, value, ...)
```

> **Note: **
>
> - **data**: data frame
> - **key, value**: nama kunci dan kolom nilai yang akan dibuat di output
> - **...**: Spesifikasi kolom untuk dikumpulkan. Nilai yang diizinkan adalah:
>       + nama variabel
>       + jika kita ingin memilih semua variabel antara a dan e, gunakan a:e
>       + jika kita ingin mengecualikan nama kolom y gunakan -y 
>       + untuk opsi lainnya, lihat: `dplyr::select()`

Visualisasi dari fungsi `gather` ini disajikan pada Gambar \@ref(fig:gather)

\begin{figure}

{\centering \includegraphics{gather} 

}

\caption{Visualisasi fungsi gather (Sumber: Rstudio,2017)}(\#fig:gather)
\end{figure}

Berikut adalah contoh penerapannya pada dataset `table4a` dan `table4b`:


```r
# Table4a
table4a_new <- gather(table4a, 
                    # variabel kunci
                    key = "year",
                    # nilai variabel
                    value = "cases",
                    # kecualikan kolom country
                    -country)

table4a_new
```

```
## # A tibble: 6 x 3
##   country     year   cases
##   <chr>       <chr>  <int>
## 1 Afghanistan 1999     745
## 2 Brazil      1999   37737
## 3 China       1999  212258
## 4 Afghanistan 2000    2666
## 5 Brazil      2000   80488
## 6 China       2000  213766
```

```r
# Table4a
table4b_new <- gather(table4b, 
                    # variabel kunci
                    key = "year",
                    # nilai variabel
                    value = "population",
                    # kecualikan kolom country
                    -country)

table4b_new
```

```
## # A tibble: 6 x 3
##   country     year  population
##   <chr>       <chr>      <int>
## 1 Afghanistan 1999    19987071
## 2 Brazil      1999   172006362
## 3 China       1999  1272915272
## 4 Afghanistan 2000    20595360
## 5 Brazil      2000   174504898
## 6 China       2000  1280428583
```

Berdasarkan hasil yang diperoleh terlihat bahwa variabel `year` pada kedua dataset tersebut memiliki jenis data karakter. Jenis data ini masih belum sesuai sehingga perlu dikonversi agar menjadi jenis data numerik (*int = integer*). Untuk melakukannya jalankan sintaks berikut:


```r
# table4a_new
table4a_new$year <- as.integer(table4a_new$year)
table4a_new
```

```
## # A tibble: 6 x 3
##   country      year  cases
##   <chr>       <int>  <int>
## 1 Afghanistan  1999    745
## 2 Brazil       1999  37737
## 3 China        1999 212258
## 4 Afghanistan  2000   2666
## 5 Brazil       2000  80488
## 6 China        2000 213766
```

```r
# table4a_new
table4b_new$year <- as.integer(table4b_new$year)
table4b_new
```

```
## # A tibble: 6 x 3
##   country      year population
##   <chr>       <int>      <int>
## 1 Afghanistan  1999   19987071
## 2 Brazil       1999  172006362
## 3 China        1999 1272915272
## 4 Afghanistan  2000   20595360
## 5 Brazil       2000  174504898
## 6 China        2000 1280428583
```

Data yang diperoleh sekaran telah rapi (*tidy*), sehingga sudah siap untuk dilakukan analisa data.

### Spread

Fungsi `spread()` berkebalikan dengan `gather()`. Fungsi `gather()` menggabungkan beberapa kolom menjadi 2 buah kolom kolom kunci sedangkan `spread()` merubah dua kolom menjadi beberapa kolom. Format sederhanya adalah sebagai berikut:

> **Note: **
>
> - **data**: data frame
> - **key**: nama kolom yang akan dijadikan heading pada kolom baru
> - **value**: nama kolom yang nilainya akan mengisi setiap sel

Visualisasi dari fungsi `spread()` ini disajikan pada Gambar \@ref(fig:spread)

\begin{figure}

{\centering \includegraphics{spread} 

}

\caption{Visualisasi fungsi spread (Sumber: Rstudio,2017)}(\#fig:spread)
\end{figure}

Pada contoh kasus pada data `table2`, kita dapat memisahkan kolom `type` menjadi kolom baru yaitu kolom `cases` dan `population`. Untuk melakukannya jalankan sintaks berikut:


```r
# spread
table2_new <- spread(table2,
                        key = type,
                        value = count)

#print
table2_new
```

```
## # A tibble: 6 x 4
##   country      year  cases population
##   <chr>       <int>  <int>      <int>
## 1 Afghanistan  1999    745   19987071
## 2 Afghanistan  2000   2666   20595360
## 3 Brazil       1999  37737  172006362
## 4 Brazil       2000  80488  174504898
## 5 China        1999 212258 1272915272
## 6 China        2000 213766 1280428583
```

Terlihat bahwa data `table2_new` tampak memenuhi syarat kerapihan data (*tidy*). 

### Separate

Fungsi `separate()` merupakan fungsi yang digunakan untuk memisahkan sejumlah nilai pada sebuah kolom menjadi beberapa kolom berdasarkan karakter pemisah yang ada di dalam nilai suatu kolom. Fungsi ini berbeda dengan fungsi sebelumnya seperti `gather()` dan `spread()` yang menggabung atau memisahkan 2 atau beberapa kolom. Visualisasi dari fungsi `separate()` ini disajikan pada Gambar \@ref(fig:separate)

\begin{figure}

{\centering \includegraphics{separate} 

}

\caption{Visualisasi fungsi separate (Sumber: Rstudio,2017)}(\#fig:separate)
\end{figure}

Jika fungsi `separate()` memisahkan sejumlah nilai menajdi beberapa kolom sesuai dengan karakter pemisah, fungsi `separate_rows()` memisahkan nilai menjadi beberapa baris berdasarkan karakter pemisah. Visualisasi dari fungsi `separate_rows()` ini disajikan pada Gambar \@ref(fig:separaterows)

\begin{figure}

{\centering \includegraphics{separate_rows} 

}

\caption{Visualisasi fungsi separate rows}(\#fig:separaterows)
\end{figure}

Format sederhana fungsi `separate()`  dan `separate_rows()` adalah sebagai berikut:


```r
separate(data, col, into, sep = "[^[:alnum:]]+", convert= FALSE)

separate(data,...., sep = "[^[:alnum:]]+", convert= FALSE)
```

> **Note: **
>
> - **data**: data frame.
> - **col**: Nama kolom yang tidak dikutip.
> - **into**: Vektor karakter menentukan nama variabel baru yang akan dibuat.
> - **sep**: Pemisah antar kolom:
>    + Jika karakter, diartikan sebagai ekspresi reguler.
Jika numerik, diartikan sebagai posisi untuk dibelah. Nilai-nilai positif mulai dari 1 di ujung kiri string; nilai negatif mulai dari -1 di ujung kanan string.
> - **convert**: nilai logik. Jika bernilai TRUE maka kolom baru yang akan diperoleh akan dikonversi berdasarkan jenis data yang seharusnya.

Pada `table3` dan `table5` kita akan mencoba memisahkan kolom `rate` menjadi 2 kolom yaitu kolom `cases` dan kolom `population`. Berikut adalah sintaks yang digunakan:


```r
# table3
table3_new <- separate(table3, col=rate,
                       into=c("cases", "population"),
                       sep="/", convert=TRUE)
table3_new
```

```
## # A tibble: 6 x 4
##   country      year  cases population
##   <chr>       <int>  <int>      <int>
## 1 Afghanistan  1999    745   19987071
## 2 Afghanistan  2000   2666   20595360
## 3 Brazil       1999  37737  172006362
## 4 Brazil       2000  80488  174504898
## 5 China        1999 212258 1272915272
## 6 China        2000 213766 1280428583
```

```r
# table5
table5_new <- separate(table5, col=rate,
                       into=c("cases", "population"),
                       sep="/", convert=TRUE)
table5_new
```

```
## # A tibble: 6 x 5
##   country     century year   cases population
##   <chr>       <chr>   <chr>  <int>      <int>
## 1 Afghanistan 19      99       745   19987071
## 2 Afghanistan 20      00      2666   20595360
## 3 Brazil      19      99     37737  172006362
## 4 Brazil      20      00     80488  174504898
## 5 China       19      99    212258 1272915272
## 6 China       20      00    213766 1280428583
```

Berdasarkan hasil yang diperoleh terlihat bahwa `table3` telah *tidy*, sedangkan `table5` belum *tidy* sebab kolom `century` dan kolom `year` perlu digabungkan menjadi kolom `year`.

Kita dapat juga memisahkan kolom `rate` pada `table3` menjadi baris baru menggunakan fungsi `separate_rows()`. Berikut adalah sintaks yang digunakan:


```r
separate_rows(table3, col=rate, sep="/")
```

```
## # A tibble: 12 x 3
##    country      year rate      
##    <chr>       <int> <chr>     
##  1 Afghanistan  1999 745       
##  2 Afghanistan  1999 19987071  
##  3 Afghanistan  2000 2666      
##  4 Afghanistan  2000 20595360  
##  5 Brazil       1999 37737     
##  6 Brazil       1999 172006362 
##  7 Brazil       2000 80488     
##  8 Brazil       2000 174504898 
##  9 China        1999 212258    
## 10 China        1999 1272915272
## 11 China        2000 213766    
## 12 China        2000 1280428583
```

### Unite

Fungsi `unite()` merupakan kebalikan dari fungsi `separate()`, dimana fungsi ini menggabungkan sejumlah kolom menjadi 1 kolom. Format sederhana untuk melakukanya disajikan sebagai berikut:


```r
unite(data, col, ..., sep = "_")
```

> **Note: **
>
> - **data**: data frame.
> - **col**: nama kolom baru (tanpa tanda kutip) untuk ditambahkan.
> - **sep**: pemisah yang akan digunakan pada antar nilai.

Visualisasi dari fungsi `unite()` ini disajikan pada Gambar \@ref(fig:spread)

\begin{figure}

{\centering \includegraphics{unite} 

}

\caption{Visualisasi fungsi unite (Sumber: Rstudio,2017)}(\#fig:unite)
\end{figure}

Pada dataset `table5_new` kita akan menggabungkan kolom `century` dan kolom `year` menjadi kolom `year` tanpa pemisah. Berikut adalah sintaks untuk melakukannya: 


```r
table5_new2 <- unite(table5_new, century,
                    year, col="year", sep="")
table5_new2
```

```
## # A tibble: 6 x 4
##   country     year   cases population
##   <chr>       <chr>  <int>      <int>
## 1 Afghanistan 1999     745   19987071
## 2 Afghanistan 2000    2666   20595360
## 3 Brazil      1999   37737  172006362
## 4 Brazil      2000   80488  174504898
## 5 China       1999  212258 1272915272
## 6 China       2000  213766 1280428583
```

Berdasarkan hasil yang diperoleh dapat dilihat bahwa `table5_new2` telah memenuhi syarat data yang *tidy* atau rapi. Data tersebut telah siap untuk dilakukan analisa lebih lanjut.

## Transformasi Data

Data frame merupakan struktur data utama dalam statistik dan dalam `R`. Struktur dasar data frame ialah ada satu observasi tiap baris dan setiap kolom mewakili variabel, ukuran, fitur, atau karakteristik pengamatan itu yang telah dijelaskan pada bagian sebelumya. `R` memiliki implementasi internal data frame yang kemungkinan besar akan kita gunakan paling sering. Namun, ada paket di CRAN yang mengimplementasikan data frame layaknya basis data relasional yang memungkinkan kita untuk beroperasi pada data frame yang sangat besar.

Mengingat pentingnya mengelola dat frame, penting bagi kita untuk memiliki alat yang baik untuk melakukannya. `R` memiliki beberapa paket seperti fungsi `subset()` dan penggunaan operator "[" dan "$" untuk mengekstrak himpunan bagian dari frame data. Namun, operasi lain, seperti pemfilteran, pengurutan, dan pengelompokan data, seringkali dapat menjadi operasi yang membosankan di `R` yang sintaksisnya tidak terlalu intuitif. Library `dplyr` dari paket `tidyverse` dirancang untuk mengurangi banyak masalah ini dan menyediakan serangkaian rutinitas yang dioptimalkan secara khusus untuk menangani data frame.

### Paket dplyr

Library `dplyr` dikembangkan oleh **Hadley Wickham** dari **RStudio** dan merupakan versi yang dioptimalkan dari library `plyr`-nya. Library `dplyr` tidak menyediakan fungsionalitas baru untuk `R` sendiri, dalam arti bahwa semua yang dilakukan `dplyr` sudah dapat dilakukan dengan fungsi basis `R`, tetapi sangat menyederhanakan fungsi yang ada di `R`.

Salah satu kontribusi penting dari library `dplyr` adalah ia menyediakan "*grammar*" (khususnya, kata kerja) untuk manipulasi data dan untuk beroperasi pada data frame. Melalui *grammar* ini, kita dapat berkomunikasi dengan masuk akal apa yang telah kita lakukan terhadap data frame dapat pula dipahami orang lain (dengan asumsi mereka juga tahu *grammar*-nya). Hal ini berguna karena memberikan abstraksi untuk manipulasi data yang sebelumnya tidak ada. Kontribusi lain yang bermanfaat adalah bahwa fungsi `dplyr` sangat cepat, karena banyak operasi utama dikodekan dalam C++.

Pada bagian ini pembaca akan belajar **6** fungsi utama yang ada pada paket `dplyr`. Fungsi tersebut antara lain:

1. Mengambil sejumlah observasi berdasarkan nilainya (`filter()`).
2. Mengurutkan kembali baris data frame berdasarkan nilai pada sebuah atau beberapa variabel (`arrange()`).
3. Mengambil atau subset terhadap sebuah atau beberapa variabel berdasarkan nama variabel/kolom (`select()`).
4. Membuat variabel baru atau menambahkan kolom baru (`mutate()`).
5. Membuat ringkasan terhadap data frame (`summarize()`)
6. Mengelompokkan operasi berdasarkan grup data (`group_by()`).

Keseluruhan fungsi tersebut format fungsi yang seragam, yaitu:

1. Argumen pertama adalah data frame.
2. Argumen selanjutnya adalah deskripsi yang akan dilakukan terhadap data frame (filter, pengurutan kembali, membuat ringkasan, dll) menggunakan nama variabel (tanpa tanda kutip).
3. Hasil operasi yang diperoleh adalah data frame baru.

Untuk memuat library `dplyr` dari `tidyverse jalankan sintaks berikut:


```r
# memuat paket
library(dplyr)
```

Dokumentasi library `dplyr` dapat pembaca akses pada tautan <https://dplyr.tidyverse.org/>. *Cheatsheet* untuk membantu pembaca berkeja menggunakan library ini tersedia pada tautan <https://github.com/rstudio/cheatsheets/blob/master/data-transformation.pdf>.

Pada contoh kali ini penulis akan menggunakan dataset `flights` dari library `nycflights13`. Berikut adalah sintaks untuk memuat dataset tersebut:


```r
library(nycflights13)

#print
flights
```

```
## # A tibble: 336,776 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1      517            515         2
##  2  2013     1     1      533            529         4
##  3  2013     1     1      542            540         2
##  4  2013     1     1      544            545        -1
##  5  2013     1     1      554            600        -6
##  6  2013     1     1      554            558        -4
##  7  2013     1     1      555            600        -5
##  8  2013     1     1      557            600        -3
##  9  2013     1     1      557            600        -3
## 10  2013     1     1      558            600        -2
## # ... with 336,766 more rows, and 13 more variables:
## #   arr_time <int>, sched_arr_time <int>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   air_time <dbl>, distance <dbl>, hour <dbl>,
## #   minute <dbl>, time_hour <dttm>
```

```r
# cek variabel
colnames(flights)
```

```
##  [1] "year"           "month"          "day"           
##  [4] "dep_time"       "sched_dep_time" "dep_delay"     
##  [7] "arr_time"       "sched_arr_time" "arr_delay"     
## [10] "carrier"        "flight"         "tailnum"       
## [13] "origin"         "dest"           "air_time"      
## [16] "distance"       "hour"           "minute"        
## [19] "time_hour"
```

```r
# ringkasan data
summary(flights)
```

```
##       year          month            day      
##  Min.   :2013   Min.   : 1.00   Min.   : 1.0  
##  1st Qu.:2013   1st Qu.: 4.00   1st Qu.: 8.0  
##  Median :2013   Median : 7.00   Median :16.0  
##  Mean   :2013   Mean   : 6.55   Mean   :15.7  
##  3rd Qu.:2013   3rd Qu.:10.00   3rd Qu.:23.0  
##  Max.   :2013   Max.   :12.00   Max.   :31.0  
##                                               
##     dep_time    sched_dep_time   dep_delay   
##  Min.   :   1   Min.   : 106   Min.   : -43  
##  1st Qu.: 907   1st Qu.: 906   1st Qu.:  -5  
##  Median :1401   Median :1359   Median :  -2  
##  Mean   :1349   Mean   :1344   Mean   :  13  
##  3rd Qu.:1744   3rd Qu.:1729   3rd Qu.:  11  
##  Max.   :2400   Max.   :2359   Max.   :1301  
##  NA's   :8255                  NA's   :8255  
##     arr_time    sched_arr_time   arr_delay   
##  Min.   :   1   Min.   :   1   Min.   : -86  
##  1st Qu.:1104   1st Qu.:1124   1st Qu.: -17  
##  Median :1535   Median :1556   Median :  -5  
##  Mean   :1502   Mean   :1536   Mean   :   7  
##  3rd Qu.:1940   3rd Qu.:1945   3rd Qu.:  14  
##  Max.   :2400   Max.   :2359   Max.   :1272  
##  NA's   :8713                  NA's   :9430  
##    carrier              flight       tailnum         
##  Length:336776      Min.   :   1   Length:336776     
##  Class :character   1st Qu.: 553   Class :character  
##  Mode  :character   Median :1496   Mode  :character  
##                     Mean   :1972                     
##                     3rd Qu.:3465                     
##                     Max.   :8500                     
##                                                      
##     origin              dest              air_time   
##  Length:336776      Length:336776      Min.   : 20   
##  Class :character   Class :character   1st Qu.: 82   
##  Mode  :character   Mode  :character   Median :129   
##                                        Mean   :151   
##                                        3rd Qu.:192   
##                                        Max.   :695   
##                                        NA's   :9430  
##     distance         hour          minute    
##  Min.   :  17   Min.   : 1.0   Min.   : 0.0  
##  1st Qu.: 502   1st Qu.: 9.0   1st Qu.: 8.0  
##  Median : 872   Median :13.0   Median :29.0  
##  Mean   :1040   Mean   :13.2   Mean   :26.2  
##  3rd Qu.:1389   3rd Qu.:17.0   3rd Qu.:44.0  
##  Max.   :4983   Max.   :23.0   Max.   :59.0  
##                                              
##    time_hour                  
##  Min.   :2013-01-01 05:00:00  
##  1st Qu.:2013-04-04 13:00:00  
##  Median :2013-07-03 10:00:00  
##  Mean   :2013-07-03 05:22:54  
##  3rd Qu.:2013-10-01 07:00:00  
##  Max.   :2013-12-31 23:00:00  
## 
```

dataset tersebut berisi 336.776 penerbangan yang berangkat dari New York pada tahun 2013. Data tersebut berasal dari *US Bureau of Transportation Statistics*. 

### filter()

Fungsi `filter()` digunakan untuk mengekstrak himpunan bagian (subset) baris dari data frame. Fungsi ini mirip dengan fungsi `subset()` yang ada di `R`. Secara sederhana format fungsi `filter()` dapat dituliskan sebagai berikut:


```r
filter(data, ....)
```

> **Note: **
>
> - **data** : data frame
> - **....** : Predikat logis didefinisikan dalam istilah variabel dalam **data**. Beberapa kondisi digabungkan dengan & (lihat Chapter 2 opeator relasi dan operator logika. Hanya baris tempat kondisi bernilai TRUE disimpan.

Visualisasi dari fungsi `filter()`disajikan pada Gambar \@ref(fig:filtervis)

\begin{figure}

{\centering \includegraphics{filtervis} 

}

\caption{Visualisasi fungsi filter (Sumber: Rstudio,2017)}(\#fig:filtervis)
\end{figure}

MIsalkan menggunakan dataset `flights` kita ingin mentehaui penerbangan apa saja yang berlangsung pada `month==1` dan `day==1` (1 Januari). Berikut adalah sintaks untuk memfilter datanya:


```r
filter(flights, month == 1 & day == 1)
```

```
## # A tibble: 842 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1      517            515         2
##  2  2013     1     1      533            529         4
##  3  2013     1     1      542            540         2
##  4  2013     1     1      544            545        -1
##  5  2013     1     1      554            600        -6
##  6  2013     1     1      554            558        -4
##  7  2013     1     1      555            600        -5
##  8  2013     1     1      557            600        -3
##  9  2013     1     1      557            600        -3
## 10  2013     1     1      558            600        -2
## # ... with 832 more rows, and 13 more variables:
## #   arr_time <int>, sched_arr_time <int>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   air_time <dbl>, distance <dbl>, hour <dbl>,
## #   minute <dbl>, time_hour <dttm>
```

Jika menggunakan paket dasar `R`:


```r
jan1 <- subset(flights, month == 1 & day == 1)
head(jan1, 10)
```

```
## # A tibble: 10 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1      517            515         2
##  2  2013     1     1      533            529         4
##  3  2013     1     1      542            540         2
##  4  2013     1     1      544            545        -1
##  5  2013     1     1      554            600        -6
##  6  2013     1     1      554            558        -4
##  7  2013     1     1      555            600        -5
##  8  2013     1     1      557            600        -3
##  9  2013     1     1      557            600        -3
## 10  2013     1     1      558            600        -2
## # ... with 13 more variables: arr_time <int>,
## #   sched_arr_time <int>, arr_delay <dbl>,
## #   carrier <chr>, flight <int>, tailnum <chr>,
## #   origin <chr>, dest <chr>, air_time <dbl>,
## #   distance <dbl>, hour <dbl>, minute <dbl>,
## #   time_hour <dttm>
```

Operator ">" merupakan operator relasi (lihat chapter 2: operator relasi). Operator tersebut banyak digunakan untuk melakukan filter terhadap variabel/kolom yang mengandung nilai numerik.

Operator "==" merupakan operator logika (lihat chapter 2: operator logika). Operator tersebut digunakan untuk melakukan filter terhadap sejumlah syarat atau kondisi yang kita tetapkan. Jika nilai yang dihasilkan TRUE, maka hanya observasi tersebut yang akan ditampilkan. Untuk lebih memahami penerapan masing-masing operator logika pada proses filter perhatikan Gambar \@ref(fig:filter) berikut:

\begin{figure}

{\centering \includegraphics{filter} 

}

\caption{Diagram operasi Boolean (Sumber: Wichham dan Grolemund, 2016)}(\#fig:filter)
\end{figure}

> **Note: ** Bagian yang di arsir adalah observasi yang akan ditampilkan pada output.

Salah satu bagian terpenting dan paling sering penulis gunakan pada fungsi ini memfilter *missing value* (melihat observasi yang mengandung *missing value* atau tidak melibatkan *missing value*). Berikut adalah contoh filter terhadap data pada  `flights` yang tidak mengandung *missing value*.


```r
flight_clean <- filter(flights,
                !(is.na(air_time)|is.na(arr_time)|
                    is.na(arr_delay)|
                    is.na(dep_time)|
                    is.na(dep_delay)))
summary(flight_clean)
```

Berdasarkan hasil yang diperoleh seluruh data tidak ada yang di drop sehingga dapat disimpulkan bahwa data tersebut tidak mengandung *missing value* dan nol.

Cara lain yang dapat digunakan adalah dengan mengunakan fungsi `drop_na()` dari library `tidyr`. Berikut adalah contoh sintaks yang digunakan:


```r
flight_clean <- drop_na(flights)
summary(flight_clean)
```

```
##       year          month            day      
##  Min.   :2013   Min.   : 1.00   Min.   : 1.0  
##  1st Qu.:2013   1st Qu.: 4.00   1st Qu.: 8.0  
##  Median :2013   Median : 7.00   Median :16.0  
##  Mean   :2013   Mean   : 6.57   Mean   :15.7  
##  3rd Qu.:2013   3rd Qu.:10.00   3rd Qu.:23.0  
##  Max.   :2013   Max.   :12.00   Max.   :31.0  
##     dep_time    sched_dep_time   dep_delay     
##  Min.   :   1   Min.   : 500   Min.   : -43.0  
##  1st Qu.: 907   1st Qu.: 905   1st Qu.:  -5.0  
##  Median :1400   Median :1355   Median :  -2.0  
##  Mean   :1349   Mean   :1340   Mean   :  12.6  
##  3rd Qu.:1744   3rd Qu.:1729   3rd Qu.:  11.0  
##  Max.   :2400   Max.   :2359   Max.   :1301.0  
##     arr_time    sched_arr_time   arr_delay     
##  Min.   :   1   Min.   :   1   Min.   : -86.0  
##  1st Qu.:1104   1st Qu.:1122   1st Qu.: -17.0  
##  Median :1535   Median :1554   Median :  -5.0  
##  Mean   :1502   Mean   :1533   Mean   :   6.9  
##  3rd Qu.:1940   3rd Qu.:1944   3rd Qu.:  14.0  
##  Max.   :2400   Max.   :2359   Max.   :1272.0  
##    carrier              flight       tailnum         
##  Length:327346      Min.   :   1   Length:327346     
##  Class :character   1st Qu.: 544   Class :character  
##  Mode  :character   Median :1467   Mode  :character  
##                     Mean   :1943                     
##                     3rd Qu.:3412                     
##                     Max.   :8500                     
##     origin              dest              air_time  
##  Length:327346      Length:327346      Min.   : 20  
##  Class :character   Class :character   1st Qu.: 82  
##  Mode  :character   Mode  :character   Median :129  
##                                        Mean   :151  
##                                        3rd Qu.:192  
##                                        Max.   :695  
##     distance         hour          minute    
##  Min.   :  80   Min.   : 5.0   Min.   : 0.0  
##  1st Qu.: 509   1st Qu.: 9.0   1st Qu.: 8.0  
##  Median : 888   Median :13.0   Median :29.0  
##  Mean   :1048   Mean   :13.1   Mean   :26.2  
##  3rd Qu.:1389   3rd Qu.:17.0   3rd Qu.:44.0  
##  Max.   :4983   Max.   :23.0   Max.   :59.0  
##    time_hour                  
##  Min.   :2013-01-01 05:00:00  
##  1st Qu.:2013-04-05 06:00:00  
##  Median :2013-07-04 09:00:00  
##  Mean   :2013-07-03 17:56:45  
##  3rd Qu.:2013-10-01 18:00:00  
##  Max.   :2013-12-31 23:00:00
```

#### Scope Filtering

*Scope filtering* menerapkan ekspresi predikat pada sejumlah variabel. Ekspresi predikat harus dikutip dengan `all_vars()` atau `any_vars()` dan harus menyebutkan kata ganti `.` untuk merujuk ke variabel. Fungsi-fungsi yang ada pada *scope filtering* dan formatnya disajikan pada sintaks berikut:


```r
filter_all(.tbl, .vars_predicate, .preserve = FALSE)

filter_if(.tbl, .predicate, .vars_predicate, .preserve = FALSE)

filter_at(.tbl, .vars, .vars_predicate, .preserve = FALSE)
```

> **Note: **
>
> - **.tbl**: tibble atau dataframe.
> - **.vars_predicate**: Ekspresi predikat yang dikutip seperti yang dikembalikan oleh `all_vars()` atau `any_vars()`. `all_vars()` melakukan filter seperti pada efek *intersect* (irisan himpunan), sedangkan  `any_vars()` melakukan filter seperti efek *union* (himpunan gabungan).
> - **.preserve**: ketika `FALSE` (default), struktur pengelompokan dihitung ulang berdasarkan data yang dihasilkan.
> - **.predicate**: fungsi predikat yang diaplikasikan pada kolom atau vektor logikal.
> - **.vars**: daftar kolom yang dihasilkan oleh `vars()`, vektor karakter dari nama kolom, vektor numerik dari posisi kolom, atau `NULL`.

Berikut adalahcontoh sintaks penerapan fungsi-fungsi tersebut:


```r
# filter seluruh kolom dan baris yang memiliki nilai sesuai
# mengambil irisan data
filter_all(flights, all_vars(. > 150))
```

```
## # A tibble: 0 x 19
## # ... with 19 variables: year <int>, month <int>,
## #   day <int>, dep_time <int>, sched_dep_time <int>,
## #   dep_delay <dbl>, arr_time <int>,
## #   sched_arr_time <int>, arr_delay <dbl>,
## #   carrier <chr>, flight <int>, tailnum <chr>,
## #   origin <chr>, dest <chr>, air_time <dbl>,
## #   distance <dbl>, hour <dbl>, minute <dbl>,
## #   time_hour <dttm>
```

```r
# mengambil himpunan gabungan data
filter_all(flights, any_vars(. > 150))
```

```
## # A tibble: 336,776 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1      517            515         2
##  2  2013     1     1      533            529         4
##  3  2013     1     1      542            540         2
##  4  2013     1     1      544            545        -1
##  5  2013     1     1      554            600        -6
##  6  2013     1     1      554            558        -4
##  7  2013     1     1      555            600        -5
##  8  2013     1     1      557            600        -3
##  9  2013     1     1      557            600        -3
## 10  2013     1     1      558            600        -2
## # ... with 336,766 more rows, and 13 more variables:
## #   arr_time <int>, sched_arr_time <int>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   air_time <dbl>, distance <dbl>, hour <dbl>,
## #   minute <dbl>, time_hour <dttm>
```

```r
# filter pada kolom tertentu berdasarkan spesifikasi 
# predikat var()

# filter kolom dengan awalan h atau 
# yang terdapat baris dengan nilai ganjil 
# pada variabel tersebut
filter_at(flights, 
          vars(starts_with("a")), 
          any_vars((. %% 2) == 1))
```

```
## # A tibble: 286,363 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1      517            515         2
##  2  2013     1     1      533            529         4
##  3  2013     1     1      542            540         2
##  4  2013     1     1      544            545        -1
##  5  2013     1     1      554            600        -6
##  6  2013     1     1      555            600        -5
##  7  2013     1     1      557            600        -3
##  8  2013     1     1      558            600        -2
##  9  2013     1     1      558            600        -2
## 10  2013     1     1      558            600        -2
## # ... with 286,353 more rows, and 13 more variables:
## #   arr_time <int>, sched_arr_time <int>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   air_time <dbl>, distance <dbl>, hour <dbl>,
## #   minute <dbl>, time_hour <dttm>
```

```r
# filter pada kolom hp dan vs dimana nilai kolom genap
filter_at(flights, vars(arr_time, arr_delay), ~.%%2==0)
```

```
## # A tibble: 82,790 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1      533            529         4
##  2  2013     1     1      544            545        -1
##  3  2013     1     1      554            558        -4
##  4  2013     1     1      557            600        -3
##  5  2013     1     1      559            559         0
##  6  2013     1     1      559            600        -1
##  7  2013     1     1      601            600         1
##  8  2013     1     1      602            610        -8
##  9  2013     1     1      606            610        -4
## 10  2013     1     1      624            630        -6
## # ... with 82,780 more rows, and 13 more variables:
## #   arr_time <int>, sched_arr_time <int>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   air_time <dbl>, distance <dbl>, hour <dbl>,
## #   minute <dbl>, time_hour <dttm>
```

```r
# filter dengan menerapkan kondisi tertentu
# filter seluruh variabel dengan observasi mengandung
# bilangan bulat dan tidak memiliki nilai 0
filter_if(flights[,16:17], ~ all(floor(.) == .), all_vars(. != 0))
```

```
## # A tibble: 336,776 x 2
##    distance  hour
##       <dbl> <dbl>
##  1     1400     5
##  2     1416     5
##  3     1089     5
##  4     1576     5
##  5      762     6
##  6      719     5
##  7     1065     6
##  8      229     6
##  9      944     6
## 10      733     6
## # ... with 336,766 more rows
```

> **Note: ** `filter_at()` dan `filter_if()` menghilangkan kolom yang tidak sesuai kriteria. Sedangkan `filter_all()` digunakan untuk memfilter baris.

#### Fungsi Lain Untuk Mengekstrak Observasi

Selain  fungsi `filter()` terdapat fungsi lain yang berguna dalam melakukan ekstrak data. Fungsi-fungsi tersebut antara lain:

1. `distinct()`: menghilangkan baris dengan nilai yang sama (*duplicate observation*).
2. `sample_frac()`: melakukan sampling sejumlah fraksi baris pada data. Fungsi ini berguna saat pembaca ingin melakukan sampling data yang cukup besar menggunakan besaran fraksi data.
3. `sample_n()`: sama dengan `sample_frac()`. Bedanya adalah kita perlu menyatakan berapa baris yang hendak kita sampling.
4. `slice()`: membuat irisan data. Berguna jika ingin membuat dataset baru berrdasarkan grup data atau membuat dataset dari sejumlah baris pada data.
5. `top_n()`: memilih data teratas (nilai tertinggi) yang telah diurutkan.

Berikut adalah contoh sintaks penerapan fungsi-fungsi tersebut:


```r
# menghilangkan baris dengan nilai
distinct(flights, tailnum)
```

```
## # A tibble: 4,044 x 1
##    tailnum
##    <chr>  
##  1 N14228 
##  2 N24211 
##  3 N619AA 
##  4 N804JB 
##  5 N668DN 
##  6 N39463 
##  7 N516JB 
##  8 N829AS 
##  9 N593JB 
## 10 N3ALAA 
## # ... with 4,034 more rows
```

```r
# Sampling dengan pengembalian secara acak 50% data
sample_frac(flights, 0.1, replace=TRUE)
```

```
## # A tibble: 33,678 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1    23      648            630        18
##  2  2013     9     5       NA           1930        NA
##  3  2013     6     7     1939           1800        99
##  4  2013     5     2      949            950        -1
##  5  2013     3     2      707            710        -3
##  6  2013    11    23     1605           1618       -13
##  7  2013    11    14     1729           1735        -6
##  8  2013    11    25     1843           1840         3
##  9  2013     5    23      956            855        61
## 10  2013     1     6     1651           1640        11
## # ... with 33,668 more rows, and 13 more variables:
## #   arr_time <int>, sched_arr_time <int>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   air_time <dbl>, distance <dbl>, hour <dbl>,
## #   minute <dbl>, time_hour <dttm>
```

```r
# sampling dengan pengembalian secara acak 10 observasi
sample_n(flights, 10, replace=TRUE)
```

```
## # A tibble: 10 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013    12     3     2045           2005        40
##  2  2013    12    11      736            745        -9
##  3  2013    12    19     1324           1326        -2
##  4  2013    11    16     1746           1755        -9
##  5  2013    10    18     1755           1659        56
##  6  2013     6    27      855            900        -5
##  7  2013     9    17      956           1000        -4
##  8  2013     2     6     1637           1645        -8
##  9  2013    10     2     1004           1005        -1
## 10  2013     4    23      826            835        -9
## # ... with 13 more variables: arr_time <int>,
## #   sched_arr_time <int>, arr_delay <dbl>,
## #   carrier <chr>, flight <int>, tailnum <chr>,
## #   origin <chr>, dest <chr>, air_time <dbl>,
## #   distance <dbl>, hour <dbl>, minute <dbl>,
## #   time_hour <dttm>
```

```r
# Pilih data dari baris ke 25 sampai 35
slice(flights, 25:35)
```

```
## # A tibble: 11 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1      607            607         0
##  2  2013     1     1      608            600         8
##  3  2013     1     1      611            600        11
##  4  2013     1     1      613            610         3
##  5  2013     1     1      615            615         0
##  6  2013     1     1      615            615         0
##  7  2013     1     1      622            630        -8
##  8  2013     1     1      623            610        13
##  9  2013     1     1      623            627        -4
## 10  2013     1     1      624            630        -6
## 11  2013     1     1      624            630        -6
## # ... with 13 more variables: arr_time <int>,
## #   sched_arr_time <int>, arr_delay <dbl>,
## #   carrier <chr>, flight <int>, tailnum <chr>,
## #   origin <chr>, dest <chr>, air_time <dbl>,
## #   distance <dbl>, hour <dbl>, minute <dbl>,
## #   time_hour <dttm>
```

```r
# 10 observasi dengan variabel Sepal.Width tertinggi
top_n(flights, 10, arr_time)
```

```
## # A tibble: 150 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1     2209           2155        14
##  2  2013     1     5     2116           2130       -14
##  3  2013     1    13     2243           2129        74
##  4  2013     1    16     2138           2107        31
##  5  2013     1    17     2256           2249         7
##  6  2013     1    22     2212           2055        77
##  7  2013     1    22     2249           2125        84
##  8  2013     1    25     2055           1725       210
##  9  2013     1    28     2303           2250        13
## 10  2013     1    30     2155           1915       160
## # ... with 140 more rows, and 13 more variables:
## #   arr_time <int>, sched_arr_time <int>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   air_time <dbl>, distance <dbl>, hour <dbl>,
## #   minute <dbl>, time_hour <dttm>
```

Untuk informasi lebih lanjut pembaca dapat mengakses menu bantuan dengan mengetikkan sintaks berikut:


```r
?<nama fungsi>
```


### arrange()

Fungsi `arrange()` bekerja mirip dengan fungsi `filter()` kecuali bahwa alih-alih memilih baris, fungsi ini mengubah urutan observasinya (mengurutkan dari yang terbesar atau sebaliknya). Dibutuhkan data frame dan sekumpulan nama kolom (atau ekspresi yang lebih rumit) untuk dipesan. Jika kita memberikan lebih dari satu nama kolom pada fungsi, setiap kolom tambahan akan digunakan untuk menentukan urutan nilai yang sama berdasarkan nilai kolom sebelumnya. 

Fungsi `arrange()` mirip dengan fungsi `order()` pada paket dasar `R`. Format sederhana fungsi ini adalah sebagai berikut:


```r
arrange(data, ....)
```

> **Note: **
>
> - **data** : data frame
> - **....** : daftar nama variabel yang tidak dikutip yang dipisahkan tanda koma, atau ekspresi yang melibatkan nama variabel. Gunakan `desc()` untuk mengurutkan variabel dalam urutan menurun.

Visualisasi dari fungsi `arrange()`disajikan pada Gambar \@ref(fig:arrange)

\begin{figure}

{\centering \includegraphics{arrange} 

}

\caption{Visualisasi fungsi arrange (Sumber: Rstudio,2017)}(\#fig:arrange)
\end{figure}

Misalkan kita ingin mengurutkan penerbangan berdasarkan variabel `year`, `month`, dan `day`. `R` akan melakukan pengurutan berdasarkan `year` terlebih dahulu. Jika ditemukan nilai yang seimbang, maka pengurutan dilakukan oleh variabel berikutnya. Berikut adalah sintaks yang digunakan:


```r
arrange(flights, year, month, day)
```

```
## # A tibble: 336,776 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1      517            515         2
##  2  2013     1     1      533            529         4
##  3  2013     1     1      542            540         2
##  4  2013     1     1      544            545        -1
##  5  2013     1     1      554            600        -6
##  6  2013     1     1      554            558        -4
##  7  2013     1     1      555            600        -5
##  8  2013     1     1      557            600        -3
##  9  2013     1     1      557            600        -3
## 10  2013     1     1      558            600        -2
## # ... with 336,766 more rows, and 13 more variables:
## #   arr_time <int>, sched_arr_time <int>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   air_time <dbl>, distance <dbl>, hour <dbl>,
## #   minute <dbl>, time_hour <dttm>
```

Jika ingin urutan yang digunakan adalah dari yang terbesar ke terkecil untuk ketiga variabel tersebut jalankan sintaks berikut:


```r
arrange(flights, desc(year, month, day))
```

```
## # A tibble: 336,776 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1      517            515         2
##  2  2013     1     1      533            529         4
##  3  2013     1     1      542            540         2
##  4  2013     1     1      544            545        -1
##  5  2013     1     1      554            600        -6
##  6  2013     1     1      554            558        -4
##  7  2013     1     1      555            600        -5
##  8  2013     1     1      557            600        -3
##  9  2013     1     1      557            600        -3
## 10  2013     1     1      558            600        -2
## # ... with 336,766 more rows, and 13 more variables:
## #   arr_time <int>, sched_arr_time <int>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   air_time <dbl>, distance <dbl>, hour <dbl>,
## #   minute <dbl>, time_hour <dttm>
```

Jika menggunakan fungsi `order()`:


```r
attach(flights)
# urutan dari kecil ke besar
flights[order(year, month, day), ]
```

```
## # A tibble: 336,776 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1      517            515         2
##  2  2013     1     1      533            529         4
##  3  2013     1     1      542            540         2
##  4  2013     1     1      544            545        -1
##  5  2013     1     1      554            600        -6
##  6  2013     1     1      554            558        -4
##  7  2013     1     1      555            600        -5
##  8  2013     1     1      557            600        -3
##  9  2013     1     1      557            600        -3
## 10  2013     1     1      558            600        -2
## # ... with 336,766 more rows, and 13 more variables:
## #   arr_time <int>, sched_arr_time <int>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   air_time <dbl>, distance <dbl>, hour <dbl>,
## #   minute <dbl>, time_hour <dttm>
```

```r
# urutan dari besar ke kecil
flights[order(-year, -month, -day), ]
```

```
## # A tibble: 336,776 x 19
##     year month   day dep_time sched_dep_time dep_delay
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013    12    31       13           2359        14
##  2  2013    12    31       18           2359        19
##  3  2013    12    31       26           2245       101
##  4  2013    12    31      459            500        -1
##  5  2013    12    31      514            515        -1
##  6  2013    12    31      549            551        -2
##  7  2013    12    31      550            600       -10
##  8  2013    12    31      552            600        -8
##  9  2013    12    31      553            600        -7
## 10  2013    12    31      554            550         4
## # ... with 336,766 more rows, and 13 more variables:
## #   arr_time <int>, sched_arr_time <int>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   air_time <dbl>, distance <dbl>, hour <dbl>,
## #   minute <dbl>, time_hour <dttm>
```

> **Note: ** *missing value* akan selalu diurutkan pada observasi terakhir baik menggunakan urutan dari terbesar ke terkecil maupun sebaliknya.

### select()

Fungsi `select()` dapat digunakan untuk memilih kolom dari data frame yang ingin kita fokuskan. Seringkali kita memiliki data frame yang besar yang berisi semua data, tetapi setiap analisis yang diberikan hanya menggunakan subset variabel atau pengamatan. Fungsi `select()` memungkinkan kita untuk mendapatkan beberapa kolom yang mungkin kita butuhkan.

Fungsi `select()` memiliki kesamaan dengan subset menggunakan tanda "[" dan "$". Perbedaanya adalah kita dapat melakukan hal lebih melalui fungsi ini seperti memilih berdasarkan kriteria tertentu menggunakan fungsi bantuan sebagai berikut:

1. `starts_with("abcd")`, pilih kolom yang memiliki awalan "abcd".
2. `end_with("abcd")`, pilih kolom yang memiliki akhiran "abcd".
3. `contains("abcd")`, pilih kolom yang mengandung nama "abcd"
4. `matches("(.)\\1")`, pilih variabel yang mengandung *regular expression*. Fungsi ini memilih variabel yang mengandung perulangan karakter.
5. `num_range("x", 1:3)`, cocokkan berdasarkan kolom dengan nama x1,x2,x3.

Berdasarkan fungsi bantuan tersebut, fungsi `select()` lebih powerfull dibandingkan dengan cara subset biasa serta lebih mudah dalam melakukannya. Berikut adalah format dari fungsi `select()`:


```r
select(data, ....)
```

> **Note: **
>
> - **data** : data frame
> - **....** : Satu atau lebih ekspresi kutip yang dipisahkan oleh koma. kita dapat memperlakukan nama variabel seperti posisi, sehingga kita dapat menggunakan ekspresi seperti x: y untuk memilih rentang variabel.Nilai positif pilih variabel; nilai negatif drop variabel. Jika ekspresi pertama negatif, `select()` akan secara otomatis dimulai dengan semua variabel. Gunakan argumen bernama, mis. `new_name = old_name`, untuk mengganti nama variabel yang dipilih.

Visualisasi dari fungsi `select()`disajikan pada Gambar \@ref(fig:select)

\begin{figure}

{\centering \includegraphics{select} 

}

\caption{Visualisasi fungsi select (Sumber: Rstudio,2017)}(\#fig:select)
\end{figure}

Berikut adalah contoh penerapan `select()` pada data frame `flights`.


```r
# pilih kolom berdasarkan nama kolom
select(flights, year, month, day)
```

```
## # A tibble: 336,776 x 3
##     year month   day
##    <int> <int> <int>
##  1  2013     1     1
##  2  2013     1     1
##  3  2013     1     1
##  4  2013     1     1
##  5  2013     1     1
##  6  2013     1     1
##  7  2013     1     1
##  8  2013     1     1
##  9  2013     1     1
## 10  2013     1     1
## # ... with 336,766 more rows
```

```r
# pilih seluruh kolom dari year sampai day
select(flights, year:day)
```

```
## # A tibble: 336,776 x 3
##     year month   day
##    <int> <int> <int>
##  1  2013     1     1
##  2  2013     1     1
##  3  2013     1     1
##  4  2013     1     1
##  5  2013     1     1
##  6  2013     1     1
##  7  2013     1     1
##  8  2013     1     1
##  9  2013     1     1
## 10  2013     1     1
## # ... with 336,766 more rows
```

```r
# drop kolom dari year sampai day
select(flights, -(year:day))
```

```
## # A tibble: 336,776 x 16
##    dep_time sched_dep_time dep_delay arr_time
##       <int>          <int>     <dbl>    <int>
##  1      517            515         2      830
##  2      533            529         4      850
##  3      542            540         2      923
##  4      544            545        -1     1004
##  5      554            600        -6      812
##  6      554            558        -4      740
##  7      555            600        -5      913
##  8      557            600        -3      709
##  9      557            600        -3      838
## 10      558            600        -2      753
## # ... with 336,766 more rows, and 12 more variables:
## #   sched_arr_time <int>, arr_delay <dbl>,
## #   carrier <chr>, flight <int>, tailnum <chr>,
## #   origin <chr>, dest <chr>, air_time <dbl>,
## #   distance <dbl>, hour <dbl>, minute <dbl>,
## #   time_hour <dttm>
```

```r
# pilih kolom dengan akhiran time
select(flights, ends_with("time"))
```

```
## # A tibble: 336,776 x 5
##    dep_time sched_dep_time arr_time sched_arr_time
##       <int>          <int>    <int>          <int>
##  1      517            515      830            819
##  2      533            529      850            830
##  3      542            540      923            850
##  4      544            545     1004           1022
##  5      554            600      812            837
##  6      554            558      740            728
##  7      555            600      913            854
##  8      557            600      709            723
##  9      557            600      838            846
## 10      558            600      753            745
## # ... with 336,766 more rows, and 1 more variable:
## #   air_time <dbl>
```

```r
# pilih kolom yang mengandung karakter "arr"
select(flights, contains("arr"))
```

```
## # A tibble: 336,776 x 4
##    arr_time sched_arr_time arr_delay carrier
##       <int>          <int>     <dbl> <chr>  
##  1      830            819        11 UA     
##  2      850            830        20 UA     
##  3      923            850        33 AA     
##  4     1004           1022       -18 B6     
##  5      812            837       -25 DL     
##  6      740            728        12 UA     
##  7      913            854        19 B6     
##  8      709            723       -14 EV     
##  9      838            846        -8 B6     
## 10      753            745         8 AA     
## # ... with 336,766 more rows
```

Kita juga dapat menggunakan fungsi tambahan `everything()` yang berguna jika kita ingin memindahkan variabel yang menjadi fokus kita ke awal data frame tanpa melakukan drop variabel. Berikut adalah contoh sintaksnya:


```r
# pindahkan kolom yang mengandung time di awal
select(flights, contains("time"), everything())
```

```
## # A tibble: 336,776 x 19
##    dep_time sched_dep_time arr_time sched_arr_time
##       <int>          <int>    <int>          <int>
##  1      517            515      830            819
##  2      533            529      850            830
##  3      542            540      923            850
##  4      544            545     1004           1022
##  5      554            600      812            837
##  6      554            558      740            728
##  7      555            600      913            854
##  8      557            600      709            723
##  9      557            600      838            846
## 10      558            600      753            745
## # ... with 336,766 more rows, and 15 more variables:
## #   air_time <dbl>, time_hour <dttm>, year <int>,
## #   month <int>, day <int>, dep_delay <dbl>,
## #   arr_delay <dbl>, carrier <chr>, flight <int>,
## #   tailnum <chr>, origin <chr>, dest <chr>,
## #   distance <dbl>, hour <dbl>, minute <dbl>
```

#### Scope Varian dari Fungsi Select

Terdapat 3 fungsi scope varian yang digunakan pada select, yaitu:

1. `select_all()`: memilih seluruh kolom dan mengaplikasikan fungsi pada nama kolom (merubah nama, merubah besar kecil huruf, dll).
2. `select_if()`: memilih kolom sesuai kondisi yang diinginkan serta dapat mengaplikasikan fungsi pada nama kolom.
3. `select_at()`: memilih kolom sesuai nama kolom atau index yang diinputkan pada `var()` dan dapat mengaplikasikan fungsi pada nama kolom.

Berikut adalah format dari fungsi-fungsi tersebut:


```r
select_all(.tbl, .funs = list(), ...)

select_if(.tbl, .predicate, .funs = list(), ...)

select_at(.tbl, .vars, .funs = list(), ...)
```

> **Note: **
>
> - **.tbl**: tibble atau dataframe
> - **.funs**: fungsi yang akan diaplikasikan.
> - **...**: argumen tambahan fungsi.
> - **.predicate**: fungsi predikat yang akan diaplikasikan pada kolom.
> - **.vars**: daftar kolom yang dibuat oleh fungsi `vars()`.

Berikut adalah contoh sintaks fungsi-fungsi tersebut:


```r
# pilih seluruh kolom dan ubah huruf kolom 
# menjadi huruf kapital
select_all(flights, toupper)
```

```
## # A tibble: 336,776 x 19
##     YEAR MONTH   DAY DEP_TIME SCHED_DEP_TIME DEP_DELAY
##    <int> <int> <int>    <int>          <int>     <dbl>
##  1  2013     1     1      517            515         2
##  2  2013     1     1      533            529         4
##  3  2013     1     1      542            540         2
##  4  2013     1     1      544            545        -1
##  5  2013     1     1      554            600        -6
##  6  2013     1     1      554            558        -4
##  7  2013     1     1      555            600        -5
##  8  2013     1     1      557            600        -3
##  9  2013     1     1      557            600        -3
## 10  2013     1     1      558            600        -2
## # ... with 336,766 more rows, and 13 more variables:
## #   ARR_TIME <int>, SCHED_ARR_TIME <int>,
## #   ARR_DELAY <dbl>, CARRIER <chr>, FLIGHT <int>,
## #   TAILNUM <chr>, ORIGIN <chr>, DEST <chr>,
## #   AIR_TIME <dbl>, DISTANCE <dbl>, HOUR <dbl>,
## #   MINUTE <dbl>, TIME_HOUR <dttm>
```

```r
# pilih kolom berdasarkan if then condition
# dan ubah nama kolom terpilih menjadi huruf kapital
select_if(flights, ~is_character(.), toupper)
```

```
## # A tibble: 336,776 x 4
##    CARRIER TAILNUM ORIGIN DEST 
##    <chr>   <chr>   <chr>  <chr>
##  1 UA      N14228  EWR    IAH  
##  2 UA      N24211  LGA    IAH  
##  3 AA      N619AA  JFK    MIA  
##  4 B6      N804JB  JFK    BQN  
##  5 DL      N668DN  LGA    ATL  
##  6 UA      N39463  EWR    ORD  
##  7 B6      N516JB  EWR    FLL  
##  8 EV      N829AS  LGA    IAD  
##  9 B6      N593JB  JFK    MCO  
## 10 AA      N3ALAA  LGA    ORD  
## # ... with 336,766 more rows
```

```r
# pilih beberapa kolom dan ubah nama kolom menjadi huruf besar.
select_at(flights, vars(contains("time")), toupper)
```

```
## # A tibble: 336,776 x 6
##    DEP_TIME SCHED_DEP_TIME ARR_TIME SCHED_ARR_TIME
##       <int>          <int>    <int>          <int>
##  1      517            515      830            819
##  2      533            529      850            830
##  3      542            540      923            850
##  4      544            545     1004           1022
##  5      554            600      812            837
##  6      554            558      740            728
##  7      555            600      913            854
##  8      557            600      709            723
##  9      557            600      838            846
## 10      558            600      753            745
## # ... with 336,766 more rows, and 2 more variables:
## #   AIR_TIME <dbl>, TIME_HOUR <dttm>
```

#### Fungsi Pull Untuk Mengambil Nilai Pada Kolom

Fungsi `pull()` digunakan untuk mengambil nilai pada variabel. Output yang dihasilkan berupa vektor. Fungsi ini mirip dengan subseting menggunakan "$" (*dolar sign*) atau "[[" (*double square brackets*). Berikut adalah format fungsi tersebut:


```r
pull(.data, var = -1)
```

> **Note: **
>
> - **.data**: tibble atau dataframe.
> - **var**: nama variabel atau indeks. Untuk indeks positif, tabel akan dibaca dari kanan. Jika negatif akan dibaca dari kiri.

Visualisasi dari fungsi `pull()`disajikan pada Gambar \@ref(fig:pull)

\begin{figure}

{\centering \includegraphics{pull} 

}

\caption{Visualisasi fungsi pull (Sumber: Rstudio,2017)}(\#fig:pull)
\end{figure}

Berikut adalah contoh sintaks menggunakan fungsi `pull()`:


```r
# menggunakan fungsi pull
pull(mtcars, mpg)
```

```
##  [1] 21.0 21.0 22.8 21.4 18.7 18.1 14.3 24.4 22.8 19.2
## [11] 17.8 16.4 17.3 15.2 10.4 10.4 14.7 32.4 30.4 33.9
## [21] 21.5 15.5 15.2 13.3 19.2 27.3 26.0 30.4 15.8 19.7
## [31] 15.0 21.4
```

```r
# menggunakan fungsi dasar
mtcars[["mpg"]]
```

```
##  [1] 21.0 21.0 22.8 21.4 18.7 18.1 14.3 24.4 22.8 19.2
## [11] 17.8 16.4 17.3 15.2 10.4 10.4 14.7 32.4 30.4 33.9
## [21] 21.5 15.5 15.2 13.3 19.2 27.3 26.0 30.4 15.8 19.7
## [31] 15.0 21.4
```

### mutate()

Fungsi `mutate()` digunakan untuk melakukan transformasi variabel dalam data frame. Seringkali, kita ingin membuat variabel baru yang berasal dari variabel yang ada dan fungsi `mutate()` menyediakan antarmuka yang bersih untuk melakukan itu. Format yang digunakan adalah sebagai berikut:


```r
mutate(data, ....)
```

> **Note: **
>
> - **data** : data frame
> - **....** : Pasangan nama-nilai ekspresi, masing-masing dengan panjang 1 atau panjang yang sama dengan jumlah baris dalam grup (jika menggunakan group_by ()) atau di seluruh input (jika tidak menggunakan grup). Nama setiap argumen akan menjadi nama variabel baru, dan nilainya akan menjadi nilai yang sesuai. Gunakan nilai NULL dalam mutasi untuk menjatuhkan drop variabel lama, sehingga variabel baru menimpa variabel yang ada dengan nama yang sama.


```r
# subset data frame
flights_sml <- select(flights,
  year:day,
  ends_with("delay"),
  distance,
  air_time
)

# mutate()
mutate(flights_sml,
  gain = arr_delay - dep_delay,
  hours = air_time / 60,
  gain_per_hour = gain / hours
)
```

```
## # A tibble: 336,776 x 10
##     year month   day dep_delay arr_delay distance
##    <int> <int> <int>     <dbl>     <dbl>    <dbl>
##  1  2013     1     1         2        11     1400
##  2  2013     1     1         4        20     1416
##  3  2013     1     1         2        33     1089
##  4  2013     1     1        -1       -18     1576
##  5  2013     1     1        -6       -25      762
##  6  2013     1     1        -4        12      719
##  7  2013     1     1        -5        19     1065
##  8  2013     1     1        -3       -14      229
##  9  2013     1     1        -3        -8      944
## 10  2013     1     1        -2         8      733
## # ... with 336,766 more rows, and 4 more variables:
## #   air_time <dbl>, gain <dbl>, hours <dbl>,
## #   gain_per_hour <dbl>
```

Jika hanya ingin menyisakan variabel output fungsi `mutate()` pada data frame (variabel lain di drop), kita dapat menggunakan fungsi `transmute()`. Berikut adalah contoh sintaks yang digunakan:


```r
transmute(flights,
  gain = arr_delay - dep_delay,
  hours = air_time / 60,
  gain_per_hour = gain / hours
)
```

```
## # A tibble: 336,776 x 3
##     gain hours gain_per_hour
##    <dbl> <dbl>         <dbl>
##  1     9 3.78           2.38
##  2    16 3.78           4.23
##  3    31 2.67          11.6 
##  4   -17 3.05          -5.57
##  5   -19 1.93          -9.83
##  6    16 2.5            6.4 
##  7    24 2.63           9.11
##  8   -11 0.883        -12.5 
##  9    -5 2.33          -2.14
## 10    10 2.3            4.35
## # ... with 336,766 more rows
```

Adapaun fungsi-fungsi dan operator yang dapat digunakan pada `mutate()` untuk membuat variabel baru adalah sebagai berikut:

1. **Operator aritmatik** (+,-,*,/,^, %/%, %%). operator aritmetik seperti %/% dan %% sangat berguna dalam memecah integer menjadi beberapa bagian seperti hasil bagi tanpa sisa (%/%) dan sisa hasil bagi (%%). Berikut adalah contoh penerapannya:


```r
transmute(flights,
  dep_time,
  hour = dep_time %/% 100,
  minute = dep_time %% 100
)
```

```
## # A tibble: 336,776 x 3
##    dep_time  hour minute
##       <int> <dbl>  <dbl>
##  1      517     5     17
##  2      533     5     33
##  3      542     5     42
##  4      544     5     44
##  5      554     5     54
##  6      554     5     54
##  7      555     5     55
##  8      557     5     57
##  9      557     5     57
## 10      558     5     58
## # ... with 336,766 more rows
```

2. **Fungsi aritmetik** (`log()`,`sin()`,`cos()`,dll)
3. **Fungsi Offsets** (`lead()`dan `lag()`). memungkinkan kita untuk merujuk pada nilai-nilai memimpin atau tertinggal. Berikut adalah contoh penerapannya:


```r
(x <- 1:10)
```

```
##  [1]  1  2  3  4  5  6  7  8  9 10
```

```r
lag(x)
```

```
##  [1] NA  1  2  3  4  5  6  7  8  9
```

```r
lead(x)
```

```
##  [1]  2  3  4  5  6  7  8  9 10 NA
```

4. **Fungsi kumulatif** (`cumsum()`,`cumprod()`,`cummin()`,`cummax()`, dan `cummean()`). Jika kita membutuhkan agregat bergulir (mis., Jumlah yang dihitung di atas jendela bergulir). Berikut adalah contoh penerapannya:


```r
x
```

```
##  [1]  1  2  3  4  5  6  7  8  9 10
```

```r
cumsum(x)
```

```
##  [1]  1  3  6 10 15 21 28 36 45 55
```

```r
cummean(x)
```

```
##  [1] 1.0 1.5 2.0 2.5 3.0 3.5 4.0 4.5 5.0 5.5
```

5. **Operator logik** (<, <=, >, >=, !=). Jika kita melakukan urutan operasi logis yang kompleks, seringkali ide yang baik untuk menyimpan nilai sementara dalam variabel baru sehingga kita dapat memeriksa bahwa setiap langkah berfungsi seperti yang diharapkan.

6. Rangking (`min_rank()`, `row_number()`, `dense_rank()`, `percent_rank()`, `cume_dist()`dan `ntile()`).

#### Scope Variant Fungsi Mutate dan Transmute

**Scope variants** dari fungsi `mutate()` dan `transmute` berfungsi melakukan transformasi yang sama terhadap beberapa variabel. Terdapat tiga varaian umum dari fungsi-fungsinya, antara lain:

1. `_all`:bekerja pada seluruh variabel.
2. `_at`: bekerja pada variabel terpilih melalui vektor numerik atau string.
3. `_if`: berkeja pada variabel terpilih melalui fungsi predikat.

Berikut adalah format fungsi-fungsi tersebut:


```r
mutate_all(.tbl, .funs, ...)

mutate_if(.tbl, .predicate, .funs, ...)

mutate_at(.tbl, .vars, .funs, ...)

transmute_all(.tbl, .funs, ...)

transmute_if(.tbl, .predicate, .funs, ...)

transmute_at(.tbl, .vars, .funs, ...)
```

> **Note: **
>
> - **.tbl**: tibble atau dataframe.
> - **.funs**: fungsi yang diaplikasikan.
> - **...**: argumen tambahan pada fungsi.
> - **.predicate**: fungsi predikat yang diaplikasikan pada kolom.
> - **.vars**: daftra kolom yang dibuat menggunakan fungsi `vars()`.

Berikut adalah contoh sintaks dari fungsi-fungsi tersebut:


```r
# melakukan standarisasi variabel numerik
# fungsi standarisasi
scale2 <- function(x, na.rm = FALSE) (x - mean(x, na.rm = na.rm)) / sd(x, na.rm)

# standarisasi variabel dataset mtcars
mutate_all(mtcars, scale2)
```

```
##         mpg    cyl     disp       hp     drat       wt
## 1   0.15088 -0.105 -0.57062 -0.53509  0.56751 -0.61040
## 2   0.15088 -0.105 -0.57062 -0.53509  0.56751 -0.34979
## 3   0.44954 -1.225 -0.99018 -0.78304  0.47400 -0.91700
## 4   0.21725 -0.105  0.22009 -0.53509 -0.96612 -0.00230
## 5  -0.23073  1.015  1.04308  0.41294 -0.83520  0.22765
## 6  -0.33029 -0.105 -0.04617 -0.60802 -1.56461  0.24809
## 7  -0.96079  1.015  1.04308  1.43390 -0.72298  0.36052
## 8   0.71502 -1.225 -0.67793 -1.23518  0.17475 -0.02785
## 9   0.44954 -1.225 -0.72554 -0.75387  0.60492 -0.06873
## 10 -0.14777 -0.105 -0.50930 -0.34549  0.60492  0.22765
## 11 -0.38006 -0.105 -0.50930 -0.34549  0.60492  0.22765
## 12 -0.61235  1.015  0.36371  0.48587 -0.98482  0.87152
## 13 -0.46302  1.015  0.36371  0.48587 -0.98482  0.52404
## 14 -0.81146  1.015  0.36371  0.48587 -0.98482  0.57514
## 15 -1.60788  1.015  1.94675  0.85050 -1.24666  2.07750
## 16 -1.60788  1.015  1.84993  0.99635 -1.11574  2.25534
## 17 -0.89442  1.015  1.68856  1.21513 -0.68558  2.17460
## 18  2.04239 -1.225 -1.22659 -1.17684  0.90416 -1.03965
## 19  1.71055 -1.225 -1.25079 -1.38103  2.49390 -1.63753
## 20  2.29127 -1.225 -1.28791 -1.19142  1.16600 -1.41268
## 21  0.23385 -1.225 -0.89255 -0.72470  0.19346 -0.76881
## 22 -0.76168  1.015  0.70420  0.04831 -1.56461  0.30942
## 23 -0.81146  1.015  0.59124  0.04831 -0.83520  0.22254
## 24 -1.12671  1.015  0.96240  1.43390  0.24957  0.63646
## 25 -0.14777  1.015  1.36582  0.41294 -0.96612  0.64157
## 26  1.19619 -1.225 -1.22417 -1.17684  0.90416 -1.31048
## 27  0.98049 -1.225 -0.89094 -0.81221  1.55876 -1.10097
## 28  1.71055 -1.225 -1.09427 -0.49134  0.32438 -1.74177
## 29 -0.71191  1.015  0.97046  1.71102  1.16600 -0.04829
## 30 -0.06481 -0.105 -0.69165  0.41294  0.04383 -0.45710
## 31 -0.84464  1.015  0.56704  2.74657 -0.10579  0.36052
## 32  0.21725 -1.225 -0.88529 -0.54968  0.96027 -0.44688
##        qsec     vs      am    gear    carb
## 1  -0.77717 -0.868  1.1899  0.4236  0.7352
## 2  -0.46378 -0.868  1.1899  0.4236  0.7352
## 3   0.42601  1.116  1.1899  0.4236 -1.1222
## 4   0.89049  1.116 -0.8141 -0.9318 -1.1222
## 5  -0.46378 -0.868 -0.8141 -0.9318 -0.5030
## 6   1.32699  1.116 -0.8141 -0.9318 -1.1222
## 7  -1.12413 -0.868 -0.8141 -0.9318  0.7352
## 8   1.20387  1.116 -0.8141  0.4236 -0.5030
## 9   2.82675  1.116 -0.8141  0.4236 -0.5030
## 10  0.25253  1.116 -0.8141  0.4236  0.7352
## 11  0.58830  1.116 -0.8141  0.4236  0.7352
## 12 -0.25113 -0.868 -0.8141 -0.9318  0.1161
## 13 -0.13920 -0.868 -0.8141 -0.9318  0.1161
## 14  0.08464 -0.868 -0.8141 -0.9318  0.1161
## 15  0.07345 -0.868 -0.8141 -0.9318  0.7352
## 16 -0.01609 -0.868 -0.8141 -0.9318  0.7352
## 17 -0.23993 -0.868 -0.8141 -0.9318  0.7352
## 18  0.90728  1.116  1.1899  0.4236 -1.1222
## 19  0.37564  1.116  1.1899  0.4236 -0.5030
## 20  1.14791  1.116  1.1899  0.4236 -1.1222
## 21  1.20947  1.116 -0.8141 -0.9318 -1.1222
## 22 -0.54772 -0.868 -0.8141 -0.9318 -0.5030
## 23 -0.30709 -0.868 -0.8141 -0.9318 -0.5030
## 24 -1.36476 -0.868 -0.8141 -0.9318  0.7352
## 25 -0.44699 -0.868 -0.8141 -0.9318 -0.5030
## 26  0.58830  1.116  1.1899  0.4236 -1.1222
## 27 -0.64286 -0.868  1.1899  1.7789 -0.5030
## 28 -0.53093  1.116  1.1899  1.7789 -0.5030
## 29 -1.87401 -0.868  1.1899  1.7789  0.7352
## 30 -1.31440 -0.868  1.1899  1.7789  1.9734
## 31 -1.81805 -0.868  1.1899  1.7789  3.2117
## 32  0.42041  1.116  1.1899  0.4236 -0.5030
```

```r
# standarisasi variabel mpg dan hp
mutate_at(mtcars, vars(mpg,hp), scale2)
```

```
##         mpg cyl  disp       hp drat    wt  qsec vs am
## 1   0.15088   6 160.0 -0.53509 3.90 2.620 16.46  0  1
## 2   0.15088   6 160.0 -0.53509 3.90 2.875 17.02  0  1
## 3   0.44954   4 108.0 -0.78304 3.85 2.320 18.61  1  1
## 4   0.21725   6 258.0 -0.53509 3.08 3.215 19.44  1  0
## 5  -0.23073   8 360.0  0.41294 3.15 3.440 17.02  0  0
## 6  -0.33029   6 225.0 -0.60802 2.76 3.460 20.22  1  0
## 7  -0.96079   8 360.0  1.43390 3.21 3.570 15.84  0  0
## 8   0.71502   4 146.7 -1.23518 3.69 3.190 20.00  1  0
## 9   0.44954   4 140.8 -0.75387 3.92 3.150 22.90  1  0
## 10 -0.14777   6 167.6 -0.34549 3.92 3.440 18.30  1  0
## 11 -0.38006   6 167.6 -0.34549 3.92 3.440 18.90  1  0
## 12 -0.61235   8 275.8  0.48587 3.07 4.070 17.40  0  0
## 13 -0.46302   8 275.8  0.48587 3.07 3.730 17.60  0  0
## 14 -0.81146   8 275.8  0.48587 3.07 3.780 18.00  0  0
## 15 -1.60788   8 472.0  0.85050 2.93 5.250 17.98  0  0
## 16 -1.60788   8 460.0  0.99635 3.00 5.424 17.82  0  0
## 17 -0.89442   8 440.0  1.21513 3.23 5.345 17.42  0  0
## 18  2.04239   4  78.7 -1.17684 4.08 2.200 19.47  1  1
## 19  1.71055   4  75.7 -1.38103 4.93 1.615 18.52  1  1
## 20  2.29127   4  71.1 -1.19142 4.22 1.835 19.90  1  1
## 21  0.23385   4 120.1 -0.72470 3.70 2.465 20.01  1  0
## 22 -0.76168   8 318.0  0.04831 2.76 3.520 16.87  0  0
## 23 -0.81146   8 304.0  0.04831 3.15 3.435 17.30  0  0
## 24 -1.12671   8 350.0  1.43390 3.73 3.840 15.41  0  0
## 25 -0.14777   8 400.0  0.41294 3.08 3.845 17.05  0  0
## 26  1.19619   4  79.0 -1.17684 4.08 1.935 18.90  1  1
## 27  0.98049   4 120.3 -0.81221 4.43 2.140 16.70  0  1
## 28  1.71055   4  95.1 -0.49134 3.77 1.513 16.90  1  1
## 29 -0.71191   8 351.0  1.71102 4.22 3.170 14.50  0  1
## 30 -0.06481   6 145.0  0.41294 3.62 2.770 15.50  0  1
## 31 -0.84464   8 301.0  2.74657 3.54 3.570 14.60  0  1
## 32  0.21725   4 121.0 -0.54968 4.11 2.780 18.60  1  1
##    gear carb
## 1     4    4
## 2     4    4
## 3     4    1
## 4     3    1
## 5     3    2
## 6     3    1
## 7     3    4
## 8     4    2
## 9     4    2
## 10    4    4
## 11    4    4
## 12    3    3
## 13    3    3
## 14    3    3
## 15    3    4
## 16    3    4
## 17    3    4
## 18    4    1
## 19    4    2
## 20    4    1
## 21    3    1
## 22    3    2
## 23    3    2
## 24    3    4
## 25    3    2
## 26    4    1
## 27    5    2
## 28    5    2
## 29    5    4
## 30    5    6
## 31    5    8
## 32    4    2
```

```r
# standarisasi hanya pada variabel numerik
mutate_if(mtcars, is_numeric, scale2)
```

```
##         mpg    cyl     disp       hp     drat       wt
## 1   0.15088 -0.105 -0.57062 -0.53509  0.56751 -0.61040
## 2   0.15088 -0.105 -0.57062 -0.53509  0.56751 -0.34979
## 3   0.44954 -1.225 -0.99018 -0.78304  0.47400 -0.91700
## 4   0.21725 -0.105  0.22009 -0.53509 -0.96612 -0.00230
## 5  -0.23073  1.015  1.04308  0.41294 -0.83520  0.22765
## 6  -0.33029 -0.105 -0.04617 -0.60802 -1.56461  0.24809
## 7  -0.96079  1.015  1.04308  1.43390 -0.72298  0.36052
## 8   0.71502 -1.225 -0.67793 -1.23518  0.17475 -0.02785
## 9   0.44954 -1.225 -0.72554 -0.75387  0.60492 -0.06873
## 10 -0.14777 -0.105 -0.50930 -0.34549  0.60492  0.22765
## 11 -0.38006 -0.105 -0.50930 -0.34549  0.60492  0.22765
## 12 -0.61235  1.015  0.36371  0.48587 -0.98482  0.87152
## 13 -0.46302  1.015  0.36371  0.48587 -0.98482  0.52404
## 14 -0.81146  1.015  0.36371  0.48587 -0.98482  0.57514
## 15 -1.60788  1.015  1.94675  0.85050 -1.24666  2.07750
## 16 -1.60788  1.015  1.84993  0.99635 -1.11574  2.25534
## 17 -0.89442  1.015  1.68856  1.21513 -0.68558  2.17460
## 18  2.04239 -1.225 -1.22659 -1.17684  0.90416 -1.03965
## 19  1.71055 -1.225 -1.25079 -1.38103  2.49390 -1.63753
## 20  2.29127 -1.225 -1.28791 -1.19142  1.16600 -1.41268
## 21  0.23385 -1.225 -0.89255 -0.72470  0.19346 -0.76881
## 22 -0.76168  1.015  0.70420  0.04831 -1.56461  0.30942
## 23 -0.81146  1.015  0.59124  0.04831 -0.83520  0.22254
## 24 -1.12671  1.015  0.96240  1.43390  0.24957  0.63646
## 25 -0.14777  1.015  1.36582  0.41294 -0.96612  0.64157
## 26  1.19619 -1.225 -1.22417 -1.17684  0.90416 -1.31048
## 27  0.98049 -1.225 -0.89094 -0.81221  1.55876 -1.10097
## 28  1.71055 -1.225 -1.09427 -0.49134  0.32438 -1.74177
## 29 -0.71191  1.015  0.97046  1.71102  1.16600 -0.04829
## 30 -0.06481 -0.105 -0.69165  0.41294  0.04383 -0.45710
## 31 -0.84464  1.015  0.56704  2.74657 -0.10579  0.36052
## 32  0.21725 -1.225 -0.88529 -0.54968  0.96027 -0.44688
##        qsec     vs      am    gear    carb
## 1  -0.77717 -0.868  1.1899  0.4236  0.7352
## 2  -0.46378 -0.868  1.1899  0.4236  0.7352
## 3   0.42601  1.116  1.1899  0.4236 -1.1222
## 4   0.89049  1.116 -0.8141 -0.9318 -1.1222
## 5  -0.46378 -0.868 -0.8141 -0.9318 -0.5030
## 6   1.32699  1.116 -0.8141 -0.9318 -1.1222
## 7  -1.12413 -0.868 -0.8141 -0.9318  0.7352
## 8   1.20387  1.116 -0.8141  0.4236 -0.5030
## 9   2.82675  1.116 -0.8141  0.4236 -0.5030
## 10  0.25253  1.116 -0.8141  0.4236  0.7352
## 11  0.58830  1.116 -0.8141  0.4236  0.7352
## 12 -0.25113 -0.868 -0.8141 -0.9318  0.1161
## 13 -0.13920 -0.868 -0.8141 -0.9318  0.1161
## 14  0.08464 -0.868 -0.8141 -0.9318  0.1161
## 15  0.07345 -0.868 -0.8141 -0.9318  0.7352
## 16 -0.01609 -0.868 -0.8141 -0.9318  0.7352
## 17 -0.23993 -0.868 -0.8141 -0.9318  0.7352
## 18  0.90728  1.116  1.1899  0.4236 -1.1222
## 19  0.37564  1.116  1.1899  0.4236 -0.5030
## 20  1.14791  1.116  1.1899  0.4236 -1.1222
## 21  1.20947  1.116 -0.8141 -0.9318 -1.1222
## 22 -0.54772 -0.868 -0.8141 -0.9318 -0.5030
## 23 -0.30709 -0.868 -0.8141 -0.9318 -0.5030
## 24 -1.36476 -0.868 -0.8141 -0.9318  0.7352
## 25 -0.44699 -0.868 -0.8141 -0.9318 -0.5030
## 26  0.58830  1.116  1.1899  0.4236 -1.1222
## 27 -0.64286 -0.868  1.1899  1.7789 -0.5030
## 28 -0.53093  1.116  1.1899  1.7789 -0.5030
## 29 -1.87401 -0.868  1.1899  1.7789  0.7352
## 30 -1.31440 -0.868  1.1899  1.7789  1.9734
## 31 -1.81805 -0.868  1.1899  1.7789  3.2117
## 32  0.42041  1.116  1.1899  0.4236 -0.5030
```

#### Kustomisasi Nama Kolom dan Nama Baris

*Tidy* data tidak menggunakan nama variabel yang di simpan pada variabel diluar kolom. Untuk bekerja dengan nama kolom kita perlu memindahkan nama baris menjadi kolom baru. Terdapat dua fungsi untuk bekerja dengan nama baris, antara lain:

1. `rownames_to_column()`: merubah nama baris menjadi kolom baru.
2. `column_to_rownames()`: merubah kolom menjadi nama baris.


```r
rownames_to_column(.data, var = "rowname")

column_to_rownames(.data, var = "rowname")
```

> **Note: **
>
> - **.data**: dataframe.
> - **var**: nama kolom yang akan digunakan atau dibuat.

Berikut adalah contoh sintaks pada fungsi tersebut:


```r
# membuat kolom nama mobil
mtcars2 <- rownames_to_column(mtcars, var="nama_mobil")
head(mtcars2)
```

```
##          nama_mobil  mpg cyl disp  hp drat    wt  qsec
## 1         Mazda RX4 21.0   6  160 110 3.90 2.620 16.46
## 2     Mazda RX4 Wag 21.0   6  160 110 3.90 2.875 17.02
## 3        Datsun 710 22.8   4  108  93 3.85 2.320 18.61
## 4    Hornet 4 Drive 21.4   6  258 110 3.08 3.215 19.44
## 5 Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02
## 6           Valiant 18.1   6  225 105 2.76 3.460 20.22
##   vs am gear carb
## 1  0  1    4    4
## 2  0  1    4    4
## 3  1  1    4    1
## 4  1  0    3    1
## 5  0  0    3    2
## 6  1  0    3    1
```

```r
# membuat kolom nama mobil menajdi nama baris
mtcars3 <- column_to_rownames(mtcars2, var="nama_mobil")
head(mtcars3)
```

```
##                    mpg cyl disp  hp drat    wt  qsec
## Mazda RX4         21.0   6  160 110 3.90 2.620 16.46
## Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02
## Datsun 710        22.8   4  108  93 3.85 2.320 18.61
## Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44
## Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02
## Valiant           18.1   6  225 105 2.76 3.460 20.22
##                   vs am gear carb
## Mazda RX4          0  1    4    4
## Mazda RX4 Wag      0  1    4    4
## Datsun 710         1  1    4    1
## Hornet 4 Drive     1  0    3    1
## Hornet Sportabout  0  0    3    2
## Valiant            1  0    3    1
```

Sering kali nama variabel atau kolom yang kita miliki tidak sesuai dengan deskripsi data yang kita dimiliki. Kita dapat mengubah nama kolom tersebut menggunakan fungsi `rename()`. Format fungsi tersebut adalah sebagai berikut:


```r
rename(.data, ...)
```

> **Note: **
>
> - **.data**: dataframe.
> - **...**: Argumen tambahan pada yan berisi nam kolom baru disertai nama kolom lama.

Berikut adalah contoh sintaks untuk mengubah nama kolom:


```r
rename(mtcars, horse_power=hp)
```

```
##                      mpg cyl  disp horse_power drat
## Mazda RX4           21.0   6 160.0         110 3.90
## Mazda RX4 Wag       21.0   6 160.0         110 3.90
## Datsun 710          22.8   4 108.0          93 3.85
## Hornet 4 Drive      21.4   6 258.0         110 3.08
## Hornet Sportabout   18.7   8 360.0         175 3.15
## Valiant             18.1   6 225.0         105 2.76
## Duster 360          14.3   8 360.0         245 3.21
## Merc 240D           24.4   4 146.7          62 3.69
## Merc 230            22.8   4 140.8          95 3.92
## Merc 280            19.2   6 167.6         123 3.92
## Merc 280C           17.8   6 167.6         123 3.92
## Merc 450SE          16.4   8 275.8         180 3.07
## Merc 450SL          17.3   8 275.8         180 3.07
## Merc 450SLC         15.2   8 275.8         180 3.07
## Cadillac Fleetwood  10.4   8 472.0         205 2.93
## Lincoln Continental 10.4   8 460.0         215 3.00
## Chrysler Imperial   14.7   8 440.0         230 3.23
## Fiat 128            32.4   4  78.7          66 4.08
## Honda Civic         30.4   4  75.7          52 4.93
## Toyota Corolla      33.9   4  71.1          65 4.22
## Toyota Corona       21.5   4 120.1          97 3.70
## Dodge Challenger    15.5   8 318.0         150 2.76
## AMC Javelin         15.2   8 304.0         150 3.15
## Camaro Z28          13.3   8 350.0         245 3.73
## Pontiac Firebird    19.2   8 400.0         175 3.08
## Fiat X1-9           27.3   4  79.0          66 4.08
## Porsche 914-2       26.0   4 120.3          91 4.43
## Lotus Europa        30.4   4  95.1         113 3.77
## Ford Pantera L      15.8   8 351.0         264 4.22
## Ferrari Dino        19.7   6 145.0         175 3.62
## Maserati Bora       15.0   8 301.0         335 3.54
## Volvo 142E          21.4   4 121.0         109 4.11
##                        wt  qsec vs am gear carb
## Mazda RX4           2.620 16.46  0  1    4    4
## Mazda RX4 Wag       2.875 17.02  0  1    4    4
## Datsun 710          2.320 18.61  1  1    4    1
## Hornet 4 Drive      3.215 19.44  1  0    3    1
## Hornet Sportabout   3.440 17.02  0  0    3    2
## Valiant             3.460 20.22  1  0    3    1
## Duster 360          3.570 15.84  0  0    3    4
## Merc 240D           3.190 20.00  1  0    4    2
## Merc 230            3.150 22.90  1  0    4    2
## Merc 280            3.440 18.30  1  0    4    4
## Merc 280C           3.440 18.90  1  0    4    4
## Merc 450SE          4.070 17.40  0  0    3    3
## Merc 450SL          3.730 17.60  0  0    3    3
## Merc 450SLC         3.780 18.00  0  0    3    3
## Cadillac Fleetwood  5.250 17.98  0  0    3    4
## Lincoln Continental 5.424 17.82  0  0    3    4
## Chrysler Imperial   5.345 17.42  0  0    3    4
## Fiat 128            2.200 19.47  1  1    4    1
## Honda Civic         1.615 18.52  1  1    4    2
## Toyota Corolla      1.835 19.90  1  1    4    1
## Toyota Corona       2.465 20.01  1  0    3    1
## Dodge Challenger    3.520 16.87  0  0    3    2
## AMC Javelin         3.435 17.30  0  0    3    2
## Camaro Z28          3.840 15.41  0  0    3    4
## Pontiac Firebird    3.845 17.05  0  0    3    2
## Fiat X1-9           1.935 18.90  1  1    4    1
## Porsche 914-2       2.140 16.70  0  1    5    2
## Lotus Europa        1.513 16.90  1  1    5    2
## Ford Pantera L      3.170 14.50  0  1    5    4
## Ferrari Dino        2.770 15.50  0  1    5    6
## Maserati Bora       3.570 14.60  0  1    5    8
## Volvo 142E          2.780 18.60  1  1    4    2
```

### summarize() dan group_by()

Kita dapat membuat ringkasan data menggunakan fungsi `summarize()`. Fungsi tersebut akan merubah data frame menjadi sebuah baris berisi ringkasan data yang kita inginkan. Berikut adalh contoh penerapannya:


```r
summarize(flights, delay = mean(dep_delay, na.rm = TRUE))
```

```
## # A tibble: 1 x 1
##   delay
##   <dbl>
## 1  12.6
```

FUngsi ini akan lebih berguna saat digunakan dengan fungsi `group_by()` sehingga dapat diperoleh ringkasan data pada setiap grup. berikut adalah contoh penerapannya:


```r
by_day <- group_by(flights, year, month, day)
    summarize(by_day, delay = mean(dep_delay, na.rm = TRUE))
```

```
## # A tibble: 365 x 4
## # Groups:   year, month [12]
##     year month   day delay
##    <int> <int> <int> <dbl>
##  1  2013     1     1 11.5 
##  2  2013     1     2 13.9 
##  3  2013     1     3 11.0 
##  4  2013     1     4  8.95
##  5  2013     1     5  5.73
##  6  2013     1     6  7.15
##  7  2013     1     7  5.42
##  8  2013     1     8  2.55
##  9  2013     1     9  2.28
## 10  2013     1    10  2.84
## # ... with 355 more rows
```

### Mengkombinasikan Beberapa Operasi Menggunakan Operator Pipe (%>%)

Operator pipa (%>%) sangat berguna untuk merangkai bersama beberapa fungsi `dplyr` dalam suatu urutan operasi. Perhatikan contoh sebelumnya dimana setiap kali kita ingin menerapkan lebih dari satu fungsi, urutannya akan dimulai dalam urutan panggilan fungsi bersarang yang sulit dibaca. Secara ringkas dapat kita tulis sebagai berikut:


```r
third(second(first(x)))
```

Jika dituliskan menggunakan operator pipa akan menghasilkan sintak berikut:


```r
x %>%
  first() %>%
  second() %>%
  third()
```

Dengan menuliskannya melalui cara tersebut kita dapat membacanya lebih mudah.

Misal kita ingin mengetahui hubungan antara variabel jarak (`dist`) terhadap rata-rata delay (`arr_delay`). Langkah-langkah untuk melakukannya dengan menggunakan operator pipa adalah sebagai berikut:

1. Kelompokkan penerbangan berdasarkan destinasinya (`group_by()`).
2. Hitung ringkasan data berdasarkan jarak, rata-rata delay, dan jumlah penerbangan.
3. Lakukan filter untuk membuang *noisy point* (jika diperlukan). Dalam hal ini jumlah penerbangan > 20 dan tujuan penerbangan Honolulu ("HNL") adalah *outlier* atau *noisy point*.

Berikut adalah sintaks untuk melakukannya:

```r
# Tanpa pipe operator
by_dest <- group_by(flights, dest)
delay <- summarize(by_dest,
  count = n(),
  dist = mean(distance, na.rm = TRUE),
  delay = mean(arr_delay, na.rm = TRUE)
)
delay <- filter(delay, count > 20, dest != "HNL")

# Dengan pipe operator
library(magrittr)
```

```
## 
## Attaching package: 'magrittr'
```

```
## The following object is masked from 'package:tidyr':
## 
##     extract
```

```
## The following object is masked from 'package:purrr':
## 
##     set_names
```

```r
delays <- flights %>%
  group_by(dest) %>%
  summarize(
  count = n(),
  dist = mean(distance, na.rm = TRUE),
  delay = mean(arr_delay, na.rm = TRUE)
  ) %>%
  filter(count > 20, dest != "HNL")

# Print
delays
```

```
## # A tibble: 96 x 4
##    dest  count  dist delay
##    <chr> <int> <dbl> <dbl>
##  1 ABQ     254 1826   4.38
##  2 ACK     265  199   4.85
##  3 ALB     439  143  14.4 
##  4 ATL   17215  757. 11.3 
##  5 AUS    2439 1514.  6.02
##  6 AVL     275  584.  8.00
##  7 BDL     443  116   7.05
##  8 BGR     375  378   8.03
##  9 BHM     297  866. 16.9 
## 10 BNA    6333  758. 11.8 
## # ... with 86 more rows
```



```r
# Visualisasikan dengan ggplot
library(ggplot2)
ggplot(data = delay, mapping = aes(x = dist, y = delay)) +
geom_point(aes(size = count), alpha = 1/3) +
geom_smooth(se = FALSE)
```

```
## `geom_smooth()` using method = 'loess' and formula 'y ~ x'
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/distvsave-1} 

}

\caption{Jarak vs rata-rata delay}(\#fig:distvsave)
\end{figure}

Berdasarkan Gambar \@ref(fig:distvsave), rata-rata delay meningkat seiring dengan pertambahan jarak penerbangan.

## Referensi

1. Wickham, H. Grolemund G. 2016. **R For Data Science: Import, Tidy, Transform, Visualize, And Model Data**. O'Reilly Media, Inc.
2. Peng, R.D. 2015. **Exploratory Data Analysis with R**. Leanpub book.
3. Dplyr Documentation. <https://dplyr.tidyverse.org/>
4. Quick-R. **Data Input**. <https://www.statmethods.net/input/index.html>
5. Quick-R. **Data Management**. <https://www.statmethods.net/management/index.html>
6. STHDA. **Importing Data Into R **. <http://www.sthda.com/english/wiki/importing-data-into-r>
7. STHDA. **Exporting Data From R**. <http://www.sthda.com/english/wiki/exporting-data-from-r>

<!--chapter:end:03-manajemen-data-r.Rmd-->

# (PART\*) Visualisasi Data - R {-}

<style>
body{
text-align: justify}
</style>

# Visualisasi Data Menggunakan Fungsi Dasar R

Visualisasi data merupakan bagian yang sangat penting untuk mengkomunikasikan hasil analisa yang telah kita lakukan. Selain itu, komunikasi juga membantu kita untuk memperoleh gambaran terkait data selama proses analisa data sehingga membantu kita dalam memutuskan metode analisa apa yang dapat kita terapkan pada data tersebut.

`R` memiliki library visualisasi yang sangat beragam, baik yang merupakan fungsi dasar pada `R` maupun dari sumber lain seperti ggplot dan lattice. Seluruh library visualisasi tersebut memiliki kelebihan dan kekurangannya masing-masing.

Pada *chapter* ini kita tidak akan membahas seluruh library tersebut. Kita akab berfokus pada fungsi visualisasi dasar bawaan dari `R`. kita akan mempelajari mengenai jenis visualisasi data sampai dengan melakukan kustomisasi pada parameter grafik yang kita buat.

## Visualisasi Data Menggunakan Fungsi plot()

Fungsi `plot()` merupakan fungsi umum yang digunakan untuk membuat plot pada `R`. Format dasarnya adalah sebagai berikut:


```r
plot(x, y, type="p")
```

> **Note: **
>
> - **x dan y**: titik koordinat plot Berupa variabel dengan panjang atau jumlah observasi yang sama.
> - **type**: jenis grafik yang hendak dibuat. Nilai yang dapat dimasukkan antara lain:
>   + type="p" : membuat plot titik atau scatterplot. Nilai ini merupakan default pada fungsi `plot()`.
>   + type="l" : membuat plot garis.
>   + type="b" : membuat plot titik yang terhubung dengan garis.
>   + type="o" : membuat plot titik yang ditimpa oleh garis.
>   + type="h" : membuat plot garis vertikal dari titik ke garis y=0.
>   + type="s" : membuat fungsi tangga.
>   + type="n" : tidak membuat grafik plot sama sekali, kecuali plot dari axis. Dapat digunakan untuk mengatur tampilan suatu plot utama yang diikuti oleh sekelompok plot tambahan.

Untuk lebih memahaminya berikut penulis akan sajikan contoh untuk masing-masing grafik tersebut. Berikut adalah contoh sintaks dan hasil plot yang disajikan pada Gambar \@ref(fig:plot):


```r
# membuat vektor data 
x <- c(1:10); y <- x^2
```


```r
# membagi jendela grafik menajdi 4 baris dan 2 kolom
par(mfrow=c(3,3))

# loop
type <- c("p","l","b","o","h","s","n")
for (i in type){
  plot(x,y, type= i,
       main= paste("type=", i))
}
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/plot-1} 

}

\caption{Plot berbagai jenis setting type}(\#fig:plot)
\end{figure}




Pada contoh selanjutnya akan dilakukan plot terhadap dataset `trees`. Untuk memuatnya jalankan sintaks berikut:

```r
library(tibble)
```



```r
# memuat dataset
trees <- as_tibble(trees)

# print 
trees
```

```
## # A tibble: 31 x 3
##    Girth Height Volume
##    <dbl>  <dbl>  <dbl>
##  1   8.3     70   10.3
##  2   8.6     65   10.3
##  3   8.8     63   10.2
##  4  10.5     72   16.4
##  5  10.7     81   18.8
##  6  10.8     83   19.7
##  7  11       66   15.6
##  8  11       75   18.2
##  9  11.1     80   22.6
## 10  11.2     75   19.9
## # ... with 21 more rows
```

Pada dataset tersebut kita ingin membuat scatterplot untuk melihat korelasi antara variabel `Height` dan `Volume`. Untuk melakukannya jalankan sintaks berikut:


```r
plot(trees$Height, trees$Volume)
```


```r
# atau 
with(trees, plot(Height, Volume))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/scatter-1} 

}

\caption{Scatterplot Height vs Volume}(\#fig:scatter)
\end{figure}

Kita juga dapat menggunakan formula untuk membuat scatterplot pada Gambar \@ref(fig:scatter). Berikut adalah contoh sintaks yang digunakan:


```r
x <- trees$Height
y <- trees$Volume

plot(y~x)
```

Fungsi `plot()` juga dapat digunakan untuk membentuk matriks scatterplot. Untuk membuatnya kita hanya perlu memasukkan seluruh dataset kedalam fungsi `plot()`. Berikut adalah sintaks dan output yang dihasilkan berupa Gambar \@ref(fig:scatter2):


```r
plot(trees)
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/scatter2-1} 

}

\caption{Matriks scatterplot dataset trees}(\#fig:scatter2)
\end{figure}

Selain itu jika kita memasukkan objek `lm()` yang merupakan fungsi untuk melakukan operasi regresi linier pada fungsi `plot()`, output yang dihasilkan berupa plot diagnostik yang berguna untuk menguji asumsi model regresi linier. Berikut adalah contoh sintaks dan output yang dihasilkan pada Gambar \@ref(fig:diag):


```r
# membagi jendela grafik menjadi 2 baris dan 2 kolom
par(mfrow=c(2,2))

# plot
plot(lm(Volume~Height, data=trees))
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/diag-1} 

}

\caption{Plot diagnostik regresi linier}(\#fig:diag)
\end{figure}



Selain objek-objek tersebut, fungsi `plot()` akan banyak digunakan dalam analisis statistika kita pada chapter lainnya.

## Matriks Scatterplot

Pada bagian sebelumnya kita telah belajar bagaimana membuat matriks scatterplot mengggunakan fungsi `plot()`. Pada bagian ini kita akan belajar cara membuat matriks scatterplot menggunakan fungsi `pairs()`. Secara umum format fungsi dituliskan sebagai berikut:


```r
pairs(data, lower.panel=NULL)
```

> **Note: **
>
> - **data**: data frame
> - **lower.panel**: menampilkan atau tidak menampilkan panel bawah

Untuk lebih memahami penggunaan fungsi tersebut, berikut akan disajikan contoh penggunaannya pada dataset `iris`. Sebelum melakukannya jalankan sintaks berikut untuk memuat dataset:


```r
# memuat dataset irir
iris <- as_tibble(iris)

# print
iris
```

```
## # A tibble: 150 x 5
##    Sepal.Length Sepal.Width Petal.Length Petal.Width
##           <dbl>       <dbl>        <dbl>       <dbl>
##  1          5.1         3.5          1.4         0.2
##  2          4.9         3            1.4         0.2
##  3          4.7         3.2          1.3         0.2
##  4          4.6         3.1          1.5         0.2
##  5          5           3.6          1.4         0.2
##  6          5.4         3.9          1.7         0.4
##  7          4.6         3.4          1.4         0.3
##  8          5           3.4          1.5         0.2
##  9          4.4         2.9          1.4         0.2
## 10          4.9         3.1          1.5         0.1
## # ... with 140 more rows, and 1 more variable:
## #   Species <fct>
```

Untuk membuat matriks scatterplot kita hanya perlu memasukkan objek `iris` kedalam fungsi `pairs()`. Berikut adalah sintaks yang digunakan dan output yang dihasilkan pada Gambar \@ref(fig:matscat):


```r
pairs(iris)
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/matscat-1} 

}

\caption{Matriks scatterplot iris}(\#fig:matscat)
\end{figure}

Kita dapat melakukan drop terhadap panel bawah grafik tersebut. Untuk melakukannya kita perlu memasukkan parameter `lower.panel=NULL`. Output yang dihasilkan akan tampak seperti pada Gambar \@ref(fig:matscat2).


```r
pairs(iris, lower.panel=NULL)
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/matscat2-1} 

}

\caption{Matriks scatterplot iris tanpa panel bawah}(\#fig:matscat2)
\end{figure}

Kita dapat merubah warna titik berdasarkan factor `Species`. Langkah pertama yang perlu dilakukan adalah melakukan drop variabel `Species` pada dataset dan memasukkan objek baru tanpa variabel tersebut kedalam fungsi `pairs()`. Warna berdasarkan grup diberikan dengan menambahkan parameter `col= ` pada fungsi `pairs()`. Berikut adalah contoh penerapannya dan output yang dihasilkan pada Gambar \@ref(fig:matscat3):


```r
# drop variabel Species
# simpan dataset baru pada objek iris2
iris2 <- iris[ ,1:4]

# print
iris2
```

```
## # A tibble: 150 x 4
##    Sepal.Length Sepal.Width Petal.Length Petal.Width
##           <dbl>       <dbl>        <dbl>       <dbl>
##  1          5.1         3.5          1.4         0.2
##  2          4.9         3            1.4         0.2
##  3          4.7         3.2          1.3         0.2
##  4          4.6         3.1          1.5         0.2
##  5          5           3.6          1.4         0.2
##  6          5.4         3.9          1.7         0.4
##  7          4.6         3.4          1.4         0.3
##  8          5           3.4          1.5         0.2
##  9          4.4         2.9          1.4         0.2
## 10          4.9         3.1          1.5         0.1
## # ... with 140 more rows
```

```r
# spesifikasi vaktor warna titik berdasarkan spesies
my_col <- c("#00AFBB", "#E7B800", "#FC4E07")

# plot
pairs(iris2, lower.panel=NULL,
      # spesifikasi warna
      col= my_col[iris$Species])
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/matscat3-1} 

}

\caption{Matriks scatterplot iris tanpa panel bawah}(\#fig:matscat3)
\end{figure}

Kita juga dapat mengganti panel bawah menjadi nilai korelasi antar variabel. Untuk melakukannya kita perlu mendefinisikan sebuah fungsi untuk panel bawah dan panel atas (jika ingin warna titik berdasarkan factor). Setelah fungsi panel bawah dan atas didefinisikan, langkah selanjutnya adalah melakukan memasukkan nilainya kedalam fungsi `pairs()`. Berikut adalah sintaks yang digunakan serta output yang dihasilkan pada Gambar \@ref(fig:matscat4):


```r
# membuat fungsi untuk menghitung
# nilai korelasi yang ditempatkan pada panel bawah
panel.cor <- function(x, y){
    # definisi parameter grafik 
    usr <- par("usr"); on.exit(par(usr))
    par(usr = c(0, 1, 0, 1))
    # menghitung koefisien korelas
    r <- round(cor(x, y), digits=2)
    # menambahkan text berdasarkan koefisien korelasi
    txt <- paste0("R = ", r)
    # mengatur besar text sesuai besarnya nilai korelasi
    cex.cor <- 0.8/strwidth(txt)
    text(0.5, 0.5, txt, cex = cex.cor * abs(r))
}

# kustomisasi panel atas agar
# warna titik berdasarkan factor
my_col <- c("#00AFBB", "#E7B800", "#FC4E07")
upper.panel<-function(x, y){
  points(x,y, col = my_col[iris$Species])
}

pairs(iris2,
      lower.panel= panel.cor,
      upper.panel= upper.panel)
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/matscat4-1} 

}

\caption{Matriks scatterplot iris dengan koefisien korelasi}(\#fig:matscat4)
\end{figure}

Jika kita tidak ingin nilai korelasi ditampilkan di panel bawah, kita dapat merubahnya sehingga dapat tampil pada panel atas bersamaan dengan scatterplot. Untuk melakukannya kita perlu mendefinisikan fungsi pada panel atas dan memasukkannya pada parameter `upper.panel= `. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:matscat5):


```r
# kustomisasi panel atas
upper.panel<-function(x, y){
  points(x,y, col=c("#00AFBB", "#E7B800", "#FC4E07")[iris$Species])
  r <- round(cor(x, y), digits=2)
  txt <- paste0("R = ", r)
  usr <- par("usr"); on.exit(par(usr))
  par(usr = c(0, 1, 0, 1))
  text(0.5, 0.9, txt)
}

# plot
pairs(iris2, lower.panel = NULL, 
      upper.panel = upper.panel)
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/matscat5-1} 

}

\caption{Matriks scatterplot iris dengan koefisien korelasi di panel atas}(\#fig:matscat5)
\end{figure}

## Box plot

Box plot pada `R` dapat dibuat menggunakan fungsi `boxplot()`. Berikut adalah sintaks untuk membuat boxplot variabel `Sepal.Lenght` pada dataset `iris` dan output yang dihasilkan pada Gambar \@ref(fig:boxplot):


```r
boxplot(iris$Sepal.Length)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/boxplot-1} 

}

\caption{Boxplot variabel Sepal.Length}(\#fig:boxplot)
\end{figure}

Boxplot juga dapat dibuat berdasarkan variabel factor. Hal ini berguna untuk melihat perbedaan ditribusi data pada masing-masing grup. Pada sintaks berikut dibuat boxplot berdasarkan variabel `Species`. Output yang dihasilkan disajikan pada Gambar \@ref(fig:boxplot2):


```r
boxplot(iris$Sepal.Length~iris$Species)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/boxplot2-1} 

}

\caption{Boxplot berdasarkan variabel species}(\#fig:boxplot2)
\end{figure}

Kita juga dapat mengubah warna outline dan box pada boxplot. Berikut adalah contoh sintaks yang digunakan untuk melakukannya dan output yang dihasilkan disajikan pada Gambar \@ref(fig:boxplot3):


```r
boxplot(iris$Sepal.Length~iris$Species,
        # ubah warna outline menjadi steelblue
        border = "steelblue",
        # ubah warna box berdasarkan grup
        col= c("#999999", "#E69F00", "#56B4E9"))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/boxplot3-1} 

}

\caption{Boxplot dengan warna berdasarkan spesies}(\#fig:boxplot3)
\end{figure}

Kita juga dapat membuat boxplot pada *multiple group*. Data yang digunakan untuk contoh tersebut adalah dataset `ToothGrowth`. Berikut adalah sintaks untuk memuat dataset tersebut:


```r
# memuat dataset sebagai tibble
ToothGrowth <- as_tibble(ToothGrowth)

# print
ToothGrowth
```

```
## # A tibble: 60 x 3
##      len supp   dose
##    <dbl> <fct> <dbl>
##  1   4.2 VC      0.5
##  2  11.5 VC      0.5
##  3   7.3 VC      0.5
##  4   5.8 VC      0.5
##  5   6.4 VC      0.5
##  6  10   VC      0.5
##  7  11.2 VC      0.5
##  8  11.2 VC      0.5
##  9   5.2 VC      0.5
## 10   7   VC      0.5
## # ... with 50 more rows
```

```r
# ubah variable dose menjadi factor
ToothGrowth$dose <- as.factor(ToothGrowth$dose)

# print
ToothGrowth
```

```
## # A tibble: 60 x 3
##      len supp  dose 
##    <dbl> <fct> <fct>
##  1   4.2 VC    0.5  
##  2  11.5 VC    0.5  
##  3   7.3 VC    0.5  
##  4   5.8 VC    0.5  
##  5   6.4 VC    0.5  
##  6  10   VC    0.5  
##  7  11.2 VC    0.5  
##  8  11.2 VC    0.5  
##  9   5.2 VC    0.5  
## 10   7   VC    0.5  
## # ... with 50 more rows
```

Contoh sintaks dan output boxplot *multiple group* disajikan pada Gambar \@ref(fig:boxplot4):


```r
boxplot(len ~ supp*dose, data = ToothGrowth,
        col = c("white", "steelblue"))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/boxplot4-1} 

}

\caption{Boxplot multiple group}(\#fig:boxplot4)
\end{figure}

## Bar Plot

Barplot pada `R` dapat dibuat menggunakan fungsi `barplot()`. Untuk lebih memahaminya berikut disajikan contoh barplot menggunakan dataset `VADeaths`. Untuk memuatnya jalankan sintaks berikut:


```r
VADeaths
```

```
##       Rural Male Rural Female Urban Male Urban Female
## 50-54       11.7          8.7       15.4          8.4
## 55-59       18.1         11.7       24.3         13.6
## 60-64       26.9         20.3       37.0         19.3
## 65-69       41.0         30.9       54.6         35.1
## 70-74       66.0         54.3       71.1         50.0
```

Contoh bar plot untuk variabel `Rural Male` disajikan pada Gambar \@ref(fig:barplot):


```r
par(mfrow=c(1,2))
barplot(VADeaths[, "Rural Male"], main="a")
barplot(VADeaths[, "Rural Male"], main="b", horiz=TRUE)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/barplot-1} 

}

\caption{a. bar plot vertikal; b. bar plot horizontal}(\#fig:barplot)
\end{figure}


```r
par(mfrow=c(1,1))
```


Kita dapat mengubah warna pada masing-masing bar, baik outline bar maupun box pada bar. Selain itu kita juga dapat mengubah nama grup yang telah dihasilkan sebelumnya. Berikut sintaks untuk melakukannya dan output yang dihasilkan pada Gambar \@ref(fig:barplot2):


```r
barplot(VADeaths[, "Rural Male"],
        # ubah warna ouline menjadi steelblue
        border="steelblue",
        # ubah wana box
        col= c("grey", "yellow", "steelblue", "green", "orange"),
        # ubah nama grup dari A sampai E
        names.arg = LETTERS[1:5],
        # ubah orientasi menajadi horizontal
        horiz=TRUE)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/barplot2-1} 

}

\caption{Kustomisasi bar plot}(\#fig:barplot2)
\end{figure}

Untuk bar plot dengan *multiple group*, tersedia dua pengaturan posisi yaitu *stacked bar plot*(menunjukkan proporsi penyusun pada masing-masing grup) dan *grouped bar plot*(melihat perbedaan individual pada masing-masing grup). Pada Gambar \@ref(fig:barplot3) dan Gambar \@ref(fig:barplot4) , disajikan kedua jenis bar plot tersebut.


```r
# staked
barplot(VADeaths,
         col = c("lightblue", "mistyrose", "lightcyan", 
                 "lavender", "cornsilk"),
        legend = rownames(VADeaths))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/barplot3-1} 

}

\caption{Stacked bar plot}(\#fig:barplot3)
\end{figure}


```r
# grouped
barplot(VADeaths,
         col = c("lightblue", "mistyrose", "lightcyan", 
                 "lavender", "cornsilk"),
        legend = rownames(VADeaths), beside = TRUE)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/barplot4-1} 

}

\caption{Grouped bar plot}(\#fig:barplot4)
\end{figure}

## Line Plot

Line plot pada `R` dapat dibentuk menggunakan fungsi `plot()`. Selain itu fungsi `lines()` dapat pula digunakan untuk menambahkan line plot pada grafik. Berikut adalah sintaks untuk membuat line plot dan outputnya pada Gambar \@ref(fig:line):


```r
# Membuat vektor data
x <- c(1:20)
y <- 2*x
z <- x^2

# Membuat line plot x vs y
plot(y~x, type="b",
     lty=1,
     col="blue")

# Menambahkan line plot x vs z
lines(z~x, type="o",
      lty=2,
      col="red")

# Menambahkan legend
legend("topleft", legend=c("Line 1", "Line 2"),
       col=c("red", "blue"), lty = 1:2, cex=0.8)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/line-1} 

}

\caption{Line plot}(\#fig:line)
\end{figure}

## Pie Chart

Pie chart digunakan untuk membuat visualisasi proporsi pada sebuah data. Pie chart pada `R` dibuat menggunakan fungsi `pie()`. Berikut adalah sintaks untuk membuat pie chart dan output yang dihasilkan pada Gambar \@ref(fig:pie):


```r
par(mar = c(0, 1, 0, 1))
pie(
  c(280, 60, 20),
  c('Sky', 'Sunny side of pyramid', 'Shady side of pyramid'),
  col = c('#0292D8', '#F7EA39', '#C4B632'),
  init.angle = -50, border = NA
)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/pie-1} 

}

\caption{Pie chart}(\#fig:pie)
\end{figure}

## Histogram dan Density Plot

Fungsi `hist()` dapat digunakan untuk membuat histogram pada `R`. Secara sederhana fungsi tersebut didefinisikan sebagai berikut:

```r
hist(x, breaks="Sturges")
```

> **Note: **
>
> - **x**: vektor numerik
> - **breaks**: *breakpoints* antar sel histogram.

Pada dataset `trees` akan dibuat histogram variabel `Height`. Untuk melakukannya jalankan sintaks berikut:


```r
hist(trees$Height)
```

Output yang dihasilkan disajikan pada Gambar \@ref(fig:hist): 

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/hist-1} 

}

\caption{Histogram}(\#fig:hist)
\end{figure}

Density plot pada `R` dapat dibuat menggunakan fungsi `density()`. Berbeda dengan fungsi `hist()`, fungsi ini tidak langsung menghasilkan grafik densitas. Fungsi `density()` hanya menghitung kernel densitas pada data. Densitas yang telah dihitung selanjutnya diplotkan menggunakan fungsi `plot()`. Berikut adalah sintaks dan output yang dihasilkan pada  Gambar \@ref(fig:dens):


```r
# menghitung kernel density
dens <- density(trees$Height)

# plot densitas dengan outline merah
plot(dens,col="red")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/dens-1} 

}

\caption{Density plot}(\#fig:dens)
\end{figure}

Kita juga dapat menambahkan grafik densitas pada histogram sehingga mempermudah pembacaan pada histogram. Untuk melakukannya kita perlu mengubah kernel histigram dari frekuensi menjadi density dengan menambahkan argumen `freq=FALSE` pada fungsi `hist()`. Selanjutnya tambahkan fungsi `polygon()` untuk memplotkan grafik densitas. Berikut adalah sintak dan output yang dihasilkan pada  Gambar \@ref(fig:denshist):


```r
# menghitung kernel density
dens <- density(trees$Height)

# histogram
hist(trees$Height, freq=FALSE, col="steelblue")

# tambahkan density plot
polygon(dens, border="red")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/denshist-1} 

}

\caption{Density plot dan histogram}(\#fig:denshist)
\end{figure}

## QQ Plot

QQ plot digunakan untuk mengecek distribusi suatu data apakah berdistribusi normal atau tidak. Pada `R` QQ plot dibuat menggunakan 2 fungsi yaitu: `qqnorm()` dan `qqline()`. Fungsi `qqnorm()` digunakan untuk memproduksi normal QQ plot suatu variabel. Sedangkan fungsi `qqline()` digunakan untuk membuat garis referensi distiribusi normal. Suatu distribusi dikatan normal jika titik observasi yang dihasilkan mengikuti garis referensi tersebut.

Berikut adalah cara membuat QQ plot menggunakan variabel `Volume` pada dataset `trees`. Output yang dihasilkan disajikan pada Gambar \@ref(fig:qq).


```r
qqnorm(trees$Volume)
qqline(trees$Volume, col="red")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/qq-1} 

}

\caption{QQ plot}(\#fig:qq)
\end{figure}

## Dot Chart

Fungsi `dotchart()` pada `R` digunakan untuk membuat dot chart. Format yang digunakan adalah sebagai berikut:


```r
dotchart(x, labels = NULL, groups = NULL, 
         gcolor = par("fg"), color = par("fg"))
```

> **Note: **
>
> - **x**: vektor atau matriks numerik.
> - **labels**: vektor label untuk tiap titik.
> - **groups**: grouping variabel yang mengindikasikan bagaimana **x** dikelompokkan.
> - **gcolor**: warna yang digunakan pada label grup dan nilai observasi.
> - **color**: warna yang digunakan untuk titik dan label.

Pada contoh berikut disajikan cara membuat dot chart pada dataset `mtcars` untuk melihat mobil yang paling hemat bahan bakar berdasarkan variabel `mpg` dan jumlah silinder (`cyl`). Berikut sintaks yang digunakan dan output yang dihasilkan pada Gambar \@ref(fig:dot):


```r
# mengurutkan dataset mtcars berdasarkan variabel mpg
mtcars <- mtcars[order(mtcars$mpg), ]

# mengubah variabel cyl menjadi factor
grps <- as.factor(mtcars$cyl)

# membuat vektor warna berdasarkan jumlah grup
my_cols <- c("#999999", "#E69F00", "#56B4E9")

# plot
dotchart(mtcars$mpg, labels = row.names(mtcars),
         groups = grps, gcolor = my_cols,
         color = my_cols[grps],
         cex = 0.6,  pch = 19, xlab = "mpg")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/dot-1} 

}

\caption{Dot chart}(\#fig:dot)
\end{figure}

## Kustomisasi Parameter Grafik

Pada bagian ini penulis akan menjelaskan cara untuk kustomisasi parameter grafik seperti:

a. menambahkan judul, legend, teks, axis, dan garis.
b. mengubah skala axis, simbol plot, jenis garis, dan warna.

### Menambahkan Judul

Pada grafik di `R`, kita dapat menambahkan judul dengan dua cara, yaitu: pada plot melalui parameter dan melalui fungsi plot(). Kedua cara tersebut tidak berbeda satu sama lain pada parameter input.

Untuk menambahkan judul pada plot secara langsung, kita dapat menggunakan argumen tambahan sebagai berikut:

a. **main**: teks untuk judul.
b. **xlab**: teks untuk keterangan axis X.
c. **ylab**: teks untuk keterangan axis y.
d. **sub**: teks untuk sub-judul.

Berikut contoh sintaks penerapan masing-masing argumen tersebut beserta dengan output yang dihasilkan pada Gambar \@ref(fig:title):


```r
# menambahkan judul
barplot(c(2,5), main="Main title",
        xlab="X axis title",
        ylab="Y axis title",
        sub="Sub-title")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/title-1} 

}

\caption{Menambahkan Judul}(\#fig:title)
\end{figure}

kita juga dapat melakukan kustomisasi pada warna, *font style*, dan ukuran font judul. Untuk melakukan kustomisasi pada warna pada judul, kita dapat menambahkan argumen sebagai berikut:

a. **col.main**: warna untuk judul.
b. **col.lab**: warna untuk keterangan axis.
c. **col.sub**: warna untuk sub-judul

Untuk kustomisasi font judul, kita dapat menambahkan argumen berikut:

a. **font.main**: *font style* untuk judul.
b. **font.lab**: *font style* untuk keterangan axis.
c. **font.sub**: *font style* untuk sub-judul.

> **Note: **
> 
> Nilai yang dapat dimasukkan antara lain:
>
> - **1**: untuk teks normal.
> - **2**: untuk teks cetak tebal.
> - **3**: untuk teks cetak miring.
> - **4**: untuk teks cetak tebal dan miring.
> - **5**: untuk font simbol.

Sedangkan untuk ukuran font, kita dapat menambahkan variabel berikut:

a. **cex.main**: ukuran teks judul.
b. **cex.lab**: ukuran teks keterangan axis.
c. **cex.sub**: ukuran teks sub-judul.

Berikut sintaks penerapan seluruh argumen tersebut beserta output yang dihasilkan pada Gambar \@ref(fig:title2):


```r
# menambahkan judul
barplot(c(2,5), 
        # menambahkan judul
        main="Main title",
        xlab="X axis title",
        ylab="Y axis title",
        sub="Sub-title",
        # kustomisasi warna font
        col.main="red", 
        col.lab="blue", 
        col.sub="black",
        # kustomisasi font style
        font.main=4, 
        font.lab=4, 
        font.sub=4,
        # kustomisasi ukuran font
        cex.main=2, 
        cex.lab=1.7, 
        cex.sub=1.2)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/title2-1} 

}

\caption{Menambahkan Judul (2)}(\#fig:title2)
\end{figure}

Kita telah belajar bagaimana menambahkan judul langsung pada fungsi plot. Selain cara tersebut, telah penulis jelaskan bahwa kita dapat menambahkan judul melalui fungsi `title()`. argumen yang dimasukkan pada dasarnya tidak berbeda dengan ketika kita menambahkan judul secara langsung pada plot. Berikut adalah contoh sintaks dan output yang dihasilkan pada Gambar \@ref(fig:title3):


```r
# menambahkan judul
barplot(c(2,5,8))

# menambahkan judul
title(main="Main title",
      xlab="X axis title",
      ylab="Y axis title",
      sub="Sub-title",
      # kustomisasi warna font
      col.main="red", 
      col.lab="blue", 
      col.sub="black",
      # kustomisasi font style
      font.main=4, 
      font.lab=4, 
      font.sub=4,
      # kustomisasi ukuran font
      cex.main=2, 
      cex.lab=1.7, 
      cex.sub=1.2)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/title3-1} 

}

\caption{Menambahkan Judul (3)}(\#fig:title3)
\end{figure}

### Menambahkan Legend

Fungsi `legend()` pada `R` dapat digunakan untuk menambahkan legend pada grafik. Format sederhananya adalah sebagai berikut:


```r
legend(x, y=NULL, legend, fill, col, bg)
```

> **Note: **
>
> - **x** dan **y**: koordinat yang digunakan untuk posisi legend.
> - **legend**: teks pada legend
> - **fill**: warna yang digunakan untuk mengisi box disamping teks legend.
> - **col**: warna garis dan titik disamping teks legend.
> - **bg**: warna latar belakang legend box.

Berikut adalah contoh sintaks dan ouput penerapan argumen disajikan pada Gambar \@ref(fig:legend):


```r
# membuat vektor numerik
x <- c(1:10)
y <- x^2
z <- x*2

# membuat line plot
plot(x,y, type="o", col="red", lty=1)

# menambahkan line plot
lines(x,z, type="o", col="blue", lty=2)

# menambahkan legend
legend(1, 95, legend=c("Line 1", "Line 2"),
       col=c("red", "blue"), lty=1:2, cex=0.8)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/legend-1} 

}

\caption{Menambahkan legend}(\#fig:legend)
\end{figure}

Kita dapat menambahkan judul, merubah font, dan merubah warna backgroud pada legend. Argumen  yang ditambahkan pada legend adalah sebagai berikut:

a. **title**: Judul legend
b. **text.font**: integer yang menunjukkan *font style* pada teks legend. Nilai yang dapat dimasukkan adalah sebagai berikut:
    + **1**: normal
    + **2**: cetak tebal
    + **3**: cetak miring
    + **4**: cetak tebal dan miring.
c. **bg**: warna background legend box.

Berikut adalah penerapan sintaks dan output yang dihasilkan pada Gambar \@ref(fig:legend2):


```r
# membuat line plot
plot(x,y, type="o", col="red", lty=1)

# menambahkan line plot
lines(x,z, type="o", col="blue", lty=2)

# menambahkan legend
legend(1, 95, legend=c("Line 1", "Line 2"),
       col=c("red", "blue"), lty=1:2, cex=0.8,
       title="Line types", text.font=4, bg='lightblue')
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/legend2-1} 

}

\caption{Menambahkan legend (2)}(\#fig:legend2)
\end{figure}

Kita dapat melakukan kustomisasi pada border dari legend melalui argumen `box.lty= `(jenis garis), `box.lwd= `(ukuran garis), dan `box.col= `(warna box). Berikut adalah penerapan argumen tersebut beserta output yang dihasilkan pada Gambar \@ref(fig:legend3):


```r
# membuat line plot
plot(x,y, type="o", col="red", lty=1)

# menambahkan line plot
lines(x,z, type="o", col="blue", lty=2)

# menambahkan legend
legend(1, 95, legend=c("Line 1", "Line 2"),
       col=c("red", "blue"), lty=1:2, cex=0.8,
       title="Line types", text.font=4, bg='white',
       box.lty=2, box.lwd=2, box.col="steelblue")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/legend3-1} 

}

\caption{Menambahkan legend (3)}(\#fig:legend3)
\end{figure}

Selain menggunakan koordinat, kita juga dapat melakukan kustomisasi posisi legend menggunakan *keyword* seperti: bottomright", "bottom", "bottomleft", "left", "topleft", "top", "topright", "right" and "center". Sejumlah kustomisasi legend berdasarkan *keyword* disajikan pada Gambar \@ref(fig:legend4):


```r
# plot
plot(x,y, type = "n")

# posisi kiri atas, inset =0.05
legend("topleft",
  legend = "(x,y)",
  title = "topleft, inset = .05",
  inset = 0.05)
# posisi atas
legend("top",
       legend = "(x,y)",
       title = "top")
# posisi kanan atas inset = .02
legend("topright",
       legend = "(x,y)",
       title = "topright, inset = .02",
       inset = 0.02)
# posisi kiri
legend("left",
       legend = "(x,y)",
       title = "left")
# posisi tengah
legend("center",
       legend = "(x,y)",
       title = "center")
# posisi kanan
legend("right",
       legend = "(x,y)",
       title = "right")
# posisi kiri bawah
legend("bottomleft",
       legend = "(x,y)",
       title = "bottomleft")
# posisi bawah
legend("bottom",
       legend = "(x,y)",
       title = "bottom")
# posisi kanan bawah
legend("bottomright",
       legend = "(x,y)",
       title = "bottomright")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/legend4-1} 

}

\caption{Kustomisasi posisi legend}(\#fig:legend4)
\end{figure}

### Menambahkan Teks Pada Grafik

Teks pada grafik dapat kita tambahkan baik sebagai keterangan yang menunjukkan label suatu observasi, keterangan tambahan disekitar bingkai grafik, maupun sebuah persamaan yang ada pada bidang grafik. Untuk menambahkannya kita dapat menggunakan dua buah fungsi yaitu: `text()` dan `mtext()`.

FUngsi `text()` berguna untuk menambahkan teks di dalam bidang grafik seperti label titik observasi dan persamaan di dalam bidang grafik. Format yang digunakan adalah sebagai berikut:


```r
text(x, y, labels)
```

> **Note: **
>
> - **x** dan **y**: vektor numerik yang menunjukkan koordinat posisi teks.
> - **labels**: vektor karakter yang menunjukkan teks yang hendak ditulis.

Berikut adalah contoh sintaks untuk memberi label pada sejumlah data yang memiliki kriteria yang kita inginkan dan output yang dihasilkan pada Gambar \@ref(fig:text):


```r
# tandai observasi yang memiliki nilai
# mpg < 15 dan wt > 5
d <- mtcars[mtcars$wt >= 5 & mtcars$mpg <= 15, ]


# plot
plot(mtcars$wt, mtcars$mpg, main="Milage vs. Car Weight",
      xlab="Weight", ylab="Miles/(US) gallon")

# menambahkan text
text(d$wt, d$mpg,  row.names(d),
     cex=0.65, pos=3,col="red")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/text-1} 

}

\caption{Menambahkan teks}(\#fig:text)
\end{figure}

Sedangkan sintaks berikut adalah contoh bagaimana menambahkan persamaan kedalam bidang grafik dan output yang dihasilkan pada Gambar \@ref(fig:text2):


```r
plot(1:10, 1:10, 
     main="text(...) examples\n~~~~~~~~~~~")
text(4, 9, expression(hat(beta) == (X^t * X)^{-1} * X^t * y))
text(7, 4, expression(bar(x) == sum(frac(x[i], n), i==1, n)))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/text2-1} 

}

\caption{Menambahkan teks (2)}(\#fig:text2)
\end{figure}

Fungsi `mtext()` berguna untuk menambahkan teks pada frame sekitar bidang grafik. Format yang digunakan adalah sebagai berikut:


```r
mtext(text, side=3)
```

> **Note: **
>
> - **text**: teks yang akan ditulis.
> - **side**: integer yang menunjukkan lokasi teks yang akan ditulis. Nilai yang dapat dimasukkan antara lain:
>   + **1**: bawah
>   + **2**: kiri
>   + **3**: atas
>   + **4**: kanan.

Berikut adalah contoh penerapan dan output yang dihasilkan pada Gambar \@ref(fig:text3):


```r
plot(1:10, 1:10, 
     main="mtext(...) examples\n~~~~~~~~~~~")
mtext("Magic function", side=3)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/text3-1} 

}

\caption{Menambahkan teks (3)}(\#fig:text3)
\end{figure}

### Menambahkan Garis Pada Plot

Fungsi `abline()` dapat digunakan untuk menamabahkan garis pada plot. Garis yang ditambahkan dapat berupa garis vertikal, horizontal, maupun garis regresi. Format yang digunakan adalah sebagi berikut:


```r
abline(v=y)
```

Berikut adalah contoh sintaks bagaimana menambahkan garis pada sebuah plot dan output yang dihasilkan disajikan pada Gambar \@ref(fig:abline):


```r
# membuat plot
plot(mtcars$wt, mtcars$mpg, main="Milage vs. Car Weight",
      xlab="Weight", ylab="Miles/(US) gallon")

# menambahkan garis vertikal di titik rata-rata weight
abline(v=mean(mtcars$wt), col="red", lwd=3, lty=2)

# menambahkan garis horizontal di titik rata-rata  mpg
abline(h=mean(mtcars$mpg), col="blue", lwd=3, lty=3)

# menambahkan garis regresi
abline(lm(mpg~wt, data=mtcars), lwd=4, lty=4)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/abline-1} 

}

\caption{Menambahkan garis}(\#fig:abline)
\end{figure}

### Merubah Simbol plot dan Jenis Garis

Simbol plot (jenis titik) dapat diubah dengan menambahkan argumen `pch= ` pada plot. Nilai yang dimasukkan pada argumen tersebut adalah integer dengan kemungkinan nilai sebagai berikut:

- pch = 0,square
- pch = 1,circle (default)
- pch = 2,triangle point up
- pch = 3,plus
- pch = 4,cross
- pch = 5,diamond
- pch = 6,triangle point down
- pch = 7,square cross
- pch = 8,star
- pch = 9,diamond plus
- pch = 10,circle plus
- pch = 11,triangles up and down
- pch = 12,square plus
- pch = 13,circle cross
- pch = 14,square and triangle down
- pch = 15, filled square
- pch = 16, filled circle
- pch = 17, filled triangle point-up
- pch = 18, filled diamond
- pch = 19, solid circle
- pch = 20,bullet (smaller circle)
- pch = 21, filled circle blue
- pch = 22, filled square blue
- pch = 23, filled diamond blue
- pch = 24, filled triangle point-up blue
- pch = 25, filled triangle point down blue

Untuk lebih memahami bentuk simbol tersebut, penulis akan menyajikan sintaks yang menampilkan seluruh simbol tersebut pada satu grafik. Output yang dihasilkan disajikan pada Gambar \@ref(fig:symbol):


```r
generateRPointShapes<-function(){
  # menentukan parameter plot
  oldPar<-par()
  par(font=2, mar=c(0.5,0,0,0))
  # produksi titik axis
  y=rev(c(rep(1,6),rep(2,5), rep(3,5), rep(4,5), rep(5,5)))
  x=c(rep(1:5,5),6)
  # plot seluruh titik dan label
  plot(x, y, pch = 0:25, cex=1.5, ylim=c(1,5.5), xlim=c(1,6.5), 
       axes=FALSE, xlab="", ylab="", bg="blue")
  text(x, y, labels=0:25, pos=3)
  par(mar=oldPar$mar,font=oldPar$font )
}

# Print
generateRPointShapes()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/symbol-1} 

}

\caption{Symbol plot}(\#fig:symbol)
\end{figure}

Pada `R` kita juga dapat mengatur jenis garis yang akan ditampilkan pada plot dengan menambahkan argumen `lty= ` (*line type*) pada fungsi plot. Nilai yang dapat dimasukkan adalah nilai integer. Keterangan masing-masing nilai tersebut adalah sebagai berikut:

- lty = 0, blank
- lty = 1, solid (default)
- lty = 2, dashed
- lty = 3, dotted
- lty = 4, dotdash
- lty = 5, longdash
- lty = 6, twodash

Untuk lebih memahaminya, pada sintaks berikut disajikan plot seluruh jenis garis tersebut beserta output yang dihasilkannya pada Gambar \@ref(fig:lty):


```r
generateRLineTypes<-function(){
  oldPar<-par()
  par(font=2, mar=c(0,0,0,0))
  plot(1, pch="", ylim=c(0,6), xlim=c(0,0.7), axes = FALSE ,xlab="", ylab="")
  for(i in 0:6) lines(c(0.3,0.7), c(i,i), lty=i, lwd=3)
  text(rep(0.1,6), 0:6, 
       labels=c("0.'blank'", "1.'solid'", "2.'dashed'", "3.'dotted'", 
                "4.'dotdash'", "5.'longdash'", "6.'twodash'"))
  par(mar=oldPar$mar,font=oldPar$font )
}
generateRLineTypes()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/lty-1} 

}

\caption{Line type}(\#fig:lty)
\end{figure}

### Mengatur Axis Plot

Kita dapat melakukan pengaturan lebih jauh terhadap axis, seperti: menambahkan axis tambahan pada atas dan bawah frame, mengubah rentang nilai axis, serta kustomisasi *tick mark* pada nilai axis. Hal ini diperlukan karena fungsi grafik dasar `R` tidak dapat mengatur axis secara otomatis saat plot baru ditambahkan pada plot pertama dan rentang nilai plot baru lebih besar dibanding plot pertama, sehingga sebagian nilai plot baru tidak ditampilkan pada hasil akhir.

Untuk menambahkan axis pada `R` kita dapat menambahkan fungsi `axis()` setelah plot dilakukan. Format yang digunakan adalah sebagai berikut:


```r
axis(side, at=NULL, labels=TRUE)
```

> **Note: **
>
> - **side**: nilai integer yang mengidikasikan posisi axix yang hendak ditambahkan. Nilai yang dapat dimasukkan adalah sebagai berikut:
>     + **1**: bawah
>     + **2**: kiri
>     + **3**: atas
>     + **4**: kanan.
> - **at**: titik dimana *tick-mark* hendak digambarkan. Nilai yang dapat dimasukkan sama dengan **side**.
> - **labels**: Teks label *tick-mark*. Dapat juga secara logis menentukan apakah anotasi harus dibuat pada *tick mark*.

Berikut contoh sintaks penerapan fungsi tersebut dan output yang dihasilkan pada Gambar \@ref(fig:axis):


```r
# membuat vektor numerik
x <- c(1:4)
y <- x^2

# plot
plot(x, y, pch=18, col="red", type="b",
     frame=FALSE, xaxt="n") # Remove x axis

# menambahkan axis
# bawah
axis(1, 1:4, LETTERS[1:4], col.axis="blue")
# atas
axis(3, col = "darkgreen", lty = 2, lwd = 0.5)
# kanan
axis(4, col = "violet", col.axis = "dark violet", lwd = 2)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/axis-1} 

}

\caption{Menambahkan axis}(\#fig:axis)
\end{figure}

Kita dapat mengubah rentang nilai pada axis menggunakan fungsi `xlim()` dan `ylim()` yang menyatakan vektor nilai masimum dan minimum rentang. Selain itu kita dapat juga melakukan tranformasi baik pada sumbu x dan sumbu y. Berikut adalah argumen yang dapat ditambahkan pada fungsi grafik:

- **xlim**: limit nilai sumbu x dengan format: `xlim(min, max)`.
- **ylim**: limit nilai sumbu x dengan format: `ylim(min, max)`.

Untuk transformasi skala log, kita dapat menambahkan argumen berikut:

- **log="x"**: transformasi log sumbu x.
- **log="y"**: transformasi log sumbu y.
- **log="xy"**: transformasi log sumbu x dan y.

Berikut adalah contoh sintaks penerapan argumen tersebut beserta output yang dihasilkan pada Gambar \@ref(fig:axis2):


```r
# membagi jendela grafik menjadi 1 baris dan 3 kolom
par(mfrow=c(1,3))

# membuat vektor numerik
x<-c(1:10); y<-x*x

# simple plot
plot(x, y)

# plot dengan pengaturan rentang skala
plot(x, y, xlim=c(1,15), ylim=c(1,150))

# plot dengan transformasi skala log
plot(x, y, log="y")
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/axis2-1} 

}

\caption{Mengubah rentang dan skala axis}(\#fig:axis2)
\end{figure}



Kita dapat melakukan kustomisasi pada *tick mark*. Kustomisasi yang dapat dilakukan adalah merubah warna, *font style*, ukuran font, orientasi, serta menyembunyikan *tick mark*.

Argumen yang ditambahkan adalah sebagai berikut:

- **col.axis**: warna *tick mark*.
- **font.axis**: integer yang menunjukkan *font style*. Sama dengan pengaturan judul.
- **cex.axis**: pengaturan ukuran *tick mark*.
- **las**: mengatur orientasi *tick mark*. Nilai yang dapat dimasukkan adalah sebagai berikut:

  + **0**: paralel terhadap posisi axis (default)
  + **1**: selalu horizontal
  + **2**: selalu perpendikular dengan posisi axis
  + **3**: selalu vertikal

- **xaxt** dan **yaxt**: karakter untuk menunjukkan apakah axis akan ditampilkan atau tidak. nilai dapat berupa "n"(sembunyika) dan "s"(tampilkan).

Berikut adalah contoh penerapan argumen tersebut beserta output pada Gambar \@ref(fig:axis3):


```r
# membuat vektor numerik
x<-c(1:10); y<-x*x

# plot
plot(x,y,
     # warna
     col.axis="red",
     # font style
     font.axis=2,
     # ukuran
     cex=1.5,
     # orientasi
     las=3,
     # sembunyikan sumbu x
     xaxt="n")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/axis3-1} 

}

\caption{Kustomisasi tick mark}(\#fig:axis3)
\end{figure}

### Mengatur Warna

Pada fungsi dasar `R`, warna dapat diatur dengan mengetikkan nama warna maupun kode hexadesimal. Selain itu kita juga dapat menamambahkan warna lain melalui library lain yang tidak dijelaskan pada chapter ini.

Untuk penggunaan warna hexadesima kita perlu mengetikkan "#" yang diukuti oleh 6 kode warna. Untuk memperlajari kode-kode dan warna yang dihasilkan, silahkan pembaca mengunjungi situs <http://www.visibone.com/>.

Pada sintaks berikut disajikan visualisasi nama-nama warna bawaan yang ada pada `R`. Output yang dihasilkan disajikan pada Gambar \@ref(fig:color):


```r
showCols <- function(cl=colors(), bg = "grey",
                     cex = 0.75, rot = 30) {
    m <- ceiling(sqrt(n <-length(cl)))
    length(cl) <- m*m; cm <- matrix(cl, m)
    require("grid")
    grid.newpage(); vp <- viewport(w = .92, h = .92)
    grid.rect(gp=gpar(fill=bg))
    grid.text(cm, x = col(cm)/m, y = rev(row(cm))/m, rot = rot,
              vp=vp, gp=gpar(cex = cex, col = cm))
}

# print 60 nama warna pertama
showCols(bg="gray20", cl=colors()[1:60], rot=30, cex=0.9)
```

```
## Loading required package: grid
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/color-1} 

}

\caption{Nama warna}(\#fig:color)
\end{figure}

## Alternatif Library Dasar Lain

Kita juga dapat melakukan visualisasi menggunakan library lain yang memiliki tampilan mirip dengan fungsi visualisasi dasar `R`. Bedanya adalah library-library ini memberikan fungsi tambahan sehingga visualisasi yang dihasilkan menjadi lebih praktis.

### Scatterplot Menggunakan Library car

Library `car` menyediakan alternatif lain visualisasi menggunakan scatterplot. Berikut adalah contoh sintaks dan output yang dihasilkan pada Gambar \@ref(fig:carscatter):


```r
# memasang paket
# install.packages("car")

# memuat paket
library(car)

# plot
scatterplot(Volume~Height, data=trees)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/carscatter-1} 

}

\caption{Enhanced scatterplot}(\#fig:carscatter)
\end{figure}

Pada grafik tersebut terkandung beberapa elemen penting, yaitu:

- titik observasi
- garis regresi (garis lurus)
- non-parametric regression smooth (*dashed line*)
- garis smoothed conditional (*point dashed line*)
- box plot masing-masing variabel.

### Matriks Scatterplot Menggunakan Library psych

FUngsi `pairs.panels()` pada library `psych` dapat digunakan untuk membuat matriks scatterplot. Grafik yang dihasilkan juga lebih ringkas dan menampilkan fungsional lain pada bagian diagonal lain berupa histogram dan density plot yang dapat menunjukkan distribusi dari variabel yang ada. Selain itu pada fungsionalitas grafik juga dapat ditingkatkan dengan penambahan nilai korelasi antar variabel yang secara default ditambahkan pada panel atas. Berikut adalah contoh sintaks dan output yang dihasilkan pada Gambar \@ref(fig:psychscatter):


```r
# memasang paket
# install.packages("psych")

# memuat paket
library(psych)

# plot
pairs.panels(trees, 
             method = "pearson", # metode korelasi
             hist.col = "grey",
             density = TRUE,  # menampilkan plot densitas
             ellipses = FALSE, # menampilkancorrelation ellipses
             lm = TRUE # menampilkan garis regresi linier
             )
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/psychscatter-1} 

}

\caption{Enhanced scatterplot matrices}(\#fig:psychscatter)
\end{figure}

### Box Plot Menggunakan Library gplots

Fungsi `boxplot2()` pada paket `gplots` memberikan fungsionalitas lebih dibandingkan box plot yang dihasilkan dari fungsi dasar `R`. Plot yang dihasilkan akan menampilkan jumlah observasi pada tiap box. Berikut adalah contoh sintask penerapan dan output yang dihasilkan pada Gambar \@ref(fig:gplotsboxplot2):


```r
# memasang paket
# install.packages("gplots")

# memuat paket
library(gplots)

# plot
boxplot2(len ~ dose, data = ToothGrowth)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gplotsboxplot2-1} 

}

\caption{Enhanced box plot}(\#fig:gplotsboxplot2)
\end{figure}

### QQ Plot Menggunakan Library car

Fungsi `qqPlot()` pada library `car` dapat pula digunakan untuk membuat qq plot. Kelebihannya adalah qqplot yang dihasilkan akan dilengkapi dengan garis referensi yang memudahkan dalam membaca apakah data masih dalam rentang distribusi normal atau tidak. Selain itu, untuk membuatnya juga hanya diperlukan satu perintah saja. Hal ini tentu berbeda ketika kita menggunakan fungsi dasar `R`. Berikut adalah contoh sintask penerapan dan output yang dihasilkan pada Gambar \@ref(fig:carqqplot):


```r
# memasang paket
# install.packages("car")

# memuat paket
library(car)

# plot
qqPlot(trees$Height)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/carqqplot-1} 

}

\caption{Enhanced qq plot}(\#fig:carqqplot)
\end{figure}

```
## [1]  3 20
```

### Plot Group Means Menggunakan Library gplots

Plot ini akan sering kita gunakan saat melakukan analisis statistik menggunakan anova baik anova satu arah maupun dua arah. Plot ini berguna untuk melihat adanya interaksi antar faktor saat melakukan analisis anova dua arah. Berikut adalah contoh sintask penerapan dan output yang dihasilkan pada Gambar \@ref(fig:plotmeans):


```r
# memasang paket
# install.packages("gplots")

# memuat paket
library(gplots)

# plot
plotmeans(len ~ dose, data = ToothGrowth)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/plotmeans-1} 

}

\caption{Plot group means}(\#fig:plotmeans)
\end{figure}

## Referensi

1. Maindonald, J.H. 2008. **Using R for Data Analysis and Graphics Introduction, Code and Commentary**. Centre for Mathematics and Its Applications Australian National University.
2. Scherber, C. 2007. **An introduction to statistical data analysis using R**. R_Manual Goettingen.
3. Venables, W.N. Smith D.M. and R Core Team. 2018. **An Introduction to R**. R Manuals.
4. STHDA. **R Base Graphs**. <http://www.sthda.com/english/wiki/r-base-graphs>









<!--chapter:end:04-visualisasi-data-menggunakana-fungsi-dasar-R.Rmd-->

<style>
body{
text-align: justify}
</style>

# Visualisasi Data Menggunakan GGPLOT

Library `ggplot2` merupakan implementasi dari *The Grammar of Graphics* yang ditulis oleh **Leland Wilkinson**. `ggplot2` merupakan library yang dikembangkan oleh **Hadley Wicham** ketika ia sedang menempuh kuliah di **Lowa State Universuty** dan masih dikembangkan hingga sekarang.

`ggplot2` merupakan paket visualisasi yang powerfull. Kita dapat menggunakannya bersamaan dengan *piping operator* yang disediakan oleh paket `dplyr` sehingga menambah kemudahan kita dalam melakukan analisis data.

Grafik `ggplot2` terdiri dari sejumlah komponen kunci. Berikut adalah sejumlah komponen kunci yang membentuk grafik `ggplot2`.

- **data frame**: menyimpan semua data yang akan ditampilkan di plot.
- **aesthetic mapping**: menggambarkan bagaimana data dipetakan ke warna, ukuran, bentuk, lokasi. Dalam plot diberikan pada fungsi `aes()`
- **geoms**: objek geometris seperti titik, garis, bentuk.
- **facets**: menjelaskan bagaimana plot bersyarat / panel harus dibangun.
- **stats**: transformasi statistik seperti binning, quantiles, smoothing.
- **scales**: skala apa yang digunakan oleh *aesthetic map* (contoh: pria = merah, wanita = biru).
- **coordinate system**: menggambarkan sistem di mana lokasi geom akan digambarkan.

Sebelum kita mulai memcoba melakukan visualisasi data menggunakan `ggplot2`, kita perlu menginstall dan memuat terlebih dahulu library `ggplot2`. Berikut adalah sintaks yang digunakan untuk menginstall dan memuat paket `ggplot2`:


```r
# memasang paket
# install.packages('ggplot2')

# memuat paket
library(ggplot2)
```

Dataset yang akan kita gunakan adalah dataset `gapminder`. Dataset ini berisi data demografi penduduk dari berbagai negara dan benua. Untuk dapat menggunakannya kita perlu menginstall dan memuatnya terlebih dahulu. Berikut adalah sintaks untuk menginstall dan memuat dataset tersebut:


```r
# memasang paket
# install.packages("gapminder")

# memuat paket
library(gapminder)

# memuat paket dplyr dan tibble
library(dplyr)
library(tibble)
```


```r
# melihat struktur dataset
glimpse(gapminder)
```

```
## Observations: 1,704
## Variables: 6
## $ country   <fct> Afghanistan, Afghanistan, Afghan...
## $ continent <fct> Asia, Asia, Asia, Asia, Asia, As...
## $ year      <int> 1952, 1957, 1962, 1967, 1972, 19...
## $ lifeExp   <dbl> 28.80, 30.33, 32.00, 34.02, 36.0...
## $ pop       <int> 8425333, 9240934, 10267083, 1153...
## $ gdpPercap <dbl> 779.4, 820.9, 853.1, 836.2, 740....
```

```r
# melihat variabel year
unique(gapminder$year)
```

```
##  [1] 1952 1957 1962 1967 1972 1977 1982 1987 1992 1997
## [11] 2002 2007
```

Dataset gapminder memiliki 6 variabel dan 1704 observasi. 20 observasi pertama dataset gapminder dapat dilihat pada Tabel \@ref(tab:gapminder)

\begin{table}[t]

\caption{(\#tab:gapminder)20 observasi pertama dataset gapminder}
\centering
\begin{tabular}{l|l|r|r|r|r}
\hline
country & continent & year & lifeExp & pop & gdpPercap\\
\hline
Afghanistan & Asia & 1952 & 28.80 & 8425333 & 779.4\\
\hline
Afghanistan & Asia & 1957 & 30.33 & 9240934 & 820.9\\
\hline
Afghanistan & Asia & 1962 & 32.00 & 10267083 & 853.1\\
\hline
Afghanistan & Asia & 1967 & 34.02 & 11537966 & 836.2\\
\hline
Afghanistan & Asia & 1972 & 36.09 & 13079460 & 740.0\\
\hline
Afghanistan & Asia & 1977 & 38.44 & 14880372 & 786.1\\
\hline
Afghanistan & Asia & 1982 & 39.85 & 12881816 & 978.0\\
\hline
Afghanistan & Asia & 1987 & 40.82 & 13867957 & 852.4\\
\hline
Afghanistan & Asia & 1992 & 41.67 & 16317921 & 649.3\\
\hline
Afghanistan & Asia & 1997 & 41.76 & 22227415 & 635.3\\
\hline
Afghanistan & Asia & 2002 & 42.13 & 25268405 & 726.7\\
\hline
Afghanistan & Asia & 2007 & 43.83 & 31889923 & 974.6\\
\hline
Albania & Europe & 1952 & 55.23 & 1282697 & 1601.1\\
\hline
Albania & Europe & 1957 & 59.28 & 1476505 & 1942.3\\
\hline
Albania & Europe & 1962 & 64.82 & 1728137 & 2312.9\\
\hline
Albania & Europe & 1967 & 66.22 & 1984060 & 2760.2\\
\hline
Albania & Europe & 1972 & 67.69 & 2263554 & 3313.4\\
\hline
Albania & Europe & 1977 & 68.93 & 2509048 & 3533.0\\
\hline
Albania & Europe & 1982 & 70.42 & 2780097 & 3630.9\\
\hline
Albania & Europe & 1987 & 72.00 & 3075321 & 3738.9\\
\hline
\end{tabular}
\end{table}

## Scatterplot

Scatterplot dapat dibuat pada `ggplot2` menggunakan fungsi `geom_point()`. Format sederhananya dituliskan sebagai berikut:


```r
ggplot(data, aes(...))+
  geom_point(size, color, shape)
```

Berikut adalah contoh sederhana scatterplot variabel `lifeExp` terhadap variabel `gdpPercap`. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggscatter):


```r
ggplot(gapminder, aes(gdpPercap, lifeExp))+
  geom_point()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggscatter-1} 

}

\caption{Scatterplot lifeExp vs gdpPercap}(\#fig:ggscatter)
\end{figure}

Kita dapat mengubah warna, jenis, dan ukuran titik pada scatterplot. Pengubahan warna dan jenis titik berguna untuk menunjukkan grup data pada grafik. Sedangkan perubahan ukuran titik sangat berguna untuk menunjukkan nilai variabel lain khususnya variabel kontinyu pada sebuah titik. Berikut adalah contoh penerapannya. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggscatter2) sampai dengan Gambar \@ref(fig:ggscatter4):


```r
ggplot(gapminder, aes(gdpPercap,lifeExp, color=continent))+
  geom_point()+
  # merubah sumbu x kedalam fungsi log
  scale_x_log10()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggscatter2-1} 

}

\caption{Scatterplot lifeExp vs gdpPercap tiap benua (1)}(\#fig:ggscatter2)
\end{figure}


```r
ggplot(gapminder, aes(gdpPercap,lifeExp, shape=continent))+
  geom_point()+
  # merubah sumbu x kedalam fungsi log
  scale_x_log10()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggscatter3-1} 

}

\caption{Scatterplot lifeExp vs gdpPercap tiap benua (2)}(\#fig:ggscatter3)
\end{figure}


```r
ggplot(gapminder, aes(gdpPercap,lifeExp, 
                      size=pop, color=continent))+
  geom_point()+
  # merubah sumbu x kedalam fungsi log
  scale_x_log10()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggscatter4-1} 

}

\caption{Scatterplot lifeExp vs gdpPercap dan populasi tiap negara dan benua}(\#fig:ggscatter4)
\end{figure}

Untuk menujukkan asosiasi antara dua variabel kontinyu kita juga dapat menambahkan garis regresi dan confidence interval garis regresinya. Fungsi yang digunakan adalah `geom_smooth()`. Secara default fungsi tersebut akan membuat garis loess regression pada grafik. Agar dapat membuat garis regresi linier kita perlu menambahkan argumen `method="lm"`. Selain itu, jika kita tidak ingin menampilkan garis confidence interval kita dapat menambahkan argumen `se=FALSE`. Format sederhananya disajikan pada sintaks berikut:


```r
geom_smooth(method="auto", se=TRUE, fullrange=FALSE, level=0.95)
```

> **Note: **
>
> - **method**: metode penghalusan yang digunakan. Nilai yang dapat dimasukkan adalah lm, glm, gam, loess, rlm.
> 
>    + method="loess": merupakan nilai default pada fungsi dan menghasilkan metode penghalusan loess regression.
>    + method="lm": menghasilkan metode penghalusan regresi linier. Kita juga dapat melakukan spesifikasi terhadap fungsi persamaan regresi yang digunakan dengan menambahkan argumen formula=y~x....
>
> - **se**: nilai logis. Jika TRUE garis confidence interval akan ditampilkan sepanjang garis penghalusan.
> - **fullrange**: nilai logis. Jika TRUE kecocokan mencakup seluruh plot.
> - level: level confidence interal yang digunakan. Secara default bernilai 0.95.

Berikut adalah contoh sintaks penerapan pada variabel `gdpPercap` dan `lifeExp`. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggscatter5):


```r
ggplot(gapminder, aes(gdpPercap,lifeExp))+
  geom_point()+
  # merubah sumbu x kedalam fungsi log
  scale_x_log10()+
  # menambahkan smoothing method
  geom_smooth(method="lm", level=0.99)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggscatter5-1} 

}

\caption{Scatterplot lifeExp vs gdpPercap dengan garis penghalusan regresi linier}(\#fig:ggscatter5)
\end{figure}

## Box Plot dan Violin Plot

Box plot merupakan visualisasi yang powerful dalam menggambarkan distribusi data, melihat adanya outlier, serta membandingkan distribusi antar data. Format visualisasi dapat dituliskan sebagai berikut:


```r
ggplot(data, aes(...))+
  geom_boxplot(geom_boxplot(outlier.colour="black", 
                            outlier.shape=16,
                            outlier.size=2, 
                            notch=FALSE))
```

> **Note: **
>
> - **outlier.colour, outlier.shape, outlier.size**: Warna, bentuk dan ukuran untuk titik-titik outlier.
> - **notch**: nilai logis. Jika TRUE, buat **notched box plot**. *Notch* menunjukkan *confidence interval* di sekitar median yang biasanya didasarkan pada median $\pm1,58\cdot\frac{\left(IQR\right)}{\sqrt{\left(n\right)}}$. *Notch* digunakan untuk membandingkan kelompok; jika takik dua kotak tidak tumpang tindih, ini adalah bukti kuat bahwa median berbeda.

Berikut merupakan contoh visualisasi variabel `lifeExp` pada dataset `gapminder`. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggboxplot):


```r
ggplot(gapminder, aes("", lifeExp))+
  geom_boxplot()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggboxplot-1} 

}

\caption{Box plot variabel lifeExp}(\#fig:ggboxplot)
\end{figure}

Kita dapat melakukan visualisasi bagi setiap kelompok data. Pada sintaks berikut visualisasi dilakukan untuk variabel `lifeExp` pada tiap `continent`. Pada contoh berikut akan ditampilkan cara menmabahkan titik rata-rata dan warna pada masing-masing grup. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggboxplot2):


```r
ggplot(gapminder, aes(continent, lifeExp, color=continent))+
  geom_boxplot()+
  stat_summary(fun.y=mean, geom="point", 
               shape=23, size=3, color="red")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggboxplot2-1} 

}

\caption{Box plot variabel lifeExp pada tiap continent}(\#fig:ggboxplot2)
\end{figure}


Misalkan kita ingin mengetahui perubahan distribusi dari variabel `lifeExp` pada masing-masing `continet` pada tahun 1952 dan 2007. Untuk melakukannya kita perlu melakukan subset pada dataset `gapminder` untuk memfilter data pada tahun 1952 dan 2007. Data selanjutnya dilakukan input kedalam fungsi `ggplot()`. Berikut adalah contoh sintaks yang digunakan. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggboxplot3):


```r
gapminder %>%
  filter(year==1952 | year==2007) %>%
  ggplot(aes(continent, lifeExp, fill=factor(year)))+
  geom_boxplot(notch=TRUE)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggboxplot3-1} 

}

\caption{Box plot variabel lifeExp pada tiap continent (1952 dan 2007)}(\#fig:ggboxplot3)
\end{figure}

Berdasarkan Gambar \@ref(fig:ggboxplot3) terlihat bahwa usia harapan hidup pada tiap benua meningkat sejak tahun 1952 sampai 2007. Selain itu, peningkatan tersebut bersifat signifikan yang ditunjukkan dari tidak adanya *notch* yang saling overlap pada masing-masing benua.

Untuk lebih detailnya kita akan coba melakukan visualisasi pada benua Asia untuk melihat perubahan variabel `lifeExp`. Berikut adalah sintaks yang digunakan dan output yang dihasilkan disajikan pada Gambar \@ref(fig:ggboxplot4):


```r
gapminder %>%
  filter(continent=="Asia") %>%
  ggplot(aes(factor(year), lifeExp))+
  geom_boxplot()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggboxplot4-1} 

}

\caption{Box plot variabel lifeExp Benua Asia}(\#fig:ggboxplot4)
\end{figure}

Violin plot memiliki kesamaan dengan box plot. Perbedaanya terletak pada violin plot tidak hanya menyajikan data titik-titikkuartil data, namun violin plot juga menampilkan kernel probabilitas distibusi data. Fungsi yang digunakan untuk membuatnya adalah `geom_violin()`.

Pada dataset `gapminder` kita ingin meisualisasikan distribusi `lifeExp` pada masing-masing `continent`. Berikut adalah contoh sintaks untuk membuat visualisasi dasar violin plot. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggviolin):


```r
gapminder %>%
  ggplot(aes(continent, lifeExp, fill=continent))+
  # violin plot
  geom_violin()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggviolin-1} 

}

\caption{Violin plot variabel lifeExp pada masing-masing benua}(\#fig:ggviolin)
\end{figure}

Kita juga dapat melakukan modifikasi terhadap violin plot tersebut seperti penambahan titik kuartil, titik mean dan modifikasi terhadap warna tampilaknnya. COntoh sintaksnya dan output disajikan pada Gambar \@ref(fig:ggviolin2):


```r
gapminder %>%
  ggplot(aes(continent, lifeExp, fill=continent))+
  # violin plot
  geom_violin()+
  # menambahkan boxplot dengan lebar 0.1
  geom_boxplot(width=0.1, fill="white")+
  # menambahkan titik mean
  stat_summary(fun.y=mean, geom="point",
               # ukuran dan jenis titik
               size=1, shape=23,
               # warna titik
               color="red", fill="white")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggviolin2-1} 

}

\caption{Violin plot variabel lifeExp pada masing-masing benua (2)}(\#fig:ggviolin2)
\end{figure}

## Bar Plot

Pada `ggplot2` bar plot dapat dibuat menggunakan fungsi `geom_bar()`. Untuk membuat bar plot, langkah pertama yang perlu dilakukan adalah membuat tabulasi data variabel terlebih dahulu. Berikut adalah contoh sintaks untuk membuat bar plot dari rata-rata `lifeExp` pada masing-masing `continent`. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggbar):


```r
gapminder %>%
  # kelompokkan berdasarkan continet
  group_by(continent)%>%
  # membuat ringkasan data
  summarize(mean_lifeExp=mean(lifeExp))%>%
  # urutkan dari yang terbesar
  arrange(desc(mean_lifeExp))%>%
  # plot
  ggplot(aes(continent, mean_lifeExp))+
  # membuat bar plot berdasarkan nilai observasi
  geom_bar(stat="identity")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggbar-1} 

}

\caption{Bar plot rata-rata lifeExp masing-masing benua}(\#fig:ggbar)
\end{figure}

Kita juga dapat membuat bar plot dengan garis confidence interval. Untuk melakukannya kita perlu terlebih dahulu menghitung standard error dari data. Standard error selanjutnya digunakan untuk menghitung nilai atas dan bawah dari nilai rata-rata. Berikut adalah contoh visualisasi bar plot dengan confidence interval (Gambar \@ref(fig:ggbar2)):


```r
gapminder %>%
  # kelompokkan berdasarkan continet
  group_by(continent)%>%
  # membuat ringkasan data
  summarize(mean_lifeExp=mean(lifeExp),
            n=n(), sd=sd(lifeExp), 
            se=sd/sqrt(n))%>%
  # plot
  ggplot(aes(continent, mean_lifeExp))+
  # membuat bar plot
  geom_bar(stat="identity", color="white")+
  # menambahkan error bar
  geom_errorbar(aes(ymin=mean_lifeExp-se,
                    ymax=mean_lifeExp+se),
                width=0.2)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggbar2-1} 

}

\caption{Bar plot rata-rata lifeExp masing-masing benua dengan confidence interval}(\#fig:ggbar2)
\end{figure}

Kita juga dapat melakukannya pada visualisasi data beberapa grup. Berikut adalah contoh sintaks dan output (Gambar \@ref(fig:ggbar3)) bar plot dengan beberapa grup:


```r
gapminder %>%
  # filter data tahun 1952 dan 2007
  filter(year==1952|year==2007)%>%
  # Ubah year menjadi factor
  mutate(year=as.factor(year))%>%
  # kelompokkan berdasarkan continet
  group_by(continent,year)%>%
  # membuat ringkasan data
  summarize(mean_lifeExp=mean(lifeExp),
            n=n(), sd=sd(lifeExp), 
            se=sd/sqrt(n))%>%
  # plot
  ggplot(aes(continent, mean_lifeExp, 
             fill=year))+
  # membuat bar plot
  geom_bar(stat="identity", 
           position=position_dodge())+
  # menambahkan error bar
  geom_errorbar(aes(ymin=mean_lifeExp-se,
                    ymax=mean_lifeExp+se),
                width=0.2,
                position=position_dodge(0.9))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggbar3-1} 

}

\caption{Bar plot rata-rata lifeExp masing-masing benua (1952 dan 2007) dengan confidence interval}(\#fig:ggbar3)
\end{figure}

## Line Plot

Line plot dapat digunakan untuk menunjukkan adanya perubahan pada selang waktu tertentu. Pada `ggplot2`, line plot dapat dibuat menggunakan fungsi `geom_line()`. Berikut adalah contoh sintaks dan grafik (Gambar \@ref(fig:ggline)) untuk membuat line plot:


```r
gapminder%>%
  # kelompokkan data berdasarkan year dan continent
  group_by(year,continent)%>%
  # ringkasan data
  summarize(mean_lifeExp=mean(lifeExp))%>%
  # plot
  ggplot(aes(year, mean_lifeExp, 
             linetype=continent))+
  # membuat line plot
  geom_line()+
  # menambahkan point
  geom_point()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggline-1} 

}

\caption{Line plot lifeExp masing-masing benua }(\#fig:ggline)
\end{figure}

Kita juga dapat menambahkan error bar pada line plot. Berikut adalah contoh sintak dan grafik (Gambar \@ref(fig:ggline2)) yang dihasilkan:


```r
gapminder%>%
  # filter benua asia
  filter(continent=="Asia")%>%
  # kelompokkan data berdasarkan year dan continent
  group_by(year)%>%
  # ringkasan data
  summarize(mean_lifeExp=mean(lifeExp), 
            sd=sd(lifeExp))%>%
  # plot
  ggplot(aes(year, mean_lifeExp))+
  # membuat line plot
  geom_line()+
  # menambahkan point
  geom_point(size=2)+
  # menambahkan error bar
  geom_errorbar(aes(ymin=mean_lifeExp-sd,
                    ymax=mean_lifeExp+sd),
                width=0.2, color="red")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggline2-1} 

}

\caption{Histogram lifeExp }(\#fig:ggline2)
\end{figure}

## Pie Chart

Pie chart pada `ggplot2` dapat dibuat menggunakan fungsi `geom_bar()` dan `coord_polar()`.Berikut adalah contoh sintaks yang digunakan dan output (Gambar \@ref(fig:ggpie)) yang dihasilkan:


```r
total <- sum(gapminder$pop)
gapminder%>%
  # kelompokkan berdasarkan continent
  group_by(continent)%>%
  # ringkasan data 
  summarize(pop=sum(as.numeric(pop)), percent=(pop/total)*100)%>%
  ggplot(aes(x="", percent, fill=continent))+
  geom_bar(stat="identity")+
  coord_polar("y", start=0)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggpie-1} 

}

\caption{Pie chart pop}(\#fig:ggpie)
\end{figure}


## Histogram dan Desity Plot

Histogram pada `ggplot2` dapat dibuat dengan fungsi `geom_histogram()`. Berikut adalah sintaks untuk membuat hitogram pada variabel `lifeExp`. Output yang dihasilkan disajikan pada Gambar \@ref(fig:gghist):


```r
gapminder %>%
  ggplot(aes(lifeExp))+
  geom_histogram()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gghist-1} 

}

\caption{Histogram lifeExp }(\#fig:gghist)
\end{figure}

Kita dapat membuat grafik histogram berdasarkan grup data. Pada contoh sebelumnya dibuat histogram berdasarkan variabel `continent`. Berikut adalah sintaks dan output yang dihasilkan pada Gambar \@ref(fig:gghist2):


```r
gapminder %>%
  ggplot(aes(lifeExp, fill=continent))+
  geom_histogram(alpha=0.5, 
                 # atur posisi agar sesuai grup
                 position="identity",
                 color="black")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gghist2-1} 

}

\caption{Histogram lifeExp berdasarkan benua}(\#fig:gghist2)
\end{figure}

Density plot dapat dibuat dengan menggunakan fungsi `geom_density()`. Berikut adalah contoh sintaks untuk membuat density plot variabel `lifeExp`. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggdens):


```r
gapminder %>%
  ggplot(aes(lifeExp))+
  geom_density()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggdens-1} 

}

\caption{Density plot lifeExp }(\#fig:ggdens)
\end{figure}

Kita juga dapat membuat grafik density berdasarkan grup data. Pada contoh sebelumnya dibuat density plot berdasarkan variabel `continent`. Berikut adalah sintaks dan output yang dihasilkan pada Gambar \@ref(fig:ggdens2):


```r
gapminder %>%
  ggplot(aes(lifeExp, fill=continent))+
  geom_density(alpha=0.5, 
                 # atur posisi agar sesuai grup
                 position="identity",
                 color="black")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggdens2-1} 

}

\caption{Density plot lifeExp berdasarkan benua}(\#fig:ggdens2)
\end{figure}

Jika dinginkan kita juga dapat menambahkan density plot pada histogram. Pada Gambar \@ref(fig:hist) ditambahkan density plot sehingga dihasilkan output seperti Gambar \@ref(fig:ggdenshist).


```r
gapminder %>%
  ggplot(aes(lifeExp))+
  geom_histogram(aes(y=..density..),
                 # spesifikasi warna bar
                 color="black", fill="white")+
  geom_density(fill="red", alpha=0.3)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggdenshist-1} 

}

\caption{histogram dan density plot lifeExp }(\#fig:ggdenshist)
\end{figure}

## QQ Plot

QQ plot pada paket `ggplot2` dapat dibuat dengan menggunakan fungsi `stat_qq()`. Berikut adalah contoh sintaks untuk melakukannya. Output yang dihasilkan disajikna pada Gambar \@ref(fig:ggqq).


```r
ggplot(gapminder, aes(sample=lifeExp))+
  # qq plot
  stat_qq()+
  # garis referensi
  stat_qq_line()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggqq-1} 

}

\caption{QQ plot variabel lifeExp}(\#fig:ggqq)
\end{figure}

## Dot Plot

Dot plot dapat dibuat menggunakan fungsi `geom_dotplot` atau `geom_jitter()`. Perbedaan keduanya adalah `geom_jitter()` menambahkan *noise* pada plot sehingga mencegah terjadinya *overplotting*. Berikut adalah contoh sintaks untuk membuat dotplot pada multiple group dan output yang dihasilkan pada Gambar \@ref(fig:dotplot):


```r
gapminder %>%
  filter(year==1952 | year==2007) %>%
  ggplot(aes(continent, lifeExp, fill=factor(year)))+
  geom_dotplot(binaxis="y", 
               # spesifikasi posisi plot
               stackdir="center",
               position=position_dodge(0.8),
               size=0.1)
```

```
## Warning: Ignoring unknown parameters: size
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/dotplot-1} 

}

\caption{Dot plot variabel lifeExp masing-masing benua (1952-2007)}(\#fig:dotplot)
\end{figure}

Kita juga dapat menambahkan plot dari dari plot yang sudah ada seperti box plot atau violin plot. Berikut adalah contoh sintaks dan output yang dihasilkan pada Gambar \@ref(fig:dotplot2):


```r
gapminder %>%
  filter(year==1952 | year==2007) %>%
  ggplot(aes(continent, lifeExp, fill=factor(year)))+
  # box plot dibawah
  geom_boxplot(position=position_dodge(0.8))+
  # dot plot diatas
  geom_dotplot(binaxis="y", 
               # spesifikasi posisi plot
               stackdir="center",
               position=position_dodge(0.8))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/dotplot2-1} 

}

\caption{Dot plot variabel lifeExp masing-masing benua (1952-2007) (2)}(\#fig:dotplot2)
\end{figure}

## ECDF Plot

*Empirical Cumulative Density FUnction* (ECDF) plot merupakan grafik yang digunakan untuk menggambarkan ditribusi suatu data. Dari grafik ini kita dapat mengetahui faraksi suatu data baik yang terendah maupun yang tertinggi. ECDF pada `ggplot2` dapat dibuat dengan dua cara yaitu dengan `geom_line()` dan `stat_ecdf()`. Jika menggunakan fungsi `geom_line()` kita perlu membuat fraksi kumulatif dari variabel yang akan kita plotkan. Sedangkan dengan menggunakan `stat_ecdf()`, kita tidak perlu melakukannya karena fungsi tersebut akan secara otomatis memproses data kita. Berikut adalah sintaks dan output (Gambar \@ref(fig:ggecdf)) contoh ecdf:


```r
ggplot(gapminder, aes(lifeExp))+
  stat_ecdf(geom="line")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggecdf-1} 

}

\caption{ECDF plot variabel lifeExp}(\#fig:ggecdf)
\end{figure}

## Parameter Grafik

Pada bagian ini penulis akan menjelaskan bagaimana cara mengatur parameter grafik seperti judul grafik, legend, warna, tema, dll. Pengaturan parameter grafik pada `ggplot2` sebenarnya jauh lebih sederhana dibandingkan dengan fungsi dasar visualisasi `R`. Selain itu, kita dapat membuat tampilan grafik kita jauh lebih menarik dengan membuat tema kustom pada grafik kita.

### Merubah Judul Grafik, Keterangan Axis dan Legend

Untuk merubah judul grafik dan keterangan axis kita dapat melakukannya melalui dua cara. Cara pertama adalah dengan memasukkan mengubahnya satu persatu menggunakan fungsi `ggtitle()` (judul grafik), `xlab()` (keterangan sumbu x), dan `ylab()` (keterangan pada sumbu y). Cara kedua adalah dengan menggunakan fungsi `labs()` dimana selain dapat mengubah judul grafik dan keterangan axis fungsi tersebut dapat juga digunakan untuk mengubah keterangan legend.

Pada sintaks berikut penulis akan memberikan contoh bagaimana mengubah judul grafik dan keterangan axis menggunakan dua cara tersebut. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggtitle).


```r
# Cara 1
ggplot(gapminder, aes(continent, gdpPercap, fill=continent))+
  # membuat box plot
  geom_boxplot()+
  # menambahkan judul
  ggtitle("GDP Per Capita Tiap Benua")+
  # mengubah keterangan axis
  xlab("Benua")+
  ylab("GDP Per Kapita")
```


```r
# cara 2
ggplot(gapminder, aes(continent, gdpPercap, fill=continent))+
  # membuat box plot
  geom_boxplot()+
  # kustomisasi judul dan keterangan axis
  labs(title="GDP Per Capita Tiap Benua",
       x="Benua", y="GDP Per Kapita")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggtitle-1} 

}

\caption{Mengubah judul grafik dan keterangan axis}(\#fig:ggtitle)
\end{figure}

Pada Gambar \@ref(fig:ggtitle) kita belum mengubah keterangan legend. Berikut adalah sintaks untuk mengubah keterangan legend pada grafik tersebut beserta output yang disajikan pada Gambar \@ref(fig:ggtitle2).


```r
# cara 2
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna box berdasarkan benua
                      fill=continent))+
  # membuat box plot
  geom_boxplot()+
  # kustomisasi judul dan keterangan axis
  labs(title="GDP Per Capita Tiap Benua",
       x="Benua", y="GDP Per Kapita",
       # mengubah keterangan legend
       fill="Benua")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggtitle2-1} 

}

\caption{Mengubah keterangan legend pada grafik}(\#fig:ggtitle2)
\end{figure}

Judul, keterangan axis, dan keterangan legend dapat dikustomisasi menggunakan fungsi `theme()` dan `element_text()`. Berikut adalah format yang digunakan:


```r
# Judul
<ggplot> + theme(plot.title = element_text(family, face, colour, size))
# keterangan sumbu x
<ggplot> + theme(axis.title.x = element_text(family, face, colour, size))
# keterangan sumbu y
<ggplot> + theme(axis.title.y = element_text(family, face, colour, size))
# keterangan legend
<ggplot> + theme(axis.title.y = element_text(family, face, colour, size))
```

> **Note: **
>
> - **family**: font family.
> - **face**: tampilan font. Nilai yang dapat digunakan antara lain:  “plain”, “italic”, “bold” dan “bold.italic”.
> - **colour**: warna teks.
> - **size**: ukuran teks

Berikut adalah contoh penerapan fungsi tersebut pada grafik Gambar \@ref(fig:ggtitle2). Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggtitle3).


```r
# cara 2
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna box berdasarkan benua
                      fill=continent))+
  # membuat box plot
  geom_boxplot()+
  # kustomisasi judul dan keterangan axis
  labs(title="GDP Per Capita Tiap Benua",
       x="Benua", y="GDP Per Kapita",
       # mengubah keterangan legend
       fill="Benua")+
  theme(
      plot.title = element_text(color="red", size=14, face="bold.italic"),
      axis.title.x = element_text(color="blue", size=14, face="bold"),
      axis.title.y = element_text(color="#993333", size=14, face="bold"),
      legend.text = element_text(colour="blue", size=10, face="bold")
      )
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggtitle3-1} 

}

\caption{Kustomisasi judul grafik dan keterangan axis}(\#fig:ggtitle3)
\end{figure}


### Merubah Tampilan dan Posisi Legend

Posisi legend dapat diubah dengan menambahkan argumen `legend.position` pada fungsi `theme()`. Posisi legend dapat diubah dengan memasukkan nilai berupa karakter seperti “left”,“top”, “right”, dan “bottom”. Selain itu, posisi legend dapat dispesifikasi menggunakan vektor numerik c(x,Y). Nilai x dan y berkisar antara 0 sampai 1. Nilai c(0,0) menandakan posisi legend pada bagian kiri bawah dan c(0,1) menyatakan kiri atas. 

Penggunaan karakter dan vektor numerik akan menghasilkan output posisi legend yang berbeda. Jika menggunakan karakter posisi legend akan diubah diluar bidang plot. Sedangkan vektor numerik akan mengubah posisi legend menjadi ada pada bidang plot. Untuk lebih memahaminya berikut disajikan dua buah gambar. Gambar \@ref(fig:gglegend) menyajikan pengaturan legend menggunakan karakter, sedangkan Gambar \@ref(fig:gglegend2) menyajikan pengaturan legend menggunakan vektor numerik.


```r
# cara 2
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna box berdasarkan benua
                      fill=continent))+
  # membuat box plot
  geom_boxplot()+
  # kustomisasi judul dan keterangan axis
  labs(title="GDP Per Capita Tiap Benua",
       x="Benua", y="GDP Per Kapita",
       # mengubah keterangan legend
       fill="Benua")+
  theme(legend.position="top")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglegend-1} 

}

\caption{Kustomisasi posisi legend berdasarkan karakter}(\#fig:gglegend)
\end{figure}


```r
# cara 2
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna box berdasarkan benua
                      fill=continent))+
  # membuat box plot
  geom_boxplot()+
  # kustomisasi judul dan keterangan axis
  labs(title="GDP Per Capita Tiap Benua",
       x="Benua", y="GDP Per Kapita",
       # mengubah keterangan legend
       fill="Benua")+
  theme(legend.position=c(0.9,0.75))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglegend2-1} 

}

\caption{Kustomisasi posisi legend berdasarkan vektor numerik}(\#fig:gglegend2)
\end{figure}

Pada fungsi `theme()` kita juga dapat merubah backgroud dari legend box menggunakan argumen `legend.bacground` dan `element_rect`. Selain itu kita juga dapat mengubah orientasi dari legend yang semula vertikal menjadi horizontal dengan menambahkan argumen `legend.box`. Berikut adalah contoh sintaks penerapannya. Output yang dihasilkan disajikan pada Gambar \@ref(fig:gglegend3).


```r
# cara 2
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna box berdasarkan benua
                      fill=continent,
                      # warna outline berdasarkan benua
                      color=continent))+
  # membuat box plot
  geom_boxplot()+
  # kustomisasi judul dan keterangan axis
  labs(title="GDP Per Capita Tiap Benua",
       x="Benua", y="GDP Per Kapita",
       # mengubah keterangan legend
       fill="Benua (fill)",
       color="Benua (outline)")+
  theme(legend.position="bottom",
        # mengubah tampilan legend box 
        legend.background = element_rect(fill="lightblue",
                                  size=0.5, linetype="solid", 
                                  colour ="darkblue"),
        # mengubah orientasi legend
        legend.box= "horizontal")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglegend3-1} 

}

\caption{Kustomisasi tampilan legend}(\#fig:gglegend3)
\end{figure}

Kita dapat juga menghilangkan legend baik seluruh legend maupun legend spesifik. Pada Gambar \@ref(fig:gglegend4) dan Gambar \@ref(fig:gglegend5) disajikan contoh cara menghilangkan seluruh legend maupun sebagian legend. 


```r
# Menghilangkan seluruh legend
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna box berdasarkan benua
                      fill=continent,
                      # warna outline berdasarkan benua
                      color=continent))+
  # membuat box plot
  geom_boxplot()+
  # kustomisasi judul dan keterangan axis
  labs(title="GDP Per Capita Tiap Benua",
       x="Benua", y="GDP Per Kapita",
       # mengubah keterangan legend
       fill="Benua")+
  theme(legend.position="none")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglegend4-1} 

}

\caption{Menghilangkan seluruh legend}(\#fig:gglegend4)
\end{figure}


```r
# Menghilangkan seluruh legend
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna box berdasarkan benua
                      fill=continent,
                      # warna outline berdasarkan benua
                      color=continent))+
  # membuat box plot
  geom_boxplot()+
  # kustomisasi judul dan keterangan axis
  labs(title="GDP Per Capita Tiap Benua",
       x="Benua", y="GDP Per Kapita",
       # mengubah keterangan legend
       fill="Benua (fill)",
       color="Benua (outline)")+
  theme(legend.position="bottom",
        # mengubah tampilan legend box 
        legend.background = element_rect(fill="lightblue",
                                  size=0.5, linetype="solid", 
                                  colour ="darkblue"))+
  # Menghilangkan legend Benua (outline)
  guides(color=FALSE)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglegend5-1} 

}

\caption{Menghilangkan sebagian legend legend}(\#fig:gglegend5)
\end{figure}

### Merubah Warana Pada Grafik Secara Otomatis dan Manual

Kita dapat merubah warna grafik baik secara otomatis dan manual. Secara otomatis warna dapat diubah dengan memasukkan nama variabel kedalam argumen `fill` dan `color`. Namun, jika kita inginkan kita dapat memasukkan kode warna untuk memperoleh warna yang seragam pada seluruh kelompok data.

Pada contoh sintaks berikut diberikan contoh bagaimana merubah warna pada seluruh grup data dengan satu warna yang seragam. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggcolor):


```r
ggplot(gapminder, aes(continent, lifeExp))+
  # spesifikasi warna tunggal
  geom_boxplot(color="darkred",fill="#A4A4A4")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggcolor-1} 

}

\caption{Merubah warna grup berdasarkan satu warna}(\#fig:ggcolor)
\end{figure}

Selain itu, kita dapat mengubah warna berdasarkan grup baik secara otomatis maupun manual. Berikut adalah contoh sintaks warna berdasarkan grup secara otomatis. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggcolor2).


```r
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna berdasarkan grup
                      fill=continent))+
  geom_boxplot()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggcolor2-1} 

}

\caption{Merubah warna grup secara otomatis}(\#fig:ggcolor2)
\end{figure}

Kita dapat mengatur pecahayaan (l) dan intensitas warna (c) dari warna yang kita tampilkan menggunakan fungsi `scale_fill_hue()`. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggcolor3).


```r
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna berdasarkan grup
                      fill=continent))+
  geom_boxplot()+
  # merubah l dan c
  scale_color_hue(l=40, c=35)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggcolor3-1} 

}

\caption{Merubah pencahayaan dan intensitas warna}(\#fig:ggcolor3)
\end{figure}

Jika kita tidak menginginkan warna yang secara otomatis ditampilkan oleh `ggplot2`, kita dapat mengubahnya secara manual menggunakan fungsi `scale_fill_manual()` (untuk box plot, bar plot, dll) dan `scale_color_manual()` (untuk line plot, dot plot dan scatterplot). Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggcolor4).


```r
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna berdasarkan grup
                      fill=continent))+
  geom_boxplot()+
  # merubah warna secara manual
  scale_fill_manual(values=c("#999999", "#E69F00", "#56B4E9",
                             "#B47846","#B4464B"))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggcolor4-1} 

}

\caption{Merubah warna secara manual}(\#fig:ggcolor4)
\end{figure}

JIka kita tidak hafal dengan kode hexadesimal warna tersebut kita dapat juga menggunakan palet warna. Contoh palet warna yang akan digunakan adalah dari library `RColorBrewer`. Berikut adalah contoh sintaks untuk menginstal dan memuat paket tersebut:


```r
# memasang paket
# install.packages("RColorBrewer")

# memuat paket
library(RColorBrewer)
```

Pada sintak berikut penulis akan menampilkan seluruh palet warna pada pekt tersebut. Output yang dihasilkan disajikan pada Gambar \@ref(fig:ggcolor5).


```r
display.brewer.all()
```

\begin{figure}

{\centering \includegraphics{EnvStat_files/figure-latex/ggcolor5-1} 

}

\caption{Palet warna RColorBrewer}(\#fig:ggcolor5)
\end{figure}

Pada Gambar \@ref(fig:ggcolor5) terdapat 3 jenis warna antara lain:

1. **Sequential palettes**, digunakan untuk menunjukkan urutan dari rendah ke tinggi atau gradien. Nama palet yang ada antara lain: Blues, BuGn, BuPu, GnBu, Greens, Greys, Oranges, OrRd, PuBu, PuBuGn, PuRd, Purples, RdPu, Reds, YlGn, YlGnBu YlOrBr,dan YlOrRd.
2. **Diverging palettes**, digunakan untuk menunjukkan perubahan pada data yang memiliki nilai positif dan negatif. Palet yang tersedia antara lain:  BrBG, PiYG, PRGn, PuOr, RdBu, RdGy, RdYlBu, RdYlGn, dan Spectral.
3. **Qualitative palettes**, digunakan untuk merepresentasikan variabel nominal atau kategori karena tidak menunjukkan besaran atau perbedaan nilai antar grup. Palete yang tersedia antara lain: Accent, Dark2, Paired, Pastel1, Pastel2, Set1, Set2, dan Set3.

Pada contoh sintaks berikut disajikan contoh penerapan dan output yang dihasilkan pada Gambar \@ref(fig:ggcolor6).


```r
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna berdasarkan grup
                      fill=continent))+
  geom_boxplot()+
  # merubah warna menggunakan palet
  scale_color_brewer(palette="Dark2")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggcolor6-1} 

}

\caption{Merubah warna menggunakan palet}(\#fig:ggcolor6)
\end{figure}

Jika kita tidak menginginkan warna-warna terang, kita dapat menggunakan fungsi `scale_color_grey()` (untuk line plot, dot plot, dan scatterplot) dan `scale_fill_grey()` (untuk bar plot, histogram, box plot, dll). Funsi tersebut akan memberikan warna palet gray pada plot. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggcolor7).


```r
ggplot(gapminder, aes(continent, gdpPercap, 
                      # warna berdasarkan grup
                      fill=continent))+
  geom_boxplot()+
  # merubah warna menggunakan palet
  scale_fill_grey()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggcolor7-1} 

}

\caption{Merubah warna menggunakan palet gray}(\#fig:ggcolor7)
\end{figure}

### Kustomisasi Titik 

Untuk mengubah jenis titik pada scatterplot, outlier pada box plot, dan dot plot, kita dapat menambahkan argumen `shape` pada fungsi geometrinya. Nilai yang mungkin dimasukkan berupa nilai diskrit yang berkisar antara 0 sampai 25. Selain itu, ukuran dari titik dapat diinput dengan menambahkan argumen `size`. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggpoint).


```r
ggplot(gapminder, aes(gdpPercap, lifeExp))+
  # spesifikasi jenis, ukuran dan warna titik
  geom_point(shape=4, size=2, color="blue")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggpoint-1} 

}

\caption{Kustomisasi jenis, ukuran dan warna titik}(\#fig:ggpoint)
\end{figure}

Untuk data dengan multiple group, kita dapat mengubah jenis, ukuran dan warna secara otomatis dengan memasukkan nama variabel kedalam argumen `shape`, `size` dan `color`. Sedangkan secara manual kita dapat menambahkan fungsi `scale_shape_manual()` (jenis titik), `scale_color_manual()` (warna titik), dan `scale_size_manual()` (ukuran titik). Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggpoint2) dan Gambar \@ref(fig:ggpoint3).


```r
# cara otomatis
ggplot(gapminder, aes(gdpPercap, lifeExp,
                      # spesifikasi jenis, ukuran dan warna
                      shape=continent, color=continent,
                      size=pop))+
  geom_point()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggpoint2-1} 

}

\caption{Kustomisasi jenis, ukuran dan warna titik untuk multiple group secara otomatis}(\#fig:ggpoint2)
\end{figure}


```r
# cara manual
ggplot(gapminder, aes(gdpPercap, lifeExp,
                      # spesifikasi jenis, ukuran dan warna
                      shape=continent, color=continent,
                      size=pop))+
  geom_point()+
  scale_shape_manual(values=c(1:5))+
  scale_color_manual(values=c("#999999", "#E69F00", "#56B4E9",
                             "#B47846","#B4464B"))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggpoint3-1} 

}

\caption{Kustomisasi jenis, ukuran dan warna titik untuk multiple group secara manual}(\#fig:ggpoint3)
\end{figure}

### Kustomisasi Jenis Garis

Jenis, warna dan ukuran garis dapat diatur dengan menambahkan argumen `linetype`, `size` dan `color`. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:gglty).


```r
gapminder%>%
  filter(continent=="Asia")%>%
  group_by(year)%>%
  summarize(mean_pop=mean(pop))%>%
  # plot
  ggplot(aes(year, mean_pop))+
    geom_line(linetype="dashed", color="blue",
              size=1)+
    geom_point(shape=1, color="red")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglty-1} 

}

\caption{Kustomisasi jenis, ukuran dan warna garis}(\#fig:gglty)
\end{figure}

Untuk data dengan multiple group, kita dapat mengubah jenis garis, warna dan ukuran secara manual maupun secara otomatis. Secara otomatis kita dapat menginputkan nama variabel kedalam argumen `linetype`, `size` dan `color`. Secara manual, kita dapat mengubah jenis, warna dan ukuran menggunakan fungsi `scale_linetype_manual()` (jenis garis), `scale_color_manual()` (warna garis), dan `scale_size_manual()` (ukuran garis). Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:gglty2) dan Gambar \@ref(fig:gglty3).


```r
# cara otomatis
gapminder%>%
  filter(continent %in% c("Asia","Africa"))%>%
  group_by(year, continent)%>%
  summarize(mean_pop=mean(pop))%>%
  # plot
  ggplot(aes(year, mean_pop,
             linetype=continent,
             color=continent))+
    geom_line()+
    geom_point(shape=1, color="red")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglty2-1} 

}

\caption{Kustomisasi jenis, ukuran dan warna garis untuk multiple group secara otomatis}(\#fig:gglty2)
\end{figure}


```r
# cara manual
gapminder%>%
  filter(continent %in% c("Asia","Africa"))%>%
  group_by(year, continent)%>%
  summarize(mean_pop=mean(pop))%>%
  # plot
  ggplot(aes(year, mean_pop,
             linetype=continent,
             color=continent))+
    geom_line()+
    geom_point(shape=1, color="red")+
    scale_linetype_manual(values=c("dotted", "twodash"))+
    scale_color_manual(values=c("red","blue"))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglty3-1} 

}

\caption{Kustomisasi jenis, ukuran dan warna garis untuk multiple group secara manual}(\#fig:gglty3)
\end{figure}

### Menambahkan Label Pada Titik Observasi dan Bidang Plot

Pada artikel ini penulis akan menjelaskan bagaimana kita dapat menambahkan teks pada plot. Fungsi-fungsi yang dapat digunakan antara lain:

- `geom_text()`: menambahkan teks secara langsung pada plot.
- `geom_label()`: menambahkan teks dengan kotak disekelilingnya.
- `annotate()`: menambahkan teks tertentu pada bagian tertentu bidang plot.
- `annotation_custom()`: menambahkan anotasi statik yang sama pada setiap panel.

Misal kita akan membuat plot antara variabel `pop` vs `gdpPercap` seperti yang ditunjukkan pada Gambar \@ref(fig:gglabel) berikut:


```r
ggplot(gapminder, aes(gdpPercap, pop))+
  geom_point()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglabel-1} 

}

\caption{Scatterplot variabel pop vs gdpPercap}(\#fig:gglabel)
\end{figure}

Misalkan kita ingin menandai negara yang memiliki gdpPercap > 50000. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:gglabel2).


```r
ggplot(gapminder, aes(gdpPercap, pop))+
  geom_point(shape=1)+
  geom_label(
    # subset data sesua kriteria
    data=subset(gapminder,gdpPercap>50000),
    # label berdasarkan kriteria
    aes(label=country),
    # ukuran teks
    size = 3)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglabel2-1} 

}

\caption{Scatterplot variabel pop vs gdpPercap dengan label}(\#fig:gglabel2)
\end{figure}

Selain teks yang menunjukkan observasi, kita dapat menambahkan anotasi pada grafik. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:gglabel3).


```r
ggplot(gapminder, aes(gdpPercap, pop))+
  geom_point(shape=1)+
  # menambahkan label sesuai kriteria data
  geom_label(
    # subset data sesua kriteria
    data=subset(gapminder,gdpPercap>50000),
    # label berdasarkan kriteria
    aes(label=country),
    # ukuran teks
    size = 3)+
  annotate(geom="text", x=90000,
          y=2e+08, label="outlier",
          color="red")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglabel3-1} 

}

\caption{Scatterplot variabel pop vs gdpPercap dengan label dan notasi}(\#fig:gglabel3)
\end{figure}

Kita dapat pula menambahkan teks statik yang sama pada setiap panel. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:gglabel4).


```r
library(grid)

# membuat teks
d <- grob <- grobTree(textGrob("Scatter plot", x=0.1,  y=0.95, hjust=0,
  gp=gpar(col="red", fontsize=13, fontface="italic")))

# plot
ggplot(gapminder, aes(gdpPercap, pop))+
  geom_point(shape=1)+
  # menambahkan anotasi
  annotation_custom(d)+
  # membagi plot menjadi beberapa panel
  facet_wrap(~continent, scales="free")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglabel4-1} 

}

\caption{Scatterplot variabel pop vs gdpPercap dengan label dan notasi pada tiap panel}(\#fig:gglabel4)
\end{figure}

### Kustomisasi Tema Pada Plot

Kita dapat melakukan kustomisasi tema plot untuk membuat tampilan plot kita lebih menarik. Pada bagian ini penulis akan membahas tema yang dapat digunakan serta cara untuk melakukan edit terhadap tema yang telah ada sebelumnya.

Tema-tema yang telah terpasang secara defautl pada paket `ggplot2` antara lain:

- **theme_gray**: backround dengan warna abu-abu dengan garis grid putih.
- **theme_bw**: background putih dan garis grid berwarna abu-abu.
- **theme_linedraw**: garis hitam di sekeliling bidang plot.
- **theme_light**: garis grid dan axis berwarna abu-abu terang.
- **theme_minimal**: tidak memiliki frame disekeliling bidang plot.
- **theme_classic**: tidak ada garis grid dan axis.
- **theme_void**: tema kosong
- **theme_dark**: background gelap.

Pada contoh berikut disajikan sebagian contoh penerapan tema pada plot. Output yang dihasilkan pada Gambar \@ref(fig:ggtema). 


```r
ggplot(gapminder, aes(gdpPercap, lifeExp))+
  geom_point()+
  theme_bw()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggtema-1} 

}

\caption{Scatterplot dengan tema black and white}(\#fig:ggtema)
\end{figure}

Kita juga dapat menggunakan tema kustom yang terdapat pada library `ggthemes`. Berikut adalah sintaks yang digunakan untuk menginstall dan memuat paket tersebut:


```r
# Memasang paket
install.packages("ggthemes")
```


```r
# memuat paket
library(ggthemes)
```

tema-tema yang tersedia pada paket tersebut antara lain:

- **theme_tufte**: tema minimalis.
- **theme_economist**: tema yang digunakan pada majalah Economist.
- **theme_stata**: tema yang digunakan pada visualisasi progra stata.
- **theme_wsj**: tema yang digunakan pada Wall Street Journal.
- **theme_cal**: tema yang digunakan pada LibreOffice Calc dan Google Docs.
- **theme_hc**: tema yang didasarkan pada Highcharts JS.

Pada contoh berikut disajikan sebagian contoh penerapan tema pada plot. Output yang dihasilkan pada Gambar \@ref(fig:ggtema2). 


```r
ggplot(gapminder, aes(gdpPercap, lifeExp, 
                      color=continent))+
  geom_point()+
  theme_wsj()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggtema2-1} 

}

\caption{Scatterplot dengan tema Wall Street Journal}(\#fig:ggtema2)
\end{figure}

Kita dapat juga membuat tema kustom berdasarkan tema yang telah ada. Untuk melakukannya kita hanya perlu merubah sejumlah argument default yang ada pada fungsi tema dan menamai tema sesuai dengan yang kita inginkan menggunakan *user define function*. Berikut adalah contoh argumen yang dapat diubah pada `theme_wsj`.


```r
theme_wsj
```

```
## function (base_size = 12, color = "brown", base_family = "sans", 
##     title_family = "mono") 
## {
##     colorhex <- ggthemes::ggthemes_data$wsj$bg[color]
##     theme_foundation(base_size = base_size, base_family = base_family) + 
##         theme(line = element_line(linetype = 1, colour = "black"), 
##             rect = element_rect(fill = colorhex, linetype = 0, 
##                 colour = NA), text = element_text(colour = "black"), 
##             title = element_text(family = title_family, size = rel(2)), 
##             axis.title = element_blank(), axis.text = element_text(face = "bold", 
##                 size = rel(1)), axis.text.x = element_text(colour = NULL), 
##             axis.text.y = element_text(colour = NULL), axis.ticks = element_line(colour = NULL), 
##             axis.ticks.y = element_blank(), axis.ticks.x = element_line(colour = NULL), 
##             axis.line = element_line(), axis.line.y = element_blank(), 
##             legend.background = element_rect(), legend.position = "top", 
##             legend.direction = "horizontal", legend.box = "vertical", 
##             panel.grid = element_line(colour = NULL, linetype = 3), 
##             panel.grid.major = element_line(colour = "black"), 
##             panel.grid.major.x = element_blank(), panel.grid.minor = element_blank(), 
##             plot.title = element_text(hjust = 0, face = "bold"), 
##             plot.margin = unit(c(1, 1, 1, 1), "lines"), strip.background = element_rect())
## }
## <bytecode: 0xfb852e8>
## <environment: namespace:ggthemes>
```

Berdasarkan output yang disajikan kita dapat merubah sejumlah argumen seperti base size, color, base_family, dll.

### Penskalaan dan Transformasi Axis

Pada bagian ini penulis akan menjelaskan bagaimana cara melakukan modifikasi terhadap sumbu x dan y seperti menetapkan limit nilai maksimum dan minimum axis serta melakukan transformasi pada tiap axis.

Untuk mengatur rentang nilai axis, kita dapat melakukannya dengan fungsi sebagai berikut:

- **xlim()** dan **ylim()**: mengatur limit aksis sumbu x dan y.
- **expand_limits()**: mengatur limit sumbu x dan y sekaligus dapat mengatur intercept kedua sumbu tersebut.
- **scale_x_continous()** dan **scale_y_continous()**: megatur limit axis termasuk axis tick dan label.

Pada contoh berikut akan disajikan cara mengatur limit axis dengan menggunakan `xlim()` dan `ylim()` serta menggunakan `expand_limits()`. Output yang dihasilkan disajikan pada Gambar \@ref(fig:gglimits).


```r
gapminder%>%
  filter(continent=="Europe")%>%
  ggplot(aes(gdpPercap, lifeExp))+
  geom_point()+
  theme_wsj(base_size=7)+
  labs(title="GDP per Capita vs Life Expectancy",
       y="Life Expectancy",
       x="GDP per Capita (US Dollar)")+
  # mengatur limit axis
  expand_limits(x=c(0, 55000), y=c(0, 90))
```


```r
# atau
gapminder%>%
  filter(continent=="Europe")%>%
  ggplot(aes(gdpPercap, lifeExp))+
  geom_point()+
  theme_wsj(base_size=7)+
  labs(title="GDP per Capita vs Life Expectancy",
       y="Life Expectancy",
       x="GDP per Capita (US Dollar)")+
  # mengatur limit axis
  xlim(0,55000)+
  ylim(0,90)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglimits-1} 

}

\caption{Scatterplot dengan axis limits }(\#fig:gglimits)
\end{figure}

Kita juga dapat menggunakan fungsi `scale_x_continuous()` dan `scale_y_continuous()` untuk mengatur limit axis ,*axis tick* dan label. Format yang digunakan adalah sebagai berikut:


```r
scale_x_continuous(name, breaks, labels, limits, trans)
scale_y_continuous(name, breaks, labels, limits, trans)
```

> **Note: **
>
> - **name**: label axis sumbu x dan y.
> - **breaks**: untuk mengontrol jeda dalam panduan (*axis tick*, garis grid, ...). Di antara nilai-nilai yang mungkin, adalah sebagai berikut:
>
>   + NULL: menyembunyikan seluruh breaks.
>   + **waiver()**: komputasi break default.
>   + vektor numerik atau karakter untuk menspesifikasikan break yang akan ditampilkan.
>
> - **labels**: label axis. Nilai yang dapat dimasukkan antara lain;
>   + NULL: tanpa label.
>   + **waiver()**: label default.
>   + vektor karakter yang digunakan untuk spesifikasi label break.
>
> - **limits**: vektor numerik untuk spesifikasi limit sumbu x dan y.
> - **trans**: transformasi axis. Nilai yang dapat digunakan adalah "log2", "log10", dll.

Pada contoh berikut disajikan contoh mengatur limit axis dan label axis menggunakan fungsi `scale_x_continous()` dan `scale_y_continous()`. Grafik yang dihasilkan akan tampak seperti Gambar \@ref(fig:gglimits2).


```r
# atau
gapminder%>%
  filter(continent=="Asia")%>%
  ggplot(aes(gdpPercap, lifeExp))+
  geom_point()+
  theme_wsj(base_size=7)+
  ggtitle("GDP per Capita vs Life Expectancy")+
  # spesifikasi limit dan label axis
  scale_x_continuous(name="GDP per Capita", 
                     limits=c(0, 125000))+
  scale_y_continuous(name="Life Expectancy",
                     limits=c(0,100))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglimits2-1} 

}

\caption{Scatterplot dengan axis limits (2) }(\#fig:gglimits2)
\end{figure}

Tranformasi axis dapat dilakukan dengan fungsi bawaan dari `ggplot2`. Fungsi transformasi bawaan berupa transformasi log dan sqrt. Berikut adalah fungsi bawaan untuk transformasi tersebut:

- **scale_x_log10()** dan **scale_y_log10()**: transformasi log basis 10.
- **scale_x_sqrt()** dan **scale_y_sqrt()**: transformasi akar kuadrat.
- **scale_x_reverse()** dan **scale_x_reverse()**: membalikkan koordinat.
- **coord_trans(x="log10", y="log10")**: memungkinkan transformasi untuk kedua axis sesuai fungsi yang diinputkan pada sumbu x dan sumbu y seperti “log2”, “log10”, “sqrt”, dll.
- **scale_x_continuous(trans="log2")** dan **scale_y_continuous(trans="log2")**: nilai lain yang dapat diinputkan adalah "log10".

Pada contoh berikut disajikan contoh transformasi sumbu x menggunakan fungsi `scale_x_log10()`. Grafik yang dihasilkan akan tampak seperti Gambar \@ref(fig:gglimits3).


```r
# atau
gapminder%>%
  filter(continent=="Europe")%>%
  ggplot(aes(gdpPercap, lifeExp))+
  geom_point()+
  theme_wsj(base_size=7)+
  labs(title="log(GDP per Capita) vs Life Expectancy",
       y="Life Expectancy",
       x="GDP per Capita (US Dollar)")+
  # transformasi sumbu x
  scale_x_log10()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglimits3-1} 

}

\caption{Scatterplot dengan transformasi axis }(\#fig:gglimits3)
\end{figure}

*Tick mark* pada axis juga dapat kita atur menggunakan fungsi `scale_x_continous()` dan `scale_y_continous()`. Untuk mengubah format dan label *tick mark* kita perlu menginstall dan memuat library `scales` yang berfungsi untuk mengakses fungsi pada argumen break. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:gglimits4).


```r
# memasang paket
# install.packages("scales")

# memuat paket
library(scales)

# plot
ggplot(gapminder, aes(gdpPercap, lifeExp))+
  geom_point()+
  theme_bw()+
  # kustomisasi tick mark sumbu y
  scale_y_continuous(trans= log2_trans(),
                     breaks=trans_breaks("log2", function(x) 2^x),
                     labels= trans_format("log2", math_format(2^.x)))+
  # kustomisasi sumbu x
  scale_x_continuous(labels = dollar)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gglimits4-1} 

}

\caption{Scatterplot dengan transformasi tick mark axis }(\#fig:gglimits4)
\end{figure}

### Kustomisasi Tick Mark Axis

Pada bagian ini pembaca akan mempelajari bagaimana melakukan kustomisasi tampilan *tick mark*. Selain itu kita juga akan belajar bagaimana melakukan pengaturan pada garis axis.

Warna, ukuran font, dan tampilan font (*font style*) pada *tick mark* dapat diubah menggunakan fungsi `theme()` dan `element_text()`. Format yang digunakan adalah sebagai berikut:


```r
# x axis tick mark labels
<plot> + theme(axis.text.x= element_text(family, face, colour, size, angle))
# y axis tick mark labels
<plot> + theme(axis.text.y = element_text(family, face, colour, size, angle))
```

> **Note: **
>
> - **family**: *font family*, seperti: "sans","times new roman", dll.
> - **face**: *font face*, nilai yang mungkin adalah “plain”, “italic”, “bold” dan “bold.italic”.
> - **color**: warna teks.
> - **size**: ukuran teks dalam satuan pts.
> - **angle**: sudut kemiringan teks berkisar antara 0 sampai 360.

Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggtick).


```r
ggplot(gapminder, aes(continent, gdpPercap,
                      fill=continent))+
  geom_boxplot()+
  theme_economist()+
  scale_fill_economist()+
  # kustomisasi tick mark
  theme(axis.text.x = element_text(face="bold", 
                                   color="#993333",
                                   size=10, 
                                   angle=30),
          axis.text.y = element_text(face="bold", 
                                     color="#993333",
                                     size=10, 
                                     angle=30))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggtick-1} 

}

\caption{Mengubah tampilan dari tick mark}(\#fig:ggtick)
\end{figure}

Untuk menonaktifkan *tick mark* pada plot kita dapat menggunakan fungsi `element_blank()`. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggtick2).


```r
ggplot(gapminder, aes(continent, gdpPercap,
                      fill=continent))+
  geom_boxplot()+
  theme_stata()+
  scale_fill_stata()+
  # menyembunyikan tick mark dan tick mark label
  theme(axis.text.x=element_blank(),
  axis.text.y=element_blank(),
  axis.ticks=element_blank())
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggtick2-1} 

}

\caption{Menyembunyikan tampilan dari tick mark}(\#fig:ggtick2)
\end{figure}
 
Kita dapat melakukan pengaturan terhadap garis axis menggunakan argumen `axis.lines` dan fungsi `element_line`. Berikut adalah format yang digunakan:


```r
<plot> + theme(axis.line = element_line(color,size, linetype,
                                        lineend, color))
```

> **Note: **
>
> - **color**: warna garis.
> - **size**: ukuran garis.
> - **linetype**: jenis garis.
> - **lineend**: akhir dari garis. Nilai yang dapat dimasukkan antara lain: “round”, “butt” atau “square”.

Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggtick3).


```r
ggplot(gapminder, aes(continent, gdpPercap,
                      fill=continent))+
  geom_boxplot()+
  theme_wsj()+
  scale_fill_wsj()+
  # kustomisasi garis axis
  theme(axis.line = element_line(colour = "darkblue", 
                      size = 1, linetype = "solid"))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggtick3-1} 

}

\caption{Kustomisasi tampilan dari garis axis}(\#fig:ggtick3)
\end{figure}

Kita dapat mengatur *tick* pada axis baik yang memiliki skala diskrit maupun kontinyu. Fungsi yang digunakan adalah `scale_x_continous()` dan `scale_y_continous()` untuk *tick* dengan nilai kontinyu dan `scale_x_discrete()` dan `scale_y_discrete()`.

Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggtick4).


```r
ggplot(gapminder, aes(continent, lifeExp,
                      fill=continent))+
  geom_boxplot()+
  theme_gdocs()+
  scale_fill_gdocs()+
  # kustomisasi tick mark
  scale_y_continuous(
    # nilai dari 0 sampai 100 tiap 10 tick
    breaks=seq(0,100,10))
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggtick4-1} 

}

\caption{Kustomisasi tick mark}(\#fig:ggtick4)
\end{figure}

### Menambahkan Garis Lurus Pada Plot

Fungsi yang dapat digunakan untuk menambahkan garis lurus antara lain:

- **geom_hline()**: menambahkan garis horizontal.
- **geom_abline()**: menambahkan garis regresi.
- **geom_vline()**: menambahkan garis vertikal.
- **geom_segment()**: menambahkan garis segmen.

Format yang digunakan untuk fungsi `geom_hline()` dan `geom_vline()` adalah sebagai berikut:


```r
geom_hline(yintercept, linetype, color, size)
geom_vline(xintercept, linetype, color, size)
```

Berikut adalah contoh penerapan kedua fungsi tersebut yang disajikan pada Gambar \@ref(fig:ggvline) dan Gambar \@ref(fig:gghline):


```r
ggplot(gapminder, aes(lifeExp, fill=..count..))+
  geom_histogram()+
  theme_calc()+
  # menambahkan garis vertikal
  geom_vline(xintercept=mean(gapminder$lifeExp), 
             linetype="twodash",
             color="red",
             size=1.5)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggvline-1} 

}

\caption{Penerapan vline}(\#fig:ggvline)
\end{figure}


```r
ggplot(gapminder, aes(continent, lifeExp, 
                      fill=continent))+
  geom_boxplot()+
  theme_calc()+
  scale_fill_calc()+
  # menambahkan garis horizontal
  geom_hline(yintercept=mean(gapminder$lifeExp), 
             linetype="twodash",
             color="red",
             size=1.5)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gghline-1} 

}

\caption{Penerapan hline}(\#fig:gghline)
\end{figure}

Selain menggunakan fungsi `geom_smooth()`, garis regresi dapat ditambahkan melalui fungsi `geom_abline(). Format yang digunakan adalah sebagai berikut:


```r
geom_abline(intercept, slope, linetype, color, size)
```

Untuk membuat garis regresi kita perlu membuat model regresi terlebih dahulu menggunakn fungsi `lm()`. Berikut adalah contoh model yang dibuat beserta koefisien regresinya.


```r
# membuat model regresi
mod <- lm(lifeExp~gdpPercap, data=gapminder)

# print model
mod
```

```
## 
## Call:
## lm(formula = lifeExp ~ gdpPercap, data = gapminder)
## 
## Coefficients:
## (Intercept)    gdpPercap  
##    5.40e+01     7.65e-04
```

```r
# koefisien regresi model
coef <- coefficients(mod)

# print koefisien
coef
```

```
## (Intercept)   gdpPercap 
##   5.396e+01   7.649e-04
```

Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggabline) untuk membuat plot regresi linier.


```r
ggplot(gapminder, aes(gdpPercap, lifeExp))+
  geom_point(shape=1, color="grey")+
  theme_stata()+
  # menambahkan garis regresi
  geom_abline(intercept=5.395556e+01,
         slope=7.648826e-04,
         linetype="twodash",
             color="red",
             size=1)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggabline-1} 

}

\caption{Penerapan abline}(\#fig:ggabline)
\end{figure}

Kita dapat menambahkan garis segment untuk menunjukkan sebuah observasi. Format yang digunakan adalah sebagai berikut:


```r
geom_segment(aes(x, y, xend, yend))
```

Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggsegment) untuk membuat garis segmen.


```r
library(grid)
ggplot(gapminder, aes(gdpPercap, lifeExp))+
  geom_point(shape=1, color="grey")+
  theme_stata()+
  # menambahkan tanda panah
  geom_segment(x=70000, y=80,
                   xend=60000, yend=70,
                   arrow=arrow(length=unit(0.1, "inches")),
               linetype="twodash",
               color="red",
               size=1)
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggsegment-1} 

}

\caption{Penerapan garis segmen}(\#fig:ggsegment)
\end{figure}

### Melakukan Rotasi Pada Grafik

Rotasi grafik atau pembalikan axis dapat dilakukan menggunakan fungsi berikut:

- **coord_flip()**: untuk membuat plot horizontal.Rotasi axis sehingga sumbu x dapat menjadi sumbu y dan sebaliknya.
- **scale_x_reverse()** dan **scale_x_reverse()**: pembalikan skala pada axis.

Misalkan kita ingin membuat plot horizontal pada box plot sehingga mempermudah kita dalam melakukan perbandingan terhadap masing-masing grup. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggcoord).


```r
ggplot(gapminder, aes(continent, lifeExp, 
                      fill=continent))+
  geom_boxplot()+
  theme_economist()+
  scale_fill_economist()+
  # rotasi axis
  coord_flip()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggcoord-1} 

}

\caption{Rotasi axis}(\#fig:ggcoord)
\end{figure}

Kita dapat juga melakukan pembalikan skala pada axis sehingga skala yang semula berawal dari min ke max menjadi sebaliknya. Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggyreverse).


```r
ggplot(gapminder, aes(lifeExp, fill=..count..))+
  geom_histogram()+
  theme_wsj()+
  # pembalikan sumbu y
  scale_y_reverse()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/ggyreverse-1} 

}

\caption{Pembalikan sumbu y}(\#fig:ggyreverse)
\end{figure}

### Facet

Facet digunakan untuk membagi plot menjadi panel matriks. Setiap panel menunjukkan setiap kelompok data. Fungsi facet yang dapat digunakan antara lain:

- **facet_grid()**
- **facet_wrap()**

Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggfacetgrid) dan Gambar \@ref(fig:ggfacetgrid2) untuk membuat facet pada satu variabel.


```r
ggplot(gapminder, aes(lifeExp, fill=..count..))+
  geom_histogram()+
  theme_gdocs()+
  facet_grid(.~continent)
```

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{EnvStat_files/figure-latex/ggfacetgrid-1} 

}

\caption{Facet horizontal satu variabel}(\#fig:ggfacetgrid)
\end{figure}


```r
ggplot(gapminder, aes(lifeExp, fill=..count..))+
  geom_histogram()+
  theme_gdocs()+
  facet_grid(continent~.)
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/ggfacetgrid2-1} 

}

\caption{Facet vertikal satu variabel}(\#fig:ggfacetgrid2)
\end{figure}

Kita dapat pula melakukan facet terhadap dua buah variabel.Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggfacetgrid3) untuk membuat facet pada dua variabel.


```r
gapminder%>%
  filter(year==1952|year==2007,
         continent %in% c("Asia","Americas"))%>%
  ggplot(aes(continent, lifeExp, 
             fill=factor(year)))+
  geom_boxplot()+
  theme_stata()+
  scale_fill_stata()+
  facet_grid(continent~factor(year))
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/ggfacetgrid3-1} 

}

\caption{Facet dua variabel}(\#fig:ggfacetgrid3)
\end{figure}

Kita dapat mengatur skala dari axis menggunakan argument sebagai berikut:

- **free**: skala akan disesuaikan berdasarkan pada setiap axis.
- **free_x**: skala pada sumbu x akan dibiarkan menyesuaikan secara bebas.
- **free_y**: skala pada sumbu y akan dibiarkan menyesuaikan secara bebas.
- **fixed** (default): skala axis diseragamkan pada seluruh panel.

Berikut adalah sintaks yang digunakan beserta output yang dihasilkan pada Gambar \@ref(fig:ggfacetgrid4) untuk membuat facet pada dua variabel dengan skala bebas pada sumbu y.


```r
gapminder%>%
  filter(year==1952|year==2007,
         continent %in% c("Asia","Americas"))%>%
  ggplot(aes(continent, lifeExp, 
             fill=factor(year)))+
  geom_boxplot()+
  theme_stata()+
  scale_fill_stata()+
  facet_grid(continent~factor(year), scales="free_y")
```

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{EnvStat_files/figure-latex/ggfacetgrid4-1} 

}

\caption{Facet dua variabel dengan skala bebas pada sumbu y}(\#fig:ggfacetgrid4)
\end{figure}

## Referensi

1. Wickham, H. Grolemund G. 2016. **R For Data Science: Import, Tidy, Transform, Visualize, And Model Data**. O'Reilly Media, Inc.
2. Peng, R.D. 2015. **Exploratory Data Analysis with R**. Leanpub book.
3. GGPLOT2 Documentation. <https://ggplot2.tidyverse.org/>
4. STHDA. ggplot2 - Essentials. <https://www.sthda.com/english/wiki/ggplot2-essentials>


<!--chapter:end:05-visualisasi-data-menggunakan-ggplot.Rmd-->

# (PART\*) Statistika Deskriptif - R {-}

<style>
body{
text-align: justify}
</style>

# Ringkasan Numerik

Pada bidang lingkungan kita sering kali menemui sebuah pernyataan "konsentrasi rata-rata TSS pada sungai tersebut adalah 30 mg/l" atau "kedalaman penampang saluran tersebut berkisar antara 1 sampai 2 meter". Kedua pernyataan tersebut merupakan sebuah penyapaian informasi terkait karakteristik data yang ada. Pernyataan yang pertama menyatakan karakteristik nilai pemusatan data, sedangkan yang kedua menyatakan karakteristik sebaran suatu data.

Karakteristik lain yang sering digunakan untuk menjelaskan suatu data adalah bentuk distibusi suatu data dan estimasi nilai ekstrim seperti nilai masimum dan minimum suatu data. Seluruh karakteristik data tersebut perlu dihitung untuk memperoleh informasi numerik pada data.

Pada chapter ini kita akan membahas terkait metode untuk membuat ringkasan dan deksripsi data. Pembahasan akan terdiri dari ukuran nilai pemusatan data, ukuran sebaran atau variabilitas data dan bentuk distribusi data. Selain itu kita akan membahas nilai ekstrim yang ada pada sebuah data dan transformasi data.

## Ukuran Pemusatan Data

Nilai rata-rata (mean) dan nilai tengah (median) merupakan dua nilai yang paling umum digunakan untuk menyatakan lokasi pemusatan data meskipun kedua nilai bukanlah satu atau dua ukuran yang tersedia. Apa sajakah properti dari kedua ukuran tersebut dan kapan salah satu atau keduanya dapat digunakan bersamaan?.

### Pengukuran Klasik-Mean

Nilai mean ($\overline{X}$) diperoleh dengan menjumlahkan seluruh data dan membaginya dengan jumlah observasinya yang dapat dituliskan seperti Persamaan \@ref(eq:mean):

\begin{equation}
  \overline{X}=\text{}\sum_{_{i=1}}^n\frac{X_i}{n}
  (\#eq:mean)
\end{equation}

Nilai mean yang disimbolkan dengan "X bar" merupakan nilai mean untuk sampel. Nilai mean untuk populasi disimbolkan oleh huruf Yunani "mu atau $\mu$".

Pada Persamaan \@ref(eq:mean), jika data terdiri dari banyak grup maka nilai rata-rata dihitung berdasarkan jumlah nilai observasi dikali dengan bobotnya. Nilai mean tersebut disebut sebagai *weighted mean* yang dapat ditulis berdasarkan Persamaan Persamaan \@ref(eq:weightedmean).

\begin{equation}
  \overline{X}\ =\text{}\sum_{_{i=1}}^n\overline{X_i}\cdot\frac{n_i}{n}
  (\#eq:weightedmean)
\end{equation}

dimana $\overline{X_i}$ merupakan nilai rata-rata grup ke-i dan $\frac{n_i}{n}$ merupakan bobot pengali yang berupa rasio antara observasi grup ke-i dengan keseluruhan observasi. 

Kita biasanya akan berhadapan dengan nilai observasi yang baru sehingga nilai mean yang telah ada akan ikut berubah. Perubahan nilai mean tersebut disebabkan karena setiap observasi yang disertakan dalam perhitungan mean memiliki pengaruhnya masing-masing. Jika observasi tersebut cenderung ekstrim besar maka nilai mean akan bergeser menuju kearahnya begitu juga sebaliknya.

Pengaruh dari sebuah nilai observasi ke-j atau $X_j$ dapat dilihat dengan menghitung seluruh observasi secara bersamaan kecuali observasi ke-j pada sebuah grup. Dapat dituliskan pada Persamaan \@ref(eq:influencemean2)

\begin{equation}
  \overline{X} =\text{}\overline{X_{\left(j\right)}}\ \cdot\frac{\left(n-1\right)}{n}+X_j\cdot\frac{1}{n}
  (\#eq:influencemean1)
\end{equation}

\begin{equation}
  \overline{X} =\overline{X}_{\left(j\right)}+\left(X_j-\overline{X}_{\left(j\right)}\right)\cdot\frac{1}{n}
  (\#eq:influencemean2)
\end{equation}

dimana $\overline{X}_{\left(j\right)}$ adalah nilai mean seluruh observasi kecuali $X_j$. Setiap observasi yang mempengaruhi nilai mean keseluruhan ($\overline{X}$) didefinisikan oleh $\left(X_j-\overline{X}_{\left(j\right)}\right)$ sebagai jarak antara observasi tersebut dengan nilai rata-rata yang tidak termasuk observasi tersebut di dalamnya. Sehingga seluruh nilai observasi tidak memiliki pengaruh yang sama terhadap nilai rata-rata seluruh observasi.

*Outlier* merupakan observasi yang memiliki nilai yang ekstrim tinggi atau rendah dibanding seluruh observasi yang ada sehingga memiliki pengaruh yang besar terhadap nilai mean keseluruhan ($\overline{X}$). Pengaruhnya yang sangat besar terhadap nilai rata-rata keseluruhan akan menyebabkan nilai rata-rata akan bergeser ke arah *outlier* tersebut. Selain itu penampilan dari distribusi frekuensi yang terbentuk akan terlihat memiliki ekor yang panjang.

Untuk lebih memahami pengaruh observasi terhadap nilai rata-rata, disajikan dua buah gambar yaitu: Gambar \@ref(fig:mean1) dan Gambar \@ref(fig:mean2)

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{mean1} 

}

\caption{Nilai mean (segitiga) sebagai titik kesetimbangan pada data.}(\#fig:mean1)
\end{figure}

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{mean2} 

}

\caption{Pergeseran nilai mean (segitiga) ke kiri setelah penghilangan outlier.}(\#fig:mean2)
\end{figure}

Pada Gambar \@ref(fig:mean1) disajikan 7 buah data konsentrasi TSS di suatu sungai. Nilai rata-rata TSS pada sungai tersebut adalah 11 mg/l. Jika kita amati sebagian besar data (6 observasi) berada pada interval nilai konsentrasi TSS 2 sampai 12 mg/l. Observasi yang lain terletak jauh dari mayoritas observasi lainnya yaitu sebesar 37 mg/l. Observasi yang berbeda secara ekstrim dari nilai secara umum pada suatu data disebut sebagai *outlier*. Nilai *outlier* tersebut menyebabkan nilai rata-rata yang terbentuk tidak representatif terhadap keseluruhan data yang ada dan cenderung menggeser nilai rata-rata mendekati nilai *outlier* tersebut. Nilai observasi yang ekstrim biasanya muncul dari adanya kesalahan perlakuan terhadap sampel seperti botol sampel yang digunakan tidak bersih atau prosedur analisa yang dilakukan tidak standar sehingga memungkinkan adanya partikulat udara yang terukur pada proses penimbangan.

Salah satu cara untuk menangani adanya *outlier* tersebut adalah dengan menghapus observasi yang merupakan *outlier*. Pada Gambar \@ref(fig:mean2) terlihat bahwa penghapusan *outlier* telah menggeser nilai rata-rata ke kiri. Nilai rata-rata yang baru tersebut jika diperhatikan dari Gambar \@ref(fig:mean2) lebih menggambarkan keseluruhan data yang ada. Tidak terlihat adanya nilai yang berada jauh jaraknya dari nilai rata-rata yang baru.

Pada contoh tersebut dapat kita simpulkan bahwa nilai mean sangat sensitif terhadap adanya *outlier*. Pada prakteknya nilai mean tidaklah berdiri sendiri selama proses analisa. Nilai mean memerlukan nilai lain seperti median untuk menganalisa apakah data yang diperoleh tidak simetris yang dapat mengindikasikan adanya outlier.

Pada `R` untuk menghitung nilai rata-rata, kita dapat menggunakan fungsi `mean()`. Format fungsi yang digunakan dituliskan pada persamaan berikut:


```r
mean(x, trim = 0, na.rm = FALSE)
```

> **Note:**
>
> - **x**: objek atau vektor numerik.
> - **trim**: menyatakan fraksi data (berkisar antara 0 sampai 0,5) yang perlu dilakukan pemotongan (*trim*) pada observasi awal dan akhir **x** (yang telah diurutkan) sebelum nilai mean dihitung.
> **na.rm**: nilai logis yang menyatakan apakah *missing value* perlu disertakan dalam perhitungan atau tidak. Jika disertakan maka output yang akan dihasilkan adalah NA.

---------------------------------

**Contoh**

- **Analisa Nilai Mean Grup Data Tunggal (Single Group)**

Untuk lebih memahami penerapannya pada `R`, pada Tabel \@ref(tab:debitsungai) berikut disajikan data terkait debit air suatu sungai.

\begin{table}[t]

\caption{(\#tab:debitsungai)Data Debit Sampel (m3/detik)}
\centering
\begin{tabular}{r|r}
\hline
observasi & debit\\
\hline
1 & 457\\
\hline
2 & 185\\
\hline
3 & 133\\
\hline
4 & 160\\
\hline
5 & 119\\
\hline
6 & 115\\
\hline
7 & 101\\
\hline
8 & 58\\
\hline
9 & 68\\
\hline
10 & 50\\
\hline
11 & 65\\
\hline
12 & 128\\
\hline
\end{tabular}
\end{table}

Data pada Tabel \@ref(tab:debitsungai) dapat divisualisasikan seperti pada Gambar \@ref(fig:debitvis):

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/debitvis-1} 

}

\caption{Visualisasi debit sungai pada sampel}(\#fig:debitvis)
\end{figure}

Berdasarkan Gambar \@ref(fig:debitvis), terdapat *outlier* yang ditunjukkan pada debit sungai yang lebih besar dari 400 m3/detik. Hasil tersebut dapat terjadi salah satunya karena adanya kondisi ekstrim seperti banjir yang menyebabkan sungai meluap atau terjadi kesalahan pengukuran dari alat ukur yang ada di lapangan.

Untuk menghitung nilai rata-rata debit pada data tersebut, masukkan variabel `debit` yang telah penulis simpan sebagai objek `sungai` kedalam fungsi `mean()` seperti berikut:


```r
mean(sungai$debit)
```

```
## [1] 136.6
```

Berdasarkan hasil yang diperoleh, dapat dilihat bahwa nilai rata-rata debit pada sungai tersebut adalah 136.5833 $m^3/detik$. 

Kita dapat menghitung nilai mean dengan terlebih dahulu menghilangkan *outlier* pada data. Untuk melakukannya kita perlu melakukan subset terhadap data tanpa *outlier* di dalamnya sebelum data tersebut dimasukkan kedalam fungsi mean(). Berikut sintaks yang digunakan untuk melakukan hal tersebut:


```r
# memuat paket
library(tidyverse)

# melakukan filter terhadap data
sungai_subset<-sungai%>%
  filter(debit<=400)

# menghitung mean
mean(sungai_subset$debit)
```

```
## [1] 107.5
```

Berdasarkan hasil yang diperoleh terlihat bahwa nilai rata-rata yang baru lebih kecil dari yang sebelumnya (bergeser ke kiri) dengan nilai mean debit sungai yang baru sebesar 107.4545 $m^3/detik$. Hal ini terjadi karena pengaruh dari data *outlier* yang telah dihilangkan.


- **Analisa Nilai Rata-Rata Berdarsarkan Grup Data**

Pada contoh sebelumnya kita telah melakukan perhitungan nilai mean untuk studi kasus grup tunggal. Pada contoh ini akan disajikan contoh kasus perhitungan nilai mean untuk data berkelompok.

Dataset pada contoh kasus ini diambil dari buku **Statistical Methods in Water Resources**. Data yang digunakan adalah data konsentrasi TDS dan Uranium di airtanah dengan perbedaan konsentrasi bikarbonate dalam air tanah yaitu $\leq 50$% (0) dan $>50$% (1). Dataset yang digunakan disajikan pada Tabel \@ref(tab:gwtdsur).

> **Note: ** data yang digunakan dapat diunduh pada link berikut [google.drive](https://drive.google.com/open?id=1-k_1Fkl2hWmI9ZohG9hWGrqKe4o8GArW). Simpan dataset tersebut pada *working directory* pembaca agar mudah dalam proses membaca data.



```r
# memuat library
library(readxl)

# memuat data excel
data_gw <- read_excel("hhappc.xls", sheet="appc16")

# membuang kolom ke-4
data_gw<-data_gw %>%
  select(TDS, Uranium, Bicarbonate) %>%
  mutate(Bicarbonate=as.factor(Bicarbonate))
```


\begin{table}[t]

\caption{(\#tab:gwtdsur)Kosentrasi TDS dan Uranium dalam berbagai kondisi kesadahan}
\centering
\begin{tabular}{r|r|l}
\hline
TDS & Uranium & Bicarbonate\\
\hline
682.6 & 0.9315 & 0\\
\hline
819.1 & 1.9380 & 0\\
\hline
303.8 & 0.2919 & 0\\
\hline
1151.4 & 11.9042 & 0\\
\hline
582.4 & 1.5674 & 0\\
\hline
1043.4 & 2.0623 & 0\\
\hline
634.8 & 3.8858 & 0\\
\hline
1087.2 & 0.9772 & 0\\
\hline
1123.5 & 1.9354 & 0\\
\hline
688.1 & 0.4367 & 0\\
\hline
1174.5 & 10.1142 & 0\\
\hline
599.5 & 0.7551 & 0\\
\hline
1240.8 & 6.8559 & 0\\
\hline
538.4 & 0.4806 & 0\\
\hline
607.8 & 1.1452 & 0\\
\hline
705.9 & 6.0876 & 0\\
\hline
1290.6 & 10.8823 & 0\\
\hline
526.1 & 0.1473 & 0\\
\hline
784.7 & 2.6741 & 0\\
\hline
953.1 & 3.0918 & 0\\
\hline
1149.3 & 0.7592 & 0\\
\hline
1074.2 & 3.7101 & 0\\
\hline
1116.6 & 7.2446 & 0\\
\hline
301.2 & 5.7129 & 1\\
\hline
265.4 & 4.7366 & 1\\
\hline
295.9 & 2.8057 & 1\\
\hline
442.4 & 5.6290 & 1\\
\hline
342.7 & 3.0950 & 1\\
\hline
361.3 & 3.5774 & 1\\
\hline
262.1 & 1.7711 & 1\\
\hline
546.2 & 11.2724 & 1\\
\hline
273.9 & 4.9807 & 1\\
\hline
281.4 & 4.0833 & 1\\
\hline
588.9 & 14.6342 & 1\\
\hline
574.1 & 12.3835 & 1\\
\hline
307.1 & 1.5291 & 1\\
\hline
409.4 & 4.4647 & 1\\
\hline
327.1 & 2.4574 & 1\\
\hline
425.7 & 6.3042 & 1\\
\hline
310.1 & 4.5441 & 1\\
\hline
289.8 & 0.9672 & 1\\
\hline
408.2 & 2.1568 & 1\\
\hline
383.0 & 8.3810 & 1\\
\hline
255.2 & 2.7957 & 1\\
\hline
\end{tabular}
\end{table}

Visualisasi data Tabel \@ref(tab:gwtdsur), disajikan pada  Gambar \@ref(fig:gwvis1) dan Gambar \@ref(fig:gwvis2):

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gwvis1-1} 

}

\caption{Visualisasi konsentrasi TDS pada air tanah}(\#fig:gwvis1)
\end{figure}

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gwvis2-1} 

}

\caption{Visualisasi konsentrasi Uranium pada air tanah}(\#fig:gwvis2)
\end{figure}

Pada dataset tersebut kita ingin melihat apakah terdapat perbedaan antara konsentrasi TDS dan uranium pada kondisi kesadahan bikarbonat $\leq 50$% dan $> 50$%. Untuk melakukannya pada `R` kita perlu mengelompokkan data tersebut terlebih dahulu berdasarkan variabel bikarbonat. Setelah itu nilai rata-rata dapat dihitung. Berikut sintaks yang digunakan:


```r
data_gw %>%
  group_by(Bicarbonate) %>%
  summarize(TDS = mean(TDS), Uranium = mean(Uranium))
```

```
## # A tibble: 2 x 3
##   Bicarbonate   TDS Uranium
##   <fct>       <dbl>   <dbl>
## 1 0            864.    3.47
## 2 1            364.    5.16
```

Berdasarkan hasil yang diperoleh konsentrasi TDS dan Uranium dipengaruhi oleh kesadahan airtanah. Pada konsentrasi Bikarbonate > 50% konsentrasi TDS akan lebih rendah sedangkan konsentrasi Uranium sebaliknya. Untuk menguji apakah nilai tersebut berbeda signifikan, kita perlu melakukan uji hipotesis yang akan dibahas pada Chapter selanjutnya.

---------------------------------------------------------

### Median Sebagai Ukuran Pemusatan Data yang Resistan

Median atau persentil 50 ($P_{50}$) merupakan nilai pusat dari distribusi suatu data yang telah dirangkin berdasarkan besar nilai orbservasinya. Untuk data dengan jumlah observasi ganjil median adalah titik tengah yang memiliki jumlah observasi yang sama baik di atas nilai media maupun di bawahnya. Untuk data dengan jumlah observasi genap, media merupakan rata-rata dari dua titik observasi pusat. Untuk memperoleh median dari suatu distribusi data, langkah pertama yang perlu dilakukan adalah mengurutkan data dari observasi dengan nilai terkecil sampai dengan yang besar sehingga $x_1$ merupakan observasi terkecil hingga $x_n$ merupakan observasi terbesar. Persamaan \@ref(eq:med1) (untuk data ganjil) dan Persamaan \@ref(eq:med2) (untuk data genap) merupakan persamaan untuk menghitung median berdasarkan jumlah observasi yang ada.

\begin{equation}
  Median (P_{0.5}) =\frac{X_{\left(n+1\right)}}{2}
  (\#eq:med1)
\end{equation} 

\begin{equation}
  Median (P_{0.5}) =\frac{1}{2}\cdot\left(X_{\left(\frac{n}{2}\right)}+X_{\left(\frac{n}{2}\right)+1}\right)
  (\#eq:med2)
\end{equation} 

Median hanya dipengaruhi minimal oleh besarnya nilai observasi tunggal, yang ditentukan semata-mata oleh urutan relatif observasi. Resitensi terhadap efek dari perubahan nilai atau kehadiran pengamatan terpencil (*outlier*) sering merupakan sifat yang diinginkan. Meski demikian median memiliki kelemahan utama yaitu kurang representatif dalam mendeskripsikan rata-rata dari data dibandingkan mean. Hal ini disebabkan karena median tidak menggunakan seluruh nilai yang ada pada data.

---------------------------------------------------------

**Contoh**

- **Analisa Nilai Median Grup Data Tunggal (Single Group)**

Kita akan menggunakan kembali data pada Tabel \@ref(tab:debitsungai) untuk menghitung median data tersebut. Pada `R` median dihitung menggunakan fungsi `median()`. Fotmat yang digunakan adalah sebagai berikut:


```r
median(x, na.rm = FALSE)
```

> **Note:**
>
> - **x**: objek atau vektor numerik.
> - **na.rm**: nilai logis yang menyatakan apakah *missing value* perlu disertakan dalam komputasi atau tidak. 

Untuk data pada Tabel \@ref(tab:debitsungai), median dapat dihitung menggunakan sintaks berikut:


```r
median(sungai$debit)
```

```
## [1] 117
```

Berdasarkan hasil komputasi diperoleh median debit sungai sebesar 117 $m^3/detik$. Nilai tersebut tidak berbeda juah dengan nilai mean tanpa *outlier* data sungai sebesar 107.4545 $m^3/detik$.

Jika kita melakukan perhitungan menggunakan menggunakan data `sungai_subset` (tanpa *outlier*), maka diperoleh 115 $m^3/detik$ yang nilainya juga tidak bergeser jauh dengan median sebelumnya yang membuktikan bahwa median resisten terhadap *outlier*.

- **Analisa Nilai Median Berdarsarkan Grup Data**

Paca contoh ini kita akan menggunakan kembali data pada Tabel \@ref(tab:gwtdsur). Sintaks berikut adalah cara menghitung median untuk data berkelompok:


```r
data_gw %>%
  group_by(Bicarbonate) %>%
  summarize(TDS=median(TDS), Uranium=median(Uranium))
```

```
## # A tibble: 2 x 3
##   Bicarbonate   TDS Uranium
##   <fct>       <dbl>   <dbl>
## 1 0            819.    1.94
## 2 1            327.    4.46
```

Pada median TDS kita tidak menemui perbedaan dengan nilai rata-ratanya. Hal ini disebabkan karena bentuk distribusinya yang relatif simetris. Sedangkan pada Uranium distribusi yang terbentuk memiliki kemencengan (*skewness*) positif. Hal ini menyebabkan nilai mean yang terbentuk akan sangat dipengaruhi oleh observasi dengan nilai ekstrim yang dimiliki.

---------------------------------------------------------

### Ukuran Pemusatan Data Lainnya

Ukuran pemusatan data lainnya yang kurang sering digunakan adalah modus, rata-rata geometrik (*geometric mean*), dan *trimmed mean*. Modus merupakan nilai observasi yang sering muncul. Jika kita visualisasikan menggunakan histogram maka modus merupakan bar tertinggi pada histogram. Modus lebih dapat diaplikasikan pada data berkelompok yang nilai observasinya merupakan integer (*finite number*) dibanding data dengan nilai kontinyu. Modus sangat mudah diperoleh, namun sangat buruk sebagai ukuran pemusatan data untuk jenis data kontinyu karena sering bergantung pengelompokan data yang sewenang-wenang atu semaunya.

*Geometric mean* sering digunakan untuk distribusi data memiliki bentuk kemencengan positif. *Geometric mean* merupakan rata-rata logaritmik yang diubah kembali ke unit asalnya. Untuk menghitungnya digunakan Persamaan \@ref(eq:geomean).

\begin{equation}
  GM = \exp\left(\overline{Y}\right)
  (\#eq:geomean)
\end{equation}

dimana

\begin{equation}
  Y_i = \ln\left(X_i\right)
  (\#eq:geomean2)
\end{equation}

Untuk data yang memiliki kemencengan positif, *geometric mean* biasanya cukup dekat dengan median. Bahkan, ketika logaritma data simetris, *geometric mean* adalah estimasi median. Ini karena median dan *geometric mean* sama. Ketika ditransformasikan kembali ke satuan asli, rerata geometris terus menjadi estimasi untuk median, tetapi bukan merupakan estimasi untuk rerata.

Pada `R` *geometric mean* dapat kita hitung menggunakan sintaks fungsi yang kita buat sendiri:


```r
geomean <- function(x){
  y = log(x)
  GM = exp(mean(y))
  return(GM)
}
```

Data pada Tabel \@ref(tab:debitsungai) merupakan data dengan kemencengan positif. Nilai *geometric mean* data tersebut dihitung menggunakan sintaks berikut:


```r
geomean(sungai$debit)
```

```
## [1] 112.4
```

Berdasarkan hasil komputasi diperoleh nilai *geometric mean* debit sungai sebesar 112.4315 $m^3/detik$. Nilai yang diperoleh tidak berbeda dengan nilai median sebesar 117 $m^3/detik$.

Kompromi antara median dan mean tersedia dengan memotong beberapa observasi terendah dan tertinggi, dan menghitung mean dari apa yang tersisa. Perkiraan pemusatan data seperti itu tidak dipengaruhi oleh observasi yang paling ekstrem (dan mungkin anomali), seperti mean. Namun mereka memungkinkan besarnya sebagian besar nilai untuk mempengaruhi estimasi, tidak seperti median. Estimator ini disebut "*trimmed mean*", dan persentase data yang diinginkan dapat dipangkas. Pemangkasan yang paling umum adalah menghapus 25 persen dari data di setiap ujung - rata-rata yang dihasilkan dari 50 persen pusat data biasanya disebut "*trimmed mean*", tetapi lebih tepatnya 25 persen *trimmed mean*. "*trimmed mean* 0%" adalah mean sampel itu sendiri, sementara memangkas semua kecuali 1 atau 2 nilai pusat menghasilkan median. Persentase pemangkasan harus secara eksplisit dinyatakan saat digunakan. *Trimmed mean* adalah estimator yang resistan, karena tidak sangat dipengaruhi oleh *outlier*, dan bekerja dengan baik untuk berbagai macam bentuk distribusi (normal, lognormal, dll). Ini dapat dianggap sebagai rata-rata tertimbang (*weighted mean*), di mana data di luar 'jendela' cutoff diberi bobot 0, dan mereka yang berada di dalam jendela bobot 1,0 (lihat Gambar \@ref(fig:tm)).

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{tm} 

}

\caption{Jendela diagram trimmed mean.}(\#fig:tm)
\end{figure}

Pada `R` *trimmed mean* dapat dihitung dengan spesifikasi argumen `trim` pada fungsi `mean()`. Pada data debit sungai (Tabel \@ref(tab:debitsungai)) dihitung *trimmed mean* dengan data yang dipangkas adalah 5% di kedua ujung observasi atau `trim=0.1`.


```r
mean(sungai$debit, trim=0.1)
```

```
## [1] 113.2
```

Nilai yang diperoleh sekarang mendekati nilai median dan *geometric mean* yaitu sebesar 113.2 $m^3/detik$.

## Ukuran Sebaran Data

Saat kita mengetahui kedalaman rata-rata sungai, kita pasti ingin mengetahui berapa interval atau variasi dari kedalamannya. Kita tidak cukup hanya dengan mengetahui nilai pemusatan datanya saja, kita juga perlu mengetahui seberapa besar variasi atau variabilitas datanya.

Variabilitas suatu data diukur dengan melihat sebaran data dari nilai rata-ratanya (mean). Semakin besar sebaran suatu data, semakin tidak berarti nilai rata-ratanya karena nilai rata-ratanya bisa sangat berbeda dari sejumlah nilai pada datanya.

### Pengukuran Klasik (Varian dan Simpangan Baku)

Varian sampel dan nilai akar dari varian sampel (Simpangan Baku) merupakan ukuran penyebaran data klasik. Sama dengan mean varian dan simpangan baku dipengaruhi oleh *outlier*. Semakin besar nilai keduanya, semakin besar variabilitas datanya. Kedua ukuran tersebut dinyatakan pada Persamaan \@ref(eq:var) dan Persamaan \@ref(eq:sd).

**Varian Sampel**

\begin{equation}
  s^2=\sum_{i=1}^n\frac{\left(X_i-\overline{X}\right)^2}{\left(n-1\right)}
  (\#eq:var)
\end{equation}

**simpangan baku**

\begin{equation}
  s=\sqrt{s^2}
  (\#eq:sd)
\end{equation}

Kedua nilai tersebut di hitung berdasarkan kuadrat deviasi nilai observasi dari rata-ratanya, sehingga jika pada data terdapat *outlier* maka nilai outlier akan memperbesar deviasi data dari nilai mean. Ketika *outlier* hadir, pengukuran menjadi tidak stabil. Hal ini akan memberi kesan sebaran data menjadi jauh lebih besar daripada yang ditunjukkan oleh mayoritas nilai pada data.

Varian dan simpangan baku pada `R` dihitung menggunakan fungsi `var()` (varian) dan `sd()`. Format yang digunakan adalah sebagai berikut:


```r
var(x, na.rm = FALSE)
sd(x, na.rm = FALSE)
```

> **Note:**
>
> - **x**: objek atau vektor numerik.
> - **na.rm**: nilai logis yang menyatakan apakah *missing value* perlu disertakan dalam komputasi atau tidak.

---------------------------------------------------------

**Contoh**

- **Analisa Varian dan simpangan baku Grup Tunggal**

Kita akan menggunakan kembali data pada Tabel \@ref(tab:debitsungai) untuk menghitung varian dan simpangan baku data tersebut. Berikut adalah sintaks untuk melakukannya:


```r
# varian data sungai
var(sungai$debit)
```

```
## [1] 11926
```

```r
# simpangan baku data sungai
sd(sungai$debit)
```

```
## [1] 109.2
```

Sekarang mari kita bandingkan dengan data yang tidak menyertakan outlier.


```r
# varian data sungai
var(sungai_subset$debit)
```

```
## [1] 1919
```

```r
# simpangan baku data sungai
sd(sungai_subset$debit)
```

```
## [1] 43.8
```

Berdasarkan hasil yang diperoleh terlihat bahwa nilai varian dan simpangan baku data dengan *outlier* jauh lebih besar dibanding data tanpa *outlier*.

- **Analisa Varian dan simpangan baku Multi Grup**

Paca contoh ini kita akan menggunakan kembali data pada Tabel \@ref(tab:gwtdsur). Sintaks berikut adalah cara menghitung varian dan simpangan baku untuk data berkelompok:


```r
data_gw %>%
  group_by(Bicarbonate) %>%
  summarize(var_TDS=var(TDS), var_Uranium=var(Uranium),
            sd_TDS=sd(TDS), sd_Uranium=sd(Uranium))
```

```
## # A tibble: 2 x 5
##   Bicarbonate var_TDS var_Uranium sd_TDS sd_Uranium
##   <fct>         <dbl>       <dbl>  <dbl>      <dbl>
## 1 0            79471.        13.0   282.       3.61
## 2 1            10559.        13.5   103.       3.68
```

Jika kita perhatikan nilai varian dan simpangan baku Uranium pada dua kondisi kesadahan memiliki nilai yang nyaris sama. Hal sebaliknya terjadi pada variabel TDS yang menunjukkan perbedaan pada dua ukuran sebaran datanya. TDS pada kesadahan >50% memiliki varian dan simpangan baku yang lebih kecil dibanding kondisi kesadahan satunya, yang menunjukkan data pada kondisi kesadahan >50% lebih tidak tersebar dibanding kesadahan satunya.

---------------------------------------------------------

### Ukuran Sebaran Data yang Resisten Terhadap Outlier

Simpangan kuartil atau *interquartile range* (IQR) merupakan ukuran sebaran data yang resisten dan paling sering digunakan. IQR mengukur kisaran 50% pusat data sehingga pengukuran tidak dipengaruhi oleh adanya outlier pada 25% pada data pada setiap ujungnya. Untuk visualisasinya kita dapat melihat kembali pada ambar \@ref(fig:tm).

IQR didefinisikan sebagai persentil ke-75 dikurangi dengan persentil ke-25. Persentil ke-75, ke-50 (median) dan ke-25 membagi data menjadi empat tempat berukuran sama. Persentil ke-75 ($P_{.75}$), juga disebut kuartil atas, adalah nilai yang melebihi tidak lebih dari 75% data dan dilampaui oleh tidak lebih dari 25 persen data. Persentil ke-25 ($P_{.25}$) atau kuartil lebih rendah adalah nilai yang melebihi tidak lebih dari 25% dari data dan dilampaui oleh tidak lebih dari 75%. Dengan mempertimbangkan data yang telah diurutkan dari yang terkecil ke yang terbesar: $X_{i}$, $i=1,...n$. Persentil ($P_j$) dihitung berdasarkan Persamaan \@ref(eq:iqr).

\begin{equation}
  P_j=X_{\left(n+1\right)\cdot j}
  (\#eq:iqr)
\end{equation}

dimana $n$ merupakan ukuran sampel $X_j$, dan $j$ merupakan fraksi data yang kurang dari atau sama dengan nilai persentil (untuk persentil ke-25, 50, dan 75, $j=.25, .50., dan .75$).

Pada `R`, IQR dapat dihitung secara langsung menggunakan fungsi `IQR()` atau secara tidak langsung menggunakan fungsi `quantile()`. Penggunaan fungsi `quantile()` digunakan untuk mencari persentil dari data. Telah dijelaskan sebelumnya bahwa IQR merupakan selisih dari persentil 75 dan persentil 25. Format yang digunakan untuk menghitung IQR adalah sebagai berikut:


```r
# secara langsung
IQR(x, na.rm=FALSE)

# secara tidak langsung
quantile(x, 3/4)-quantile(x, 1/4)

# atau
quantile(x, .75)-quantile(x, .25)
```

> **Note:**
>
> - **x**: objek atau vektor numerik.
> - **na.rm**: nilai logis yang menyatakan apakah *missing value* perlu disertakan dalam komputasi atau tidak. 

Pada Tabel \@ref(tab:debitsungai), kita dapat menghitung IQR dari data. Berikut adalah contoh sintaks yang digunakan:


```r
IQR(sungai$debit)
```

```
## [1] 72.5
```

Salah satu penaksir penyebaran yang resisten selain IQR adalah *Median Absolute Deviation*, atau MAD. MAD dihitung dengan pertama-tama mendaftar nilai absolut dari semua selisih $|d|$ antara masing-masing pengamatan dan median. Median dari nilai absolut ini adalah MAD yang ditulis berdasarkan Persamaan \@ref(eq:mad).

\begin{equation}
  MAD\ \left(X_i\right)=median\left|d\right|
  (\#eq:mad)
\end{equation}

dimana

\begin{equation}
  d_i=X_i-median\left(X_i\right)
  (\#eq:mad2)
\end{equation}

Pada `R`, MAD tidak dapat dihitung secara langsung. Kita perlu membuat *user defined function* untuk dapat digunakan sewaktu-waktu. Berikut adalah fungsi yang dibuat:


```r
MAD <- function(x){
  # median data
  m = median(x)
  # MAD
  d = abs(x-m)
  mad = mean(d)
  # print
  return (mad)
}
```

---------------------------------------------------------

**Contoh**

Pada Tabel \@ref(tab:debitsungai), kita dapat menghitung MAD dari data menggunakan fungsi yang telah dibuat. Berikut adalah contoh sintaks yang digunakan:


```r
MAD(sungai$debit)
```

```
## [1] 60.42
```

---------------------------------------------------------

## Ringkasan Data Menggunakan Fungsi summary() dan stat.desc()

Ringkasan data menggunakan fungsi `summary()` akan memberikan ringkasan data seperti nilai mean, kuartil, nilai minimum dan maksimum, serta *missing value*. Jika data berupa variabel tunggal maka output yang dihasilkan berupa nilai-nilai yang telah penulis sebutkan sebelumnya. Berikut adalah contoh sintaks yang digunakan:


```r
summary(sungai$debit)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##    50.0    67.2   117.0   136.6   139.8   457.0
```

Jika objek yang diinputkan kedalam fungsi tersebut adalah data frame, maka ringkasan data akan diberikan pada setiap kolom dengan ketentuan berikut:

- jika kolom berupa variabel numerik maka output yang diperoleh berupa mean, median, min, max dan kuartil.
- jika kolom berupa factor maka output yang dihasilkan berupa rekapan jumlah observasi pada masing-masing grup.

Berikut adalah contoh sintaks penerapannya:


```r
summary(data_gw)
```

```
##       TDS          Uranium       Bicarbonate
##  Min.   : 255   Min.   : 0.147   0:23       
##  1st Qu.: 323   1st Qu.: 1.558   1:21       
##  Median : 560   Median : 3.093              
##  Mean   : 626   Mean   : 4.276              
##  3rd Qu.: 853   3rd Qu.: 5.807              
##  Max.   :1291   Max.   :14.634
```

Ringkasan data lain dapat dilakukan dengan menggunakan fungsi `stat.desc()` dari library `pastecs`. Kelebihan dari ringkasan data menggunakan fungsi ini adalah kita tidak hanya memperoleh ringkasan data dengan ouput seperti diatas, namun kita juga memperoleh output berupa nilai *standadr error* (SE), *confidence interval* (CI), dan koefisien variasi (coef.var) yang merupakan hasil bagi dari simpangan baku dibagi dengan nilai rata-rata.

Berikut adalah sintak yang digunakan untuk menghasilkan ringkasan data menggunakan fungsi `stat.desc()`:


```r
# memasang paket
install.packages("pastecs")
```


```r
# memuat paket
library(pastecs)

# ringkasan data
stat.desc(data_gw)
```

```
##                    TDS  Uranium Bicarbonate
## nbr.val      4.400e+01  44.0000          NA
## nbr.null     0.000e+00   0.0000          NA
## nbr.na       0.000e+00   0.0000          NA
## min          2.552e+02   0.1473          NA
## max          1.291e+03  14.6342          NA
## range        1.035e+03  14.4869          NA
## sum          2.753e+04 188.1604          NA
## median       5.602e+02   3.0934          NA
## mean         6.257e+02   4.2764          NA
## SE.mean      4.986e+01   0.5572          NA
## CI.mean.0.95 1.005e+02   1.1238          NA
## var          1.094e+05  13.6623          NA
## std.dev      3.307e+02   3.6963          NA
## coef.var     5.286e-01   0.8643          NA
```

## Ukuran Kemencengan Data

Ketika data memiliki kemencengan, nilai mean tidak sama dengan median, tetapi bergeser ke arah ekor distribusi. Jadi untuk kemencengan positif, nilai mean melebihi lebih dari 50% dari data, seperti pada Gambar \@ref(fig:skew) dan Gambar \@ref(fig:skew2). Simpangan baku juga meningkat dengan data di bagian ekor. Data yang menceng juga mempertanyakan penerapan tes hipotesis yang didasarkan pada asumsi bahwa data memiliki distribusi normal. Tes-tes ini, yang disebut tes parametrik, mungkin bernilai dipertanyakan ketika diterapkan pada data seperti data sumber daya air, karena data seringkali tidak normal atau bahkan simetris. 

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{skewness} 

}

\caption{a) Kemencengan negatif, b) Kemencengan positif.}(\#fig:skew)
\end{figure}

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{skewnessbox} 

}

\caption{Box plot untuk data dengan a) Kemencengan negatif, b) Kemencengan positif.}(\#fig:skew2)
\end{figure}

### Ukuran Kemencengan Klasik

Koefisien kemencengan ($g$) merupakan ukuran kemencengan yang sering digunakan. Koefisien kemencengan dituliskan pada Persamaan \@ref(eq:g).

\begin{equation}
  g=\frac{n}{\left(n-1\right)\left(n-2\right)}\sum_{i=1}^n\frac{\left(x_i-\overline{X}\right)^3}{s^3}
  (\#eq:g)
\end{equation}

Kemencengan positif (ekor panjang kekanan) memiliki nilai $g$ positif sedangkan kemencengan negatif (ekor panjang kekiri) memiliki nilai $g$ negatif. Sekali lagi, Pengaruh beberapa *outlier* adalah penting - suatu distribusi simetris yang memiliki satu *outlier* akan menghasilkan ukuran kemencengan ($g$) yang besar (dan mungkin menyesatkan).

---------------------------------------------------------

**Contoh**

Pada `R` Kita dapat menghitung sendiri koefisien kemencengan ($g$) menggunakan *user define function*. Berikut adalah contoh sintaks fungsi yang dibuat:


```r
skew <- function(x){
  ave = mean(x)
  n = length(x)
  sd = sd(x)
  g=(n/((n-1)*(n-2)))*sum(((x-ave)^3)/(sd^3))
  return(g)
}
```

Pada contoh sebelumnya dengan menggunakan fungsi yang telah dibuat diperoleh koefisien kemencengan sebagai berikut:


```r
skew(data_gw$Uranium)
```

```
## [1] 1.184
```

---------------------------------------------------------

### Ukuran Kemencengan yang Resisten

Ukuran kemencengan yang lebih resisten adalah *quartile skew coefficient* ($qs$). Merupakan ukuran kemencengan didasarkan pada ketiga nilai kuartil data seperti yang ditunjukkan pada Persamaan \@ref(eq:qs) yang menyatakan perbedaan pada jarak kuartil atas dan bawah terhadap median dibagi dengan IQR.

\begin{equation}
  qs=\frac{\left(P_{.75}-P_{.50}\right)-\left(P_{.75}-P_{.25}\right)}{P_{.75}-P_{.25}}
  (\#eq:qs)
\end{equation}

Kemencengan positif akan memiliki nilai $qs$ positif dan begitupun sebaliknya. Pada `R` kita dapat menghitung nilai $qs$ menggunakan *user define function*. Berikut adalah contoh sintaks fungsi yang dibuat:


```r
qs <- function(x){
  p75 = quantile(x, 3/4)
  p50 = median(x)
  p25 = quantile(x, 1/4)
  skew = ((p75-p50)-(p50-p25))/(p75-p25)
  return(skew)
}
```

---------------------------------------------------------

**Contoh**

Pada contoh sebelumnya dengan menggunakan fungsi yang telah dibuat diperoleh koefisien kemencengan sebagai berikut:


```r
qs(data_gw$Uranium)
```

```
##    75% 
## 0.2772
```

---------------------------------------------------------

## Outlier

*Outlier* merupakan pengamatan yang nilainya sangat berbeda dari yang lain dalam kumpulan data, sering menimbulkan kekhawatiran atau alarm. Meskipun sebenarnya kita tidak perlu khawatir dengan adanya *outlier* . *Outlier* sering ditangani dengan membuangnya sebelum mendeskripsikan data, atau sebelum beberapa prosedur uji hipotesis chapter-chapter selanjutnya. Sekali lagi, mereka seharusnya tidak perlu dikhawatirkan. *Outlier* mungkin merupakan poin paling penting dalam kumpulan data dan harus diselidiki lebih lanjut.

Untuk lebih memahami kenapa *outlier* begitu penting pada data kita berikut merupakan contoh kasus dari asal kata *outlier*. Misalkan bahwa data pada "lubang" ozon Antartika, suatu daerah dengan konsentrasi ozon yang sangat rendah, telah dikumpulkan selama kurang lebih 10 tahun sebelum penemuan aktualnya. Namun, rutinitas pengecekan data otomatis selama pemrosesan data menyertakan instruksi untuk menghapus "*outlier*". Definisi *outlier* didasarkan pada konsentrasi ozon yang ditemukan pada pertengahan garis lintang. Dengan demikian semua data yang tidak biasa ini tidak pernah dilihat atau dipelajari selama beberapa waktu. Jika *outlier* dihapus, risiko diambil hanya dengan melihat apa yang diharapkan dilihat. Jika hal tersebut dilakukan maka anomali yang terjadi pada atmosfer dapat luput kita pelajari.

Berdasarkan kasus tersebut kita perlu dengan baik mempertimbangkan apakah *outlier* pada data perlu dihapus atau tidak. Jika berkaitan dengan pembuatan model, penghapusan *outlier* merupakan sesuatu yang dapat memperbaiki akurasi dari model. Namun, pada sebuah penelitian terkadang diperlukan informasi lebih lanjut mengapa terdapat *outlier* pada data sehingga kita dapat memperoleh pengetahuan baru dari proses pencarian tersebut.

*Outlier* dapat terjadi karena tiga hal, yaitu:

1. Kesalahan pengukuran atau perekaman data.
2. Observasi dari populasi tidak sama dengan sebagian besar data seperti misalnya data debit banji akibat jebolnya sebuah bendungan akan berbeda dengan debit banjir akibat presipitasi.
3. Kejadian langka pada sebuah populasi yang sedikit memiliki kemencengan pada distribusinya.

Metode grafis seperti box plot sangat membantu dalam mengidentifikasi *outlier*. Setiap kali *outlier* terjadi, pertama-tama verifikasi bahwa tidak ada penyalinan, titik desimal, atau kesalahan nyata lainnya yang telah dibuat. Jika tidak, tidak mungkin untuk menentukan apakah titik itu valid. Upaya yang dilakukan untuk verifikasi, seperti menjalankan kembali sampel di laboratorium, akan tergantung pada manfaat yang diperoleh versus biaya verifikasi. Kejadian masa lalu mungkin tidak dapat diduplikasi. Jika tidak ada kesalahan yang dapat dideteksi dan diperbaiki, ** *outlier* tidak boleh dibuang hanya berdasarkan fakta bahwa mereka tampak tidak biasa**. *Outlier* sering dibuang untuk membuat data cocok dengan distribusi teoretis yang sudah terbentuk sebelumnya seperti distribusi normal. Tidak ada alasan untuk menganggap bahwa mereka seharusnya dibuang! Seluruh rangkaian data dapat muncul dari distribusi yang memiliki kemencengan, dan mengambil logaritma atau transformasi lain dapat menghasilkan data yang cukup simetris. Bahkan jika tidak ada transformasi yang mencapai simetri, outlier tidak perlu dibuang. Daripada menghilangkan data aktual (dan mungkin sangat penting) untuk menggunakan prosedur analisis yang membutuhkan simetri atau normalitas, prosedur yang tahan terhadap *outlier* harus digunakan. Jika menghitung rata-rata tampak bernilai kecil karena *outlier*, median telah terbukti menjadi ukuran lokasi yang lebih tepat untuk data yang memiliki kemencengan. Jika melakukan uji-t (dijelaskan pada chapter selanjutnya) tampaknya tidak valid karena set data yang tidak normal, gunakan *rank-sum test* sebagai gantinya.

Singkatnya, biarkan panduan data prosedur analisis yang digunakan, daripada mengubah data untuk menggunakan beberapa prosedur yang memiliki persyaratan terlalu ketat untuk situasi yang dihadapi.

## Transformasi Data

Transformasi data dilakukan untuk memenuhi tiga tujuan, antara lain:

1. membuat data lebih simetris,
2. membuat data lebih linier, dan
3. membuat data memiliki varian yang konsisten.

Beberapa ilmuwan lingkungan takut bahwa dengan mentransformasikan data, hasilnya diperoleh yang sesuai dengan gagasan yang telah terbentuk sebelumnya. Oleh karena itu, transformasi adalah metode untuk **melihat apa yang ingin kita lihat** dari data. Namun dalam kenyataannya, masalah serius dapat terjadi ketika prosedur dengan asumsi simetri, linieritas, atau homoseksualitas (varians konstan) digunakan pada data yang tidak memiliki karakteristik yang diperlukan ini. Transformasi dapat menghasilkan karakteristik ini, dan dengan demikian penggunaan variabel yang diubah memenuhi tujuan. 

Satu unit pengukuran tidak lebih valid secara apriori daripada yang lainnya. Sebagai contoh, logaritma negatif konsentrasi ion hidrogen (pH), sama validnya dengan sistem pengukuran dengan konsentrasi ion hidrogen itu sendiri. Transformasi seperti akar kuadrat kedalaman air pada sumur sumur, atau akar kubik volume curah hujan, seharusnya tidak mengandung stigma lebih daripada pH. Skala pengukuran ini mungkin lebih sesuai untuk analisis data daripada unit aslinya. Hoaglin (1988) telah menulis artikel yang bagus tentang transformasi tersembunyi, secara konsisten diterima begitu saja, yang umum digunakan oleh semua orang. Oktaf dalam musik adalah transformasi frekuensi logaritmik. Setiap kali piano dimainkan, transformasi logaritmik digunakan! Begitu pula dengan skala Richter untukgempa bumi, mil per galon untuk konsumsi bensin, f-stop untuk eksposur kamera, dll. semua menggunakan transformasi. Dalam ilmu analisis data, keputusan yang menggunakan skala pengukuran harus ditentukan oleh data, bukan dengan kriteria yang ditentukan sebelumnya. Tujuan penggunaan transformasi adalah untuk kesimetrian, linieritas, dan homoskedastisitas. Selain itu, penggunaan banyak teknik tahan seperti persentil dan prosedur uji nonparametrik (akan dibahas kemudian) tidak berbeda dengan skala pengukuran. Hasil *rank-sum test*, setara nonparametrik dari uji-t, akan persis sama apakah unit asli atau logaritma dari unit tersebut digunakan.

Untuk membuat distribusi asimetris menjadi lebih simetris, data dapat diubah atau diekspresikan kembali menjadi unit baru. Unit-unit baru ini mengubah jarak antara pengamatan pada plot garis. Efeknya adalah memperluas atau mengecilkan jarak ke pengamatan ekstrem di satu sisi median, membuatnya lebih pada setiap sisinya. Transformasi yang paling umum digunakan dalam bidang lingkungan adalah logaritma, seperti Log debit air, konduktivitas hidrolik, atau konsentrasi sering diambil sebelum analisis statistik dilakukan.

Transformasi data biasanya melibatkan fungsi power seperti pada fungsi $y=x^\theta$, dimana x merupakan data yang belum ditransformasi, y adalah data yang telah ditransformasi, dan $\theta$ merupakan power eksponensial. Pada Gambar \@ref(fig:power) nilai $\theta$ di-list kedalam "*ladder of powers*" (Velleman dan Hoaglin, 1981 dalam helsel dan Hirsch, 2002), sebuah struktur yang berguna untuk menentukan nilai $\theta$ yang tepat.

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{ladder} 

}

\caption{Ladder of power}(\#fig:power)
\end{figure}

Seperti yang dapat dilihat dari *ladder of powers*, setiap transformasi dengan $\theta$ kurang dari 1 dapat digunakan untuk membuat data dengan kemencengan positif lebih simetris. Dengan membuat box plot atau plot Q-Q dari data yang diubah kita dapat mengetahui apakah transformasi yang telah dilakukan sesuai. Jika transformasi logaritmik memberikan kompensasi yang berlebihan untuk kemiringan yang tepat dan menghasilkan distribusi yang sedikit kiri (kemencengan negatif), transformasi 'lebih ringan' dengan $\theta$ lebih dekat ke 1, seperti transformasi kuadrat atau akar kubik, harus digunakan. Transformasi dengan $\theta$> 1 akan membantu membuat data yang condong ke kiri lebih simetris.

Namun, kecenderungan untuk mencari transformasi 'terbaik' harus dihindari. Misalnya, ketika berhadapan dengan beberapa set data yang serupa, mungkin lebih baik untuk menemukan satu transformasi yang bekerja cukup baik untuk semua, daripada menggunakan yang sedikit berbeda untuk masing-masingnya. Harus diingat bahwa setiap set data adalah sampel dari populasi yang lebih besar, dan sampel lain dari populasi yang sama kemungkinan akan menunjukkan transformasi 'terbaik' yang sedikit berbeda. Penentuan 'terbaik' dalam ketelitian tinggi adalah pendekatan yang jarang sepadan dengan usaha.

Pada Gambar \@ref(fig:gwvis2) kosentrasi distribusi `Uranium` pada tiap grup memiliki kemencengan positif. Untuk membuatnya simetris kita perlu melakukan transformasi yang sesuai jenis transformasi yang dilakukan dapat dimulai dari akar kuadrat sampai invers akar kuadrat (berdasarkan Gambar \@ref(fig:power)). Pada contoh ini kita akan mencoba melakukan trasnformasi logaritmik. Berikut adalah contoh visualisasi hasil transformasinya (lihat Gambar \@ref(fig:urantrans):

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/urantrans-1} 

}

\caption{Visualisasi konsentrasi Uranium  hasil tansformasi pada air tanah}(\#fig:urantrans)
\end{figure}

Berdasarkan hasil transformasi, kita telah memperoleh ditribusi yang cukup simetris untuk kedua grup data tersebut. Pembaca dapat mencobanya menggunakan transformasi lainnya sendiri.

## Referensi

1. Damanhuri, E. 2011. **Statitika Lingkunga**. Penerbit ITB.
2. Helsel, D.R., Hirsch, R.M. 2002. **statistical Methods in Water Resources**. USGS.
3. Ofungwu, J. 2014. **Statistical Applications For Environmental Analysis and Risk Assessment**.  John Wiley & Sons, Inc.
4. Rosadi, D. 2015. **Analisis Statistika dengan R**. Gadjah Mada University Press.
5. STHDA. **Descriptive Statistics and Graphics**. <http://www.sthda.com/english/wiki/descriptive-statistics-and-graphics>.



<!--chapter:end:06-eksplorasi-data-ringkasan-numerik.Rmd-->

# Ekplorasi Data Menggunakan Grafik

Pada Chapter 4 dan 5 kita telah belajar bagaimana cara membuat grafik menggunakan `R`. Sejauh ini kita belum belajar kegunaan dari masing-masing grafik yang telah kita pelajarai. Pada Chapter ini kita tidak lagi akan membahas bagaimana membuat grafik menggunakan `R`. Kita akan fokus terhadap fungsi grafik tersebut dalam analisa kita. Secara umum grafik dibuat untuk memvisualisasikan distribusi, perbedaan antar sampel, korelasi dan asosiasi antar sampel, serta ukuran sampel.

Penulis dan pembaca pasti sepakat bahwa visualisasi data merupakan tahapan awal yang perlu kita lakukan sebelum memutuskan untuk melakukan analisa data seperti uji hipotesis dan modeling. Angka yang ditampilkan dalam ringkasan data tidaklah cukup untuk melihat data terutama kaitannya dengan pengecekan terhadap asumsi model. 

Pada Gambar \@ref(fig:visscat) disajikan delapan buah scatterplot dengan koefisien korelasi yang sama persis. Komputasi statistik tanpa melihat pada visualisasi data akan menyebabkan misinterpretasi pada data. Grafik memberikan ringkasan visual data dengan cepat dan lengkap dibandingkan penyajian data dalam tabel angka.

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{visscat} 

}

\caption{Scatterplot dengan koefisien korelasi r=0,7.}(\#fig:visscat)
\end{figure}

Grafik sangat penting untuk dua tujuan:

1. untuk memberikan wawasan bagi analis ke dalam data di bawah pengawasan, dan
2. untuk mengilustrasikan konsep-konsep penting ketika mempresentasikan hasil kepada orang lain.

Tugas pertama disebut **Analisis Data Eksplorasi (EDA)**, dan merupakan subjek Chapter ini. Prosedur EDA seringkali merupakan (atau seharusnya) menjadi 'pandangan pertama' pada data. Pola dan teori tentang bagaimana sistem berperilaku dikembangkan dengan mengamati data melalui grafik. Ini adalah prosedur induktif - data dirangkum dibanding dilakukan pengujian. Hasil mereka memberikan panduan untuk pemilihan prosedur pengujian hipotesis deduktif yang tepat.

Setelah analisis selesai, temuan harus dilaporkan kepada orang lain. Apakah laporan tertulis atau presentasi lisan, analis harus meyakinkan audiens bahwa kesimpulan yang dicapai didukung oleh data. Tidak ada cara yang lebih baik untuk melakukan ini selain melalui grafik. Banyak metode grafis yang sama yang merangkum informasi dengan ringkas untuk analis juga akan memberikan wawasan tentang data untuk pembaca atau audiens.

## Grafik Untuk Melihat Ditribusi Data

Analisis yang umumnya dilihat pada distribusi data adalah apakah data berdistribusi normal atau tidak. Hal ini akan mempengaruhi jenis analisis statistika yang digunakan pada data. Terdapat beberapa grafik yang dapat digunakan untuk melihat bentuk ditribusi data. Grafik-grafik tersebut antara lain: *stem and leaf*, histogram, density plot, QQ-plot, serta box plot atau violin plot. Pada analisis distribusi *stem and leaf* kurang populer untuk digunakan. Hal ini disebabkan karena visualisasinya kurang cocok diterapkan pada data dengan jumlah observasi besar. Selain itu, kita juga tidak bisa melakukan perbandingan antar grup menggunakan jenis visualisasi tersebut.

### Histogram

Histogram adalah grafik yang sudah dikenal, dan konstruksinya dirinci dalam berbagai teks pengantar tentang statistik. Batang digambar dengan tinggi $n_i$, atau fraksi $n_i/n$, dari data yang termasuk dalam salah satu dari beberapa kategori atau interval (Gambar \@ref(fig:histeda)). Iman dan Conover (1983) mengemukakan bahwa untuk ukuran sampel $n$, jumlah interval $k$ harus bilangan bulat terkecil sehingga $2^k≥n$.

Histogram sangat berguna untuk menggambarkan perbedaan besar dalam bentuk data seperti apakah data simetris seperti distribusi normal atau memiliki kemencengan. Histogram tidak dapat digunakan untuk penilaian yang lebih tepat karena tampilan dipengaruhi oleh jumlah batang yang digunakan. Untuk lebih memahaminya perhatikan Gambar \@ref(fig:histeda) dan Gambar \@ref(fig:histeda2). Kedua histogram tersebut tampak berbeda meskipun data input yang diberikan sama. Pada Gambar \@ref(fig:histeda) kita akan melihat bahwa debit dengan kejadian terbanyak terjadi pada rentang 800-900 cfs, sedangkan pada Gambar \@ref(fig:histeda2) kita melihat bahwa debit dengan kejadian terbanyak terjadi pada 800-1200 cfs.


```r
# memuat library
library(readxl)
library(ggplot2)
library(ggthemes)

# memuat data excel
sungai <- read_excel("hhappc.xls", sheet="appc1")
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/histeda-1} 

}

\caption{Histogram dengan bin.width=default debit sungai Saddle}(\#fig:histeda)
\end{figure}

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/histeda2-1} 

}

\caption{Histogram dengan bin.width=500 debit sungai Saddle}(\#fig:histeda2)
\end{figure}

### Density Plot

Density plot memecahkan masalah yang dimiliki histogram dalam melihat grafik dengan menyajikan data bukan dari jumlah kejadian atau observasi, namun data disajikan berdasarkan frekuensi relatif data (density) yang digambarkan dalam bentuk *smooth curve*. Contoh density plot dapat dilijat pada Gambar \@ref(fig:denseda). Dari grafik yang dihasilkan sekaran tampak jelas bahwa distibusi data memiliki kemencengan positif dengan frekuensi relatif debit terbanyak berada pada debit 1000 cfs.

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/denseda-1} 

}

\caption{Density plot debit sungai Saddle}(\#fig:denseda)
\end{figure}

### QQ-plot

Kita telah mempelajari sebelumnya pada Chapter 5 bahwa QQ-plot data digunakan untuk mengecek apakah data yang kita miliki berdistribusi normal atau tidak. Contoh QQ-plot dapat dilijat pada Gambar \@ref(fig:qqeda). Pada grafik yang dihasilkan terlihat bahwa data tidak berdistribusi normal. Hal ini terlihat dari sebagian observasi pada debit <1000 cfs yang tidak mengikuti garis referensi.


```r
ggplot(sungai, aes(sample=Flow))+
  # qq plot
  stat_qq()+
  # garis referensi
  stat_qq_line()+
  theme_economist()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/qqeda-1} 

}

\caption{QQ plot debit sungai Saddle}(\#fig:qqeda)
\end{figure}

Bentuk lain yang dapat digunakan untuk menguji kecocokan suatu distribusi dengan distribusi normal adalah grafik ECDF. Berbeda dengan QQ-plot, grafik ini dapat digunakan untuk melakukan pengecekan distribusi secara umum.

### Box Plot dan Violin Plot

Grafik lain yang dapat digunakan untuk menggambarkan distribusi data adalah box plot dan violin plot. Box plot memberikan cara yang simpel untuk melihat ditribusi data seperti melihat posisi sejumlah kuartil, nilai minimum dan maksimum. Selain itu kita juga dapat melihat adanya outlier pada data. 

Kita dapat menambah fungsionalitas dari box plot ini dengan menambahkan violin plot. Pada Chapter 5 kita telah belajar bahwa kita dapat menambahkan box plot pada violin plot atau sebaliknya sehingga memudahkan dalam mendeskripsikan bentuk distribusi data. Jika dengan box plot kita tidak dapat melihat secara baik bentuk dari data yang sesungguhnya karena hanya menampilkan lokasi sejumlah kuartil. Pada violin plot kita dapat melihat bentuk data yang ada melalui tampilan dua denisty plot (tampak seperti biola) yang digambarkan. Kekurangannya adalah kita tidak dapat melihat observasi mana yang menjadi outlier, sehingga kedua grafik ini biasa digambarkan secara bersamaan. Berikut adalah contoh box plot dan violin plot dari data debit sungai Saddle (Gambar \@ref(fig:bpeda)).


```r
ggplot(sungai, aes(x="", y=Flow))+
  geom_violin(fill="blue", alpha=0.5, color="white")+
  geom_boxplot(width=0.1)+
  theme_economist()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/bpeda-1} 

}

\caption{Box plot dan violin plot debit sungai Saddle}(\#fig:bpeda)
\end{figure}

Berdasarkan grafik yang dihasilkan pada Gambar \@ref(fig:bpeda) kita dapat melihat bahwa ditribusi data debit sungai memiliki kemencengan positif. Hal ini terjadi karena terdapat satu *outlier* pada data yang disebabkan karena nilai observasinya diluar dari nilai maksimum data yang ditetapkan sebagai $max=Q3 + 1,5*IQR$.

## Grafik Untuk Melihat Beda Distribusi Data Antar Grup

Grafik yang telah dijelaskan sebelumnya seperti box plot, violin plot, histogram, dan density plot merupakan grafik yang bagus untuk memvisualisasikan beda distribusi data antar grup untuk data numerik. Untuk data berupa kategori kita dapat menggunakan bar plot. Pada penerapannya bar plot juga dapat memvisualisasikan ringkasan data seperti nilai mean dan sebarannya pada data.

Pada contoh ini penulis hanya akan memberikan contoh penerapan menggunakan box plot dan bar plot menggunakan data konsentrasi Antrazine yang diukur pada bulan Juni dan September. Untuk melakukannya kita perlu memuat data dan melakukan transformasi terhadap datanya terlebih dahulu.


```r
# memuat data excel
atrazine <- read_excel("hhappc.xls", sheet="appc4")

# print
head(atrazine)
```

```
## # A tibble: 6 x 2
##   June_atrazine Sept_atrazine
##           <dbl>         <dbl>
## 1          0.38         2.66 
## 2          0.04         0.63 
## 3         -0.01         0.59 
## 4          0.03         0.05 
## 5          0.03         0.84 
## 6          0.05         0.580
```

```r
# transformasi data
library(tidyr)
atrazine <- gather(atrazine,
                 key="month",
                 value="concentration")

# print
head(atrazine)
```

```
## # A tibble: 6 x 2
##   month         concentration
##   <chr>                 <dbl>
## 1 June_atrazine          0.38
## 2 June_atrazine          0.04
## 3 June_atrazine         -0.01
## 4 June_atrazine          0.03
## 5 June_atrazine          0.03
## 6 June_atrazine          0.05
```

Pada data konsentrasi Atrazine tersebut terdapat nilai negatif yang dalam hal ini merupakan kesalahan dalam pengukuran dari alat. Untuk membersihkannya kita dapat membuat nilai observasi tersebut menjadi NA.


```r
atrazine$concentration[atrazine$concentration<0]<-NA

head(atrazine)
```

```
## # A tibble: 6 x 2
##   month         concentration
##   <chr>                 <dbl>
## 1 June_atrazine          0.38
## 2 June_atrazine          0.04
## 3 June_atrazine         NA   
## 4 June_atrazine          0.03
## 5 June_atrazine          0.03
## 6 June_atrazine          0.05
```


Selanjutnya kita akan memvisualisasikan beda antara distribusi data pada kedua bulan menggunakan box plot (Gambar \@ref(fig:bpgeda)). Konsentrasi rata-rata Atrazine akan divisualisasikan menggunakan bar plot (Gambar \@ref(fig:bargeda)).


```r
ggplot(atrazine, aes(month, concentration, fill=month))+
  geom_boxplot()+
  theme_economist()+
  scale_fill_economist()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/bpgeda-1} 

}

\caption{Box plot konsentrasi Atrazine pada bulan Juni dan September}(\#fig:bpgeda)
\end{figure}


```r
library(dplyr)
atrazine %>%
  group_by(month) %>%
  summarize(mean_atrazine=mean(concentration, na.rm=TRUE)) %>%
  ggplot(aes(month, mean_atrazine, fill=month))+
    geom_bar(stat="identity")+
    theme_economist()+
    scale_fill_economist()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/bargeda-1} 

}

\caption{Bar plot konsentrasi Atrazine pada bulan Juni dan September}(\#fig:bargeda)
\end{figure}

Pada visualisasi yang dihasilkan terdapat perbedaan signifikan antara distribusi dan nilai rata-rata konsentrasi Atrazine pada dua periode tersebut. Hal ini disebabkan karena terdapat sebuah outlier pada periode Sepetember yang menyebabkan nilai rata-rata yang dihasilkan bergeser jauh kearah outlier. Pembaca dapat membuat visualisasi data pada data tersebut tanpa *outlier* dengan terlebih dahulu melakukan filter terhadap *outlier*.

## Grafik Untuk Memvisualisasikan Korelasi Antar Variabel

Scatterplot dapat digunakan untuk memvisualisasikan korelasi antar dua variabel. Pada bagian ini akan diberikan contoh visualisasi antara variabel konsentrasi TDS dan Uranium pada air tanah. 

Untuk melakukannya kita perlu memuat terlebih dahulu dataset yang digunakan. Visualisasi data disajikan pada Gambar \@ref(fig:scateda).


```r
# memuat data excel
gw <- read_excel("hhappc.xls", sheet="appc16")
```


```r
ggplot(gw, aes(TDS, Uranium))+
  geom_point()+
  geom_smooth(method="lm")+
  theme_economist()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/scateda-1} 

}

\caption{Scatterplot hubungan antara konsentrasi TDS dan Uranium pada airtanah}(\#fig:scateda)
\end{figure}

Berdasarkan grafik yang dihasilkan terdapat hubungan linier antara konsentrasi TDS dan Uranium pada airtanah. Meningkatnya konsentrasi TDS pada air tanah juga menyebabkan peningkatan konsentrasi Uranium pada airtanah.

## Grafik Yang Digunakan Untuk Memvisualisasikan Asosiasi Antar Variabel

Asosiasi antar variabel kategori dapat dilakukan baik dengan pie chart maupun dengan bar plot. Pie chart kurang sering digunakan untuk visualisasi *multiple group* sehingga bar plot lebih sering digunakan.

Pada contoh kali ini penulis akan melihat terdapat asoiasi antara musim dan strata terhadap jumlah Corbicula di sungai Tennessee. Untuk melakukannya kita perlu memuat terlebih dahulu dataset yang digunakan. Visualisasi data disajikan pada Gambar \@ref(fig:barteneda).


```r
# memuat data excel
corbicula<- read_excel("hhappc.xls", sheet="appc8")

# print
head(corbicula)
```

```
## # A tibble: 6 x 4
##    Year Season Strata Corbicula
##   <dbl> <chr>   <dbl>     <dbl>
## 1  1969 Winter      1        25
## 2  1969 Winter      1        20
## 3  1969 Winter      1        30
## 4  1969 Spring      1         9
## 5  1969 Spring      1         8
## 6  1969 Spring      1         9
```


```r
corbicula %>%
  mutate(Season=as.factor(Season),
         Strata=as.factor(Strata)) %>%
  group_by(Season,Strata) %>%
  summarize(Corbicula=mean(Corbicula)) %>%
  ggplot(aes(Season, Corbicula, fill=Strata))+
    geom_bar(stat="identity",position=position_dodge2())+
    theme_economist()+
    scale_fill_economist()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/barteneda-1} 

}

\caption{Bar plot Jumlah rata-rata corbicula pada sungai Tennessee}(\#fig:barteneda)
\end{figure}

Berdasarkan grafik yang dihasilkan terdapat pengaruh musim dan strata terhadap jumlah corbicula di sungai Tennessee. Jumlah tertinggi berada saat musim semi pada strata 3, sedangkan terendah berada pada musim dingin juga pada strata 3.

## Grafik Yang Digunakan Untuk Memisualisasikan Ukuran Sampel dan Perubahan Sepanjang Waktu

Untuk memvisualisasikan perubahan sepanjang waktu, kita dapat menggunakan line plot. Pada data `corbicula` kita ingin memvisualisasikan perubahan jumlah corbicula rata-rata pada setiap tahun. Visualisasi dari data disajikan pada Gambar \@ref(fig:lineeda).


```r
corbicula %>%
  group_by(Year) %>%
  summarize(Corbicula=mean(Corbicula)) %>%
  ggplot(aes(Year, Corbicula))+
    geom_line()+
    geom_point(shape=1)+
    theme_economist()
```

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/lineeda-1} 

}

\caption{Line plot perubahan jumlah rata-rata corbicula di sungai Tennessee}(\#fig:lineeda)
\end{figure}

Berdasarkan garfik yang dihasilkan dapat disimpulkan bahwa jumlah rata-rata corbicula menurun setiap tahunnya.

## Referensi

1. Gardener, M. 2012. **Statistics for Ecologists Using R and Excel-Data collection, exploration, analysis and presentation**. Pelagic Publishing. 
2. Helsel, D.R., Hirsch, R.M. 2002. **statistical Methods in Water Resources**. USGS.
3. Ofungwu, J. 2014. **Statistical Applications For Environmental Analysis and Risk Assessment**.  John Wiley & Sons, Inc.
4. Peck, R.Devore, J.L. 2012. **Statistics The Exploration & Analysis of Data- Seventh Edition**. Brooks/Cole. 

<!--chapter:end:07-ekplorasi-data-menggunakan-grafik.Rmd-->

# (PART\*) Probabilitas dan Distribusi Probabilitas {-}

<style>
body{
text-align: justify}
</style>

# Probabilitas

Probabilitas merupakan kemungkinan suatu peristiwa akan terjadi. Probabilitas memiliki rentang nilai dari 0 sampai dengan 1. Probabilitas 0 artinya suatu peristiwa (*event*) mustahil atau tidak pernah terjadi, sedangkan probabilitas 1 menunjukkan suatu peristiwa yang selalu terjadi.

Contoh sederhana dari probabilitas dalam kehidupan sehari-hari adalah ketika kita melempar koin ke udara untuk melihat kemungkinan sisi yang akan tampak saat koin tersebut jatuh ke tanah. Peristiwa yang mungkin akan terjadi adalah mata uang akan menampilkan sisi depan (*head*) atau sisi belakang (*tail*). Kemungkinan untuk mendapatkan *tail* maupun *head* adalah sama yaitu 0,5. 

Pada contoh pelempan koin, kita misalkan kejadian munculnya sisi *head* adalah $A$, sedangkan peluang munculnya selain sisi *head* (sisi lainnya) adalah $A'$  Secara sederhana peluang munculnya suatu kejadian $A$ pada contoh tersebut dapat dituliskan kedalam Persamaan \@ref(eq:prob) dan Persamaan \@ref(eq:prob).

\begin{equation}
   P\left(A\right)+P\left(A'\right)=1
  (\#eq:prob)
\end{equation}

dimana

\begin{equation}
   P_A=\frac{Jumlah\ peristiwa\ A}{Jumlah\ peristiwa\ yang\ mungkin\ terjadi}
  (\#eq:prob2)
\end{equation}

Pada contoh pelemparan koin, kita ingin mengetahui peluang munculnya *head* pada pelemparan koin. Jumlah peristiwa yang mungkin terjadi saat pelemparan koin ada 2 yaitu munculnya *head* atau *tail*. Peluang munculnya sisi *head* dapat dihitung menggunakan Persamaan \@ref(eq:prob) seperti berikut:

$$
P_{head}=\frac{Jumlah\ peristiwa\ head}{Jumlah\ peristiwa\ yang\ mungkin\ terjadi}=\frac{1}{2}=0,5
$$

Probabilitas suatu peristiwa dapat dibedakan kedalam 3 kategori, yaitu:

1. **Probabilitas apriori**: probabilitas yang ditentukan sebelumnya tanpa perlu melakukan suatu eksperimen atau kita dapat memperkirakan sebelumnya peristiwa apa saja yang dapat terjadi. Contoh: pelemparan koin, pelemparan dadu,dll.
2. **Probabilitas frekuensi relatif (empiris)**: probabilitas yang ditentukan berdasarkan fakta setelah kejadian. Contoh: Berdasarkan hasil survey 80 dari 100 orang responden mahasiswa sadar akan pentingnya memilah sampah, sehingga peluang seorang mahasiswa sadar akan pentingnya pemilahan sampah berdasarkan hasil survey tersebut adalah $P_A=\frac{80}{100}=0,8$.
3. **Probabilitas subyektif**: probabilitas yang dilakukan berdasarkan pertimbangan perseorangan (seorang ahli atau orang yang berpengalaman). Contoh: probabilitas 10 kantong kompos memiliki berat < 1 kg menurut seorang penjual berdasarkan pengalamannya adalah 0,1 atau dari 10 kantong kompos terdapat satu kantong yang beratnya < 1 kg.

## Aturan Dasar Probabilitas

Secara umum terdapat dua buah aturan dasar yang digunakan dalam perhitungan probabilitas yaitu aturan penjumlahan dan aturan perkalian. Kedua aturan tersebut akan penulis bahas secara detail pada bagian ini.

Sebelum kita membahas keduanya sebaiknya kita bahas terlebih dahulu pengertian umum yang merupakan elemen dasar dalam memahami konsep probabilitas. Berikut adalah istilah-istilah yang digunakan dalam probabilitas:

1. **Ruang sampel (*sample space*)**: gabungan dari semua kemungkinan, dan kemungkinan secara individual yang disebut sebagai titik sampel. Suatu peristiwa didefinisikan sebagai sub-himpunan (*subset*) dari ruang sampel. Ruang sampel bisa bersifat diskrit atau kontinu, yang dapat bernilai berhingga (*finite*) maupun tak berhingga. Peristiwa dalam pelemparan koin merupakan contoh ruang sampel berhingga. Contoh lainnya adalah pada pelemparan 2 buah dadu. Ruang sampel yang mungkin terbentuk merupakan kombinasi dari keenam masing-masing mata dadu. Berikut adalah contoh sintaks `R` untuk menghasilkan ruang sampel pada 2 buah dadu:


```r
# install.packages("prob")
library(prob)

# ruang sampel 2 buah dadu
rolldie(2)
```

```
##    X1 X2
## 1   1  1
## 2   2  1
## 3   3  1
## 4   4  1
## 5   5  1
## 6   6  1
## 7   1  2
## 8   2  2
## 9   3  2
## 10  4  2
## 11  5  2
## 12  6  2
## 13  1  3
## 14  2  3
## 15  3  3
## 16  4  3
## 17  5  3
## 18  6  3
## 19  1  4
## 20  2  4
## 21  3  4
## 22  4  4
## 23  5  4
## 24  6  4
## 25  1  5
## 26  2  5
## 27  3  5
## 28  4  5
## 29  5  5
## 30  6  5
## 31  1  6
## 32  2  6
## 33  3  6
## 34  4  6
## 35  5  6
## 36  6  6
```

Berdasarkan sintaks tersebut terdapat 36 ruang sampel pada pelemparan 2 buah dadu. Ruang sampel yang dihasilkan dapat ditulis $Ruang\ sampel\ S=\left\{\left(X1,X2\right)\left|1\le X1\le6;\ 1\le X2\le6\right|\right\}$.

2. **Peristiwa mustahil (*impossible event*)**: dinyatakan dengan $\phi$, merupakan peristiwa yang tidak memiliki titik sampel. Dengan demikian , peristiwa tersebut mempunyai himpunan kosong.
3. **Peristiwa tertentu (*certain event*)**: dinyatakan dengan S, merupakan semua peristiwa yang mengandung semua titik sampel dalam ruang sampel.
4. **Peristiwa komplementer (*complementary event*)**: Untuk suatu peristiwa dalam ruang sampel S, peristiwa komplementer dinyatakan dengan E yang mencakup semua titik sampel dalam S yang tidak terkandung dalam E.

Setelah pembaca memahami seluruh istilah tersebut, kita akan kembali menjelaskan kedua aturan dasar perhitungan probabilitas yaitu aturan penjumlahan dan perkalian.

Aturan penjumlahan merupakan aturan yang digunakan untuk menghitung suatu peristiwa A atau peristiwa lain yaitu peristiwa B yang akan terjadi dan ditulis sebagai $P\left(A\ atau\ B\right)$ atau $P\left(A\cup B\right)$. Terdapat dua buah aturan penjumlahan yaitu:

1. Aturan penjumlahan peristiwa *mutually exclusive*.
2. Aturan penjumlahan untuk peristiwa *not mutually exclusive*.

Aturan selanjutnya adalah aturan perkalian yaitu aturan yang digunakan untuk menghitung bahwa peristiwa A dan peristiwa B akan terjadi bersamaan dan ditulis sebagai $P\left(A\ dan\ B\right)$ atau $P\left(A\cap B\right)$. Aturan ini terdiri atas:

1. Aturan perkalian peristiwa *independent* (bebas).
2. Aturan perkalian peristiwa *dependent* (tidak bebas).

### Peristiwa *Mutually Exclusive*

Peristiwa *mutually exclusive* merupakan suatu kondisi dimana peristiwa peristiwa satu tidak memungkinkan terjadinya peristiwa lainnya (tidak mungkin terjadi bersamaan). Terjadinya peristiwa A atu B merupakan penjumlahan kemungkinan terjadinya kedua peristiwa tersebut. Probabilitas peritiwa *mutually exclusive* dapat dituliskan menggunakan Persamaan \@ref(eq:pme).

\begin{equation}
   P\left(A\cup B\right)=P\left(A\right)+P\left(B\right)
  (\#eq:pme)
\end{equation}

**Contoh**

Bayangkan pembaca diminta melemparkan sebuah dadu. Pembaca diminta untuk menentukan peluang munculnya angka 1 atau 6 pada dadu. Kedua peristiwa tersebut tidak mungkin terjadi bersamaan karena hanya dilakukan menggunakan satu dadu. Selain itu, jumlah himpunan masing-masing peristiwa pertama dan kedua hanyalah satu sehingga tidak memungkinkan adanya irisan pada kedua peristiwa tersebut. Untuk menghitungnya kita dapat langsung menggunakan Persamaan \@ref(eq:pme).

$$
P\left(1\cup 6\right)=P\left(1\right)+P\left(6\right)=\frac{1}{6}+\frac{1}{6}=\frac{1}{3}
$$

Peristiwa pada contoh soal tersebut dapat digambarkan menggunakan diagram venn yang ditunjukkan pada Gambar \@ref(fig:pmevis)).

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{pmevis} 

}

\caption{Diagram venn peristiwa mutually exclusive}(\#fig:pmevis)
\end{figure}

Jika pembaca ingin menggunakan `R` untuk menghitung probabilitas peristiwa *mutually exclusive*, pembaca dapat menggunakan fungsi `Prob()` pada library `prob` untuk menghitung secara langsung probabilitas dari *subset* data. Berikut adalah contoh sintak untuk menghitung probabilitas munculnya angka 1 atau 6 dari pelemparan sebuah dadu:


```r
# menentukan ruang sampel (S)
S <- rolldie(1, makespace=TRUE)

# print
S
```

```
##   X1  probs
## 1  1 0.1667
## 2  2 0.1667
## 3  3 0.1667
## 4  4 0.1667
## 5  5 0.1667
## 6  6 0.1667
```

```r
# membuat subset peristiwa 1 dan 2
P1 <- subset(S, X1==1)
P6 <- subset(S, X1==6)

# menghitung probabilitas gabungan
P1$probs + P6$probs
```

```
## [1] 0.3333
```

```r
# atau
Prob(P1) + Prob(P6)
```

```
## [1] 0.3333
```

Persamaan \@ref(eq:pme) dapat diperluas tidak hanya berlaku pada dua buah peristiwa. Jika jenis peristiwa A yang ada sebanyak $n$, maka Persamaan \@ref(eq:pme) dapat dituliskan kembali menjadi Persamaan \@ref(eq:pme2).

\begin{equation}
   P\left(A_1\cup A_2\cup...\cup A_n\right)=P\left(A_1\right)+P\left(A_2\right)+...+P\left(A_n\right)
  (\#eq:pme2)
\end{equation}

Kumpulan peristiwa yang terjadi $\left\{A_1,\ A_2,...,A_n\right\}$ pada ruang sampel $S$ disebut sebagai *partisi S* jika $A_1,\ A_2,...,A_n$ merupakan peristiwa dan $A_1\cup A_2\cup...\cup A_n=S$. Sehingga probabilitas seluruh partisi tersebut dapat dituliskan pada Persamaan \@ref(eq:pme3).

\begin{equation}
   P\left(A_1\cup A_2\cup...\cup A_n\right)=P\left(A_1\right)+P\left(A_2\right)+...+P\left(A_n\right)=P\left(S\right)=1
  (\#eq:pme3)
\end{equation}  

### Peristiwa *Not Mutually Exclusive*

Bila dua buah peristiwa tidak *mutually exclusive*, maka kedua peristiwa tersebut dapat terjadi secara bersamaan atau memiliki himpunan yang saling beririsan jika ditinjau dari pembahasan pelemparan dadu sebelumnya. Probabilitas suatu peristiwa yang tidak *mutually exclusive* dapat dituliskan berdasarkan Persamaan \@ref(eq:pnme).

\begin{equation}
   P\left(A\cup B\right)=P\left(A\right)+P\left(B\right)-P\left(A\cap B\right)
  (\#eq:pnme)
\end{equation}

**Contoh 1**

Pembaca dapat membayangkan kembali melempar sebuah dadu. Pembaca diminta menghitung probabilitas keluar angka ganjil pada dadu atau angka prima pada dadu. Kedua peristiwa tersebut memiliki himpunannya masing-masing. Untuk peristiwa angka ganjil himpunan yang terjadi adalah ganjil={1, 3, 5}, sedangkan untuk angka prima adalah prima={1, 2, 3, 5}. Kedua peristiwa tersebut memiliki irisan himpunan yaitu saat mata dadu menunjukkan angka 1, 3, dan 5. Nilai probabilitas kedua peristiwa tersebut tidak bisa dihitung dengan langsung menjumlahkan probabilitas keduanya masing-masing karena terdapat satu peristiwa yang merupakan bagian dari peristiwa lain sehingga peristiwa tersebut sebagian perlu dihilangkan dari probabilitas salah satunya seperti yang ditulikan pada Persamaan \@ref(eq:pnme). Berdasarkan persamaan tersebut probabilitas yang peristiwa tersebut adalah sebagai berikut:

$$
P\left(ganjil\cup prima\right)=P\left(ganjil\right)+P\left(prima\right)-P\left(ganjil\cap prima\right)=\frac{3}{6}+\frac{4}{6}-\frac{3}{6}=\frac{3+4-3}{6}=\frac{2}{3}
$$

Peristiwa *not mutually exclusiev* dapat digambarkan menggunakan diagram venn yang ditunjukkan pada Gambar \@ref(fig:pnmevis)).

\begin{figure}

{\centering \includegraphics[width=0.8\linewidth]{pnmevis} 

}

\caption{Diagram venn peristiwa not mutually exclusive}(\#fig:pnmevis)
\end{figure}

Pada `R` peristiwa tersebut dapat dihitung menggunakan sintaks berikut:


```r
# kita akan menggunakan kembali objek S pada sintaks sebelumnya
# melakukan subset pada masing-masing peristiwa
ganjil <-subset(S, X1 %in% c(1, 3, 5))
prima <-subset(S, X1 %in% c(1, 2, 3, 5))

# menghitung irirsan kedua peristiwa
irisan <- intersect(ganjil, prima)

# menghitung probabilitas yang terbentuk
Prob(ganjil)+Prob(prima)-Prob(irisan)
```

```
## [1] 0.6667
```

**Contoh 2**

Misalkan seorang konsultan pengendalian kerugian diberikan data kerugian klien akibat kebakaran. Terdapat 250 kasus kebakaran dengan sejumlah penyebab. Penyebab utama disebabkan oleh membuang putung rokok sembarangan sebanyak 108 kasus, peralatan memasak sebanyak 95 kasus, pembakaran sebanyak 12 kasus, dan sumber kebakaran tidak diketahui sebanyak 35 kasus. Konsultan pengendalian kerugian ingin mengetahui berapa probabilitas untuk memilih klaim kebakaran dari kelompok dengan penyebab utama akibat aktivitas merokok sembarangan atau akibat pembakaran. Karena konsultan menentukan probabilitas "satu atau yang lain," ia akan menentukan probabilitas berdasarkan peristiwa majemuk. Konsultan kemudian harus menentukan apakah peristiwa tersebut *mutually exclusive* atau tidak. Untuk melakukannya ia harus menjawab pertanyaan "Dapatkan seseorang melakukan klaim bahwa peristiwa kebakaran dapat disebabkan oleh aktivitas merokok dan pembakaran yang dilakukan secara bersamaan?. Konsultan menentukan bahwa ini tidak mungkin Oleh karena itu, peristiwa-peristiwa tersebut *mutually exclusive* dan probabilitas dari kedua peristiwa yang terjadi pada saat yang sama adalah nol. Probabilitas selanjutnya dapat dihitung menggunakan Persamaan \@ref(eq:pnme).

$$
P\left(merokok\cup pembakaran\right)=P\left(merokor\right)+P\left(pembakaran\right)-P\left(merokok\cap pembakaran\right)
$$

$$
P\left(merokok\cup pembakaran\right)=\left(\frac{108}{250}\right)+\left(\frac{12}{250}\right)-0=0,48\ atau\ 48\%
$$

Persamaan \@ref(eq:pnme) dapat diperluas tidak hanya menggunakan dua buah peristiwa tapi dapat dihitung nilai probabilitasnya untuk lebih dari dua peristiwa. Pada Persamaan \@ref(eq:pnme2) disajikan persamaan untuk menghitung probabilitas untuk 3 buah peristiwa.

\begin{equation}
   P\left(A\cup B\cup C\right)=P\left(A\right)+P\left(B\right)+P\left(C\right)-P\left(A\cap B\right)-P\left(A\cup C\right)-P\left(B\cup C\right)+P\left(A\cup B\cup C\right)
  (\#eq:pnme2)
\end{equation}

Untuk peristiwa yang lebih banyak kita perlu menggambarkan terlebih dahulu diagram venn dari ruang sampel yang akan kita gunakan.

### Peristiwa *Dependent*

Peristiwa *dependent* terjadi bila probabilitas terjadinya satu peristiwa (peristiwa A) dipengaruhi oleh probabilitas terjadinya peristiwa lainnya (peristiwa B) atau $P\left(B\mid A\right)$. Peristiwa ini merupakan probabilitas kondisional karena terjadinya B dipengaruhi oleh terjadinya A. Pendekatan yang digunakan dituliskan pada Persamaan \@ref(eq:pd).

\begin{equation}
   P\left(A\mid B\right)=\frac{P\left(A\cap B\right)}{P\left(A\right)}\ \text{dimana P(A)>0}
  (\#eq:pd)
\end{equation}

**Contoh**

Bayangkan pembaca harus melakukan survey terkait studi AMDAL di suatu kota. Responden yang digunakan merupakan seseorang yang telah menyelesaikan kuliahnya atau telah memperoleh gelar sarjana. Kategorisasi terhadap populasi dilakukan berdasarkan jenis kelamin dan status pekerjaan dengan jumlah yang proporsional dengan jumlah populasinya yang dapat dilihat pada Tabel \@ref(tab:tabpd). Sampel diambil dari populasi tersebut sesuai dengan proporsi jenis kelamin dan status pekerjaan. Pada studi ini ingin diketahui manfaat dari pembangunan industri pendirian industri baru bagi kota tersebut.

**Jenis Kelamin**  | **Bekerja** | **Belum Bekerja** | **Total**
-------------------|-------------|-------------------|----------  
Laki-Laki          | 460         | 40                | 500
Perempuan          | 140         | 260               | 400
**Total**          | 600         | 300               | 900

: (\#tab:tabpd) Populasi orang yang telah menyelesaikan masa studinya di suatu kota.

Proses survey dilakukan dengan metode wawancara. Responden yang telah dilakukan wawancara selanjutnya tidak boleh diwawancarai lagi sehingga pada jumlah keseluruhan sampel terus berkurang. Hitunglah probabilitas kondisional dari pengambilan responden laki-laki akibat pengambilan responden seseorang yang telah bekerja?.

Berdasarkan contoh tersebut terdapat dua buah peristiwa yaitu peristiwa responden yang telah bekerja (dilambangkan dengan E) dan responden laki-laki (dilambangkan dengan M) atau dapat dituliskan sebagai berikut:

M : seorang laki-laki yang terpilih.
E : seseorang yang dipilih dan telah bekerja.

Probabilitas kondisional dari pengambilan responden laki-laki akibat pengambilan responden seseorang yang telah bekerja selanjutnya dihitung seperti berikut:

$$
P\left(M\mid E\right)=\frac{460}{600}=\frac{23}{30}
$$

Misalkan $n\left(A\right)$ merupakan notasi yang menyatakan jumlah elemen dari suatu set A. Dengan menggunakan notasi tersebut, dimana setiap orang dewasa yang telah menyelesaikan studinya memiliki kesempatan yang sama untuk dipilih sebagai responden dalam penelitian dapat dituliskan sebagai berikut:

$$
P\left(M\mid E\right)=\frac{n\left(E\cap M\right)}{n\left(E\right)}=\frac{\frac{n\left(E\cap M\right)}{n\left(S\right)}}{\frac{n\left(E\right)}{n\left(S\right)}}
$$

$$
P\left(M\mid E\right)=\frac{P\left(E\cap M\right)}{P\left(E\right)}
$$

Persamaan yang dihasilkan sesuai dengan Persamaan \@ref(eq:pd), dimana $P\left(E\cap M\right)$ dan $P\left(E\right)$ dihitung berdasarkan besarnya ruang sampel S. Untuk memverivikasi hasil yang telah diperoleh sebelumnya, kita dapat melakukan perhitungan seperti berikut:

$$
P\left(E\right)=\frac{600}{900}
$$
serta

$$
P\left(E\cap M\right)=\frac{460}{900}=\frac{23}{45}
$$

Sehingga

$$
P\left(E\ \mid M\right)=\frac{\frac{23}{45}}{\frac{2}{3}}=\frac{23}{30}
$$

Berdasarkan hasil yang diperoleh telah dapat dibuktikan bahwa probabilitas kondisional dari pengambilan responden laki-laki akibat pengambilan responden seseorang yang telah bekerja sebesar $\frac{23}{30}$. Probabilitas lainnya dapat pembaca hitung sendiri untuk lebih memperdalam pengetahuan pembaca mengenai probabilitas kondisional.

Pada `R` dengan menggunakan contoh soal sebelumnya kita dapat melakukan perhitungan probabilitas kondisional pengambilan sampel laki-laki akibat dari pengambilan sampel seseorang yang telah bekerja. Sintaks yang digunakan adalah sebagai berikut:


```r
# membuat data frame
S <- data.frame("jenis_kelamin"=c("laki-laki","perempuan"),"bekerja"=c(460,140), "belum_bekerja"=c(40,260))

# reshaping
library(tidyr)
S<-gather(S, key="status_pekerjaan",value="frekuensi",-jenis_kelamin)

# melakukan subset dan menghitung probabilitas
# peluang responden merupakan pegawai
E <- subset(S, status_pekerjaan=="bekerja")
P_E <- sum(E$frekuensi)/sum(S$frekuensi)
# peluang reponden laki-laki dan berkerja
E_M <- subset(S, status_pekerjaan=="bekerja"&jenis_kelamin=="laki-laki")
P_E_M <-sum(E_M$frekuensi)/sum(S$frekuensi)

# Probabilitas kondisional
P_E_M/P_E
```

```
## [1] 0.7667
```

### Peristiwa *Independent*

Untuk menentukan probabilitas dua atau lebih peristiwa akan terjadi bersamaan, perlu ditentukan terlebih dahulu apakaha peristiwa-peristiwa tersebut bersifat bebas. Misalnya dalam melempar 2 buah dadu, probabilitas munculnya angka 1 pada dadu pertama adalah $\frac{1}{6}$ dan probabilitas munculnya angka 2 pada dadu kedua juga sama dengan dadu pertama. Jika kita menginginkan kedua nilai tersebut muncul bersamaan pada saat pelemparan, maka probabilitas kejadiannya adalah hasil perkalian kedua probabilitas peristiwa pada masing-masing dadu yaitu $\frac{1}{6}\cdot\frac{1}{6}=\frac{1}{36}$. Pendekatan perhitungan probabilitas untuk peristiwa *independent* dapat dituliskan pada Persamaan \@ref(eq:pi).

\begin{equation}
   P\left(A\cap B\right)=P\left(A\right)\cdot P\left(B\right)
  (\#eq:pi)
\end{equation}

**Contoh**

Dengan menggunakan contoh soal sebelumnya, kita akan menentukan probabilitas responden penelitian kita adalah laki-laki (L) dan bekerja (E). Berdasarkan Persamaan \@ref(eq:pi), probabilitas terpilihnya jenis responden tersebut adalah sebagai berikut:

$$
P\left(L\cap E\right)=\frac{500}{900}\cdot\frac{300}{900}=\frac{5}{27}
$$

Dengan menggunakan `R` sintaks yang digunakan adalah sebagai berikut:


```r
# subset responden laki-laki
L <- subset(S, jenis_kelamin=="laki-laki")
E <- subset(S, status_pekerjaan=="bekerja")

# probabilitas
P_L <- sum(L$frekuensi)/sum(S$frekuensi)
P_E <- sum(E$frekuensi)/sum(S$frekuensi)

# Probabilitas peristiwa independen
P_L*P_E
```

```
## [1] 0.3704
```

## Teori Bayes

Teori Bayes memberikan formula probabilitas suatu peristiwa yang tergantung pada kontribusi dan ragam pada tahap sebelumnya. Formula tersebut dapat dituliskan pada Persamaan \@ref(eq:tb).

\begin{equation}
   P\left(B_k\mid A\right)=\frac{P\left(B_k\right)\cdot P\left(A\mid B_k\right)}{\sum_{i=1}^nP\left(B_i\right)\cdot P\left(A\mid B_i\right)}\ \text{dimana k=1,2,...,n}
  (\#eq:tb)
\end{equation}

Untuk membuktikan persamaan tersebut, kita akan menggunakan Persamaan \@ref(eq:pd) dengan melihat $P\left(B_k\cap A\right)$ dengan dua cara yang berbeda. Untuk lebih mudahnya, misalkan nilai $P\left(B_k\right)>0$ untuk seluruh $k$, sehingga:

\begin{equation}
   P\left(A\right)\cdot P\left(B_k\mid A\right)=P\left(B_k\cap A\right)=P\left(B_k\right)\cdot P\left(A\mid B_k\right)
  (\#eq:tb2)
\end{equation}

sejak nilai $P\left(A\right)>0$ kita dapat membaginya untuk mendapatkan

\begin{equation}
   P\left(B_k\mid A\right)=\frac{P\left(B_k\right)\cdot P\left(A\mid B_k\right)}{P\left(A\right)}
  (\#eq:tb3)
\end{equation}

Sekarang ingat kembaili bahwa $\left\{B_k\right\}$ adalah partisi, teorema probabilitas total probabilitas total memberikan penyebut pada persamaan terkahir menjadi

\begin{equation}
   P\left(A\right)=\sum_{k=1}^nP\left(B_k\cap A\right)=\sum_{k=1}^nP\left(B_k\right)\cdot P\left(A\mid B_k\right)
  (\#eq:tb4)
\end{equation}

Apa artinya? Biasanya dalam aplikasinya kita diberikan (atau tahu) probabilitas apriori $P\left(B_k\right)$. Kita keluar dan mengumpulkan sejumlah data yang kita gunakan untuk mewakili peristiwa A. Kita ingin tahu: bagaimana kita dapat memperbaharui $P\left(B_k\mid A\right)$ menjadi $P\left(B_k\mid A\right)$? Jawabannya adalah dengan teori Bayes.

**Contoh**

Sebuah instalasi air menggunakan tawas sebagai koagulannya. Tawas ini disuplai dari 4 perusahaan pemasok bahan kimia. Spesifikasi yang diinginkan adalah paling tidak tawas tersebut mengandung kadar efektif 60%. Data tentang perusaan pemasok dan kegagalan untuk memenuhi standar yang diinginkan adalah:

- Perusahaan 1: memasok 20% dengan kegagalan 1 dalam 20 atau kegagalan = 0,05,
- Perusahaan 2: memasok 60% dengan kegagalan 1 dalam 10 atau kegagalan = 0,10,
- Perusahaan 3: memasok 15% dengan kegagalan 1 dalam 10 atau kegagalan = 0,10,
- Perusahaan 4: memasok 5% dengan kegagalan 1 dalam 20 atau kegagalan = 0,05.

Bila dari stok tawas digudang tersebut direksi ingin mengetahui berapa kemungkinan terjadinya kegagalan pada stok tawas dari perusaan 1, dengan menggunakan teori Bayes kita dapat menghitungnya seperti berikut:

$$
P\left(B_i\mid A\right)=\frac{0,20\cdot0,05}{\left(0,6\cdot0,1+0,15\cdot0,1+0,05\cdot0,05\right)}=0,114
$$

## Ekspektasi Matematis

Misalkan Menteri Kesehatan Republik Indonesia merilis hasil studi yang menyatakan usia harapan hidup masyarakat Indonesia adalah 70 tahun. Ini tidak berarti saat kita berusia 65 tahun kita akan meninggal 5 tahun berikutnya. Pengertian usia harapan hidup ini didasarkan pada probabilitas yaitu ekspektasi matematis yang dituliskan pada Persamaan \@ref(eq:em).

\begin{equation}
   E\left(X\right)=\sum_{i=1}^nx_i\cdot P\left(X_i\right)
  (\#eq:em)
\end{equation}

Misalkan terdapat eksperimen yang menghasilkan i buah peristiwa, dan masing-masing mempunyai probabilitas terjadi: p1,p2,p3,..,pi. 

sehingga: p1+p2+p3+...+pk=1
maka ekspektasinya adalah $E=p1\cdot x1+p2\cdot x2+p3\cdot x3+...+pi\cdot xi$. Hasil perjumlahan tersebut akan menghasilkan Persamaan \@ref(eq:em).

**Contoh**

Misalkan sebuah konsultan sedang menyiapkan proposal untuk sebuah proyek. Biaya untuk menyiapkan proposal adalah 5 juta rupiah, sedang keuntunga kotor bila proyek ini diperoleh adalah:

- 50 juta rupiah dengan probabilitas 0,20
- 30 juta rupiah dengan probabilitas 0,50
- 10 juta rupiah dengan probabilitas 0,20
- 0 rupiah dengan probabilitas 0,10.

Bila kemungkinan mendapatkan proyek tersebut adalah 0,30, maka keuntungan yang diharapkan adalah:

- Probabilitas memperoleh keuntungan 45 juta rupiah (keuntungan kotor-modal)=probabilitas mendapatkan proyek x keuntungan proyek tersebut=0,30 x 0,20 = 0,06
- Probabilitas memperoleh keuntungan 25 juta = 0,30 x 0,50 = 0,15
- Probabilitas memperoleh keuntungan 5 juta = 0,30 x 0,20 = 0,06
- Probabilitas memperoleh kerugian 5 juta = (0,30 x 0,10)+0,70 = 0,73

Maka ekspektasinya = (45 juta x 0,06)+(5 juta x 0,15)+(5 juta x 0,06)-(5 juta x 0,73)=3,1 juta. Dengan demikian perusahaan tersebut dapat memutuskan apakah akan meneruskan membuat proposal tersebut, dengan kemungkinan merugi sebesar 5 juta rupiah (biaya membuat proposal) dan kemungkinan untung 3 juta rupiah.

## Referensi

1. Damanhuri, E. 2011. **Statitika Lingkunga**. Penerbit ITB.
2. Kerns, G.Jay. 2018. **Introduction to Probability and Statistics Using R Third Edition**. GNU Free Documentation License.
3. Janicak, C.A. 2007. **Applied Statistics in Occupational Safety and Health**. Government Institutes.
4. Walpole, E. R., Myers, H.M., Myers, S.L., Keying Ye. 2011. **Probability $ Statistics for Engineering & Scientists Ninth Edition**. Prentice Hall.








<!--chapter:end:08-probabilitas.Rmd-->

<style>
body{
text-align: justify}
</style>

# Distribusi Probabilitas

Distribusi probabilitas merupakan sebuah fungsi yang menggambarkan kemungkinan memperoleh sejumlah nilai dalam suatu variabel acak. Dengan kata lain distribusi probabilitas menjelaskan bahwa nilai yang muncul pada sampel acak akan bervariasi berdasarkan distribusi probabilitas yang menyertainya.

Untuk memahaminya misalkan kita melakukan suatu sampling dengan cara survey terhadap sejumlah responden untuk mengetahui produksi sampah hariannya. Keseluruhan nilai timbulan yang diperoleh selajutnya disebut sebagai distribusi timbulan sampah. Distribusi tersebut berguna saat kita mengetahui hasil mana yang paling mungkin, sebaran nilai potensial serta kemungkinan hasil yang berbeda.

## Properti Umum dari Distribusi Probabilitas

Distribusi probabilitas menjelaskan kemungkinan suatu peristiwa atau nilai muncul. Ahli statistika menjelaskan distribusi probabilitas kedalam Persamaan \@ref(eq:pudbp).

\begin{equation}
   P\left(x\right)=kemungkinan\ suatu\ variabel\ acak\ mengandung\ nilai\ x
  (\#eq:pudbp)
\end{equation}

Jumlah seluruh probabilitas adalah 1. Selain itu retang nilai probabilitas berkisar antara 0 sampai 1, dimana hal ini telah penulis jelaskan pada Chapter sebelumnya.

Distribusi probabilitas menjelaskan sebaran nilai variabel acak. Akibatnya, jenis variabel menentukan jenis distribusi probabilitas. Untuk variabel acak tunggal, ahli statistik membagi distribusi menjadi dua jenis berikut:

- **Distribusi probabilitas yang diskrit**

Fungsi probabilitas diskrit dikenal sebagai fungsi massa probabilitas, dimana kita dapat mengasumsikan sejumlah nilai diskrit. Misalnya pelemparan dadu serta perhitungan sebuah peristiwa seperti flu di suatu daerah merupakan fungsi tersendiri. Kedua contoh tersebut merupakah contoh peristiwa diskrit karena tidak ada nilai antara, misalnya pada dadu tidak ada nilai antara 1 dan 2, dan seterunya. Pada perhitungan jumlah peristiwa flu juga tidak ada nilai antara orang terserang dlu dan tidak. Contoh lainnya adalah perhitungan jumlah buku diperpustakaan yang diperiksa tiap jam. Kita dapat menghitung jumlah buku perjam seperti 21 buku atau 22 buku, tetapi kita tidak dapat menghitung jumlah buku pada nilai antara kedua nilai tersebut. Distribusi probabilitas diskrit terdiri atas:

  a. Binomial
  b. Hypergeometric
  c. Poisson
  d. Geometric
  e. Multinomial
  
- **Distribusi probabilitas yang bersifat kontinu**

Fungsi probabilitas kontinu dikenal juga sebagai fungsi densitas probabilitas. Suatu distribusi dikatakan sebagai distribusi kontinu jika nilai yang terkandung dalam distribusi tersebut tidak terbatas serta skala yang digunakan dapat pula mengandung nilai desimal. Contoh suatu pengukuran yang menghasilkan distribusi kontinu adalah tinggi, berat, suhu, dll. Distribusi probabilitas kontinu terdiri atas:

  a. Normal
  b. Binomial
  c. Uniform
  d. Loh Normal
  e. Gamma, dll.

## Distribusi Binomial dan Multinomial

Suatu percobaan sering dilakukan dengan proses yang berulang-ulang. Tiap proses percobaan yang dilakukan akan menghasilkan dua luaran yaitu **sukses** atau **gagal**. Untuk memahaminya misalkan pembaca melakukan pelemparan sebuah koin. Jika yang keluar adalah bagian kepala (*head*) maka proses tersebut dikatakan sukses, jika sebaliknya maka gagal. Proses penentuan sukses dan gagal tersebut tergantung pada sudut pandang kita melihatnya. Proses percobaan demikian disebut sebagai **Bernoulli process** (proses bernouli). Setiap percobaan yang dilakukan disebut sebagai **Bernoulli trial**. 

**Bernoulli process** memiliki ciri-ciri sebagai berikut:

- Eksperimen terdiri atas sejumlah perulangan percobaan.
- Setiap perulangan percobaan menghasilkan luaran yang diklasifikasikan sebagai **sukses** atau **gagal**.
- Probabilitas sukses (dinotasikan $p$) konstan dari setiap perulangan.
- Setiap perulangan percobaan bersifat independen.

**Contoh**

Misalkan kita akan melakukan percobaan pelemparan dadu sebanyak 3 kali. Probabilitas munculnya bagian angka 1 pada dadu adalah $\frac{1}{6}$. Probabilitas ini konstan pada setiap perulangan. Jika kita menginginkan ketiga perulangan tersebut menghasilkan angka 1. Probabilitasnya merupakan hasil kali probabilitas pada tiap giliran pelemparan seperti berikut:

$$
P\left(111\right)=\frac{1}{6}\cdot\frac{1}{6}\cdot\frac{1}{6}=\frac{1}{216}
$$

### Distribusi Binomial

Jumlah $X$ keberhasilan atau jumlah percobaan sukses dalam percobaan Bernoulli disebut **variabel acak binomial**. Distribusi probabilitas dari variabel acak diskrit ini disebut distribusi binomial, dan nilainya akan dinotasikan dengan $b\left(x;n,p\right)$ karena mereka bergantung pada jumlah percobaan dan probabilitas keberhasilan pada percobaan yang diberikan. 

**Bernouli trial** dapat menghasilkan percobaan yang sukses dengan probabilitas $p$ dan percobaan gagal dengan probabilitas $q=1-p$. Sehingga distribusi probabilitas binomial percobaan sukses untuk variabel acak $X$ dengan jumlah $n$ percobaan yang independen dinyatakan kedalam Persamaan \@ref(eq:dbinom).

\begin{equation}
   b\left(x;n,p\right)=\left(nC_x\right)p^xq^{n-x},\ x=0,1,2,...,n.
  (\#eq:dbinom)
\end{equation}

dimana

\begin{equation}
   nC_x=\frac{n!}{x!\left(n-x\right)!}
  (\#eq:dbinom2)
\end{equation}

**Contoh**

Dengan menggunakan contoh sebelumnya kita dapat menghitung probabilitas keluarnya angka 1 pada dadu untuk 3 kali percobaan ($n$) atau seluruh percobaan menghasilkan angka 1 ($n=x=3$) adalah:

$$
b\left(3;3,\frac{1}{6}\right)=\left(\frac{3!}{3!\left(3-3\right)!}\right)\left(\frac{1}{6}\right)^3\left(\frac{5}{6}\right)^{\left(3-3\right)}
$$
$$
b\left(3;3,\frac{1}{6}\right)=\left(1\right)\cdot\left(\frac{1}{6}\right)^3\cdot\left(1\right)=\frac{1}{216}
$$
  
Kita juga dapat melakukan perhitungan tersebut menggunakan `R` untuk mengetahui probabilitas munculnya angka 1 pada dadu untuk 3 kali percobaan. Sintak yang digunakan adalah sebagai berikut:


```r
dbinom(x=3, # jumlah kejadian sukses 
       size=3, # jumlah percobaan
       prob=1/6) # probabilitas kejadian
```

```
## [1] 0.00463
```

**Probabilitas Kumulatif Binomial**

Pada kondisi lain kita tidak hanya tertarik dengan probabilitas munculnya suatu peristiwa. Kita terkadang tertarik untuk menghitung probabilitas kumulatif dari suatu peristiwa. Misalnya probabilitas munculnya nomor dadu $<4$ atau pada perhitungan kendaraan per jam yang melalui suatu jalan kita tertarik menghitung peluang kendaraan yang melintas tiap jam $<50$ kendaraan. Untuk menghitung probabilitas yang demikian kita perlu melakukan akumulasi probabilitas yang memenuhi kriteria yang telah kita tentukan sebelumnya. Probabilitas kumulatif distribusi binomial berdasarkan kondisi tertentu dinyatakan pada Persamaan \@ref(eq:dbinom3).

\begin{equation}
   B\left(r,n,p\right)=\sum_{x=0}^rb\left(x;n,p\right)
  (\#eq:dbinom3)
\end{equation} 

dimana $r$ adalah kondisi probabilitas yang kita inginkan yang dapat dituliskan sebagai $P\left(X<r\right)$ atau $P\left(X>r\right)$. Kondisi lain yang dapat kita gunakan adalah $P\left(a\le X\le b\right)$.

**Contoh**

Misalkan kita diminta untuk melakukan analisis kerusakan *diffused aerator* pada suatu instalasi air limbah. Jumlah aerator total pada instalasi tersebut adalah 10 buah. Probabilitas sebuah aerator rusak sebesar $\frac{1}{10}$. Tentukan berapa probabilitas jika (a) setidaknya 3 aerator tersebut tidak rusak? (b) 4 sampai 5 buah aerator rusak? serta (c) sebanyak 5 aerator rusak?.

(a) jika setidaknya 3 aerator tidak rusak

$$
P\left(X\le 3\right)=\sum _{x=0}^3b\left(x;10,0.1\right)
$$

$$
P\left(X\le3\right)=b\left(0;10,0.1\right)+b\left(1;10,0.1\right)+b\left(2;10,0.1\right)+b\left(3;10,0.1\right)
$$

$$
P\left(X\le3\right)=0,987
$$

Kita juga dapat memperoleh nilai tersebut dengan melihat tabel statistika yang dapat pembaca lihat pada tautan [berikut](https://onlinepubs.trb.org/onlinepubs/nchrp/cd-22/manual/v2appendixc.pdf)

(b) jika 4 sampai 5 aerator rusak

$$
P\left(4\le X\le5\right)=\sum_{x=4}^5b\left(x;10,0.1\right)=\sum_{x=0}^5b\left(x;10,0.1\right)-\sum_{x=0}^3\left(x;10,0.1\right)
$$

$$
P\left(4\le X\le5\right)=1-0,987=0,013
$$

(c) jika tepat 5 aerator rusak

$$
P\left(X=5\right)=b\left(5;10,0.1\right)=\sum_{x=0}^5b\left(x;10,0.1\right)-\sum_{x=0}^4b\left(x;10,0.1\right)
$$

$$
P\left(X=5\right)=1-0,998=0,002
$$

Untuk melakukan perhitungannya pada `R` kita dapat menggunakan fungsi `pbinom()`. Fungsi tersebut akan menghitung probabilitas bedasarkan nilai kondisi yang telah kita masukkan. Berikut adalah sintaks yang digunakan:


```r
# a) jika setidaknya 3 aerator tidak rusak
pbinom(q=3,  
       size=10, # jumlah percobaan
       prob=0.1) # probabilitas sukses
```

```
## [1] 0.9872
```

```r
# b) jika setidaknya 4 sampai 5 aerator rusak
pbinom(q=5,size=10,prob=0.1)-pbinom(q=3,size=10,prob=0.1) 
```

```
## [1] 0.01265
```

```r
# c) jika tepat 5 aerator rusak
dbinom(x=5, # jumlah kejadian sukses
       size=10, # jumlah percobaan
       prob=0.1) # probabilitas sukses
```

```
## [1] 0.001488
```

**Menghitung Nilai Rata-Rata dan Varians Distribusi Binomial**

Kita sudah mengetahui bahwa distribusi probabilitas binomial hanya bergantung pada nilai $n$, $p$, dan $q$. Berdasarkan tersebut nilai mean, dan varians dari distribusi probabilitasnya juga bergantung pada ketiga nilai tersebut. Nilai mean dituliskan pada Persamaan \@ref(eq:dbinom4), sedangkan varians dari distribusi probababilitas distuliskan pada Persamaan \@ref(eq:dbinom5).

\begin{equation}
   \mu=np
  (\#eq:dbinom4)
\end{equation}

\begin{equation}
   \sigma^2=npq
  (\#eq:dbinom5)
\end{equation}

### Multinomial Eksperimen dan Distribusi Multinomial

Eksperimen Binomial (*Binomial process*) dapat menjadi **eksperimen multinomial** jika kita menginginkan luaran dari percobaan yang dilakukan memiliki lebih dari satu hasil. Contoh dari eksperimen multinomial ini misalnya adalah penarikan kartu dari seperangkan kartu. Kita dapat mengaggap penarikan kartu dengan pengembalian sebagai eksperimen multinomial jika luaran yang diinginkan adalah 4 jenis kartu dalam set kartu tersebut.

Secara umum, jika percobaan yang diberikan dapat menghasilkan salah satu $k$ dari hasil yang mungkin $E_1,E_2,...,E_k$ dengan probabilitas yang dihasilkan sebesar $p_1,p_2,...,p_k$, maka **distribusi multinomial** akan memberikan nilai probabilitas yang dinyatakan $E_1$ terjadi sebanyak $x_1$ kali, $E_2$ terjadi sebanyak $x_2$ kali, sampai dengan $E_k$ terjadi sebanyak $x_k$ kali dalam $n$ percobaan yang independent, dimana

$$
x_1+x_2+...+x_k=n
$$

Selanjutnya fungsi probabilitas dituliskan sebagai berikut:

$$
f\left(x_1,x_2,...,x_k;\ p_1,p_2,...,p_k\right)
$$

Seperti yang telah kita ketahui bersama bahwa nilai $p_1+p_2+...+p_k=1$. Sejak percobaan yang dilakukan independen, maka setiap percobaan yang menghasilkan $x_1$ yang merupakan luaran dari $E_1$, $x_2$ yang merupakan luaran dari $E_2$ sampai dengan $x_k$ yang merupakan luaran dari $E_k$ akan terjadi dengan probabilitas $p^{x_1}p^{x_2}...p^{x_k}$.  Jumlah urutan yang menghasilkan hasil yang serupa untuk percobaan $n$ adalah sama dengan jumlah partisi $n$ item ke dalam $k$ grup dengan $x_1$ di grup pertama, $x_2$ di grup kedua, sampai dengan $x_k$ di grup $k$. Kondisi ini dapat dituliskan seperti berikut:

$$
\binom{n}{x_1,x_2,...,x_k}=\frac{n!}{x_1!x_2!...x_k!}
$$

Sejak seluruh partisi bersifat *mutually exlusive* dan terjadi dengan probabilitas yang setara, kita dapat memperoleh distribusi multinomial dengan mengalikan probabilitas tiap luaran spesifik dengan jumlah total partisinya. Persamaan distribusi multinomial yang diperoleh dituliskan kedalam Persamaan \@ref(eq:dmultinom).

\begin{equation}
   f\left(x_1,x_2,...,x_k;\ p_1,p_2,...,p_k\right)=\binom{n}{x_1,x_2,...,x_k}p^{x_1}p^{x_2}...p^{x_k}
  (\#eq:dmultinom)
\end{equation}

dimana 

\begin{equation}
   \sum_{i=1}^kx_i=n\ dan\ \sum_{i=1}^kp_i=1
  (\#eq:dmultinom2)
\end{equation}

**Contoh**

Probabilitas sejenis pompa memiliki umur ekonomis 2 tahun sebesar 0,30, antara 2-4 tahun adalah 0,50, dan 4-5 tahun adalah 0,20. Hitunglah probabilitas 8 buah pompa dimana pompa dengan umur ekonomis 2 tahun sebanyak 2 buah, 2-4 tahun sebanyak 5 buah, dan antara 4-5 sebanyak 1 buah.

Untuk menyelesaikannya kita perlu mendata jumlah kemunculan disertai dengan probabilitas kejadia pada tiap grup seperti berikut:

$$
n=8;\ x_1=2\ dengan\ p_1=0,30;\ x_2=5\ dengan\ p_2=0,50,\ dan\ x_3=1\ dengan\ p_1=0,20\ 
$$

dengan menggunakan Persamaan \@ref(eq:dmultinom), maka probabilitasnya dapat dihitung seperti berikut:

$$
f\left(2,5,1;0.30,0.50,0.20\right)=\binom{8}{2,5,1}\left(0,3\right)^2\left(0,5\right)^5\left(0,2\right)^1
$$

$$
f\left(2,5,1;0.30,0.50,0.20\right)=0,0945
$$

Pada `R` kita dapat menggunakan fungsi `dmultinom()` untuk menghitung probabilitas distribusi multinomial. Komponen dari fungsi tersebut adalah sebagai berikut:


```r
dmultinom(x, size, prob)
```

> **Note: **
>
> - **x**: vektor numerik
> - **size**: jumlah percobaan atau perulangan
> - **prob**: vektor numerik probabilitas tiap grup hasil.

Berikut adalah sintaks untuk menghitung probabilitas multinomial pada contoh kasus di atas:


```r
dmultinom(c(2,5,1), # jumlah kejadian tiap grup 
          size=8, # jumlah percobaan
          prob=c(0.3,0.5,0.2)) # probabilitas masing-masing luaran
```

```
## [1] 0.0945
```

## Distribusi Hipergeometris

Distribusi hipergeometris didasarkan pada eksperimen hipergeometris yang memiliki asumsi sebagai berikut:

1. Sampel dengan ukuran $n$ diambil secara acak tanpa pengembalian (*sampel without replacement*) dari populasi berukuran $N$.
2. Pada populasi, $k$ didefinisikan sebagai observasi yang **sukses**, sedangkan $N-k$ didefiniskan sebagai observasi yang **gagal**.

Melalui asusmsi tersebut, kita dapat menemukan perbedaan antara distribusi hipergeometris dengan distribusi binomial. Perbedaan yang paling mendasar adalah metode sampling yang digunakan, dimana distribusi binomial mengasumsikan sampel dengan pengembalian (*sample with replacement*), sedangkan distribusi hipergeometris mengasumsikan sebaliknya.

Distribusi probabilitas hipergeometris untuk variabel acak $X$ dengan jumlah sampel $n$ dari populasi terpilih dengan ukuran populasi $N$, dimana $k$ merupakan observasi **sukses** dan $N-k$ merupakan observasi yang gagal dapat dituliskan berdasarkan Persamaan \@ref(eq:dhiper).

\begin{equation}
   h\left(x;N,n,k\right)=\frac{\binom{k}{x}\binom{N-k}{n-x}}{\binom{N}{n}},\ \max\left\{0,n-\left(N-k\right)\right\}\le x\le\min\left\{n,k\right\}
  (\#eq:dhiper)
\end{equation}

Range dari $x$ dapat ditentukan dari 3 koefisien binomial, dimana $x$ dan $n-x$ tidak lagi lebih besar dari $k$ dan $N-k$ dan nilai keduanya tidak boleh lebih kecil dari 0. Biasanya ketika kedua nilai $k$ dan $N-k$ lebih besar dari ukuran sampel $n$, range dari variabel acak hipergeometris akan menjadi $x=0,1,...,n$.

**Contoh**

Misalkan pembaca ditugaskan untuk melakukan sortir terhadap 40 sak kompos yang akan dijual dengan berat rata-rata 2 kg. Pembaca diberi tahu bahwa 3 dari seluruh kompos tersebut memiliki berat kurang dari 2 kg sehingga tidak dapat dijual. Tugas pembaca adalah menemukan ketiga sak kompos tersebut. Untuk mempermudah proses tersebut pembaca melakukan sampling secara acak dengan jumlah sampling 5 buah kompos tanpa pengembalian. Hitunglah berapa peluang pada tiap sampling tersebut pembaca menemukan 1 kompos yang memiliki berat lebih kecil dari 2 kg tersebut?.

Berdasarkan studi kasus tersebut kita dapat menyimpulkan bahwa proses sampling yang dilakukan adalah dengan menggunakan prosedur sampling tanpa pengembalian, sehingga distribusi hipergeometris dapat diterapkan dengan nilai $n=5$, $N=40$, $k=3$, dan $x=1$. Dengan menggunakan Persamaan \@ref(eq:dhiper), peluang ditemukan 1 sak kompos yang tidak sesuai adalah sebagai berikut:

$$
h\left(1;40,5,3\right)=\frac{\binom{3}{1}\binom{40-3}{5-1}}{\binom{40}{5}}=0,3011
$$

Berdasarkan hasil perhitungan diketahui bahwa peluang untuk menemukan 1 sak kompos dari 3 sak kompos yang tidak sesuai sebesar 30% pada tiap kali sampling.

Pada `R` distribusi probabilitas hipergeometris dapat dihitung menggunakan fungsi `dhyper()`. Format yang digunakan pada fungsi tersebut adalah sebagai berikut:


```r
dhyper(x, m, n, k)
```

> **Note: **
>
> - **x**: vektor numerik yang menyatakan observasi sukses pada tiap sampling
> - **m**: jumlah observasi sukses
> - **n**: jumlah observasi gagal
> - **k**: ukuran sampel

Berikut adalah sintaks untuk menghitung probabilitas hipergeometris contoh kasus di atas:


```r
dhyper(x=1, # observasi sukses tiap sampling
       m=3, # observasi sukses (k)
       n=37, # observasi gagal (N-k)
       k=5) # sampel
```

```
## [1] 0.3011
```

**Probabilitas Kumulatif Hipergeometris**

Pada contoh kasus sebelumnya, sak kompos yang tidak memenuhi kriteria bisa saja saat sampling tidak hanya ditemukan 1 sak yang tidak memenuhi, bisa dua , tiga atau sama sekali tidak ada yang ditemukan sak yang tidak memenuhi kriteria. Kondisi tersebut mengharuskan kita menghitung probabilitas kumulatif dari suatu kondisi seperti $P\left(X<r\right),\ P\left(X>r\right),\ atau\ P\left(a<X<b\right)$ yang dapat dituliskan pada Persamaan \@ref(eq:dhiper2).

\begin{equation}
   H\left(r;N,n,k\right)=\sum_{x=0}^rh\left(x;N,n,k\right)
  (\#eq:dhiper2)
\end{equation}

Pada contoh sebelumnya, hitunglah probabilitas jika paling banyak 2 sak kompos yang tidak memenuhi kriteria ditemukan pada sampel?.

Untuk melakukannya kita perlu menghitung probabilitas hipergeometris untuk kondisi saat $x=0,1,2$. Dengan menggunakan Persamaan \@ref(eq:dhiper2), nilai probabilitas yang dihasilkan adalah sebagai berikut:

$$
P\left(X\le2\right)=b\left(0;40,5,3\right)+b\left(1;40,5,3\right)+b\left(2;40,5,3\right)=0,999
$$

Pada `R` probabilitas kumulatif dapat dihitung menggunakan fungsi `phyper()`. Format fungsi yang digunakan adalah sebagai berikut:


```r
phyper(q, m, n, k, lower.tail=TRUE)
```

> **Note: **
>
> - **q**: vektor numerik yang menyatakan observasi maksimum yang sukses saat sampling
> - **m**: jumlah observasi sukses
> - **n**: jumlah observasi gagal
> - **k**: ukuran sampel
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE

Dengan menggunakan sintaks tersebut, probabilitas kumulatif dapat dihitung sebagai berikut:


```r
phyper(q=2, # probabilitas <=2
       m=3, # observasi sukses
       n=37, # jumlah gagal
       k=5) # jumlah sampel
```

```
## [1] 0.999
```

```r
# atau
dhyper(0,3,37,5)+dhyper(1,3,37,5)+dhyper(2,3,37,5)
```

```
## [1] 0.999
```

**Menghitung Nilai Rata-Rata dan Varians Distribusi Hipergeometris**

Nilai rata-rata dan varians distribusi hipergeometris dituliskan kedalam Persamaan \@ref(eq:dhiper3):

\begin{equation}
   \mu=\frac{nk}{N}\ dan\ \sigma^2=\frac{N-n}{N-1}\cdot n\cdot\frac{k}{N}\left(1-\frac{k}{N}\right)
  (\#eq:dhiper3)
\end{equation}

Bila nilai $n<<<N$, maka pendekatan distribusi binomial dapat dilakukan dengan pendekatan $n$ dan $p=\frac{k}{N}$. Pendekatan yang dilakukan akan cukup baik bila $n\le0,1N$.

## Distribusi Binomial Negatif dan Distribusi Geometris

Mari kita bayangkan percobaan di mana sifat-sifatnya (propertinya) sama dengan percobaan binomial, dengan pengecualian bahwa uji coba akan diulangi sampai sejumlah keberhasilan terjadi. Oleh karena itu, alih-alih probabilitas $x$ keberhasilan dalam $n$ percobaan, di mana $n$ tetap, kita sekarang tertarik pada probabilitas bahwa keberhasilan $k$ terjadi pada percobaan ke-$x$. Eksperimen semacam ini disebut eksperimen **binomial negatif**.

Sifat-sifat dari percobaan binomial negatif adalah sebagai berikut:

1. Percobaan terdiri atas sejumlah $x$ perulangan.
2. Setiap percobaan memiliki dua hasil (**sukses** dan **gagal**).
3. Probabilitas sukses dinotasikan dengan $p$ yang sama pada setiap percobaan.
4. Setiap percobaan bersifat independen yang berarti hasil dari sebuah percobaan tidak akan mempengaruhi hasil percobaan lainnya.
5. Percobaan dilakukan secara terus-menerus sampai dengan sejumlah $k$ sukses terjadi, dimana $k$ ditentukan terlebih dahulu.

**Contoh**

Misalkan kita menguji sebuah obat dengan memberikannya kepada pasien yang sakit. Keberhasilan obat tersebut Obat dinyatakan sukses jika secara efektif memberikan efek pemulihan bagi pasien. Probabilitas obat tersebut melakukannya berdasarkan hasil studi yang telah dilakukan sebesar 60%. Kita tertarik untuk mengetahui probabilitas pasien kelima yang mengalami efek penyembuhan dimana pasien ini merupakan pasien ketujuh yang diberikan obat tersebut. Untuk melakukannya kita definisikan kejadian sukses dengan simbol $S$ dan gagal dengan simbol $F$, urutan yang mungkin dari ketujuh pasien berdasarkan respon terhadap obat adalah $SFSSSFS$ yang probabilitas kejadian berdasarkan urutan tersebut adalah sebagai berikut:

$$
\left(0,6\right)\left(0,4\right)\left(0,6\right)\left(0,6\right)\left(0,6\right)\left(0,4\right)\left(0,6\right)=\left(0,6\right)^5\left(0,4\right)^2
$$

Kita dapat mendaftar sejumlah luaran yang mungkin pada kejadian tersebut mengatur ulang $F$ dan $S$ kecuali untuk hasil terakhir, yang harus menjadi keberhasilan kelima. Jumlah total luaran yang mungkin sama dengan jumlah partisi dari enam (7-1) percobaan pertama menjadi dua kelompok dengan 2 buah gagal dan 4 buah sukses menjadi kelompok tersendiri. Hal ini dapat dilakukan berdasarkan $\binom{6}{4}=15$ cara yang *mutually exclusive*. Oleh karena itu, jika $X$ mewakili hasil dimana keberhasilan kelima terjadi, maka

$$
P\left(X=7\right)=\binom{6}{4}\left(0.6\right)^2\left(0,4\right)^2=0,1866
$$

### Distribusi Binomial Negatif

Berdasarkan contoh kasus tersebut, kita dapat mendefinisikan formula untuk distribusi probabilitas binomial negatif. Jika percobaan yang bersifat independen dan berulang dapat menghasilkan keberhasilan (kejadian sukses) dengan probabilitas $p$ dan kegagalan dengan probabilitas $q=1-p$, maka distribusi probabilitas variabel acak $X$, jumlah percobaan di mana keberhasilan k terjadi dinyatakan pada Persamaan \@ref(eq:dnegbinom):

\begin{equation}
   b^{\ast}\left(x;k,p\right)=\binom{x-1}{k-1}p^kq^{x-k},\ \ \ \ \ x=k,k+1,k+2,....
  (\#eq:dnegbinom)
\end{equation}

**Contoh**

Misalkan pada suatu kejuaraan NBA (Championship series) atau final antar juara wilayah, dimana pada pertandingan puncak kedua tim dari dua wilayah akan melakukan 7 pertandingan terkahir. Suatu tim dinyatakan juara jika berhasil meraih 4 kemenangan dari 7 pertandingan yang ada. Anggaplah tim A dan B berhadapan satu sama lain. Probabilitas A memenangkan suatu pertandingan terhadap tim B sebesar 0,55, tentukan:

- Berapakah probabilitas tim A memenangkan kejuaraan pada pertandingan ke-6 dari 7 pertandingan yang ada?
- Berapakah probabilitas A memenangkan kejuaraan?

Dengan menggunakan Persamaan \@ref(eq:dnegbinom), probabilitas kemenangan tim A terhadap tim B dapat dihitung sebagai berikut:

- **Tim A juara pada pertandingan ke-6 ($x=6$, $k=4$, dan $p=0,55$)**

$$
b^{\ast}\left(6;4,0.55\right)=\binom{6-1}{4-1}0,55^4\left(1-0,55\right)^{6-4}=0,1853
$$

- **Tim A menjuarai kejuaraan**

Tim A dapat menjuarai kejuaraan jika telah memenangkan 4 dari 7 pertandingan. Kemungkinan Tim A dapat memenangkan pertandingan tersebut dapat terjadi pada pertandingan ke-4 (menang berturut-turut), pertandingan ke-6, dan pertandingan ke-7.

$$
b^{\ast}\left(4;4,0.55\right)+b^{\ast}\left(5;4,0.55\right)+b^{\ast}\left(6;4,0.55\right)+b^{\ast}\left(7;4,0.55\right)
$$

$$
0,0915+0,1647+0,1853+0,1668=0,6083
$$

Pada `R` kita dapat menghitung probabilitas binomial negatif menggunakan fungsi `dnbinom()`. Format fungsi tersebut adalah sebagai berikut:


```r
dnbinom(x, size, prob)
```

> **Note: **
>
> - **x**: jumlah observasi gagal
> - **size**: jumlah observasi sukses
> - **prob**: probabilitas kejadian sukses

Dengan menggunakan fungsi `dnbinom()`, probabilitas Tim A menang pada pertandingan ke-6 dapat dihitung sebagai berikut:


```r
dnbinom(x=2, # jumlah observasi gagal
        size=4, # jumlah observasi sukses
        prob=0.55) # probabilitas sukses
```

```
## [1] 0.1853
```

Pada pertanyaan kedua soal dapat kita impulkan bahwa kita hendak mencari probabilitas kumulatif kemenangan Tim A. Untuk melakukannya kita dapat menggunakan fungsi `pnbinom()`. Format fungsi tersebut adalah sebagai berikut:


```r
pnbinom(q, size, prob, lower.tail = TRUE)
```

> **Note: **
>
> - **q**: jumlah observasi gagal minimum 
> - **size**: jumlah observasi sukses maksimum
> - **prob**: probabilitas sukses
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE

Dengan menggunakan fungsi tersebut, probabilitas kumulatif kemenangan Tim A adalah sebagai berikut:


```r
pnbinom(q=3, # jumlah observasi gagal min
        size=4, # jumlah observasi sukses maks
        prob=0.55) # probabilitas sukses
```

```
## [1] 0.6083
```

```r
# atau
dnbinom(x=0,size=4,prob=0.55)+
  dnbinom(x=1,size=4,prob=0.55)+
  dnbinom(x=2,size=4,prob=0.55)+
  dnbinom(x=3,size=4,prob=0.55)
```

```
## [1] 0.6083
```

### Distribusi Geometris

Pada kenyataannya kita hanya tertarik terhadap probabilitas kejadian sukses pertama kali akan terjadi. Probabilitas kejadian tersebut merupakan kejadian pada **distribusi probabilitas geometris**. Distribusi ini merupakan kasus khusus distribusi binomial negatif.

Jika suatu suatu percobaan independen dapat menghasilkan kejadian sukses dengan probabilitas $p$ dan gagal dengan probabilitas $q=1-p$, maka distribusi probabilitas variabel acak $X$, jumlah percobaan dimana sukses pertama terjadi didefinisikan pada Persamaan \@ref(eq:dgeom):

\begin{equation}
   g\left(x;p\right)=pq^{x-1},\ \ \ \ \ x=1,2,3,...
  (\#eq:dgeom)
\end{equation}

**Contoh 1**

Suatu pabrik memiliki probabilitas 1 dari 100 barang produksinya merupakan produk cacat. Pemeriksaan dilakukan pada setiap barang tersebut. Tentukan probabilitas barang ke-5 hasil pengecekan merupakan barang yang cacat?

Dengan menggunakan Persamaan \@ref(eq:dgeom) probabilitas barang ke-5 merupakan produk gagal sebagai berikut:

$$
g\left(5;0.01\right)=\left(0,01\right)\left(0,99\right)^{5-1}=0,0096
$$

Pada `R` probabilitas tersebut dapat dihitung menggunakan fungsi `dgeom()`. Format fungsi tersebut adalah sebagai berikut:


```r
dgeom(x, prob)
```

> **Note: **
>
> - **x**: vektor numerik observasi dimana kejadian sukses terjadi pertama kali
> - **prob**: probabilitas kejadian sukses

Dengan menggunakan fungsi tersebut, probabilitas geometris dapat dihitung seperti berikut:


```r
dgeom(x=5, # observasi kejadian sukses pertama terjadi
      prob=0.01) # probabilitas kejadian sukses
```

```
## [1] 0.00951
```

Terkadang kita tertarik untuk mempelajari probabilitas kejadian sukses pertama kali berdasarkan suatu rentang observasi atau dapat didefinisikan $P\left(X<r\right),\ P\left(X>r\right),\ atau\ P\left(a<X<b\right)$ yang dapat dituliskan pada Persamaan \@ref(eq:dgeom2).

\begin{equation}
   G\left(r;p\right)=\sum _{x=0}^rg\left(x,p\right)
  (\#eq:dgeom2)
\end{equation}

**Contoh 2**

Berdasarkan contoh sebelumnya hitunglah probabilitas barang cacat pertama kali ditemukan pada observasi kurang dari sama dengan observasi ke-5?

$$
P\left(P\le5\right)=g\left(0;0.01\right)+g\left(1;0.01\right)+...+g\left(5;0.01\right)=0.0585
$$

Pada `R` fungsi yang digunakan untuk menghitung probabilitas kumulatif distribusi probabilitas geometris adalah `pgeom()`. Format yang digunakan adalah sebagai berikut:


```r
pgeom(q, prob, lower.tail = TRUE)
```

> **Note: **
>
> - **q**: batas observasi minimum terjadi
> - **prob**: probabilitas sukses
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE

Berdasarkan hal tersebut, maka probabilitas dapat dihitung seperti berikut:


```r
pgeom(5,0.01)
```

```
## [1] 0.05852
```

```r
# atau
dgeom(0,0.01)+
  dgeom(1,0.01)+
  dgeom(2,0.01)+
  dgeom(3,0.01)+
  dgeom(4,0.01)+
  dgeom(5,0.01)
```

```
## [1] 0.05852
```

Nilai rata-rata dan varians distribusi probabilitas geometris disajikan pada Persamaan \@ref(eq:dgeom3).

\begin{equation}
   \mu=\frac{1}{p}\ dan\ \sigma^2=\frac{1-p}{p^2}
  (\#eq:dgeom3)
\end{equation}

## Distribusi Poisson

**Distribusi probabilitas Poisson** menggambarkan berapa kali suatu peristiwa terjadi pada sebuah interval yang spesifik. Interval dapat berupa waktu, jarak, area, atau volume.

Distribusi Poisson didasarkan pada dua asumsi. Asumsi pertama menjelaskan bahwa probabilitas proporsional terhadap panjang interval. Asumsi yang kedua adalah interval bersifat independen. Dengan kata lain semakin panjang suatu interval, semakin besar probabilitas, dan jumlah kejadian pada sebuah interval tidak mempengaruhi interval lainnya. Distribusi ini juga merupakan bentuk terbatas dari distribusi binomial dimana probabilitas keberhasilan sangat kecil dengan ukuran sampel $n$ besar.

Probabilitas Poisson memiliki karakteristik sebagai berikut:

1. variabel acak merupakan berapa kali suatu peristiwa terjadi selama interval yang ditentukan.
2.probabilitas suatu peristiwa proporsional terhadap ukuran interval.
3. interval tidak tumpang tindih dan bersifat independen

Distribusi probabilitas Poisson pada variabel acak $X$, merepresentasikan jumlah luaran yang terjadi pada interval waktu yang diberikan atau wilayah yang spesifik dan dinotasikan sebagai $t$. Distribusi probabilitas dituliskan pada Persamaan \@ref(eq:dpoisson):

\begin{equation}
   p\left(x;\lambda t\right)=\frac{e^{-\lambda t}\left(\lambda t\right)^x}{x!},\ \ \ \ \ \ x=0,1,2,....
  (\#eq:dpoisson)
\end{equation}

dimana $\lambda$ merupakan rata-rata jumlah luaran per satuan waktu, jarak, area, atau volume dan $e=2,71828...$

Kumulatif probabilitas Poisson dituliskan berdasarkan Persamaan \@ref(eq:dpoisson2):

\begin{equation}
   P\left(r;\lambda t\right)=\sum_{x=0}^rp\left(x;\lambda t\right)
  (\#eq:dpoisson2)
\end{equation}

dengan nilai rata-rata dan varians distribusinya disajikan pada Persamaan \@ref(eq:dpoisson3).

\begin{equation}
   \mu\ dan\ \sigma=\lambda t
  (\#eq:dpoisson3)
\end{equation}

**Contoh**

Selama melakukan eksperimen laboratorium, rata-rata jumlah partikel radioaktif yang melewati couter pada 1 milidetik sebesar 4. Berapa probabilitas 6 partikel memasuki counter pada milidetik yang diberikan?

Contoh kasus tersebut dapat diselesaikan menggunakan Persamaan \@ref(eq:dpoisson) dengan nilai $x=4$ dan $\lambda t=4$ seperti berikut:

$$
p\left(6;4\right)=\frac{e^{-4}\left(4\right)^6}{6!}=0,1042
$$

Kita dapat menggunakan fungsi `dpois()` pada `R` untuk menghitung probabilitas Poisson. Format yag digunakan adalah sebagai berikut:


```r
dpois(x, lambda)
```

> **Note: **
>
> - **x**: vektor numerik
> - **lamda**: jumlah rata-rata luaran

Probabilitas 6 partikel memasuki counter berdasarkan fungsi tersebut adalah sebagai berikut:


```r
dpois(x=6, lambda=4)
```

```
## [1] 0.1042
```

Contoh kasus tersebut juga dapat diselesaikan menggunakan Persamaan \@ref(eq:dpoisson2) dengan terlebih dahulu menghitung selisih $P(X\le6)$  terhadap $P(X\le5)$. Pada `R` fungsi yang digunakan adalah `ppois()`. Format fungsi tersebut adalah sebagai berikut:


```r
ppois(q, lambda, lower.tail = TRUE)
```

> **Note: **
>
> - **q**: vektor numerik
> - **lambda**: jumlah rata-rata luaran
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE

Dengan menggunakan fungsi tersebut, hasil yang diperoleh adalah sebagai berikut:


```r
ppois(6,4)-ppois(5,4)
```

```
## [1] 0.1042
```

## Distribusi Uniform

**Distribusi uniform** merupakan distribusi kontinu yang paling sederhana yang ditandai dengan fungsi densitas yang datar serta probabilitas yang seragam sepanjang interval tertutup. Distribusi ini juga disebut sebagai distribusi persegi panjang sebab bentuk distribusinya yang menyerupai persegi panjang. Fungsi densitas untuk distribusi uniform disajikan pada Persamaan \@ref(eq:duniform).

\begin{equation}
f(x;A,B) =
  \begin{cases}
    \frac{1}{B-A}       & \quad A\le x\le B\\
    0                   & \quad\text{}
    \end{cases}
 (\#eq:duniform)
\end{equation}

Nilai mean dan varians dari distribusi uniform disajikan pada Persamaan \@ref(eq:duniform2).

\begin{equation}
   \mu=\frac{A+B}{2}\ dan\ \sigma^2=\frac{\left(B-A\right)^2}{12}
  (\#eq:duniform2)
\end{equation}

Untuk memudahkan pemahaman pembaca mengenai distribusi ini, berikut penulis sajikan visualisasi distribusi uniform dengan nilai minimum=1 dan maksimum=3. Variabel acak dibuat menggunakan fungsi `runif()`. Format fungsi yang digunakan adalah sebagai berikut:


```r
runif(n, min = 0, max = 1)
```

> **Note: **
>
> - **n**: jumlah data atau panjang variabel acak
> - **min**: nilai minimum variabel acak
> - **max**: nilai maksimum variabel acak

Visualisasi disajikan pada Gambar \@ref(fig:uniformvis).

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/uniformvis-1} 

}

\caption{Distribusi uniform dengan nilai min 1 dan max 3}(\#fig:uniformvis)
\end{figure}

Berdasarkan Gambar \@ref(fig:uniformvis), probabilitas distribusinya adalah sebagai berikut:

$$
f(x;A,B) =
  \begin{cases}
    \frac{1}{3}       & \quad 0\le x\le 4\\
    0                   & \quad\text{}
    \end{cases}
$$

Kita juga dapat menghitung probabilitas suatu nilai melalui distribusi tersebut. Sebagai contoh, hitunglah probabilitas nilai $X\ge3$?

$$
P\left[X\ge3\right]=\int_3^4dx=\frac{1}{4}
$$

Jika contoh tersebut divisualisasikan, maka akan tampak seperti pada Gambar \@ref(fig:uniformvis2).

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/uniformvis2-1} 

}

\caption{Probabilitas distribusi uniform pada rentang nilai x 3 sampai 4}(\#fig:uniformvis2)
\end{figure}

Pada `R` terdapat 2 buah fungsi untuk menghitung probabilitas distribusi unifofm. Fungsi pertama adalah `dunif()` dan yang kedua adalah `punif()`. Fungsi pertama akan menghasilkan probabilitas (*likelihood*) dari suatu nilai yang kita inginkan, sedangkan fungsi kedua adalah fungsi probabilitas kumulatif yang akan menghasilkan nilai berdasarkan rentang yang dimasukkan (rentang satu arah bisa $\le$ atau $\ge$).

Format fungsi `dunif()` adalah sebagai berikut:


```r
dunif(x, min = 0, max = 1)
```

> **Note: **
>
> - **n**: jumlah data atau panjang variabel acak
> - **min**: nilai minimum variabel acak
> - **max**: nilai maksimum variabel acak

Format fungsi `punif` adalah sebagai berikut:


```r
punif(q, min = 0, max = 1, lower.tail = TRUE)
```

> **Note: **
>
> - **q**: vektor numerik
> - **min**: nilai minimum variabel acak
> - **max**: nilai maksimum variabel acak
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE.

Nilai probabilitas berdasarkan contoh soal sebelumnya merupakan contoh kasus probabilitas kumulatif sehingga digunakan fungsi `punif()` untuk menghitung probabilitasnya.


```r
punif(3, min=1, max=4, lower.tail=FALSE)
```

```
## [1] 0.3333
```

## Distribusi Normal

Distribusi kontinu yang paling sering digunakan dalam analisa statistik adalah **distribusi normal** atau disebut juga sebagai distribusi Gauss. Distribusi ini dicirikan dari bentuknya yang mirip dengan lonceng. Secara umum fungsi densitas distribusi normal disajikan pada Persamaan \@ref(eq:dnorm).

\begin{equation}
   n\left(x;\mu,\sigma\right)=\frac{1}{\sqrt{2\pi\sigma}}e^{-\frac{1}{2\sigma^2}\left(x-\mu\right)^2},\ \ \ \ \ \ -\infty<x<\infty
  (\#eq:dnorm)
\end{equation}

dimana $\pi=3,14159...$ dan $e=2,71828...$.

Berdasarkan persamaan di atas terdapat dua parameter penting dalam distribusi normal yaitu nilai mean $\mu$ dan simpangan baku $\sigma$. Kedua nilai tersebut akan mempengaruhi bentuk dari distribusi normal yang terbentuk. Pada contoh selanjutnya akan diberikan visualisasi mengenai bentuk distribusi normal dengan berbagai variasi mean dan simpangan baku.

- **Distribusi normal dengan $\mu$ berbeda dan $\sigma$ yang sama.**

Pada Gambar \@ref(fig:normvis) disajikan visualisasi dua buah distribusi normal dengan nilai $\mu$ sama dan $\sigma$ berbeda.

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/normvis-1} 

}

\caption{Distribusi normal dengan nilai mean sama dan simpangan baku berbeda.}(\#fig:normvis)
\end{figure}

- **Distribusi normal dengan $\mu$ sama dan $\sigma$ yang berbeda.**

Pada Gambar \@ref(fig:normvis2) disajikan visualisasi dua buah distribusi normal dengan nilai $\mu$ berbeda dan $\sigma$ sama. Perbedaan $\sigma$ menyebabkan bentuk distribusi yang lebih datar. $\sigma$ kecil membuat bentuk distribusi yang lebih lancip (sebaran data kecil), sedangkan $\sigma$ akan berlaku sebaliknya.

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/normvis2-1} 

}

\caption{Distribusi normal dengan nilai mean sama dan simpangan baku berbeda.}(\#fig:normvis2)
\end{figure}

- **Distribusi normal dengan $\mu$ berbeda dan $\sigma$ yang berbeda.**

Pada Gambar \@ref(fig:normvis3) disajikan visualisasi dua buah distribusi normal dengan nilai $\mu$ berbeda dan $\sigma$ yang berbeda pula. Perbedaan tersebut menyebabkan perbedaan letak distribsui normal serta bentuk distribusinya.

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/normvis3-1} 

}

\caption{Distribusi normal dengan nilai mean berbeda dan simpangan baku berbeda.}(\#fig:normvis3)
\end{figure}

Berdasarkan visualisasi di atas, sifat-sifat dasar distribusi normal adalah sebagai berikut:

1. Modus distribusi normal berada pada titik horizontal dimana kurva berada pada posisi maksimum atau $x=\mu$.
2. Kurva berbentuk simestris terhadap nilai mean $\mu$.
3. Kurva memiliki titik infleksi pada $x=\mu \pm \sigma$, yang cekung kebawah jika $\mu-\sigma<X<\mu+\sigma$ dan cekung ke atas pada titik diluar rentang tersebut.
4. Kurva normal mendekati sumbu horizontal asimtotik saat kita melanjutkan ke arah mana pun dari rata-rata.
5. Luas total di bawah kurva dan di atas sumbu horizontal adalah 1.

Sifat lain yang dimiliki oleh distribusi normal adalah sebagai berikut:

1. Sekitar 68% luas dibawah kurva normal berada pada kisaran 1 $\sigma$ dari nilai $\mu$.
2. Sekitar 95% luas dibawah kurva normal berada pada kisaran 2 $\sigma$ dari nilai $\mu$.
3. Sekitar 99,7% luas dibawah kurva normal berada pada kisaran 3 $\sigma$ dari nilai $\mu$.

Secara kolektif, titik-titik ini dikenal sebagai **aturan empiris** atau **aturan 68-95-99,7**. Hal ini jelas, mengingat distribusi normal sebagian besar hasil akan berada dalam 3 $\sigma$ dari $\mu$.

### Luas Area Di Bawah Kurva Normal

Untuk memperoleh luas area dibawah distribusi normal kita perlu membuat batasan pada kurva tersebut. Dua koordinat pembatas dapat kita definisikan sebagai $x_1$ dan $x_2$. Luas area yang diarsir (lihat Gambar \@ref(fig:normvis4)) selanjutnya dihitung dengan cara mengintegralkan area yang diarsir dengan batasan dua koordinat sebelumnya atau dapat ditulis sebagai berikut:

$$
P\left(x_1<X<x_2\right)=\int_{x_1}^{x_2}n\left(x;\mu,\sigma\right)dx=\frac{1}{\sqrt{2\pi\sigma}}\int_{x_1}^{x_2}e^{-\frac{1}{2\sigma^2}\left(x-\mu\right)^2}dx
$$

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/normvis4-1} 

}

\caption{Luas area di bawah kurva normal.}(\#fig:normvis4)
\end{figure}


Menghitung luas area di bawah kurva normal bukanlah pekerjaan yang mudah dilakukan sehingga terkadang kita memerlukan alat bantu untuk melakukan proses perhitungan. Alat bantu yang umum digunakan adalah Tabel distribusi normal standard (distribusi normal dengan $\mu$ 0 dan $\sigma^2$ 1) yang dapat pembaca unduh pada tautan [berikut](https://onlinepubs.trb.org/onlinepubs/nchrp/cd-22/manual/v2appendixc.pdf). Untuk dapat menggunakan Tabel tersebut kita perlu mengubah nilai $x_1$ dan $x_2$ pada Gambar \@ref(fig:normvis4) menjadi $Z$. Untuk melakukannya kita dapat menggunakan Persamaan \@ref(eq:dnorm2).

\begin{equation}
   Z=\frac{X-\mu}{\sigma}
  (\#eq:dnorm2)
\end{equation}

Jika kita lihat berdasarkan Gambar \@ref(fig:normvis4), luas area yang diblok dapat dihitung dengan Tabel distribusi normal. Luas area yang dicari dihitung sebagai berikut:

$$
P\left(x_1<z\le x_2\right)=P\left(z< x_2\right)+P\left(z> x_1\right)
$$

Agar pembaca lebih memahami penerapan distribusi ini, misalkan 
kita diminta untuk menghitung probabilitas masa layan lampu. Rerata masa layan lampu suatu produk adalah 750 jam dengan simpangan baku 80 jam. Distribusi dari masa layan lampu tersebut diasumsikan mengikuti distribusi normal. Hitunglah probabilitas:

a. Lampu memiliki masa layan antara 750 sampai 830 jam?
b. Lampu dengan masa layan tepat 830 jam?
c. Lampu dengan masa layan lebih dari atau sama dengan 830 jam

**Masa layan lampu antara 750 sampai 830 jam**

Distribusi dan luasan yang dicari dapat digambarkan berdasarkan Gambar \@ref(fig:normvis5) berikut:

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/normvis5-1} 

}

\caption{Luas area masa layan lampu antara 750 sampai 830 jam.}(\#fig:normvis5)
\end{figure}

Nilai rentang perlu dikonversi kedalam nilai distribusi normal standard menggunakan Persamaan \@ref(eq:dnorm2). Berikut adalah proses perhitungannya:

$$
Z_{750}=\frac{750-750}{80}=0\ \ \ dan\ \ \ Z_{830}=\frac{830-750}{80}=1
$$

Dengan menggunakan Tabel distribusi normal, probabilitas yang diinginkan dapat dihitung sehingga diperoleh nilai probabilitas sebagai berikut:

$$
P\left(z<1\right)=0,3413
$$

**Masa layan lampu tepat 830 jam**

Pertanyaan dapat dijawab menggunakan Persamaan \@ref(eq:dnorm). Hasil yang diperoleh adalah sebagai berikut:

$$
n\left(750;750,80\right)=\frac{1}{\sqrt{2\pi\left(80\right)}}e^{-\frac{1}{2\left(80\right)^2}\left(\left(750\right)-\left(750\right)\right)^2}=0.003
$$

**Masa layan lampu lebih dari atau sama dengan 830 jam**

Distribusi dan luasan yang dicari dapat digambarkan berdasarkan Gambar \@ref(fig:normvis6) berikut:

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/normvis6-1} 

}

\caption{Luas area masa layan lampu lebih dari atau sama dengan 830 jam.}(\#fig:normvis6)
\end{figure}

Probabilitas berdasarkan luas area tersebut dapat dihitung seperti berikut:

$$
P\left(z>1\right)=0,5-0,3413=0,1578
$$

Pada `R` probabilitas distribusi normal dapat dihitung menggunakan dua buah fungsi yaitu `dnorm()` (probabilitas distribusi normal) dan `pnorm()` (probabilitas kumulatif distribusi normal). Format yang digunakan adalah sebagai berikut:


```r
dnorm(x, mean = 0, sd = 1)
pnorm(q, mean = 0, sd = 1, lower.tail = TRUE)
```

> **Note: **
>
> - **x,p**: vektor numerik atau kuantil
> - **mean**: rata-rata populasi
> - **sd**: simpangan baku populasi

Berikut adalah contoh penyelesaian contoh soal masa layan lampu menggunakan sintaks `R`:


```r
# masa layan 750 sampai 830 jam
pnorm(q=830, mean=750, sd=80)-pnorm(q=750, mean=750, sd=80)
```

```
## [1] 0.3413
```

```r
# masa layan 830 jam
dnorm(x=830, mean=750, sd=80)
```

```
## [1] 0.003025
```

```r
# masa layan lebih dari sama dengan 830 jam
pnorm(q=830, mean=750, sd=80, lower.tail=FALSE)
```

```
## [1] 0.1587
```

### Uji Kecocokan Distribusi Normal

Uji kecocokan distribusi data apakah distribusi tersebut berdistribusi normal dapat dilakukan dengan dua cara yaitu: analisis grafik dan analisis numerik. Analisis grafik dilakukan dengan menggunakan grafik yaitu histogram, density plot, QQ-plot dan ECDF. Dalam Chapter sebelumnya telah penulis jelaskan bahwa ECDF dapat digunakan untuk menguji kecocokan distribusi secara umum. Metode lain yang dapat digunakan adalah metode numerik menggunakan metode Shapiro-Wilk (SW), Shapiro-Francia (SF), dll. Dalam buku ini penulis hanya akan menjelaskan uji kecocokan distribusi normal menggunakan metode Shaphiro-Wilk.

Kita adakn menggunakan dataset `airquality` yang merupakan data pengukuran kualitas udara New York bulan Mei sampai September 1973. Pertama-tama kita perlu melihat ringkasan data dari dataset tersebut. Berikut adalah sintaks untuk melakukannya:


```r
library(tibble)
```


```r
glimpse(airquality)
```

```
## Observations: 153
## Variables: 6
## $ Ozone   <int> 41, 36, 12, 18, NA, 28, 23, 19, 8,...
## $ Solar.R <int> 190, 118, 149, 313, NA, NA, 299, 9...
## $ Wind    <dbl> 7.4, 8.0, 12.6, 11.5, 14.3, 14.9, ...
## $ Temp    <int> 67, 72, 74, 62, 56, 66, 65, 59, 61...
## $ Month   <int> 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5...
## $ Day     <int> 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11,...
```

Kita akan mengecek distribusi dari konsentrasi ozon apakah berdistribusi normal atau tidak, kita dapat memvisualisasikannya menggunakan grafik dalam contoh ini adalah grafik QQ-plot dan ECDF. Berikut adalah visualisasi yang dihasilkan


```r
# install.packages("ggpubr")
library(ggplot2)
library(dplyr)
library(ggpubr)
```


```r
## set tema default dari paket ggpubr
theme_set(theme_pubr())

## QQ-plot
qq<-ggplot(airquality, aes(sample=Ozone))+
  stat_qq(color="#2E9FDF")+
  stat_qq_line(color="#FC4E07")

## membuat data frame
x <- sort(airquality[!is.na(airquality$Ozone), 1])

y <- rnorm(length(x),mean=mean(x),sd=sd(x))

data <- data.frame(x=c(x,y),
               dist=gl(2,length(x),
                       labels=c("Empiris","Normal")))
## ECDF
ecdf<-ggplot(data, aes(x, colour=dist))+
  stat_ecdf()+
  labs(y="F(Ozon)", x="Ozon")+
  scale_color_manual(values=c("#2E9FDF", "#FC4E07"))+
  scale_x_continuous(breaks=seq(round(min(y)),round(max(x)),35))+
  geom_rug()

## density
dens<-ggplot(data, aes(x, fill=dist))+
  geom_density(alpha=0.5)+
  labs(x="Ozon")+
  scale_fill_manual(values=c("#2E9FDF", "#FC4E07"))+
  scale_x_continuous(breaks=seq(round(min(y)),round(max(x)),35))+
  geom_rug()

## Boxplot
data2 <- subset(data, dist=="Empiris")
bxp <- ggplot(data2, aes(x="", y=x))+
  geom_boxplot(color="#FC4E07",outlier.alpha=0)+
  geom_jitter(color="#2E9FDF",shape=1,position=position_jitter(0.1))+
  labs(y="Ozon", x="")+
  scale_y_continuous(breaks=seq(round(min(y)),round(max(x)),35))+
  coord_flip()+
  geom_rug()
  
## Menggabungkan grafik
ggarrange(dens,bxp,ecdf,qq,
          ncol=2, nrow=2,
          labels=c("a)","b)","c)","d)"))
```

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{EnvStat_files/figure-latex/normvis7-1} 

}

\caption{Visualisasi distribusi konsentrasi ozon Kota New York a)density plot, b)boxplot, c)ecdf, d)qq-plot}(\#fig:normvis7)
\end{figure}

Berdasarkan kedua grafik tersebut terlihat bahwa titik observasi tidak mengikuti garis referensi distribusi normal sehingga dapat disimpulkan bahwa distribusi konsentrasi ozon tidak berdistribusi normal.

Metode lain yang digunakan untuk melakukan uji kecocokan terhadap distribusi normal adalah dengan menggunakan metode Shapiro-Wilk (SW). Metode ini merupakan metode nonparametrik yang memiliki power yang cukup besar untuk ukuran sampel relatif kecil ($<2000$). Perintah yang digunakan pada `R` untuk melakukan uji SW adalah `shapiro.test()`. Format yang digunakan adalah sebagai berikut:


```r
shapiro.test(x)
```

> **Note: **
>
> **x**: vektor numerik.

Pengujian ini merupakan suatu bentuk pengujian statistik sehingga melibatkan dua buah hipotesis. Pengujian statistik tidak akan dijelaskan secara detail pada Chapter ini. Hipotesis yang digunakan adalah sebagai berikut

$H_0$: Sampel berdistribusi normal

$H_1$: Sampel data tidak berdistribusi normal

Berikut adalah uji kecocokan yang dilakukan pada `R`:


```r
shapiro.test(airquality$Ozone)
```

```
## 
## 	Shapiro-Wilk normality test
## 
## data:  airquality$Ozone
## W = 0.88, p-value = 3e-08
```

Berdasarkan hasil perhitungan diperoleh nilai p-value sebesar 2.79e-08. Dengan menggunakan tingkat kepercayaan 95% (error=5%), dapat disimpulkan bahwa distribusi ozon tidak berdistribusi normal (p-value<error).

### Pendekatan Distribusi Binomial Menggunakan Distribusi Normal

Nilai probabilitas distribusi diskrit seperti distribusi binomial dapat dihitung dengan menggunakan pendekatan distribusi binomial. Pendekatan ini berlaku jika jumlah sampel yang digunakan sangat besar. Dengan menggunakan pendekatan ini, kita dapat menghitung probabilitas kumulatif distribusi binomial menggunakan Tabel distribusi normal.

Jika $X$ merupakan variabel acak binomial dengan mean $\mu=np$ dan varians $\sigma^2=npq$, maka bentuk batas distribusi $z$ dengan pendekatan distribusi normal standard dituliskan kedalam Persamaan \@ref(eq:dnorm3).

\begin{equation}
   Z=\frac{X-np}{\sqrt{npq}}
  (\#eq:dnorm3)
\end{equation}

dimana $n\to\infty$ merupakan distribusi normal standard $n\left(z;0,1\right)$. Nilai $z$ yang diperoleh selanjutnya dapat digunakan untuk mencari luasan dibawah kurva normal menggunakan Tabel distribusi normal.

Untuk memahami penerapannya, misalkan diketahui probabilitas suatu pompa air rusak disuatu kawasan adalah 0,4. Jika pada kawasan tersebut terdapat 100 buah pompa. Hitunglah probabilitas jumlah pompa rusak di kawasan tersebut kurang dari 30? ?

Pada kasus tersebut kejadian sukses didefinisikan jika terdapat pompa yang rusak. Untuk menghitungnya pertama-tama kita perlu menghitung nilai mean dan simpangan baku dari populasinya.

$$
\mu=np=\left(100\right)\left(0,4\right)=40\ \ \ dan\ \ \ \sigma=\sqrt{npq}=\sqrt{\left(100\right)\left(0,4\right)\left(0,6\right)}=4,899
$$
Selanjutnya dihitung nilai $z$ dengan nilai $X=29,5$ berdasarkan Persamaan \@ref(eq:dnorm3).

$$
Z=\frac{29,5-40}{\sqrt{4,899}}=-2,14
$$

Dengan menggunakan tabel distribusi normal standard, probabilitas dari kejadian tersebut adalah sebagai berikut (lihat Gambar \@ref(fig:normvis6)):

$$
P\left(X<30\right)\approx P\left(Z<-2,14\right)=0,0162.
$$

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/normvis8-1} 

}

\caption{Luas area jumlah pompa rusak kurang dari 30.}(\#fig:normvis8)
\end{figure}

Pada `R` probabilitas dari peristiwa tersebut dapat dihitung seperti berikut:


```r
pnorm(q=29.5,mean=40,sd=4.899)
```

```
## [1] 0.01604
```

## Distribusi Gamma dan Eksponensial

Distribusi eksponensial dan gamma merupakan distribusi yang berperan penting dalam menjelaskan teori antrian dan masalah reliabilitas. Waktu antara kedatangan di fasilitas layanan dan waktu kegagalan komponen bagian dan sistem kelistrikan sering dimodelkan dengan baik oleh distribusi eksponensial. Hubungan antara gamma dan eksponensial memungkinkan gamma digunakan dalam jenis masalah yang serupa.

Variabel acak kontinu $X$ memiliki distribusi gamma, dengan parameter $\alpha$ dan $\beta$. Fungsi densitas dari distribusi tersebut dituliskan kedalam Persamaan \@ref(eq:dgamma).

\begin{equation}
f\left(x;\alpha ,\beta \right) =
  \begin{cases}
    \frac{1}{\beta^{\alpha}\Gamma\left(\alpha\right)}x^{\alpha-1}e^{-\frac{x}{\beta}}       & \quad x>0\\
    0                   & \quad\text{}
    \end{cases}
 (\#eq:dgamma)
\end{equation}

dimana $\Gamma\left(\alpha\right)$ merupakan fungsi gamma yang dituliskan pada Persamaan \@ref(eq:dgamma2)

\begin{equation}
   \Gamma\left(\alpha\right)=\int_0^{\infty}x^{\alpha-1}e^{-x}dx
  (\#eq:dgamma2)
\end{equation}

Pada Gambar \@ref(fig:gammavis) disajikan visualisasi distribusi gamma dengan variasi $\alpha$ dan $\beta$.


```r
x <- seq(0,6, length=100)
x1 <- dgamma(x, shape=1, scale=1); x1_cum <- cumsum(x1)/max(cumsum(x1)) 
x2 <- dgamma(x, shape=2, scale=1); x2_cum <- cumsum(x2)/max(cumsum(x2))
x3 <- dgamma(x, shape=4, scale=1); x3_cum <- cumsum(x3)/max(cumsum(x3))

data <- data.frame(value=c(x,x,x),
                   density=c(x1,x2,x3),
                   cum_dens=c(x1_cum,x2_cum,x3_cum),
                   alpha=gl(3,length(x1),
                       labels=c(1,2,4)))

dens <- ggplot(data, aes(x=value, y=density, color=alpha))+
  geom_line()+
  scale_color_manual(values=c("#E7B800","#2E9FDF","#FC4E07")
)
ecdf <- ggplot(data, aes(x=value, y=cum_dens, color=alpha))+
  geom_line()+
  labs(y="Fn(x)")+
  scale_color_manual(values=c("#E7B800","#2E9FDF","#FC4E07")
)

ggarrange(dens, ecdf, nrow=1, ncol=2, labels=c("a)","b)"))
```

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{EnvStat_files/figure-latex/gammavis-1} 

}

\caption{Visualisasi distribusi gamma dengan variasi alpha dengan beta 1 a) density plot, b)ecdf}(\#fig:gammavis)
\end{figure}

Distribusi eksponensial merupakan kasus khusus dari distribusi gamma dengan nilai $\alpha=1$. Distribusi probabilitas eksponensial dituliskan kedalam Persamaan \@ref(eq:deksponen).

\begin{equation}
f\left(x;\beta \right) =
  \begin{cases}
    \frac{1}{\beta}e^{-\frac{x}{\beta}}       & \quad x>0\\
    0                   & \quad\text{}
    \end{cases}
 (\#eq:deksponen)
\end{equation}

dimana $\beta>0$.

Persamaan-persamaan berikut merupakan cara untuk menghitung mean dan varians dari kedua distribusi tersebut. Persamaan \@ref(eq:dgamma3) merupakan persamaan untuk menghitung kedua nilai tersebut untuk distribusi gamma, sedangkan Persamaan \@ref(eq:deksponen2) digunakan pada distribusi eksponensial.

\begin{equation}
   \mu=\alpha\beta\ \ \ dan\ \ \ \sigma^2=\alpha\beta^2
  (\#eq:dgamma3)
\end{equation}

\begin{equation}
   \mu=\beta\ \ \ dan\ \ \ \sigma^2=\beta^2
  (\#eq:deksponen2)
\end{equation}


Misalkan dalam suatu kawasan terdapat sistem penyediaan air minum lingkup kecil dengan komponen utama pompa, dimana waktu dalam tahun dimana pompa tersebut gagal beroperasi (rusak) disimbolkan sebagai $T$. Variabel acak $T$ dimodelkan dengan cukup baik menggunakan distribusi eksponensial dengan waktu sampai pompa tersebut gagal berfungsi $\beta=5$. Jika 5 buah pompa dipasang pada sistem yang berbeda , berapa probabilitas setidaknya 2 buah pompa masih berfungsi hingga akhir tahun ke-8?

Probabilitas suatu pompa masih dapat berfungsi setelah 8 tahun dari kasus tersebut dapat dituliskan sebagai berikut:

$$
P\left(T>8\right)=\frac{1}{5}\int_0^{\infty}e^{-\frac{t}{5}}dt=e^{-\frac{8}{5}}\approx0,2.
$$

Probabilitas sedikitnya 2 buah pompa yang masih beroperasi setelah 8 tahun dapat dihitung menggunakan probabilitas kumulatif distribusi binomial seperti berikut:

$$
P\left(X\ge2\right)=\sum_{x=2}^5b\left(x;5,0.2\right)=1-\sum_{x=0}^1b\left(x;5,0.2\right)=1-0,7373=0,2627
$$

Pada `R` probabilitas gamma dapat dihitung menggunakan 2 fungsi yaitu `dgamma()` dan `pgamma()` (probabilitas kumulatif). Format fungsi tersebut adalah sebagai berikut:


```r
dexp(x, rate=1)
pexp(q, rate=1, lower.tail = TRUE)
```

> **Note: **
>
> - **x,p**: vektor numerik atau kuantil
> - **rate**: nilai 1/beta
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE.

Berikut adalah sintaks yang digunakan untuk menghitung probabilitas pada contoh soal tersebut:


```r
# probabilitas pompa masih berfungsi lebih dari 8 tahun
pexp(q=8, rate=1/5, lower.tail=FALSE)
```

```
## [1] 0.2019
```

```r
# probabilitas sedikitnya 2 pompa yang masih berfungsi
pbinom(q=1, size=5, prob=0.2018965, lower.tail=FALSE)
```

```
## [1] 0.2666
```

Contoh lainnya misalkan pada pengujian toksikan terhadap hewan uji untuk menentukan dosis mematikan pada suatu hewan uji. Toksikan yang digunakan merupakan logam berat yang ada di perairan. Berdasarkan dosis tertentu, hasil percobaan menentukan bahwa *survival time*, dalam minggu dari hewan uji, memiliki distribusi gamma dengan $\alpha=5$ dan $\beta=10$. Hitunglah probabilitas hewan uji tidak dapat selamat tidak lebih dari 60 minggu?

Diberikan variabel acak $X$ yang menyatakan *survival time* (waktu hingga mati). Probabilitas yang terjadi dapat dituliskan sebagai berikut:

$$
P\left(X\le60\right)=\frac{1}{\beta^5}\int_0^{\infty}\frac{x^{\alpha-1}e^{-\frac{x}{\beta}}}{\Gamma\left(5\right)}dx
$$

Intergral pada persamaan diatas dapat diselesaikan dengan menggunakan **incomplete gamma function**, yang menjadikan persamaan di atas menjadi fungsi distribusi kumulatif untuk distribusi gamma yang dapat dituliskan kembali seperti berikut:

$$
F\left(x;\alpha\right)=\int_0^x\frac{y^{\alpha-1}e^{-y}}{\Gamma\left(\alpha\right)}dy
$$

jika diberikan $y=\frac{x}{\beta}$ dan $x=\beta y$, persamaan tersebut dapat dituliskan lagi menjadi berikut:

$$
P\left(X\le60\right)=\int_0^6\frac{y^4e^{-y}}{\Gamma\left(\alpha\right)}dy
$$

yang dapat dituliskan sebagai $F\left(6;5\right)$ pada tabel **incomplete gamma function** yang dapat pembaca lihat pada buku yang ditulis oleh Ronald E. Walpole (2012) pada Appendix A.23. Berdasarkan tabel tersebut diperoleh nilai probabilitas sebagai berikut:

$$
P\left(X\le60\right)=F\left(6;5\right)=0,715
$$

Pada `R` probabilitas distribusi gamma dapat dihitung menggunakan fungsi `dgamma()` dan `pgamma()` (probabilitas kumulatif). Format fungsi tersebut adalah sebagi berikut:


```r
dgamma(x, shape, scale)
pgamma(q, shape, scale, lower.tail = TRUE)
```

> **Note: **
>
> - **x,p**: vektor numerik atau kuantil
> - **shape**: nilai alpha
> - **scale**: niali beta
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE.

Berikut adalah nilai probabilitas dari contoh kasus tersebut:


```r
pgamma(q=60, shape=5, scale=10)
```

```
## [1] 0.7149
```

## Distribusi Chi-Square, Student's t, dan Snedecor's F.

Pada sub-chapter kali ini penulis akan menjelaskan sejumlah distribusi probabilitas yang memegang peranan penting dalam statistika inferensi. Distribusi ini tidak akan penulis jelaskan secara detail karena akan terdapat porsi tersendiri pada chapter selanjutnya.  

### Distribusi Chi-Square

Distribusi chi-square merupakan kasus khusu lain dari distribusi gamma, dimana nilai $\alpha$ dan $\beta$ dari distribusi ini masing-masing adalah $\alpha=\nu/2$ dan $\beta=2$ dengan nilai $\nu$ merupakan integer positif. Distribusi ini memiliki parameter tunggal yaitu $\nu$ yang disebut sebagai *degrees of freedom* (derajat kebebasan). Fungsi densitas distribusi ini disajikan pada Persamaan \@ref(eq:dcsq).

\begin{equation}
f\left(x;\nu \right) =
  \begin{cases}
    \frac{1}{2^{\frac{\nu}{2}}\Gamma\left(\frac{\nu}{2}\right)}x^{\frac{\nu}{2}-1}e^{-\frac{x}{2}}       & \quad x>0\\
    0                   & \quad\text{}
    \end{cases}
 (\#eq:dcsq)
\end{equation} 


dimana $\nu$ adalah integer positif.

Pada Gambar \@ref(fig:csqvis) disajikan visualisasi distribusi chi-square dengan variasi $\nu$.


```r
x <- seq(0,20, length=100)
x1 <- dchisq(x, df=1); x1_cum <- cumsum(x1)/max(cumsum(x1))
x2 <- dchisq(x, df=3); x2_cum <- cumsum(x2)/max(cumsum(x2))
x3 <- dchisq(x, df=5); x3_cum <- cumsum(x3)/max(cumsum(x3))
x4 <- dchisq(x, df=7); x4_cum <- cumsum(x4)/max(cumsum(x4))


data <- data.frame(value=c(x,x,x,x),
                   density=c(x1,x2,x3,x4),
                   cum_dens=c(x1_cum,x2_cum,x3_cum,x4_cum),
                   df=gl(4,length(x1),
                       labels=c(1,3,5,7)))

dens <- ggplot(data, aes(x=value, y=density, color=df))+
  geom_line()+
  scale_color_manual(values=c("#E7B800", "#2E9FDF", "#FC4E07", "black"))
ecdf <- ggplot(data, aes(x=value, y=cum_dens, color=df))+
  geom_line()+
  labs(y="Fn(x)")+
  scale_color_manual(values=c("#E7B800", "#2E9FDF", "#FC4E07","black"))

ggarrange(dens, ecdf, nrow=1, ncol=2, labels=c("a)","b)"))
```

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{EnvStat_files/figure-latex/csqvis-1} 

}

\caption{Visualisasi distribusi chi-square dengan variasi derajat kebebasan a) density plot, b)ecdf}(\#fig:csqvis)
\end{figure}

Pada `R` terdapat dua buah fungsi yang digunakan untuk menghitung probabilitas distribusi chi-square yaitu `dchisq()` dan `pchisq()` (probabilitas kumulatif). Format fungsi tersebut adalah sebagai berikut:


```r
dgamma(x, df)
pgamma(q, df, lower.tail = TRUE)
```

> **Note: **
>
> - **x,p**: vektor numerik atau kuantil
> - **df**: derajat kebebasan (n-1)
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE.

### Distribusi Student's t

Distribusi student's t merupakan kasus lain dari distribusi gamma. Fungsi densitas probabilitasnya disajikan pada Persamaan \@ref(eq:dst).

\begin{equation}
   \frac{\Gamma\left[\frac{\left(r+1\right)}{2}\right]}{\sqrt{r\pi}\Gamma\left(\frac{r}{2}\right)}\left(1+\frac{x^2}{r}\right)^{-\frac{\left(r+1\right)}{2}},\ \ \ \ \ -\infty<x<\infty
  (\#eq:dst)
\end{equation}

dimana $r$ merupakan derajat kebebasan atau $\left(n-1\right)$.

Pada Gambar \@ref(fig:dtvis) disajikan visualisasi distribusi t dengan variasi $r$.


```r
x <- seq(-7,7, length=100)
x1 <- dt(x, df=1); x1_cum <- cumsum(x1)/max(cumsum(x1))
x2 <- dt(x, df=12); x2_cum <- cumsum(x2)/max(cumsum(x2))
x3 <- dt(x, df=20); x3_cum <- cumsum(x3)/max(cumsum(x3))
x4 <- dnorm(x); x4_cum <- cumsum(x4)/max(cumsum(x4))


data <- data.frame(value=c(x,x,x,x),
                   density=c(x1,x2,x3,x4),
                   cum_dens=c(x1_cum,x2_cum,x3_cum,x4_cum),
                   df=gl(4,length(x1),
                       labels=c(1,12,20,"Normal")))

dens <- ggplot(data, aes(x=value, y=density, color=df))+
  geom_line()+
  scale_color_manual(values=c("#E7B800", "#2E9FDF", "#FC4E07", "black"))
ecdf <- ggplot(data, aes(x=value, y=cum_dens, color=df))+
  geom_line()+
  labs(y="Fn(x)")+
  scale_color_manual(values=c("#E7B800", "#2E9FDF", "#FC4E07", "black"))

ggarrange(dens, ecdf, nrow=1, ncol=2, labels=c("a)","b)"))
```

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{EnvStat_files/figure-latex/dtvis-1} 

}

\caption{Visualisasi distribusi t dengan variasi derajat kebebasan a) density plot, b)ecdf}(\#fig:dtvis)
\end{figure}

Jika kita perhatikan dengan seksama terlihat bahwa peningkatan derajat kebebasan akan membuat distribusi yag dihasilkan semakin mendekati kurva normal.

Pada `R` terdapat dua fungsi yang berguna untuk menghitung probabilitas distribusi t yaitu `dt()` dan `pt()` (probabilitas kumulatif). Format fungsi yang digunakan adalah sebagai berikut:


```r
dt(x, df)
pt(q, df, lower.tail = TRUE)
```

> **Note: **
>
> - **x,p**: vektor numerik atau kuantil
> - **df**: derajat kebebasan (n-1)
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE.

### Distribusi Snedecor's F

Fungsi densitas probabilitas distribusi F disajikan pada Persamaan \@ref(eq:dF).

\begin{equation}
f\left(x;df1,df2 \right) =
  \begin{cases}
    \frac{\Gamma\left[\frac{\left(df1+df2\right)}{2}\right]}{\Gamma\left(\frac{df1}{2}\right)\Gamma\left(\frac{df2}{2}\right)}\left(\frac{df1}{df2}\right)^{\frac{df1}{2}}x^{\frac{df1}{2}-1}\left(1+\frac{df1}{df2}x\right)^{-\frac{\left(df1+df2\right)}{2}}       & \quad x>0\\
    0                   & \quad\text{}
    \end{cases}
 (\#eq:dF)
\end{equation}

dimana $df1$ dan $df2$ merupakan derajat kebebasan.

Pada Gambar \@ref(fig:dFvis) disajikan visualisasi distribusi F dengan variasi $df1$ dan $df2$.


```r
x <- seq(0,5, length=100)
x1 <- df(x, df1=1, df2=10); x1_cum <- cumsum(x1)/max(cumsum(x1))
x2 <- df(x, df1=6, df2=60); x2_cum <- cumsum(x2)/max(cumsum(x2))
x3 <- df(x, df1=10,df2=100); x3_cum <- cumsum(x3)/max(cumsum(x3))

data <- data.frame(value=c(x,x,x),
                   density=c(x1,x2,x3),
                   cum_dens=c(x1_cum,x2_cum,x3_cum),
                   df1=gl(3,length(x1),
                       labels=c(1,6,10)),
                   df2=gl(3,length(x1),
                        labels=c(10,60,100)))

dens <- ggplot(data, aes(x=value, y=density, color=df1, linetype=df2))+
  geom_line()+
  theme(legend.position="right", legend.box="vertical")+
  guides(color=FALSE)+
  scale_color_manual(values=c("#E7B800", "#2E9FDF", "#FC4E07"))
ecdf <- ggplot(data, aes(x=value, y=cum_dens, color=df1, linetype=df2))+
  geom_line()+
  labs(y="Fn(x)")+
  theme(legend.position="right", legend.box="vertical")+
  guides(linetype=FALSE)+
  scale_color_manual(values=c("#E7B800", "#2E9FDF", "#FC4E07"))

ggarrange(dens, ecdf, nrow=2, ncol=1, labels=c("a)","b)"))
```

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{EnvStat_files/figure-latex/dFvis-1} 

}

\caption{Visualisasi distribusi F dengan variasi derajat kebebasan a) density plot, b)ecdf}(\#fig:dFvis)
\end{figure}

Pada `R` terdapat dua fungsi yang berguna untuk menghitung probabilitas distribusi F yaitu `df()` dan `pf()` (probabilitas kumulatif). Format fungsi yang digunakan adalah sebagai berikut:


```r
dt(x, df1, df2)
pt(q, df1, df2, lower.tail = TRUE)
```

> **Note: **
>
> - **x,p**: vektor numerik atau kuantil.
> - **df1,df2**: derajat kebebasan.
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE.

## Distribusi Kontinu Lainnya

### Distribusi Beta

Distribusi ini merupakan perluasan dari distribusi uniform. Distribusi ini didasarkan pada fungsi beta yang disajikan pada Persamaan \@ref(eq:dbeta).

\begin{equation}
   B\left(\alpha,\beta\right)=\int_0^1x^{\alpha-1}\left(1-x\right)^{\beta-1}dx=\frac{\Gamma\left(\alpha\right)\Gamma\left(\beta\right)}{\Gamma\left(\alpha+\beta\right)},\ \ \ untuk\ \alpha,\beta>0
  (\#eq:dbeta)
\end{equation}

dimana $\Gamma\left(\alpha\right)$ merupakan fungsi gamma.

Suatu variabel acak kontinu $X$ memiliki distribusi beta dengan parameter $\alpha>0$ dan $\beta>0$ jika densitas fungsiya diberikan pada Persamaan \@ref(eq:dbeta2).

\begin{equation}
f\left(x \right) =
  \begin{cases}
    \frac{1}{B\left(\alpha,\beta\right)}x^{\alpha-1}\left(1-x\right)^{\beta-1}       & \quad 0<x<1\\
    0                   & \quad\text{}
    \end{cases}
 (\#eq:dbeta2)
\end{equation}

Nilai mean dan varians distribusi beta dituliskan kedalam Persamaan \@ref(eq:dbeta3).

\begin{equation}
   \mu=\frac{\alpha}{\alpha+\beta}\ \ \ \ dan\ \ \ \ \sigma^2=\frac{\alpha\beta}{\left(\alpha+\beta\right)^2\left(\alpha+\beta+1\right)}
  (\#eq:dbeta3)
\end{equation}

Pada Gambar \@ref(fig:dbeta) disajikan visualisasi distribusi beta dengan variasi $\alpha$ dan $\beta$.


```r
x <- seq(0,1, length=100)
x1 <- dbeta(x, shape1=1, shape2=5); x1_cum <- cumsum(x1)/max(cumsum(x1))
x2 <- dbeta(x, shape1=6, shape2=30); x2_cum <- cumsum(x2)/max(cumsum(x2))
x3 <- dbeta(x, shape1=10,shape2=50); x3_cum <- cumsum(x3)/max(cumsum(x3))

data <- data.frame(value=c(x,x,x),
                   density=c(x1,x2,x3),
                   cum_dens=c(x1_cum,x2_cum,x3_cum),
                   alpha=gl(3,length(x1),
                       labels=c(1,6,10)),
                   beta=gl(3,length(x1),
                        labels=c(10,60,100)))

dens <- ggplot(data, aes(x=value, y=density, color=alpha, linetype=beta))+
  geom_line()+
  theme(legend.position="right", legend.box="vertical")+
  guides(color=FALSE)+
  scale_color_manual(values=c("#E7B800", "#2E9FDF", "#FC4E07"))
ecdf <- ggplot(data, aes(x=value, y=cum_dens, color=alpha, linetype=beta))+
  geom_line()+
  labs(y="Fn(x)")+
  theme(legend.position="right", legend.box="vertical")+
  guides(linetype=FALSE)+
  scale_color_manual(values=c("#E7B800", "#2E9FDF", "#FC4E07"))

ggarrange(dens, ecdf, nrow=2, ncol=1, labels=c("a)","b)"))
```

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{EnvStat_files/figure-latex/dbeta-1} 

}

\caption{Visualisasi distribusi beta dengan variasi derajat kebebasan a) density plot, b)ecdf}(\#fig:dbeta)
\end{figure}

Pada `R` terdapat dua fungsi yang berguna untuk menghitung probabilitas distribusi beta yaitu `dbeta()` dan `pbeta()` (probabilitas kumulatif). Format fungsi yang digunakan adalah sebagai berikut:


```r
dbeta(x, shape1, shape2)
pbeta(q, shape1, shape2, lower.tail = TRUE)
```

> **Note: **
>
> - **x,p**: vektor numerik atau kuantil.
> - **shape1**: alpha.
> - **shape2**: beta.
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE.

### Distribusi Lognormal

Distribusi lognormal telah digunakan pada berbagai aplikasi yang luas. Distribusi berlaku dalam kasus di mana transformasi log natural menghasilkan distribusi normal.

Suatu variabel acak $X$ berdistribusi lognormal jika variabel acak $Y=ln\left(X\right)$ berdistribusi normal dengan nilai mean $\mu$ dan simpangan baku $\sigma$. Fungsi densitas yang digunakan disajikan pada Persamaan \@ref(eq:dlognormal).

\begin{equation}
f\left(x;\mu,\sigma \right) =
  \begin{cases}
    \frac{1}{\sqrt{2\pi\sigma x}}e^{-\frac{1}{2\sigma^2}\left[\ln\left(x\right)-\mu\right]^2}       & \quad x\ge 0\\
    0                   & \quad x<0
    \end{cases}
 (\#eq:dlognormal)
\end{equation}

Nilai mean dan varians distribusi lognormal dihitung menggunakan Persamaan \@ref(eq:dlognormal2).

\begin{equation}
   \mu=e^{\mu+\frac{\sigma^2}{2}}\ \ \ \ dan\ \ \ \ \sigma^2=e^{2\mu+\sigma^2}\left(e^{\sigma^2}-1\right)
  (\#eq:dlognormal2)
\end{equation}

Pada Gambar \@ref(fig:dlognnormalvis) disajikan visualisasi distribusi lognormal dengan variasi $\mu$ dan $\sigma$.


```r
x <- seq(0,5, length=100)
x1 <- dlnorm(x, meanlog=0, sdlog=1); x1_cum <- cumsum(x1)/max(cumsum(x1))
x2 <- dlnorm(x, meanlog=1, sdlog=1.5); x2_cum <- cumsum(x2)/max(cumsum(x2))
x3 <- dlnorm(x, meanlog=2, sdlog=2); x3_cum <- cumsum(x3)/max(cumsum(x3))

data <- data.frame(value=c(x,x,x),
                   density=c(x1,x2,x3),
                   cum_dens=c(x1_cum,x2_cum,x3_cum),
                   mean=gl(3,length(x1),
                       labels=c(0,1,2)),
                   sd=gl(3,length(x1),
                        labels=c(1,1.5,2)))

dens <- ggplot(data, aes(x=value, y=density, color=mean, linetype=sd))+
  geom_line()+
  theme(legend.position="right", legend.box="vertical")+
  guides(color=FALSE)+
  scale_color_manual(values=c("#E7B800", "#2E9FDF", "#FC4E07"))
ecdf <- ggplot(data, aes(x=value, y=cum_dens, color=mean, linetype=sd))+
  geom_line()+
  labs(y="Fn(x)")+
  theme(legend.position="right", legend.box="vertical")+
  guides(linetype=FALSE)+
  scale_color_manual(values=c("#E7B800", "#2E9FDF", "#FC4E07"))

ggarrange(dens, ecdf, nrow=2, ncol=1, labels=c("a)","b)"))
```

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{EnvStat_files/figure-latex/dlognnormalvis-1} 

}

\caption{Visualisasi distribusi beta dengan variasi mean dan sd a) density plot, b)ecdf}(\#fig:dlognnormalvis)
\end{figure}

Pada `R`, fungsi utama yang digunakan untuk menghitung probabilitas distribusi lognormal adalah `dlnorm()` dan `plnorm()` (probabilitas kumulatif). Format fungsi tersebut adalah sebagai berikut:


```r
dlnorm(x, meanlog = 0, sdlog = 1)
plnorm(q, meanlog = 0, sdlog = 1, lower.tail = TRUE)
```

> **Note: **
>
> - **x,p**: vektor numerik atau kuantil.
> - **meanlog**: mean dalam bentuk logaritmik.
> - **sdlog**: simpangan baku dalam bentuk logaritmik.
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE.

### Distribusi Cauchy

Distribusi Chauchy merupakan kasus khusus dari distribusi t ketika nilai $r$ atau derajat kebebasannya adalah 1. Distribusi ini tampak mirip dengan distribusi normal, namun dengan ekor yang lebih panjang. Parameter utama dari distribusi probabilitas ini adalah $\beta$ dan $m$ atau median. Fungsi densitas probabilitasnya dituliskan kedalam Persamaan \@ref(eq:dcauchy).

\begin{equation}
   f\left(x;m,\beta\right)=\frac{1}{\beta\pi}\left[1+\left(\frac{x-m}{\beta}\right)^2\right]^{-1},\ \ \ \ \ \ \ \ -\infty<x<\infty
  (\#eq:dcauchy)
\end{equation}

Pada Gambar \@ref(fig:dcauchyvis) disajikan visualisasi distribusi Cauchy dengan variasi $m$ dan $\beta$.


```r
x <- seq(-7,7, length=100)
x1 <- dcauchy(x, location=0, scale=1); x1_cum <- cumsum(x1)/max(cumsum(x1))
x2 <- dcauchy(x, location=0.5, scale=1.5); x2_cum <- cumsum(x2)/max(cumsum(x2))
x3 <- dcauchy(x, location=1, scale=2); x3_cum <- cumsum(x3)/max(cumsum(x3))
x4 <- dnorm(x); x4_cum <- cumsum(x4)/max(cumsum(x4))

data <- data.frame(value=c(x,x,x,x),
                   density=c(x1,x2,x3,x4),
                   cum_dens=c(x1_cum,x2_cum,x3_cum,x4_cum),
                   m=gl(4,length(x1),
                       labels=c(0,1,1.5,"Normal")),
                   beta=gl(4,length(x1),
                       labels=c(1,1.5,2,"Normal")))

dens <- ggplot(data, aes(x=value, y=density, color=m, linetype=beta))+
  geom_line()+
  theme(legend.position="right", legend.box="vertical")+
  guides(color=FALSE)+
  scale_color_manual(values=c("#E7B800","#2E9FDF","#FC4E07","black"))
ecdf <- ggplot(data, aes(x=value, y=cum_dens, color=m, linetype=beta))+
  geom_line()+
  labs(y="Fn(x)")+
  theme(legend.position="right", legend.box="vertical")+
  guides(linetype=FALSE)+
  scale_color_manual(values=c("#E7B800","#2E9FDF","#FC4E07","black"))

ggarrange(dens, ecdf, nrow=2, ncol=1, labels=c("a)","b)"))
```

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{EnvStat_files/figure-latex/dcauchyvis-1} 

}

\caption{Visualisasi distribusi t dengan variasi m dan beta a) density plot, b)ecdf}(\#fig:dcauchyvis)
\end{figure}

Pada `R`, fungsi utama yang digunakan untuk menghitung probabilitas distribusi Cauchy adalah `dcauchy()` dan `pcauchy()` (probabilitas kumulatif). Format fungsi tersebut adalah sebagai berikut:


```r
dcauchy(x, location = 0, scale = 1)
pcauchy(q, location = 0, scale = 1, lower.tail = TRUE)
```

> **Note: **
>
> - **x,p**: vektor numerik atau kuantil.
> - **location**: median.
> - **scale**: beta.
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE.

### Distribusi Logistik

Distribusi logistik sering diterapkan untuk memodelkan pertumbuahan populasi berdasarkan asumsi tertentu seperti keterbatasan lahan atau ruang atau bahkan makanan. Fungsi densitas probabilitas distribusi logistik disajikan pada Persamaan \@ref(eq:dlogistik).

\begin{equation}
   f\left(x;\mu,\sigma\right)=\frac{1}{\sigma}\exp\left(-\frac{x-\mu}{\sigma}\right)\left[1+\exp\left(-\frac{x-\mu}{\sigma}\right)\right]^{-2},\ \ \ \ \ \ \ \ -\infty<x<\infty
  (\#eq:dlogistik)
\end{equation}

Pada Gambar \@ref(fig:dlogistikvis) disajikan visualisasi distribusi Cauchy dengan variasi $m$ dan $\beta$.


```r
x <- seq(-7,7, length=100)
x1 <- dlogis(x, location=0, scale=1); x1_cum <- cumsum(x1)/max(cumsum(x1))
x2 <- dlogis(x, location=0.5, scale=1.5); x2_cum <- cumsum(x2)/max(cumsum(x2))
x3 <- dlogis(x, location=1, scale=2); x3_cum <- cumsum(x3)/max(cumsum(x3))
x4 <- dnorm(x); x4_cum <- cumsum(x4)/max(cumsum(x4))

data <- data.frame(value=c(x,x,x,x),
                   density=c(x1,x2,x3,x4),
                   cum_dens=c(x1_cum,x2_cum,x3_cum,x4_cum),
                   mean=gl(4,length(x1),
                       labels=c(0,1,1.5,"Normal")),
                   sd=gl(4,length(x1),
                       labels=c(1,1.5,2,"Normal")))

dens <- ggplot(data, aes(x=value, y=density, color=mean, linetype=sd))+
  geom_line()+
  theme(legend.position="right", legend.box="vertical")+
  guides(color=FALSE)+
  scale_color_manual(values=c("#E7B800","#2E9FDF","#FC4E07","black"))
ecdf <- ggplot(data, aes(x=value, y=cum_dens, color=mean, linetype=sd))+
  geom_line()+
  labs(y="Fn(x)")+
  theme(legend.position="right", legend.box="vertical")+
  guides(linetype=FALSE)+
  scale_color_manual(values=c("#E7B800","#2E9FDF","#FC4E07","black"))

ggarrange(dens, ecdf, nrow=2, ncol=1, labels=c("a)","b)"))
```

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{EnvStat_files/figure-latex/dlogistikvis-1} 

}

\caption{Visualisasi distribusi logistik dengan variasi mean dan simpangan baku, a) density plot, b)ecdf}(\#fig:dlogistikvis)
\end{figure}

Pada `R`, fungsi utama yang digunakan untuk menghitung probabilitas distribusi Logistik adalah `dlogis()` dan `plogis()` (probabilitas kumulatif). Format fungsi tersebut adalah sebagai berikut:


```r
dlogis(x, location = 0, scale = 1)
plogis(q, location = 0, scale = 1, lower.tail = TRUE)
```

> **Note: **
>
> - **x,p**: vektor numerik atau kuantil.
> - **location**: mean.
> - **scale**: simpangan baku
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE.

### Distribusi Weibull

Distribusi lain yang digunakan secara intensif selain distribusi gamma dan eksponensial untuk memperkirakan probabilitas kegagalan suatu proses adalah distribusi Weibull. Fungsi densitas probabilitas distribusi Weibull disajikan pada Persamaan \@ref(eq:dweibull).

\begin{equation}
f\left(x;\alpha,\beta \right) =
  \begin{cases}
    f\left(x;\alpha,\beta\right)=\frac{\alpha}{\beta}\left(\frac{x}{\beta}\right)^{\alpha-1}\exp\left(\frac{x}{\beta}\right)^{\alpha}     & \quad x>0\\
    0                   & \quad\text{}
    \end{cases}
 (\#eq:dweibull)
\end{equation} 

Pada Gambar \@ref(fig:weibullvis) disajikan visualisasi distribusi gamma dengan variasi $\alpha$ dan $\beta$.


```r
x <- seq(0,6, length=100)
x1 <- dweibull(x, shape=1, scale=1); x1_cum <- cumsum(x1)/max(cumsum(x1)) 
x2 <- dweibull(x, shape=2, scale=1); x2_cum <- cumsum(x2)/max(cumsum(x2))
x3 <- dweibull(x, shape=4, scale=1); x3_cum <- cumsum(x3)/max(cumsum(x3))

data <- data.frame(value=c(x,x,x),
                   density=c(x1,x2,x3),
                   cum_dens=c(x1_cum,x2_cum,x3_cum),
                   alpha=gl(3,length(x1),
                       labels=c(1,2,4)))

dens <- ggplot(data, aes(x=value, y=density, color=alpha))+
  geom_line()+
  scale_color_manual(values=c("#E7B800","#2E9FDF","#FC4E07")
)
ecdf <- ggplot(data, aes(x=value, y=cum_dens, color=alpha))+
  geom_line()+
  labs(y="Fn(x)")+
  scale_color_manual(values=c("#E7B800","#2E9FDF","#FC4E07")
)

ggarrange(dens, ecdf, nrow=1, ncol=2, labels=c("a)","b)"))
```

\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{EnvStat_files/figure-latex/weibullvis-1} 

}

\caption{Visualisasi distribusi weibull dengan variasi alpha dengan beta 1 a) density plot, b)ecdf}(\#fig:weibullvis)
\end{figure}

Pada `R` probabilitas distribusi Weibull dapat dihitung menggunakan fungsi `dweibull()` dan `pweibull()` (probabilitas kumulatif). Format fungsi tersebut adalah sebagi berikut:


```r
dweibull(x, shape, scale)
pweibull(q, shape, scale, lower.tail = TRUE)
```

> **Note: **
>
> - **x,p**: vektor numerik atau kuantil
> - **shape**: nilai alpha
> - **scale**: niali beta
> - **lower.tail**: probabilitas dihitung dari ujung bawah. Nilai yang mungkin adalah TRUE atau FALSE.

## Referensi

1. Chi Yau. 2014. **R Tutorial with Bayesian Statistics Using OpenBUGS**. Amazon Kindle
2. Damanhuri, E. 2011. **Statitika Lingkunga**. Penerbit ITB.
3. Janicak, C.A. 2007. **Applied Statistics in Occupational Safety and Health**. Government Institutes.
4. Kerns, G.Jay. 2018. **Introduction to Probability and Statistics Using R Third Edition**. GNU Free Documentation License.
5. King, William B. **PROBILITY DISTRIBUTIONS, QUANTILES, CHECKS FOR NORMALITY**. <http://ww2.coastal.edu/kingw/statistics/R-tutorials/prob.html>.
6. Ofungwu, J. 2014. **Statistical Applications For Environmental Analysis and Risk Assessment**.  John Wiley & Sons, Inc.
7. Quick-R. **Probability Plots **. <https://www.statmethods.net/advgraphs/probability.html>
8. STAT TREK. **Binomial Probability Distribution**.<https://stattrek.com/probability-distributions/binomial.aspx?tutorial=prob>.
9. ____.**Hypergeometric Distribution**. <https://stattrek.com/probability-distributions/hypergeometric.aspx?tutorial=prob>.
10. ____. **Multinomial Distribution**. <https://stattrek.com/probability-distributions/multinomial.aspx?tutorial=prob>.
11. ____. **Negative Binomial Distribution**. <https://stattrek.com/probability-distributions/negative-binomial.aspx?tutorial=prob>.
12. ____. **Poisson Distribution**. <https://stattrek.com/probability-distributions/poisson.aspx?tutorial=prob>.
13. UBC. **Probability DIstribution**. <https://www.zoology.ubc.ca/~schluter/R/probability/>.
14. Walpole, E. R., Myers, H.M., Myers, S.L., Keying Ye. 2011. **Probability $ Statistics for Engineering & Scientists Ninth Edition**. Prentice Hall.







<!--chapter:end:09-distribusi-probabilitas.Rmd-->

# (PART\*) Statistika Inferensial - R {-}

<style>
body{
text-align: justify}
</style>

# Penaksiran Secara Statistika

Pada Chapter 6-Ringkasan Numerik kita telah belajar beberapa atribut kunci dari data seperti $\overline{X}$ dan $s$. Kedua nilai tersebut disebut sebagai nilai estimasi sampel dari populasi (untuk mean $\mu$ dan simpangan baku $\sigma$). Pada Chapter ini kita akan melakukan eksplorasi lebih jauh lagi mengenai interval estimasi (*interval estimate*) yang akan menyinggung kedua nilai tersebut lebih jauh.

## Definisi Interval Estimasi

Median sampel dan mean sampel menyatakan titik pemusatan data. Estimasi menggunakan kedua nilai tersebut disebut sebagai estimasi titik (*point estimation*). Estimasi titik sendiri tidak menggambarkan reliabilitas  atau kurangnya reliabilitas (variabilitas) dari estimasi ini. Sebagai contoh, anggaplah terdapat dua data X dan Y dengan mean 5 dengan jumlah observasi yang sama. Data Y memiliki nilai mean 5 dengan sangat sedikit variasi didalamnya, sedangkan data X jauh lebih bervariasi. Perkiraan titik 5 untuk X jauh lebih tidak dapat diandalkan dibandingkan dengan untuk Y karena variabilitas yang lebih besar dalam data X. Dengan kata lain, lebih banyak kehati-hatian diperlukan ketika menyatakan bahwa 5 memperkirakan mean populasi sebenarnya X daripada ketika menyatakan ini untuk Y. Melaporkan hanya perkiraan mean sampel (poin) 5 gagal memberikan petunjuk tentang perbedaan ini.

Sebagai alternatif untuk estimasi titik, estimasi interval adalah interval yang memiliki probabilitas yang dinyatakan mengandung nilai populasi sebenarnya. interval lebih lebar untuk set data yang memiliki variabilitas lebih besar. Jadi dalam contoh di atas, interval antara 4,7 dan 5,3 mungkin memiliki kemungkinan 95% untuk mengandung mean populasi Y yang sebenarnya (tidak diketahui). Butuh interval yang jauh lebih luas, katakanlah antara 2,0 dan 8,0, untuk memiliki probabilitas yang sama untuk mengandung rerata sebenarnya dari X. Karena itu, perbedaan keandalan dari dua estimasi dengan jelas dinyatakan menggunakan estimasi interval. Estimasi interval dapat memberikan dua informasi yang estimasi poin tidak dapat berikan, antara lain:

1. Pernyataan probabilitas atau kemungkinan bahwa interval berisi nilai populasi sebenarnya (keandalannya).
2. Pernyataan kemungkinan bahwa satu titik data dengan besaran tertentu berasal dari populasi yang diteliti.

Estimasi interval untuk poin pertama disebut sebagai interval kepercayaan (*confidence interval*), sedangkan yang kedua disebut sebagai interval prediksi (*prediction interal*). Meskipun salin terkait, pembaca perlu berhati-hati sebab kedua definisi tersebut sering kali tertukar satu sama lain.

## Interpretasi Interval Estimasi

Untuk lebih memahami mengenai definisi interval estimasi pada sub-chapter ini akan diberikan contoh yang diambil dari buku **statistical Methods in Water Resources** karya Helsel dan Hirsch (2012). Misalkan mean populasi sebenarnya $\mu$ konsentrasi dalam akuifer adalah 10. Sleain itu, anggaplah bahwa varians populasi sebenarnya $\sigma^2$ sama dengan 1. Karena nilai-nilai ini dalam praktiknya tidak pernah diketahui, sampel diambil untuk memperkirakannya dengan mean sampel $x$ dan sampel varian $s^2$ . Dana yang cukup tersedia untuk mengambil 12 sampel air (kira-kira satu per bulan) selama satu tahun, dan hari-hari di mana pengambilan sampel terjadi dipilih secara acak. Dari 12 sampel ini $x$x dan $s^2$ dihitung. Meskipun pada kenyataannya hanya satu set 12 sampel akan diambil setiap tahun, menggunakan komputer 12 hari dapat dipilih beberapa kali untuk menggambarkan konsep perkiraan interval. Untuk masing-masing dari 10 set independen dari 12 sampel, interval kepercayaan pada mean dihitung dengan menggunakan persamaan yang diberikan pada Tabel \@ref(tab:iie) dan Gambar \@ref(fig:iievis).

**No.** | **N** | **Mean** | **St.Dev** | **90% Interval kepercayaan**
--------|-------|----------|------------|--------------------------
1       | 12    | 10,06    | 1,11       | 9,46 sampai 10,64
2       | 12    | 10,60    | 0,81       | $^+$ 10,18 sampai 11,02
3       | 12    | 9,95     | 1,26       | 9,29 sampai 10,60
4       | 12    | 10,18    | 1,26       | 9,52 sampai 10,83
5       | 12    | 10,17    | 1,33       | 9,48 sampai 10,85
6       | 12    | 10,22    | 1,19       | 9,60 sampai 10,84
7       | 12    | 9,71     | 1,51       | 8,92 sampai 10,49
8       | 12    | 9,90     | 1,01       | 9,38 sampai 10,43
9       | 12    | 9,95     | 0.10       | 9,43 sampai 10,46
10      | 12    | 9,88     | 1,37       | 9,17 sampai 10,59

: (\#tab:iie) Sepuluh  interval kepercayaan 90% sekitar nilai mean sebenarnya sebesar 10 (Data berdistribusi normal dan Tanda plus menyatakan data tidak disertakan dalam nilai mean sebenarnya)

Kesepuluh interval pada contoh di atas disebut dengan dengan **interval kepercayaan 90%** dari nilai mean sesungguhnya. Nilai mean sebenarnya akan terdapat pada interval tersebut dengan probabilitas 90%. Sehingga berdasarkan Tabel \@ref(tab:iie) terdapat 9 interval yang memiliki nilai mean sesungguhnya didalamnya (probabilitas 90%). Jika kita sekali lagi melakukan sampling dengan jumlah sampling yang sama pada interval nilai baru yang dihasilkan akan mengandung nilai mean sesungguhnya dan dapat juga tidak. Probabilitas interval tersebut mengandung nilai mean sesungguhnya disebut sebagai **tingkat kepercayaan** (*confidence level*). Probabilitas nilai interval tidak mengandung mean sesungguhnya disebut sebagai **alpha level** ($\alpha$) yang ditulis berdasarkan Persamaan \@ref(eq:alpha).

\begin{equation}
  \alpha=1-confidence\ level\ 
  (\#eq:alpha)
\end{equation}

Lebar interval kepercayaan adalah fungsi dari bentuk distribusi data (variabilitas dan kemencengannya), ukuran sampel, dan tingkat kepercayaan yang diinginkan. Ketika tingkat kepercayaan meningkat, lebar interval juga meningkat, karena interval yang lebih besar lebih mungkin mengandung nilai sebenarnya daripada interval yang lebih pendek. Dengan demikian interval kepercayaan 95% akan lebih luas daripada interval 90% untuk data yang sama.

\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{iievis} 

}

\caption{Sepuluh interval kepercayaan 90 persen data dengan nilai mean sebenarnya 10 (Helsel dan Hirsch, 2002)}(\#fig:iievis)
\end{figure}

Interval kepercayaan simetris pada rata-rata biasanya dihitung dengan asumsi data mengikuti distribusi normal. Jika tidak, distribusi rerata itu sendiri akan mendekati normal sepanjang ukuran sampel besar (katakanlah 50 pengamatan atau lebih besar). Interval kepercayaan dengan asumsi normalitas kemudian akan memasukkan mean sebenarnya ($1-\alpha$)% dari waktu. Dalam contoh di atas, data dihasilkan dari distribusi normal, sehingga ukuran sampel kecil 12 tidak menjadi masalah. Namun ketika data memiliki kemencengan dan ukuran sampel di bawah 50 atau lebih, interval kepercayaan simetris tidak akan mengandung rata-rata ($1-\alpha$)% sepanjang waktu. Dalam contoh di bawah ini, interval kepercayaan simetris secara salah dihitung untuk data yang miring (Gambar \@ref(fig:iiedata)). Hasil (Gambar \@ref(fig:iievis2) dan Tabel \@ref(tab:iie2)) menunjukkan bahwa interval kepercayaan kehilangan nilai sebenarnya dari 1 lebih sering daripada yang seharusnya. Semakin besar skewness, semakin besar ukuran sampel harus sebelum interval kepercayaan simetris dapat diandalkan. Sebagai alternatif, interval kepercayaan asimetris dapat dihitung untuk situasi umum data yang memiliki kemencengan. 


**No.** | **N** | **Mean** | **St.Dev** | **90% Interval kepercayaan**
--------|-------|----------|------------|--------------------------
1       | 12    | 0,784    | 0,320      | $^+$ 0,618 sampai 0,950
2       | 12    | 0,811    | 0,299      | $^+$ 0,656 sampai 0,966
3       | 12    | 1,178    | 0,700      | 0,815 sampai 1,541
4       | 12    | 1,030    | 0,459      | 0,792 sampai 1,267
5       | 12    | 1,079    | 0,573      | 0,782 sampai 1,376
6       | 12    | 0,833    | 0,363      | 0,644 sampai 1,021
7       | 12    | 0,789    | 0,240      | $^+$ 0,644 sampai 0,913
8       | 12    | 1,159    | 0,815      | 0,736 sampai 1,581
9       | 12    | 0,822    | 0,365      | $^+$ 0,633 sampai 0,992
10      | 12    | 0,837    | 0,478      | 0,589 sampai 1,085

: (\#tab:iie2) Sepuluh  interval kepercayaan 90% sekitar nilai mean sebenarnya sebesar 1 (Data tidak berdistribusi normal dan Tanda plus menyatakan data tidak disertakan dalam nilai mean sebenarnya)

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{iiedata} 

}

\caption{Histogram data dengan nilai mean populasi 1 dan simpangan baku populasi 0.75 (Helsel dan Hirsch, 2002)}(\#fig:iiedata)
\end{figure}


\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{iievis2} 

}

\caption{Sepuluh interval kepercayaan 90 persen data dengan nilai mean sebenarnya  (Helsel dan Hirsch, 2002)}(\#fig:iievis2)
\end{figure}

## Interval Kepercayaan Median

Interval kepercayaan median populasi dapat dihitung tanpa perlu mengikuti asumsi distribusi tertentu. Sehingga nilai median dapat digunakan untuk memperkirakan nilai pusat data untuk distribusi data yang tidak berdistribusi normal.

### Interval Estimasi Median Metode Nonparametrik

Interval estimasi nonparametrik untuk median populasi sebenarnya dihitung menggunakan distribusi binomial. Pertama, tingkat signifikansi yang diinginkan $\alpha$ dinyatakan, error yang dapat diterima tidak termasuk median yang sebenarnya. Satu-setengah ($\alpha/2$) dari error ini digunakan untuk setiap akhir interval (Gambar \@ref(fig:iemednp)). Tabel distribusi binomial memberikan nilai kritis bawah dan atas $x'$ dan $x$ pada setengah tingkat alfa yang diinginkan ($\alpha/2$). Nilai-nilai kritis ini ditransformasikan ke dalam rangking $R_l$ dan $R_u$ yang sesuai dengan titik data $C_l$ dan $C_u$ di ujung interval kepercayaan.

\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{iemednp} 

}

\caption{Probabilitas median populasi P50 pada dua sisi interval estimasi (Helsel dan Hirsch, 2002)}(\#fig:iemednp)
\end{figure}

Untuk ukuran sampel kecil, tabel binomial dimasukkan pada kolom p = 0,5 (median) untuk menghitung interval kepercayaan pada median.  Nilai kritis $x'$ diperoleh dari tabel distribusi binomial yang sesuai dengan $\alpha/2$, atau sedekat mungkin dengan $\alpha/2$. Nilai kritis ini kemudian digunakan untuk menghitung peringkat $R_u$ dan $R_l$ yang sesuai dengan nilai data pada batas kepercayaan atas dan bawah untuk median. Batas-batas ini adalah titik data peringkat $R_l$th yang masuk dari setiap ujung daftar n  observasi. Interval kepercayaan yang dihasilkan akan mencerminkan bentuk (menceng atau simetris) dari data asli.

\begin{equation}
  R_l=x'+1 
  (\#eq:rl)
\end{equation}

\begin{equation}
  R_u=n-x'=x\ untuk\ x'\ dan\ x\ dari\ tabel\ dist.\ binomial 
  (\#eq:ru)
\end{equation}

Interval nonparametrik tidak selalu dapat secara tepat menghasilkan tingkat kepercayaan yang diinginkan ketika ukuran sampel kecil. Ini karena mereka terpisah, melompat dari satu nilai data ke yang berikutnya di ujung interval. Namun, tingkat kepercayaan yang dekat dengan yang diinginkan tersedia untuk semua kecuali ukuran sampel terkecil.

Untuk lebih memahaminya diberikan data 25 pengukuran konsentrasi arsenin di air tanah dalam ppb yang disajikan pada Tabel \@ref(tab:gwardat).

\begin{table}[t]

\caption{(\#tab:gwardat)Konsentrasi Arsenik dalam air tanah (ppb)}
\centering
\begin{tabular}{r|r}
\hline
observasi & konsentrasi\\
\hline
1 & 1.3\\
\hline
2 & 1.5\\
\hline
3 & 1.8\\
\hline
4 & 2.6\\
\hline
5 & 2.8\\
\hline
6 & 3.5\\
\hline
7 & 4.0\\
\hline
8 & 4.8\\
\hline
9 & 8.0\\
\hline
10 & 9.5\\
\hline
11 & 12.0\\
\hline
12 & 14.0\\
\hline
13 & 19.0\\
\hline
14 & 23.0\\
\hline
15 & 41.0\\
\hline
16 & 80.0\\
\hline
17 & 100.0\\
\hline
18 & 110.0\\
\hline
19 & 120.0\\
\hline
20 & 190.0\\
\hline
21 & 240.0\\
\hline
22 & 250.0\\
\hline
23 & 300.0\\
\hline
24 & 340.0\\
\hline
25 & 580.0\\
\hline
\end{tabular}
\end{table}

Visualisasi Tabel \@ref(tab:gwardat) ditunjukkan pada Gambar \@ref(fig:gwardatvis). Berdasarkan gambar tersebut terlihat bahwa data memiliki kemencengan yang positif sehingga penaksiran rata-rata populasi menggunakan nilai mean tidak dapat dilakukan.

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gwardatvis-1} 

}

\caption{Distribusi konsentrasi arsenik dalam air tanah}(\#fig:gwardatvis)
\end{figure}

Berdasarkan data pada Tabel \@ref(tab:gwardat), median konsentrasi arsenik $\hat{C}_{0.5}$=19 yang berada pada urutan data ke-13 dari data yang telah diurutkan dari yang terkecil ke yang terbesar. Untuk menentukan interval kepercayaan 95% median kosentrasi arsenik $C_{0.5}$, nilai kritis berdasarkan nilai error mendekati $\alpha/2$=0,025 adalah $x'$=7. Untuk lebih memahaminya pembaca dapat mengunduh tabel distribusi binomial pada laman [berikut](https://onlinepubs.trb.org/onlinepubs/nchrp/cd-22/manual/v2appendixc.pdf). Nilai $x'$=7 diperoleh menggunakan Tabel distribusi binomial dengan $n$=25 dan $p$=0,5 yang ditampilkan pada Gambar \@ref(fig:tabbinom) dengan nilai probabilitas sebesar 0,022 (mendekati 0,025) yang setara dengan area yang diarsir pada Gambar \@ref(fig:iemednp).

\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{tabbinom} 

}

\caption{Lokasi probabilitas x berdasarkan tabel distribusi binomial}(\#fig:tabbinom)
\end{figure}

Berdasarkan Persamaan \@ref(eq:rl) dan Persamaan \@ref(eq:ru), rangking $R_l$ pada observasi yang menyatakan batas kepercayaan bawah (*lower confidence limit*) adalah 8 ($R_i$=7+1) dan $R_u$ yang menyatakan batas kepercayaan atas (*upper confidence level*) adalah 25-7=18. Berdasarkan nilai probabilitas $x'$=0,022, maka nilai alpha yang sesunggunya sebesar $\alpha=2*0,022=0,044$. Nilai tersebut setara dengan tingkat kepercayaan $1-0,044$ atau 95,6%. Nilai interval kepercayaan median antara observasi ke-8 dan 18 adalah $C_l=4,8\le C_{0.5}\le110=C_u\ \ pada\ \alpha=0,044$. Nilai asimetrik disekitar $\hat{C}_{0.5}$=19 mencerminkan kemencengan pada data.

Jika pembaca ingin melakukan perhitungan pada `R`, pembaca harus membuat fungsi sebagai berikut:


```r
med_npCI <- function(x,alpha){
  # mengurutkan data
  x_sort=sort(x)
  # menghitung jumlah observasi
  n=length(x)
  # menghitung median data
  med = median(x, na.rm=TRUE)
  # loop untuk mencari nilai probabilitas terdekat
  # dengan alpha
  for(i in 1:n){
    b = pbinom(i,n,0.5)
    if(b>alpha/2){
      break
    }
  }
  # mengambil x'
  x_i=i-1
  # menghitung Rl dan Ru
  rl=x_i+1
  ru=n-x_i
  # menghitung true confidence level
  CL=1-2*(pbinom(x_i,n,0.5))
  # menghitung Lower dan Upper CL
  LCL=x_sort[rl]
  UCL=x_sort[ru]
  # menggabungkannya dalam satu data
  data=data.frame("median"=med,
                  "True CL %"=CL*100,
                  "Lower CL"=LCL,
                  "Upper CL"=UCL)
  return(data)
}
```

> **Note: **
>
> - **x**: vektor numerik
> - **alpha**: alpha level yang digunakan

Fungsi yang telah dibuat tersebut selanjutnya dapat pembaca gunakan saat akan menghitung interval kepercayaan median populasi menggunakan metode Nonparametrik. Berikut penerapannya menggunakan data pada Tabel \@ref(tab:gwardat) yang telah disimpan kedalam objek `gwardat`.


```r
med_npCI(x=gwardat$konsentrasi, alpha=0.05)
```

```
##   median True.CL.. Lower.CL Upper.CL
## 1     19     95.67      4.8      110
```

Alternatif lain yang dapat digunakan untuk menghitung interval kepercayaan jika sampel cukup besar n>20 menggunakan metode Nonparametrik adalah dengan menggunakan pendekatan tabel distribusi normal untuk memperkirakan distribusi binomial. Dengan menggunakan pendekatan ini, hanya sebagian kecil tabel distribusi binomial (n=20) yang diperlukan untuk melakukannya. Nilai kritis $z_{\alpha/2}$ dari tabel distribusi normal menentukan rangking atas dan  bawah observasi yang menyatakan awal dan akhir nilai interval kepercayaan yang dinyatakan pada Persamaan \@ref(eq:rlz) dan Persamaan \@ref(eq:ruz). Pembulatan diperlukan dalam proses ini sebab nilai ranking harus berupa integer.

\begin{equation}
  R_l=\frac{n-z_{\frac{\alpha}{2}}\cdot\sqrt{n}}{2} 
  (\#eq:rlz)
\end{equation}

\begin{equation}
   R_l=\frac{n-z_{\frac{\alpha}{2}}\cdot\sqrt{n}}{2}+1
  (\#eq:ruz)
\end{equation}

Menggunakan contoh data pada Tabel \@ref(tab:gwardat), dengan 95% interval kepercayaan ($z_{\alpha/2}$=1,96) median dapat dihitung seperti berikut:

$$
  R_l=\frac{25-1,96\cdot\sqrt{25}}{2}=7,6 
$$

$$
  R_l=\frac{25+1,96\cdot\sqrt{25}}{2}+1=18,4 
$$

Berdasarkan hasil perhitungan diperoleh rangking bawah adalah data ke-8 dan rangking atas adalah 18. Kedua data dibulatkan berdasarkan integer terdekat. Nilai interval kepercayaan median yang diperoleh sama dengan metode sebelumnya sebab rangking batas bawah dan atasnya yang seragam.

Jika pembaca ingin menggunakan `R`, maka fungsi yang sebelumya telah kita buat dapat dimodifikasi seperti berikut:


```r
med_norCI <- function(x, alpha){
  # mengurutkan data dari yang terkecil
  x_sort=sort(x)
  # menghitung jumlah observasi
  n = length(x)
  # menghitung median data
  med = median(x, na.rm=TRUE)
  # menghitung Rl dan Ru
  rl=round((n-abs(qnorm(alpha/2))*sqrt(n))/2,0)
  ru=round(((n+abs(qnorm(alpha/2))*sqrt(n))/2)+1,0)
  # menghitung Lower dan Upper CL
  LCL=x_sort[rl]
  UCL=x_sort[ru]
  # menggabungkannya dalam satu data
  data=c("median"=med,
                  "Lower CL"=LCL,
                  "Upper CL"=UCL)
  data
}
```

Fungsi `med_norCI()` sama dengan fungsi `med_npCI()`. Perbedaannya terletak pada penggunaan distribusi normal pada proses penentuan titik kritisnya.

Dengan menggunakan fungsi `med_norCI()`, rentang kepercayaan median dapat dihitung seperti berikut:

> **Note: **
>
> - **x**: vektor numerik
> - **alpha**: alpha level yang digunakan


```r
med_norCI(x=gwardat$konsentrasi, alpha=0.05)
```

```
##   median Lower CL Upper CL 
##     19.0      4.8    110.0
```

Jika kita ingin menghitung interval estimasi median masing-masing kolom data frame kita pasti akan mencopy fungsi tersebut dan menjalankannya satu persatu. Metode lain untuk mengefektifkan proses tersebut adalah dengan menggunakan for loop, apply function dan map function. Metode-metode tersebut telah kita bahas pada chapter sebelumnya. Pada Chapter ini penulis akan memberikan contohnya satu-persatu. Berikut adalah contoh sintaks apply dan map function untuk melakukannya:


```r
# menggunakan sapply
sapply(X=airquality, FUN=med_norCI, alpha=0.05)
```

```
##          Ozone Solar.R Wind Temp Month Day
## median    31.5     205  9.7   79     7  16
## Lower CL  35.0     190  9.2   77     7  13
## Upper CL  65.0     236 10.3   81     7  18
```

```r
# menggunakan map function
library(purrr)
map(.x=airquality, .f=med_norCI, alpha=0.05)
```

```
## $Ozone
##   median Lower CL Upper CL 
##     31.5     35.0     65.0 
## 
## $Solar.R
##   median Lower CL Upper CL 
##      205      190      236 
## 
## $Wind
##   median Lower CL Upper CL 
##      9.7      9.2     10.3 
## 
## $Temp
##   median Lower CL Upper CL 
##       79       77       81 
## 
## $Month
##   median Lower CL Upper CL 
##        7        7        7 
## 
## $Day
##   median Lower CL Upper CL 
##       16       13       18
```


Jika kita tidak ingin menggunakan vektor dalam fungsi, kita dapat juga menggunakan data frame sebagai inputnya. Kelebihannya adalah kita dapat menghitung rentang kepercayaan seluruh kolom dalam satu kali proses. Hal ini tentunya akan menghemat waktu yang digunakan. Berikut adalah contoh sintaks fungsi untuk menghitung interval kepercayaan median menggunakan distribusi normal dengan metode nonparametrik yang digunakan:


```r
med_norCI <- function(df, alpha){
  # membuat matrik untuk menyimpan
  # hasil loop
  med = rep(NA, ncol(df))
  LCL = rep(NA, ncol(df))
  UCL = rep(NA, ncol(df))
  var = rep(NA, ncol(df))
  # looping
  for(i in 1:ncol(df)){
    # mengurutkan data
    x_sort = sort(df[, i])
    # mengambil nama kolom dataset
    var[i] = colnames(df[i])
    # menghitung jumlah observasi
    n = length(x_sort)
    # menghitung median data
    med[i] = median(x_sort, na.rm=TRUE)
    # menghitung Lower dan Upper CL
    LCL[i]=x_sort[(round((n-abs(qnorm(alpha/2))*sqrt(n))/2,0))]
    UCL[i]=x_sort[(round(((n+abs(qnorm(alpha/2))*sqrt(n))/2)+1,0))]
  }
  # menggabungkannya dalam satu data
  data=data.frame("variabel"=var,
                  "median"=med,
                  "Lower CL"=LCL,
                  "Upper CL"=UCL)
  data
}
```

> **Note: **
>
> - **df**: data frame
> - **alpha**: alpha level yang digunakan

Fungsi tersebut dapat menghitung sekaligus Interval kepercayaan median dengan metode nonparametrik. Pembaca dapat mencobanya dengan menggunakan dataset yang pembaca miliki. Pembaca dapat mengabaikan peringatan yang muncul dan berfokus pada hasil yang diperoleh. Sebagai contoh jalankan fungsi tersebut menggunakan dataset `airquality` berikut:


```r
med_norCI(df=airquality, alpha=0.05)
```

```
##   variabel median Lower.CL Upper.CL
## 1    Ozone   31.5     23.0     39.0
## 2  Solar.R  205.0    187.0    225.0
## 3     Wind    9.7      9.2     10.3
## 4     Temp   79.0     77.0     81.0
## 5    Month    7.0      7.0      7.0
## 6      Day   16.0     13.0     18.0
```



### Metode Parametrik Interval Estimasi Median

Telah dijelaskan pada chapter 6 bahwa rata-rata geometrik  merupakan merupakan nilai rata-rata yang digunakan untuk mengestimasi median sampel untuk data yang memiliki kemencengan dengan transformasi yang digunakan agar data simetris adalah transformasi logaritmik $y=\ln(x)$. Pada metode ini data diasumsikan memiliki distribusi lognormal (kemencengan positif). Rerata dan interval geometris akan lebih efisien (interval lebih pendek) dari median dan interval kepercayaannya ketika data benar-benar lognormal. Median sampel dan intervalnya lebih tepat dan lebih efisien jika logaritma data masih menunjukkan kemencengan dan/atau *outlier*. Estimasi media menggunakan metode parametrik dituliskan kedalam Persamaan \@ref(eq:gmci) dan Persamaan \@ref(eq:gmci2).

\begin{equation}
  GM_x=\exp\left(\overline{y}\right) 
  (\#eq:gmci)
\end{equation}

dimana $y=\ln(x)$ dan $\overline{y}$=mean sampel $y$.

\begin{equation}
  \exp\left(\overline{y}-t_{\left(\frac{\alpha}{2},n-1\right)}\sqrt{\frac{s_y^2}{n}}\right)\le GM_x\le\exp\left(\overline{y}+t_{\left(\frac{\alpha}{2},n-1\right)}\sqrt{\frac{s_y^2}{n}}\right) 
  (\#eq:gmci2)
\end{equation}

dimana $s_{y}^2$= varians sampel y pada unit log natural.

Pada Tabel \@ref(tab:gwardat), untuk menghitung interval keyakinan median menggunakan pendekatan mean geometrik $GM_x$ kita perlu mentransformasi datanya terlebih dahulu sehingga menjadi bentuk natural log. hasil transformasi disajikan pada Tabel \@ref(tab:gwardat2).

\begin{table}[t]

\caption{(\#tab:gwardat2)Tranformasi logaritmik konsentrasi Arsenik dalam air tanah (ppb)}
\centering
\begin{tabular}{r|r}
\hline
observasi & konsentrasi\\
\hline
1 & 0.2624\\
\hline
2 & 0.4055\\
\hline
3 & 0.5878\\
\hline
4 & 0.9555\\
\hline
5 & 1.0296\\
\hline
6 & 1.2528\\
\hline
7 & 1.3863\\
\hline
8 & 1.5686\\
\hline
9 & 2.0794\\
\hline
10 & 2.2513\\
\hline
11 & 2.4849\\
\hline
12 & 2.6391\\
\hline
13 & 2.9444\\
\hline
14 & 3.1355\\
\hline
15 & 3.7136\\
\hline
16 & 4.3820\\
\hline
17 & 4.6052\\
\hline
18 & 4.7005\\
\hline
19 & 4.7875\\
\hline
20 & 5.2470\\
\hline
21 & 5.4806\\
\hline
22 & 5.5215\\
\hline
23 & 5.7038\\
\hline
24 & 5.8289\\
\hline
25 & 6.3630\\
\hline
\end{tabular}
\end{table}

visualisasi distribusi yang baru disajikan pada Gambar \@ref(fig:gwardatvis2).

\begin{figure}

{\centering \includegraphics[width=0.7\linewidth]{EnvStat_files/figure-latex/gwardatvis2-1} 

}

\caption{Distribusi logaritmik konsentrasi arsenik dalam air tanah}(\#fig:gwardatvis2)
\end{figure}

Nilai mean dari data tersebut adalah 3,17 dengan simpangan baku sebesar 1,96. Berdasarkan Gambar \@ref(fig:gwardatvis2), kita telah memperoleh distribusi yang simetris.

Dengan menggunakan Persamaan \@ref(eq:gmci) dan Persamaan \@ref(eq:gmci2) selanjutnya dapat dihitung interval kepercayaannya dengan derajat kepercayaan 95%.

$$
  GM_x=\exp\left(3,17\right)=23,8
$$

$$
  \exp\left(3.17-2,064\cdot\sqrt{\frac{1.96^2}{25}}\right)\le GM_x\le\exp\left(3.17-2,064\cdot\sqrt{\frac{1.96^2}{25}}\right)
$$

$$
  \exp\left(2,36\right)\le GM_x\le\exp\left(3,98\right)
$$

$$
  10,6\le GM_x\le53,5
$$

Dengan menggunakan `R` dapat dikerjakan menggunakan fungsi sebagai berikut:


```r
med_gm <- function(x, alpha){
  x = log(x)
  # rata-rata geometrik
  gm = exp(mean(x, na.rm=TRUE))
  # menghitung derajat kebebasan
  df = length(x)-1
  # menghitung batas bawah dan atas
  LCL = exp(mean(x, na.rm=TRUE)-qt(1-alpha/2,df)*sqrt(var(x, na.rm=TRUE)/length(x)))
  UCL = exp(mean(x, na.rm=TRUE)+qt(1-alpha/2,df)*sqrt(var(x, na.rm=TRUE)/length(x)))
  # menggabungkan hasil
  data=c("GM"=gm,
        "Lower CL"=LCL,
        "Upper CL"=UCL)
  data
}
```

> **Note: **
>
> - **x**: vektor numerik
> - **alpha**: alpha level yang digunakan


```r
med_gm(x=gwardat$konsentrasi, alpha=0.05)
```

```
##       GM Lower CL Upper CL 
##    23.87    10.63    53.60
```

Fungsi tersebut juga dapat digunakan bersamaan dengan fungsi seperti apply function atau map function. Ini berguna jika data yang kita miliki memiliki banya kolom yang perlu dihitung masing-masing interval kepercayaannya. Berikut adalah contoh sintaks yang digunakan:


```r
# menggunakan zpply function
sapply(airquality, med_gm, alpha=0.05)
```

```
##          Ozone Solar.R  Wind  Temp Month   Day
## GM       30.52   149.6 9.273 77.28 6.847 12.27
## Lower CL 26.58   131.4 8.697 75.74 6.623 10.73
## Upper CL 35.05   170.2 9.888 78.86 7.079 14.03
```

```r
# menggunakan map function
map(airquality, med_gm, alpha=0.05)
```

```
## $Ozone
##       GM Lower CL Upper CL 
##    30.52    26.58    35.05 
## 
## $Solar.R
##       GM Lower CL Upper CL 
##    149.6    131.4    170.2 
## 
## $Wind
##       GM Lower CL Upper CL 
##    9.273    8.697    9.888 
## 
## $Temp
##       GM Lower CL Upper CL 
##    77.28    75.74    78.86 
## 
## $Month
##       GM Lower CL Upper CL 
##    6.847    6.623    7.079 
## 
## $Day
##       GM Lower CL Upper CL 
##    12.27    10.73    14.03
```


Fungsi `med_gm()` dapat dilakukan sejumlah modifikasi seperti penggunaan data frame sebagai input serta proses transformasi yang dilakukan didalam fungsi yang ada sekaligus. Berikut adalah contoh fungsi yang digunakan untuk input berupa data frame dan proses transformasi termasuk didalamnya:


```r
med_gm <- function(df, alpha){
  # membuat vektor untuk menyimpan hasil loop
  var = rep(NA, ncol(df))
  gm = rep(NA, ncol(df))
  LCL = rep(NA, ncol(df))
  UCL = rep(NA, ncol(df))
  # looping
  for(i in 1:ncol(df)){
    # mengambil nama kolom
    var[i] = colnames(df[i])
    # transformasi variabel (logaritmik)
    x = log(df[,i])
    # rata-rata geometrik
    gm[i] = exp(mean(x, na.rm=TRUE))
    # menghitung derajat kebebasan
    d = length(x)-1
    # menghitung batas bawah dan atas
    LCL[i] = exp(mean(x, na.rm=TRUE)-qt(1-alpha/2,d)*sqrt(var(x, na.rm=TRUE)/length(x)))
    UCL[i] = exp(mean(x, na.rm=TRUE)+qt(1-alpha/2,d)*sqrt(var(x,na.rm=TRUE)/length(x)))
  }
  # menggabungkan hasil
  data=data.frame("Variabel"=var,
                  "GM"=gm,
                  "Lower CL"=LCL,
                  "Upper CL"=UCL)
  data
}
```

> **Note: **
>
> - **df**: data frame
> - **alpha**: alpha level yang digunakan

Untuk menguji fungsi tersebut jalankan fungsi tersebut menggunakan dataset yang pembaca miliki. Dalam contoh ini ak diberikan contoh penerapannya menggunakan dataset `airquality`. Jalankan fungsi berikut untuk memperoleh hasilnya.


```r
med_gm(airquality, 0.05)
```

```
##   Variabel      GM Lower.CL Upper.CL
## 1    Ozone  30.524   26.583   35.049
## 2  Solar.R 149.561  131.409  170.220
## 3     Wind   9.273    8.697    9.888
## 4     Temp  77.284   75.740   78.859
## 5    Month   6.847    6.623    7.079
## 6      Day  12.270   10.728   14.034
```

Pembaca perlu berhati-hati dalam menentukan apakah akan menggunakan metode Nonparametrik atau parametrik. Jika data berditribusi lognormal kita dapat menggunakan metode parametrik.

## Interval Kepercayaan Mean

Estimasi interval juga dapat dihitung untuk mean populasi sebenarnya $\mu$. Hal ini sangat sesuai jika pusat data menjadi fokus dalam analisa statistik. Interval simetris di sekitar sampel rata-rata X paling sering dihitung. Untuk ukuran sampel besar, interval simetris secara memadai menggambarkan variasi rata-rata, terlepas dari bentuk distribusi data. Ini karena distribusi rata-rata sampel akan mendekati dengan distribusi normal ketika ukuran sampel semakin besar, meskipun data mungkin tidak terdistribusi secara normal. Untuk ukuran sampel yang lebih kecil, rata-rata tidak akan didistribusikan secara normal kecuali jika data itu sendiri terdistribusi secara normal. Ketika data meningkat kemencengannya, lebih banyak data diperlukan sebelum distribusi rata-rata dapat didekati secara memadai oleh distribusi normal. Untuk distribusi yang sangat miring atau data yang mengandung *outlier*, mungkin diperlukan lebih dari 100 pengamatan sebelum nilai rata-rata tidak akan terpengaruh oleh nilai terbesar untuk mengasumsikan bahwa distribusinya akan simetris.

### Interval Kepercayaan Mean Untuk Distribusi Yang Simetris

Interval kepercayaan mean untuk distribusi simetris dihitung menggunakan tabel distribusi *student's t* yang tersedia dalam buku teks statistik dan perangkat lunak. Tabel ini dimasukkan untuk menemukan nilai kritis untuk t pada setengah tingkat alfa yang diinginkan. Pada buku lain sering dijelaskan bahwa distribusi t hanya digunakan untuk sampel kecil (beberapa menyebutkan n<30), sedangkan untuk distribusi besar digunakan distribusi normal. Penggunaan distribusi normal jarang digunakan dalam prakiraan. Hal ini disebabkan karena pada proses perhitungan diperlukan nilai simpangan baku $\sigma$. Pada kenyataannya pada pengukuran dilapangan kita sering sekalin melakukan estimasi terhadap simpangan baku melalui sampel $s$ karena kita tidak mengetahui nilai simpangan baku populasinya sehingga pada buku ini akan digali lebih jauh metode estimasi interval menggunakan persamaan distribusi t.

Lebar interval kepercayaan adalah fungsi dari nilai-nilai kritis dari tabel distribusi t, simpangan baku data, dan ukuran sampel. Ketika data memiliki kemecengan atau mengandung *outlier*, asumsi di balik interval t dan distribusi normal tidak berlaku. Interval simetris yang dihasilkan akan sangat luas sehingga sebagian besar pengamatan akan dimasukkan di dalamnya. Ini juga dapat mencapai di bawah nol di ujung bawah. Titik akhir negatif dari interval kepercayaan untuk data yang tidak dapat menjadi negatif adalah sinyal yang jelas bahwa asumsi interval kepercayaan simetris tidak diperlukan. Untuk data tersebut, dengan asumsi distribusi lognormal seperti yang dijelaskan dalam sub chapter sebelumnya (interval kepercayaan median) akan lebih tepat. Interval kepercayaan dihitung menggunakan Persamaan \@ref(eq:pmeancisim).

\begin{equation}
  \overline{x}-t_{\left(\frac{\alpha}{2},n-1\right)}\cdot\sqrt{\frac{s^2}{n}}\le\mu\le\overline{x}+t_{\left(\frac{\alpha}{2},n-1\right)}\cdot\sqrt{\frac{s^2}{n}}
  (\#eq:pmeancisim)
\end{equation}

Untuk lebih memahami cara penerapannya, kita akan menggunakan kembali data pada Tabel \@ref(tab:gwardat2). Langkah pertama yang perlu dilakukan adalah menghitung mean sampel $\overline{x}$ dan simpangan baku sampel $s$. Berdasarkan hasil perhitungan diperoleh nilai $\overline{x}$ =98.352 dan $s$ = 144.685. Dengan meggunakan Persamaan \@ref(eq:pmeancisim), interval estimasi mean dengan tingkat kepercayaan 95% dapat dihitung sebagai berikut:

$$
  3,17\ -\ t_{\left(0.25,24\right)}\cdot\sqrt{\frac{1,96^2}{25}}\le\mu\le3,17\ -\ t_{\left(0.25,24\right)}\cdot\sqrt{\frac{1,96^2}{25}}
$$

$$
  2,36\le\mu\le3,98
$$

Berdasarkan hasil yang diperoleh terdapat 95% peluang nilai mean populasi $\mu$ terletak pada interval 2,36 sampai 3,98. Perlu diingat bahwa metode parametrik sangat sensitif dengan adanya *outlier* sehingga jika pembaca ingin menggunakannya pastikan terlebih dahulu tidak ada *outlier* pada data dengan cara melakukan visualisasi data.

Pada `R` kita dapat menggunakan fungsi `stat.desc()` untuk menhitung statistika deskriptif serta interval kepercayaan mean-nya. Berikut adalah sintaks yang digunakan:


```r
# memuat paket
library(pastecs)

# ringkasan data
r=stat.desc(gwardat2$konsentrasi)
r
```

```
##      nbr.val     nbr.null       nbr.na          min 
##      25.0000       0.0000       0.0000       0.2624 
##          max        range          sum       median 
##       6.3630       6.1007      79.3167       2.9444 
##         mean      SE.mean CI.mean.0.95          var 
##       3.1727       0.3919       0.8089       3.8400 
##      std.dev     coef.var 
##       1.9596       0.6176
```

```r
# batas bawah (LCL)
mean(gwardat2$konsentrasi)-r[[11]]
```

```
## [1] 2.364
```

```r
# batas atas (UCL)
mean(gwardat2$konsentrasi)+r[[11]]
```

```
## [1] 3.982
```

Selain itu , kita juga dapat menghitung interval kepercayaan mean menggunakan fungsi `t.test()`. Fungsi ini pada dasarnya dilakukan untuk melakukan uji hipotesis terhadap satu rata-rata. Untuk lebih tahu mengenai fungsi tersebut jalankan sintaks bantuan berikut:


```r
?t.test
```

Untuk menghitung interval kepercayaan mean jalankan sintaks berikut:


```r
t.test(gwardat$konsentrasi, conf.level= 0.95) 
```

```
## 
## 	One Sample t-test
## 
## data:  gwardat$konsentrasi
## t = 3.4, df = 24, p-value = 0.002
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##   38.63 158.08
## sample estimates:
## mean of x 
##     98.35
```

Fungsi t-test tersebut juga dapat dikombinasikan dengan apply dan map function. Hal ini berguna jika pembaca ingin menghitung interval kepercayaan mean untuk setiap kolom data disertai dengan uji signifikansinya. Berikut adalah contoh sintaks yang digunakan:


```r
# menggunakan apply function
apply(X=airquality, MARGIN=2, FUN=t.test, conf.level=0.95)
```

```
## $Ozone
## 
## 	One Sample t-test
## 
## data:  newX[, i]
## t = 14, df = 115, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##  36.06 48.20
## sample estimates:
## mean of x 
##     42.13 
## 
## 
## $Solar.R
## 
## 	One Sample t-test
## 
## data:  newX[, i]
## t = 25, df = 145, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##  171.2 200.7
## sample estimates:
## mean of x 
##     185.9 
## 
## 
## $Wind
## 
## 	One Sample t-test
## 
## data:  newX[, i]
## t = 35, df = 152, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##   9.395 10.520
## sample estimates:
## mean of x 
##     9.958 
## 
## 
## $Temp
## 
## 	One Sample t-test
## 
## data:  newX[, i]
## t = 102, df = 152, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##  76.37 79.39
## sample estimates:
## mean of x 
##     77.88 
## 
## 
## $Month
## 
## 	One Sample t-test
## 
## data:  newX[, i]
## t = 61, df = 152, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##  6.767 7.220
## sample estimates:
## mean of x 
##     6.993 
## 
## 
## $Day
## 
## 	One Sample t-test
## 
## data:  newX[, i]
## t = 22, df = 152, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##  14.39 17.22
## sample estimates:
## mean of x 
##      15.8
```

```r
# menggunakan map function
map(airquality, t.test, conf.level=0.95)
```

```
## $Ozone
## 
## 	One Sample t-test
## 
## data:  .x[[i]]
## t = 14, df = 115, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##  36.06 48.20
## sample estimates:
## mean of x 
##     42.13 
## 
## 
## $Solar.R
## 
## 	One Sample t-test
## 
## data:  .x[[i]]
## t = 25, df = 145, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##  171.2 200.7
## sample estimates:
## mean of x 
##     185.9 
## 
## 
## $Wind
## 
## 	One Sample t-test
## 
## data:  .x[[i]]
## t = 35, df = 152, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##   9.395 10.520
## sample estimates:
## mean of x 
##     9.958 
## 
## 
## $Temp
## 
## 	One Sample t-test
## 
## data:  .x[[i]]
## t = 102, df = 152, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##  76.37 79.39
## sample estimates:
## mean of x 
##     77.88 
## 
## 
## $Month
## 
## 	One Sample t-test
## 
## data:  .x[[i]]
## t = 61, df = 152, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##  6.767 7.220
## sample estimates:
## mean of x 
##     6.993 
## 
## 
## $Day
## 
## 	One Sample t-test
## 
## data:  .x[[i]]
## t = 22, df = 152, p-value <2e-16
## alternative hypothesis: true mean is not equal to 0
## 95 percent confidence interval:
##  14.39 17.22
## sample estimates:
## mean of x 
##      15.8
```


### Interval Kepercayaan Mean Untuk Distribusi Yang Asimetris

Mean dan interval kepercayaan dapat dihitung dengan mengasumsikan distribusi data mengikuti distribusi logaritmik $y=\ln{(x)}$. Metode ini berguna untuk jenis data yang memiliki bentuk distribusi data yang memiliki kemencengan positif (perlu transformasi logaritmik agar simetris).Metode ini memberikan perkiraan rata-rata yang lebih dapat diandalkan (varians lebih rendah) daripada perhitungan rata-rata sampel biasa tanpa transformasi log.

Untuk memperkirakan rata-rata populasi $\mu_x$ dalam unit aslinya, anggap datanya berdistribusi normal. Satu-setengah varians logaritma ditambahkan ke $\overline{y}$ (rata-rata log) sebelum eksponensial. Karena varians sampel $s^2_y$ hanya perkiraan varians sebenarnya dari logaritma, estimasi sampel rata-rata akan menjadi bias. Namun, untuk sampel dengan $s^2_y$ kecil dan ukuran sampel besar bias dapat diabaikan. Interval kepercayaan dapat dituliskan berdasarkan Persamaan \@ref(eq:pmeanciasim).

\begin{equation}
  \mu_x=\exp\left(\overline{y}+0,5\cdot s_y^2\right)
  (\#eq:pmeanciasim)
\end{equation}

dimana $y=\ln{(x)}$, $\overline{y}$= mean sampel dan $s^2_y$= varians sampel y dalam unit log natural.

Interval kepercayaan sekitar $\mu_x$ bukan estimasi interval yang dihitung untuk rata-rata geometri dalam Persamaan \@ref(eq:gmci2). Interval kepercayaan tidak dapat dihitung hanya dengan mengekspansi interval sekitar $\overline{y}$. Interval kepercayaan yang tepat dalam satuan asli untuk rata-rata data lognormal dapat dihitung. Untuk lebih jelasnya pembaca dapat melihatnya pada situs <http://jse.amstat.org/v13n1/olsson.html>.

Metode Cox dapat digunakan untuk menghitung interval keyakinan dengan nilai estimasi rata-rata menggunakan Persamaan \@ref(eq:pmeanciasim). Persamaan yang digunakan dapat dituliskan sebagai berikut (Persamaan \@ref(eq:pmeanciasimci)).

\begin{equation}
  \ln\left(\mu_x\right)=\overline{Y}+\frac{s_y^2}{2}\pm z_{\left(\frac{\alpha}{2}\right)}\sqrt{\frac{s_y^2}{n}+\frac{s_y^4}{2\left(n-1\right)}}
  (\#eq:pmeanciasimci)
\end{equation}

Persamaan \@ref(eq:pmeanciasimci) dapat dimodifikasi dengan menggunakan distribusi t dibanding menggunakan distribusi normal. Penggunaan distribusi t akan memperbaiki kelemahan penggunaan distribusi normal pada sampel yang berukuran kecil.

Data Tabel \@ref(tab:gwardat) dapat kita gunakan untuk menghitung rata-rata menggunakan Persamaan \@ref(eq:pmeanciasimci). Hal ini disebabkan karena data yang ada memiliki kemencengan positif sehingga dapat dianggap bahwa transformasi logaritmik dapat membentuk distribusi ini menjadi lebih simetris. 

Berdasarkan hasil perhitungan diperoleh nilai $\overline{Y}$ =3.173 dan $s^2_y$ = 1.96. Sehingga nilai interval selanjutnya dapat dihitung menggunakan Persamaan \@ref(eq:pmeanciasimci) dengan interval keyakinan 95%.

$$
  \ln\left(\mu_x\right)=3,17+\frac{1,96^2}{2}\pm1,96\sqrt{\frac{1,96^2}{25}+\frac{1,96^4}{2\left(25-1\right)}}
$$

$$
  \ln\left(\mu_x\right)=5,10\pm1,33
$$

Sehingga

$$
  \exp\left(5,10-1,33\right)\le\mu_x\le\exp\left(5,10+1,33\right)
$$

$$
  43,38\le\mu_x\le620,17
$$

Nilai interval yang dihasilkan sangat panjang sehingga nilai rata-rata yang dihasilkan tidak dapat diandalkan untuk memperkirankan lokasi nilai mean populasi. 

Pada contoh berikut akan disajikan sintaks untuk menghitung interval kepercayaan mean data pada Tabel \@ref(tab:gwardat) berdasarkan Persamaan \@ref(eq:pmeanciasimci) dan sitribusi yang digunakan adalah distribusi t. Pembaca dapat memodifikasi sintaks berikut jika ingin menggunakan distribusi normal.


```r
mean_asci<-function(x,alpha){
  m=mean(x, na.rm=TRUE)
  # mean data hasil transformasi logaritmik
  ave = mean(log(x), na.rm=TRUE)
  # simpangan baku data hasil transformasi
  sd = sd(log(x), na.rm=TRUE)
  # jumlah observasi
  n = length(x)
  # derajat kebebasa
  df = n-1
  # interval keyakinan satu sisi
  re = 1-(alpha/2)
  # CI menggunakan distribusi t
  LCL = exp(ave+(0.5*sd^2)-qt(re,df)*sqrt(((sd^2)/n)+((sd^4)/(2*df))))
  UCL = exp(ave+(0.5*sd^2)+qt(re,df)*sqrt(((sd^2)/n)+((sd^4)/(2*df))))
  # menggabungkan hasil
  data = c("Mean"=m,
            "Lower CL"=LCL,
            "Upper CL"=UCL)
  data
}
```

> **Note: **
>
> - **x**: vektor numerik
> - **alpha**: alpha level yang digunakan


```r
mean_asci(x=gwardat$konsentrasi, alpha=0.05)
```

```
##     Mean Lower CL Upper CL 
##    98.35    40.11   660.94
```

Fungsi tersebut juga dapat digunakan bersamaan dengan apply dan map function, sehingga fungsionalitas fungsi tersebut juga meningkat. Berikut adalah contoh sintak yang digunakan:


```r
# menggunakan apply function
sapply(airquality, mean_asci, alpha=0.05)
```

```
##          Ozone Solar.R   Wind  Temp Month   Day
## Mean     42.13   185.9  9.958 77.88 6.993 15.80
## Lower CL 37.74   178.9  9.404 76.34 6.766 14.94
## Upper CL 52.21   241.1 10.747 79.50 7.237 20.43
```

```r
# menggunakan map function
map(airquality, mean_asci, alpha=0.05)
```

```
## $Ozone
##     Mean Lower CL Upper CL 
##    42.13    37.74    52.21 
## 
## $Solar.R
##     Mean Lower CL Upper CL 
##    185.9    178.9    241.1 
## 
## $Wind
##     Mean Lower CL Upper CL 
##    9.958    9.404   10.747 
## 
## $Temp
##     Mean Lower CL Upper CL 
##    77.88    76.34    79.50 
## 
## $Month
##     Mean Lower CL Upper CL 
##    6.993    6.766    7.237 
## 
## $Day
##     Mean Lower CL Upper CL 
##    15.80    14.94    20.43
```


Jika pembaca ingin menggunakan data frame sebagai input yang digunakan selain vektor, fungsi tersebut dapat dimodifikasi seperti berikut:


```r
mean_asci<-function(df,alpha){
  # membuat vektor untuk menyimpan hasil loop
  var = rep(NA, ncol(df))
  m = rep(NA, ncol(df))
  LCL = rep(NA, ncol(df))
  UCL = rep(NA, ncol(df))
  # looping
  for(i in 1:ncol(df)){
    # mengambil nama kolom
    var[i] = colnames(df[i])
    # menghitung mean data
    m[i]=mean(df[,i], na.rm=TRUE)
    # mean data hasil transformasi logaritmik
    ave = mean(log(df[,i]), na.rm=TRUE)
    # simpangan baku data hasil transformasi
    sd = sd(log(df[,i]), na.rm=TRUE)
    # jumlah observasi
    n = length(df[,i])
    # derajat kebebasa
    d = n-1
    # interval keyakinan satu sisi
    re = 1-(alpha/2)
    # CI menggunakan distribusi t
    LCL[i] = exp(ave+(0.5*sd^2)-qt(re,d)*sqrt(((sd^2)/n)+((sd^4)/(2*d))))
    UCL[i] = exp(ave+(0.5*sd^2)+qt(re,d)*sqrt(((sd^2)/n)+((sd^4)/(2*d))))
  }
  # menggabungkan hasil
  data = data.frame("Variabel"=var,
                    "Mean"=m,
                    "Lower CL"=LCL,
                    "Upper CL"=UCL)
  data
}
```

> **Note: **
>
> - **df**: data frame
> - **alpha**: alpha level yang digunakan

Untuk menguji fungsi tersebut, pembaca dapat memasukkan data frame yang pembaca miliki kedalam persamaan tersebut. Berikut adalah contoh sintaks yang digunakan untuk menghitung interval kepercayaan mean pada dataset `airquality`. Pembaca dapat menjalankannya pada komputer pembaca.


```r
mean_asci(airquality, 0.05)
```

```
##   Variabel    Mean Lower.CL Upper.CL
## 1    Ozone  42.129   37.744   52.209
## 2  Solar.R 185.932  178.856  241.060
## 3     Wind   9.958    9.404   10.747
## 4     Temp  77.882   76.341   79.498
## 5    Month   6.993    6.766    7.237
## 6      Day  15.804   14.945   20.433
```

## Interval Prediksi Nonparametrik

Pertanyaan yang sering diajukan adalah apakah satu pengamatan baru kemungkinan berasal dari distribusi yang sama dengan data yang dikumpulkan sebelumnya, atau sebagai alternatif dari distribusi yang berbeda. Pertanyaan dapat dievaluasi dengan menentukan apakah pengamatan baru di luar interval prediksi yang dihitung dari data yang ada. Interval prediksi mengandung $100\cdot\left(1-\alpha\right)$ persen dari distribusi data, sementara $100\cdot\alpha$ persen berada di luar interval. Jika pengamatan baru datang dari distribusi yang sama dengan data yang diukur sebelumnya, ada kemungkinan $100\cdot\alpha$ persen bahwa pengamatan baru tersebut akan berada di luar interval prediksi. Karena pengamatan baru tersebut berada di luar interval tidak "membuktikan" pengamatan baru itu berbeda, hanya saja sepertinya begitu. Seberapa besar kemungkinan ini tergantung pada pilihan $\alpha$ yang ditentukan oleh peneliti.

Interval prediksi dihitung dengan tujuan yang berbeda dari interval kepercayaan. Interval prediksi terkait dengan nilai data individu yang berlawanan dengan ringkasan statistik seperti nilai mean. Interval prediksi lebih luas daripada interval kepercayaan, karena pengamatan individu lebih bervariasi daripada ringkasan statistik yang dihitung dari beberapa pengamatan. Tidak seperti interval kepercayaan, interval prediksi memperhitungkan variabilitas titik data tunggal di sekitar median atau rata-rata, di samping kesalahan dalam memperkirakan pusat distribusi. Ketika mean $\pm$ 2 simpangan baku secara keliru digunakan untuk memperkirakan lebar interval prediksi, data baru dinyatakan berasal dari populasi yang berbeda lebih sering daripada yang seharusnya.

### Interval Prediksi Nonparametrik Dua Sisi

Interval prediksi tingkat kepercayaan nonparametrik $\alpha$ secara sederhana dinyatakan sebagai interval antara persentil distribusi $\alpha/2$ dan $1-\left(\frac{\alpha}{2}\right)$ (Gambar \@ref(fig:ipnds)). Interval ini mengandung $100\cdot\left(1-\alpha\right)$ data, sedangkan $100\cdot\alpha$ persen berada di luar interval. Oleh karena itu jika titik data tambahan baru berasal dari distribusi yang sama dengan data yang diukur sebelumnya, ada kemungkinan $100\cdot\alpha$ persen bahwa itu akan berada di luar interval prediksi. Interval akan mencerminkan bentuk data yang dikembangkannya, dan tidak ada asumsi tentang bentuk bentuk yang perlu dibuat. Interval prediksi nonparametrik dua sisi dinyatakan berdasarkan Persamaan \@ref(eq:eqipnds).

\begin{equation}
  PI_{np}=X_{\frac{\alpha}{2}\cdot\left(n+1\right)}\ sampai\ dengan\ X_{\left[1-\left(\frac{\alpha}{2}\right)\right]\cdot\left(n+1\right)}
  (\#eq:eqipnds)
\end{equation}

\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{ipnds} 

}

\caption{Prediksi interval dua sisi (Helsel dan Hirsch, 2002)}(\#fig:ipnds)
\end{figure}

Kita akan kembali menggunakan data pada Tabel \@ref(tab:gwardat). Dengan menggunakan tingkat kepercayaan 90% kita diminta untuk menentukan interval prediksi dari konsentrasi arsenik pada data tersebut tanpa mengasumsikan distribusi dari data.

Untuk melakukannya kita perlu menentukan observasi ke-2,5 dan 97,5 (berdasarkan nilai $\alpha/2$) dengan rangking observasi berdasarkan Persamaan \@ref(eq:eqipnds) adalah $(0,05*26)$ atau rangking observasi antara observasi 1 ($R_1$) dan 2 ($R_2$) dan $(0,95*26)$ rangking observasi antara observasi 24 ($R_{24}$) dan 25 ($R_{25}$). Dengan menggunakan interpolasi linier pada observasi ke-1, 2 , 24 dan 25, interval prediksi yang diperoleh adalah sebagai berikut:

$$
  X_1+\left(\frac{R_{\left(0.05\cdot26\right)}-R_1}{R_2-R_1}\right)\cdot\left(X_2-X_1\right)\ sampai\ dengan\ X_{24}+\left(\frac{R_{\left(0.95\cdot26\right)}-R_{24}}{R_{25}-R_{24}}\right)\cdot\left(X_{25}-X_4\right)
$$

$$
  1,3+\left(\frac{1,3-1}{2-1}\right)\cdot\left(1,5-1,3\right)\ sampai\ dengan\ 340+\left(\frac{24,5-24}{25-24}\right)\cdot\left(580-340\right)
$$

$$
  1,4\ sampai\ dengan\ 508\ ppb
$$

Observasi baru diluar rentang tersebut akan dianggap berasal dari distribusi yang berbeda dengan tingkat error sebesar 10% ($\alpha$=10%).

Dengan menggunakan `R` pembaca depat menghitung interval prediksi menggunakan fungsi berikut:


```r
PInp <- function(x, alpha){
  # mengurutkan data
  x_sort = sort(x)
  # jumlah observasi
  n = length(x)
  # menghitung alpha masing-masing sisi
  err <- alpha/2
  # menentukan rangkin observasi sesuai alpha
  rl = err*(n+1)
  ru = (1-err)*(n+1)
  # menentukan observasi untuk interpolasi linier
  rl_1= ceiling(rl) # bulatkan ke bawah
  rl_2= floor(rl) # bulatkan ke atas
  ru_1= ceiling(ru) 
  ru_2= floor(ru)
  # menentukan interval prediksi
  LPI = round(x_sort[rl_1]+((rl-rl_1)/(rl_2-rl_1))*(x_sort[rl_2]-x_sort[rl_1]),1)
  UPI = round(x_sort[ru_1]+((ru-ru_1)/(ru_2-ru_1))*(x_sort[ru_2]-x[ru_1]),1)
  # menggabungkan hasil
  data = data.frame("Lower PI"=LPI,
                    "Upper PI"=UPI)
  return(data)
}
```

> **Note: **
>
> - **x**: vektor numerik
> - **alpha**: alpha level yang digunakan


```r
PInp(x=gwardat$konsentrasi, alpha=0.1)
```

```
##   Lower.PI Upper.PI
## 1      1.4      508
```

### Interval Prediksi Nonparametrik Satu Sisi

Interval prediksi satu sisi digunakan jika kita ingin mengecek apakah pengamatan baru lebih besar dari data yang ada, atau lebih kecil dari data yang ada, tetapi tidak keduanya. Keputusan untuk menggunakan interval satu sisi harus didasarkan sepenuhnya pada pertanyaan yang menarik. Seharusnya tidak ditentukan setelah melihat data dan memutuskan bahwa pengamatan baru cenderung hanya lebih besar, atau hanya lebih kecil, daripada informasi yang ada. Interval satu sisi menggunakan $\alpha$ dibanding $\alpha/2$ sebagai nilai error, menempatkan semua error di satu sisi interval (Gambar \@ref(fig:ipss)). Interval prediksi dituliskan berdasarkan Persamaan \@ref(eq:eqipss).

\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{ipss} 

}

\caption{Prediksi interval satu sisi (Helsel dan Hirsch, 2002)}(\#fig:ipss)
\end{figure}

\begin{equation}
  PI_{np}:\ x_{baru}<X_{\alpha\cdot\left(n+1\right)}\ atau\ x_{baru}>X_{\left[1-\alpha\right]\cdot\left(n+1\right)}
  (\#eq:eqipss)
\end{equation}

Untuk memahami penerapannya, misalkan kita memiliki nilai arsenik baru dengan konsentrasi 355 ppb. Kita perlu menentukan apakah nilai tersebut lebih besar dari sebagian besar data yang ada.

Dengan menggunakan Persamaan \@ref(eq:eqipss) dan $\alpha$=0,1 atau tingkat kepercayaan 90%, interval prediksi satu sisi atau data teratas dari persentil ke-90 dari data yang ada adalah $X_{0,9}*26=X_{23,4}$. Dengan menggunakan interpolasi linier pada observasi data dengan rangking ke-23 ($R_{23}$) dan 24 ($R_{23}$) diperoleh:

$$
  X_{23}+0,4\cdot\left(X_{24}-X_{23}\right)=300+0,4\cdot40=316\ ppb
$$

Berdasarkan data yang diperoleh diketahui bahwa batas atas dari interval prediksi adalah 316<355 pbb, sehingga disimpulkan bahwa konsentrasi 355 pbb lebih besar dari sebagian besar data yang ada.

Dengan menggunakan `R` interval prediksi menggunakan satu sisi dapat dihitung menggunakan fungsi berikut:


```r
PInp_os <- function(x, obs, alpha, side){
  # mengurutkan data dari yang terkecil
  x_sort = sort(x)
  # jumlah observasi
  n = length(x)
  # rangking observasi
  ru = (1-alpha)*(n+1)
  ru_1 = ceiling(ru)
  ru_2 = floor(ru)
  rl = alpha*(n+1)
  rl_1 = ceiling(rl)
  rl_2 = floor(rl)
  # perhitungan interval atas dan bawah
  PIup = x_sort[ru_1]+((ru-ru_1)/(ru_2-ru_1))*(x_sort[ru_2]-x_sort[ru_1])
  PIdown = x_sort[rl_1]+((rl-rl_1)/(rl_2-rl_1))*(x_sort[rl_2]-x_sort[rl_1])
  # decision making
  if((side=="upper") & (PIup<obs)){
    cat("PI =",PIup,",observasi baru=",obs)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi lebih besar dibandingkan sebagian besar nilai yang ada")
  } else if((side=="lower") & (PIdown>obs)){
    cat("PI =",PIdown, ",observasi baru=",obs)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi lebih kecil dibandingkan sebagian besar nilai yang ada")
  } else if(side==""){
    print("side belum ditentukan tentukan apakah lower atau upper")
  } else{
    cat("batas bawah =",PIdown,", batas atas =",PIup)
    cat("\n---------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi sama dengan sebagian besar nilai yang ada")
  }
}
```

> **Note: **
>
> - **x**: vektor numerik
> - **alpha**: alpha level yang digunakan
> - **obs**: observasi baru yang akan dibandingkan
> - **side**: untuk memilih jenis uji satu sisi yang digunakan. nilai yang mungkin adalah **Upper** (membandingkan dengan limit atas) dan **Lower** (membandingkan dengan limit bawah)


```r
PInp_os(x=gwardat$konsentrasi, obs=355, alpha=0.1, side="upper")
```

```
## PI = 316 ,observasi baru= 355
## ----------------------------------------------------------------------
## Kesimpulan:
## nilai observasi lebih besar dibandingkan sebagian besar nilai yang ada
```

## Interval Prediksi Parametrik

Interval prediksi parametrik juga digunakan untuk menentukan apakah pengamatan baru kemungkinan berasal dari distribusi yang berbeda dari data yang dikumpulkan sebelumnya. Namun, pada metode parametrik asumsi bentuk dari distribusi data akan diperhitungkan. Asumsi ini memberikan lebih banyak informasi untuk membangun interval, asalkan asumsi tersebut valid. Jika data tidak mengikuti distribusi yang diasumsikan, interval prediksi mungkin tidak akurat.

### Interval Prediksi Distribusi Simetris

Asumsi yang digunakan untuk melakukan perhitungan interval prediksi untuk distribusi data yang simetris adalah data haruslah berdistribusi normal. Interval prediksi selanjutnya dibentuk secara simetris pada kedua sisi nilai mean. Interval ini lebih lebar rentangnya dibandingkan dengan interval kepercayaan nilai mean. Persamaan matematis yang digunakan untuk menghitungnya dituliskan pada Persamaan  \@ref(eq:ipds).

\begin{equation}
  PI=\overline{X}-t_{\left(\frac{\alpha}{2},n-1\right)}\cdot\sqrt{s^2+\left(\frac{s^2}{n}\right)}sampai\ \overline{X}+t_{\left(\frac{\alpha}{2},n-1\right)}\cdot\sqrt{s^2+\left(\frac{s^2}{n}\right)}
  (\#eq:ipds)
\end{equation}

Untuk interval satu sisi Persamaan  \@ref(eq:ipds), menjadi Persamaan \@ref(eq:ipds2).

\begin{equation}
  PI=\overline{X}-t_{\left(\alpha,n-1\right)}\cdot\sqrt{s^2+\left(\frac{s^2}{n}\right)}sampai\ \overline{X}+t_{\left(\alpha,n-1\right)}\cdot\sqrt{s^2+\left(\frac{s^2}{n}\right)}
  (\#eq:ipds2)
\end{equation}

Untuk lebih memahaminya misalkan terdapat hasil pengukuran baru konsentrasi arsenik sebesar 350 ppb dengan menggunakan data pada Tabel \@ref(tab:gwardat) sebagai pembanding. Buktikan bahwa observasi baru tersebut berasal dari distrubusi yang sama dengan $\alpha$=5%.

Dengan menggunakan Persamaan  \@ref(eq:ipds), interval prediksi dapat dihitung sebagai berikut:

$$
PI\ =\ 98,4-t_{\left(0.025,24\right)}\cdot\sqrt{144,7^2+\frac{144,7^2}{25}\ }sampai\ \ 98,4+t_{\left(0.025,24\right)}\cdot\sqrt{144,7^2+\frac{144,7^2}{25}}
$$

$$
PI\ =\ 98,4-2,064\cdot147,6\ \ sampai\ \ 98,4+2,064\cdot147,6
$$

$$
PI\ =\ -206,25\ \ sampai\ \ 403,05
$$

Berdasarkan hasil perhitungan yang dilakukan terlihat bahwa limit interval prediksi yang dihasilkanterdapat nilai negatif. Kosentrasi negatif mengindikasikan bahwa data yang digunakan tidaklah simetris sehingga penggunaan interval prediksi untuk data yang simetris tidak dapat digunakan pada data tersebut. Metode perhitungan interval prediksi untuk data asimetris lebih cocok untuk digunakan.

Pada `R` interval prediksi disekitar nilai mean dapat dihitung menggunakan fungsi berikut:


```r
PI_sim <- function(x, obs, alpha, side){
  # menghitung nilai mean
  ave = mean(x, na.rm=TRUE)
  # menghitung nilai varians dara
  var = var(x, na.rm=TRUE)
  # menghitung df
  n = length(x)
  df = n-1
  # perhitungan rentang satu sisi
  pi_l1 = ave-qt((1-alpha), df)*sqrt(var+(var/n))
  pi_u1 = ave+qt((1-alpha), df)*sqrt(var+(var/n))
  # perhitungan rentang dua sisi
  pi_l2 = ave-qt((1-alpha/2), df)*sqrt(var+(var/n))
  pi_u2 = ave+qt((1-alpha/2), df)*sqrt(var+(var/n))
  # decision making
  if(side=="upper" & obs>pi_u1){
    cat("PI Atas =",pi_u1,",observasi baru=",obs)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi lebih besar dibandingkan sebagian besar nilai yang ada")
  }else if(side=="lower" & obs<pi_l1){
    cat("PI Bawah =",pi_l1,",observasi baru=",obs)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi lebih kecil dibandingkan sebagian besar nilai yang ada")
  }else if(side=="two side" & obs>pi_u2){
    cat("PI Bawah =",pi_l2,",observasi baru=",obs, ",PI Atas =",pi_u2)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi lebih besar dibandingkan sebagian besar nilai yang ada")
  }else if(side=="two side" & obs<pi_l2){
    cat("PI Bawah =",pi_l2,",observasi baru=",obs, ",PI Atas =",pi_u2)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi lebih kecil dibandingkan sebagian besar nilai yang ada")
  }else if(side=="upper" & obs<pi_u1){
    cat("PI Atas =",pi_u1,",observasi baru=",obs)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi sama dengan sebagian besar nilai yang ada")
  }else if(side=="lower" & obs>pi_l1){
    cat("PI Bawah =",pi_l1,",observasi baru=",obs)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi sama dengan sebagian besar nilai yang ada")
  }else{
    cat("PI Bawah =",pi_l2, ",observasi baru=",obs,",PI Atas =",pi_u2)
    cat("\n---------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi sama dengan sebagian besar nilai yang ada")
  }
}
```

> **Note: **
>
> - **x**: vektor numerik
> - **alpha**: alpha level yang digunakan
> - **obs**: observasi baru yang akan dibandingkan
> - **side**: untuk memilih jenis uji digunakan. nilai yang mungkin adalah **upper** (membandingkan dengan limit atas uji satu sisi), **lower** (membandingkan dengan limit bawah uji satu sisi) dan **two side** (uji dua sisi).


```r
# interval prediksi satu sisi
PI_sim(x = gwardat$konsentrasi, obs = 350, alpha=0.05, side=2)
```

```
## PI Bawah = -206.2 ,observasi baru= 350 ,PI Atas = 402.9
## ---------------------------------------------------------
## Kesimpulan:
## nilai observasi sama dengan sebagian besar nilai yang ada
```

### Interval Prediksi Untuk Distribusi Data Yang Tidak Simetris

Untuk distribusi data yang tidak simetris, data perlu dilakukan transformasi terlebih dahulu sebelum dilakukan. Data di lingkungan khusunya parameter di air cenderung memiliki bentuk distribusi tidak simetris (cenderung memiliki kemencengan positif). Transformasi logaritmik biasanya dapat digunakan untuk data tersebut agar bentuknya dapat simetris dan dapat memenuhi asumsi normalitas pada data. Data yang telah dilakukan transformasi selanjutnya dihitung menggunakan Persamaan  \@ref(eq:ipds) untuk interval prediksi dua sisi dan Persamaan  \@ref(eq:ipds2) untuk interval prediksi satu sisi. Hasil perhitungan selanjutnya dilakukan transformasi kembali sesuai dengan invers dari transformasinya dalam hal ini menggunakan transformasi eksponensial (jika tranformasi awalnya adalah natural log). Untuk data dengan bentuk distribusi logaritmik (kemencengan positif), interval prediksi yang digunakan disajikan pada Persamaan  \@ref(eq:ipdas) (dua sisi) dan Persamaan  \@ref(eq:ipdas2) (satu sisi).

\begin{equation}
  PI=\exp\left(\overline{X}-t_{\left(\frac{\alpha}{2},n-1\right)}\cdot\sqrt{s^2+\left(\frac{s^2}{n}\right)}\right)\ sampai\ \exp\left(\overline{X}+t_{\left(\frac{\alpha}{2},n-1\right)}\cdot\sqrt{s^2+\left(\frac{s^2}{n}\right)}\right)
  (\#eq:ipdas)
\end{equation}

\begin{equation}
  PI=\exp\left(\overline{X}-t_{\left(\alpha,n-1\right)}\cdot\sqrt{s^2+\left(\frac{s^2}{n}\right)}\right)\ sampai\ \ \exp\left(\overline{X}+t_{\left(\alpha,n-1\right)}\cdot\sqrt{s^2+\left(\frac{s^2}{n}\right)}\right)
  (\#eq:ipdas2)
\end{equation}

dimana $y=\ln{(x)}$, $\overline{y}$ adalah nilai rata-rata dari tranformasi logaritmik data, dan $s^2_y$ adalah varians dari tranformasi logaritmik data.

Dengan menggunakan contoh soal sebelumnya misalkan terdapat observasi baru konsentrasi arsenik sebesar 350 ppb. Kita perlu menentukan apakah observasi baru tersebut berasal dari distribusi yang sama berdasarkan data pada Tabel \@ref(tab:gwardat). 

Berdasarkan hasil visualisasi diketahui bahwa distribusi data yang dihasilkan memiliki bentuk kemencengan positif sehingga interval prediksi asimetris dapat digunakan. Dengan menggunakan $\alpha$=5% prediksi interval dua sisi dapat dihitung menggunakan Persamaan  \@ref(eq:ipdas).

$$
\ln\left(PI\right)\ =\ 3,71-t_{\left(0.025,24\right)}\cdot\sqrt{1,96^2+\frac{1,96^2}{25}\ }sampai\ \ 3,71+t_{\left(0.025,24\right)}\cdot\sqrt{1,96^2+\frac{1,96^2}{25}\ }
$$
$$
\ln\left(PI\right)\ =\ 3,71-2,064\cdot2,11\ sampai\ \ 3,71+2,064\cdot2,11
$$

$$
\ln\left(PI\right)\ =\ -1,19\ \ sampai\ \ 7,53
$$

$$
PI=\ 0,31\ \ sampai\ \ 1476.07
$$

Berdasarkan hasil yang diperoleh diketahui bahwa observasi baru berada diantara rentang tersebut. Rentang yang dihasilkan cukup besar yang disebabkan karena tinkat kepercayaan yang digunakan juga besar (95%). Pembaca dapat juga menggunakan tingkat kepercayaan yang lain seperti 99% dan 90%. Semakin besar alpha yang digunakan interval prediksi yang dihasilkan semakin kecil. Namun perlu diingat bahwa semakin kecil rentangnya maka error (alpha) juga semakin besar.

Pembaca juga dapat menggunakan bentuk transformasi lain untuk membentuk data yang lebih simetris dan memnuhi asumsi distribusi normal. Bentuk transformasi lain akan mengubah bentuk persamaan yang digunakan. Transformasi kuadrat misalnya akan mengubah transformasi pada ersamaan  \@ref(eq:ipdas) dan Persamaan  \@ref(eq:ipdas2) menjadi akar kuadrat.

Pada `R` interval prediksi dengan bentuk transformasi data logaritmik dapat dituliskan sebagai berikut:


```r
PI_asim <- function(x, obs, alpha, side){
  # transformasi logaritmik (kemencengan positif)
  x_trans = log(x)
  # menghitung nilai mean
  ave = mean(x_trans)
  # menghitung nilai varians dara
  var = var(x_trans)
  # menghitung df
  n = length(x)
  df = n-1
  # perhitungan rentang satu sisi
  pi_l1 = exp(ave-qt((1-alpha), df)*sqrt(var+(var/n)))
  pi_u1 = exp(ave+qt((1-alpha), df)*sqrt(var+(var/n)))
  # perhitungan rentang dua sisi
  pi_l2 = exp(ave-qt((1-alpha/2), df)*sqrt(var+(var/n)))
  pi_u2 = exp(ave+qt((1-alpha/2), df)*sqrt(var+(var/n)))
  # decision making
  if(side=="upper" & obs>pi_u1){
    cat("PI Atas =",pi_u1,",observasi baru=",obs)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi lebih besar dibandingkan sebagian besar nilai yang ada")
  }else if(side=="lower" & obs<pi_l1){
    cat("PI Bawah =",pi_l1,",observasi baru=",obs)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi lebih kecil dibandingkan sebagian besar nilai yang ada")
  }else if(side=="two side" & obs>pi_u2){
    cat("PI Bawah =",pi_l2,",observasi baru=",obs, ",PI Atas =",pi_u2)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi lebih besar dibandingkan sebagian besar nilai yang ada")
  }else if(side=="two side" & obs<pi_l2){
    cat("PI Bawah =",pi_l2,",observasi baru=",obs, ",PI Atas =",pi_u2)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi lebih kecil dibandingkan sebagian besar nilai yang ada")
  }else if(side=="upper" & obs<pi_u1){
    cat("PI Atas =",pi_u1,",observasi baru=",obs)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi sama dengan sebagian besar nilai yang ada")
  }else if(side=="lower" & obs>pi_l1){
    cat("PI Bawah =",pi_l1,",observasi baru=",obs)
    cat("\n----------------------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi sama dengan sebagian besar nilai yang ada")
  }else{
    cat("PI Bawah =",pi_l2, ",observasi baru=",obs,",PI Atas =",pi_u2)
    cat("\n---------------------------------------------------------")
    cat("\nKesimpulan:")
    cat("\nnilai observasi sama dengan sebagian besar nilai yang ada")
  }
}
```

> **Note: **
>
> - **x**: vektor numerik
> - **alpha**: alpha level yang digunakan
> - **obs**: observasi baru yang akan dibandingkan
> - **side**: untuk memilih jenis uji digunakan. nilai yang mungkin adalah **upper** (membandingkan dengan limit atas uji satu sisi), **lower** (membandingkan dengan limit bawah uji satu sisi) dan **two side** (uji dua sisi).


```r
# interval prediksi satu sisi
PI_asim(x = gwardat$konsentrasi, obs = 350, alpha=0.05, side=2)
```

```
## PI Bawah = 0.386 ,observasi baru= 350 ,PI Atas = 1476
## ---------------------------------------------------------
## Kesimpulan:
## nilai observasi sama dengan sebagian besar nilai yang ada
```

## Interval Kepercayaan Persentil (Interval Toleransi)

Kuantil atau persentil telah digunakan secara tradisional dalam sumber daya air untuk menggambarkan frekuensi kejadian banjir. Dengan demikian banjir 100 tahun adalah persentil ke-99 (0,99 kuantil) dari distribusi puncak banjir tahunan. Besarnya banjir yang diperkirakan hanya akan dilampaui sekali dalam 100 tahun. Banjir 20 tahun besarnya besarnya yang diperkirakan hanya akan dilampaui sekali dalam 20 tahun (5 kali dalam 100 tahun), atau merupakan persentil ke-95 dari puncak tahunan. Demikian pula, banjir 2 tahun adalah median atau persentil ke-50 dari puncak tahunan. Persentil banjir ditentukan dengan asumsi bahwa aliran puncak mengikuti distribusi yang ditentukan seperti distribusi Log Pearson type III atau distribusi Gumbel.

Interal kepercayaan persentil berbeda dengan interval kepercayaan median. Hal yang paling jelas terlihat adalah interval kepercayaan persentil mengukur interval kepercayaan pada setiap persentil data yang ada, sedangkan intervak kepercayaan media hanya mengukur pada lokasi pusat data atau persentil ke-50.

Interval kepercayaan persentil juga disebut sebagai interval toleransi. Nilai persentil digunakan sebagai **koefisien cakupan** dari interal toleransi. Pada chapter ini akan dibahas lebih jauh mengenai metode perhitungan interval toleransi baikdengan metode parametrik maupun dengan metode nonparametrik.

### Interval Kepercayaan Nonparametrik Persentil

Metode perhitungan interval kepercayaan nonparametrik persentil mirip dengan perhitungan interval kepercayaan median. Kita akan menggunakan kembali tabel binomial jika sampel kita kecil untuk menentukan limit atas dan bawah yang merupakan nilai kritis dari alpha yang telah kita tetapkan. Nilai kritis ini selanjutnya akan ditransformasikan kedalam bentuk rangking pada data yang menunjukkan titik observasi ujung pada interval kepercayaan.

Tabel binomial dimasukkan pada kolom dengan nilai $p$, persentil yang diinginkan interval kepercayaannya. Jadi untuk interval kepercayaan pada persentil ke-75, kolom $p=0,75$ digunakan. Cari pada baris kolom tersebut sampai $n$ dengan probabilitas mendekati alpha level ($\alpha/2$) ditemukan. Nilai kritis $x_l$ bawah adalah bilangan bulat yang sesuai dengan probabilitas $p^*$. Nilai kritis kedua $x_u$ juga diperoleh dengan melanjutkan pada kolom tersebut sampai menemukan probabilitas $p'=\left(1-\frac{\alpha}{2}\right)$. Nilai kritis $x_l$ dan $x_u$ digunakan untuk menghitung rangking $R_l$ dan $R_u$ yang sesuai dengan nilai data di ujung atas dan bawah limit kepercayaan (Persamaan  \@ref(eq:iknp) dan Persamaan  \@ref(eq:iknp2)). Level interval kepercayaan yang dihasilkan akan sama dengan $\left(p'-p\cdot\right)$.

\begin{equation}
  R_l=x_l+1
  (\#eq:iknp)
\end{equation}

\begin{equation}
  R_u=x_u
  (\#eq:iknp2)
\end{equation}

Untuk memahami mengenai penerapan interval kepercayaan persentil diberikan sebuah contoh kita diminta untuk menentukan 95% interval kepercayaan nilai persentil ke-20 ($C_{0.20}$)  data konsentrasi arsenik pada Tabel \@ref(tab:gwardat) (p=0,2).

Berdasarkan data pada Tabel \@ref(tab:gwardat), nilai persentil ke-20 ($\overline{C}_{0.20}$)= 3.36ppb, yaitu data yang berada pada rangking 0,2*(26)=5,2 atau dua per sepuluh jarak antara data ke-5 dan ke-6. Untuk menentukan rentang kepercayaan persentil ke-20 sebenarnya dari data, kita perlu menggunakan kembali tabel binomial dengan menginputkan nilai p=0,2. nilai kritis $x_l$ diperoleh dengan mencari probabilitas data pada kolom p=0,2 yang mendekati nilai $\alpha/2$=0,025 adalah 1 ($p'$=0,027, error probabilitas sisi bawah distribusi). Dengan menggunakan Persamaan  \@ref(eq:iknp), diperoleh $R_l=2$. Dengan cara sama untuk sisi atas distribusi nilai kritis atas $x_u$ diperoleh dengan menginputkan nilai p=0,20 dengan nilai probabilitas mendekati $1-\frac{\alpha}{2}$= 0,975 diperoleh sebesar 9 ($p'$=0,983, error probabilitas sisi atas distribusi). Sehingga rentang kepercayaang 95,6% (0,983-0,027=0,956) untuk persentil ke-20 berada pada range data dengan rangkin ke-2 dan ke-9, atau

$$
1,5\le C_{0.20}\le8\ pada\ \alpha=0,044
$$

Jika data yang kita miliki cukup besar dengan jumlah sampel $n>20$ (sebagian buku menyebutkan $n>30$), kita dapat menggunakan distribusi normal untuk memperkirakan rentang kepercayaan persentil.Persamaan yang digunakan untuk menentukan batas atas dan bawah disajikan pada Persamaan  \@ref(eq:iknp3) dan Persamaan  \@ref(eq:iknp4).

\begin{equation}
  R_l=np+z_{\frac{\alpha}{2}}\cdot\sqrt{np\left(1-p\right)}+0,5
  (\#eq:iknp3)
\end{equation}

\begin{equation}
  R_l=np+z_{\left[1-\frac{\alpha}{2}\right]}\cdot\sqrt{np\left(1-p\right)}+0,5
  (\#eq:iknp4)
\end{equation}

Dengan menggunakan contoh sebelumnya kita dapat menghitung kembali rentang kepercayaan 95% persentil ke-20 menggunakan Persamaan  \@ref(eq:iknp3) dan Persamaan  \@ref(eq:iknp4) diperoleh rangking data batas bawah dan atas sebagai berikut:

$$
R_l=25\cdot0,2+\left(-1,96\right)\cdot\sqrt{25\cdot0,2\left(1-0,2\right)}+0,5\ =\ 5-1,96\cdot2+0,5=1,6
$$

$$
R_u=25\cdot0,2+1,96\cdot\sqrt{25\cdot0,2\left(1-0,2\right)}+0,5\ =\ 5+1,96\cdot2+0,5=9,4
$$

Berdasarkan hasil perhitungan diperoleh rangking data batas bawah dan batas atas secara berurutan adalah data ke-2 (batas bawah) dan data-9 (batas atas). Hasil yang diperoleh ini sama dengan yang telah diperoleh sebelumnya.

Pada `R` kita dapat membentuk fungsi untuk menghitung interval kepercayaan persentil sesuai dengan yang kita inginkan seperti lokasi persentil yang ingin kita uji serta jenis uji yang digunakan berdasarkan jumlah sampel yang kita inputkan. Selain itu rentang kepercayaan ini dapat pula digunakann untuk menghitung rentang kepercayaan median atau persentil ke-50.


```r
CI_npPercent <- function(x, p, alpha){
  # jumlah observasi
  n = length(x)
  # mengurutkan data
  x = sort(x)
  # membuat vektor yang akan menyimpan
  # hasil loop
  bl = rep(NA,n)
  bu = rep(NA,n)
  # decision makin
  if(n<= 20){
    # looping
    for(i in 1:n){
      bl[i] = pbinom(i, n, p)
      if(b>alpha/2){
        break
      }
    }
    for(i in 1:n){
      bu[i] = pbinom(i, n, p)
      if(b>(1-(alpha/2))){
        break
      }
    }
   # menghitung selisih terhadap alpha  
   dbl = abs(alpha-bl)
   dbu = abs(alpha-bu)
   # mencari titik kritis
   min_bl = which.min(dbl)
   min_bu = which.min(dbu)
   # menhitung rangking nilai bawah dan atas
   rl = min_bl + 1
   ru = min-bu
   # mencari data sesuai rangking bawah dan atas
   LCI = x[rl]
   UCI = x[ru]
  }else{
    # menghitung rangking nilai bawah dan atas
    rl = (n*p)+qnorm(alpha/2)*sqrt((n*p)*(1-p))+0.5
    ru = (n*p)+(qnorm(1-(alpha/2))*sqrt((n*p)*(1-p)))+0.5
    # mencari data sesuai rangking bawah dan atas
    LCI = x[floor(rl)]+ 
      ((rl-floor(rl))/(ceiling(rl)-floor(rl)))*(x[ceiling(rl)]-x[floor(rl)])
    UCI = x[floor(ru)]+ 
      ((ru-floor(ru))/(ceiling(ru)-floor(ru)))*(x[ceiling(ru)]-x[floor(ru)])
  }
  cat("Lower CI=", LCI," <= C(", p, ") <= ", 
       "Upper CI=", UCI)
}
```

> **Note: **
>
> - **x**: vektor numerik.
> - **p**: persentil yang ingin dicari. Nilai berkisar antara 0 sampai 1.
> - **alpha**: alpha level yang digunakan.

Pembaca dapat menjalankan fungsi tersebut mengggunakan data pada contoh soal sebelumnya yaitu mencari interval kepercayaan persentil ke-20. Jalankan sintaks berikut untuk mengetahui hasil yang diperoleh.


```r
CI_npPercent(x= gwardat$konsentrasi, p= 0.2, alpha=0.05)
```

### Uji Nonparametrik Untuk Persentil

Pengujian persentil dilakukan untuk mengecek apakah sebuah persentil berbeda (lebih besar atau lebih kecil) dibandingkan dengan sejumlah nilai. Sebagai contoh misalkan terdapat median kualitas harian suatu parameter tidak boleh melebihi standar yang berlaku sebesar $X_0$ ppb. Contoh lain dalam bidang hidrologi periode ulang hujan (PUH) 10 tahun atau persentil ke-90 dari debit puncak tahunan suatu kawasan dapat dilakukan pengujian apakah nilai yang ada dilapangan berbeda dengan PUH 10 tahunan yang telah kita hitung untuk digunakan dalam mendesain saluran drainase. Pembahasan pengujian persentil tersebut tidak akan sampai menyinggung pengujian hipotesis yang akan dibahas pada Chapter selanjutnya. Pembahasan akan berkisar membandingkan suatu nilai dengan interval kepercayaan seperti yang telah dijelaskan pada pembahasan terkait interval prediksi.

Pengujian apakah sebuah nilai $X_0$ berbeda dengan sejumlah rentang nilai yang ditetapkan dapat dilakukan dengan pengujian dua sisi dan satu sisi. Pengujian satu sisi melihat apakah suatu nilai $X_0$ berada diluar interval kepercayaan persentil atau diantara nilai batas bawah $X_l$ dan nilai batas atasnya $X_u$ (lihat Gambar \@ref(fig:unup1)). Sedangkan pengujian satu sisi melihat apakah suatu nilai lebih besar atau lebih kecil (tergantung apakah pengujian satu sisi sebelah atas distribusi atau sebelah bawah distribusi) dari interval kepercayaan persentil yang digunakan (lihat Gambar \@ref(fig:unup2) dan Gambar \@ref(fig:unup3)).

\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{unup1} 

}

\caption{Interval estimasi persentil Xp sebagai penguji apakah Xp=X0. A) X0 didalam interval estimasi sehingga Xp tidak berbeda secara signifikan dari X0, B) X0 berada diluar rentang estimasi sehingga Xp berbeda secara signifikan dari X0. (Helsel dan Hirsch, 2002)}(\#fig:unup1)
\end{figure}

\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{unup2} 

}

\caption{Interval estimasi persentil Xp sebagai penguji apakah Xp>X0. A) X0 didalam interval estimasi sehingga Xp tidak signifikan lebih besar dari X0, B) X0 berada diluar rentang estimasi sehingga Xp signifikan lebih besar dari X0. (Helsel dan Hirsch, 2002)}(\#fig:unup2)
\end{figure}

\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{unup3} 

}

\caption{Interval estimasi persentil Xp sebagai penguji apakah Xp>X0. A) X0 didalam interval estimasi sehingga Xp tidak signifikan lebih kecil dari X0, B) X0 berada diluar rentang estimasi sehingga Xp signifikan lebih kecil dari X0. (Helsel dan Hirsch, 2002)}(\#fig:unup3)
\end{figure}

Untuk menghitungnya secara nonparametrik menggunakan Persamaan  \@ref(eq:iknp3) dan Persamaan  \@ref(eq:iknp4) untuk jumlah sampel kecil sedangkan untuk sampel besar kita dapat menggunakan Persamaan  \@ref(eq:iknp3) dan Persamaan  \@ref(eq:iknp4).

Dengan menggunakan kembali data pada Tabel \@ref(tab:gwardat) kita akan menghitung apakah kadar arsenik kualitas air tanah tersebut melebihi baku mutu arsenik pada air minum dengan baku mutu konsentrasi arsenik tidak melampaui 300 ppb. Dengan menggunakan nilai $\alpha$=0,05 dan batas bawah persentil yang digunakan sebagai acuan pembanding adalah persentil ke-90 dapat dihitung sebagai berikut:

$$
\overline{C}_{0.90}=\left(25+1\right)\cdot0,9=23,4\ \left(data\ point\right)=300+0,4\left(340-300\right)=316\ ppb
$$
Karena jumlah sampel lebih besar dari 20, maka kita dapat menghitung batas atas data menggunakan Persamaan  \@ref(eq:iknp4).

$$
R_l=np+z_{0,05}\sqrt{np\left(1-p\right)}=25\cdot0,9+\left(-1,64\right)\cdot\sqrt{2,25}+0,5=20,5
$$
Kita dapat membulatkan hasilnya menjadi observasi 20 atau 21. Interpolasi linier dapat dilakukan sehingga diperoleh nilai observasi sebesar 215 ppb. Nilai ini lebih kecil dibandingkan $X_0$=300 ppb, sehingga baku mutu arsenik belum terlampaui oleh kualitas air tanah tersebut.

Kita dapat menggunakan fungsi `CI_npPercent()` untuk menghitung rentang persentil yang kita inginkan. Untuk pengujian satu sisi nilai `alpha` yang akan diinputkan perlu dikali oleh dua karena fungsi tersebut pada dasarnya digunakan untuk menghitung rentang kepercayaan persentil secara nonparametrik (nilai alpha dibagi pada kedua sisi). Berikut adalah contoh sintaks untuk menguji apakah sampel yang kita miliki melebihi baku mutu (persentil ke-90 dan alpha=5%):


```r
CI_npPercent(gwardat$konsentrasi, 0.9, 0.1)
```

### Interval Kepercayaan Parametrik Untuk Persentil

Interval kepercayaan untuk persentil juga dapat dihitung dengan mengasumsikan bahwa data mengikuti distribusi tertentu. Asumsi distribusi digunakan karena sering ada data yang tidak cukup untuk menghitung persentil dengan presisi yang diperlukan. Menambahkan informasi yang terkandung dalam distribusi akan meningkatkan ketepatan estimasi selama asumsi distribusi masuk akal. Namun ketika distribusi yang diasumsikan tidak sesuai dengan data dengan baik, estimasi yang dihasilkan kurang akurat, dan lebih menyesatkan, daripada jika tidak ada yang diasumsikan. Sayangnya, situasi di mana asumsi paling dibutuhkan ketika ukuran sampel yang kecil, adalah situasi yang sama di mana sulit untuk menentukan apakah data mengikuti distribusi yang diasumsikan.

Pada interval kepercayaan parametrik asumsi terhadap kecocokan data terhadap suatu distribusi perlu diperhatikan. Data di lingkungan umumnya memiliki bentuk distribusimengikuti distribusi lognormal. Selain itu, distribusi yang sering sekali digunakan adalah distribusi Pearson Tipe III dan Gumbel. Kedua pendekatan distribusi tersebut akan mempengaruhi metode perhitungan yang digunakan. Sehingga pengetahuan yang lebih baik mengenaik distribusi tersebut diperlukan. Pada buku ini kita hanya akan membahas mengenai perhitungan interval kepercayaan menggunakan distribusi lognormal. Pembaca dapat membaca mengenai penerapan distribusi lainnya melalui junal yang ditulis oleh [Wei dan Song (2019)](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=28&ved=2ahUKEwjnkojIgNnhAhXBh3AKHSJOBLM4ChAWMBF6BAgHEAI&url=https%3A%2F%2Fwww.preprints.org%2Fmanuscript%2F201901.0164%2Fv1%2Fdownload&usg=AOvVaw0evYfNso3_IwVWnmJMKsSp).

Perhitungan estimasi titik dan interval untuk persentil dengan asumsi distribusi lognormal dapat dilakukan dengan mudah. Pertama sampel rata-rata $y$ dan sampel simpangan baku $s_y$ logaritma dihitung. Estimasi titik kemudian dihitung menggunakan Persamaan  \@ref(eq:ikp1).

\begin{equation}
  X_p=\exp\left(\overline{y}+z_p\cdot s_y\right)
  (\#eq:ikp1)
\end{equation}

dimana $z_p$ merupakan kuantil ke-$p$ dari distribusi normal standard dan $y=\ln{(x)}$.

Estimasi interval untuk median sebelumnya diberikan pada Persamaan \@ref(eq:gmci2) dengan asumsi bahwa data mengikuti distribusi lognormal. Untuk persentil lainnya, interval kepercayaan dihitung menggunakan distribusi t non-sentral [(Stedinger, 1983)](https://www.researchgate.net/publication/277664323_Confidence_Intervals_for_Design_Events). Tabel distribusi itu ditemukan dalam artikel Stedinger, dengan list yang lebih lengkap terdapat pada perpustakaan online atau perangkat lunak matematika. Interval kepercayaan pada $X_p$ dihitung menggunakan Persamaan  \@ref(eq:ikp2).

\begin{equation}
  CI\left(X_p\right)=\exp\left(\overline{y}+\zeta_{\frac{\alpha}{2}}\cdot s_y,\ \overline{y}+\zeta_{\left[1-\frac{\alpha}{2}\right]}\cdot s_y\right)
  (\#eq:ikp2)
\end{equation}

dimana $\zeta{\alpha/2}$ merupakan $\alpha/2$ dari kuantil distribusi t non-sentral untuk persentil dengan ukuran sampel $n$ yang diinginkan.

Untuk lebih memahami penerapannya pembaca dapat mengerjakan contoh soal pada bagian sebelumnya. Dengan menggunakan estimasi interval 90% kita perlu menentukan interval estimasi persentil ke-90 dari data konsentrasi arsenik dengan asumsi distribusi yang digunakan berupa distribusi lognormal.

Dengan menggunakan Persamaan  \@ref(eq:ikp1) estimasi titik persentil ke-90 dapat dihitung.

$$
C_{0,90}=\exp\left(3,17+1,28\cdot1,96\right)=292,6\ ppb
$$
Nilai tersebut lebih rentanh dibanding estimasi konsentrasi sebelumnya asumsi data mengikuti distribusi lognormal dengan konsentrasi persentil ke-90 arsenik sebesar 316 ppb.

Dengan menggunakan Persamaan  \@ref(eq:ikp2), interval kepercayaan 90% dapat dihitung.

$$
\exp\left(3,17+0,898\cdot1,96\right)<C_{0,90}<\exp\left(3,17+1,838\cdot1,96\right)
$$

$$
138,4<C_{0,90}<873,5
$$

### Uji Parametrik Untuk Persentil

Seperti pada bagian sebelumnya kita ingin melihat apakah persentil dari sekumpulan data berbeda dengan nilai tertentu (dapat berupa baku mutu). Pengujian dilakukan dengan melihat apakah nilai tertentu tersebut berada diantara interval kepercayaan persentil dari data (uji dua sisi), lebih besar atau lebih kecil dari batas bawah atau batas atas interval kepercayaan persentil (uji satu sisi). Langkah pengujian dilakukan sama dengan sebelumnya dengan menghitung terlebih dulu batas atas atau batas bawah persentil data yang selanjutnya dibandingkan dengan nilai tertentu.

Dengan menggunakan hasil dari perhitungan sebelumnya, dengan menggunakan alpha=0,05 kita perlu menentukan apakah batas bawah interval kepercayaan melampaui baku mutu arsenik sebesar 300 ppb (uji satu sisi). Berdasarkan hasil perhitungan diperoleh batas bawah interval kepercayaan persentil ke-90 sebesar 138,4 ppb atau lebih kecil dibandingkan batas yang ditentukan, sehingga disimpulkan bahwa konsentrasi arsenik persentil ke-90 pada data tidak melampaui baku mutu yang ditentukan.

## Interval Kepercayaan Menggunakan Metode Bootstrap

Bootstrap merupakan metode inferensi populasi menggunakan data sampel. Metode ini dikembangkan oleh Bradley Efron pada tahun 1979. Jika pembaca ingin lebih mengenal metode ini pembaca dapat membaca makalahnya di tautan [berikut](https://projecteuclid.org/euclid.aos/1176344552). Pembaca dapat membaca makalah tersebut secara gratis.

Bootstrap mengandalkan pengambilan sampel dengan pengembalian dari data sampel. Teknik ini dapat digunakan untuk memperkirakan standard error (se) dari setiap statistik dan untuk memperoleh interval kepercayaan (CI) untuk itu. Bootstrap sangat berguna ketika CI tidak memiliki bentuk tertutup, atau memiliki bentuk yang sangat rumit.

Misalkan kita memiliki sejumlah sampel dengan ukuran $n$: $X=\left\{x_1,x_2,...,x_n\right\}$ dan kita tertarik dengan CI dari beberapa statistik data $T=t\left(X\right)$. Metode ini sangat mudah untuk dikerjakan. Kita hanya perlu mengulang sejumlah $R$ kali skema berikut: Untuk pengulangan ke-$i$, sampling dengan pengembalian $n$ data dari data sampel yang tersedia. Namai sampel baru tersebut sebagai sampel bootstrap ke-$i$ , $X_i$, dan hitung statistik (mean, median atu persentil) yang ingin dihitung interval kepercayaannya.

Sebagai hasilnya, kita akan mendapatkan nilai R dari statistik yang telah kita hitung: $T_1,T_2,\ ....,\ T_R$. Kita dapat menyebutnya sebagai realisasi bootstrap dari $T$ atau distribusi bootstrap dari $T$. Berdasarkan hal tersebut, kita dapat menghitung CI untuk T. 

Pada contoh kali ini penulis akan menyajikan cara melakukan bootstrap untuk menghitung interval kepercayaan pada mean, median, dan persentil. Data yang penulis gunakan adalah data `gwardat` pada Tabel \@ref(tab:gwardat).

Bootstrap pada `R` dilakukan dengan menggunakan library `boot`. Berikut adalah contoh pertama menghitung interval kepercayaan median:


```r
# memuat paket
library(boot)
```

```
## 
## Attaching package: 'boot'
```

```
## The following object is masked from 'package:psych':
## 
##     logit
```

```
## The following object is masked from 'package:car':
## 
##     logit
```


```r
# membuat hasil yang diperoleh lebih random
# dan reproducible
set.seed(100)

# membuat fungsi boot
med.boot.func <- function(x,i){
  median(x[i])
}

# melakukan bootstrap
median.boot <- boot(gwardat$konsentrasi,
                    # memasukkan fungsi boot
                    med.boot.func,
                    # menentukan jumlah replikasi
                    R=1000)
# print hasil
median.boot
```

```
## 
## ORDINARY NONPARAMETRIC BOOTSTRAP
## 
## 
## Call:
## boot(data = gwardat$konsentrasi, statistic = med.boot.func, R = 1000)
## 
## 
## Bootstrap Statistics :
##     original  bias    std. error
## t1*       19   9.319       26.59
```

Berdasarkan hasil yang diperoleh diketahui bahwa median dataset original sebesar 19. Pada hasil juga diperoleh nilai bias bootstrap. Nilai bias tersebut merupakan selisih dari nilai rata-rata 1000 median hasil bootstrap dikurangi dengan median sampel keseluruhan (original median). Standard error merupakan standard deviasi dari 1000 median yang terhitung.

Untuk mengetahui distribusi sampling yang telah kita lakukan. kita dapat melihat distribusi dengan mengeplotkan semua sampel bootstrap pada histogram dan QQ-plot dengan menjalankan sintaks berikut:

\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{EnvStat_files/figure-latex/boot1-1} 

}

\caption{Distribusi bootstrap median}(\#fig:boot1)
\end{figure}

Berdasarkan Gambar \@ref(fig:boot1) diketahui bahwa median tidak berdistribusi normal. Hal ini ditunjukkan dari distribusi pada histogram yang membentuk kemencengan positif. Selain itu, distribusi data pada QQ-plot juga tidak mengikuti garis referensi yang ada sehingga dapat disimpulkan bahwa distribusi median bootstrap tidak berdistribusi normal.

Untuk menghitung interval kepercayaan median dengan tingkat kepercayaan 95%, kita dapat menggunakan fungsi `boot.ci()`. Berikut adalah sintaks yang digunakan:


```r
boot.ci(boot.out=median.boot, conf=0.95)
```

```
## Warning in boot.ci(boot.out = median.boot, conf =
## 0.95): bootstrap variances needed for studentized
## intervals
```

```
## BOOTSTRAP CONFIDENCE INTERVAL CALCULATIONS
## Based on 1000 bootstrap replicates
## 
## CALL : 
## boot.ci(boot.out = median.boot, conf = 0.95)
## 
## Intervals : 
## Level      Normal              Basic         
## 95%   (-42.43,  61.79 )   (-71.75,  33.20 )  
## 
## Level     Percentile            BCa          
## 95%   (  4.8, 109.8 )   (  4.8, 100.0 )  
## Calculations and Intervals on Original Scale
```

Terdapat 4 buah hasil dari 4 buah metode yang dihasilkan sebagai output fungsi tersebut. Metode Normal mengasumsikan distribusi median bootstrap berdistribusi normal. Berdasarkan hasil visualisasi yang diperoleh diketahui bahwa distribusi data cenderung memiliki kemencengan positif sehingga metode ini tidak dapat digunakan, Selain itu, rentang yang dihasilkan juga terdapat nilai negatif yang mustahik dihasilkan pada konsentrasi arsenik (sebagian besar parameter lingkungan memiliki nilai terkecil $\le0$). Metode *Basic* memiliki asumsi bahwa tidak ada bias antara median data dengan median rata-rata hasil bootstrap. Berdasarkan hasil perhitungan yang dilakukan terlihat bahwa terdapat bias pada hasil bootstrap yang cukup besar sehingga metode ini tidak dapat diterapkan. Metode ketiga adalah metode persentil. Metode ini mengasumsikan bahwa distribusi median simetris, yang telah disinggung sebelumnya bahwa distribusi median tidak simetris sehingga metode ini tidak dapat diterapkan pada kasus ini. Metode terakhir adalah metode BCa (*bias-corrected and accelerated*) mengoreksi bias dan membuat lebih sedikit asumsi. Metode ini akan sering banyak kita gunakan pada data kita. Berdasarkan seluruh hasil yang telah diperoleh dapat kita simpulkan bahwa metode BCa cukup baik dalam menjelaskan interval kepercayaan median. Selain itu, metode persentil juga mempunyai hasil yang relatif mirip dengan BCa meskipun dari asumsi yang digunakan keempat metode tersebut tidak ada yang terpenuhi.

Pesan peringatan dalam *output* hasil menunjukkan bahwa interval kepercayaan kelima, disebut sebagai *studentized interval*, tidak dapat dihitung karena varians untuk sampel bootstrap tidak disediakan. Interval kepercayaan *studentized* berusaha untuk mengoreksi bias dengan "*studentizing*" setiap median yang dihitung (misal: mengurangi rata-rata median dan kemudian membaginya dengan standard error). Tampaknya tidak ada rumus umum untuk menghitung standard error untuk median, tetapi ada pedoman dalam literatur untuk memperkirakan kesalahan standar ketika populasi data yang mendasarinya diasumsikan terdistribusi secara normal. Dalam contoh ini, interval BCa tampaknya cukup baik. Perhatikan bahwa dalam beberapa kasus, mungkin ada peringatan bahwa "beberapa interval BCa mungkin tidak stabil." Dalam hal itu, hasil BCa harus diabaikan jika intervalnya tampak tidak masuk akal, dan pilihan dibuat dari opsi lain yang tersisa, berdasarkan pada Ulasan histogram dan plot probabilitas estimasi bootstrap.

Setelah pembaca memahami prosedur melakukan bootstrap pada median, pembaca dapat melakukan bootstrap pada persentil dan mean. Untuk bootstrap mean jalankan sintaks berikut:


```r
# membuat hasil yang diperoleh lebih random
# dan reproducible
set.seed(100)

# membuat fungsi boot
mean.boot.func <- function(x,i){
  mean(x[i])
}

# melakukan bootstrap
mean.boot <- boot(gwardat$konsentrasi,
                    # memasukkan fungsi boot
                    mean.boot.func,
                    # menentukan jumlah replikasi
                    R=1000)
# print hasil
mean.boot
```

```
## 
## ORDINARY NONPARAMETRIC BOOTSTRAP
## 
## 
## Call:
## boot(data = gwardat$konsentrasi, statistic = mean.boot.func, 
##     R = 1000)
## 
## 
## Bootstrap Statistics :
##     original  bias    std. error
## t1*    98.35  -1.839       27.19
```

Distribusi mean bootstrap disajikan pada Gambar \@ref(fig:boot2)

\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{EnvStat_files/figure-latex/boot2-1} 

}

\caption{Distribusi bootstrap mean}(\#fig:boot2)
\end{figure}

Berdasrkan hasil yang diperoleh, distribusi mean bootstrap mengikuti distribusi normal. Untuk memperoleh interval kepercayaan mean bootstrap jalankan sintaks berikut:


```r
boot.ci(boot.out=mean.boot, conf=0.95)
```

```
## Warning in boot.ci(boot.out = mean.boot, conf = 0.95):
## bootstrap variances needed for studentized intervals
```

```
## BOOTSTRAP CONFIDENCE INTERVAL CALCULATIONS
## Based on 1000 bootstrap replicates
## 
## CALL : 
## boot.ci(boot.out = mean.boot, conf = 0.95)
## 
## Intervals : 
## Level      Normal              Basic         
## 95%   ( 46.90, 153.48 )   ( 43.89, 150.36 )  
## 
## Level     Percentile            BCa          
## 95%   ( 46.34, 152.81 )   ( 55.95, 171.77 )  
## Calculations and Intervals on Original Scale
## Some BCa intervals may be unstable
```

Berdasarkan hasil yang diperoleh dapat dilihat bahwa metode BCa tidak dapat digunakan karena hasil yang diperoleh tidak stabil, Ketiga metode lainnya dapat digunakan karena asumsi normalitas (simetri) terpenuhi. Selain itu bias yang dihasilkan relatif kecil sehingga metode *Basic* juga dapat digunakan. 

Bootstrap terkahir yang kita lakukan adalah untuk memperoleh interval kepercayaan persentil dalam hal ini penulis akan mencobanya dengan persentil ke-90. Berikut alah sintaks yang digunakan:


```r
# membuat hasil yang diperoleh lebih random
# dan reproducible
set.seed(100)

# membuat fungsi boot
p90.boot.func <- function(x,i){
  quantile(x[i], probs=0.9)
}

# melakukan bootstrap
p90.boot <- boot(gwardat$konsentrasi,
                    # memasukkan fungsi boot
                    p90.boot.func,
                    # menentukan jumlah replikasi
                    R=1000)
# print hasil
p90.boot
```

```
## 
## ORDINARY NONPARAMETRIC BOOTSTRAP
## 
## 
## Call:
## boot(data = gwardat$konsentrasi, statistic = p90.boot.func, R = 1000)
## 
## 
## Bootstrap Statistics :
##     original  bias    std. error
## t1*      280  -3.756       77.38
```

Visualisasi distribusi bootstrap persentil 90 disajikan pada Gambar \@ref(fig:boot3)

\begin{figure}

{\centering \includegraphics[width=0.65\linewidth]{EnvStat_files/figure-latex/boot3-1} 

}

\caption{Distribusi bootstrap persentil 90}(\#fig:boot3)
\end{figure}

Bentuk visualisasi distribusi bootstrap persentil ke-90 yang dihasilkan pada Gambar \@ref(fig:boot3) terlihat sedikit memiliki kemencengan positif. untuk menghitung interval kepercayaan 95% persentil ke-90 jalankan sintaks berikut:


```r
boot.ci(boot.out=p90.boot, conf=0.95)
```

```
## Warning in boot.ci(boot.out = p90.boot, conf = 0.95):
## bootstrap variances needed for studentized intervals
```

```
## BOOTSTRAP CONFIDENCE INTERVAL CALCULATIONS
## Based on 1000 bootstrap replicates
## 
## CALL : 
## boot.ci(boot.out = p90.boot, conf = 0.95)
## 
## Intervals : 
## Level      Normal              Basic         
## 95%   (132.1, 435.4 )   ( 76.0, 444.0 )  
## 
## Level     Percentile            BCa          
## 95%   (116.0, 484.0 )   (160.8, 580.0 )  
## Calculations and Intervals on Original Scale
## Some BCa intervals may be unstable
```

Berdasarkan keempat hasil yang diperoleh, metode BCa cukup baik digunakan sebab distribusi bootstrap yang dihasilkan tidak memenuhi asumsi ketiga metode lainnya.

## Kegunaan Lain Dari Interval Kepercayaan

Selain digunakan untuk menghitung interval estimasi, interval kepercayaan dapat pula digunakan sebagai pendeteksi adanya *outlier*, kontrol kualitas, dan penentuan ukuran sampel yang akan digunakan pada suatu penelitian agar hasil yang diperoleh lebih presisi. Pembahasan juga akan disertai apakah normalitas pada distribusi data akan mempengaruhi performa dari ketiga jenis kegunaan interval kepercayaan.

### Implikasi Non-Normalitas Pada Pendeteksian *Outlier*

*Outlier* merupakan pengamatan yang tampak berbeda karakteristiknya dibandingkan sebagian besar pengamatan yang ada. Pengamatan ini seringkli dihapus dari prosedur analisis yang mengharuskan distribusi suatu data mengikuti distribusi normal. Penghapusan observasi ini bisa jadi tidak baik dilakukan sebab bisa saja observasi tersebut valid. Observasi yang bersifat *outlier* bisa jadi merupakan observasi terpenting sebab bisa saja dapat memberikan gambaran penting pada suatu kondisi ekstrim atau hubungan kausatif yang penting. Penghapusan ini tidak perlu dilakukan selam prosedur pengukuran yang sejenis tersedia dan tidak mengharuskan suatu distribusi data mengikuti distribusi tertentu, meskipun terdapat kelebihan dan kekurangan yang perlu kita perhatikan.

Untuk menghapus observasi yang kita identifikasikan sebagai *outlier*, aturan atau tes perlu dilakukan seperti tes yang diajukan oleh Beckman dan Cook (1983). Tes yang paling umum didasarkan pada interval-t, dan mengasumsikan data mengikuti distribusi normal. Biasanya Persamaan  \@ref(eq:ipds) untuk interval pediksi data yang mengikuti distribusi normal disederhanakan dengan mengabaikan nilai $\frac{s^2}{n}$. Nilai diluar interval prediksi tersebut selanjutnya dapat dinyatakan sebagai *oulier*. Uji lain yang dapat dilakukan adalah dengan visualisasi menggunakan box plot. Nilai diluar $Q1-1,5IQR$ atau $Q3+1,5IQR$ dinyatakan sebagai *outlier*. Namun pada Chapter ini tidak akan dibahas lebih lanjut sebab pada Chapter 7 telah dibahas mengenai deteksi *outlier* mellaui visualisasi data.

### Implikasi Non-Normalitas Pada Kontrol Kualitas

Presentasi visual interval kepercayaan yang digunakan secara luas dalam proses industri adalah kontrol chart. Sejumlah kecil produk disampel dari total kemungkinan pada titik waktu tertentu, dan rerata dihitung. Pengambilan sampel diulang pada interval reguler atau acak, tergantung pada desain, menghasilkan serangkaian cara sampel. Ini digunakan untuk membangun satu jenis kontrol chart, xbar chart. Chart ini secara visual mendeteksi ketika rata-rata sampel masa depan menjadi berbeda dari yang digunakan untuk membangun grafik. Keputusan perbedaan didasarkan pada melebihi interval kepercayaan parametrik di sekitar rata-rata yang telah dijelaskan dibagian lain Chapter ini.

Misalkan laboratorium kimia mengukur larutan standar yang sama beberapa kali selama sehari untuk menentukan apakah peralatan dan operator menghasilkan hasil yang konsisten. Untuk serangkaian pengukuran $n$ pada interval waktu $m$, ukuran sampel total $N=N\cdot M$. Perkiraan konsentrasi terbaik untuk standar itu adalah rata-rata keseluruhan yang dihitung menggunakan Persamaan  \@ref(eq:innpkk).

\begin{equation}
  \overline{X}=\sum_{i=1}^N\frac{X_i}{N}
  (\#eq:innpkk)
\end{equation}

$\overline{X}$ diplot sebagai garis tengah grafik. Interval kepercayaan pada rata-rata tersebut dijelaskan oleh Persamaan \@ref(eq:pmeancisim), menggunakan ukuran sampel $n$ yang tersedia untuk menghitung setiap nilai rata-rata individu. Batas interval tersebut juga diplotkan sebagai garis paralel pada chart kontrol kualitas. Nilai rata-rata yang akan berada diluar batas plot rata-rata ini hanya sebesar $\alpha\cdot100\%$ dari waktu jika rata-rata berditribusi normal. Observasi yang berada di luar batas lebih sering daripada ini diambil untuk menunjukkan bahwa sesuatu dalam proses telah berubah.

Jika $n$ besar (katakanlah 30 atau lebih), Teorema Limit Pusat menyatakan bahwa rata-rata akan terdistribusi secara normal meskipun data yang mendasarinya mungkin tidak. Namun jika $n$ jauh lebih kecil, seperti yang sering terjadi, berarti mungkin tidak mengikuti pola ini. Khususnya, untuk data yang memiliki kemencengan (data dengan *outlier* hanya pada satu sisi), distribusi di sekitar rata-rata mungkin masih memiliki kemencengan. Hasilnya adalah nilai besar untuk simpangan baku, dan pita kepercayaan yang lebar. Oleh karena itu, chart akan memiliki kekuatan yang lebih rendah untuk mendeteksi observasi yang mulai menjauh dari nilai rata-rata yang diharapkan daripada jika data tidak memiliki kemencengan.

Chart kontrol juga diproduksi untuk menggambarkan varians proses. Chart kontrol juga menggunakan nilai range (R chart) atau simpangan baku (S chart). Kedua grafik bahkan lebih sensitif terhadap perubahan data dari kondisi normal dibandingkan $\overline{X}$ chart. Keduanya akan mengalami kesulitan dalam mendeteksi perubahan varian ketika data yang mendasarinya tidak normal, dan ukuran sampel $n$ untuk setiap rata-rata kecil.

### Implikasi Non-Normalitas Terhadap Desain Sampling

Persamaan t-interval juga digunakan untuk menentukan jumlah sampel yang diperlukan untuk memperkirakan rata-rata dengan tingkat presisi yang ditentukan. Namun, persamaan tersebut membutuhkan data untuk kira-kira mengikuti distribusi normal. Persamaan tersebut harus mempertimbangkan *power* serta lebar interval. Artinya kita harus memutuskan apakah mean adalah karakteristik yang paling tepat untuk mengukur data yang memiliki kemencengan.

Untuk memperkirakan ukuran sampel telah cukup untuk menentukan interval estimasi dengan lebar spesifik dapat menggunakan Persamaan  \@ref(eq:inntds).

\begin{equation}
  n=\left(\frac{t_{\frac{\alpha}{2},n-1}\cdot s}{\Delta}\right)^2
  (\#eq:inntds)
\end{equation}

dimana $s$ merupakan simpangan baku sampel dan $\Delta$ merupakan setengah lebar interval yang diinginkan. Seperti yang telah dibahas di atas, untuk ukuran sampel kurang dari 30 hingga 50 dan bahkan lebih besar dengan data yang sangat menceng, perhitungan ini mungkin memiliki kesalahan besar. Perkiraan $s$ akan tidak akurat, dan akan sangat sangat meningkat nilainya karena kemencenga dan/atau *outlier* apapun. Karenanya, estimasi $n$ yang dihasilkan akan besar. Sebagai contoh, Hakanson (1984) memperkirakan jumlah sampel yang diperlukan untuk memberikan lebar interval yang masuk akal untuk karakteristik sedimen sungai dan danau, termasuk kimia sedimen. Berdasarkan koefisien variasi yang dilaporkan dalam artikel, data untuk sedimen sungai cukup menceng, seperti yang mungkin diharapkan. Ukuran sampel yang diperlukan untuk sungai dihitung pada 200 dan lebih tinggi.

Sebelum menggunakan persamaan sederhana seperti itu, data yang menceng harus ditransformasi terlebih dahulu sehingga lebih simetris, jika bukan berdistribusi normal. Misalnya, logaritma akan secara drastis menurunkan taksiran ukuran sampel untuk data miring, setara dengan Persamaan  \@ref(eq:ipdas). Ukuran sampel akan dihasilkan yang memungkinkan median (rata-rata geometris) diperkirakan dalam faktor toleransi multiplikasi sama dengan $\pm2\Delta$dalam satuan log.

Masalah kedua dengan Persamaan  \@ref(eq:inntds) untuk memperkirakan ukuran sampel, bahkan ketika data mengikuti distribusi normal, ditunjukkan oleh Kupper dan Hafner (1989). Mereka menunjukkan Persamaan  \@ref(eq:inntds) meremehkan ukuran sampel sebenarnya yang diperlukan untuk tingkat presisi tertentu, bahkan untuk perkiraan $n\le40$. Hal ini disebabkan karena Persamaan  \@ref(eq:inntds) tidak mengakui bahwa simpangan baku $s$ hanya estimasi dari nilai sebenarnya $\sigma$. Mereka menyarankan menambahkan probabilitas toleransi ke Persamaan  \@ref(eq:inntds), mirip dengan *statement of power*. Maka perkiraan lebar interval setidaknya sekecil lebar interval yang diinginkan untuk beberapa persentase tertentu (katakanlah 90 atau 95%) dari waktu tersebut. Misalnya, ketika $n$ akan sama dengan 40 berdasarkan Persamaan  \@ref(eq:inntds), lebar interval yang dihasilkan akan lebih kecil dari lebar yang diinginkan $2\Delta$ hanya sekitar 42% dari waktu. Ukuran sampel seharusnya menjadi 53 untuk memastikan lebar interval berada dalam kisaran toleransi 90% dari waktu. 

Ukuran sampel yang diperlukan untuk estimasi interval median atau untuk melakukan tes nonparametrik dari Chapter selanjutnya dapat diturunkan tanpa asumsi normalitas yang diperlukan di atas untuk interval-t. Noether (1987) menjelaskan estimasi ukuran sampel yang lebih kuat ini, yang memasukkan pertimbangan *power* sehingga lebih valid daripada Persamaan  \@ref(eq:inntds). Namun, baik estimasi normalitas distribusi data atau nonparametric mempertimbangkan efek penting dan sering diamati dari musiman atau tren, dan karenanya mungkin tidak pernah memberikan perkiraan yang cukup akurat untuk menjadi sesuatu yang lebih dari sekadar panduan kasar.

## Referensi

1. Bachman, L. J. 1984. **Field and laboratory analyses of water from the Columbia Aquifer in Eastern Maryland**. Ground Water 22. 460-467.
2. Damanhuri, E. 2011. **Statitika Lingkunga**. Penerbit ITB.
3. Deryto, T. tanpa tahun. **Bootstrap in R**. Datacamp. <https://www.datacamp.com/community/tutorials/bootstrap-r>
4. Efron, B. 1979. **Bootstrap Methods: Another Look at The Jacknife**. The Annuals of Statistics. Vol:7(1). 1-26.
5. Helsel, D.R., Hirsch, R.M. 2002. **statistical Methods in Water Resources**. USGS.
6. Kupper, L. L., and K. B. Hafner. 1989. **How appropriate are popular sample size formulas?**. American Statistician 43. 101-105.
7. Noether, G. E. 1987. **Sample size determination for some common nonparametric tests**. Journal American Statistical Assoc.. 82, 645-647.
8. Ofungwu, J. 2014. **Statistical Applications For Environmental Analysis and Risk Assessment**.  John Wiley & Sons, Inc.
9. Ting Wei, Songbai Song. 2019. **Confidence interval estimation for precipitation quantiles based on principle of maximum entropy**. Entropy. 21.


<!--chapter:end:10-penaksiran-secara-statistika.Rmd-->


<style>
body{
text-align: justify}
</style>

# Uji Hipotesis

Environmental Engineer sering mengumpulkan sejumlah data dari lingkungan untuk mempelajari proses yang terjadi pada sistem lingkungan dimana data tersebut berada. Sering kali mereka memiliki dugaan awal yang selanjutnya kita sebut sebagai hipotesis bagaimana suatu sistem bekerja. Tujuan pengumpulan data yang dilakukan untuk menguji apakah hipotesis yang telah terbentuk dapat dipertahankan sesuai dengan bukti-bukti yang disajikan oleh data. Ui statistik merupakan cara kuantitatif untuk menentukan apakah suatu hipotesis dapat dipertahankan atau hipotesis tersebut perlu ditolak.

## Klasifikasi Uji Hipotesis

Uji hipotesis dapat diklasifikasikan berdasarkan beberapa kriteria sebagai berikut:

### Klasifikasi Berdasarkan Skala Pengukuran

Skala pengukuran dalam suatu data dapat berupa kategorikal atau numerikal. Suatu pengukuran dapat melakukan perbandingan antara dua buah grup (kategori) berdasarkan data kontinu yang dimiliki masing-masing grup. Uji hipotesis yang digunakan adalah uji perbandingan dua populasi. Jika terdapat lebih dari dua populasi maka uji yang digunakan adalah uji anova.

Contoh lainnya misalkan kita memiliki dua buah data dengan skala kontinu. Kita ingin mengetahui korelasi antara dua variabel tersebut, maka uji hipotesis yang digunakan adalah uji korelasi.

Bagaimana jika skala pengukuran data kita seluruhnya kategorikal? jika skala pengukuran data kita seluruhnya adalah kategori, kita perlu membuat tabel kontingensi yang mengukur frekuensi kejadian pada masing-masing grup atau antara satu gruo terhadap grup yang lain. Uji hipotesis yang digunakan adalah uji asosiasi.

Pada Chapter ini kita hanya akan membahas uji hipotesis yang digunakan pada satu populasi. Uji hipotesis lain seperti uji hipotesis untuk 2 populasi, anova, korelasi dan asosiasi akan dibahas pada Chapter lainnya.

### Klasifikasi Berdasarkan Distribusi Data

Uji hipotesis yang melibatkan sejumlah asumsi seperti ditribusi data mengikuti distribusi tertentu (biasanya ditribusi normal) disebut sebagai **uji hipotesis parametrik**. Dinamakan uji parametrik karena uji ini melibatkan parameter-parameter yang ada pada data seperti nilai mean dan simpangan baku. Uji ini sangat bagus digunakan jika data kita benar-benar mengikuti asumsi ditribusi yang diinginkan. Jika tidak maka hasil uji yang diperoleh dapat menghasilkan keputusan yang salah. Hal ini disebabkan karena uji ini memiliki sensitifitas yang rendah (power) untuk mendeteksi efek nyata.

Alternatif lain yang dapat digunakan untuk melakukan uji hipotesis adalah dengan melakukan uji hipotesis **nonparameterik**. Uji ini tidak mengasumsikan data mengikuti distribusi tertentu. Informasi pada uji ini diperoleh dengan melakukan rangking pada data. Hal ini tentu berbeda dengan uji parametrik yang mengharuskan kita mengekstrak parameter pada data. Kesalahpahaman yang umum adalah pada uji nonparametrik memungkinkan terjadinya kehilangan informasi dibandingkan dengan tes parametrik karena tes nonparametrik membuang nilai data. Bradley (1968) dalam  bukunya "*Distribution-Free Statistical Tests*" menanggapi kesalahpahaman ini: "Sebenarnya, pemanfaatan informasi sampel tambahan [dalam parameter] dimungkinkan oleh informasi populasi tambahan yang terkandung dalam asumsi uji parametrik. Oleh karena itu, uji bebas distribusi hanya membuang informasi hanya jika pada uji parametrik asumsi diketahui benar (data mengikuti distribusi tertentu)." Alih-alih membuang informasi, tes nonparametrik secara efisien mengekstraksi informasi pada besaran relatif (rangking) data tanpa menciutkan informasi menjadi hanya beberapa statistik sederhana. 


## Menyiapkan Prosedur UJi Hipotesis

### Memilih Uji yang Sesuai

Prosedur uji dipilih berdasarkan karakteristik data dan tujuan studi. Kriteria pertama untuk memilih uji statistik yang sesuai adalah dengan melihat skala pengukuran pada data. Kita telah membahas ini pada klasifikasi uji berdasarkan skala pengukuran data.

Kriteria kedua yang digunakan adalah tujuan dari pengujian. Uji hipotesis yang tersedia dapat digunakan untuk melihat beda antara dua nilai sentral dua grup, tiga atau lebih grup, sebaran data antar grup, kovariansi antara dua atau lebi variabel antara satu sama lain.

Kriteria ketiga yang digunakan adalah memilih apakah akan melakukan uji parameterik atau nonparameterik. Pemilihan berdasarkan kriteria ini perlu melihat asumsi distribusi uji statististik apakah telah terpenuhi atau belum. Jika suatu data berdistribusi normal maka uji parametrik akan lebih dipilih, jika sebaliknya atau distribusi data tidak mengikuti distribusi tertentu maka uji yang digunakan adalah uji nonparametrik. Power dar uji parametrik untuk menolah hipotesis nol ketika hipotesis nol salah dapat sangat rendah jika digunakan pada data yang tidak berdistribusi normal. Selain itu, error tipe II biasanya juga terjadi pada uji parametrikpada data dengan distribusi tidak normal.

Transformasi data sering digunakan agar distribusi data mendekati distribusi normal. Jenis tranformasi akan berbeda pada setiap data sehingga proses transformasi akan mencoba pada berbagai format. Kendala yang timbul pada proses ini adalah jika kita akan melakukan uji pada dua atau lebih grup data. Jenis transformasi pada satu grup data bisa saja tidak berlaku untuk grup data lainnya. Jika kita paksakan transformasi ynag berbeda-beda pada tiap grup, maka pembacaan hasil yang diperoleh akan lebih sulit. Hal ini tidak terjadi jika sejak awal data yang tidak mengikuti distribusi normal dilakukan uji nonparametrik.

Untuk mempermudah proses pemilihan uji yang sesuai, Gardener (2012) membuat skema pemilihan uji hipotesis yang disajikan pada Gambar \@ref(fig:test)

\newpage
\begin{landscape}
\begin{figure}

{\centering \includegraphics{test} 

}

\caption{Skema pemilihan uji hipotesis (sumber: Gradener, 2012).}(\#fig:test)
\end{figure}
\end{landscape}

### Hipotesis Nol dan Alternatif

Uji hipotesis akan melakukan perbandingan antara dua buah hipotesis, hipotesis nol ($H_0$) dan hipotesis alternatif ($H_a$). Desain $H_0$ dan $H_a$ yang benar merupakan tahapan yang paling penting sebab prosedur uji hipotesis didesain untuk cenderung memilih hipotesis nol, sehingga $H_0$ tidak akan ditolak kecuali terdapat bukti kuat untuk menolaknya berdasarkan data yang kita miliki. Analogi ini mirip dengan istilah "praduga tak bersalah", dimana tersangka akan dianggap tidak bersalah kecuali terbukti sebaliknya berdasarkan bukti-bukti persidangan.

Impilkasi dari kondisi yang telah dijelaskan di atas adalah ketika $H_0$ diterima, kita tidak bisa menyatakan bahwa hipotesis tersebut benar. Hal yang tepat pada kondisi tersebut adalah tidak ada bukti yang cukup kuat pada data untuk menolaknya. Untuk memahaminya kita akan menggunakan contoh prosedur uji berbasis rentang kepercayaan (*confidence interval*) yang menolak $H_0:\mu=\mu_0$ jika $\mu_0$ tidak berada pada rentang kepercayaan $\mu$ (lihat lagi pada Chapter 10). Karena setiap nilai dalam rentang kepercayaan adalah kandidat yang masuk akal  (diberikan pada set data) untuk nilai parameter sebenarnya, jelas bahwa dengan tidak menolak $H_0:\mu=\mu_0$, kita belum membuktikan bahwa $H_0$ benar. Prosedur pengujian memberikan bukti statistik hanya ketika H0 ditolak. Dalam hal ini dapat diklaim bahwa alternatif telah dibuktikan (dalam arti statistik) pada tingkat signifikansi $\alpha$. Tingkat signifikansi mengkuantifikasi keraguan wajar yang bersedia kita terima ketika menolak hipotesis nol.

Berdasarkan pembahasan di atas dapat disimpulkan bahwa pernyataan yang perlu dibuktikan secara statistika disebut sebagai $H_a$. Penyataan pelengkapnya disebut sebagai $H_0$ atau peryataan yang dianggap benar kecuali terbukti sebaliknya. Hal terpenting dalam desain $H_0$ adalah perlunya penggunaan *equality sign* (=, $\le$, atau $\ge$) sebagai bagian dari desain $H_0$.

Untuk memahaminya misalkan diinginkan pengujian hipotesis bahwa rata-rata populasi adalah 100. Buatlah format hipotesis yang digunakan jika hipotesis alternatifnya menginginkan nilai rata-rata yang lebih besar?. Berdasarkan kondisi tersebut maka format hipotesisnya adalah sebagai berikut.

**$H_0$**: $\mu=100$

**$H_a$**: $\mu > 100$


### Statistik Uji dan Aturan Penolakan

Pada uji statistik terdapat dua buah nilai yang penting untuk diketahui yaitu **nilai statistik uji** dan **aturan penolakan**. Uji statistik yang digunakan untuk menguji $H_0$ terkait parameter $\mu$ dapat didasarkan pada titik estimasi $\hat\mu$ dari $\mu$. Aturan penolakan menentukan kapan $H_0$ harus ditolak. Pada dasarnya $H_0$ ditolak ketika nilai uji statistik berada pada sejumlah rentang (lebih besar, atau lebih kecil, atau keduanya tergantung pada $H_a$) yang menyatakan bahwa pada nilai tersebut tidak mungkin jika $H_0$ benar.

Menggunakan contoh kasus sebelumnya dimana kita kan menguji **$H_0$**: $\mu=100$. $H_0$ ditolak jika nilai statistik uji lebih kecil sama dengan 100 atau $H_a\le C_1$ sebagai contoh nilai statistika ujinya adalah 90,80, dst. Bagaimana jika hipotesis ujinya  **$H_a$**: $\mu \le 100$?. Sama dengan sebelumnya maka penolakan $H_0$ terjadi jika nilai uji statistiknya $H_a>C_2$ seperti 110, 120, dst. Kondisi lain yang dapat juga diterapkan jika **$H_a$**: $\mu \neq 100$, maka $H_0$ ditolak jika nilai statistika ujinya adalah $H_a<C_3$ atau $H_a>C_4$

Bagaimana cara tepat untuk memilih menggunakan nilai konstanta $C_1$, $C_2$, $C_3$, atau $C_4$? jawabannya adalah dengan menggunakan **tingkat signifikansinya** atau **error** (tingkat kesalahan). Tingkat signifikansi didefinisikan sebagai probabilitas (terbesar) untuk menolak $H_0$ secara tidak benar, atau, dengan kata lain, probabilitas (terbesar) untuk menolak $H_0$ ketika $H_0$ benar.

Seperti yang telah disebutkan, tingkat signifikansi menentukan risiko (atau, dalam hal legalistik, keraguan yang masuk akal) kita bersedia menerima kesalahan karena menyimpulkan bahwa $H_0$ salah. Ternyata konstanta $C_1$ dan $C_2$ dapat ditentukan dengan menentukan tingkat signifikansi.

#### Probabilitas Error Tipe I

Terdapat dua buah error yang terjadi pada saat pengambilan keputusan. Secara sederhana penulis akan menjelaskan error tersebut dengan menggunakan contoh pemberian vaksin kepada pasien. Vaksin baru tersebut tidak lebih baik atau sama kualitasnya dengan vaksin yang telah ada sebelumnya ($H_0$ benar). Sebagai data pendukung, pengujian telah dilakukan dengan memilih individu secara acak, dimana 8 individu melewati 2 tahun tanpa tertular virus. Kita akan melakukan kesalahan dengan menolak $H_0$ dan mendukung $H_a$ (vaksin lebih baik) sedangkan kenyataannya $H_0$ benar. Error yang disebabkan oleh penolakan $H_0$ padahal $H_0$ benar disebut sebagai **error tipe I**.

Jenis error kedua dapat terjadi jika 8 individu atau kurang melewati dua tahun periode penggunaan vaksin secara sukses, namun kita tidak dapat menyimpulkan bahwa vaksin tersebut lebih baik meskipun pada kenyataannya demikian ($H_a$ benar). Sehingga pada kasus ini kita gagal menolak $H_0$ meskipun kenyataannya $H_0$ salah. Kondisi dimana kita tidak menolak $H_0$ meskipun $H_0$ salah disebut sebagai **error tipe II**.

Dalam menguji hipotesis statistik apa pun, ada empat kemungkinan situasi yang menentukan apakah keputusan kita benar atau salah. Keempat kemungkinan tersebut disajikan pada Tabel \@ref(tab:error):


|                  | **$H_0$ Benar**  | **$H_0$ Salah**
-------------------|------------------|----------------
**Terima $H_0$**   | Keputusan benar  | Error tipe II
**Tolak $H_0$**    | Error tipe I     | Keputusan benar

: (\#tab:oparitmatika) Kondisi yang mungkin terjadi pada saat pengujian hipotesis.

Peluang untuk melakukan error tipe I disebut sebagai **tingkat signifikansi**, dilambangkan dengan huruf Yunani $\alpha$. Dalam kondisi di atas kesalahan tipe satu terjadi ketika lebih dari 8 orang dari 20 orang yang diinokulasi  dengan vaksin baru melampaui periode 2 tahun tanpa tertular virus dan peneliti menyimpulkan bahwa vaksin baru lebih baik padahal kenyataannya setara dengan vaksin yang sudah ada. Oleh karena itu, jika $X$ adalah jumlah orang yang tetap bebas dari virus selama minimal 2 tahun dengan probabilitas sukses $p=0,25$, maka probabilitas error tipe satu adalah sebagai berikut:

$$
\alpha=P\left(error\ tipe\ I\right)=P\left(X>8\ ketika\ p=\frac{1}{4}\right)=\sum_{x=9}^{20}b\left(x;20,\frac{1}{4}\right)
$$

$$
\alpha=1-\sum_{x=0}^8b\left(x;20,\frac{1}{4}\right)=1-0,9591=0,0409
$$

Kita dapat mengatakan bahwa hipotesis nol dengan probabilitas kejadian sukses sebesar $p=0,25$ telah teruji dengan tingkat signifikansi $\alpha=0,0409$. Nilai yang dihasilkan sangat kecil, sehingga error tipe I kemungkinan tidak terjadi. Akibatnya, akan lebih tidak biasa bagi lebih dari 8 orang untuk tetap kebal terhadap virus selama periode 2 tahun menggunakan vaksin baru yang pada dasarnya setara dengan yang sekarang ada di pasaran.

#### Probabilitas Error Tipe II

Probabilitas terjadinya error tipe II disimbolkan dengan $\beta$. Error tipe II sulit untuk dihitung kecuali kita memiliki hipotesis alternatif. Pada contoh kali ini kita akan menguji hipotesis nol dengan nilai $p=0,25$ melawan hipotesis alternatif dengan $p=0,5$, sehingga kita dapat melakukan perhitungan probabilitas untuk tidak menolak $H_0$ meskipun $H_0$ salah. Kita selanjutnya dapat menghitung probabilitas 8 individu atau kurang yang melampaui periode 2 tahun ketika nilai $p=0,5$.

$$
\beta =P\left(error\ tipe\ II\right)=P\left(X\le 8\ ketika\ p=\frac{1}{2}\right)
$$

$$
\beta=\sum_{x-0}^8b\left(x;20,\frac{1}{2}\right)=0,2517
$$

Berdasarkan hasil perhitungan diperoleh nilai probabilitas yang relatif tinggi. Hal ini mengidikasikan penolakan vaksin baru tersebut meskipun kenyataannya vaksin baru tersebut lebih superior dibandingkan vaksin yang telah ada. 

Idealnya kita akan menggunakan prosedur pengujian dimana probabilitas error tipe I dan II sangat kecil. Berdasarkan berbagai *text book* probabilitas error tipe I dan II dapat diturunkan dengan cara meningkatkan jumlah sampel yang kita miliki. 

Berdasarkan pembahasan terkait error pada pengujian hipotesis, terdapat beberapa properti penting terkait pengujian hipotesis, antara lain:

1. Error tipe I dan tipe II pada pengujian hipotesis saling terkait. Penurunan salah satu akan meningkatkan error lainnya.
2. Ukuran wilayah kritis dan probabilitas melakukan error tipe I selalu dapat dikurangi dengan menyesuaikan nilai kritis (meningkatkan atau menurunkan tingkat signifikansi).
3. Peningkatan ukuran sampel akan menurunkan nilai $\alpha$ dan $\beta$ secara simultan.
4. Jika hipotesis nol salah, nilai $\beta$ akan maksimum ketika nilai sebenarnya dari suatu parameter mendekati nilai yang sebenarnya. Semakin besar jarak antara nilai sebenarnya dengan nilai yang dihipotesiskan maka semakin kecil nilai $\beta$.

### P-Value

P-value merupakan probabilitas untuk memperoleh statistik uji yang dihitung, atau yang lebih kecil kemungkinannya, ketika hipotesis nolnya benar. P-value mengukur "kepercayaan" dari hipotesis nol. Semakin kecil p-value, semakin kecil kemungkinan statistik uji kemungkinan statistik uji yang diamati ketika $H_0$ benar, dan semaikn kuat bukti penolakan $H_0$. P-value disebut juga sebagai **tingkat signifikansi yang dicapai** oleh data.

Bagaimana bisa p-value berbeda dengan $\alpha$-level?. $\alpha$-level tidak bergantung pada data, tapi telah ditetapkan sebagai suatu resiko untuk melakukan error tipe I yang dapat diterima. $\alpha$-level merupakan nilai kritis yang memungkinkan sebuah keputusan "ya/tidak" dibuat. P-value menyediakan informasi lebih sepeti bukti kuat secara scientific. Penggunaan p-value memungkinkan seseorang dengan toleransi resiko berbeda-beda ($\alpha$ berbeda) untuk membuat keputusannya sendiri.

### Membuat Keputusan Untuk Menolak Hipotesis Nol atau Tidak

Ketika p-value lebih kecil dari $\alpha$-level, maka $H_0$ ditolak. Sebaliknya jika p-value lebih besar dari $\alpha$, maka $H_0$ diterima. Telah dijelaskan sebelumnya bahwa penerimaan hipotesis nol tidak berarti $H_0$ pasti benar. $H_0$ siasumsikan benar sampai terbukti sebaliknya dan tidak ditolak sampai dengan terdapat bukti yang cukup kuat untuk menolaknya.

## Uji Nilai Rata-Rata Sampel Tunggal

Pada bagian ini penulis akan menjelaskan prosedur uji hipotesis untuk satu populasi. Sebelum pembahasan dilakukan pembaca perlu mengingat bahwa uji ini sangat berkaitan dengan perhitungan interval kepercayaan yang telah kita bahas pada Chapter sebelumnya. Jika sebelumnya kita menghitung nilai mean suatu observasi pada selang tertentu, pada bagian ini kita akan membahas bagaimana menguji suatu rata-rata apakah berasal dari suatu populasi atau tidak berdasarkan p-value.

Prosedur uji hipotesis untuk satu populasi yang akan penulis bahas kali ini akan bergantung pada berbagai kondisi. Kondisi yang menjadi pertimbangan antara lain:

1. Apakah sampel berdistribusi normal?
2. Apakah jumlah sampel besar atau kecil?

Untuk mempermudahnya, pada Gambar \@ref(fig:singletest) penulis sajikan skema pemilihan uji hipotesis untuk satu sampel.


\newpage
\begin{landscape}
\begin{figure}

{\centering \includegraphics[width=0.9\linewidth]{singletest} 

}

\caption{Skema pemilihan uji hipotesis untuk satu populasi.}(\#fig:singletest)
\end{figure}
\end{landscape}

### Uji Parametrik

Pada uji parametrik asumsi normalitas distribusi sampel menjadi sesuatu yang penting agar hasil yang diperoleh valid. Pada uji satu populasi untuk uji parametrik terdapat dua pertimbangan dalam pemilihan metode uji yaitu varians populasi serta ukuran sampel.

Jika varians populasi diketahui maka kita dapat menggunakan pendekatan distribusi normal. Jika simpangan baku populasi ($\sigma$) tidak diketahui serta jumlah sampel kecil maka pendekatan dilakukan menggunakan distribusi t. Kondisi lain yang perlu dipertimbangkan adalah saat sampel yang kita miliki besar, namun simpangan baku populasi tidak diketahui. Hal ini merupakan kondisi yang banyak ditemukan di lingkungan. Beberapa *textbook* menjelaskan bahwa uji satu sampel untuk kondisi tersebut dapat menggunakan pendekatan distribusi normal sehingga simpangan baku populasi didekati dengan simpangan baku sampel ($s$). Hal ini sesuai dengan teori limit pusat dimana semakin besar ukuran sampel, maka nilai statistik sampel (mean dan simpangan baku) akan mendekati populasinya. Berikut adalah prosedur dalam melakukan uji hipotesisnya:

**Prosedur Uji Hipotesis**

- **Asumsi** : Distribusi normal
- **Hipotesis nol ($H_0$)** : $\mu=\mu_0$
- **Statistik Uji**:

\begin{equation}
  Z_{H_0}=\frac{\overline{X}-\mu_0}{\frac{\sigma}{\sqrt{n}}}\ \ \ n>30\ atau\ \sigma\ diketahui
  (\#eq:stparam)
\end{equation}

\begin{equation}
  T_{H_0}=\frac{\overline{X}-\mu_0}{\frac{s}{\sqrt{n}}}\ \ \ n\le30\ atau\ \sigma\ tidak\ diketahui
  (\#eq:stparam2)
\end{equation}

- **Aturan penolakan (RR) berdasarkan variasi $H_a$**


**$H_a$**       | **RR pada level $\alpha$**
----------------|-----------------------------------------------------------
$\mu>\mu_0$     | $Z_{H_0}\ge Z_\alpha$
$\mu<\mu_0$     | $Z_{H_0}\le -Z_\alpha$
$\mu\neq\mu_0$  | $Z_{\frac{\alpha}{2}} \le Z_{H_0}\le Z_{\frac{\alpha}{2}}$

: (\#tab:stha) Aturan penolakan berdasakan hipotesis alternatif distribusi normal.

**$H_a$**          | **RR pada level $\alpha$**
-------------------|----------------------------------------------------------------
$\mu>\mu_0$        | $T_{H_0}>t_{n-1,\alpha}$
$\mu<\mu_0$        | $T_{H_0}< -t_{n-1,\alpha}$
$\mu\neq\mu_0$     | $-t_{n-1,\frac{\alpha}{2}}<T_{H_0}< t_{n-1,\frac{\alpha}{2}}$

: (\#tab:stha1) Aturan penolakan berdasakan hipotesis alternatif distribusi t.

- **Formula p-value**

  + *Distribusi Normal*

\begin{equation}
p-value =
  \begin{cases}
    1-\Phi\left(Z_{H_0}\right)\ \ \ \ \ \ \ untuk\ H_a:\mu>\mu_0\\
    \Phi\left(Z_{H_0}\right)\ \ \ \ \ \ \ untuk\ H_a:\mu<\mu_0\\
    2\left[1-\Phi\left|Z_{H_0}\right|\right]\ \ \ \ \ \ \ untuk\ H_a:\mu\ne \mu_0
    \end{cases}
  (\#eq:stparam3)
\end{equation}

  + *Distribusi t*

\begin{equation}
p-value =
  \begin{cases}
    1-G_{n-1}\left(T_{H_0}\right)\ \ \ \ \ \ \ untuk\ H_a:\mu>\mu_0\\
    G_{n-1}\left(T_{H_0}\right)\ \ \ \ \ \ \ untuk\ H_a:\mu<\mu_0\\
    2\left[1-G_{n-1}\left|T_{H_0}\right|\right]\ \ \ \ \ \ \ untuk\ H_a:\mu\ne \mu_0
    \end{cases}
  (\#eq:stparam4)
\end{equation}

dimana $G_{n-1}$ adalah CDF (fungsi densitas kumulatif) dari distribusi t.

**Uji Hipotesis Menggunakan `R`**

- **Distribusi Normal**

Untuk menghitung p-value pada distribusi normal kita dapat menggunakan fungsi `pnorm()` (probabilitas kumulatif). Berikut adalah sintaks yang digunakan:


```r
# uji satu sisi
1-pnorm(((x/n)-mu)/(sd/sqrt(n)))
pnorm(((x/n)-mu)/(sd/sqrt(n)))

# uji dua sisi
2*(1-pnorm(abs(((x/n)-mu)/(sd/sqrt(n)))))
```

> **Note: **
>
> - **x/n**: rata-rata sampel
> - **mu**: rata-rata populasi
> - **sd**: simpangan baku
> - **n**: ukuran sampel

- **Distribusi t**

Pada uji hipotesis menggunakan distribusi t, fungsi yang digunakan sudah tersedia pada `R`. Fungsi yang digunakan adalah `t.test()`. Berikut adalah format fungsi yang digunakan:


```r
t.test(x, y = NULL,
       alternative = c("two.sided", "less", "greater"),
       mu = 0, paired = FALSE, var.equal = FALSE,
       conf.level = 0.95, ...)
```

> **Note: **
>
> - **x,y**: vektor numerik. Kedua argumen akan terisi jika akan dilakukan uji hipotesis untuk dua populasi.
> - **alternative**: diguanakan untuk menentukan jenis uji hipotesis apakah satu sisi("less" dan "greater"), atau dua sisi ("two.sided").
> - **mu**: rata-rata populasi. Secara default nilainya 0
> - **paired**: vektor logikal yang menentukan apakah uji dua populasi digunakan untuk sampel berpasangan (TRUE) atau tidak (FALSE).
> - **conf.level**: tingkat kepercayaan. Secara default tingkat kepercayaan yang digunakan adalah 95%.


**Contoh 1 ($\sigma$ dikeathui)**

Suatu produk kompos dalam kantong berisi rata-rata 16 kg per kantong, dengan simpangan baku=0,2 kg. Bila berat tersebut secara signifikan lebih kecil, maka toko penyalur berhak untuk menolak. Untuk mengujinya diambil sampel secara acak sebanyak 36 kantong, kemudian ditimbang, dan berat rata-rata yang diperoleh sebesar 15,7 kg. Dengan menggunakan $\alpha=0,01$ tentukan apakah berat rata-rata sampel lebih kecil dari berat seharusnya dengan asumsi distribusi yang terbentuk adalah distribusi normal?

**Jawab**:

$$
Hipotesis
  \begin{cases}
    H_0:\mu=16kg\\
    H_a:\mu<16kg
    \end{cases}
$$

dengan $n>30$ dan $\sigma$ diketahui, maka digunakan distribusi normal. Nilai Z untuk $\alpha=0,01$ adalah $-2,33$ dengan daerah penolakan berada pada rentang $Z_{H_0}\le -Z_\alpha$.

Statistik uji diperoleh berdasarkan Persamaan \@ref(eq:stparam).

$$
Z_{H_0}=\frac{15,7-16}{\frac{0,2}{\sqrt{36}}}=-9,00
$$

Nilai p-value selanjutnya dapat dihitung menggunakan Persamaan \@ref(eq:stparam3).

$$
\Phi\left(Z_{-9}\right)=1.128588e-19
$$

Pada `R` p-value dapat dihitung menggunakan sintaks berikut:


```r
pnorm(((15.7)-16)/(0.2/sqrt(36)))
```

```
## [1] 1.129e-19
```

**Kesimpulan**: p-value < $\alpha$, atau $H_0$ ditolak. Berat rata-rata sampel < 16 kg (di bawah standard) sehingga diperlukan pembenahan dalam penimbangan kompos ke kantongnya agar sesuai standard.

**Contoh 2 ($\sigma$ tidak diketahui)**

Menurut seorang pengusaha industri, unit pengolah limbahnya mengeluarkan effluent dengan parameter BOD rata-rata harian sebesar 17 mg/l. Untuk itu dilakukan sampling komposit selama 7 hari berturut-turut, dan ternyata rerata BOD sampelnya adalah 19 mg/l, dengan simpangan baku 4 mg/l. Bila fenomena tersebut berdistribusi normal, lakukan pengujian dengan tingkat keyakinan $\alpha=0,01$?

**Jawab**:

$$
Hipotesis
  \begin{cases}
    H_0:\mu=17kg\\
    H_a:\mu\ne17kg
    \end{cases}
$$

dengan $n\le30$ dan $\sigma$ tidak diketahui maka pengujian dilakukan dengan menggunakan distribusi t. Daerah penerimaan $H_0$ untuk $\alpha=0,01$ dan $df=7-1=6$ berada pada rentang $-3,143<T{H_0}<3,143$. 

Statistik uji dihitung menggunakan Persamaan \@ref(eq:stparam2).

$$
T_{H_0}=\frac{19-17}{\frac{4}{\sqrt{7}}}=1,322876
$$

p-value selanjutnya dapat dihitung menggunakan Persamaan \@ref(eq:stparam4).

$$
2\left[1-G_{6}\left|T_{1,323}\right|\right]=0,2340573
$$

p-value pada `R` dapat dihitung menggunakan fungsi `pt()` (fungsi densitas kumulatif). Berikut adalah sintaks yang digunakan:


```r
2*(1-pt(1.322876, df=6))
```

```
## [1] 0.2341
```

```r
# atau
set.seed(48)
t.test(x=rnorm(n=7, mean=19, sd=4), 
       mu=17,alternative="two.sided",
       conf.level=0.99)
```

```
## 
## 	One Sample t-test
## 
## data:  rnorm(n = 7, mean = 19, sd = 4)
## t = 1.2, df = 6, p-value = 0.3
## alternative hypothesis: true mean is not equal to 17
## 99 percent confidence interval:
##  10.97 28.62
## sample estimates:
## mean of x 
##     19.79
```

**Kesimpulan**: p-value > $\alpha$. Terima $H_0$. Pernyataan pengusaha tersebut dapat diterima.

Berdasarkan hasil perhitungan di atas penulis menggunakan dua cara yaitu dengan menggunakan fungsi `pt()` dan `t.test()`. Pada fungsi `t.test()` penulis perlu mereproduksi kembali data berdasarkan nilai mean dan simpangan baku yang ada. Hal ini tentu berbeda dengan cara satunya, namun kelebihan cara ini kita bisa melakukan uji hipotesis sekaligus menghitung rentang keyakinan dari sampel. Hasil yang diperoleh juga tidak berbeda antara kedua cara tersebut, sehingga pembaca bebas untuk menggunakan salah satunya.

### Uji Nonparametrik

Uji nonparametrik tidak memerlukan asumsi sampel untuk mengikuti distribusi tertentu. Untuk uji hipotesis satu populasi terdapat dua macam uji nonparametrik, yaitu: sign test dan signed-rank test. Kedua uji tersebut menggunakan nilai median sebagai nilai pemusatan data (data tidak berdistribusi normal). 

#### Sign Test

Sign test digunakan untuk menguji hipotesis terhadap nilai median populasi. Uji ini sangat cocok digunakan untuk sampel yang kecil dengan ukuran sampel $n<30$.

Pada uji sign test, nilai sampel yang selisihnya positif akan diganti nilainya dengan tanda "+", Sedangkan jika hasilnya negatif nilainya diganti dengan "-". Jika hipotesis nol benar ($H_0:\tilde{\mu}=\tilde{\mu_0}$) dan populasi simetris, maka jumlah tanda positif dan tanda negatif akan sama. Ketika salah satu tanda muncul lebih sering, maka kita dapat menolak $H_0$.

Secara teorotis, sign test dapat diaplikasikan hanya pada situasi dimana $\tilde{\mu_0}$ tidak sama dengan nilai observasi yang ada (selisih median terhadap observasi tidak menghasilkan angka nol). Meskipun terdapat nol peluang untuk memperoleh sampel dengan nilai tepat sama dengan $\tilde{\mu_0}$ ketika distribusi populasinya berasal dari distribusi kontinu. Pada kondisi aktual nilai sampel sama dengan $\tilde{\mu_0}$ berasal dari kurang presisinya proses pengukuran data. Jika memang benar diketahui nilai sampel sama dengan $\tilde{\mu_0}$, maka nilai tersebut selanjutnya akan dikecualikan pada proses perhitungan.

p-value pada sign test dihitung menggunakan menggunakan distribusi binomial, dimana kejadian sukses didefinisikan sebagai jumlah observasi dengan tanda "+" dengan probabilitas sukses $p=0,5$. Pembaca  dapat membuka kembali Chapter yang membahas mengenai distribusi probabilitas binomial untuk memahami cara perhitungannya.

**Prosedur Uji Hipotesis**

- **Asumsi** : jumlah sampel $n<30$
- **Hipotesis nol ($H_0$)** : $\tilde{\mu}=\tilde{\mu_0}$
- **Hipotesis nol terkonversi**: $H_0:p=0,5$, dimana p merupakan probabilitas observasi $>\tilde{\mu_0}$.
- **Sign Statistic**: Y = # observasi yang $>\tilde{\mu_0}$
- **Hipotesis alternatif terkonversi**

**$H_a$ untuk $\tilde{\mu}$** | **$H_a$ untuk $p$**
------------------------------|---------------------------
$\tilde{\mu}>\tilde{\mu_0}$   | $p>0,5$
$\tilde{\mu}<\tilde{\mu_0}$   | $p<0,5$
$\tilde{\mu}\ne\tilde{\mu_0}$ | $p\ne0,5$.

: (\#tab:signtest) Hipotesis alternatif terkonversi.


**$H_a$**                      | **RR pada level $\alpha$**
-------------------------------|-----------------------------------------------
$\tilde{\mu}> \tilde{\mu_0}$   | $Z_{H_0}\ge Z_\alpha$
$\tilde{\mu}< \tilde{\mu_0}$   | $Z_{H_0}\le -Z_\alpha$
$\tilde{\mu}\ne\tilde{\mu_0}$  | $|Z_{H_0}|\ge z_{\frac{\alpha}{2}}$

: (\#tab:signtest) Hipotesis alternatif terkonversi pendekatan  distribusi normal.


- **Statistik Uji**

**$n<10$**: Fungsi densitas kumulatif distribusi binomial. Lihat tabel distribusi binomial untuk $p=0,5$.

**$n\ge10$**:

\begin{equation}
Z_{H_0}=\frac{x-np}{\sqrt{npq}}
  (\#eq:signtesteq)
\end{equation}

dimana $X$ merupakan jumlah observasi bertanda "+". $p$ merupakan probabilitas kejadian sukses, dimana $p=q=0,5$. $n$ merupakan jumlah observasi.

- **p-value**

**$n<10$**

\begin{equation}
p-value =
  \begin{cases}
    P\left(X\ge x,\ \text{dimana}\ p=\frac{1}{2}\right)\ \ \ \ \ \ \ untuk\ H_a:\tilde{\mu}>\tilde{\mu_0}\\
    P\left(X\le x,\ \text{dimana}\ p=\frac{1}{2}\right)\ \ \ \ \ \ \ untuk\ H_a:\tilde{\mu}<\tilde{\mu_0}\\
    2\left(P\left(X\le x,\ \text{dimana}\ p=\frac{1}{2}\right)\right)\ \ \ \ \ \ \ untuk\ H_a:\tilde{\mu}\ne \tilde{\mu_0}
    \end{cases}
  (\#eq:signtesteq2)
\end{equation}

**$n\ge10$**

\begin{equation}
p-value =
  \begin{cases}
    1-\Phi\left(Z_{H_0}\right)\ \ \ \ \ \ \ untuk\ H_a:\tilde{\mu}>\tilde{\mu_0}\\
    \Phi\left(Z_{H_0}\right)\ \ \ \ \ \ \ untuk\ H_a:\tilde{\mu}<\tilde{\mu_0}\\
    2\left[1-\Phi\left(Z_{H_0}\right)\right]\ \ \ \ \ \ \ untuk\ H_a:\tilde{\mu}\ne \tilde{\mu_0}
    \end{cases}
  (\#eq:signtesteq3)
\end{equation}


**Contoh**

Nilai di bawah ini merupakan waktu yang diperlukan untuk menyisihkan suatu polutan di air sebesar 70% melalui proses sedimentasi pada percobaan di laboratorium:

```
1,1; 2,2; 0,9; 1,3; 2,0; 1,6; 1,8; 1,5; 2,0; 1,2; 1,7.
```

Gunakan sign test untuk mengecek apakah median dari hasil tersebut sesuai sama dengan yang dihasilkan penelitian sebelumnya sebesar 1,8 jam? Gunakan tingkat keyakinan 0,05 pendekatan distribusi binomial dan normal untuk kasus tersebut.

**Jawab**:

- $H_0:\tilde{\mu}=1,8$
- $H_a:\tilde{\mu}\ne1,8$
- $\alpha=0,05$
- Uji statistik: Binomial variabel X dengan p=0,5.
- perhitungan statistik uji:

Gnatilah tiap selisih nilai observasi terhadap median 1,8. Jika nilai selisih lebih besar dari median maka ganti dengan tanda "+", sedangkan jika lebih kecil ganti dengan tanda "-". Jika nilai nol yang dihasilkan maka kecualikan observasi tersebut. Berikut adalah hasil yang diperoleh:

$$
- + - - + - - + - -
$$

Berdassarkan hasil tersebut diperoleh jumlah kejadian sukses (nilai positif) $x=3$ dan $n=10$ (satu observasi nol dikecualikan).

**Pendekatan Distribusi Binomial**

Pembaca dapat menggunakan tabel distribusi binomial untuk menghitung probabilitas binomial dengan $n=10$, $p=0,5$, dan $x=3$. Berikut adalah hasil perhitungan yang dilakukan:

$$
P=2P\left(X\le3\ ketika\ p=\frac{1}{2}\right)=2\sum_{x=0}^3b\left(x;10;\frac{1}{2}\right)=0,3438>0,05
$$

Dengan menggunakan `R` kita dapat menggunakan fungsi `pbinom()` untuk menghitung probabilitas kumulatif dari distribusi binomial. Langkah pertama yang perlu dilakukan adalah membuat vektor yang berisikan observasi tersebut:


```r
# membuat vektor numerik
df <- c(1.5, 2.2, 0.9, 1.3, 2.0, 
        1.6, 1.8, 1.5, 2.0, 1.2, 1.7)

# cek panjang vektor
length(df)
```

```
## [1] 11
```

Langkah selanjutnya yang perlu dilakukan adalah menghitung selisih dari elemen vektor tersebut dengan nilai median yang telah kita miliki.


```r
# menghitung selisih nilai elemen vektor dengan median
df_new <- df-1.8

# print
df_new
```

```
##  [1] -0.3  0.4 -0.9 -0.5  0.2 -0.2  0.0 -0.3  0.2 -0.6
## [11] -0.1
```

Selanjutnya menghitung nilai x (jumlah observasi bernilai positif) dan ukuran sampel yang baru (n).


```r
# subset nilai vektor positif
df_new2 <- df_new[df_new>0]

# print
df_new2
```

```
## [1] 0.4 0.2 0.2
```

```r
# x
x <- length(df_new2)

# n
n <- length(df_new[df_new!=0])
```

Langkah terakhir setelah kita memperoleh nilai x dan n adalah menghitung probabilitas binomial menggunakan fungsi `pbinom()` dengan $p=0,5$.


```r
2*pbinom(q=x, size=n, prob=0.5)
```

```
## [1] 0.3438
```

**Pendekatan Distribusi Normal**

Untuk menghitung p-value dengan menggunakan pendekatan distribusi normal, kita perlu menghitung nilai mean dan simpangan baku dari contoh kasus di atas. Contoh kasus di atas merupakan contoh kasus percobaan binomial. Kita perlu menghitung nilai mean dan simpangan baku dari percobaan di atas. Data yang diperlukan untuk melakukannya adalah data yang telah dikonversi kedalam bentuk tanda "+" dan "-". Berdasarkan hasil perhitungan di atas telah diketahui $n=10$ dan $x=3$. Berikut adalah hasil perhitungan nilai mean dan simpangan baku contoh kasus tersebut:

$$
\tilde{\mu}=np=\left(10\right)\left(0,5\right)=5
$$

$$
\sigma=\sqrt{npq}=\sqrt{\left(10\right)\left(0,5\right)\left(0,5\right)}=1,581139
$$

Setelah kedua nilai tersebut dihitung selanjutnya kita dapat menghitung nilai Z dan menggunakan tabel distribusi normal untuk menghitung p-value.

$$
Z_{H_0}=\frac{2,5-5}{1,581139}=-1,581139
$$

Sehingga nilai p-value yang diperoleh:

$$
P=2\left[\Phi\left(Z_{-1,581139}\right)\right]=0,1138463
$$

Pada `R` kita dapat menggunakan fungsi `pnorm()` untuk menghitung probabilitas kumulatif dari distribusi normal. Berikut adalah sintaks yang digunakan:


```r
2*pnorm(q=2.5, mean=n*0.5, sd=sqrt(n*(0.5^2)))
```

```
## [1] 0.1138
```

**Kesimpulan**: p-value > $\alpha$. Terima $H_0$. Median hasil observasi tidak berbeda signifikan dengan median hasil percobaan sebelumnya.

Berdasarkan kedua pendekatan tersebut terlihat bahwa p-value yang diperoleh berbeda hampir 2 kali lipat, namun kesimpulan yang diperoleh tidak berbeda. Pada penerapannya pembaca dapat memilih salah satu pendekatan tersebut dengan memperhatikan jumlah sampel ($n$) yang dimiliki oleh pembaca. Jika jumlah sampel $n\ge10$ maka gunakan pendekatan distribusi normal.

Kita juga dapat membuat *user define function* kita sendiri jika suatu saat kita akan melakukan perhitungan kembali. Berikut adalah contoh sintaks yang digunakan untuk melakukan sign test:


```r
sign.test <- function(df, median, alternative){
  df_new <- df-median
  x <- length(df_new[df_new>0])
  n <- length(df_new[df_new!=0])
  if(n<10){
    if(alternative=="two.sided"){
      p.value=2*pbinom(q=x, size=n, prob=0.5)
    }else if(alternative=="greater"){
      p.value=1-pbinom(q=x, size=n, prob=0.5)
    }else if(alternative=="lower"){
      p.value=pbinom(q=x, size=n, prob=0.5)
    }else{
      warning("You must determine the alternative")
    }
  }else{
    if(alternative=="two.sided"){
      p.value=2*pnorm(q=x-0.5, mean=n*0.5, 
                      sd=sqrt(n*(0.5^2)))
    }else if(alternative=="greater"){
      p.value=0.5-pnorm(q=x-0.5, mean=n*0.5, 
                      sd=sqrt(n*(0.5^2)))
    }else if(alternative=="lower"){
      p.value=pnorm(q=x-0.5, mean=n*0.5, 
                      sd=sqrt(n*(0.5^2)))
    }else{
    warning("You must determine the alternative")
    }
  }
  p.value
}
```

Pembaca juga dapat mengedit script di atas sesuai dengan apa yang pembaca inginkan. Berikut adalah contoh output script tersebut menggunakan objek `df`:


```r
sign.test(df=df, median=1.8, alternative="two.sided")
```

```
## [1] 0.1138
```

#### Signed-Rank Test

signed-rank test disebut juga sebagai **Wilcoxon signed-rank test** merupakan metode nonparameterik untuk melakukan uji median pada satu populasi dengan distribusi yang simetris. Dengan kondisi tersebut, kita dapat melakukan uji hipotesis nol ($H_0=\tilde{\mu}=\tilde{\mu_0}$). Langkah pertama kita perlu menguragi seluruh nilai sampel dengan $\tilde{\mu_0}$, serta mengecualikan hasil pengurangan bernilai nol. Hasil pengurangan selanjutnya dirangking (diperingkat) tanpa memperdulikan tandanya. Rangking pertama merupakan nilai absolut terkecil dari hasil pengurangan (tanpa mempedulikan tanda), rangkin kedua merupakan absolut terkecil kedua, dst. Ketika nilai absolut hasil pengurangan memiliki nilai yang sama, maka peringkat masing-masing nilai merupakan rata-rata dari peringkat tersebut. Sebagai contoh misalnya nilai hasil pengurangan peringkat 5 dan 6 sama, maka peringkat masing-masing selanjutnya di ubah menjadi 5,5 (rata-rata kedua peringkat). Jika hipotesis nol benar, maka total rangking hasil penurangan yang positif akan sama dengan total rangkin hasil pengurangan yang negatif. Total pengurangan yang positif selanjutnya dilambangkan dengan $w_+$ dan total pengurangan yang negatif dengan $w_-$. Nilai terkecil dari kedua nilai tersebut dilambangkan dengan $w$.

Dalam penentuan penerimaan hipotesis terdapat beberapa hal yang perlu pembaca cermati. Jika hipotesis alternatif yang digunakan adalah $\tilde{\mu}<\tilde{\mu_0}$, hipotesis nol dapat ditolak hanya jika nilai $w_+$ kecil dan $w_-$ besar. Sebaliknya jika hipotesis alternatif yang digunakan adalah $\tilde{\mu}>\tilde{\mu_0}$, hipotesis nol dapat ditolak hanya jika nilai $w_+$ besar dan $w_-$ kecil. Untuk uji dua sisi, hipotesis nol akan ditolak jika kedua nilai $w_+$ dan $w_-$ cukup kecil.

**Prosedur Uji Hipotesis**

- **Asumsi** : Distribusi simetris.
- **Hipotesis nol ($H_0$)** : $\tilde{\mu}=\tilde{\mu_0}$
- **signed-rank**: Menghitung:

$d_i$ = selisih nilai observasi dengan median pembanding.

$r_i$ = rangking $d_i$ tanpa mempedulikan tanda (nol dikecualikan)

$w_+$ = Total $r_i$ positif

$w_-$ = Total $r_i$ negatif

$w$ = Nilai terkecil antara $w_-$ dan $w_+$

- **Komputasi jumlah rangking dan aturan penolakan berdasarkan $H_a$**

**$H_a$**                      | **RR pada level $\alpha$**  | **komputasi** 
-------------------------------|-----------------------------|---------------
$\tilde{\mu}> \tilde{\mu_0}$   | $w \le w_\alpha$            | $w_-$
$\tilde{\mu}< \tilde{\mu_0}$   | $w \le w_\alpha$            | $w_+$
$\tilde{\mu}\ne\tilde{\mu_0}$  | $w \le w_\alpha$            | $w$

: (\#tab:signranktest) Komputasi jumlah rangking dan aturan penolakan berdasarkan hipotesif alternatif.

Untuk $n\ge15$ aturan penolakan dapat menggunakan pendekatan distribusi normal seperti pada Tabel \@ref(tab:signtest).

- **Statistik Uji**

Untuk ukuran sampel $n<15$ nilai kritis dapat ditentukan berdasarkan tabel nilai kritis untuk Signed-Rank Test yang dapat pembaca unduh pada tautan [berikut](https://math.ucalgary.ca/files/math/wilcoxon_signed_rank_table.pdf).

Untuk ukuran sampel $n\ge15$ dapat menggunakan pendekatan distribusi normal dengan sebelumnya menghitung nilai Z berdasarka nilai $w_+$ (atau $w_-$).

\begin{equation}
\mu w_+=\frac{n\left(n+1\right)}{4}\ dan\ \sigma_{w_+}^2=\frac{n\left(n+1\right)\left(2n+1\right)}{24}
  (\#eq:signranktesteq)
\end{equation}

Sehingga nilai Z dapat dihitung menggunakan persamaan berikut:

\begin{equation}
Z=\frac{w_+-\mu w_+}{\sigma w_+}
  (\#eq:signranktesteq2)
\end{equation}

**Prosedur Uji Hipotesis**

Prosedur uji signed-rank test juga dapat dilakukan di `R` menggunakan fungsi `wilcox.test()`. Fungsi ini dapat digunakan untuk melakukan dua buah uji yaitu signed-rank dan Wilcoxon Rank Sum. Khusus untuk signed rank kita dapat melakukan test untuk satu atau dua populasi. Jika kita ingin melakukannya untuk satu populasi, maka kita hanya perlu menginputkan satu vektor saja. Berikut adalah format fungsi tersebut:


```r
wilcox.test(x, y = NULL,
            alternative = c("two.sided", "less", "greater"),
            mu = 0, paired = FALSE, conf.level = 0.95, ...)
```

> **Note: **
>
> - **x,y**: vektor numerik. Kedua argumen akan terisi jika akan dilakukan uji hipotesis untuk dua populasi.
> - **alternative**: diguanakan untuk menentukan jenis uji hipotesis apakah satu sisi("less" dan "greater"), atau dua sisi ("two.sided").
> - **mu**: rata-rata populasi. Secara default nilainya 0
> - **paired**: vektor logikal yang menentukan apakah uji dua populasi digunakan untuk sampel berpasangan (TRUE) atau tidak (FALSE).
> - **conf.level**: tingkat kepercayaan. Secara default tingkat kepercayaan yang digunakan adalah 95%.


**Contoh**

Kita akan menggunakan kembali data pada contoh soal sebelumnya. Pada contoh kali ini hitunglah menggunakan signed-rank test?

**Jawab**:

- $H_0: \tilde{\mu}=1,8$
- $H_a: \tilde{\mu}\ne1,8$
- $\alpha=0,05$
- Berdasarkan Tabel nilai kritis signed-rank test diperoleh nilai kritis untuk $\alpha=0,05$ sebesar 8 dengan menggunakan parameter n=10 (pengecualian selisih sama dengan nol) dan median=1.8. Aturan penolakan berdasarkan nilai tersebut berada pada rentang nilai $w\le8$.

- Hasil perhitungan $d_i$ dan rangking masing-masing nilai disajikan sebagai berikut:

**$d_i$**  | **$r_i$**
-----------|-----------
-0,3       | 5,5       
0,4        | 7         
-0,9       | 10
-0,5       | 8
0,2        | 3
-0,2       | 3
-0,3       | 5,5
0,2        | 3
-0,6       | 9
-0,1       | 1

: (\#tab:signranktest2) Komputasi signed-rank test.

Berdasarkan nilai $w_+=13$ dan $w_-=42$. Karena berupa uji dua sisi maka nilai $w$ perlu ditentukan. Berdasarkan kedua nilai tersebut nilai $w=13$ (nilai terkecil).

Dengan menggunakan `R` kita dapat melakukan uji menggunakan fungsi `wilcox.test()`. Uji ini akan menghasilkan p-value sehingga aturan penolakan $H_0$ menggunakan p-value akan sama seperti uji lainnya, dimana jika p-value $\ge H_0$, maka hipotesis nol diterima. Berikut adalah sintaks untuk melakukannya:


```r
wilcox.test(x=df, alternative ="two.sided", mu = 1.8,
            conf.level = 0.95)
```

```
## Warning in wilcox.test.default(x = df, alternative =
## "two.sided", mu = 1.8, : cannot compute exact p-value
## with ties
```

```
## Warning in wilcox.test.default(x = df, alternative =
## "two.sided", mu = 1.8, : cannot compute exact p-value
## with zeroes
```

```
## 
## 	Wilcoxon signed rank test with continuity
## 	correction
## 
## data:  df
## V = 13, p-value = 0.2
## alternative hypothesis: true location is not equal to 1.8
```

**Kesimpulan**: $w$ > $w_\alpha$. Terima $H_0$. Median hasil observasi tidak berbeda signifikan dengan median hasil percobaan sebelumnya.




<!--chapter:end:11-uji-hipotesis.Rmd-->

