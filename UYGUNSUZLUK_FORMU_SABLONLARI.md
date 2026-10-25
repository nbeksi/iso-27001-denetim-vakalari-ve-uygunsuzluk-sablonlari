# ISO 19011 Uygunsuzluk Raporlama Şablonları (NCR)

Uluslararası akredite ISO/IEC 27001 belgelendirme denetimlerinde denetçilerin en çok zorlandığı konu, tespit edilen bulguların standart diliyle net, tartışmaya yer bırakmayacak ve nesnel kanıtlarla desteklenmiş biçimde yazılmasıdır.

---

## 📐 Üçlü Formülasyon Kuralı (The 3-Part Statement)

Geçerli ve kabul edilebilir bir uygunsuzluk raporu (Non-Conformity Report - NCR) mutlaka şu 3 unsuru içermelidir:

1. **Uygunsuzluk İfadesi (Statement of Non-Conformity):** Ne eksik, ne yanlış yapılmış? (Duygudan uzak, net ve tarafsız).
2. **Nesnel Kanıt (Objective Evidence):** Nerede, hangi belgede, hangi tarihte veya kimin kaydında tespit edildi? (Örneklem referansı, dosya no, bilet ID vb.).
3. **Standart Şartı / Referans Kriter (Requirement):** ISO/IEC 27001 standardının hangi maddesi veya kurumun hangi iç prosedürü ihlal edildi?

> ❌ **Hatalı Yazım:** "Zafiyet yönetimi kötü yapılıyor ve sunucular tehlikede." *(Kişisel kanaat, kanıt yok, standart maddesi yok).*  
> ✅ **Doğru Yazım:** "Kurumun Zafiyet Yönetimi Prosedürü Madde 4.2'de kritik açıkların 7 günde kapatılması gerektiği belirtilmesine rağmen; internete açık web sunucusunda tespit edilen CVE-2024-XXXX zafiyetinin 45 gündür kapatılmadığı ve risk onayının alınmadığı tespit edilmiştir. (İhlal edilen şart: ISO/IEC 27001:2022 Ek-A 8.8)."

---

## 📝 1. Majör Uygunsuzluk Raporu Şablonu

```markdown
# UYGUNSUZLUK RAPORU (NCR) - MAJÖR

- Rapor No: NCR-2026-001
- Denetlenen Kurum / Departman: 
- Denetim Türü: [ ] Aşama 1  [x] Aşama 2  [ ] Gözetim  [ ] Yeniden Belgelendirme
- İlgili Standart: ISO/IEC 27001:2022
- İlgili Standart Maddesi / Kontrolü: 
- Sınıflandırma: [x] MAJÖR UYGUNSUZLUK

1. UYGUNSUZLUK TANIMI:
[Standardın bir gereksiniminin tamamen işletilmediği veya BGYS'nin hedeflerine ulaşma kabiliyetini doğrudan riske atan durumun açıklaması]

2. NESNEL KANIT (OBJECTIVE EVIDENCE):
[İncelenen doküman adı, versiyonu, sistem kaydı, bilet numarası veya örneklem detayı]

3. İHLAL EDİLEN ŞART / POLİTİKA:
[İlgili ISO 27001 maddesi veya iç politika maddesi referansı]

4. KÖK NEDEN ANALİZİ VE DÜZELTİCİ FAALİYET TAAHHÜDÜ (Denetlenen Tarafça Doldurulur):
- Kök Neden: 
- Anlık Düzeltme (Correction): 
- Düzeltici Faaliyet (Corrective Action): 
- Tamamlanma Hedef Tarihi: 

Denetçi Adı / İmzası: ___________________    Tarih: __/__/2026
```

---

## 📝 2. Minör Uygunsuzluk Raporu Şablonu

```markdown
# UYGUNSUZLUK RAPORU (NCR) - MİNÖR

- Rapor No: NCR-2026-002
- Denetlenen Departman: 
- İlgili Standart: ISO/IEC 27001:2022
- İlgili Standart Maddesi: 
- Sınıflandırma: [x] MİNÖR UYGUNSUZLUK

1. UYGUNSUZLUK TANIMI:
[Yönetim sisteminin genel işleyişini bozmayan, izole bir operasyonel aksama veya kısmi uygulama eksikliği]

2. NESNEL KANIT:
[Örneklem içerisindeki tekil aykırılık referansı]

3. İHLAL EDİLEN ŞART:
[Madde / Kontrol referansı]

Denetçi Adı / İmzası: ___________________    Tarih: __/__/2026
```

---

## 📝 3. İyileştirme Fırsatı / Gözlem Formu (OFI)

```markdown
# İYİLEŞTİRME FIRSATI / GÖZLEM (OFI)

- Rapor No: OFI-2026-001
- İlgili Süreç: 
- İlgili Standart: ISO/IEC 27001:2022

1. GÖZLEM TANIMI:
[Mevcut durumda standarda aykırı bir uygunsuzluk bulunmamakla birlikte, gelecekte bir uygunsuzluğa dönüşme riski taşıyan veya sistemin etkinliğini artırabilecek potansiyel gelişim alanı]

2. MEVCUT DURUM KANITI:
[Gözlemlenen operasyonel durum]

3. DENETÇİ TAVSİYESİ (Rehberlik):
[Tarafsız, danışmanlık sınırına girmeyen profesyonel tavsiye]
```
