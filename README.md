# Çözülmeyen Konular — Dedektif Masası

Türkçe, mobil öncelikli ve GitHub Pages ile yayınlanabilen bir PWA dedektif oyunu.

## İçerik
- 3 özgün kurgusal vaka; başlangıç, orta ve zor seviye
- Kanıt dosyaları, şüpheli sorguları ve soru-cevaplar
- Cihazda saklanan dedektif notları
- İpucu sistemi, final suçlaması ve çözüm açıklaması
- XP, dedektif rütbesi ve vaka kilidi açma
- `localStorage` ile cihaz içi kayıt
- Service Worker ile temel çevrimdışı açılış ve PWA manifesti

## GitHub Pages kurulumu
1. GitHub'da yeni bir **Public** repository oluştur (ör. `cozulmeyen-konular`).
2. Bu klasördeki **tüm dosyaları** repository'nin kök dizinine yükle. `index.html` doğrudan kökte olmalı.
3. Repository → **Settings → Pages** bölümüne git.
4. **Deploy from a branch** seç; Branch `main`, Folder `/(root)` seçip Save'e bas.
5. GitHub'ın verdiği `https://KULLANICI_ADIN.github.io/cozulmeyen-konular/` adresini aç. Yayınlanması birkaç dakika sürebilir.

## Telefona ekleme
**Android:** Linki Chrome'da aç → menü → **Yükle** veya **Ana ekrana ekle**. Bazı telefonlarda yükleme seçeneği birkaç ziyaret veya sayfa yüklendikten sonra görünür.

**iPhone:** Linki Safari'de aç → Paylaş → **Ana Ekrana Ekle** → Ekle.

PWA kurulumu ve Service Worker HTTPS gerektirir; GitHub Pages HTTPS sağlar.

## Test
Bilgisayarında Python varsa klasörde `python -m http.server 8000` çalıştırıp `http://localhost:8000` adresinden test edebilirsin. `file://` ile açma; Service Worker çalışmaz.

## Sınırlar ve sonraki geliştirme
- İlerleme sadece aynı cihaz/tarayıcıda saklanır. Tarayıcı verileri temizlenirse kayıt silinebilir. Bulut senkronizasyonu veya kullanıcı hesabı yoktur.
- İlk sürümde üç vaka var; yeni vaka içeriği `app.js` içindeki `CASES` dizisine eklenebilir.
- Google Fonts bağlantısı internet ister; çevrimdışıyken sistem yazı tipleri kullanılır.
- Vakalardaki karakterler ve olaylar kurgusaldır.
