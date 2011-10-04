Warnung: Du verwendest diese Programm auf eigene Gefahr hin!
1) Wenn das Programm abst�rzt wird du wahrscheinlich keinen Support
    vom Spielehersteller bekommen. Aber du kannst den Fehler gerne
    angeben unter  http://code.google.com/p/texmod/issues/list
2) Spiele k�nnen detektieren ob sie ver�ndert werde, daher riskierst du
    einen Bann deines online Accounts.
3) Dies ist eine open-source Projekt. Der Code kann von jedem erhalten, ver�ndert
    und kompiliert werden. Lade OpenTexMod nur von offiziellen Quellen runter,
    denen du vertraust. Lade es selbst runter und verwende keine Versionen
    die du von Team- oder Gildenmitgliedern geschickt bekommen hast.
    http://code.google.com/p/texmod/downloads/list

   
OpenTexMod verwendet die D3DX9_43.dll. Wegen den EULA kann diese dll nicht mit OpenTexMod
mit geliefert werden. Wenn diese dll auf deinem System nicht installiert ist, wird dich OpenTexMod
darauf hinweisen.


Was kann OpenTexMod alpha V0.9?

-einzelne Texturen aus einem Spiel extrahieren und speichern (Die Zieltextur kann im Spiel ge�ndert werden)
-alle Texturen aus einem Spiel extrahieren und speichern
-Texturen in ein Spiel laden und Zieltexturen ersetzen
-Support von zip-Dateien
-Support der originalen TexMod *.tpf Datein

Alle diese Optionen k�nnen w�hrend des Spieles an und aus geschaltet werden!
Du kannst also nach einer Textur suchen, diese speichern, sie anschlie�end
editieren, sie in das Spiel laden, sie nach bearbeiten und wieder in das
Spiel laden, ...
und das alles ohne das Spiel neu starten zu m�ssen.

Randbemerkung: Wenn alle Texturen gespeichert werden sollen, so geschieht das nur,
wenn die Texturen vom Spiel geladen werden und auch nur in dem Moment, wenn sie
geladen werden. Stellst du diese Option an, w�hrend die Map bereits geladen ist, wird
wahrscheinlich nichts geschehen, da alle Texturen f�r diese Map bereits geladen sind.
Wechsle also die Map oder lade erneut.

Zip Dateien k�nnen eine "texmod.def" Datei enthalten, welche die Hash-Werte und
Dateinamen enth�lt. Jede Zeile sollte dem Format "hash|filename.dds" entsprechen.
Wenn es keine "texmod.def" Datei enth�lt, wird jede Datei entpackt und jene, deren 
Namen auf das Wildcard  "*_hash.dds" zutrifft, werden benutzt.
Die Zip Datei kann eine "Comment.txt" enthalten. Der Inhalte wird als Kommentar
in der GUI angezeigt.

Wenn du einzelne Dateien l�dst, sollten diese dem Wildcard  "*_hash.dds" entsprechen.


Wie interagiert OpenTexMod mit den Spielen?

OpenTexMod klingt sich zwischen die Verbindung vom Spiel und DirectX ein.
Das verlangt, dass OpenTexMod bereits vor dem Spiel gestartet wird.

Die GUI von OpenTexMod fungiert als Server. Ein Spiel, in das sich erfolgreich
eingeklingt wurde, verbindet sich beim Programmstart mit dem Server.
Die GUI von OpenTexMod kann mehrere Spiele gleichzeitig verwalten.
Jede Instanz eines Spieles wird auch separat gehandhabt (wenn ein Spiel
mehrfach gestartet wird).


Wie bekomme ich OpenTexMod zum laufen?

Es gibt zwei Wege wie OpenTexMod sich in die DirectX Verbindung einklinken kann:

1) (bevorzugt)  F�ge die Spiel-exe �ber das Men� Spiele->"Spiel hinzuf�gen" hinzu.
    Wenn du Steam verwendest, lies weiter unten nach.
   
2) Kopiere die d3d9.dll (vom OpenTexMod Verzeichnis) in das Spiele Verzeichnis.
    Einige Spiele laden eine dll zuerst aus dem eigenen Verzeichnis bevor sie im
    Systemverzeichnis suchen. Nur f�r diese Spiele wird diese Methode funktionieren.
    WARNUNG: Kopiere diese dll niemals in das Systemverzeichnis!!
   
Wenn  du dich f�r eine Methode entschieden hast, starte einfach OpenTexMod
und danach das Spiel. Es ist nicht n�tig (du kannst auch nicht) das Spiel �ber
OpenTexMod zu starten.

Wenn das Spiel startet und alles glatt l�uft, �ffnet sich sofort ein neuer Tab in OpenTexMod.
In diesem Tab kannst du nun das Spiel  modden. Dr�cke den "Update" Button um
die Einstellungen an das Spiel zu senden. Du kannst deine aktuellen Einstellungen auch
speichern. Sie werden dann automatisch geladen und an das Spiel gesendet, wenn du
dieses Spiel das n�chste Mal startest.

Um einen Mod zu laden, musst du das H�kchen vor den Namen setzen. Wenn du
den Mod entladen willst, entferne das H�kchen und klicke auf "Update". Zurzeit
werden die Mods nicht aus dem Spiel entladen, wenn du den "X" Button dr�ckst.

Weil verschiedene Mods die gleiche Ziel-Textur ver�ndern k�nnten, wird nur die
Mod-Textur des ersten Mods ber�cksichtigt. Die Aktion dieses Mods (also Laden oder
Entladen) wird durchgef�hrt, ungeachtet dessen, was die restlichen Mods mit der
Ziel-Textur machen sollen.


Wie bekommt man OpenTexMod mit Steam zum Laufen?

OpenTexMod schaut auf den Namen der ausgef�hrten Spiel-Datei, nicht nach dem Verzeichnis.
Daher solltest du nicht die steam.exe sondern die Spiel.exe hinzuf�gen.
z.B.: Steam\SteamApps\acoount_name\portal\hl2.exe
BTW: Dies w�rde auch alle anderen HalfLife 2 Spiele betreffen.

Wenn du deine Spiele-exe nicht finden kannst, schau im TaskManager nach und:
1) f�ge sie per Hand hinzu: editiere unter Windows 7
    C:\Users\user_name\AppData\Roaming\OpenTexMod\OTM_DX9.txt
    oder:
2) erstelle irgendwo eine Datei mit dem Namen der Spiele-exe und f�ge diese
    mithilfe des Men�s in OpenTexMod hinzu, anschlie�end kannst du diese
    Datei l�schen.