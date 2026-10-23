# Turbo Garage (Fabric, Minecraft 1.21.11)

Autos und Motorräder zum Fahren und Tunen.

## Was die Mod kann
- 4 Autos: **Rosso GT**, **Corsa Turbo**, **Roadking SUV**, **City Mini** + 1 Motorrad: **Speed Bike**
- **Tuning-Tisch**: Rechtsklick öffnet das Menü. Fahrzeug muss max. 8 Blöcke entfernt sein.
  - Lackfarbe (16 Farben), Felgenfarbe (16 Farben), Spoiler an/aus
  - Motor (Stufe 1–3: mehr Tempo und Beschleunigung), Reifen (Stufe 1–3: besser lenken), Nitro (mehr Tempo)
  - Kosten (außer im Kreativmodus): Spoiler 4 Eisen, Motor 5/10/15 Eisen, Reifen 4/8/12 Kohle, Nitro 3 Diamanten
- Fahren: Rechtsklick aufs Fahrzeug, dann W/A/S/D. Aussteigen mit Shift.
- Fahrzeug aufnehmen: Shift + Schlag.
- Alle Fahrzeuge und der Tisch sind im Kreativmenü unter "Werkzeuge & Hilfsmittel" und craftbar.

## Bauen (wichtig: Gradle-Wrapper fehlt, siehe Schritt 1)
1. Auf https://fabricmc.net/develop/template/ ein Projekt für **Minecraft 1.21.11** erzeugen (Mojang-Mappings wählen).
   Daraus die Ordner `gradle/` sowie `gradlew` und `gradlew.bat` in diesen Projektordner kopieren.
   Dort stehen auch die aktuellen Versionen für `gradle.properties` (Loader, Loom, Fabric API).
2. Java 21 installieren, Ordner in IntelliJ IDEA öffnen (oder im Terminal `./gradlew build`).
3. Die fertige Mod liegt danach unter `build/libs/turbogarage-1.0.0.jar` (nimm die Datei OHNE `-sources`).
4. Zum Testen die .jar plus Fabric API in den `mods`-Ordner legen.

## Texturen austauschen
`python3 tools/gen_textures.py` erzeugt einfarbige Platzhalter. Eigene Texturen einfach in
`src/main/resources/assets/turbogarage/textures/` überschreiben.
- `entity/vehicle.png` ist ein Farb-Atlas (jede Farbe eine Zone), Aufbau siehe `CarModel.java`.

## Hinweise zu Modrinth
- In `fabric.mod.json` bei `authors` deinen Namen eintragen.
- Keine Markennamen (z. B. Ferrari) verwenden, das kann zur Entfernung führen.
- Für die Projektseite ein Icon (PNG) und Screenshots vorbereiten.
