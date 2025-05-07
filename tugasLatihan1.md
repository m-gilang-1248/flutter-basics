# Tugas Latihan 1
 1. Bagaimana cara membuat project Flutter menggunakan terminal/cmd?
 > Buka terminal, lalu ketikkan ```bash flutter create project_flutter_pertama```
 2. Apa aturan dalam memberikan nama project pada Flutter?
 > Semua huruf kecil
 > Bila terdapat lebih dari 1 kata, dihubungkan dengan karakter underscore
 3. Apa saja folder yang secara khusus disiapkan oleh Flutter untuk menjalankan aplikasi pada platform tertentu?
 > Folder, android, ios, linux, macos, web, dan windows adalah folder yang sudah disiapkan khusus oleh flutter supaya aplikasi yang kita buat bisa di jalankan di platform tersebut.
 4. Apa fungsi dari folder .dart_tools dan .idea?
 > Folder .idea ini menyimpan beberapa konfigurasi untuk android studio. Karena kita nantinya tidak menggunakan android studio untuk editornya, maka kita tidak butuh untuk mengubah apapun di dalam folder ini.

> Folder .dart_tool sendiri berisi konfigurasi dart package yang di generate oleh flutter. Folder ini pun tidak perlu kita ubah-ubah. Dapat kita abaikan terlebih dahulu.
 5. Bagaimana cara membuka project Flutter menggunakan Visual Studio Code?
 > Membuka folder project dengan shortcut ```bash CTRL + M + O```
 6. Mengapa kita perlu memastikan Android SDK terinstall untuk menjalankan aplikasi Flutter di sistem operasi Android?
 > Menginstal Android SDK sangat penting untuk menjalankan aplikasi Flutter di sistem operasi Android karena SDK ini menyediakan alat dan pustaka yang diperlukan untuk membangun, menguji, dan menjalankan aplikasi Android.
 7. Apa langkah-langkah untuk mengatasi masalah "Android Toolchain error" pada perintah flutter doctor?
 > Jika Anda mengalami **"Android Toolchain error"** saat menjalankan `flutter doctor`, berikut beberapa langkah yang dapat membantu mengatasinya:

 > 1. **Periksa Instalasi Android SDK**  
   - Pastikan Android SDK telah terinstal dengan benar.  
   - Buka **Android Studio** > **SDK Manager** > **SDK Tools** dan pastikan **Android SDK Command-line Tools (Latest)** telah diinstal.

 > 2. **Terima Lisensi Android SDK**  
   - Jalankan perintah berikut di terminal atau command prompt:  
     ```
     flutter doctor --android-licenses
     ```
   - Ikuti instruksi untuk menerima semua lisensi yang diperlukan.

 > 3. **Pastikan Path SDK Sudah Benar**  
   - Periksa apakah path SDK sudah dikonfigurasi dengan benar.  
   - Cek dengan perintah:  
     ```
     echo $ANDROID_HOME
     ```
   - Jika perlu, tambahkan path SDK ke variabel lingkungan.

 > 4. **Perbarui atau Instal Ulang SDK Manager**  
   - Jika error terkait dengan **cmdline-tools**, coba jalankan:  
     ```
     sdkmanager --install "cmdline-tools;latest"
     ```
   - Pastikan `sdkmanager` tersedia di direktori SDK.

 > 5. **Restart Android Studio dan Coba Lagi**  
   - Setelah melakukan perubahan, tutup dan buka kembali Android Studio.  
   - Jalankan `flutter doctor` lagi untuk memeriksa apakah masalah telah teratasi.

 8. Bagaimana cara menambahkan Android SDK Command-line tools melalui Android Studio?
 > - Buka Android Studio
 > - Jalankan Android Studio di komputer Anda.
 > - Akses SDK Manager
 > - Klik File > Settings (Windows/Linux) atau Android Studio > Preferences (Mac).
 > - Pilih Appearance & Behavior > System Settings > Android SDK.
 > - Pilih Tab SDK Tools
 > - Di dalam SDK Manager, buka tab SDK Tools.
 > - Centang opsi Android SDK Command-line Tools (Latest).
 > - Instal Command-line Tools
 > - Klik Apply atau OK untuk memulai proses instalasi.
 > - Tunggu hingga proses selesai.
 > - Verifikasi Instalasi
 > - Buka terminal atau command prompt dan jalankan perintah berikut untuk memastikan alat telah terinstal:

 9. Apa fungsi dari file .gitignore dalam struktur folder Flutter?
 > .gitignore berisi list folder atau file yang tidak akan ikut masuk kedalam git repository ketika kita push ke repository tersebut.
 10. Mengapa file pubspec.yaml sangat penting dalam pengembangan aplikasi Flutter?
 > Pubspec.yml merupakan file yang akan sering kita gunakan. File ini yang memungkinan kita untuk mengelola sebagian besar dependensi project kita.
 11. Apa yang dimaksud dengan widget dalam konteks Flutter?
 > Flutter adalah tentang widget, dan setiap aplikasi yang kita buat hanya sekumpulan widget dan widget adalah blok penyusun UI yang dapat kita lihat di layar. Lihat yang saya kotakin merah, itu semua adalah widget. Jika disatukan di dalam satu widget, akan menjadi tampilan yang sesuai dengan kebutuhan UI.
 12. Bagaimana pewarisan (inheritance) digunakan dalam pembuatan widget Flutter?
 > Cara pewarisan class yang sudah dibuat oleh flutter adalah dengan menambahkan kata kunci extends setelah nama class dan sebelum kurung kurawal dan memberitahu dart bahwa class ini akan mewarisi class lain dan kita hanya dapat memperluas atau mewarisi satu class dalam satu waktu.
 13. Apa peran widget MaterialApp dalam pembuatan aplikasi Flutter?
 > MaterialApp ini memiliki beberapa argumen yang dapat kita gunakan, janis argumennya adalah named argument. Seperti contoh disamping, saya menggunakan argument home untuk memasukan widget text yang bertuliskan Coding Flutter ke dalam widget MaterialApp yang nantinya akan diteruskan ke widget tree MyApp lalu di eksekusi dengan runApp dan akhirnya bisa tampil dilayar.
 14. Mengapa kita membutuhkan fungsi runApp untuk menjalankan aplikasi Flutter?
 > runApp sendiri function yang disediakan oleh flutter untuk menjalankan aplikasi flutter setelah aplikasi android atau ios di-boot. Alurnya dia akan mencoba mengambil widget tree yang kita buat, dan menggambarnya ke layar yang didasarkan pada widget tree tersebut. Jadi disini dia akan menggambar text Coding Flutter ke layar.
 15. Apa kegunaan widget Scaffold dalam struktur aplikasi Flutter?
 > runApp sendiri function yang disediakan oleh flutter untuk menjalankan aplikasi flutter setelah aplikasi android atau ios di-boot. Alurnya dia akan mencoba mengambil widget tree yang kita buat, dan menggambarnya ke layar yang didasarkan pada widget tree tersebut. Jadi disini dia akan menggambar text Coding Flutter ke layar.
 16. Bagaimana cara menambahkan app bar dan body pada widget Scaffold?
 > Di Flutter, bisa menambahkan **AppBar** dan **Body** ke dalam **Scaffold** dengan mudah menggunakan properti yang sudah tersedia. Berikut contoh sederhana cara melakukannya:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text("Contoh AppBar"),
          backgroundColor: Colors.blue,
        ),
        body: Center(
          child: Text(
            "Halo, ini adalah Body!",
            style: TextStyle(fontSize: 20),
          ),
        ),
      ),
    );
  }
}
```
 17. Apa perbedaan antara Stateless Widget dan Stateful Widget?
 > Stateless sendiri widget yang tidak memiliki state, sehingga perubahan dan hasil render UI nya itu ditentukan oleh inputan yang masuk kedalam stateless widget tersebut.
 > Untuk stateful dia adalah widget yang memiliki state didalamnya. Sehingga class yang meng extends class statefulwidget, akan dapat memiliki internal state nya sendiri, hal ini dapat menguntungkan karena render UI nya tidak hanya bergantung dari inputan dari widget lain, namun dengan memanggil setState maka widget build akan re-run ulang dengan state yang baru tanpa harus menunggu perubahan di widget tree atas nya.
 18. Mengapa Stateful Widget disebut memiliki state internal?
 > Untuk stateful dia adalah widget yang memiliki state didalamnya. Sehingga class yang meng extends class statefulwidget, akan dapat memiliki internal state nya sendiri, hal ini dapat menguntungkan karena render UI nya tidak hanya bergantung dari inputan dari widget lain, namun dengan memanggil setState maka widget build akan re-run ulang dengan state yang baru tanpa harus menunggu perubahan di widget tree atas nya.
 19. Berikan contoh penggunaan Stateless Widget dalam pembuatan aplikasi Flutter.
 > **StatelessWidget** adalah widget di Flutter yang bersifat immutable, artinya tidak memiliki state yang bisa berubah selama siklus hidupnya. Widget ini cocok untuk tampilan yang tidak berubah seperti teks atau gambar statis.

Berikut contoh sederhana penggunaan **StatelessWidget** dalam aplikasi Flutter:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text("Contoh Stateless Widget"),
        ),
        body: Center(
          child: MyTextWidget(),
        ),
      ),
    );
  }
}

class MyTextWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Text(
      "Halo, ini adalah contoh Stateless Widget!",
      style: TextStyle(fontSize: 20, fontWeight: FontWeight.bold),
    );
  }
}
```
 20. Berikan contoh penggunaan Stateful Widget dalam pembuatan aplikasi Flutter beserta alasan penggunaannya.
 > **StatefulWidget** digunakan dalam Flutter ketika suatu tampilan perlu berubah berdasarkan interaksi pengguna atau data yang diperbarui. Ini cocok untuk fitur seperti tombol yang bisa diklik, formulir yang diperbarui secara dinamis, atau animasi yang berubah seiring waktu.

Berikut contoh **StatefulWidget** untuk tombol yang mengubah teks saat ditekan:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text("Contoh Stateful Widget"),
        ),
        body: Center(
          child: MyStatefulWidget(),
        ),
      ),
    );
  }
}

class MyStatefulWidget extends StatefulWidget {
  @override
  _MyStatefulWidgetState createState() => _MyStatefulWidgetState();
}

class _MyStatefulWidgetState extends State<MyStatefulWidget> {
  String _text = "Tekan tombol untuk mengubah teks";

  void _updateText() {
    setState(() {
      _text = "Teks telah berubah!";
    });
  }

  @override
  Widget build(BuildContext context) {
    return Column(
      mainAxisAlignment: MainAxisAlignment.center,
      children: [
        Text(
          _text,
          style: TextStyle(fontSize: 20),
        ),
        SizedBox(height: 20),
        ElevatedButton(
          onPressed: _updateText,
          child: Text("Tekan Saya"),
        ),
      ],
    );
  }
}
```