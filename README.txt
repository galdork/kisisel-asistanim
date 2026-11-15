# Kişisel Asistanım — ilk sürüm

## Özellikler
- PIN ile kilit ve AES-GCM şifreli yerel veri kasası
- Doğum günü kaydı ve yaklaşan doğum günleri listesi
- Borç/alacak kaydı, kısmi ödeme ve ilerleme çubuğu
- Şifreli yedek indirme ve geri yükleme
- PWA / çevrimdışı önbellek

## Windows üzerinden ücretsiz yayınlama
1. GitHub hesabı oluştur veya mevcut hesabına giriş yap.
2. Yeni bir **Public** repository oluştur (ör. `kisisel-asistanim`).
3. Bu klasördeki `index.html`, `manifest.json` ve `sw.js` dosyalarını repository ana dizinine yükle.
4. Repository > Settings > Pages bölümüne gir.
5. "Deploy from a branch" seç, `main` ve `/(root)` seçip Save'e bas.
6. Yayın adresi `https://KULLANICIADI.github.io/kisisel-asistanim/` biçiminde olur.
7. iPhone 13'te Safari ile bu adresi aç. Paylaş > Ana Ekrana Ekle > Web Uygulaması Olarak Aç seçeneğini etkinleştir > Ekle.
8. İlk açılışta PIN oluştur. İnternet bağlıyken bir kez açtıktan sonra çevrimdışı test et.

## Güvenlik ve önemli notlar
- Kayıtlar cihazdaki tarayıcı depolamasında AES-GCM ile şifreli saklanır. PIN, PBKDF2-SHA256 ile anahtar türetmek için kullanılır.
- PIN'i unutursan verileri kurtarmanın yolu yoktur; şifreli yedeği ve doğru PIN'i sakla.
- Yedek dosyası da şifrelidir; dosyayı ve PIN'i ayrı ve güvenli yerlerde tut.
- Safari web sitesi verilerini temizlemek, cihazı sıfırlamak veya uygulama verilerini silmek yerel kayıtları silebilir.
- İlk sürümde doğum günü bildirimleri için işletim sistemi seviyesinde garantili bildirim yoktur; yaklaşan doğum günleri uygulama içinde görünür.
- GitHub Pages deposu public ise uygulama kaynak kodu herkesçe görülebilir. Kişisel kayıtlar depoya yüklenmez; yalnızca şifreli şekilde telefonda tutulur.
- Bu sürüm prototiptir. Gerçek hassas finansal kayıtlar için yedekleri düzenli alın ve PIN'inizi güçlü tutun.
