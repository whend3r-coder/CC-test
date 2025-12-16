# Minimal Android App

Eine einfache Android App, die automatisch via GitHub Actions zu einer APK kompiliert wird.

## Features

- Minimal funktionierende Android App
- Kotlin-basiert
- Material Design 3
- Automatischer APK Build via GitHub Actions

## Anforderungen

- Android SDK API Level 24+ (Android 7.0)
- Java 17+

## Lokale Entwicklung

1. Projekt in Android Studio öffnen
2. Gradle Sync durchführen
3. App auf Emulator oder Gerät ausführen

## APK Build via GitHub Actions

Bei jedem Push auf den Branch `claude/android-app-feasibility-mxcBT` wird automatisch eine APK gebaut.

### APK herunterladen:

1. Gehe zu **GitHub Actions** Tab im Repository
2. Wähle den neuesten erfolgreichen Workflow Run
3. Scrolle zu **Artifacts**
4. Lade `app-release` herunter

### APK auf Android-Gerät installieren:

**Methode 1: Direkter Download auf Handy**
1. APK auf dein Handy herunterladen (z.B. via Browser oder Cloud-Speicher)
2. Datei-Manager öffnen
3. APK-Datei antippen
4. Installation aus unbekannten Quellen erlauben (wenn gefragt)
5. Installation bestätigen

**Methode 2: Via ADB (Android Debug Bridge)**
```bash
# APK vom Artifact-ZIP entpacken
unzip app-release.zip

# Installation via ADB
adb install app-release-unsigned.apk
```

**Wichtig:** Da die APK unsigned ist, musst du eventuell "Apps aus unbekannten Quellen" in den Sicherheitseinstellungen aktivieren.

## Projektstruktur

```
MinimalApp/
├── app/
│   ├── src/main/
│   │   ├── java/com/example/minimalapp/
│   │   │   └── MainActivity.kt
│   │   ├── res/
│   │   │   ├── layout/
│   │   │   │   └── activity_main.xml
│   │   │   └── values/
│   │   │       └── strings.xml
│   │   └── AndroidManifest.xml
│   └── build.gradle.kts
├── build.gradle.kts
└── settings.gradle.kts
```

## Technologie-Stack

- **Sprache:** Kotlin
- **Minimum SDK:** API 24 (Android 7.0)
- **Target SDK:** API 34 (Android 14)
- **Build System:** Gradle 8.5
- **UI:** Material Design 3
