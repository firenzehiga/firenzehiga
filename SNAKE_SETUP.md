# GitHub Snake Animation Setup

## Langkah-langkah untuk mengaktifkan snake animation:

### 1. Upload files ke GitHub
1. Buat repository baru di GitHub dengan nama yang sama dengan username Anda: `firenzehiga/firenzehiga`
2. Upload semua file dari folder ini ke repository tersebut
3. Pastikan repository bersifat **PUBLIC**

### 2. Aktifkan GitHub Actions
1. Buka repository `firenzehiga/firenzehiga` di GitHub
2. Klik tab **Actions**
3. Jika diminta, aktifkan GitHub Actions
4. Actions akan otomatis berjalan sesuai schedule yang sudah diatur

### 3. Jalankan Action secara manual (opsional)
1. Di tab Actions, klik workflow **"Generate Snake Animation"**
2. Klik tombol **"Run workflow"** untuk menjalankan secara manual
3. Tunggu sampai workflow selesai (biasanya 1-2 menit)

### 4. Verifikasi hasil
1. Setelah workflow selesai, cek apakah branch `output` sudah terbuat
2. Di branch `output`, seharusnya ada file:
   - `github-contribution-grid-snake.svg`
   - `github-contribution-grid-snake-dark.svg`

### 5. Update README (sudah dilakukan)
README.md sudah diupdate dengan kode yang benar untuk menampilkan snake animation.

## Troubleshooting

### Jika snake animation tidak muncul:
1. **Cek repository visibility**: Pastikan repository `firenzehiga/firenzehiga` bersifat PUBLIC
2. **Cek GitHub Actions**: Pastikan workflow berhasil dijalankan tanpa error
3. **Cek branch output**: Pastikan branch `output` ada dan berisi file SVG
4. **Tunggu cache refresh**: GitHub Pages kadang butuh waktu 5-10 menit untuk refresh
5. **Cek URL langsung**: Buka URL gambar langsung di browser:
   ```
   https://raw.githubusercontent.com/firenzehiga/firenzehiga/output/github-contribution-grid-snake.svg
   ```

### Jika workflow gagal:
1. Cek apakah nama repository benar: `firenzehiga/firenzehiga`
2. Pastikan file `.github/workflows/snake.yml` ada di root repository
3. Cek log error di tab Actions
4. Pastikan GitHub Actions enabled untuk repository

## Fitur Snake Animation

- **Auto-update**: Snake akan update otomatis setiap 24 jam
- **Dark/Light mode**: Mendukung tema gelap dan terang
- **Responsive**: Menyesuaikan dengan contribution graph GitHub Anda
- **Interactive**: Menampilkan animasi snake yang "memakan" contribution squares

## Kustomisasi

Untuk mengubah tampilan snake, edit file `.github/workflows/snake.yml`:
- Ubah `github_user_name` jika username berbeda
- Tambah palette warna berbeda
- Ubah schedule untuk auto-update

Contoh palette lain:
```yaml
outputs: |
  dist/github-contribution-grid-snake.svg
  dist/github-contribution-grid-snake-dark.svg?palette=github-dark
  dist/github-contribution-grid-snake-purple.svg?palette=github-purple
```
