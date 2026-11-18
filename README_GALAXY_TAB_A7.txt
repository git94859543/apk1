iOS 27 Liquid Glass Launcher — проект для сборки .APK под Samsung Galaxy Tab A7 (SM-T500 / SM-T505)
====================================================================================================

Этот архив содержит готовый исходный код Android Studio (Kotlin + WebView Launcher) и GitHub Actions
workflow для автоматической сборки установочного .apk файла.

ОСОБЕННОСТИ ПРОЕКТА:
1. Настроен как системный Home Launcher (CATEGORY_HOME + CATEGORY_DEFAULT) — планшет может открывать
   iOS 27 Liquid Glass сразу при нажатии кнопки «Домой».
2. Полный иммерсивный полноэкранный режим (скрывает панель навигации и статус-бар Android One UI).
3. Поддерживает аппаратное ускорение GPU (Adreno 610 на Snapdragon 662 в Galaxy Tab A7) для плавного
   backdrop-filter размытия Liquid Glass и режима Clear ↔ Tinted.

СПОСОБ 1 — Сборка без установки Android Studio (через GitHub Actions):
1. Создайте пустой репозиторий на GitHub и загрузите туда содержимое этой папки.
2. Откройте вкладку Actions → запустите workflow "Build Galaxy Tab A7 APK".
3. Скачайте готовый артефакт "ios27-liquid-glass-tab-a7-debug.apk" и установите на планшет.

СПОСОБ 2 — Сборка в Android Studio:
1. Откройте эту папку в Android Studio (Koala / Ladybug или новее).
2. Подключите Galaxy Tab A7 по USB с отладкой по USB (или выберите Build → Build APK(s)).
3. Установите app/build/outputs/apk/debug/app-debug.apk на планшет.

URL оболочки (зашит в MainActivity.kt): https://ais-dev-e6kzljkq2nbxcmbz2rblcl-1012548962491.europe-west2.run.app
При необходимости вы можете заменить URL в MainActivity.kt или положить статическую сборку (dist/)
в папку app/src/main/assets/www/ и переключить loadUrl на "file:///android_asset/www/index.html".
