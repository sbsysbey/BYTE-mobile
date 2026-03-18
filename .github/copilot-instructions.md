# BYTE-mobile Copilot Instructions

## Amaç
Bu dosya, BYTE-mobile workspace'inde Copilot ve benzeri AI agent'ların verimli çalışabilmesi için proje konvansiyonlarını, mimari kararları ve potansiyel tuzakları özetler.

---

## Dosya ve Modül Yapısı
- Her modül ayrı bir HTML dosyasıdır: `modul1.html`–`modul13.html`.
- Ortak JS ([js/app.js], [js/index1.js]) ve CSS ([css/style.css], [css/modules.css]) dosyaları ile modüller arası tutarlılık sağlanır.
- Quiz soruları ve geri bildirimler hem JSON ([quiz_130_sorular.json]) hem HTML içinde, genellikle `opts`, `correct`, `fb` anahtarlarıyla tanımlanır.
- Navigasyon ve erişim kontrolleri JS dosyalarında merkezi olarak yönetilir.

## Mimari ve Konvansiyonlar
- Modül isimlendirmesi: `modulX.html` (X: 1-13).
- Quiz mantığı: Sorular, seçenekler ve geri bildirimler hem JS hem HTML’de, veri tekrarı olabilir.
- XP ve badge hesaplamaları JS’de.
- Modül tamamlanmadan sonraki modüle geçiş engellenir.
- Güvenlik temaları ve anahtar noktalar her modülün başında ve sonunda özetlenir.

## Potansiyel Tuzaklar
- Build/test scriptleri yok; otomasyon ve CI/CD entegrasyonu zor.
- Her modülün ayrı HTML dosyası olması, güncellemelerde tutarsızlık riski yaratır.
- Quiz mantığı hem JS hem HTML’de; veri tekrarı ve bakım zorluğu var.
- Güvenlik önerileri metin olarak gömülü; merkezi güncelleme yok.

## Öneriler
- Ortak fonksiyonlar ve veri yapıları JS dosyalarında merkezi tutulmalı.
- Quiz soruları ve geri bildirimler mümkünse tek bir JSON dosyasında yönetilmeli.
- Otomasyon ve test altyapısı eklenmesi tavsiye edilir.

---

## Örnek Prompts
- "modul5.html dosyasındaki quiz sorularını güncelle"
- "js/app.js içindeki XP hesaplama fonksiyonunu optimize et"
- "Yeni bir modül ekle: modul14.html, güvenlik teması ile"

---

## İlgili Agent-Customization
- applyTo: js/, modul*.html, quiz_130_sorular.json
- Özelleştirilmiş test veya güncelleme agent'ı önerilebilir.

Daha fazla detay veya alan bazlı talep için dosya güncellenebilir.