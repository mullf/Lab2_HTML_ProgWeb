# Lab2_HTML_ProgWeb
## Langkah-langkah Praktikum
### 1. Membuat dokumen HTML
- Buatlah dokumen HTML seperti berikut
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Dasar</title>
</head>
<body>
  <header>
    <h1>CSS Internal dan <i>Inline CSS</i></h1>
  </header>
  <nav>
    <a href="lab2_css_dasar.html">CSS Dasar</a>
    <a href="lab2_css_eksternal.html">CSS Eksternal</a>
    <a href="lab1_tag_dasar.html">HTML Dasar</a>
  </nav>
  <!-- CSS ID Selector -->
  <div id="intro">
    <h1>Hello World</h1>
<p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman
Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat
adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML
dan CSS.</p>
    <!-- CSS Class Selector -->
    <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
  </div>
</body>
</html>
```

- Selanjutnya buka pada brwoser untuk melihat hasilnya.

![Prak2_html1](https://github.com/mullf/Lab2_HTML_ProgWeb/assets/115521049/b5be1d42-4f6a-4cb7-ba79-065154c89eae)


### 2. Mendeklarasikan CSS Internal
- Kemudian tambahkan deklarasi CSS internal seperti berikut pada bagian head dokumen.
```
<head>
  <title>CSS Dasar</title>
  <style>
  body {
  font-family:'Open Sans', sans-serif;
  }
  header {
  min-height: 80px;
  border-bottom:1px solid #77CCEF;
  }
  h1 {
  font-size: 24px;
  color: #0F189F;
  text-align: center;
  padding: 20px 10px;
  }
  h1 i {
  color:#6d6a6b;
  }
  </style>
</head>
```

- Selanjutnya buka pada brwoser untuk melihat hasilnya.

![prak2_html2](https://github.com/mullf/Lab2_HTML_ProgWeb/assets/115521049/0e7236b2-7ef0-4347-a968-0627d04eb6a1)

### 3. Menambahkan Inline CSS
- Kemudian tambahkan deklarasi inline CSS pada tag ``<p>``seperti berikut.
```
<p style="color:#77CCEF">
```

- Simpan kembali dan refresh kembali browser untuk melihat perubahannya.

![prak2_html3](https://github.com/mullf/Lab2_HTML_ProgWeb/assets/115521049/928a2bd3-80a4-4a87-a011-56fa3a308245)

### 4. Membuat CSS Eksternal
- Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut.
```
nav {
  background: #20A759;
  color:#fff;
  padding: 10px;
}
nav a {
  color: #fff;
  text-decoration: none;
  padding:10px 20px;
}
nav .active,
nav a:hover {
  background: #0B6B3A;
}
```

- Kemudian tambahkan tag ``<link>`` untuk merujuk file css yang sudah dibuat pada bagian ``<head>``
```
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- menyisipkan css eksternal -->
    <link rel="stylesheet" href="style_eksternal.css" type="text/css">
    <title>CSS Dasar</title>
</head>
```

- Selanjutnya refresh kembali browser untuk melihat perubahannya.

![prak2_html4](https://github.com/mullf/Lab2_HTML_ProgWeb/assets/115521049/c7787f0a-08d0-4214-8237-d7a0342a9407)

## 5. Menambahkan CSS Selector
- Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file style_eksternal.css, tambahkan kode berikut.
```
/* ID Selector */
#intro {
  background: #418fb1;
  border: 1px solid #099249;
  min-height: 100px;
  padding: 10px;
}
#intro h1 {
  text-align: left;
  border: 0;
  color: #fff;
}
/* Class Selector */
.button {
  padding: 15px 20px;
  background: #bebcbd;
  color: #fff;
  display: inline-block;
  margin: 10px;
  text-decoration: none;
}
.btn-primary {
  background: #E42A42;
}
```

-Kemudian simpan kembali dan refresh browser untuk melihat perubahannya.

![prak2_html5](https://github.com/mullf/Lab2_HTML_ProgWeb/assets/115521049/5df090e7-6d76-4f9f-b6a1-1bb410016260)

# Pertanyaan dan Tugas
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
 
2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
  - Kalau h1 menggunakan internal dan inline pada penggunaan style nya sedangkan intro menggunakan eksternal css style nya

3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!

  - Ketika ada deklarasi CSS secara internal, CSS eksternal, dan inline CSS pada elemen yang sama, maka urutan keutamaan (specificity) akan menentukan deklarasi mana yang akan ditampilkan pada browser. Urutan prioritas biasanya adalah sebagai berikut, dari yang paling tinggi hingga yang paling rendah:

  - a. Inline CSS memiliki prioritas tertinggi.
  
  - b. Kemudian, deklarasi CSS yang ada dalam elemen `<style>` secara internal (internal CSS) akan digunakan jika ada konflik antara inline dan internal CSS.
  
  - c. Terakhir, deklarasi dari file CSS eksternal akan digunakan jika ada konflik dengan inline dan internal CSS.

4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! `( <p id="paragraf-1" class="text-paragraf"> )`
   

  - Ketika sebuah elemen HTML memiliki ID dan class, dan keduanya memiliki deklarasi CSS, maka deklarasi yang akan digunakan akan bergantung pada spesifikitas (specificity) dari selector tersebut. Secara umum, ID selector memiliki spesifikitas yang lebih tinggi daripada class selector. Oleh karena itu, jika ada konflik antara deklarasi CSS ID dan class, deklarasi dari ID akan digunakan.
