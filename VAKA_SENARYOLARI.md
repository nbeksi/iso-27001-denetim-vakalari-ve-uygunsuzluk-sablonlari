# ISO/IEC 27001:2022 Uygulamalı Denetim Vakaları

Bu belgede yer alan vaka senaryoları; ISO/IEC 27001 baş denetçi eğitimlerinde, denetim simülasyonlarında ve iç tetkikçi atölyelerinde kullanılan gerçekçi denetim durumlarıdır.

Her vaka; senaryoyu, ilk denetim temasını, denetçinin derinleşme adımlarını, tespit edilen durumu ve yazılması gereken uygunsuzluk tipini içerir.

---

## 📌 Vaka 1: Liderlik ve Risk Değerlendirme Metodolojisi

- **İlgili Standart Maddeleri:** Madde 5.3 (Kurumsal Roller, Yetki ve Sorumluluklar), Madde 6.1.2 (Bilgi Güvenliği Risk Değerlendirmesi).
- **Denetim Ortamı:** Bir e-ticaret firmasının genel müdürlük binasında Aşama 2 (Stage 2) belgelendirme denetimi.

### Senaryo ve Denetçi Gözlemi:
Denetçi, BGYS Yöneticisi ile mülakat yapmaktadır. Kurumun Risk Değerlendirme Prosedürü incelendiğinde; risk kabul kriterlerinin yönetim kurulunca yılda bir kez onaylandığı ve risk puanı 15 ve üzeri olan tüm risklerin zorunlu olarak "Risk İşleme Planı"na alınması gerektiği belirtilmiştir.

Denetçi, güncel Risk İşleme Planı'nı (RTP) talep eder. İncelenen tabloda, "Ödeme Geçidi API Entegrasyonunda Zafiyet" riski 16 puan (Yüksek) olarak hesaplanmış, ancak tablonun aksiyon sütununda *"Maliyet yüksek olduğu için risk kabul edildi"* notu düşülmüştür. Bu risk kabul kararının altında ise yalnızca Yazılım Ekip Lideri'nin imzası yer almaktadır.

### Denetçinin Derinleşme Sorusu:
> *"Risk kabul kriterlerinizde 15 üzeri risklerin kabul edilebilmesi için kimin yetkilendirildiği tanımlandı mı? Madde 5.3 ve 6.1.3 (f) gereğince risk sahiplerinin risk işleme planını ve artık riskleri onaylama yetkisi dokümante edildi mi?"*

### Sonuç ve Bulgu Türü:
Kurumda risk sahipliği matrisi açıkça tanımlanmamış, yönetim kurulunun belirlediği risk iştahı aşılarak operasyonel düzeydeki bir ekip liderinin onayıyla yüksek risk kabul edilmiştir.
- **Bulgu Sınıfı:** **Majör Uygunsuzluk** (Madde 6.1.3 f ve Madde 5.3 ihlali).

---

## 📌 Vaka 2: İK Güvenliği, Yetkinlik ve Sosyal Mühendislik

- **İlgili Standart Maddeleri:** Madde 7.2 (Yetkinlik), Madde 7.3 (Farkındalık), Ek-A 6.3 (Bilgi Güvenliği Farkındalığı, Eğitimi ve Öğretimi).
- **Denetim Ortamı:** Finansal teknoloji kuruluşu, İK ve Eğitim Departmanı tetkiki.

### Senaryo ve Denetçi Gözlemi:
Kurumun BGYS Farkındalık Prosedürü'nde, yılda en az iki kez tüm çalışanlara yönelik kimlik avı (phishing) simülasyonu yapılacağı ve simülasyonda linke tıklayan/bilgi paylaşan personelin 15 gün içinde zorunlu tazeleme eğitimine alınacağı kurala bağlanmıştır.

Denetçi, 6 ay önce yapılan son phishing testinin sonuç raporunu ve ardından düzenlenen eğitim katılım kayıtlarını talep eder. Raporda 42 personelin oltalama e-postasındaki bağlantıya tıkladığı görülmektedir. Ancak İK eğitim takip sisteminde, bu 42 personelden yalnızca 11'inin tazeleme eğitimini tamamladığı, kalan 31 personel için herhangi bir takip, uyarı veya telafi eğitimi kaydı bulunmadığı tespit edilir.

### Sonuç ve Bulgu Türü:
Kurum kendi belirlediği farkındalık ve yetkinlik prosedürünü işletmemiş, zafiyet gösteren çalışanlar için tanımlı düzeltici eylem tamamlanmamıştır.
- **Bulgu Sınıfı:** **Minör Uygunsuzluk** (Madde 7.2 ve Ek-A 6.3 ihlali).

---

## 📌 Vaka 3: Teknik Açıklıkların Yönetimi ve Zafiyet Tarama SLA'leri

- **İlgili Standart Maddeleri:** Ek-A 8.8 (Teknik Açıklıkların Yönetimi), Madde 8.1 (Operasyonel Planlama ve Kontrol).
- **Denetim Ortamı:** Bulut tabanlı SaaS sağlayıcısı, DevOps ve Bilgi Güvenliği Operasyonları tetkiki.

### Senaryo ve Denetçi Gözlemi:
Kurumun Zafiyet Yönetimi Prosedürü uyarınca; internete açık sunucularda tespit edilen "Kritik (CVSS 9.0+)" seviyedeki zafiyetlerin en geç 7 gün, "Yüksek (CVSS 7.0–8.9)" seviyedeki zafiyetlerin ise 30 gün içinde yamalanması veya geçici hafifletici kontrol (mitigation) uygulanması şart koşulmuştur.

Denetçi, SOC ekibinin kullandığı zafiyet yönetim panelinden (Tenable/Qualys) rastgele 10 adet kritik açık örneği seçer. Örneklem içerisindeki 2 adet kritik açıklığın (uzaktan kod çalıştırma zafiyeti) 45 gündür açık olduğu, bilet sisteminde "Geliştirme ekibinin sprint yoğunluğu nedeniyle bekletiliyor" notu bulunduğu, ancak herhangi bir geçici telafi edici kontrolün (WAF kuralı, IP kısıtlaması vb.) devreye alınmadığı ve bu istisnanın risk yöneticisine onaylatılmadığı görülür.

### Sonuç ve Bulgu Türü:
- **Bulgu Sınıfı:** **Majör Uygunsuzluk** (Açık hedefte aktif kritik açıklıkların prosedür süreleri dışında korumasız bırakılması - Ek-A 8.8).

---

## 📌 Vaka 4: Kriptografik Anahtar Yönetimi ve Bulut Şifreleme

- **İlgili Standart Maddeleri:** Ek-A 8.24 (Kriptografinin Kullanımı), Ek-A 5.23 (Bulut Hizmetlerinde Güvenlik).
- **Denetim Ortamı:** AWS ortamında barındırılan sağlık verisi işleyen yazılım şirketi tetkiki.

### Senaryo ve Denetçi Gözlemi:
Kurumun Kriptografi Politikası'nda; veritabanı yedeklerinin ve hassas müşteri verilerinin (PII) AES-256 algoritmasıyla şifrelenmesi ve şifreleme anahtarlarının AWS KMS (Key Management Service) üzerinde her 365 günde bir otomatik rotasyona tabi tutulması gerektiği yazılıdır.

Denetçi, AWS KMS konsolunda kullanılan anahtarları örnekler. Müşteri veritabanı şifrelemesinde kullanılan anahtar için "Otomatik Yıllık Rotasyon" seçeneğinin işaretlenmediği tespit edilir. Ancak anahtarın oluşturulma tarihi henüz 4 ay öncedir; yani fiilen 1 yıllık süre henüz aşılmamıştır ve anahtar güvenliği ihlal edilmemiştir.

### Sonuç ve Bulgu Türü:
Politika ile sistem yapılandırması arasında uyumsuzluk mevcuttur ancak henüz bir veri sızıntısı veya süre aşımı gerçekleşmemiştir. Sistemik bir çöküş değildir.
- **Bulgu Sınıfı:** **Minör Uygunsuzluk** (veya denetim heyetinin yaklaşımına göre **İyileştirme Fırsatı / OFI**).

---

## 📌 Vaka 5: Erişim Hakları ve Kullanıcı Yetki Gözden Geçirmesi

- **İlgili Standart Maddeleri:** Ek-A 5.15 (Erişim Kontrolü), Ek-A 5.18 (Erişim Hakları).
- **Denetim Ortamı:** Bankacılık yazılımı geliştiren kurum, Sistem Yönetimi ve Active Directory tetkiki.

### Senaryo ve Denetçi Gözlemi:
Erişim Hakları Prosedürü; çalışanların işten ayrılması durumunda Active Directory ve e-posta hesaplarının İK bildirimi sonrasında en geç 24 saat içinde pasife alınmasını zorunlu kılmaktadır.

Denetçi, son 3 ayda işten ayrılan 15 kişilik İK listesini alır ve Active Directory loglarıyla çapraz kontrol yapar. 14 personelin hesabı aynı gün içinde kapatılmıştır. Ancak 1 personelin (eski stajyer yazılımcı) hesabının işten ayrıldıktan sonra 18 gün boyunca aktif kaldığı, bu süre zarfında hesaba herhangi bir başarılı giriş yapılmadığı ve 18. günde rutin IT temizliği sırasında kapatıldığı tespit edilir.

### Sonuç ve Bulgu Türü:
İzole bir operasyonel aksama söz konusudur; hesap kullanılarak sisteme yetkisiz erişim sağlanmamıştır ve diğer 14 personelde süreç kusursuz işlemiştir.
- **Bulgu Sınıfı:** **Minör Uygunsuzluk** (Ek-A 5.18).
