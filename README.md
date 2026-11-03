# Aplikasi Profil (Flutter)

Tugas praktikum **Pertemuan 5** - Mata Kuliah KB1185 Aplikasi Mobile
Institut Teknologi & Bisnis Bina Sarana Global

**Nama:** Safrizal Ramadhan
**NIM:** 1124160005
**Repo:** TugasP5

## Deskripsi

Aplikasi halaman profil pengguna yang dibuat dengan Flutter. Pengerjaan dibagi ke dalam 5 hari dengan alur commit berstandar industri (**Conventional Commits**). Fokusnya adalah komposisi layout, Extract Widget (refactoring), ListView, dan interaksi dasar.

## Fitur

- Halaman profil dengan avatar, nama, dan status
- Baris statistik (Proyek, Followers, Following)
- Daftar pengalaman proyek yang bisa di-scroll
- Tombol Edit Profil untuk mengubah nama lewat dialog (Hari 5)

## Struktur Widget

| Widget | Fungsi |
|---|---|
| `MyApp` | Root aplikasi (`MaterialApp`) |
| `ProfilePage` | Halaman utama profil |
| `ProfileAvatar` | Foto profil (`CircleAvatar`) |
| `ProfileInfo` | Nama dan status (menerima parameter `name` dan `role`) |
| `ProfileStats` | Baris statistik |
| `StatItem` | Satu item angka + label |
| `ExperienceCard` | Kartu satu pengalaman proyek |

## Log Pengerjaan Harian

### Hari 1 - Kerangka Dasar & Refactoring Awal

| Sesi | Yang diupdate | Commit |
|---|---|---|
| Pagi | Membuat `main.dart` dengan `Scaffold`, `AppBar`, `CircleAvatar`, `Text`, dan tombol Edit Profil dalam satu `Column` (belum dipisah) | `feat: create basic profile page structure with avatar and text` |
| Siang | Extract `ProfileAvatar` dan `ProfileInfo` sebagai custom widget dengan parameter passing (`name`, `role`) | `refactor: extract avatar and info into custom widgets` |

### Hari 2 - Komponen Statistik Profil

| Sesi | Yang diupdate | Commit |
|---|---|---|
| Pagi | Menambahkan `Row` berisi 3 `Column` (Proyek, Followers, Following) di bawah tombol Edit Profil | `feat: add profile statistics row` |
| Siang | Extract `ProfileStats` dan `StatItem` agar reusable | `refactor: extract statistics UI into ProfileStats and StatItem widgets` |

### Hari 3 - Daftar Pengalaman (ListView)

| Sesi | Yang diupdate | Commit |
|---|---|---|
| Pagi | Menambahkan `Expanded` + `ListView.builder` dengan dummy data pengalaman proyek | `feat: add scrollable experience list using ListView.builder` |
| Siang | Extract `ExperienceCard` dengan ikon, `Card`, dan elevation | `refactor: extract list tile into ExperienceCard widget and apply styling` |

### Hari 4 - Finishing & Interaksi Statis

| Sesi | Yang diupdate | Commit |
|---|---|---|
| Pagi | Merapikan `padding`, `SizedBox`, warna latar statistik, dan bentuk kartu | `style: adjust padding and spacing for profile components` |
| Siang | Tombol Edit Profil memunculkan `SnackBar` (fitur belum aktif) | `feat: add static edit button with snackbar notification` |

### Hari 5 - State Management Dasar & Interaktivitas

| Sesi | Yang diupdate | Commit |
|---|---|---|
| Pagi | Mengubah `ProfilePage` dari `StatelessWidget` ke `StatefulWidget`, variabel `userName` tidak lagi hardcode | `refactor: convert ProfilePage to StatefulWidget for dynamic data` |
| Siang | Tombol Edit Profil membuka `showDialog` berisi `TextFormField`; tombol Simpan memperbarui `userName` lewat `setState()` (dengan validasi nama tidak boleh kosong) | `feat: implement edit profile dialog with state update` |

## Cara Menjalankan

```bash
flutter pub get
flutter run -d chrome
```

Atau jalankan di emulator/HP dengan `flutter devices` lalu `flutter run`.

## Daftar Commit

```
feat: create basic profile page structure with avatar and text
refactor: extract avatar and info into custom widgets
feat: add profile statistics row
refactor: extract statistics UI into ProfileStats and StatItem widgets
feat: add scrollable experience list using ListView.builder
refactor: extract list tile into ExperienceCard widget and apply styling
style: adjust padding and spacing for profile components
feat: add static edit button with snackbar notification
refactor: convert ProfilePage to StatefulWidget for dynamic data
feat: implement edit profile dialog with state update
```
