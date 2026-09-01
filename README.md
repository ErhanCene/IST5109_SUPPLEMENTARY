# IST5109 — Ders Verileri

**IST5109 İleri Aktüerya Teknikleri** dersinde kullanılan veri dosyaları burada
durur. Ders notlarındaki bütün sayılar bu dosyalardan üretilmiştir.

## Nasıl indirilir?

- **Tek dosya:** `data/` klasöründe dosyanın üstüne tıklayın, açılan sayfada
  **Download raw file** düğmesini kullanın.
- **Hepsi birden:** bu sayfanın üstündeki yeşil **Code** düğmesi → **Download ZIP**.

İndirdiğiniz dosyaları, çalıştıracağınız R betiğinin yanında bir
`data/derived/` klasörüne koyun. Ders notlarındaki yollar o zaman olduğu gibi
çalışır:

```r
veri_yolu <- file.path("data", "derived", "auto_claims.csv")
```

## Üç önemli uyarı

**1. Bu dosyalar değişmez.** Dönem boyunca aynı kalırlar. Amaç tektir: aynı kodu
çalıştıran herkes aynı sayıyı görsün.

**2. Kaynağından yeni bir kopya çekmeyin.** Dosyaların bir kısmı R paketlerinden
gelir (`insuranceData`, `lifecontingencies`, `ChainLadder`), ama buradaki kopyalar
o paketlerdeki hâlleriyle **aynı değildir** — bir kısmı örneklenmiş, bir kısmı
öğretim için bilerek değiştirilmiştir. Paketten okursanız ders notundaki sayıları
tutturamazsınız.

**3. `auto_claims.csv` bilerek kusurludur.** Kaynak veri eksiksiz temizdir; o
hâliyle Hafta 2'nin veri temizleme konusu gösterilemezdi. Bu yüzden dosyaya
eksik değerler, geçersiz tutarlar ve yinelenen satırlar **öğretim amacıyla**
eklenmiştir. Bu dosyayı ders dışında hiçbir analizde kullanmayın.

## Dosyalar

| Dosya | Satır | Sütun | Hangi hafta |
|---|---:|---:|---|
| `auto_claims.csv` | 6.776 | 6 | Hafta 2 — ders anlatımı |
| `auto_claims_truth.csv` | 6.773 | 2 | Hafta 2 — yalnızca MNAR bölümü |
| `auto_bi.csv` | 1.340 | 8 | Hafta 2 — laboratuvar |
| `danishuni.csv` | 2.167 | 1 | Hafta 3 |
| `canlifins_sample.csv` | 2.000 | 6 | Hafta 5 |
| `tuik_life_table.csv` | 606 | 9 | Hafta 6 ve 7 |
| `life_expectancy_education.csv` | 108 | 4 | Hafta 6 |
| `healthy_life_expectancy.csv` | 57 | 5 | Hafta 6 |
| `data_car.csv` | 67.856 | 10 | Hafta 9 |
| `genins_long.csv` | 55 | 3 | Hafta 10 |
| `data_manifest.csv` | 10 | 7 | — (aşağıya bakın) |

### `auto_claims_truth.csv` nedir?

Hafta 2'de eksik değerlerin bir kısmı **büyük hasarlardan** seçilerek silinmiştir
(MNAR). Silinen değerlerin gerçekte ne olduğunu görebilmek için, silme öncesi
tutarlar ayrı bir dosyada saklanmıştır. **Gerçek hayatta böyle bir dosya
yoktur** — kaybın büyüklüğünü ölçebiliyor olmamızın nedeni yöntemin iyiliği
değil, kaybı bizim üretmiş olmamızdır. Not bunu açıkça söyler ve dosyayı yalnızca
tek bir bölümde okur.

### `data_manifest.csv` nedir?

Her dosyanın **nereden geldiğini** kaydeder: kaynak adı, kaynak adresi, kopyanın
alındığı tarih, lisans bilgisi ve dosyaya özgü notlar. Bir sayının nereden
geldiğini merak ettiğinizde önce buraya bakın.

## Kaynaklar ve lisans

Dosyaların kaynakları `data_manifest.csv` içinde tek tek yazılıdır. Kısaca:

- **TÜİK hayat tabloları** — TÜİK'in yayımladığı tablolardır; kaynak gösterimi ve
  portal koşulları geçerlidir.
- **R paketlerinden gelen veriler** (`insuranceData`, `ChainLadder` ve benzerleri)
  — ilgili paketlerin lisansları geçerlidir; buradaki kopyalar öğretim amaçlıdır.

Bu depo yalnızca ders için vardır. Ticari bir tarife ya da fiyatlandırma
çıkarımında kullanılmaz.
