# Raumschiffe

Ein kleines JavaScript-Projekt, das die Entfernung von zwei Raumschiffen von der Erde verfolgt.

## Beschreibung

Dieses Projekt erstellt zwei Raumschiffe, die jeweils eine Methode haben, um ihre Entfernung von der Erde in Lichtjahren zu berechnen und auszugeben. Die Raumschiffe starten von der Erde und die Entfernungen ändern sich basierend auf den angegebenen Lichtjahren.

## Dateien

- `index.html`: Enthält das HTML und JavaScript für das Projekt.

## Verwendung

1. Klonen Sie das Repository:
    ```bash
    git clone https://github.com/BitSparkCode/Raumschiffe.git
    ```
2. Navigieren Sie in das Verzeichnis:
    ```bash
    cd raumschiffe
    ```
3. Öffnen Sie die Datei `index.html` in einem Webbrowser, um das Projekt auszuführen.

## Beispielcode

```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <title>Raumschiffe</title>
</head>
<body>
    <h3>Und es bewegt sich doch</h3>
    <script type="text/javascript">
        function Raumschiff(name, modell) {
            this.name = name;
            this.modell = modell;
            this.entfernung = 0;
            this.entfernen = function (lichtjahre) {
                this.entfernung += lichtjahre;
                document.write(this.name + " => Aktuelle Reise: " +
                    lichtjahre + " Lichtjahre -> Erdentfernung: " +
                    this.entfernung + " Lichtjahre<br />");
            }
        }

        var enterprise = new Raumschiff("U.S.S. Enterprise", "NCC-1701");
        var voyager = new Raumschiff("U.S.S. Voyager", "NCC-74656");

        document.write("<p>Beide Raumschiffe sind von der Erde gestartet:<br /></p>");

        enterprise.entfernen(50);
        voyager.entfernen(180);
        enterprise.entfernen(200);
        voyager.entfernen(-50);
        enterprise.entfernen(-100);
        enterprise.entfernen(-150);
        voyager.entfernen(40);
        voyager.entfernen(-120);
    </script>
</body>
</html>
```
