# Nesnel Kanıt (Objective Evidence) Kontrol Kartı

ISO/IEC 27001 denetçileri için sahadaki soru kalıpları, kabul edilebilir nesnel kanıt türleri ve geçersiz sayılan sözlü beyanlar rehberi:

| Kontrol Alanı | Denetçinin Temel Sorusu | Kabul Edilebilir Nesnel Kanıt Türü | Yetersiz / Reddedilen Beyan |
| :--- | :--- | :--- | :--- |
| **A.5.7 Tehdit İstihbaratı** | Kurum tehdit verilerini nereden alıyor ve savunmaya nasıl aktarıyor? | MISP, CTI abonelik faturaları, firewall/EDR entegrasyon kuralları, IOC engelleme listeleri. | *"Siber bültenleri e-posta ile takip ediyoruz."* (Kayıtsız/operasyonsuz) |
| **A.5.23 Bulut Güvenliği** | Bulut sağlayıcılarınızın güvenlik sertifikalarını nasıl takip ediyorsunuz? | AWS Artifact / Azure Trust portalından indirilmiş güncel SOC 2 / ISO 27001 raporları, SLA matrisleri. | *"Zaten Amazon güvencesinde, onlar dünya devi."* |
| **A.8.9 Yapılandırma Yönetimi** | Sunucularda sıkılaştırma (hardening) yapıldığını nasıl doğrularsınız? | CIS Benchmark denetim çıktısı, Ansible playbook'ları, Terraform drift raporları. | *"Sistem yöneticimiz işi iyi bilir, gereksiz portları kapatır."* |
| **A.8.10 Bilgi Silme** | Süresi dolan müşteri verileri nasıl imha ediliyor? | DB purge script logları, Wiping tutanakları, manyetik ortam degauss / fiziksel kırım sertifikaları. | *"Veritabanından siliyoruz, geri gelmez."* |
| **A.8.12 DLP (Sızıntı Önleme)** | USB ve e-posta ile veri çıkışı nasıl engelleniyor? | Endpoint DLP ajan logları, engellenen veri transferi alarmları, USB yetkilendirme istisna listesi. | *"Çalışanlarımızla gizlilik sözleşmesi imzaladık."* |
| **A.8.28 Güvenli Kodlama** | Kodlama aşamasında zafiyetler nasıl taranıyor? | CI/CD pipeline'da SonarQube/Checkmarx tarama logları, engellenen güvensiz PR kayıtları. | *"Yazılımcılarımız tecrübelidir, dikkat eder."* |
| **Madde 9.2 İç Tetkik** | İç tetkik bağımsızlığı nasıl sağlandı? | Tetkikçi sertifikaları, kendi sürecini denetlemeyen çapraz denetim görevlendirme yazısı ve rapor. | *"IT müdürü tüm IT süreçlerini tek başına denetledi."* |
| **Madde 9.3 YGG** | Yönetim sistemi performansını üst yönetim ne zaman inceledi? | Yıllık YGG toplantı tutanağı, sunum dosyası, üst yönetim imzalı karar listesi ve aksiyon takip formu. | *"Yönetimle her pazartesi ayaküstü konuşuyoruz."* |
