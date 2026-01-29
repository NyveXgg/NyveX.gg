# 📢 Simple Voice Chat – Vollständige Anleitung

**Simple Voice Chat** ist eine Mod/Plugin für Minecraft, die echten **Voice Chat direkt im Spiel ermöglicht**, inklusive **Proximity Chat**, **Gruppen‑Chat**, **Push‑to‑Talk**, **Voice‑Aktivierung** und vielen weiteren Funktionen. :contentReference[oaicite:1]{index=1}

🔗 **Offizielle Wiki & Ressourcen**
- 🌐 **Wiki:** https://modrinth.com/plugin/simple-voice-chat/wiki :contentReference[oaicite:2]{index=2}
- ⚙️ **Mod/Plugin Downloadseite:**  
  - CurseForge: https://curseforge.com/minecraft/mc-mods/simple-voice-chat :contentReference[oaicite:3]{index=3}  
  - Modrinth: https://modrinth.com/plugin/simple-voice-chat :contentReference[oaicite:4]{index=4}

---

## 📥 1. Download

Simple Voice Chat bietet **verschiedene Versionen** zum Download:
- **Fabric Mod**
- **Forge Mod**
- **NeoForge**
- **Quilt**
- **Bukkit/Spigot/Paper Plugin**
- **Velocity / BungeeCord / Waterfall Proxy** :contentReference[oaicite:5]{index=5}

📌 Du kannst alle Versionen über die oben verlinkten Seiten herunterladen. Stelle sicher, dass du die Version auswählst, die zu deinem Minecraft‑Setup passt.

---

## 🛠️ 2. Installation

### 🔹 Server‑Installation

1. Lade die gewünschte Version herunter (Mod oder Plugin).  
2. **Für Server mit Mods:**  
   - Verschiebe die `.jar` Datei in den **mods/** Ordner deines Servers.
3. **Für Server mit Plugin‑Support (Paper/Spigot/Purpur):**  
   - Verschiebe die `.jar` Datei in den **plugins/** Ordner.
4. Starte den Server neu, damit die Mod/Plugin aktiviert wird. :contentReference[oaicite:6]{index=6}

💡 Für Proxy‑Netzwerke nutze die entsprechenden Proxy‑Versionen im `plugins/`‑Ordner.

---

### 🔹 Client‑Installation

1. Stelle sicher, dass dein Client das gleiche **Loader‑System** nutzt (Fabric/Forge/Quilt).  
2. Lege die **Client‑Mod‑Jar** in den **mods/**‑Ordner deines Minecraft‑Installationsverzeichnisses.  
3. Starte Minecraft mit dem gewählten Profil. :contentReference[oaicite:7]{index=7}

✔ **Wichtig:** Ohne installierte Client‑Mod kann der Spieler zwar dem Server beitreten, aber **kein Voice‑Chat nutzen**. :contentReference[oaicite:8]{index=8}

---

## ⚙️ 3. Konfiguration

Nach der ersten Ausführung erstellt Simple Voice Chat Konfigurationsdateien unter:

- **Server Mod:** `config/voicechat-server.properties`
- **Server Plugin:** `plugins/voicechat/voicechat-server.properties` (abhängig vom Setup)
- **Client:** Ähnliche Files im Client‑Ordner unter `voicechat/` :contentReference[oaicite:9]{index=9}

### 🔹 Wichtige Einstellungen

| Option | Beschreibung |
|--------|--------------|
| `port=` | UDP‑Port, über den der Voice Chat läuft (Standard: 24454) |
| `voiceDistance=` | Reichweite des Sprachchats in Blöcken |
| `voiceChatEnabled=` | true/false → Voice Chat aktivieren oder deaktivieren |
| Audio‑Buffers, Encryption‑Optionen | Feinabstimmung der Audioqualität |

📌 **Port öffnen**  
Damit Voice Chat funktioniert, musst du den konfigurierten UDP‑Port extern erreichbar machen (z. B. Port‑Freigabe im Router/Firewall). :contentReference[oaicite:10]{index=10}

---

## 🎤 4. Nutzung im Spiel

### 🎛️ Voice Chat Menü

- Drücke **V**, um die Voice‑Chat GUI zu öffnen.  
  Dort kannst du:
  - Mikrofon ein/aus schalten
  - Push‑to‑Talk oder Voice‑Activation wählen
  - Gruppenchats verwalten
  - Lautstärke und Mikrofon‑Test starten :contentReference[oaicite:11]{index=11}

---

## 🗣️ 5. Gruppen und Chat‑Features

- **Gruppen erstellen:**  
  Öffne die Gruppen‑Ansicht in der Voice‑GUI oder verwende `/voicechat invite <spielername>` um jemanden einzuladen. :contentReference[oaicite:12]{index=12}
- **Icons:**  
  Spieler in Gruppen, sprechender Status, whispering, muted etc. werden durch Icons angezeigt. :contentReference[oaicite:13]{index=13}

---

## 🔑 6. Keybindings

| Aktion                     | Standard Taste |
|---------------------------|----------------|
| Öffne Voice Chat GUI      | `V` |
| Push‑to‑Talk / Sprechen   | konfigurierbar (Standard oft **CapsLock**) |
| Stummschalten (Mute)      | konfigurierbar |
| Gruppen‑GUI öffnen        | `G` |

🎛️ Diese Werte sind im Menü anpassbar und können je nach Version variieren. :contentReference[oaicite:14]{index=14}

---

## ⚠️ 7. Häufige Probleme & Tipps

### ❌ „Voice chat not connected“

Dies kann passieren, wenn:
- Der UDP‑Port nicht geöffnet wurde.
- Der Server nicht erreichbar ist.
- Firewall/Netzwerk blockiert UDP‑Traffic. :contentReference[oaicite:15]{index=15}

### 🎤 Mikrofon funktioniert nicht

- Überprüfe, ob Minecraft **Berechtigungen für Mikrofonzugriff** im Betriebssystem hat.
- Kontrolliere die Mod‑GUI, ob Mikrofon aktiviert ist. :contentReference[oaicite:16]{index=16}

---

## 🧠 Kompatibilität

- **Client ↔ Server:** Versionen sollten nah beieinander sein.
- **Mod ↔ Plugin:** Bei Proxy‑Netzwerken müssen alle Komponenten installiert werden.
- **Different Loaders:** Simple Voice Chat unterstützt Fabric, Forge, NeoForge, Quilt, Bukkit/Spigot/Paper usw. :contentReference[oaicite:17]{index=17}

---

## 📌 Zusammenfassung

Simple Voice Chat ermöglicht:
- **Proximity Voice Chat**
- **Gruppen‑Chat**
- **Push‑to‑Talk & Voice‑Activation**
- **GUI‑Anpassung & Audio‑Einstellungen** :contentReference[oaicite:18]{index=18}

Du benötigst sowohl:
- **Client‑Mod**
- **Server‑Mod/Plugin**
- **offene UDP‑Ports** für korrekte Funktion.

📍 Für detaillierte Infos, Konfig‑Erklärungen und Updates sieh dir unbedingt das **offizielle Wiki** an:  
➡️ https://modrinth.com/plugin/simple-voice-chat/wiki :contentReference[oaicite:19]{index=19}
