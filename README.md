# Phonedialer – Firmware

Fertige, **signierte** Firmware für den Phonedialer (ESP8266): zwei Tasten
wählen über die Wählhilfe der FRITZ!Box.

Der Quelltext liegt in einem privaten Repository. Hier liegen nur die
veröffentlichten Firmware-Stände. Die Geräte holen sich Updates von hier.

| Datei | Inhalt |
|---|---|
| `version.json` | neueste Version und Pfad zur Datei. Die Geräte lesen sie für die Update-Prüfung |
| `firmware/phonedialer-<version>.bin` | signierte Firmware |
| `firmware/notes-<version>.md` | Änderungen dieser Version |

Zu jeder Version gibt es außerdem ein GitHub-Release mit derselben Datei.

## Aufspielen

- **Über die Webseite des Geräts:** Reiter *System* → *Firmware-Update*.
  Entweder „Jetzt installieren“ oder eine heruntergeladene `.bin` hochladen.
- **Per USB:** `esptool --port <port> write-flash 0x0 phonedialer-<version>.bin`

Das Gerät nimmt über die Webseite nur Firmware an, die mit dem Schlüssel des
Projekts signiert ist. Per USB lässt sich jede Firmware aufspielen.

Dieses Repository wird automatisch gepflegt. Bitte nichts von Hand ändern.
