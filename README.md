# ELXVRO App v1.0.0

Referans web surumu: **ELXVRO Web v4.7.1**

Bu depo Android APK'yi GitHub Actions ile uretecek sekilde hazirlanmistir. Bilgisayarinda Flutter kurulu olmak zorunda degildir.

## GitHub ile APK alma

1. ZIP'i cikart.
2. GitHub'da yeni, bos bir repository olustur.
3. Bu klasordeki **tum dosyalari** repository'ye yukle. `.github` klasorunun da yuklendiginden emin ol.
4. Dosyalari `main` dalina commit et.
5. GitHub'da **Actions** sekmesine gir.
6. `Build ELXVRO APK` workflow'unu ac.
7. Otomatik baslamadiysa `Run workflow` butonuna bas.
8. Islem bittiginde ilgili run sayfasinin altindaki **Artifacts > ELXVRO-APK** dosyasini indir.
9. ZIP artifact icinden `app-release.apk` cikar. Bu APK Android cihaza kurulabilir.

> Bu ilk gelistirme APK'sidir. Google Play'e yuklenecek surumde sana ait release keystore ile imzalama ayrica eklenecek.

## Gercek ELXVRO API baglantisi

`lib/config/app_config.dart` dosyasini ac ve:

```dart
static const String apiBaseUrl = 'https://example.com/api/v1';
```

satirini gercek API adresinle degistir.

Ornek:

```dart
static const String apiBaseUrl = 'https://elxvro.com/api/v1';
```

Adres `example.com` olarak kaldigi surece uygulama **demo modunda** calisir ve herhangi bir bos olmayan e-posta/sifreyle arayuze girilebilir.

## Mevcut ekranlar

- ELXVRO giris ekrani
- Google girisi icin hazir buton (API entegrasyonu bekliyor)
- Ana sayfa
- Kategoriler / arama / kaydedilenler icin giris kartlari
- Duyurular
- Destek merkezi
- Profil
- Mobil uyumlu alt navigasyon
- Genis ekranlarda kontrollu yerlesim

## Sonraki entegrasyon

Web v4.7.1 sunucusuna uygulama API'si eklendiginde su alanlar gercek veriye baglanacak:

- kullanici girisi ve token sistemi
- Google OAuth
- kategoriler ve icerikler
- arama
- duyurular
- destek talepleri
- profil ve hesap ayarlari
- surum/guncelleme kontrolu

## Guvenlik

MySQL bilgilerini Flutter uygulamasina yazma. Mobil uygulama yalnizca HTTPS API ile sunucuyla haberlesmelidir.
