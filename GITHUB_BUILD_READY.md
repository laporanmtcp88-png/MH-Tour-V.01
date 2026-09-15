# MH Tour — GitHub Build Ready

Project ini sudah diperbaiki agar workflow GitHub Actions menjalankan Gradle dari folder `android` (bukan root), sehingga tidak bergantung pada `./gradlew` yang sebelumnya tidak ada.

File workflow ada di `.github/workflows/build-release-signed.yml`.

**Upload dengan GitHub Desktop atau Git Bash** agar file tersembunyi `.github` dan `.gitignore` ikut masuk repository.
