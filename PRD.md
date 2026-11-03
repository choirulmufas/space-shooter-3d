# PRODUCT REQUIREMENTS DOCUMENT (PRD)

# SPACE SHOOTER 3D

**Dokumen:** Product Requirements Document\
**Versi:** 1.0.0\
**Status:** Perencanaan\
**Platform:** Browser-based 3D Game\
**Genre:** Action, Arcade, Space Shooter\
**Mode:** Single Player\
**Target:** Desktop dan laptop; dukungan tablet sebagai peningkatan\
**Tagline:** Explore the Galaxy. Fight for Survival.

------------------------------------------------------------------------

## 1. Project Overview

### 1.1 Latar Belakang

Space Shooter 3D adalah game aksi bertema luar angkasa yang dapat
dimainkan langsung melalui browser tanpa mengharuskan pemain mengunduh
atau memasang aplikasi. Pemain mengendalikan pesawat tempur futuristik,
menghancurkan asteroid, melawan pesawat musuh, menghindari serangan,
mengumpulkan skor, dan menyelesaikan level dengan tingkat kesulitan yang
meningkat.

Game dirancang untuk memberikan pengalaman bermain yang mudah dipahami,
responsif, menarik secara visual, dan cukup menantang agar pemain ingin
bermain kembali.

### 1.2 Visi Produk

Menciptakan game 3D bertema luar angkasa yang interaktif, menarik secara
visual, mudah dimainkan, dan dapat diakses langsung melalui browser.

### 1.3 Tujuan Produk

1.  Menyediakan hiburan berbasis browser yang mudah diakses.
2.  Memberikan pengalaman bermain game 3D yang imersif.
3.  Menghadirkan mekanisme permainan sederhana tetapi menantang.
4.  Mendorong pemain meningkatkan skor dan menyelesaikan level.
5.  Mengoptimalkan performa agar game berjalan lancar pada perangkat
    desktop dan laptop.

### 1.4 Target Pengguna

**Pengguna utama:** - Remaja dan dewasa yang menyukai game aksi. -
Pengguna yang mencari hiburan singkat melalui browser. - Penggemar game
pesawat, luar angkasa, dan arcade shooter.

**Kebutuhan pengguna:** - Dapat langsung bermain tanpa registrasi. -
Kontrol pesawat mudah dipahami. - Visual 3D menarik. - Tantangan
meningkat secara bertahap. - Memiliki skor dan rekor untuk dikejar.

### 1.5 Masalah yang Ingin Diselesaikan

Pengguna membutuhkan hiburan yang cepat diakses, tidak membutuhkan
instalasi, dan menawarkan pengalaman bermain yang cukup menarik untuk
mengisi waktu luang. Space Shooter 3D menjawab kebutuhan tersebut
melalui permainan aksi singkat dengan kontrol sederhana dan progres yang
dapat diulang.

------------------------------------------------------------------------

## 2. Product Scope

### 2.1 Modul Utama

  -----------------------------------------------------------------------
  Modul                   Deskripsi               Prioritas
  ----------------------- ----------------------- -----------------------
  Layar Pertempuran       Kendali pesawat,        Critical
                          tembakan laser, dan     
                          manuver menghindar      

  Musuh & Asteroid        Rintangan, pesawat      Critical
                          musuh, serangan, dan    
                          ledakan sasaran         

  Darah & Game Over       Health bar, damage,     Critical
                          kondisi kalah, dan      
                          restart                 

  Skor & Rekor            Skor berjalan, high     High
                          score, dan leaderboard  
                          lokal                   

  Level Bertahap          Kenaikan level,         High
                          peningkatan kesulitan,  
                          variasi latar           

  Menu & Pengaturan       Menu utama, pause,      High
                          resume, dan pengaturan  
                          suara/kontrol           

  Efek Visual & Suara     Latar luar angkasa,     Medium
                          laser, ledakan, musik,  
                          dan SFX                 
  -----------------------------------------------------------------------

### 2.2 Ruang Lingkup MVP

Versi Minimum Viable Product (MVP) wajib memiliki: - Pesawat 3D yang
dapat dikendalikan. - Sistem tembakan laser. - Asteroid dan pesawat
musuh. - Collision detection. - Health dan damage. - Game Over dan
restart. - Skor berjalan. - Menu utama dan HUD gameplay.

### 2.3 Fitur di Luar Scope MVP

Fitur berikut tidak menjadi prioritas versi pertama: - Multiplayer
online dan PvP. - Sistem akun dan autentikasi. - Pembelian item dalam
game. - Mata uang virtual. - Kustomisasi pesawat kompleks. - Campaign
dengan cerita sinematik panjang. - Leaderboard global berbasis server.

Fitur tersebut dapat dipertimbangkan pada versi lanjutan.

------------------------------------------------------------------------

## 3. Gameplay Design

### 3.1 Konsep Permainan

Space Shooter 3D menggunakan perspektif third-person dari belakang dan
sedikit di atas pesawat. Pesawat bergerak dalam area pertempuran luar
angkasa. Lingkungan bergerak secara konsisten untuk menciptakan kesan
pesawat sedang melaju melewati ruang angkasa.

Pemain harus: 1. Mengendalikan pesawat. 2. Menembakkan laser. 3.
Menghancurkan asteroid. 4. Mengalahkan pesawat musuh. 5. Menghindari
tabrakan dan serangan. 6. Mengumpulkan skor. 7. Bertahan hidup dan
menyelesaikan level.

### 3.2 Core Gameplay Loop

1.  Pemain membuka game dan melihat Main Menu.
2.  Pemain memilih Start Game.
3.  Game menyiapkan pesawat dan arena.
4.  Asteroid dan musuh mulai muncul.
5.  Pemain bergerak, menembak, dan menghindari rintangan.
6.  Objek yang dihancurkan memberikan skor.
7.  Sistem memeriksa health dan target level.
8.  Jika health mencapai nol, game masuk ke Game Over.
9.  Jika target level tercapai, level meningkat dan kesulitan bertambah.
10. Pemain dapat mengulang permainan atau kembali ke menu utama.

### 3.3 Perspektif dan Lingkungan

-   Kamera berada di belakang dan sedikit di atas pesawat.
-   Pesawat pemain harus terlihat jelas selama permainan.
-   Lingkungan memiliki kedalaman 3D.
-   Bintang bergerak sebagai latar belakang.
-   Asteroid memiliki ukuran, rotasi, dan kecepatan berbeda.
-   Planet dan nebula menjadi objek dekoratif.
-   Kamera mengikuti pergerakan pesawat secara halus.
-   Area permainan memiliki batas agar pemain tidak keluar arena.

------------------------------------------------------------------------

## 4. Functional Requirements

### 4.1 Layar Pertempuran

#### FR-01 --- Kendali Pesawat

**Deskripsi:** Pemain dapat mengendalikan pesawat menggunakan keyboard.

Kebutuhan: - Pesawat bergerak ke kiri dan kanan. - Pesawat bergerak ke
atas dan bawah. - Pesawat memiliki batas pergerakan arena. - Gerakan
menggunakan animasi halus dan konsisten. - Kamera mengikuti pergerakan
pesawat. - Pesawat kembali ke posisi awal ketika permainan dimulai.

**Acceptance Criteria:** - Input keyboard menghasilkan gerakan sesuai
arah. - Kombinasi beberapa tombol dapat digunakan bersamaan. - Pesawat
tidak dapat keluar dari batas arena. - Kecepatan gerak tidak bergantung
pada frame rate.

#### FR-02 --- Tembak Laser

**Deskripsi:** Pemain menembakkan laser untuk menghancurkan asteroid dan
pesawat musuh.

Kebutuhan: - Laser muncul dari bagian depan pesawat. - Tembakan dapat
dilakukan berulang kali. - Laser memiliki animasi dan efek cahaya. -
Laser mendeteksi tabrakan dengan objek. - Laser dihapus setelah mengenai
target atau melewati batas arena. - Terdapat cooldown antar-tembakan
untuk menjaga keseimbangan.

**Acceptance Criteria:** - Tombol tembak menghasilkan proyektil laser. -
Laser bergerak sesuai arah tembakan. - Laser dapat mengenai target dan
memicu damage. - Satu laser tidak memberikan damage berulang pada target
yang sama.

#### FR-03 --- Manuver Menghindar

Kebutuhan: - Pemain dapat menghindari asteroid dan proyektil musuh. -
Gerakan pesawat harus responsif. - Tabrakan dengan objek berbahaya
mengurangi health. - Pesawat tidak boleh menembus batas arena.

### 4.2 Musuh & Asteroid

#### FR-04 --- Asteroid Melayang

**Deskripsi:** Asteroid menjadi rintangan yang bergerak menuju area
pemain.

Kebutuhan: - Asteroid muncul secara acak dalam batas spawn yang
ditentukan. - Asteroid memiliki variasi ukuran. - Asteroid bergerak
dengan kecepatan berbeda. - Asteroid memiliki animasi rotasi. - Asteroid
dapat dihancurkan menggunakan laser. - Asteroid yang dihancurkan
memberikan skor. - Asteroid yang menabrak pemain mengurangi health. -
Asteroid yang melewati area permainan dibersihkan.

#### FR-05 --- Pesawat Musuh

**Deskripsi:** Pesawat musuh menjadi lawan utama pemain.

Kebutuhan: - Musuh muncul dari area depan arena. - Musuh memiliki
variasi bentuk dan warna. - Musuh bergerak mengikuti pola sederhana. -
Musuh dapat menembakkan proyektil. - Musuh dapat dihancurkan oleh laser
pemain. - Musuh memberikan skor ketika dikalahkan. - Tingkat kesulitan
musuh meningkat seiring kenaikan level.

#### FR-06 --- Ledakan Sasaran

Kebutuhan: - Terdapat efek ledakan ketika asteroid dihancurkan. -
Terdapat efek ledakan ketika pesawat musuh dihancurkan. - Efek ledakan
menggunakan partikel dan animasi. - Efek suara ledakan dapat diputar. -
Objek yang hancur dihapus setelah animasi selesai. - Efek visual tidak
boleh menyebabkan penurunan performa berlebihan.

### 4.3 Darah & Game Over

#### FR-07 --- Bar Kesehatan

Health menunjukkan kondisi pesawat pemain.

Parameter awal yang direkomendasikan:

  Parameter                   Nilai
  ------------------------ --------
  Health maksimum            100 HP
  Tabrakan asteroid          -20 HP
  Proyektil musuh            -15 HP
  Tabrakan pesawat musuh     -30 HP
  Health minimum               0 HP

Kebutuhan: - Health bar tampil selama permainan. - Health berkurang
ketika pemain menerima damage. - Warna health bar berubah sesuai
kondisi. - Pesawat mendapat efek visual ketika terkena serangan. -
Health tidak boleh kurang dari nol. - Permainan berakhir ketika health
mencapai nol. - Damage tidak boleh dihitung berulang kali selama satu
kejadian tabrakan yang sama; gunakan aturan cooldown/invulnerability
singkat jika diperlukan.

#### FR-08 --- Layar Game Over

Ketika health pemain habis: 1. Hentikan pergerakan objek gameplay. 2.
Hentikan proses spawn musuh dan asteroid. 3. Hentikan aktivitas
tembakan. 4. Tampilkan layar Game Over. 5. Tampilkan skor akhir. 6.
Tampilkan level terakhir. 7. Tampilkan rekor tertinggi. 8. Sediakan
tombol Main Lagi dan Menu Utama.

#### FR-09 --- Main Ulang Cepat

Ketika tombol Main Lagi ditekan: - Skor kembali menjadi nol. - Health
kembali menjadi 100. - Level kembali ke level pertama. - Objek musuh,
asteroid, dan proyektil sebelumnya dibersihkan. - Pesawat dikembalikan
ke posisi awal. - Timer dan spawn system di-reset. - Permainan dimulai
kembali tanpa refresh halaman.

### 4.4 Skor & Rekor

#### FR-10 --- Skor Berjalan

Rekomendasi poin awal:

  Objek                   Poin
  --------------------- ------
  Asteroid kecil           +10
  Asteroid sedang          +20
  Asteroid besar           +30
  Pesawat musuh biasa      +50
  Pesawat musuh elite     +100
  Boss                    +500

Kebutuhan: - Skor diperbarui secara langsung. - Skor tidak berkurang
ketika pemain terkena damage. - Skor ditampilkan pada HUD. - Setiap
objek hanya memberikan skor satu kali. - Skor di-reset ketika permainan
baru dimulai.

#### FR-11 --- Rekor Tertinggi

-   Sistem menyimpan skor tertinggi.
-   Rekor diperbarui jika skor baru lebih tinggi.
-   Data disimpan menggunakan LocalStorage.
-   Rekor tetap tersedia setelah browser ditutup dan dibuka kembali.
-   Rekor ditampilkan pada menu utama dan layar Game Over.

#### FR-12 --- Leaderboard Lokal

Untuk MVP, leaderboard berupa daftar maksimal 10 skor terbaik pada
perangkat yang sama.

Informasi: - Nama pemain (opsional). - Skor. - Level tertinggi. -
Tanggal permainan.

Leaderboard global membutuhkan backend dan tidak termasuk MVP.

### 4.5 Level Bertahap

#### FR-13 --- Sistem Naik Level

Contoh target level awal:

  Level     Target Skor Kesulitan
  ------- ------------- ----------------
  1                 100 Mudah
  2                 250 Mudah-Menengah
  3                 450 Menengah
  4                 700 Menengah-Sulit
  5               1.000 Sulit

Target dapat disesuaikan melalui playtesting.

Ketika target tercapai: - Tampilkan notifikasi Level Up. - Level
bertambah satu. - Kecepatan asteroid meningkat. - Frekuensi kemunculan
musuh meningkat. - Pola serangan musuh menjadi lebih menantang. - Latar
belakang dapat berubah.

#### FR-14 --- Kesulitan Meningkat

Kesulitan meningkat berdasarkan level, dengan parameter: - Kecepatan
asteroid. - Jumlah asteroid aktif. - Frekuensi spawn musuh. - Kecepatan
proyektil musuh. - Ketahanan pesawat musuh. - Pola serangan musuh.

Peningkatan kesulitan harus memiliki batas maksimum agar permainan tetap
adil dan stabil.

#### FR-15 --- Variasi Latar

Tema latar yang dapat digunakan: - Deep Space: latar gelap dengan
bintang. - Blue Nebula: kabut luar angkasa biru. - Red Galaxy: galaksi
bernuansa merah. - Planetary Zone: lingkungan dengan planet besar.

Perubahan latar dapat dilakukan ketika pemain mencapai level tertentu.
Variasi latar tidak boleh mengganggu keterbacaan objek gameplay.

### 4.6 Menu & Pengaturan

#### FR-16 --- Menu Utama

Menu utama berisi: - Logo Space Shooter 3D. - Tombol Start Game. -
Tombol How to Play. - Tombol Leaderboard. - Tombol Settings. - Informasi
rekor tertinggi. - Background animasi luar angkasa. - Pesawat sebagai
objek 3D dekoratif.

#### FR-17 --- Pause & Resume

Ketika pemain menekan Escape atau tombol Pause: - Permainan berhenti
sementara. - Pergerakan musuh dan asteroid dihentikan. - Pergerakan
laser dan proyektil dihentikan. - Timer dan proses spawn dihentikan. -
Menu Pause ditampilkan.

Menu Pause memiliki: - Resume. - Restart. - Settings. - Main Menu.

#### FR-18 --- Pengaturan Suara & Kontrol

Pengaturan mencakup: - Volume musik. - Volume efek suara. - Toggle musik
ON/OFF. - Toggle sound effect ON/OFF. - Informasi kontrol keyboard. -
Sensitivitas gerakan (opsional).

Preferensi disimpan secara lokal.

### 4.7 Efek Visual & Suara

#### FR-19 --- Latar Luar Angkasa

Elemen visual: - Bintang dalam jumlah yang terkontrol. - Nebula dan
galaksi. - Planet sebagai objek dekoratif. - Asteroid dengan model 3D. -
Efek parallax untuk kedalaman. - Pencahayaan dan bayangan yang sesuai.

#### FR-20 --- Efek Ledakan & Laser

-   Laser berwarna terang dan mudah terlihat.
-   Efek cahaya pada pesawat.
-   Partikel ledakan.
-   Efek visual ketika musuh terkena tembakan.
-   Efek kerusakan ketika pesawat pemain terkena serangan.
-   Animasi transisi saat pergantian level.

#### FR-21 --- Musik & Suara

  Jenis Audio        Penggunaan
  ------------------ --------------------------------
  Background Music   Musik selama permainan
  Laser Sound        Suara tembakan
  Explosion Sound    Suara ledakan
  Hit Sound          Suara terkena serangan
  Level Up Sound     Notifikasi kenaikan level
  Game Over Sound    Efek ketika permainan berakhir
  UI Sound           Efek tombol menu

Semua audio memiliki kontrol volume dan dapat dinonaktifkan. Audio harus
dimulai setelah interaksi pengguna untuk mengikuti kebijakan autoplay
browser.

------------------------------------------------------------------------

## 5. User Interface & User Experience

### 5.1 Prinsip Desain

Game menggunakan gaya visual futuristik bertema luar angkasa: - Dark
futuristic interface. - Dominasi biru, hitam, ungu, dan cyan. - Efek
neon dan glow secukupnya. - Panel transparan bergaya sci-fi. - Tipografi
modern dan mudah dibaca. - Animasi halus dan tidak mengganggu gameplay.

### 5.2 Color Palette

  Elemen       Warna
  ------------ -----------
  Background   `#050816`
  Primary      `#2563EB`
  Secondary    `#7C3AED`
  Accent       `#22D3EE`
  Danger       `#EF4444`
  Success      `#22C55E`
  Text         `#F8FAFC`

### 5.3 Struktur Tampilan

**A. Main Menu** - Logo dan judul game. - Tombol Start Game. - Tombol
How to Play. - Tombol Leaderboard. - Tombol Settings. - High Score. -
Latar luar angkasa dan pesawat dekoratif.

**B. Gameplay HUD** - Kiri atas: Health Bar. - Tengah atas: Score. -
Kanan atas: Level dan Pause. - Area utama: pesawat, asteroid, musuh,
laser, dan lingkungan 3D. - Informasi kontrol dapat ditampilkan secara
opsional.

**C. Pause Menu** - Resume. - Restart. - Settings. - Main Menu.

**D. Game Over** - Judul Game Over. - Skor akhir. - Level terakhir. -
High Score. - Main Again. - Main Menu.

### 5.4 Kontrol Permainan

  Tombol            Fungsi
  ----------------- -------------------
  W / Arrow Up      Bergerak ke atas
  S / Arrow Down    Bergerak ke bawah
  A / Arrow Left    Bergerak ke kiri
  D / Arrow Right   Bergerak ke kanan
  Space             Menembakkan laser
  Escape / P        Pause / Resume

Ketentuan: - Mendukung kombinasi tombol. - Mencegah halaman melakukan
scroll ketika Space digunakan saat gameplay. - Kontrol harus
responsif. - Input tidak boleh tertahan setelah jendela kehilangan
fokus. - Tampilkan panduan kontrol sebelum atau saat awal permainan.

------------------------------------------------------------------------

## 6. Non-Functional Requirements

  -----------------------------------------------------------------------
  ID                      Kategori                Persyaratan
  ----------------------- ----------------------- -----------------------
  NFR-01                  Performance             Target 60 FPS pada
                                                  desktop yang memadai.

  NFR-02                  Performance             Target minimum 30 FPS
                                                  pada perangkat yang
                                                  lebih rendah.

  NFR-03                  Loading                 Menampilkan loading
                                                  screen ketika aset 3D
                                                  dimuat.

  NFR-04                  Compatibility           Mendukung Chrome, Edge,
                                                  dan Firefox versi
                                                  modern.

  NFR-05                  Responsive              Area game menyesuaikan
                                                  viewport.

  NFR-06                  Usability               Kontrol mudah dipahami
                                                  pemain baru.

  NFR-07                  Reliability             Tidak crash ketika
                                                  level meningkat.

  NFR-08                  Storage                 Rekor tersimpan secara
                                                  lokal.

  NFR-09                  Maintainability         Source code modular dan
                                                  terdokumentasi.

  NFR-10                  Accessibility           Kontras teks dan tombol
                                                  mudah dibaca.
  -----------------------------------------------------------------------

### 6.1 Optimasi Performa

-   Gunakan Object Pooling untuk asteroid, laser, musuh, dan proyektil.
-   Hapus objek yang tidak lagi digunakan.
-   Gunakan model 3D dengan jumlah polygon efisien.
-   Optimalkan ukuran dan resolusi tekstur.
-   Hindari pembuatan objek berlebihan pada setiap frame.
-   Gunakan delta time untuk pergerakan konsisten.
-   Batasi jumlah objek aktif.
-   Hentikan simulasi gameplay ketika Pause.
-   Batasi pixel ratio renderer pada perangkat beresolusi tinggi.
-   Bersihkan geometry, material, texture, dan event listener yang tidak
    lagi digunakan.

------------------------------------------------------------------------

## 7. Technical Requirements

### 7.1 Teknologi

  Teknologi              Fungsi
  ---------------------- -----------------------------------
  HTML5                  Struktur aplikasi
  CSS3                   Styling UI dan HUD
  JavaScript ES6+        Logika permainan
  Three.js               Rendering grafis 3D
  Vite                   Development server dan build tool
  WebGL                  Rendering grafis browser
  LocalStorage           Penyimpanan skor dan pengaturan
  Howler.js (opsional)   Manajemen audio

**Rekomendasi utama:** Three.js + JavaScript + Vite.

Alasan: - Three.js mendukung pembuatan lingkungan 3D. - JavaScript
sesuai untuk logika game browser. - Vite memudahkan proses
pengembangan. - MVP tidak membutuhkan backend. - Hasil dapat di-deploy
ke hosting statis seperti Vercel atau Netlify.

### 7.2 Arsitektur Sistem

Komponen utama: - Game Engine: mengelola game loop dan status. - Player
Controller: mengatur gerakan dan tembakan. - Enemy Manager: mengelola
spawn dan perilaku musuh. - Asteroid Manager: mengelola asteroid. -
Projectile Manager: mengelola laser dan proyektil musuh. - Collision
Manager: mendeteksi tabrakan. - Level Manager: mengatur progres dan
kesulitan. - Score Manager: menghitung skor dan rekor. - UI Manager:
mengatur menu dan HUD. - Audio Manager: mengatur musik dan efek suara. -
Storage Manager: menyimpan data lokal.

### 7.3 Game State Management

  State       Deskripsi
  ----------- ---------------------------------------
  LOADING     Memuat aset permainan
  MENU        Menampilkan menu utama
  PLAYING     Permainan berjalan
  PAUSED      Permainan dihentikan sementara
  LEVEL_UP    Menampilkan notifikasi kenaikan level
  GAME_OVER   Permainan berakhir

Perubahan state dikelola secara terpusat agar tidak terjadi konflik
antarmodul.

### 7.4 Struktur Folder Proyek

``` text
space-shooter-3d/
├── public/
│   └── assets/
│       ├── models/
│       │   ├── spaceship/
│       │   ├── enemies/
│       │   ├── asteroids/
│       │   └── planets/
│       ├── textures/
│       ├── audio/
│       │   ├── music/
│       │   └── sfx/
│       └── fonts/
├── src/
│   ├── main.js
│   ├── core/
│   │   ├── Game.js
│   │   ├── GameLoop.js
│   │   ├── GameState.js
│   │   └── SceneManager.js
│   ├── entities/
│   │   ├── Player.js
│   │   ├── Enemy.js
│   │   ├── Asteroid.js
│   │   └── Projectile.js
│   ├── systems/
│   │   ├── InputSystem.js
│   │   ├── CollisionSystem.js
│   │   ├── SpawnSystem.js
│   │   ├── ScoreSystem.js
│   │   ├── LevelSystem.js
│   │   └── HealthSystem.js
│   ├── managers/
│   │   ├── UIManager.js
│   │   ├── AudioManager.js
│   │   ├── StorageManager.js
│   │   └── ObjectPool.js
│   ├── ui/
│   │   ├── MainMenu.js
│   │   ├── GameHUD.js
│   │   ├── PauseMenu.js
│   │   ├── GameOver.js
│   │   └── Settings.js
│   ├── config/
│   │   ├── gameConfig.js
│   │   ├── enemyConfig.js
│   │   └── levelConfig.js
│   └── styles/
│       ├── main.css
│       ├── menu.css
│       ├── gameplay.css
│       └── responsive.css
├── index.html
├── package.json
├── vite.config.js
└── README.md
```

Struktur dapat disesuaikan selama pemisahan tanggung jawab modul tetap
terjaga.

------------------------------------------------------------------------

## 8. Data Management

### 8.1 Penyimpanan Data

MVP tidak memerlukan database server. Data disimpan menggunakan
LocalStorage.

Data yang disimpan: - High Score. - Riwayat skor lokal. - Pengaturan
volume. - Status musik. - Status efek suara. - Preferensi kontrol jika
tersedia.

### 8.2 Contoh Struktur Data

``` json
{
  "highScore": 2500,
  "settings": {
    "musicVolume": 0.5,
    "sfxVolume": 0.8,
    "musicEnabled": true,
    "sfxEnabled": true
  },
  "leaderboard": [
    {
      "name": "Player",
      "score": 2500,
      "level": 5,
      "date": "2026-11-03"
    }
  ]
}
```

Ketentuan: - Data harus memiliki nilai default. - Aplikasi tidak boleh
error jika LocalStorage kosong. - Data tidak valid harus ditangani
dengan aman. - Reset data hanya dilakukan ketika pemain memilih opsi
reset. - Data lokal tidak dianggap sebagai leaderboard global atau data
yang aman dari manipulasi.

------------------------------------------------------------------------

## 9. Game Balancing

### 9.1 Parameter Awal

  Parameter                      Nilai Awal
  ------------------------- ---------------
  Player Health                         100
  Player Movement Speed       10 unit/detik
  Laser Cooldown                 0,25 detik
  Asteroid Spawn Interval           2 detik
  Enemy Spawn Interval              8 detik
  Laser Damage                           25
  Asteroid Damage                        20
  Enemy Projectile Damage                15

Nilai ini adalah konfigurasi awal untuk diuji dan disesuaikan selama
playtesting.

### 9.2 Variasi Musuh

**Scout Fighter** - Musuh ringan. - Bergerak cepat. - Health rendah. -
Pola serangan sederhana.

**Heavy Fighter** - Health tinggi. - Gerakan lebih lambat. - Serangan
lebih kuat.

**Alien Drone** - Ukuran kecil. - Muncul dalam kelompok. - Mengganggu
pergerakan pemain.

**Boss Ship** - Ukuran besar. - Health tinggi. - Pola serangan khusus. -
Direncanakan untuk pengembangan lanjutan setelah MVP stabil.

------------------------------------------------------------------------

## 10. User Stories

  -----------------------------------------------------------------------
  ID                      User Story              Prioritas
  ----------------------- ----------------------- -----------------------
  US-01                   Sebagai pemain, saya    High
                          ingin melihat menu      
                          utama agar dapat        
                          memulai permainan.      

  US-02                   Sebagai pemain, saya    Critical
                          ingin mengendalikan     
                          pesawat agar dapat      
                          menghindari rintangan.  

  US-03                   Sebagai pemain, saya    Critical
                          ingin menembakkan laser 
                          untuk menghancurkan     
                          musuh.                  

  US-04                   Sebagai pemain, saya    Critical
                          ingin melihat health    
                          agar mengetahui kondisi 
                          pesawat.                

  US-05                   Sebagai pemain, saya    High
                          ingin mendapatkan skor  
                          ketika menghancurkan    
                          objek.                  

  US-06                   Sebagai pemain, saya    High
                          ingin menghadapi musuh  
                          yang semakin sulit.     

  US-07                   Sebagai pemain, saya    High
                          ingin melihat rekor     
                          tertinggi.              

  US-08                   Sebagai pemain, saya    High
                          ingin menghentikan      
                          permainan sementara.    

  US-09                   Sebagai pemain, saya    Medium
                          ingin mengatur volume   
                          suara.                  

  US-10                   Sebagai pemain, saya    Critical
                          ingin memainkan ulang   
                          game setelah kalah.     
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 11. Acceptance Criteria

  Fitur             Kriteria Penerimaan
  ----------------- ------------------------------------------------
  Main Menu         Tombol Start dapat memulai permainan.
  Kendali Pesawat   Pesawat bergerak sesuai input keyboard.
  Tembak Laser      Laser muncul dan dapat mengenai target.
  Asteroid          Asteroid muncul dan bergerak dalam arena.
  Musuh             Pesawat musuh muncul dan dapat menyerang.
  Collision         Tabrakan terdeteksi dengan benar.
  Health            Health berkurang ketika terkena serangan.
  Game Over         Muncul ketika health mencapai nol.
  Score             Skor bertambah ketika target dihancurkan.
  High Score        Rekor tersimpan setelah permainan berakhir.
  Level             Level bertambah ketika target tercapai.
  Pause             Semua aktivitas gameplay berhenti sementara.
  Resume            Permainan dapat dilanjutkan kembali.
  Audio             Musik dan efek suara dapat diatur.
  Restart           Permainan dimulai kembali dengan kondisi awal.

------------------------------------------------------------------------

## 12. Testing & Quality Assurance

### 12.1 Functional Testing

  -----------------------------------------------------------------------
  ID                      Skenario Pengujian      Expected Result
  ----------------------- ----------------------- -----------------------
  TC-01                   Membuka halaman game    Menu utama muncul.

  TC-02                   Menekan Start Game      Gameplay dimulai.

  TC-03                   Menekan tombol W        Pesawat bergerak ke
                                                  atas.

  TC-04                   Menekan Space           Laser ditembakkan.

  TC-05                   Laser mengenai asteroid Asteroid hancur dan
                                                  skor bertambah.

  TC-06                   Pesawat terkena         Health berkurang.
                          asteroid                

  TC-07                   Health mencapai nol     Game Over muncul.

  TC-08                   Menekan Pause           Gameplay berhenti.

  TC-09                   Menekan Resume          Gameplay berlanjut.

  TC-10                   Mencapai target level   Level bertambah.

  TC-11                   Mendapat skor baru      High Score diperbarui.

  TC-12                   Refresh browser         Data rekor tetap
                                                  tersimpan.

  TC-13                   Mematikan musik         Background music
                                                  berhenti.

  TC-14                   Menekan Restart         Kondisi permainan
                                                  di-reset.
  -----------------------------------------------------------------------

### 12.2 Performance Testing

Periksa: - FPS selama gameplay. - Waktu loading awal. - Penggunaan CPU
dan GPU. - Penggunaan memori. - Performa ketika banyak asteroid
muncul. - Performa ketika banyak laser ditembakkan. - Stabilitas
permainan dalam sesi panjang.

### 12.3 Compatibility Testing

Uji pada: - Google Chrome. - Microsoft Edge. - Mozilla Firefox. -
Resolusi desktop 1920 × 1080. - Resolusi laptop 1366 × 768. - Tablet
sebagai pengujian tambahan.

### 12.4 Regression Testing

Setiap penambahan fitur baru harus diuji agar tidak merusak: - Sistem
pergerakan. - Sistem tembakan. - Collision detection. - Perhitungan
skor. - Pengelolaan health. - Level progression. - Pause dan restart.

------------------------------------------------------------------------

## 13. Development Roadmap

Pengembangan menggunakan pendekatan MVP dan dilakukan secara bertahap.

### Phase 1 --- Project Setup

-   Setup Vite dan Three.js.
-   Membuat scene, camera, dan renderer.
-   Membuat game loop dasar.
-   Menyiapkan struktur folder dan konfigurasi.
-   Menampilkan lingkungan luar angkasa dasar.

**Output:** Fondasi aplikasi 3D berjalan.

### Phase 2 --- Core Gameplay

-   Membuat model pesawat pemain.
-   Membuat kontrol keyboard.
-   Mengatur kamera mengikuti pesawat.
-   Membuat sistem laser.
-   Mengatur batas arena.

**Output:** Pesawat dapat dikendalikan dan menembak.

### Phase 3 --- Enemy and Collision

-   Membuat asteroid.
-   Membuat pesawat musuh.
-   Membuat sistem spawn.
-   Membuat proyektil musuh.
-   Membuat collision detection.
-   Membuat sistem damage dan ledakan.

**Output:** Sistem pertempuran dapat dimainkan.

### Phase 4 --- Score and Level

-   Membuat health system.
-   Membuat score system.
-   Membuat high score.
-   Membuat level progression.
-   Mengatur peningkatan kesulitan.

**Output:** Progres permainan berfungsi.

### Phase 5 --- UI and Audio

-   Membuat Main Menu.
-   Membuat HUD.
-   Membuat Pause dan Resume.
-   Membuat Game Over.
-   Membuat Settings.
-   Mengintegrasikan musik dan SFX.

**Output:** UI dan audio lengkap.

### Phase 6 --- Polish and Optimization

-   Menambahkan efek visual.
-   Menambahkan variasi lingkungan.
-   Mengoptimalkan model dan tekstur.
-   Mengimplementasikan Object Pooling.
-   Mengoptimalkan performa dan responsivitas.

**Output:** Game lebih polished dan stabil.

### Phase 7 --- Testing and Deployment

-   Melakukan functional testing.
-   Melakukan regression testing.
-   Memperbaiki bug.
-   Menjalankan production build.
-   Melakukan deployment.

**Output:** Game siap dimainkan melalui browser.

------------------------------------------------------------------------

## 14. Risiko dan Mitigasi

  -----------------------------------------------------------------------
  Risiko                  Dampak                  Mitigasi
  ----------------------- ----------------------- -----------------------
  Model 3D terlalu berat  FPS menurun             Gunakan model low-poly
                                                  yang optimal.

  Terlalu banyak objek    Game lag                Implementasikan Object
                                                  Pooling.

  Collision tidak akurat  Gameplay tidak adil     Gunakan bounding sphere
                                                  dan pengujian
                                                  collision.

  Kontrol tidak responsif Pengalaman buruk        Gunakan delta time dan
                                                  input handling yang
                                                  baik.

  Audio tidak berjalan    Efek suara gagal        Mulai audio setelah
                                                  interaksi pengguna.

  Level terlalu sulit     Pemain cepat berhenti   Lakukan balancing
                                                  melalui playtesting.

  Data LocalStorage       Rekor tidak tersimpan   Validasi dan tangani
  hilang                                          data penyimpanan.

  Game tidak kompatibel   Game gagal dimainkan    Uji pada browser
                                                  modern.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 15. Deployment Requirements

Game harus dapat diakses melalui alamat website tanpa mengharuskan
pengguna menginstal aplikasi.

**Rekomendasi deployment:** - Vercel. - Netlify. - GitHub Pages.

Persyaratan: 1. Production build berhasil. 2. Tidak terdapat error
JavaScript kritis. 3. Semua aset 3D dan audio dapat dimuat. 4. Tidak ada
referensi file lokal yang menyebabkan aset gagal dimuat. 5. Game dapat
dimainkan melalui HTTPS. 6. LocalStorage bekerja pada domain deployment.
7. Tampilan sesuai ukuran layar. 8. Tersedia petunjuk kontrol untuk
pemain baru.

------------------------------------------------------------------------

## 16. Definition of Done

Proyek dinyatakan selesai apabila: - \[ \] Seluruh fitur MVP
berfungsi. - \[ \] Pesawat dapat dikendalikan dengan lancar. - \[ \]
Pemain dapat menghancurkan asteroid dan musuh. - \[ \] Collision
detection berjalan dengan benar. - \[ \] Health dan Game Over bekerja. -
\[ \] Skor dapat dihitung dan disimpan. - \[ \] Permainan dapat diulang
tanpa refresh browser. - \[ \] Pause dan Resume tidak menyebabkan bug. -
\[ \] Tidak terdapat bug kritis. - \[ \] Game berjalan dengan performa
yang layak. - \[ \] Semua aset tampil dengan benar. - \[ \] Production
build berhasil. - \[ \] Game dapat dimainkan langsung melalui browser.

------------------------------------------------------------------------

## 17. Future Development

Setelah versi pertama berhasil dibuat, fitur berikut dapat
dipertimbangkan:

### 17.1 Spaceship Upgrade

Pemain dapat meningkatkan kecepatan, armor, dan kekuatan laser.

### 17.2 Boss Battle

Pertarungan melawan pesawat induk alien dengan pola serangan khusus.

### 17.3 Power-Up System

Item untuk menambah health, memperkuat laser, dan memberikan shield
sementara.

### 17.4 Galaxy Exploration

Eksplorasi planet dan lingkungan galaksi baru.

### 17.5 Multiplayer dan Global Leaderboard

Fitur kompetisi online yang membutuhkan backend, autentikasi, dan
penyimpanan server.

------------------------------------------------------------------------

## 18. Kesimpulan dan Product Vision

Space Shooter 3D merupakan game aksi berbasis browser yang menggabungkan
mekanisme pesawat tempur, pertempuran luar angkasa, penghancuran
asteroid, dan sistem level progresif.

Fokus utama versi pertama adalah menghasilkan game yang benar-benar
playable, bukan sekadar visual 3D atau animasi pesawat.

Tiga prioritas utama: 1. **Gameplay:** Pesawat responsif, laser
berfungsi, dan musuh dapat dikalahkan. 2. **Experience:** Visual
menarik, UI futuristik, dan efek suara yang mendukung permainan. 3.
**Replayability:** Skor tertinggi, level bertahap, dan tingkat kesulitan
yang mendorong pemain bermain kembali.

**Target akhir:** Game Space Shooter 3D yang dapat dibuka langsung
melalui browser, memiliki gameplay lengkap, visual 3D menarik, serta
performa optimal.

------------------------------------------------------------------------

## 19. Instruksi Implementasi untuk AI Coding Agent

Gunakan dokumen PRD ini sebagai sumber utama pengembangan proyek Space
Shooter 3D.

### Aturan Pengembangan

1.  Gunakan JavaScript ES6+, Three.js, dan Vite.
2.  Terapkan arsitektur modular dan pisahkan sistem berdasarkan tanggung
    jawab.
3.  Gunakan delta time untuk seluruh pergerakan dan animasi.
4.  Gunakan Object Pooling untuk objek yang sering dibuat dan dihapus.
5.  Pisahkan game logic, rendering, UI, audio, dan data management.
6.  Gunakan konfigurasi terpusat untuk health, damage, kecepatan, skor,
    dan level.
7.  Pastikan setiap fitur dapat diuji secara independen.
8.  Jangan membuat fitur di luar prioritas MVP tanpa alasan yang jelas.
9.  Jangan menggunakan placeholder untuk fitur inti yang seharusnya
    sudah berfungsi.
10. Pastikan semua tombol dan interaksi UI benar-benar bekerja.

### Development Workflow

-   Implementasikan proyek secara bertahap berdasarkan Development
    Roadmap.
-   Selesaikan dan uji setiap fase sebelum melanjutkan ke fase
    berikutnya.
-   Jangan mengubah fitur yang sudah berfungsi tanpa alasan teknis.
-   Jalankan build dan periksa error setelah perubahan signifikan.
-   Perbarui dokumentasi dan checklist implementasi.
-   Prioritaskan gameplay stabil sebelum menambahkan efek visual
    kompleks.
-   Jika aset eksternal digunakan, pastikan lisensi dan sumbernya
    sesuai.
-   Jika aset belum tersedia, buat placeholder 3D sederhana yang tetap
    fungsional dan mudah diganti.

### Final Requirements

Hasil akhir harus berupa game 3D yang benar-benar dapat dimainkan di
browser, bukan sekadar prototype visual.

Pastikan seluruh fitur MVP memenuhi acceptance criteria dalam PRD.
Hindari implementasi yang hanya berupa tombol dekoratif atau fitur yang
belum memiliki fungsi nyata.
