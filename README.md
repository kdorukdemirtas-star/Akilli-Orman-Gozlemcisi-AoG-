# Akıllı Orman Gözlemcisi (AOG)

**TEKNOFEST 2026 · Defenders of Green**

Akıllı Orman Gözlemcisi (AOG), orman yangınlarını erken aşamada tespit etmeyi hedefleyen; LoRa haberleşmesi, sıcaklık sensörü ve biyolojik bir yangın geciktirici kaplama ile desteklenmiş bir uzaktan izleme sistemidir. Bu depo, projenin tek dosyalık (single-page) web/PWA arayüzünü içerir.

## Özellikler

- **Harita** — Verici (AOG-TX) ve alıcı (AOG-RX) düğümlerin canlı konumu, telefon GPS'i ile arasındaki mesafe, anlık sıcaklık ve LoRa RSSI sinyal göstergesi.
- **Zırh** — Aloe vera & silika tabanlı yangın geciktirici biyolojik kaplamanın TGA/DSC laboratuvar verileri ve kaplama yenileme kayıt defteri.
- **YTÜ Analiz** — Yıldız Teknik Üniversitesi Merkez Laboratuvarı'nda yapılan TGA-DSC ve FTIR-ATR analizlerinin numune bazlı sonuçları, ham veri setleri ve tam Drive klasörüne bağlantı.
- **Belgeler** — PDF rapor, Excel veri setleri, proje görselleri ve donanım bilgileri.
- **Ayarlar** — Bildirim tercihleri, alarm eşikleri ve sistem/proje bilgileri.

## Donanım

| Bileşen | Açıklama |
|---|---|
| Mikrodenetleyici (TX/RX) | Deneyap Kart 1A v2 |
| Sıcaklık Sensörü | MAX6675 Termokupl |
| Haberleşme | Ra-02 LoRa 433 MHz |
| Bulut | Supabase Realtime DB |
| Menzil | 1 – 5 km |
| Güç Kaynağı | Powerbank (~6 ay) |

## Teknoloji

- Saf HTML / CSS / JavaScript (framework yok, derleme adımı gerektirmez)
- [Leaflet.js](https://leafletjs.com/) — canlı harita
- PWA desteği (`manifest.json`, `sw.js` service worker ile çevrimdışı önbellekleme)

## Yerel Çalıştırma

Herhangi bir statik dosya sunucusu yeterlidir:

```bash
python3 -m http.server 8000
```

Ardından `http://localhost:8000` adresini açın.

## Vercel'e Deploy

Bu proje bir derleme adımı gerektirmediği için Vercel'de "Other" framework ayarıyla doğrudan import edilebilir:

1. Depoyu Vercel'de bir proje olarak içe aktarın.
2. Framework Preset: **Other**, Build Command: *(boş)*, Output Directory: *(kök dizin)*.
3. Deploy edin.

`vercel.json` dosyası statik dosya başlıkları ve temiz URL ayarlarını içerir.

## Ekip

**Defenders of Green** — TEKNOFEST 2026
