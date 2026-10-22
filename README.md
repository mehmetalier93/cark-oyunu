# 🎡 Şansına Ne Çıkarsa

İsimleri çarka ekle, her turda bir kişiyi ele ve son kalan kişinin ne ısmarlayacağını belirle!

Arkadaş grupları için hazırlanmış, tarayıcıda çalışan bir çarklı eleme oyunu. **Çarktan çıkan kişiler kurtulur; son kalan kişi seçilen hediyeyi ısmarlar.**

🔗 **[Oyunu aç](https://cark-oyunu.vercel.app/)**

## Nasıl oynanır?

1. En az iki farklı katılımcının adını yaz. İsimleri virgülle, noktalı virgülle veya alt alta ayırabilirsin.
2. **Starbucks**, **Soda** ya da **Dondurma** seçeneklerinden birini seç. İstersen özel bir hediye veya görev yaz.
3. **Oyunu Başlat** düğmesine bas.
4. **Çarkı Çevir** düğmesiyle turu başlat. Seçilen kişi otomatik olarak oyundan çıkarılır.
5. Tek kişi kalana kadar çarkı çevirmeye devam et. Son kalan kişi seçilen hediyeyi ısmarlar!

## Özellikler

- **2–40 katılımcı:** Aynı isim, Türkçe büyük/küçük harf karşılaştırmasıyla yalnızca bir kez eklenir.
- **Animasyonlu çark:** Her turda kalan katılımcılar arasından bir kişi seçilir.
- **Ana ekranda sonuçlar:** Eleme ve final sonuçları açılır pencere olmadan gösterilir.
- **Eleme geçmişi:** Kalan katılımcılar ve elenenlerin sırası takip edilir.
- **Özel hediye:** Hazır seçeneklerin yanında kendi metnini yazabilirsin.
- **İsteğe bağlı geri sayım:** 3-2-1 geri sayımı varsayılan olarak kapalıdır.
- **Ses efektleri ve konuşma:** Ses tek düğmeyle açılıp kapatılabilir.
- **Final kutlaması:** Sonuç ekranına konfeti ve ses efektleri eşlik eder.
- **Mobil uyumlu görünüm ve tam ekran seçeneği.**

## Kontroller

| Kontrol | İşlev |
| --- | --- |
| **Oyunu Başlat** | Katılımcıları ve seçilen hediyeyi oyuna aktarır. |
| **Çarkı Çevir** | Bir eleme turu başlatır. |
| **Sıfırla** | Oyunu başlangıç durumuna getirir. |
| **Yeni Oyun** | Oyun bittikten sonra hazırlık ekranına döner. |
| **Ses** | Konuşmayı ve ses efektlerini açar veya kapatır. |
| **Tam ekran** | Tarayıcı destekliyorsa tam ekran modunu değiştirir. |
| **Boşluk tuşu** | Bir metin alanında yazmıyorken ana oyun düğmesini çalıştırır. |

Oyun sırasında katılımcılar ve hediye seçimi kilitlenir. Çark dönerken yeni tur başlatılamaz ve oyun sıfırlanamaz.

## Bilgisayarda çalıştırma

Projeyi indir ve **`index.html`** dosyasını tarayıcıda aç. Paket kurulumu veya derleme gerekmez.

```text
index.html    → Sayfa, tasarım ve oyun kodu
vercel.json   → Vercel yayınlama ayarları
README.md     → Proje açıklaması
```

## Vercel'de yayınlama

1. Proje dosyalarını bir GitHub reposunun ana dizinine yükle.
2. Vercel'de **Add New → Project** üzerinden repoyu içe aktar.
3. Aşağıdaki ayarlarla yayınla:

| Ayar | Değer |
| --- | --- |
| Framework Preset | `Other` |
| Root Directory | `index.html` dosyasının bulunduğu dizin |
| Build Command | Boş |
| Output Directory | `.` |

Bu yapılandırma `vercel.json` içinde de tanımlıdır. Veritabanı veya API anahtarı gerekmez.

GitHub bağlantısı ve otomatik yayınlama etkinse, Vercel'in yayın dalına gönderilen değişiklikler yeni bir yayını başlatır. Durumu projenin **Deployments** bölümünden takip edebilirsin.

## Değişiklik yapma

Oyunun arayüzü ve davranışı `index.html` dosyasında bulunur:

- **HTML:** Başlıklar, açıklamalar, alanlar ve düğmeler.
- **`<style>`:** Renkler, yerleşim, animasyonlar ve mobil görünüm.
- **`<script>`:** Katılımcılar, çark hareketi, eleme akışı ve sesler.

Dosyayı düzenledikten sonra tarayıcıda kontrol et ve GitHub'daki dosyayı güncelle.

## Seslendirme

Konuşmalar tarayıcının **Web Speech API** desteğiyle oluşturulur. Dil `tr-TR` olarak istenir; kullanılacak ses tarayıcı tarafından seçilir. Türkçe telaffuz ve konuşma desteği, tarayıcıya ve cihazda kullanılabilen seslere bağlıdır.

Ses efektleri **Web Audio API** ile üretilir. Tarayıcı ses çalmak için önce sayfada bir düğmeye basılmasını isteyebilir. Tam ekran desteği de tarayıcıya göre değişebilir.

## Veriler ve oyun biçimi

Katılımcı listesi, eleme geçmişi ve oyun durumu uygulama tarafından bir sunucuya veya kalıcı depolamaya kaydedilmez. Sayfa yenilendiğinde oyun başlangıç durumuna döner. Konuşma seslerinin cihazda veya çevrimiçi işlenmesi, tarayıcının kullandığı ses hizmetine bağlıdır.

Oyun, aynı cihazın ekranını paylaşan katılımcılar için tasarlanmıştır. Çevrimiçi oda veya cihazlar arasında eşzamanlı oyun özelliği bulunmaz.

## Kullanılan teknolojiler

HTML, CSS, JavaScript, Canvas API, Web Audio API ve Web Speech API. Rastgele seçimde desteklenen tarayıcılarda `crypto.getRandomValues`, diğerlerinde `Math.random` kullanılır.
