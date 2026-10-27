# Simulasi Interaktif Hukum Induksi Diri pada Kumparan

Web simulasi rangkaian RL seri (DC dan AC) dengan HTML, CSS, dan JavaScript murni. Tanpa backend dan tanpa dependensi eksternal; semua path relatif sehingga berjalan di GitHub Pages.

## Tujuan belajar
Memahami εL = −L di/dt, Hukum Lenz, L = μN²A/ℓ, W = ½Li², τ = L/R, dan XL = 2πfL.

## Fitur
Simulasi (rangkaian SVG, sakelar, DC/AC, medan skematis, meter), grafik real-time (i, v, vL, vR, ε, W, fase AC), hasil hitung otomatis, 6 eksperimen, kuis 11 soal, tema terang/gelap, responsif.

## Model
Setiap langkah memakai solusi eksak L·di/dt + Ri = v(t): i(t+Δt) = ip(t+Δt) + (i − ip(t))·e^(−Δt/τ). Sakelar OFF: sumber dilepas, arus meluruh lewat R (i = I₀e^(−t/τ)). Batas: induktor ideal, tanpa saturasi.

## Struktur
`index.html`, `style.css`, `script.js`, `README.md`

## Menjalankan lokal
Buka `index.html` di browser, atau jalankan `python -m http.server` lalu buka http://localhost:8000.

## Deploy ke GitHub Pages
1. Buat repository baru (mis. `induksi-diri-simulation`) di github.com.
2. Unggah keempat file (Add file → Upload files), lalu Commit.
3. Settings → Pages → Source: *Deploy from a branch* → Branch `main`, folder `/ (root)` → Save.
4. Tunggu 1–2 menit; URL: `https://USERNAME.github.io/induksi-diri-simulation/`.
5. Perbarui: unggah/commit ulang file yang berubah; refresh dengan Ctrl+F5.

Jika CSS/JS tidak muncul: pastikan nama file persis huruf kecil, ada di root, dan hard-refresh.

## Checklist pengujian
Sudah dijalankan (Node, fungsi fisika): i(τ)=63,2% Iss; Iss=V/R; KVL; W=½Li²; peluruhan OFF 36,8% pada τ; XL naik dengan f; amplitudo AC tunak = Vm/Z; L∝N².
Belum diuji di browser (lakukan manual): tombol Mulai/Jeda/Lanjutkan/Reset, sakelar, slider, tab, grafik, kuis, tampilan HP portrait/landscape, dan setelah terbit di GitHub Pages.
