# Simple Voice Chat – Client-Mod (Nur Client-Seite)

Diese Dokumentation beschreibt ausschließlich die **Client-Seite** der Simple Voice Chat Mod. Sie enthält Installation, Speicherorte, Konfigurationsoptionen, GUI-Settings, Keybinds, Audio-Optionen, Performance-Tipps, Troubleshooting, Datenschutz und Minimal-Beispiel-Konfigurationen. 

---

## 1. Installation (Client)

1. Lade die **Client-Mod** für deinen Loader (Fabric / Forge / Quilt / NeoForge) herunter.  
2. Öffne dein Minecraft-Installationsverzeichnis (z. B. `%appdata%/.minecraft` auf Windows).  
3. Lege die heruntergeladene `.jar` in den Ordner `mods/`.  
4. Starte Minecraft mit dem passenden Profil (dasselbe Loader-System wie die Mod verwendet).  
5. Nach dem ersten Start erzeugt die Mod automatisch ihre Konfigurationsdateien.

---

## 2. Speicherorte der Client-Konfiguration

- Windows: `%appdata%/.minecraft/mods/voicechat` oder `%appdata%/.minecraft/config/voicechat*`  
- Linux: `~/.minecraft/mods/voicechat` oder `~/.config/...`  
- Innerhalb der Minecraft-Instanz:  
  - `config/voicechat-client.properties`  
  - `mods/voicechat/config/` (je nach Modloader-Version)

> Hinweis: Die genauen Pfade können je nach Launcher und Modloader leicht variieren. Suche nach `voicechat` im Minecraft-Ordner, falls die Datei nicht sofort sichtbar ist.

---

## 3. Wichtige Client-Konfigurationsoptionen (`voicechat-client.properties`)

pushToTalk=false # true = Push-to-Talk, false = Voice Activity
pushToTalkKey=86 # Keycode (86 = V), kann auch String sein
voiceDistance=16 # Reichweite in Blöcken (Proximity)
microphoneSensitivity=0.5 # Mikrofon Empfindlichkeit (0.0 - 1.0)
maxVolume=1.0 # Max Lautstärke (0.0 - 1.0)
minVolume=0.0 # Min Lautstärke
muteAll=false # alle Stimmen stummschalten
groupVolume=1.0 # Lautstärke für Gruppenmitglieder
enableNoiseSuppression=true # Rauschunterdrückung
audioBufferSize=1024 # Audio-Puffergröße (Latenz vs. Stabilität)
preferredCodec=opus # Codec: opus/pcm/...
enableEncryption=true # Verschlüsselung aktivieren
debugLogging=false # Debugging aktivieren

### Erklärung der wichtigsten Optionen

- `pushToTalk` / `pushToTalkKey`: Push-to-Talk aktivieren und Taste festlegen. Bei `false` wird Voice Activity genutzt.  
- `voiceDistance`: Radius, in dem andere Spieler deine Stimme hören können.  
- `microphoneSensitivity`: Empfindlichkeit des Mikrofons, 0.0 = sehr unempfindlich, 1.0 = sehr empfindlich.  
- `audioBufferSize`: Kleinere Werte = geringere Latenz, größere Werte = stabilere Übertragung bei schwachem Netzwerk.  
- `preferredCodec`: Bevorzugter Codec (Opus empfohlen für beste Qualität).  
- `enableEncryption`: Verschlüsselt die Audio-Übertragung.  
- `debugLogging`: Aktiviert ausführliche Logausgabe für Fehlersuche.

---

## 4. GUI & In-Game Einstellungen

- **Push-to-Talk Taste** setzen (Keybind-Menü)  
- **Voice Mode**: Push-to-Talk / Voice Activity  
- **Mikrofon-Test / Pegelanzeige**  
- **Volume Slider**: Gesamtlautstärke und Spielerlautstärke individuell  
- **Voice Distance**: Hörreichweite anpassen  
- **Group Management**: Gruppen erstellen/verlassen, Spieler einladen  
- **Mute / Unmute**: Spieler gezielt stummschalten  
- **Advanced Settings**: Audio-Puffer, Codec, Rauschunterdrückung (je nach Version)

---

## 5. Keybinds

- **Open Voice Menu**: Standard `V`  
- **Push-to-Talk**: Konfigurierbar, z. B. `V` / `CapsLock`  
- **Toggle Mute**: Optionaler Keybind

> Alle Keybinds können über die Minecraft-Steuerung oder direkt in der `voicechat-client.properties` angepasst werden.

---

## 6. Audio & Peripherie

- Minecraft benötigt Mikrofonzugriff vom Betriebssystem.  
- Standardmäßig wird das Systemmikrofon verwendet, in manchen Versionen wählbar über GUI.  
- Rauschunterdrückung und Echo-Cancellation optional aktivierbar.  
- Headset empfohlen, um Echo/Feedback zu vermeiden.

---

## 7. Performance-Tipps

- `audioBufferSize` erhöhen, wenn Audio stottert.  
- `preferredCodec=opus` nutzen für beste Qualität.  
- Bei hoher CPU-Last `enableNoiseSuppression` deaktivieren.

---

## 8. Logs & Debugging

- Standard-Logs: `logs/latest.log` im Minecraft-Ordner.  
- `debugLogging=true` erzeugt zusätzliche `voicechat` Logeinträge.  
- Typische Fehler:  
  - „Unable to bind audio device“ → Zugriff/Treiberproblem  
  - „Couldn't connect to voice server“ → UDP Port blockiert oder inkompatible Serverversion

---

## 9. Häufige Probleme & Lösungen

- **Kein Mikrofon-Input**: OS-Mikrofonrechte prüfen, GUI-Mic aktivieren, Sensitivity prüfen  
- **Andere hören mich nicht**: Push-to-Talk aktiviert? Keybind korrekt? voiceDistance? Firewall/Port prüfen  
- **Ich höre andere nicht**: muteAll, individuelle Mutes, Volume-Slider prüfen  
- **Stottern / Aussetzer**: audioBufferSize erhöhen, Codec prüfen, Netzwerk stabilisieren  
- **Echo / Feedback**: Headset nutzen, Lautstärke reduzieren

---

## 10. Datenschutz & Sicherheit

- `enableEncryption=true` empfohlen  
- Stimme wird über UDP gesendet → nur vertrauenswürdige Server  
- Logs können Audio-Metadaten enthalten → beim Teilen beachten

---

## 11. Beispiel Minimal-Konfiguration

pushToTalk=true
pushToTalkKey=86
voiceDistance=16
microphoneSensitivity=0.6
enableNoiseSuppression=true
audioBufferSize=1024
preferredCodec=opus
enableEncryption=true
debugLogging=false


> Änderungen speichern und Minecraft neu starten, damit sie wirksam werden.

---

## 12. Update & Kompatibilität

- Halte die Client-Mod aktuell (CurseForge / Modrinth)  
- Kleine Versionsunterschiede zum Server sind oft kompatibel, aber volle Funktionalität nur mit kompatibler Version  
- Client-Mod zwingend erforderlich, sonst kein Voice Chat

---

## 13. Weiterführende Links

- CurseForge: https://www.curseforge.com/minecraft/bukkit-plugins/simple-voice-chat  
- Modrinth: https://modrinth.com/plugin/simple-voice-chat  
- Offizielles Wiki / FAQ: siehe Mod-Seiten
