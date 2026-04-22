# Tolga Yenigün — Kişisel Portföy

Gazeteci ve dijital medya yöneticisi Tolga Yenigün'ün editorial/dergi estetiğinde tek sayfalık kişisel portföy sitesi.

**Canlı:** https://tolgayenigun.com/

## İçerik

Site aşağıdaki bölümlerden oluşur:

- **Hero** — Ad, unvan ve portre
- **Hakkında** — Kariyer özeti + istatistikler
- **Deneyim** — 2004'ten bugüne görevler (Cumhuriyet, Milliyet, Hürriyet, Günboyu, Kort, Ribaund, TE Bilişim)
- **Röportajlar** — Konuşulan önde gelen isimler
- **Öne Çıkan Sunum** — Google Keşfet & News haberciliği eğitim programı
- **Eğitim & Uzmanlık**
- **İletişim**

## Teknik

Bağımlılığı olmayan tek dosya (`index.html`). Vanilla HTML, CSS ve JavaScript.

- **Tipografi:** Fraunces (serif), Inter Tight (sans), JetBrains Mono (mono) — Google Fonts
- **SEO:** Open Graph, Twitter Card, JSON-LD `Person` schema, canonical URL
- **Erişilebilirlik:** `skip-link`, `aria-labelledby`, `focus-visible` outline, `prefers-reduced-motion` desteği
- **Mobil:** 900px altında drawer hamburger menü (backdrop + Escape kapatma)
- **Performans:** Inline SVG favicon, görsel için `fetchpriority` + boyut atribütleri (CLS önleme)
- **Dinamik yıl:** `data-years-since` attribute'lu alanlar (hero, hakkında, deneyim başlığı, istatistik, röportajlar) `new Date().getFullYear()` üzerinden kendiliğinden güncellenir. Footer telif yılı da dinamik.

## Dosya yapısı

```
.
├── index.html    Tüm site (HTML + CSS + JS)
├── photo.jpg     Portre fotoğrafı
├── .gitignore
└── README.md
```

## Lokal geliştirme

Harici bir derleme adımı yok — dosyayı doğrudan tarayıcıda açabilirsin:

```bash
open index.html
```

Ya da yerel bir sunucu üzerinden (relative path testleri için önerilir):

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Yayın

Site **Vercel** üzerinden **tolgayenigun.com** özel alan adı ile yayındadır.

- `main` branch'ine yapılan her push otomatik olarak üretime dağıtılır (Vercel Git entegrasyonu).
- Statik bir site olduğu için Vercel'in varsayılan ayarları yeterlidir; `vercel.json` ya da özel build komutu gerekmez.
- Alan adı Vercel Dashboard → **Settings → Domains** üzerinden yönetilir.

Alan adı değişirse aşağıdaki alanların da güncellenmesi gerekir:

- `<link rel="canonical">`
- `<meta property="og:url">` ve `<meta property="og:image">`
- `<meta name="twitter:image">`
- JSON-LD `Person` şemasındaki `url` ve `image`

## Lisans

Bu repo kişisel bir portföy sitesidir. İçerik (metin, fotoğraf) telif hakkıyla koruma altındadır ve izin alınmadan çoğaltılamaz.
