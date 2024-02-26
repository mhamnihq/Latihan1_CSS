CSS (CASCADING STYLE SHEET)
adalah aturan sederhana untuk memberikan style pada HTML

Sintaks CSS
selector {property: value;}

contoh
body {
   font-family: arial;
   font-size: 12px;
}

penempatan CSS pada HTML
ada 3 cara yang dikategorikan menjadi 2, yaitu :
1. jalur internal (1. embed 2.inline)
2. jalur external (1. external)

1. Embed
cara untuk menghubungkan css ke HTMl dengan cara menambahkan tag <style></style>
pada tag head.
contoh :
<!DOCTYPE html>
<html>
<head>
	<title></title>
	<style></style> <----- ini tag nya !
</head>
<body>

</body>
</html>

2. Inline
cara untuk menghubungkan css ke HTML dengan cara langsung menambahkan style sebagai atribut
dari tag yang ingin kita beri style.
contoh :
 <h1 style="color: blue;">Selamat Datang</h1>

3. External
cara untuk menghubungkan css ke HTML dengan cara menambahkan tag <link> didalam tag head, bedanya dengan tag link ini
file css nya terpisah dengan file HTML nya.
contoh :
<!DOCTYPE html>
<html>
<head>
	<title></title>
	<link rel="stylesheet" type="text/css" href="style.css">	<----- ini tag link nya !
</head>
<body>

</body>
</html>


font Styling

Property nya ;
font-family: menentukan jenis font, valuenya: font name
font-size: menentukan ukuran font, valuenya: px, %, em
font-style: memberikan style pada font, valuenya: normal, italic, oblique
font-weight: memberikan tebal pada font, valuenya: normal, bold, bolder, lighter
font-variant: memberikan variasi pada font, valuenya: normal, smallcaps
line-height: memberikan jarak antar baris, valuenya: normal, px, em

text styling

propertynya ;
color: memberikan warna pada text, valuenya: color name, hexadecimal, RGB
text-align: untuk meluruskan text, valuenya: right, left, center, justify
text-indent: memberikan indentasi pada text, valuenya: px, em
text-decoration: mengatur dekorasi pada text, valuenya: none, underline, overline, line-throught
text-transform: mengatur perubahan text, valuenya: none, lowercast, uppercast, capitalize.
letter-spacing: mengatur jarak antar huruf, valuenya: normal, px
word-spacing: mengatur jarak antar kata, valuenya: normal, px

shorthand font styling
body {italic bold smallcaps 12px/15px arial, sans-serif}


background
adalah style untuk mengatur latar pada sebuah html/website
property nya;
background color: untuk memberikan warna pada background, valuenya: color name, hexadecimal, RGB
background image: untuk menjadikan gambar sebagai background, valuenya: url()
background repeat: untuk mengatur pengulangan pada gambar yang dijadikan background, valuenya : no repeat, repeat-x, repeat-y
background position: untuk mengatur posisi background, valuenya : top left, top center, top right, center left, center center, center right, bottom left, bottom center, botom right, x% y%,pos-x pos-y.

shorthand background
background: "red url(image.jpg) center no repeat"

catatan :
sesuai urutan shorthand background diatas, maka yang menjadi layer dasar sebuah background adalah color, setelah itu baru image.


selector basic
selector digunakan untuk memilih dan mengenali element HTML yang akan diberi style.

macam-macam selector
1. elemen HTML, berupa tag HTML. tinggal ditulis tag nya pada CSS
	contoh : di HTML <h1>Hello World</h1>
		 di css h1 {
			font-size: 20px;
			font-family: arial;
			color: blue;
			}

2. id, dituliskan didalam tag HTML sebagai atribut dan cara memanggilnya di CSS dengan parameter (#)
	contoh : di HTML <p id="paragraf">lorem</p>
		 di css #paragraf {
				text-align: justify;
				text-indent: 15px;
				line-height: normal;
				letter-spacing: normal;
				word-spacing: 3px;
				}

3. class, dituliskan didalam tag HTML sebagai atribut dan cara memanggilnya di css dengan parameter (.)
	contoh : di HTML <h3 class="isi">Daftar Isi</h3>
		 di css .isi {
			  color: green;
			  font-weight: bold;
			 }
	seandainya ada 2 tag yang berbeda namun berada di class yang sama, cara untuk memberi style agar hanya ke tag yang kit inginkan saja style terpasang (tidak semua tag dengan class yang sama ikut berubah)
	maka caranya dengan menambahkan tag nya di css nya dan di depan sintaks class nya, 
	contoh : di HTMl <h3 class="kelas bersama">Tentang saya</h3>
			 <p class="kelas bersama">lorem</p>
		  di css p .kelas bersama {
				text-align: justify;
				text-indent: 15px;
				}
4. selector kompleks

teknik grouping
apabila ingin memberi style yang sama pada lebih dari 1 tag HTML maka bisa digabung dengan operator (,) yang berarti dan.
contoh : di HTMl <h1>Selamat Datang</h1>
		 <h2>Daftar isi</h2>
	 di css h1, h2 {
		font-weight: bold;
		font-family: arial;
		}

apabila ingin memberi style pada elemen atau tag yang berada dalam tag lain (sebagai child) maka bisa gunakan operator spasi ( ) yang berarti didalam.
contoh : di HTML <ul>
		<li><a ="href: www.https//github.com">link-1</a></li>
		</ul>
	 di css ul li a {
		   font-weight: bold:
		   }


pseudo class
   adalah kelas semu yang dimiliki oleh sebuah element HTML yang membuat kita bisa mendefinisikan style pada keadaan tertentu.
parameternya yaitu titik dua (:).
macam-macam pseudo class ada 2, yaitu :
1. Pseudo class yang berhubungan dengan link
2. Pseudo class yang berhubungan dengan posisi elemen

1. Pseudo class yang berhubungan dengan link, terdapat 4 property, yaitu:
	1. :link, yaitu defaultnya link pada a yang memiliki href
	2. :hover, yaitu style ketika kursor mouse berada pada link/elemennya (mouse over)
	3. :active, yaitu style ketika kita klik link/elemennya
	4. :visited, yaitu style ketika linknya sudah dikunjungi
	contoh :
	<p>klik <a href="halaman2.html">disini</a> untuk informasi lebih lanjut.</p>
	1. a :link {
		color:green;
		}
	
	2. a :hover {
		font-size: 15px;
		color: yellow;
		}

	3. a :active {
		color: blue;
		}

	4. a :visited {
		color : black;
		}

2. Pseudo class yang berhubungan dengan posisi elemen, terdapat 5 property, yaitu:
	1. :First-child, yaitu style untuk memilih elemen pertama pada sebuah parent (tag pembungkusnya)
	2. :last-child, yaitu style untuk memilih elemen terakhir pada sebuah parent (tag pembungkusnya)
	3. :nth-child, yaitu style untuk memilih; 1. elemen pada urutan tertentu
						 2. elemen pada kelipatan bilangan tertentu (n)
					 	 3. elemen pada kelipatan bilangan tertentu dan dimulai dari satu (3n-2)
						 4. elemen pada bilangan ganji atau genap (even) dan (odd)
	4. :first-of-tipe, yaitu style untuk memilih elemen pertama dari sebuah tipe tag (tidak memiliki parent)
	5. :last-of-tipe, yaitu style untuk memilih elemen terakhir dari sebuah tipe tag (tidak memiliki parent)

Inheritance
adalah ketika sebuah elemen mewarisi value dari property yang dimiliki oleh elemen parent nya.
kadang kala ada elemen yang tidak bisa mewarisi value dari property elemen parent nya karena keadaan default nya, 
maka disini lah fungsi inheritance, agar elemen tadi bisa untuk mewarisi value dari property element parentnya.
contoh :

di HTML nya

<body>

<p>klik <a href="https://github.com">disini</a> untuk informasi lebih lanjut.</p>

</body>

di css nya

body {
  color:black;
   }

a {color: inherit;}


Specificity
adalah kadar spesifik dari suatu elemen. setiap deklarasi/perintah didalam css terdapat suatu selector memiliki berat yang berbeda,
berat ini menentuan seberapa spesifik suatu elemen dan deklarasi yang akan dipilih oleh css untuk dijalankan.
nilai berat suatu selector, dari paling berat ke paling ringan.
1. inline	= 1000 beratnya
2. id		= 100 beratnya
3. class	= 10 beratnya
4. elemen HTML	= 1 beratnya

maka jika selector yang kita pilih kalah berat dengan selector lain, maka kita bisa menambah berat selector tersebut supaya lenih berat.
