# Republic AI Points Tracker

## Proje Özeti
Republic AI testnet üzerinde cüzdan adresi sorgulayan, RAI bakiyesi ve tahmini puan gösteren tek sayfalık web uygulaması.

## Dosya Konumu
```
/root/republic-points-tracker/index.html
```

## Teknik Bilgiler
- **Stack:** Vanilla HTML/CSS/JS (framework yok)
- **EVM RPC:** https://evm-rpc.republicai.io
- **Chain ID:** 77701 (Republic Testnet)
- **Block Explorer:** https://explorer.republicai.io
- **Adres Formatı:** `rai1...` (Keplr/Cosmos bech32) — otomatik olarak EVM hex'e dönüştürülür

## Özellikler
- `rai1...` Keplr cüzdan adresi girişi (bech32 → EVM otomatik dönüşüm)
- RAI bakiyesi gösterimi
- Gönderilen TX sayısı
- Tahmini puan hesabı: `(tx × 150) + (bakiye × 5)`
- Network durumu ve son blok numarası
- Block Explorer linki

## Puan Formülü (Tahmini)
- İşlem puanı: tx_sayısı × 150
- Bakiye puanı: bakiye × 5 (max 5000)
- Toplam = ikisinin toplamı

## Deploy
- **Platform:** Netlify
- **Canlı URL:** https://republic-points-tracker-cesariumeth.netlify.app
- **Komut:**
  ```bash
  cd /root/republic-points-tracker
  netlify deploy --prod --dir .
  ```

## GitHub
- **Repo:** https://github.com/cesareth/republic-points-tracker-cesariumeth
- **Hesap:** cesareth
- **Push komutu:**
  ```bash
  git add . && git commit -m "mesaj" && git push origin master
  ```

## Yapılacaklar / Geliştirme Fikirleri
- [x] Netlify'a deploy edildi
- [x] rai1... Keplr adresi desteği eklendi (bech32 → EVM dönüşüm)
- [x] GitHub'a yüklendi
- [ ] Republic resmi puan programı açıklandığında formülü güncelle
- [ ] Leaderboard ekle
- [ ] Birden fazla cüzdan karşılaştırma
