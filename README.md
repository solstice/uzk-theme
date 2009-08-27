UzK -- Ein Beamer-Theme fuer die Universitaet zu Koeln
======================================================

Allgemeines
-----------

Version 0.5

Die aktuellste Version finden Sie auf
[GitHub](http://solstice.github.com/uzk-theme).

Installation
------------

Das Theme besteht aus den folgenden Dateien:

- `README.md`
- `beamerthemeUzK.sty`
- `beamercolorthemeuzk.sty`
- `logo.pdf`
- `logo-small.pdf`
- `UzK-Example.tex` (lauffaehiges Beispiel)
- `UzK-Example.pdf` (PDF-Beispiel und aktuelle Anleitung fuer die
  verschiedenen Optionen von UzK)

Bitte beachten Sie die [Richtlinien zur Siegelverwendung](http://kommunikation-marketing.uni-koeln.de/marketing/corporate_design/siegelverwendung_logo_der_universitaet/index_ger.html)
der Universit‰t zu Koeln.

Um das Theme permanent zu installieren, legen Sie die Dateien im lokalen
texmf-Baum ab. Die Vorgehensweise haengt von der von Ihnen verwendeten
TeX-Distribution ab. Im naechsten Abschnitt werden kurz die notwendigen
Schritte bei Verwendung von MiKTeX dargestellt (Eine ausfuehrliche Anleitung
zur Verwendung eines lokalen texmf-Baumes finden Sie im
[MiKTeX-Manual](http://docs.miktex.org/manual/localadditions.html)).

Im Folgenden wird angenommen, dass Sie den lokalen texmf-Baum in `C:/texmf/`
anlegen wollen (diesen Pfad koennen Sie nach Belieben anpassen). Dazu
erstellen Sie zunaechst den Ordner

    C:/texmf/

Die Verzeichnisstruktur in diesem Ordner muss sich an die von TeX vorgebene
Verzeichnisstruktur halten (sie muss also TDS-konform sein, mehr dazu im oben
verlinkten MiKTeX-Manual). Darum ist im Ordner `C:/texmf/` der Ordner `tex`
und in diesem wiederum der Ordner `latex` zu erstellen. In diesen Ordner
(`C:/texmf/tex/latex/`) kopieren Sie den Ordner `uzk-theme`, der die oben
erwaehnten, vom UzK-Theme benoetigten Dateien enthaelt.

Nun muessen Sie MiKTeX mitteilen, dass es auch in diesem Ordner nach Dateien
suchen soll. Dazu oeffnen Sie die Einstellungen von MiKTeX ("Start -> Alle
Programme -> MiKTeX 2.7 -> Settings) und waehlen den Reiter "Roots". Klicken
Sie auf "Add" und waehlen Sie den Ordner `C:/texmf/` aus. Nach einem weiteren
Klick auf "OK" im "Settings"-Fenster erneuert MiKTeX die FNDB (FileName
DataBase) und Sie koennen das Theme fuer Ihre Beamer-Praesentationen
verwenden.

Unter UNIX-aehnlichen System (Linux, Mac OS) ist das Vorgehen analog: Sie
erstellen ebenfalls einen lokalen `texmf`-tree, in dem Sie den Ordner
`uzk-theme` ablegen. Am Mac koennen Sie ihren lokalen `texmf`-tree z.B. in
`~/Library/texmf/` anlegen. Den Pfad zu diesem Ordner tragen Sie in der Datei
`texmf.cnf` ein:

     TEXMFHOME = ~/Library/texmf

Die `texmf.cnf` liegt z.B. bei Verwendung von [MacTeX](https://www.tug.org/mactex/)
in `/usr/local/texlive/2008/`. Falls diese Datei dort noch nicht existiert, so
legen Sie diese einfach neu an.

Zuletzt muessen Sie den Befehl `sudo texhash` auf der Kommandozeile ausfuehren,
damit TeX von der Existenz des neuen Ordners erfaehrt.

Mitwirkende und Dank an:
------------------------

- Bernd Weiﬂ: Initiative und allgemeinen Code
- Jan Eden: Schriftart Fusszeile
- Martin Engler: Sprachauswahl ueber babel, Platzierung der
  Hintergrundgrafik, Schriftauswahl mit `setbeamerfont`
- Jonas Stein: Hilfe bei den Logos und Dateirechten
- Axel Berger: Option 'squares'
