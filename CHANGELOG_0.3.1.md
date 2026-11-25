# SilopiDijital Veresiye 0.3.1

## Vercel build düzeltmesi
- `scripts/check-security.mjs`, `.env.example` dosyasını yalnızca mevcutsa okur.
- `.env.example` bir örnek dosyadır; runtime yapılandırması veya Vercel dağıtımı için gerekli değildir. GitHub Web arayüzünden Windows klasörü yüklerken nokta ile başlayan dosyanın atlanması artık `ENOENT` hatası oluşturmaz.
- Dosya mevcut olduğunda içindeki VITE/Supabase secret/service-role anahtarları için güvenlik taraması devam eder.

## Korunan davranışlar
- Supabase proje hedefi, API proxy, login ve admin yetkilendirmesi değiştirilmedi.
- PWA, Service Worker v9 ve müşteri verilerinin cache dışı tutulması aynen korunmuştur.
- Veritabanı migration'ı veya müşteri finansal verisi değişikliği yapılmadı.
