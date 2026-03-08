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

## Özellikler
- 0x cüzdan adresi girişi
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
- Platform: Netlify
- Yöntem: `netlify deploy --prod --dir .`
- Komutlar:
  ```bash
  npm install -g netlify-cli
  cd /root/republic-points-tracker
  netlify deploy --prod --dir .
  ```

## Yapılacaklar / Geliştirme Fikirleri
- [ ] Netlify'a deploy et, canlı URL al
- [ ] Republic resmi puan programı açıklandığında formülü güncelle
- [ ] Leaderboard ekle
- [ ] Birden fazla cüzdan karşılaştırma
