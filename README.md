# Oxide Phantom Panel (Android ARM64)

Демонстрационный Android-проект с плавающей панелью в Phantom Purple.

## Что есть
- Отдельное приложение Android.
- Плавающая кнопка поверх окон (SYSTEM_ALERT_WINDOW).
- Открываемое/закрываемое меню с разделами AIMBOT, VISUALS, RADAR, MISC.
- Перетаскиваемая кнопка.
- Интерфейсные превью и подписи на русском.

## Важное ограничение
Это только интерфейсный макет. Он не подключается к Oxide: Survival Island,
не читает память игры, не рисует ESP по реальным игрокам и не автоматизирует
прицеливание. Пункты Aim Assist/ESP/Radar являются демонстрационными.

## Сборка APK
1. Распакуйте архив.
2. Откройте папку `OxidePhantomPanel` в Android Studio.
3. Дождитесь синхронизации Gradle.
4. Выберите Build -> Build Bundle(s) / APK(s) -> Build APK(s).
5. APK появится в `app/build/outputs/apk/debug/`.

Проект настроен на `arm64-v8a`-совместимые Android-устройства (код не содержит
нативных библиотек, поэтому APK может запускаться и на других ABI).
Требуется Android Studio с Android SDK Platform 35 и JDK 17.


## Облачная сборка через GitHub Actions

В архив добавлен workflow `.github/workflows/android.yml`. После загрузки файлов проекта в репозиторий GitHub на ветку `main`, откройте вкладку Actions и запустите `Build Android APK` (или дождитесь автоматической сборки после push). Готовый `app-debug.apk` появится в разделе Artifacts соответствующего запуска.
