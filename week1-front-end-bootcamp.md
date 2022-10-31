# Rangukam WEEK 1 - Front-end Bootcamp

## **React JS**

- ### **Apa Itu React JS ?**

  React JS adalah library JavaScript yang biasa digunakan saat membangun UI suatu website atau aplikasi web.

  Jadi, React JS bisa dianggap seperti perpustakaan yang berisi berbagai kode JavaScript yang sudah tertulis (pre-written). kita tinggal mengambil kode yang ingin kita gunakan. Sehingga, ini membuat proses coding menjadi lebih efisien dengan framework JavaScript tersebut.

  Selain itu, ada dua fitur tambahan yang menjadi keunggulannya yaitu JSX dan Virtual DOM.

- ### **Apa itu JSX ?**

  JSX adalah extension syntax JavaScript yang memungkinkan kita untuk memodifikasi **Document Object Model (DOM)** dengan kode bergaya HTML.

  Untuk mengetahui fungsi JSX dengan lebih jelas, kita perlu tahu tentang DOM terlebih dahulu.

  DOM adalah application programming interface (API) yang berfungsi untuk mengatur struktur halaman web. Nah, untuk menambah konten dinamis ke dalam halaman web, developer mesti memodifikasi DOM.

  Dengan kata lain, JSX akan mempermudah kita untuk menambah konten dinamis. Karena extension ini dapat membantu kita untuk memasukkan syntax bergaya HTML ke dalam DOM.

  Akan tetapi, JSX bukanlah HTML. Mungkin bahasa sederhananya seperti ini: JSX terlihat seperti HTML, tapi memiliki fungsi seperti JavaScript.

- ### **Apa itu Virtual DOM ?**

  Ketika developer mengupdate DOM dengan menggunakan JSX, React JS akan membuat Virtual DOM, yaitu salinan dari DOM asli yang ingin diupdate.

  Nah, Virtual DOM berguna untuk melihat bagian dari DOM asli yang berubah.Ketika menemukan bagian yang perlu diubah, React JS akan mengubah bagian itu saja. Jadi, pengguna tidak perlu reload satu halaman untuk melihat perubahannya.

- ### **Cara Install React JS**

  1.  Download installer **node.js**. Node JS adalah virtual environment untuk framework lain, termasuk React. Lalu install sampai selesai.
  2.  Buatlah folder baru untuk install react. Contohnya di D:\React-JS
  3.  Buka command prompt (CMD), lalu ketikkan: npm -v
  4.  Sekarang, mari masuk ke folder instalasi react yang baru Anda buat. Ketik:
      - **d:**
      - **cd React-JS** (Anda bisa mengganti “React-JS” dengan nama folder yang Anda buat)
  5.  Ketik kode di bawah untuk menginstall react:
      - **npm install -g create-react-app**
  6.  Untuk mengecek kesuksesan proses instalasinya, Anda bisa cek versi reactnya dengan mengetik:

      - **create-react-app –version**

  7.  Nah, sekarang Anda tinggal membuat project react JS Anda yang pertama. Untuk melakukannya, ketikkan kode berikut berturut-turut:
      - **create-react-app web-react-saya** (Anda bisa mengganti “web-react-saya” dengan nama project yang lain)
      - **cd web-react-saya**
      - **npm start**

- ### **Konsep Dasar React Js**

  Pada dasarnya Reacjs hanya melakukan render komponen saat ada data yang berubah. Seperti namanya “React” ia akan breaksi saat ada perubahan data (reaktif).

  Lalu komponen itu apa?

  Komponen adalah bagian-bagian dari UI, contohnya seperti tombol, label, input, dll. Komponen juga bisa dibentuk dari komponen yang lain.

  Secara sederhana, langkah-langkah yang harus dilakukan untuk membuat aplikasi react adalah sebagai berikut:

  - Menambahkan library react ke HTML;
  - Membuat elemen HTML untuk wadah aplikasi;
  - Membuat komponen;
  - Me-render komponen ke HTML;

  Setiap aplikasi react membutuhkan sebuah wadah.

  Contoh :

  Kita membuat sebuah elemen div dengan id="app".

  ```html
  <div id="app"></div>
  ```

  Setiap komponen yang kita buat di React akan di-render atau ditampilkan ke dalam div tersebut.

- ### **Apa itu Component ?**

  Komponen adalah bagian-bagian yang menyusun aplikasi React. Reactjs bekerja dengan Virtual DOM. Nah, di dalam Virtual DOM ini.. kita harus membuat komponen untuk memberitahu React tentang apa saja yang harus ditampilkan (render) ke Real DOM (HTML).

  Karena itu, setiap komponen di React pasti akan menghasilkan HTML. Dan Komponen di React sendiri bersifat reuseable, artinya bisa digunakan kembali. Sehingga bisa memudahkan kita dalam bekerja.

  Secara umum, ada tiga bagian yang biasanya ada di dalam komponen:

  - Bagian Data (State, Props, Variabel)
  - Bagian method atau fungsi
  - Bagaian method render() (wajib ada jika menggunakan class).

- ### **Cara Membuat Component**

  Komponen di Reactjs dapat kita buat dengan dua cara:

  Pertama menggunakan fungsi, dan kedua menggunakan class. Komponen yang dibuat dengan fungsi disebut juga dengan function components dan yang menggunakan class disebut class components.

  Berikut ini cara membuat **function components**:

  ```javascript
  // membuat komponen dengan fungsi
  function Header() {
    return (
      <div>
        <h1>Tutorial Reactjs untuk Pemula</h1>
        <h2>Panduan step-by-step belajar Reactjs</h2>
      </div>
    );
  }

  // render komponen ke RealDOM
  ReactDOM.render(<Header />, document.getElementById("root"));
  ```

  Hasilnya :

  ![hasil function component](https://www.petanikode.com/img/react/komponen/function-component-demo.png)

  Sedangkan untuk **class component**, cara membuatnya harus melakukan extends dari class React.Component.

  Contoh :

  ```javascript
  // membuat komponen dengan class
  class Header extends React.Component {
    render() {
      return (
        <div>
          <h1>Tutorial Reactjs untuk Pemula</h1>
          <h2>Panduan step-by-step belajar Reactjs</h2>
          <p>Membuat komponen dengan class</p>
        </div>
      );
    }
  }

  // render komponen ke RealDOM
  ReactDOM.render(<Header />, document.getElementById("root"));
  ```

  Hasilnya :

  ![Hasil class component](https://www.petanikode.com/img/react/komponen/class-component-demo.avif)

- ### **State dan Props pada Komponen Reactjs**

  **State** adalah objek yang digunakan untuk menyimpan data di dalam komponen, sedangkan **props** adalah obejek yang digunakan untuk menyimpan data yang diterima dari luar komponen.

  Data yang disimpan di dalam state bisa kita ubah-ubah, sedangkan data yang disimpan di dalam props tidak bisa diubah karena sifatnya read-only.

- ### Cara memberi Style CSS pada React Js

  Kita bisa memberikan style CSS dengan beberapa cara, yaitu :

  1. Inline CSS
  2. Internal CSS
  3. Eksternal CSS

  Selain itu kita bisa menggunakan syntax dari boostrap, caranya kita bisa menggunakan perintah

  ```
  npm i bootstrap@5.2.0
  ```
