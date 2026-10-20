# Şeker Eşeği – Mobil Uygulama Paketi

Oyun `www/index.html` içinde. Capacitor ile Android (APK/AAB) ve iOS (IPA) uygulamasına çevrilir.

## A) En kolay: APK'yı bulutta derle (bilgisayara Android Studio kurmadan)
1. GitHub'da ücretsiz bir depo aç, bu klasörün içeriğini yükle.
2. Actions sekmesi → "Android APK" → Run workflow.
3. Bitince "seker-esegi-apk" dosyasını indir → telefona at → yükle (test için). 

## B) Bilgisayarda
Gerekenler: Node 20+, Android Studio (Android), Xcode + Mac (iOS).
    npm install
    npm run add:android      # iOS için: npm run add:ios
    npm run assets           # ikon + açılış ekranı (resources/icon.svg'den)
    npm run sync
    npm run open:android     # Android Studio açılır: Build > Generate Signed Bundle (AAB)

## Mağazaya yüklemek için
- Google Play: Geliştirici hesabı (tek sefer 25 $), imzalı **AAB**, ikon, ekran görüntüleri, gizlilik politikası.
- App Store: Apple Developer (yıllık 99 $), Mac + Xcode, TestFlight → App Store Connect.
- `capacitor.config.json` içindeki `appId` değerini kendi benzersiz kimliğinle değiştir (örn. com.seninadin.sekeresegi).
- Oyun yerel kayıt kullanır (localStorage) ve çevrimdışı çalışır; veri toplamadığı için gizlilik politikası kısa olabilir.
