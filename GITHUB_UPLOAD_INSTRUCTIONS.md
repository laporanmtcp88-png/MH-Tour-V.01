# Upload MH Tour ke GitHub dengan file tersembunyi tetap ikut

**Jangan upload ZIP sebagai satu file.** Repository harus berisi isi folder project.

## Cara paling aman: GitHub Desktop

1. Extract ZIP ini.
2. Buka folder `MH_Tour_V2.3_Professional_Umrah`.
3. Di GitHub Desktop pilih **File > Add Local Repository**.
4. Pilih folder tersebut.
5. Commit seluruh perubahan.
6. **Publish repository** ke GitHub.

Cara ini ikut membawa folder/file tersembunyi seperti:
- `.github/workflows/build-release-signed.yml`
- `.gitignore`

## Jika memakai Git Bash / Terminal

Jalankan dari folder project:

```bash
git init
git add -A
git status
git commit -m "MH Tour Android v3.3 GitHub build ready"
git branch -M main
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git push -u origin main
```

`git add -A` memastikan file tersembunyi ikut masuk.

## Setelah upload

Buka GitHub → **Actions** → **Build MH Tour Android** → **Run workflow**.

- Job **Build debug APK** menghasilkan APK yang dapat dipasang untuk pengujian.
- Job **Build release APK** memeriksa build release.
- Untuk APK release yang benar-benar signed, isi 4 GitHub Secrets yang dijelaskan di `BUILD_RELEASE_SIGNED.md`.

> GitHub web tidak perlu dipakai untuk upload folder project. GitHub Desktop atau Git Bash lebih aman untuk project yang memiliki `.github`.
