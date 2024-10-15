# Anleitung: Arbeiten mit GitHub Desktop, VS Code, git, wget und curl (Windows)

## Einleitung
In dieser Anleitung zeige ich dir, wie du GitHub Desktop, VS Code, git, wget und curl unter Windows verwendest, um deine Projekte mit GitHub zu verwalten. Egal, ob du ein Anfänger oder ein fortgeschrittener Nutzer bist, diese Schritte helfen dir, deine Arbeit effizienter zu gestalten.

> Hinweis: Dieser Code wurde mithilfe einer KI erstellt. Der Ersteller ist kein professioneller Programmierer und der Code kann unfertig oder fehlerhaft sein sowie logische Lücken aufweisen.

---

## 1. Installation von GitHub Desktop

GitHub Desktop ist ein einfach zu benutzendes Tool, um deine Git-Repositories lokal zu verwalten und mit GitHub zu synchronisieren.

### Schritte:
1. [Lade GitHub Desktop herunter](https://desktop.github.com/).
2. Installiere die Software und melde dich mit deinem GitHub-Account an.
3. Klicke auf „Clone a repository from the internet“, um ein bestehendes Repository herunterzuladen, oder erstelle ein neues.
4. Du kannst „Commit“ verwenden, um Änderungen lokal zu speichern, und „Push“, um deine Änderungen auf GitHub hochzuladen.

## 2. Arbeiten mit VS Code

Visual Studio Code (VS Code) bietet eine nahtlose Integration von Git. Hier erfährst du, wie du deine Projekte in VS Code verwaltest.

### Schritte:
1. [Lade VS Code herunter](https://code.visualstudio.com/Download) und installiere es.
2. In VS Code kannst du die Erweiterung "GitHub" oder "GitLens" installieren, um eine bessere Integration zu erhalten.
3. Öffne das Terminal in VS Code mit `Strg + Ö`.
4. Nutze folgende Befehle, um ein Repository zu klonen:
   ```sh
   git clone https://github.com/dein-username/dein-repository.git
   ```
5. Du kannst alle Git-Befehle direkt aus dem integrierten Terminal in VS Code ausführen, zum Beispiel `git status`, `git add`, `git commit` oder `git push`.

## 3. Arbeiten mit Git (Befehlszeile)

Falls du lieber mit der Befehlszeile arbeitest, kannst du auch die Git-CLI verwenden.

### Schritte:
1. [Lade Git für Windows herunter](https://gitforwindows.org/) und installiere es.
2. Öffne die Git Bash oder die Eingabeaufforderung.
3. Um ein Repository zu klonen, gib folgenden Befehl ein:
   ```sh
   git clone https://github.com/dein-username/dein-repository.git
   ```
4. Verwende `git add`, `git commit` und `git push`, um deine Änderungen hochzuladen.

## 4. Arbeiten mit wget und curl

`wget` und `curl` sind praktische Tools, um Daten direkt von der Befehlszeile herunterzuladen.

### Schritte für wget:
1. [Lade wget für Windows herunter](https://eternallybored.org/misc/wget/) und installiere es.
2. Verwende folgenden Befehl, um ein GitHub-Repository als ZIP-Datei herunterzuladen:
   ```sh
   wget https://github.com/dein-username/dein-repository/archive/refs/heads/main.zip
   ```

### Schritte für curl:
1. `curl` ist in den neuesten Windows-Versionen integriert. Verwende den folgenden Befehl, um eine Datei herunterzuladen:
   ```sh
   curl -L -o repo.zip https://github.com/dein-username/dein-repository/archive/refs/heads/main.zip
   ```

## 5. Verwenden von .gitignore

Die Datei `.gitignore` ist nützlich, um bestimmte Dateien oder Ordner vom Versionskontrollsystem auszuschließen. Das hilft, sensible Daten oder unnötige Dateien nicht in das Repository hochzuladen.

### Schritte:
1. Erstelle eine Datei mit dem Namen `.gitignore` im Hauptverzeichnis deines Projekts.
2. Füge die Dateinamen oder Ordner hinzu, die du ignorieren möchtest, zum Beispiel:
   ```
   # Log-Dateien
   *.log

   # Verzeichnisse für temporäre Daten
   /tmp/

   # Betriebssystemspezifische Dateien
   Thumbs.db
   Desktop.ini
   ```
3. Sobald die `.gitignore`-Datei erstellt ist, werden die darin aufgeführten Dateien und Verzeichnisse von Git ignoriert und nicht ins Repository aufgenommen.

## 6. Verwenden von .gitattributes

Die Datei `.gitattributes` wird verwendet, um Einstellungen für die Verwaltung von Dateiattributen im Repository festzulegen. Damit kannst du beispielsweise die Behandlung von Zeilenendungen steuern, die Sprache für Syntax-Hervorhebungen festlegen oder bestimmte Dateien für die Filterung konfigurieren.

### Schritte:
1. Erstelle eine Datei mit dem Namen `.gitattributes` im Hauptverzeichnis deines Projekts.
2. Füge Regeln hinzu, um das Verhalten von Dateien zu definieren, zum Beispiel:
   ```
   # Setze die Zeilenendungen für alle Textdateien auf LF
   * text=auto

   # Bestimme den diff-Filter für bestimmte Dateitypen
   *.md diff

   # Überspringe die Verarbeitung für große Binärdateien
   *.png binary
   ```
3. Die `.gitattributes`-Datei hilft dabei, Inkonsistenzen in der Versionskontrolle zu vermeiden und sorgt für einheitliche Einstellungen über verschiedene Systeme hinweg.

## Zusammenfassung
- Nutze **GitHub Desktop** für eine benutzerfreundliche Bedienung.
- **VS Code** bietet eine nahtlose Git-Integration.
- Mit **Git** in der Befehlszeile hast du die größte Kontrolle.
- **wget** und **curl** helfen dir, Dateien schnell herunterzuladen.
- Verwende eine **.gitignore**-Datei, um unnötige oder sensible Dateien aus deinem Repository auszuschließen.
- Verwende eine **.gitattributes**-Datei, um Dateiattribute und das Verhalten der Versionskontrolle festzulegen.

Egal, welchen Weg du wählst, diese Tools helfen dir, deine Projekte effizient zu verwalten und mit GitHub zu synchronisieren.
