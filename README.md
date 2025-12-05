# 🗺️ Google Haritalar AI Ajanı

[![Lisans: MIT](https://img.shields.io/badge/Lisans-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![n8n](https://img.shields.io/badge/n8n-Otomasyon-orange)](https://n8n.io/)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o-blue)](https://openai.com/)
[![AI Destekli](https://img.shields.io/badge/AI-Konuşmalı-brightgreen)](https://github.com)

> 💥 **xCodeWraith tarafından geliştirildi**

> **Doğal dil sohbeti ile Google Haritalar'dan işletme potansiyel müşterilerini çıkaran ve zenginleştiren konuşmalı AI ajanı.**

AI ile basitçe sohbet edin: "Los Angeles'ta 100 diş kliniği bul" ve otomatik olarak verileri toplamasını, zenginleştirmesini ve Google Sheets'e düzenlemesini izleyin.

---

## 📋 İçindekiler

- [Genel Bakış](#-genel-bakış)
- [Temel Özellikler](#-temel-özellikler)
- [Nasıl Çalışır](#-nasıl-çalışır)
- [Teknoloji Yığını](#-teknoloji-yığını)
- [Gereksinimler](#-gereksinimler)
- [Kurulum](#-kurulum)
- [Yapılandırma](#-yapılandırma)
- [Kullanım Örnekleri](#-kullanım-örnekleri)
- [Veri Alanları](#-veri-alanları)
- [Sorun Giderme](#-sorun-giderme)
- [Lisans](#-lisans)

---

## 🎯 Genel Bakış

**Google Haritalar AI Ajanı**, Google Haritalar'ı güçlü bir B2B potansiyel müşteri oluşturma aracına dönüştüren akıllı bir konuşma sistemidir. Manuel olarak işletme verilerini aramak ve kopyalamak yerine, gereksinimlerinizi anlayan ve tüm süreci otomatikleştiren bir AI ajanı ile sohbet edin.

### Bu Sistemi Özel Kılan Nedir?

- 🤖 **Doğal Dil Arayüzü** - İnsan bir asistanla konuşur gibi doğal sohbet
- 🧠 **AI Destekli Anlama** - GPT-4o isteklerinizi akıllıca yorumlar
- 🔄 **Otomatik Zenginleştirme** - E-postaları ve şirket geçmişlerini otomatik bulur
- 📊 **Akıllı Organizasyon** - Google Sheets'te verileri mükemmel şekilde yapılandırır
- ⚡ **Gerçek Zamanlı İşleme** - Sohbet ederken potansiyel müşterilerin dolmasını izleyin

### Bu Kimler İçin?

| Hedef Kitle | Kullanım |
|-------------|----------|
| 💼 **Satış Ekipleri** | Konum ve nişe göre hedefli potansiyel müşteri listeleri |
| 📞 **Soğuk Aramacılar** | Telefon numaralarını ve işletme bilgilerini anında alın |
| 📧 **E-posta Pazarlamacıları** | E-posta zenginleştirmesi ile iletişim bilgileri |
| 🏢 **B2B Ajansları** | Müşteriler için yerel işletme araştırması |
| 🚀 **Girişimciler** | Potansiyel müşteriler veya ortaklar bulun |

---

## ✨ Temel Özellikler

### 🗣️ Konuşma Arayüzü
- Doğal dil girişi: "NYC'de 50 restoran bul"
- Karmaşık formlar veya parametreler yok
- AI bağlamı ve niyeti anlıyor
- Çok turlu konuşmalar

### 🔍 Akıllı Google Haritalar Kazıma
- Serper.dev Google Maps API üzerinden arama
- Sayfalamayı otomatik yönetir
- Kapsamlı işletme verilerini çıkarır
- Koordinatlarla coğrafi hedefleme

### 📧 Otomatik E-posta Zenginleştirme
- Perplexity AI şirket e-postalarını buluyor
- Web sitelerinden otomatik kazıma
- Her işletme için arka plan araştırması
- Google Sheets'i gerçek zamanlı günceller

### 🔄 İki Aşamalı Workflow

```
┌──────────────────────────────────────────────────────────┐
│                    AŞAMA 1: VERİ TOPLAMA                 │
├──────────────────────────────────────────────────────────┤
│  Chat Trigger → AI Agent → Serper API → Alt Workflow     │
│                                              ↓           │
│                                    Google Sheets Kayıt   │
└──────────────────────────────────────────────────────────┘
                           ↓
┌──────────────────────────────────────────────────────────┐
│                 AŞAMA 2: ZENGİNLEŞTİRME                  │
├──────────────────────────────────────────────────────────┤
│  Sheets Trigger → Perplexity AI → Email & Background     │
│                                              ↓           │
│                                    Sheets Güncelleme     │
└──────────────────────────────────────────────────────────┘
```

---

## 🔄 Nasıl Çalışır

### Kullanıcı Deneyimi

```
Siz: "Los Angeles'ta 100 diş kliniği için bilgi çıkar"

AI Ajanı: "Los Angeles'ta diş kliniklerini arayacağım. Başlıyorum..."
         [Google Haritalar araması]
         [Birden fazla sayfada 100+ sonuç buluyor]
         [Google Sheets'e otomatik kaydediyor]

AI Ajanı: "✅ 97 diş kliniği buldum ve sayfanıza kaydettim!"

[Arka plan işlemi otomatik başlar]
         [Her potansiyel müşteriyi e-posta ve arka plan ile zenginleştirir]
         [Sayfayı zenginleştirilmiş verilerle günceller]
```

---

## 🛠️ Teknoloji Yığını

| Kategori | Teknoloji | Amaç |
|----------|-----------|------|
| **Otomasyon** | n8n | Workflow orkestrasyonu |
| **AI Ajanı** | OpenAI GPT-4o | Doğal dil anlama ve görev yürütme |
| **AI Bellek** | Buffer Window | Konuşma bağlamı saklama |
| **Harita Arama** | Serper.dev | İşletme verileri için Google Maps API |
| **Zenginleştirme** | Perplexity AI (Sonar) | E-posta bulma ve şirket araştırma |
| **Depolama** | Google Sheets | Potansiyel müşteri veritabanı |

---

## 📦 Gereksinimler

### Gerekli Hesaplar & API Anahtarları

| Servis | Gerekli mi? | Amaç | Maliyet |
|--------|-------------|------|---------|
| **n8n** | ✅ Evet | Workflow'ları çalıştır | Ücretsiz (self-hosted) veya $20/ay |
| **OpenAI** | ✅ Evet | GPT-4o AI ajanı | İstek başına ~$0.01-0.03 |
| **Serper.dev** | ✅ Evet | Google Haritalar araması | 5,000 arama için $50/ay |
| **Perplexity AI** | ✅ Evet | E-posta zenginleştirme | $20/ay veya kullanım başına |
| **Google Hesabı** | ✅ Evet | Google Sheets depolama | Ücretsiz |

---

## 🚀 Kurulum

> ⚠️ **ÖNEMLİ:** Bu sistem 2 ayrı workflow'dan oluşur. İkisi de ayrı ayrı import edilmeli ve birbirine bağlanmalıdır!

### 📦 Workflow Dosyaları

| Dosya | Tür | Açıklama |
|-------|-----|----------|
| `Google map ai agent.json` | **Ana Workflow** | Chat arayüzü ve AI ajanı |
| `Gooogle map lead ai agent.json` | **Alt Workflow** | Veri kaydetme ve UUID oluşturma |

---

### Adım 1: ÖNCELİKLE Alt Workflow'u İçe Aktarın

> 🔴 **SIRA ÖNEMLİ!** Alt workflow ÖNCE import edilmeli!

1. n8n'i açın
2. **"Workflows"** → **"Import from File"** tıklayın
3. `Gooogle map lead ai agent.json` seçin
4. **"Import"** tıklayın
5. ✅ Import edildikten sonra **workflow ID'sini not edin:**
   - URL'de görünür: `https://your-n8n.com/workflow/WORKFLOW_ID`

---

### Adım 2: Ana Workflow'u İçe Aktarın

1. **"Workflows"** → **"Import from File"** tıklayın
2. `Google map ai agent.json` seçin
3. **"Import"** tıklayın

---

### Adım 3: İki Workflow'u Birbirine Bağlayın

> 🔗 Ana workflow, alt workflow'u çağırabilmesi için bağlanmalı!

1. Ana workflow'u açın
2. **"Call n8n Workflow Tool"** node'unu bulun
3. Node'a tıklayın
4. **"Workflow"** alanında:
   - Dropdown'dan **"💥 xCodeWraith - Google Maps Lead Alt-Workflow"** seçin

---

### Adım 4: Google Sheet Oluşturun

1. https://sheets.google.com/ adresine gidin
2. Yeni elektronik tablo oluşturun: **"Leads Google map ai agent"**
3. 1. satırda başlıklar oluşturun:

```
UUID | Name | Address | Number | Website | Rating | Opening Hours | Email | Background
```

---

### Adım 5: Google Sheets Node'larını Güncelleyin

**Her iki workflow'da da** Google Sheets node'larını güncelleyin:

**Ana Workflow'da:**
- `Google Sheets Trigger` node → Spreadsheet ID'nizi seçin
- `Google Sheets` (update) node → Spreadsheet ID'nizi seçin

**Alt Workflow'da:**
- `Append row in sheet` node → Spreadsheet ID'nizi seçin

---

### Adım 6: Workflow'ları Aktifleştirin

1. **Ana workflow'u** açın → **"Active"** toggle'ını açın (yeşil)
2. **Alt workflow** pasif kalabilir (ana tarafından otomatik çağrılır)
3. Ana workflow'daki **"When chat message received"** node'una tıklayın
4. **"Production URL"** kopyalayın
5. Bu URL'yi tarayıcıda açarak chat arayüzüne erişin!

---

## ⚙️ Yapılandırma

### 1. OpenAI API Anahtarı

**Node:** "OpenAI Chat Model"

1. https://platform.openai.com/api-keys adresinden API anahtarı alın
2. n8n'de: **Settings** → **Credentials**
3. **"OpenAi account"** kimlik bilgisi ekleyin
4. API anahtarını yapıştırın

---

### 2. Serper.dev API Anahtarı

**Node:** "Map Search Tool"

1. https://serper.dev/ adresinden kayıt olun
2. Dashboard'dan API anahtarı alın
3. Node'da **Headers** bölümünü bulun
4. `X-API-KEY` değerini anahtarınızla güncelleyin

---

### 3. Perplexity API Anahtarı

**Node:** "Message a model1"

1. https://www.perplexity.ai/settings/api adresinden API anahtarı alın
2. n8n'de: **Settings** → **Credentials**
3. **"Perplexity account"** kimlik bilgisi ekleyin

---

### 4. Google Sheets OAuth

1. n8n'de: **Settings** → **Credentials**
2. **"Google Sheets OAuth2 API"** ekleyin
3. OAuth akışını takip edin

---

## 📖 Kullanım Örnekleri

### Örnek 1: Basit Arama

```
Siz: "Seattle'da 50 kahve dükkanı bul"

AI: ✅ 47 kahve dükkanı buldum ve kaydettim!
```

### Örnek 2: Spesifik Niş

```
Siz: "Los Angeles'ta 100 diş kliniği için bilgi çıkar"

AI: Los Angeles'ta diş kliniklerini arıyorum...
    100 sonuç = 5 sayfa taranacak
    ✅ 97 diş kliniği kaydedildi!
```

---

## 📊 Veri Alanları

| Alan | Açıklama | Kaynak |
|------|----------|--------|
| **UUID** | Benzersiz tanımlayıcı | Otomatik oluşturulur |
| **Name** | İşletme adı | Google Maps |
| **Address** | Tam adres | Google Maps |
| **Number** | Telefon numarası | Google Maps |
| **Website** | Şirket web sitesi | Google Maps |
| **Rating** | Google puanı | Google Maps |
| **Opening Hours** | Çalışma saatleri | Google Maps |
| **Email** | İletişim e-postası | Perplexity AI |
| **Background** | Şirket açıklaması | Perplexity AI |

---

## 🐛 Sorun Giderme

| Sorun | Çözüm |
|-------|-------|
| Sohbet arayüzü yüklenmiyor | Ana workflow'un **Aktif** olduğunu doğrulayın |
| Harita aramasından sonuç yok | Serper.dev API anahtarını kontrol edin |
| Veriler Sheets'e kaydedilmiyor | Google Sheets credential'larını doğrulayın |
| Alt workflow çalışmıyor | Workflow bağlantısını kontrol edin |

---

## 📈 Performans Metrikleri

| Metrik | Değer |
|--------|-------|
| **Arama Hızı** | 2 saniyede sayfa başına 20 sonuç |
| **Kazıma** | ~1 dakikada 100 potansiyel müşteri |
| **Zenginleştirme** | ~5-10 dakikada 60 potansiyel müşteri |
| **Doğruluk** | %90+ veri doğruluğu |
| **Günlük Kapasite** | 5,000-10,000 potansiyel müşteri |

---

## 📄 Lisans

Bu proje **MIT Lisansı** altında lisanslanmıştır.

✅ Ticari kullanım izni  
✅ Değişiklik izni  
✅ Dağıtım izni  
✅ Özel kullanım izni  
⚠️ Garanti veya sorumluluk yok

---

**💥 xCodeWraith tarafından ❤️ ile yapıldı**

⭐ Potansiyel müşteri oluşturmanıza yardımcı oluyorsa bu repoyu yıldızlayın!

---

**Binlerce potansiyel müşteri oluşturmaya hazır mısınız?** Şimdi AI ajanınızla sohbet etmeye başlayın! 🗺️
