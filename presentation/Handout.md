# Angriffsszenarien auf etablierte Netzwerkprotokolle

## EternalBlue und WannaCry

**EternalBlue** ist eine Schachstelle in der Windows-Implementation des SMB-Protokolls, 
das zum *File-sharing* innerhalb eines Netzwerkes genuzt wird.
Der SMB-Server läuft auf Windows mit System-rechten, und ist daher ein gutes Ziel für Angreifer,
die Zugriff auf einen Rechner erlangen wollen.

**WannaCry** ist ein sog. ***Ransomworm***, der ältere Versionen von u.a. Windows 7, 8.1, 10 und Vista
angegriffen hat. Er nutzt die EternalBlue-Schwachstelle, um ein System zu infizieren.  
WannaCry wird als ein sog. *Ransomworm* (dt. *Lösegeld-Wurm*) bezeichnet, da er ein System hybrid verschlüsselt und
sich selbstständig weiterverbreitet.  

<p align=center>
    → Das BSI, Verbraucherzentrum und Microsoft raten <b>gegen</b> die Zahlung!
</p>

## OpenSSL und Heartbleed


<img align=right src="https://upload.wikimedia.org/wikipedia/commons/1/11/Simplified_Heartbleed_explanation.svg" width=250 height=250>

<p align=left>
<b>OpenSSL</b> ist eine sehr weit verbreitete Bibliothek für <code>C/C++</code>, die es erleichtern soll,
in Programmen <code>SSL bzw. TLS</code> zu nutzen, was man für <b>HTTPS</b> benötigt.
Unter anderem nutzen <code><b>Apache HTTPD</b></code> und <code><b>NGINX</b></code>, zwei der am weitesten verbreiteten Engines, wenn das HTTPS-Modul aktiv ist, OpenSSL standardmäßig.
</p>

&nbsp;

<p align=left>
    Dem Server wird eine Zeichenkette <code>(im beispiel: "bird")</code> und <wbr> die dazugehörige länge <code>(im beispiel: 4)</code>, die der Server zurücksenden soll bzw. zurücksendet. <br>
    Allerdings überschreibt die <b>angegebene Länge</b> die <b>eigentliche Länge</b> wenn sie nicht übereinstimmen <code>(im beispiel: "bird", eigentlich: 4, angegeben: 500)</code>
</p>

&nbsp;

<div class="page" />

## Prävention

<div style="display: flex">
        <details style="align: left; clear: both;" open>
            <summary><h3 style="display: inline">Als End-Nutzer</h3></summary>
            <ul style="list-style-type: none">
                <li> → Installiere Apps nur aus vertrauenswürdigen Quellen <br> &nbsp; &nbsp; &nbsp; (z.B. aus vorinstallierten App-Stores)</li>
                <li> → Halte deine Systeme immer möglichst auf dem neusten Stand</li>
                <li> → Setze möglichst auf Open-Source-Software (="OSS"/"FOSS")<br> &nbsp; &nbsp; &nbsp; <i>aber</i>: <b>auch OSS kann gravierende Fehler haben!</b></li>
            </ul>
        </details>
        <details style="align: right; clear: both; margin-left: 4px;" open>
            <summary><h3 style="display: inline">Als Entwickler</h3></summary>
            <ul style="list-style-type: none">
                <li> → Nutze <b>Kommentare</b> und <b>Dokumentiere</b> deinen Code</li>
                <li> → Halte dich an die <a href="https://www.oracle.com/java/technologies/javase/codeconventions-contents.html">Standards</a> der Programmiersprache</li>
                <li> → Nutze Versions-kontrollsysteme (z.B. <b>Git</b>)</li>
                <li> → Wenn dein Code Fehler hat nutze <a href="rubberduckdebuging.com">Rubber Duck Debugging</a></li>
            </ul>
        </details>
</div>

------------------
> Die Präsentation, das Handout selbst, die Seminararbeit und Quellen findest du unter: <img style="display: inline-block; vertical-align: bottom; margin-bottom: 3.5px;" height="16" src="https://github.githubassets.com/pinned-octocat.svg" width="16"/> [github.com/akb1154/seminararbeit](https://github.com/akb1154/seminararbeit)

<details open>
<summary><h3 style="display: inline;">System-rechte</h3></summary>
<p>
    Zugriffsrechte mit denen das System selbst arbeitet. 
    In Windows sind System-rechte höher gestellt als Administrator-rechte.   <br>
    → Windows selbst kann <code>C:\Windows\System32</code> löschen, aber ein Administrator (bzw. normaler Nutzer) können dies Nicht.
    <br><br>
    Sie sind vergleichbar mit dem <code>root</code> - Nutzer auf <cite>macOS</cite> bzw. <cite>Linux<abbr title="Der root-Account ist im sog. Linux-Kernel, aber er durch das System vor dem Nutzer versteckt werden.">*</abbr></cite>
</p>
</details>
