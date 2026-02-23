# ❤️ FiilTale: Determination (V2.1)

![FiilTale Banner](https://img.shields.io/badge/Engine-Underground_V2-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Stable-green?style=for-the-badge)
![Code](https://img.shields.io/badge/Lines-1000%2B-yellow?style=for-the-badge)

> "Yeraltına düşen bir şövalye, kadim dil bilgisi mühürlerini çözmek zorunda. Kararlılığını koru!"

**FiilTale**, Undertale evreninden ilham alan, 7. Sınıf Türkçe müfredatındaki **Fiilde Yapı (Basit, Türemiş, Birleşik)** konusunu oyunlaştırarak öğreten web tabanlı bir RPG deneyimidir.

---

## 🛠️ Mimari ve Geliştiriciler

Bu proje, eğitim teknolojilerini oyun mekanikleriyle birleştirmek amacıyla iki ana mimar tarafından geliştirilmiştir:

* **Ata(ata.dev) (Visual Architect):** Görsel tasarım, CSS animasyonları, sahne yönetimi ve kullanıcı deneyimi (UX).
* **Nadir (Systems Engineer):** Çekirdek oyun mantığı, Web Audio API entegrasyonu, veri havuzu yönetimi ve 12 saniyelik "Düşünme Barı" algoritması.

---

## 🚀 Öne Çıkan Özellikler

* **1000+ Satır Özel Kod:** Hiçbir harici kütüphane (jQuery, React vb.) kullanılmadan, saf (Vanilla) JS, CSS ve HTML ile inşa edildi.
* **12 Saniye Kuralı:** Her soru için oyuncuya 12 saniye süre tanınır. Süre azaldıkça bar mavi renkten kırmızıya döner; süre biterse düşman saldırır!
* **Dinamik Boss Sistemi:** Toriel, Papyrus, Undyne, Mettaton ve Sans. Her boss'un kendine has konuşma tarzı, intro ve yenilgi diyalogları mevcuttur.
* **Kapsamlı Veritabanı:** `turkceciyiz.com` kaynaklı 3 farklı PDF'den derlenen; "anlatılagelmiştir", "gidemez", "vazgeçti" gibi kafa karıştırıcı 50'den fazla fiil yapısı.
* **Retro Ses Motoru:** Web Audio API kullanılarak üretilen 8-bit synth ses efektleri.

---

## 🎮 Oynanış

1.  **İsim Ver:** Yeraltına düşen şövalyeye adını ver.
2.  **Haritada İlerle:** 5 farklı bölgeyi keşfet ve her bölgenin gardiyanıyla yüzleş.
3.  **Yapıyı Seç:** Karşına çıkan fiilin yapısını (Basit, Türemiş veya Birleşik) 12 saniye içinde belirle.
4.  **Saldır/Savun:** Doğru cevaplar boss'a hasar verir, yanlış cevaplar veya süre aşımı senin canını (HP) azaltır.

---

## 💻 Teknik Kurulum

Oyun tek bir HTML dosyası içinde tüm mantığı barındırır. Çalıştırmak için:

1.  `index.html` dosyasını indirin.
2.  Modern bir tarayıcıda (Chrome, Brave, Edge) dosyaya çift tıklayın.
3.  Müzik ve seslerin başlaması için ekrana bir kez tıklayın.
4.  Veya [FiilTale Web](https://lakrlakr5dev.github.io/fiiltale) adresine gidin

```javascript
// Motorun çekirdek yapısı
const ftEngine = {
    audio: { ... },  // Synth Ses Motoru
    db: [ ... ],     // Fiil Veritabanı
    battle: { ... }, // 12sn Timer ve Hasar Hesaplama
    utils: { ... }   // Typewriter ve Efektler
};
