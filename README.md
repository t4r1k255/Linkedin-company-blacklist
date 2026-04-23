# 🚫 LinkedIn — Şirket Kara Listesi
**LinkedIn — Company Blacklist**

LinkedIn iş arama sonuçlarında belirli şirketlerin ilanlarını gizler. Şirket eklemek için sağ tık menüsünü veya yönetim panelini kullanabilirsin.

> Yalnızca `/jobs` sayfalarında çalışır.

---

## ✨ Özellikler

- 🖱️ **Sağ tık menüsü** — şirket adına sağ tıkla, tek tuşla kara listeye ekle veya çıkar
- ⚙️ **Yönetim paneli** — tüm listeyi görüntüle, düzenle, dışa/içe aktar
- 🔤 **Regex desteği** — `/holding/i` gibi bir desen girerek birden fazla şirketi tek seferde yakala
- 🔢 **Sayaç rozeti** — sol üstte kaç ilanın gizlendiğini gösterir
- 🔴 **Aç/kapat butonu** — gizlemeyi geçici olarak devre dışı bırak, listeyi bozmadan
- 💾 **Kalıcı depolama** — liste `localStorage`'a kaydedilir, sayfa yenilense de silinmez
- ↕️ **Dışa / İçe aktar** — listeyi `.json` dosyası olarak yedekle veya başka bir tarayıcıya taşı

---

## 🚀 Kurulum

### Gereksinimler

Tarayıcında bir userscript yöneticisi gereklidir:

| Tarayıcı | Önerilen Eklenti |
|----------|-----------------|
| Chrome / Edge | [Tampermonkey](https://www.tampermonkey.net/) |
| Firefox | [Violentmonkey](https://violentmonkey.github.io/) |
| Safari | [Userscripts](https://apps.apple.com/app/userscripts/id1463298887) |

### Adımlar

1. Yukarıdaki eklentilerden birini kur.
2. Eklenti panosunu aç → **"Yeni script oluştur"** seçeneğine tıkla.
3. `linkedin-company-blacklist.user.js` dosyasının içeriğini kopyala ve editöre yapıştır.
4. `Ctrl+S` / `Cmd+S` ile kaydet.
5. [linkedin.com/jobs](https://www.linkedin.com/jobs) adresine git — script otomatik çalışır.

---

## 🖥️ Kullanım

### Sağ Tık Menüsü

İş kartında şirket adına **sağ tıkla**. Küçük bir menü açılır:

- Listede yoksa → **🚫 Bu şirketi gizle**
- Listede varsa → **✓ Kara listeden çıkar**

### Rozet (Sol Üst)

Sayfa `/jobs` içerdiğinde sol üstte bir rozet belirir:

```
[ 4 gizli ] [ Kara Liste ] [ ⚙ Yönet ]
```

- **Kara Liste** butonuna basarak gizlemeyi açıp kapatabilirsin (liste bozulmaz).
- **⚙ Yönet** butonuyla yönetim panelini açabilirsin.

### Yönetim Paneli

- **Şirket adı girerek** ekle (tam eşleşme, büyük/küçük harf ve aksan duyarsız)
- **Regex deseni girerek** ekle: `/holding/i` → "ABC Holding", "XYZ Holdings" gibi hepsini yakalar
- Her satırda **✕** ile tek tek sil
- **↓ Dışa Aktar** → `linkedin-blacklist.json` olarak indir
- **↑ İçe Aktar** → daha önce dışa aktarılan `.json` dosyasını yükle
- **Tümünü Sil** → listeyi komple temizle (onay sorar)

## ⚠️ Yasal Uyarı

Bu script LinkedIn ile herhangi bir bağlantısı olmayan bağımsız bir topluluk aracıdır. LinkedIn'in [Kullanım Koşulları](https://www.linkedin.com/legal/user-agreement)'na uygun şekilde kullan.

---

## 📄 Lisans

[MIT License](LICENSE)
