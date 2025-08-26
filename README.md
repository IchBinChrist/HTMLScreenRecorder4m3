# HTMLScreenRecorder4m3 (HTML-only)

> A single-file, browser-based screen recorder for **desktop** browsers.  
> Captures **Entire Screen / Window / Tab** + **microphone**, mixes audio into **one** WebM file, offers a live preview, hotkeys, and a built-in language switcher. On mobile/unsupported browsers, a **full-screen notice** replaces the UI by design.

**Live demo:** <https://4m3.org/ScreenRecorder>

**Languages:** English, Deutsch, Français, Español (auto-detect with manual switcher).

---

## Table of Contents
- [Features](#features)
- [Quick Start](#quick-start)
- [Browser Support](#browser-support)
- [Notes & Limitations](#notes--limitations)
- [Troubleshooting](#troubleshooting)
- [Customization](#customization)
- [License](#license)
- [Deutsch 🇩🇪](#screenrecorder-html-only--deutsch)

## Features
- **One HTML file** – no build, no frameworks.
- **Screen/Window/Tab capture** via `getDisplayMedia`.
- **Audio mix**: tab/system audio + **microphone** (Web Audio API) → single track.
- **Language switcher** with auto-detect (**English, Deutsch, Français, Español**, fallback: English).
- **“Open page & record”** helper to open a URL in a new tab, then pick that tab.
- **Hotkeys**: `S` (Start/Stop), `P` (Pause/Resume).
- **Live preview** while recording; **WebM (VP8/VP9 + Opus)** output.
- **Mobile-safe**: on unsupported/mobile browsers a **full-screen notice** is shown (no recording UI).

## Quick Start
1. Download `ScreenRecorder.html`.
2. Serve it from a **secure origin** (HTTPS or `http://localhost`) so microphone access works.  
   Examples:
   ```bash
   # Python
   python -m http.server 8080
   # or Node
   npx serve
   ```
3. Open in a **desktop** browser (Chrome/Edge/Firefox/Safari).
4. Click **Start recording** → choose **Entire screen / Window / Tab**.  
   Enable **Share system audio** (screen/window) or **Share tab audio** (tab), if you need sound.
5. (Optional) Allow **microphone**; audio will be mixed in.
6. **Stop** → download the generated `.webm`.

## Browser Support
- **Desktop:** Recent Chrome/Edge/Firefox/Safari supported.  
- **Mobile:** Not supported by this page. A **full-screen message** is shown on mobile/unsupported browsers. Use the phone’s system recorder instead (Android Screen Recorder / iOS Control Center).

## Notes & Limitations
- **DRM/Protected content** may refuse capture or audio by platform policy.
- Use **headphones** to avoid echo/feedback when mixing tab/system audio with mic.
- Some platforms require explicitly toggling **“Share tab/system audio.”**
- `.webm` playback: Use a modern browser or a player like VLC. For MP4 you can convert offline, or integrate `ffmpeg.wasm` if you wish.

## Troubleshooting
- **No audio in the recording?** Ensure “Share tab/system audio” is enabled in the picker; check OS/browser capture settings.
- **Mic permission not shown?** Serve via HTTPS or `localhost`.
- **Popup blocked** when using “Open page & record”? Allow popups for the page.
- **Big files** at high FPS/resolution are normal; lower FPS if needed.

## Customization
- Add more languages by extending the i18n map in the `<script>` section.
- Preset FPS/resolution, add MP4 conversion (via `ffmpeg.wasm`), or UI tweaks as needed.

## License

This project is licensed under the **MIT License**.  

---

# HTMLScreenRecorder4m3 (HTML-only) – Deutsch

> Ein einzelnes HTML-Dokument als **Desktop-Screen-Recorder**.  
> Nimmt **Gesamten Bildschirm / Fenster / Tab** + **Mikrofon** auf, mischt den Ton in **eine** WebM-Datei, zeigt eine Live-Vorschau, Hotkeys und eine integrierte Sprachumschaltung. Auf mobilen/nicht unterstützten Browsern erscheint aus Sicherheitsgründen **nur ein Vollbild-Hinweis** (keine Aufnahme-UI).

**Live-Demo:** <https://4m3.org/ScreenRecorder>

**Sprachen:** Deutsch, English, Français, Español (Auto-Erkennung + manuelle Auswahl).

---

## Inhalt
- [Funktionen](#funktionen)
- [Schnellstart](#schnellstart)
- [Browser-Support](#browser-support-1)
- [Hinweise & Grenzen](#hinweise--grenzen)
- [Fehlerbehebung](#fehlerbehebung)
- [Anpassen](#anpassen)
- [Lizenz](#lizenz)

## Funktionen
- **Nur eine HTML-Datei** – kein Build, keine Frameworks.
- **Bildschirm/Fenster/Tab** per `getDisplayMedia`.
- **Audiomix**: Tab-/System-Audio + **Mikrofon** (Web Audio API) → ein Track.
- **Sprachauswahl** mit Auto-Erkennung (**Deutsch, English, Français, Español**, Fallback: Englisch).
- **„Webseite öffnen & aufnehmen“**: URL in neuem Tab öffnen und diesen im Picker auswählen.
- **Hotkeys**: `S` (Start/Stopp), `P` (Pause/Fortsetzen).
- **Live-Vorschau**; Ausgabe als **WebM (VP8/VP9 + Opus)**.
- **Mobil-Sicherheit**: Auf mobilen/nicht unterstützten Browsern wird **ausschließlich eine Vollbild-Meldung** angezeigt (keine UI).

## Schnellstart
1. `ScreenRecorder.html` herunterladen.
2. Über einen **sicheren Ursprung** bereitstellen (HTTPS oder `http://localhost`), damit Mikrofonzugriff funktioniert.  
   Beispiele:
   ```bash
   # Python
   python -m http.server 8080
   # oder Node
   npx serve
   ```
3. In einem **Desktop-Browser** öffnen (Chrome/Edge/Firefox/Safari).
4. **Aufnahme starten** → **Gesamter Bildschirm / Fenster / Tab** wählen.  
   Für Ton **„Systemaudio teilen“** (Bildschirm/Fenster) bzw. **„Tab-Audio teilen“** (Tab) aktivieren.
5. (Optional) **Mikrofon** erlauben; der Ton wird dazugemischt.
6. **Stoppen** → `.webm` herunterladen.

## Browser-Support
- **Desktop:** Aktuelle Versionen von Chrome/Edge/Firefox/Safari.  
- **Mobil:** Von dieser Seite **nicht** unterstützt. Es erscheint eine **Vollbild-Meldung**. Nutze stattdessen den System-Screen-Recorder (Android) bzw. die Bildschirmaufnahme im Kontrollzentrum (iOS).

## Hinweise & Grenzen
- **DRM/geschützte Inhalte** können Aufnahme/Ton blockieren.
- **Kopfhörer** nutzen, um Echo/Feedback zu vermeiden.
- In manchen Dialogen muss **„Tab-/Systemaudio teilen“** aktiv gesetzt werden.
- `.webm` abspielen: moderner Browser oder VLC. Für MP4 konvertieren (offline) oder `ffmpeg.wasm` integrieren.

## Fehlerbehebung
- **Kein Ton?** „Tab-/Systemaudio teilen“ im Picker aktivieren; OS/Browser-Einstellungen prüfen.
- **Mikro nicht verfügbar?** Über **HTTPS** oder `localhost` öffnen.
- **Popup blockiert** bei „Webseite öffnen & aufnehmen“? Popups erlauben.
- **Große Dateien** bei hoher Auflösung/FPS sind normal; ggf. FPS senken.

## Anpassen
- Weitere Sprachen im i18n-Objekt ergänzen.
- FPS/Res-Presets oder MP4-Export (z. B. `ffmpeg.wasm`) hinzufügen; UI nach Bedarf anpassen.

## Lizenz
## License / Lizenz

Dieses Projekt steht unter der **MIT-Lizenz**.  
