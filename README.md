# Enigma 3

<div align="center">

**Die App zum selbst gehosteten SecureChat-Server.**

Ende-zu-Ende verschlüsselte Nachrichten, Anrufe und geteilte Räume —
auf deinem eigenen Server, nicht bei einem Konzern.

![Version](https://img.shields.io/badge/version-1.3.15-1f6feb?style=for-the-badge&logo=github&logoColor=white)
![Plattform](https://img.shields.io/badge/plattform-Windows%20·%20Linux%20·%20Android-303030?style=for-the-badge)
![E2EE](https://img.shields.io/badge/ende--zu--ende-AES--256--GCM-1a7f37?style=for-the-badge&logo=lock&logoColor=white)
![Build](https://img.shields.io/badge/build-quelloffen-6f42c1?style=for-the-badge&logo=git&logoColor=white)

[**⬇️ Herunterladen**](../../releases/latest)

</div>

---

## 📦 Downloads

Jede Version enthält alle Plattformen im selben Stand.

| Plattform | Datei | Hinweis |
| --- | --- | --- |
| 🪟 Windows 10/11 x64 | `Enigma-3-Setup-<Version>.exe` | NSIS-Installer, unsigniert (SmartScreen-Hinweis) |
| 🐧 Linux x86_64 | `Enigma-3-<Version>-x86_64.AppImage` | Einmal `chmod +x`, dann starten |
| 🐧 Linux arm64 | `Enigma-3-<Version>-arm64.AppImage` | Einmal `chmod +x`, dann starten |
| 🤖 Android 7+ | `enigma3-<Version>.apk` | Signierte Release-APK (`CN=Enigma 3`) |
| 🔐 Alle | `SHA256SUMS.txt` | Prüfsummen aller Dateien |

**Aktuell:** [Enigma 3 – 1.3.15](../../releases/tag/v1.3.15)

**Neu in 1.3.15:** Die Systemseite des Servers zeigt mehr Betrieb:
Laufzeit, aktive Sitzungen, Ereignis-Takt und freier Speicher auf dem
Datendatenträger. Die LiveKit-Diagnose listet aktive Räume, der IP-Wächter
meldet seinen Status. Anhänge sichern ihre Bildmaße jetzt verschlüsselt.


**1.3.9 nicht aktualisieren:** Deren Desktop-Pakete enthielten ein veraltetes
Frontend. Direkt auf 1.3.15 wechseln.

## 🚀 In drei Schritten loslegen

1. **Server.** Du brauchst einen laufenden SecureChat-Server mit HTTPS.
2. **App installieren.** Windows-Datei ausführen: sie ersetzt eine bestehende
   Version und behält alle Daten. AppImage einmal `chmod +x` machen. APK über
   „Unbekannte Quellen" installieren. Eine vorhandene Debug-APK vorher
   deinstallieren, denn der Release-Schlüssel ist ein anderer.
3. **Verbinden.** Beim ersten Start die Adresse deines Servers eintragen. Die
   Anmeldung öffnet den Systembrowser.

## 🔍 Integrität prüfen

Alle Dateien haben eine SHA-256-Prüfsumme in `SHA256SUMS.txt`:

```sh
sha256sum -c SHA256SUMS.txt
```

Die Desktop-App prüft Update-Hinweise automatisch gegen diese Prüfsumme. Ohne
Prüfsumme bietet die App kein Update an.

## 🛡️ Was die App schützt

| | |
| --- | --- |
| 🔒 **Ende-zu-Ende** | Dein Gerät verschlüsselt die Nachricht, bevor sie das Gerät verlässt. Der Server speichert und überträgt, was er nicht lesen kann. |
| 🔁 **Vorwärtsgeheimheit** | Jede Nachricht hat einen eigenen Schlüssel. Ein verlorener Schlüssel legt deine Vergangenheit nicht offen. |
| 📱 **Gerätesperre** | Biometrie oder PIN versiegeln die Schlüssel im lokalen Tresor (Argon2id). Android nutzt Keystore, Windows DPAPI. |
| ⏳ **Selbstlöschung** | Du bestimmst, wie lange deine Nachrichten bleiben. |

## ⚠️ Hinweise zur Sicherheit

- Die Windows-Installer sind **unsigniert**. SmartScreen zeigt deshalb einen
  Hinweis. Bestätige ihn nur, wenn diese Seite die Quelle ist.
- Updates kommen ausschließlich aus diesem Repository. Kein Hintergrund-Download:
  Die App zeigt höchstens einmal täglich einen Hinweis, und erst nach deinem
  Klick wird heruntergeladen.
- Die iPhone-App wird nicht mehr auf Geräten verteilt. iPhone-Nutzer verwenden
  die Web-App im Safari.

## 🕷️ Ältere Versionen

Nur die aktuelle Version wird verteilt.

## 💬 Kontakt

Fragen, Fehler und Sicherheitshinweise:
[**GitHub Issues**](../../issues)
