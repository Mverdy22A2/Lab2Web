# Langkah-langkah Praktikum

## 1. Membuat dokumen HTML
- Buatlah dokumen HTML seperti berikut

![Screenshot (3)](https://github.com/verz666/Lab2Web/assets/115523263/59e5d497-3d48-4011-8535-fef79012ea62)

## OUTPUT :

![Screenshot (4)](https://github.com/verz666/Lab2Web/assets/115523263/c9313857-2e8c-47b8-b0cc-e6b60cda6ae5)

## 2. Menambahkan deklarasi CSS internal
- Kemudian tambahkan deklarasi CSS internal seperti berikut pada bagian head dokumen.

![Screenshot (5)](https://github.com/verz666/Lab2Web/assets/115523263/800e8a97-cfa7-475b-9ce5-1919e8834dfb)

## OUTPUT : 

![Screenshot (6)](https://github.com/verz666/Lab2Web/assets/115523263/79108c35-5b18-41df-bedf-669009a599b9)

## 3. Menambahkan deklarasi inline CSS pada tag ``` <p> ```
- Kemudian tambahkan deklarasi inline CSS pada tag <p> seperti berikut.

![Screenshot (7)](https://github.com/verz666/Lab2Web/assets/115523263/66ca70f4-6fbd-4189-b8e3-4463cdf5fac2)

## OUTPUT :

![Screenshot (8)](https://github.com/verz666/Lab2Web/assets/115523263/1f907b40-efa3-4704-984d-45ba17db807e)

## 4. Menambahkan CSS Eksternal
- Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut.

![Screenshot (9)](https://github.com/verz666/Lab2Web/assets/115523263/57e71c11-53a5-484a-bb2e-9ac6f9e55630)

## - Kemudian tambahkan tag <link> untuk merujuk file css yang sudah dibuat pada bagian ```<head>```

![Screenshot (10)](https://github.com/verz666/Lab2Web/assets/115523263/cdce184b-926f-4613-9c7c-b47807fbe068)

## output :

![Screenshot (11)](https://github.com/verz666/Lab2Web/assets/115523263/74cb4ab0-add6-463d-8db1-e057f4a2634d)

## 5. Menambahkan CSS Selector
- Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file style_eksternal.css, tambahkan kode berikut.

![image](https://github.com/verz666/Lab2Web/assets/115523263/c11995fc-3803-435d-b4a2-6bc247f22798)

## OUTPUT :

![Screenshot (13)](https://github.com/verz666/Lab2Web/assets/115523263/a21e5484-bc87-45cc-8a56-d9c29ee7bf55)

## 6. validasi dokumen css

![Screenshot (14)](https://github.com/verz666/Lab2Web/assets/115523263/986fc36b-89d7-4c5f-8d78-224f4af3fa16)

# Pertanyaan dan Tugas
## 1. Apa perbedaan pendeklarasian CSS elemen ```h1 {...}``` dengan ```#intro h1 {...}```? berikan penjelasannya!
Pendeklarasian CSS ```h1 {...}``` dan ```#intro h1 {...}``` memiliki perbedaan dalam cara mereka mempengaruhi elemen HTML di halaman web. Ini berkaitan dengan penggunaan selektor CSS dan cara mereka mengaitkan gaya dengan elemen-elemen HTML.

1. ```h1 {...}```:

    - Ini adalah contoh dari selektor jenis (type selector).
    - Ini akan mempengaruhi semua elemen ```<h1>``` di seluruh halaman web.
    - Gaya yang dideklarasikan dalam blok tersebut akan diterapkan pada semua elemen ```<h1>``` di halaman tanpa memperhatikan di mana elemen-elemen tersebut berada dalam struktur dokumen HTML.

2. ```#intro h1 {...}```:

    - Ini adalah contoh dari selektor keturunan (descendant selector).
    - Ini akan mempengaruhi semua elemen ```<h1>``` yang terletak dalam elemen dengan ID "intro".
    - Gaya yang dideklarasikan dalam blok tersebut akan diterapkan hanya pada elemen-elemen ```<h1>``` yang berada di dalam elemen dengan ID "intro" dalam struktur dokumen HTML.
    - Ini berarti elemen ```<h1>``` di luar elemen "intro" tidak akan mendapatkan gaya yang sama.

- Contoh HTML untuk menjelaskan perbedaan ini:

      ```html
      Copy code
      <!DOCTYPE html>
      <html>
      <head>
          <style>
              h1 {
                  color: blue;
              }
              #intro h1 {
                  font-size: 24px;
              }
          </style>
      </head>
      <body>
          <h1>Ini adalah elemen h1 di luar elemen "intro".</h1>
          <div id="intro">
              <h1>Ini adalah elemen h1 di dalam elemen "intro".</h1>
          </div>
      </body>
      </html>

Dalam contoh di atas, elemen ```<h1>``` di luar elemen "intro" akan memiliki warna teks biru, karena itu terpengaruh oleh deklarasi ```h1 {...}```. Sementara itu, elemen ```<h1>``` di dalam elemen "intro" akan memiliki ukuran font 24px, karena itu terpengaruh oleh deklarasi ```#intro h1 {...}```. Ini menunjukkan perbedaan penting dalam cara selektor CSS berinteraksi dengan struktur HTML untuk mengatur gaya elemen.

---------------

## 2. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!

Ketika Kita memiliki deklarasi CSS secara internal, eksternal, dan inline yang mengarah ke elemen yang sama di halaman web, maka aturan CSS yang akan diterapkan oleh browser akan mengikuti konsep prioritas dan spesifisitas. Di bawah ini adalah urutan prioritas dari yang paling tinggi hingga yang paling rendah:

1. Inline CSS: Inline CSS memiliki prioritas tertinggi. Deklarasi CSS yang ada dalam atribut ```style``` elemen HTML akan selalu menggantikan aturan CSS lainnya.

    - Contoh:

      ```html
      <p style="color: red;">Ini adalah teks dengan inline CSS.</p>

2. Internal CSS: Deklarasi CSS dalam elemen ```<style>``` dalam tag ```<head>``` dokumen HTML memiliki prioritas di atas CSS eksternal, tetapi di bawah inline CSS.

    - Contoh:

    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <style>
            p {
                color: blue;
            }
        </style>
    </head>
    <body>
        <p>Ini adalah teks dengan internal CSS.</p>
    </body>
    </html>

3. External CSS: Deklarasi CSS dalam file eksternal yang disematkan (misalnya, stylesheet.css) memiliki prioritas di bawah inline dan internal CSS.

    - Contoh:

    ```html

    <!DOCTYPE html>
    <html>
    <head>
        <link rel="stylesheet" type="text/css" href="stylesheet.css">
    </head>
    <body>
        <p>Ini adalah teks dengan eksternal CSS.</p>
    </body>
    </html>

Jika ada konflik antara deklarasi CSS dari berbagai sumber (inline, internal, dan eksternal), aturan CSS dengan prioritas tertinggi akan digunakan oleh browser. Oleh karena itu, dalam contoh-contoh di atas, teks dalam paragraf akan memiliki warna yang berbeda sesuai dengan aturan CSS yang diberikan.

Perlu diingat bahwa baik internal maupun eksternal CSS dapat memiliki lebih dari satu aturan yang berpengaruh pada elemen yang sama. Dalam hal ini, spesifisitas dan urutan deklarasi dalam file CSS akan menjadi faktor yang lebih mendalam untuk menentukan aturan mana yang akan digunakan oleh browser. Semua ini disebut dalam konsep yang dikenal sebagai "kaskade" (cascading) dalam CSS.

------------------

## 3. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! ```( <p id="paragraf-1" class="text-paragraf"> )```

Ketika sebuah elemen HTML memiliki ID dan class yang diberikan, dan masing-masing selector tersebut memiliki deklarasi CSS, maka urutan prioritas akan memengaruhi aturan CSS yang akan diterapkan oleh browser. Di bawah ini adalah urutan prioritas yang berlaku:

1. ID Selector: ID selector memiliki prioritas tertinggi dalam CSS. Deklarasi CSS yang menggunakan ID selector akan menggantikan aturan CSS lainnya.

2. Class Selector: Class selector memiliki prioritas di bawah ID selector. Jika tidak ada ID selector yang sesuai, class selector akan diterapkan.

Untuk memberikan penjelasan lebih lanjut, berikut adalah contoh elemen HTML yang Anda sebutkan:

    ```html
    <p id="paragraf-1" class="text-paragraf">Ini adalah paragraf.</p>

Jika Kita memiliki deklarasi CSS seperti ini:

    ```css
    #paragraf-1 {
        color: blue;
    }

    .text-paragraf {
        color: red;
    }

Maka, dalam kasus ini, aturan CSS yang akan diterapkan adalah aturan yang menggunakan ID selector, yaitu ```#paragraf-1```. Oleh karena itu, teks dalam paragraf akan berwarna biru, sesuai dengan deklarasi CSS yang menggunakan ID selector.

Namun, jika Kita membalikkan urutan deklarasi CSS seperti ini:

    ```css
    .text-paragraf {
        color: red;
    }

    #paragraf-1 {
        color: blue;
    }

Maka aturan yang akan diterapkan adalah aturan yang menggunakan class selector, yaitu ```.text-paragraf```. Oleh karena itu, teks dalam paragraf akan berwarna merah.

Dalam kasus ini, perhatikan bahwa urutan deklarasi dalam file CSS sangat penting untuk menentukan aturan mana yang akan digunakan oleh browser ketika ada konflik antara ID dan class selector pada elemen yang sama.
