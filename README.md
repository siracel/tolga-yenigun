# Tolga Yenigün — Kişisel Portföy

Gazeteci ve dijital medya yöneticisi Tolga Yenigün'ün editorial/dergi estetiğinde tek sayfalık kişisel portföy sitesi.

**Canlı:** https://siracel.github.io/tolga-yenigun/

## İçerik

Site aşağıdaki bölümlerden oluşur:

- **Hero** — Ad, unvan ve portre
- **Hakkında** — Kariyer özeti + istatistikler
- **Deneyim** — 2004'ten bugüne görevler (Cumhuriyet, Milliyet, Hürriyet, Günboyu/Yeniçağ, Kort, Ribaund, TE Bilişim)
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

## Yayına alma (GitHub Pages)

1. Repo **Settings → Pages**
2. **Source:** `Deploy from a branch`
3. **Branch:** `main` / `/ (root)` → **Save**
4. Birkaç dakika içinde site yayında olur.

Custom domain kullanılacaksa Pages ayarlarından ekle ve `index.html` içindeki `canonical` / `og:url` / `og:image` bağlantılarını yeni domain ile güncelle.

## Lisans

Bu repo kişisel bir portföy sitesidir. İçerik (metin, fotoğraf) telif hakkıyla koruma altındadır ve izin alınmadan çoğaltılamaz.
