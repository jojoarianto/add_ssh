#SSH tutorial

Dibawah ini tutorial langkah yang digunakan untuk menambahkan ssh ke dalam akun github.

- Buka command line (saya menggunakan sistem operasi linux ubuntu)
- Masukkan perintah  ```$ cd ~/.ssh``` perintah itu artinya berpindah ke direktori tempat data ssh akan disimpan

- Masukkan perintah untuk mengenerate keygen ssh 
```$ ssh-keygen -t rsa -C 'email github anda' ```
- masukkan nama key rsa anda (saya sarankan menggunakan nama git_rsa karena nama itu merupakan standar)
- Setelah itu harus memasukkan passphrase (password) namun passphrase ini dapat dikosongkan.Silahkan di kosongkan saja jika merasa belum perlu
- Tunggu beberapa saat sampai proses generate selesai. Setelah selesai maka akan muncul pesan bahwa public key telah tersimpan didalam git_rsa
- Selanjutnya buka file git_rsa anda untuk mengopi value dari ssh anda. caranya silahkan buka dengan text editor atau dengan perintah
```$ gksudo gedit git_rsa.pub```
kemudian copy semua isi dari file git_rsa.pub tersebut.
- Selanjutnya buka github.com
- Silahkan masuk ke menu setting profile anda kemudian klik link untuk ssh keys
- Tekan tombol add ssh key, kemudian masukkan title (bebas) dan value (hasil copyan dari file git_rsa.pub) kemudian tekan simpan.
- Setelah ssh laptop anda tersimpan selanjutnya adalah mengetes koneksi ssh anda
silahkan masukkan perintah ini di command line anda ```$ ssh -T git@github.com``` 
- Jika berhasil maka akan tampil pesan Hi jojoarianto! You've successfully authenticated

Joko Irianto