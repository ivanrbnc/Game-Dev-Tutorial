# Tutorial 2

## Pertanyaan
1. **Apa saja pesan log yang dicetak pada panel Output?**
    * Pesan yang dicetak berupa:    
        * *Platform initialized*  : Ketika platform pertama kali dibuat
        * *Reached objective!*    : Ketika pesawat menyentuh objektif, yaitu pojok kiri atas dari map

2. **Coba gerakkan landasan ke batas area bawah, lalu gerakkan kembali ke atas hingga hampir menyentuh batas atas. Apa saja pesan log yang dicetak pada panel Output?**
    * Serupa dengan pertanyaan nomor satu, yaitu *Platform initialized* dan *Reached objective!*

3. **Buka scene MainLevel dengan tampilan workspace 2D. Apakah lokasi scene ObjectiveArea memiliki kaitan dengan pesan log yang dicetak pada panel Output pada percobaan sebelumnya?**
    * Iya, *scene* `ObjectiveArea` berkaitan dengan pesan log yang dicetak. Dilihat dari *script*, bentuk dari *scene* `ObjectiveArea` merupakan penanda bahwa pesawat menyentuh objektifnya. 

4. **Scene BlueShip dan StonePlatform sama-sama memiliki sebuah child node bertipe Sprite. Apa fungsi dari node bertipe Sprite?**
    * `Sprite` pada `BlueShip` dan `StonePlatform` adalah tekstur atau tampilan yang memudahkan *user* membedakan suatu *scene* dengan *scene* lainnya. Dengan kata lain, `Sprite` adalah wujud nyata yang ditampilkan.

5. **Root node dari scene BlueShip dan StonePlatform menggunakan tipe yang berbeda. BlueShip menggunakan tipe RigidBody2D, sedangkan StonePlatform menggunakan tipe StaticBody2D. Apa perbedaan dari masing-masing tipe node?**
    * `RigidBody2D` adalah bentuk badan yang berkaitan dengan *law of physics*. `RigidBody2D` cocok untuk digunakan sebagai "*player*" karena dapat bersifat dinamis, salah satunya adalah bergerak.
    * Berkebalikan dengan `RigidBody2D`, `StaticBody2D` tidak berkaitan dengan *law of physics*. Dapat dikatakan bahwa `StaticBody2D` cocok untuk digunakan sebagai *building blocks* atau benda-benda yang bergerak secara statis.

6. **Ubah nilai atribut Mass dan Weight pada tipe RigidBody2D secara bebas di scene BlueShip, lalu coba jalankan scene MainLevel. Apa yang terjadi?**
    * Secara ekspektasi, ketika *mass* dan *weight* diubah, seharusnya gaya gravitasi atau pergerakan pesawat tersebut menjadi semakin berat atau ringan. Akan tetapi, ketika *scene* `MainLevel` dijalankan, tidak ada perubahan yang terjadi. Hal tersebut berkemungkinan besar dipengaruhi oleh tidak adanya *script* yang menggunakan *mass* dan *weight*.

7. **Ubah nilai atribut Disabled pada tipe CollisionShape2D di scene StonePlatform, lalu coba jalankan scene MainLevel. Apa yang terjadi?**
    * `Sprite` pesawat dan `StonePlatform` tidak dapat bersentuhan.

8. **Pada scene MainLevel, coba manipulasi atribut Position, Rotation, dan Scale milik node BlueShip secara bebas. Apa yang terjadi pada visualisasi BlueShip di Viewport?**
    * Manipulasi pada atribut `Position` akan mengubah letak posisi pesawat saat dimulai
    * Manipulasi pada atribut `Rotation` akan mengubah derajat dari pesawat saat dimulai
    * Manipulasi pada atribut `Scale` akan memberikan *scaling* pada pesawat saat dimulai

9. **Pada scene MainLevel, perhatikan nilai atribut Position node PlatformBlue, StonePlatform, dan StonePlatform2. Mengapa nilai Position node StonePlatform dan StonePlatform2 tidak sesuai dengan posisinya di dalam scene (menurut Inspector) namun visualisasinya berada di posisi yang tepat?**
    * Hal tersebut dikarenakan oleh posisi `StonePlatform` dan `StonePlatform2` diatur secara relatif terhadap `PlatformBlue` sehingga nilai position `PlatformBlue` dan `StonePlatform` pada *scene* `MainLevel` menjadi tidak sesuai dengan scene itu sendiri.

## Version
* Godot : 3.5.3

## Author 
* Ivan Rabbani Cezeliano (2106701892)