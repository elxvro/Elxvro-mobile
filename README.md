# ELXVRO App v1.0.1

ELXVRO Web v4.7.1 referans alınarak hazırlanan Flutter mobil/masaüstü istemci başlangıcıdır.

## GitHub üzerinden APK

Bu proje **Flutter** projesidir; `npm install` veya `package.json` kullanılmaz.

GitHub deposunda `.github/workflows/` altında eski bir Node/npm workflow'u varsa silin. APK için gereken workflow:

- `.github/workflows/build-apk.yml`

Ardından GitHub'da **Actions → Build ELXVRO Android APK → Run workflow** yolunu kullanın. Build tamamlanınca **Artifacts → ELXVRO-APK-v1.0.1** içinden `app-release.apk` dosyasını alın.

## API

Gerçek ELXVRO web bağlantısı için `lib/config/app_config.dart` içindeki `apiBaseUrl` daha sonra gerçek API adresine çevrilecektir. Şu an demo modundadır.
