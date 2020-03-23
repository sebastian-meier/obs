This document and the templates are work in progress...

# Open Broadcaster Software (Studio)

[Deutsche Version](#deutsche-version)

## Introduction

As COVID19 is changing the way we teach this semester, i explored multiple tools for creating video content for my students. I decided to pick Open Broadcaster Software (OBS) Studio, as it has all the features (scenes, webcam, app and text input) i need, it is open source and available for mac, windows and linux. In the following i will give a very brief introduction to the software, as well as a guide on how to use my prepared templates for any HCU colleagues that are interested (or anyone else who wants to use them as a boilerplate).

This is fast-forward introduction, focussing on using OBS for teaching. There are lots of detailed tutorials and introductions to OBS out there, e.g.: https://streamshark.io/obs-guide/

## What is OBS

OBS is a software that allows you to record and/or stream video content from your computer. It is very basic, but therefore, also extremely easy to use. You can create so called scenes, which allow you to combine different kinds of inputs (screen capture, webcam, images, text, web-content, etc.). You can switch between scenes while recording (e.g. switch from focus on presenter's webcam to focus on the screen capture).

OBS is free, open source and financially supported by a couple of companies: twitch, facebook, nvidia, logitech xplit, games done quick and others.

## Requirements

You only need a computer, everything else is optional. But for a good recording i would recommend: 
1. A secondary screen: Having a second screen where you can run the OBS app on and the the other screen for screen capturing. If you are livestreaming you will also need the OBS screen for interacting with your peers. 
2. A webcam: While many laptops and screens have built in cams, they are often in an not ideal angle, try to position the camera straight in front of you, in order to avoid weird distortions and angles.
3. A mic: Check if the mic build into your laptop is good enough, otherwise get an external one.

## Get started

### Download the software

Download and install the software form the [OBS website](https://obsproject.com/)

### Note

There is no undo feature 🤯!

### First launch

On first launch the software will run you through a tutorial for the initial settings, no worries, you can change everything later from the settings menu.

![Screen Overview](./readme_graphics/00-overview.png)

### Size/Resolution of your streaming output

I am personally recording & streaming a 1920*1080 video feed. But obviously this also depends on the content you produce. It also depends on your bandwidth. Slow bandwidth might require a lower resolution. To set your video output size:

<img src="./readme_graphics/01-settings.png" width="410">

Click on settings.

![Video Settings](./readme_graphics/02-video-settings.png)

Go to Video and set the resolution. For slow bandwidth you could also reduce the frames per second (FPS).

### Adding Content

There are different types of content, for creating your seminar, most importantly Browser (show content from the web, this can also be local content), Display Capture or Window (screen   recording), Image, Text and Video Capture Device (webcam). For adding new material, simply go to the "Sources" panel, click the "+" button and add the content you require. The initial configuration of the object can be opened through a double click or right-click > "Properties".

What is quite nice, you can reuse content you once added. The good thing about this, is also a possible problem, if you for example reuse a Browser-Source and change the URL, the URL will change in all other instances of that Browser-Source. Important to keep in mind.

### Adding Text > Text Width

Text is quite straight forward. Things to know, there are two colors, you need to adjust both, otherwise, you have a gradient in your text. If you want to write longer text and want the text to automatically wrap: scroll to the end of the text properties box, enter a text-width and check "wrap text".

![Text Settings](./readme_graphics/03-text.png)

There is a special option for live feeding text from a text file. I am using this to show students the current step we are working on. Therefore check "Read from file" and select a text file below. As you update your local text file, the text will update automatically in the video (again, good to have a second monitor to do these things while screen recording on the other).

### Scaling Content

<img src="./readme_graphics/04-scaling.png" width="585">

For some reason, scaling things, while keeping the height/width ratio locked, is a bit buggy at times. The easiest way to fix this. Right-click on the content > Transform > Edit Transform > Bounding Box > Scale to inner bounds. Now you can resize as you want the content inside the bounding box will keep it's ratio.

### Fonts

I had some problems with certain fonts and using different font styles (bold, italic). Arial (even though not the nices font) has proven to be very reliable. For those a little bit more experimental, i have included the Lato font in the assets/Lato2OFL folder, which is available under Open Font License (http://www.latofonts.com/).

### Showing Presentations

I used a PDF-viewer like Acrobat in full screen on the secondary screen, which worked nicely, still able to see the OBS controls and could simply click through the presentation. I used my Screen or Window Template Scences for this.

### Exporting Video Files

![Video Export](./readme_graphics/05-export.png)

Once you recorded a video, your video data is stored (per default, recommended) in an MKV file format. In order to turn this into a usable video format, like MP4, got to the Menu "File", select "Remux Recordings". Select the recordings you want to convert. And press the Remux button. After remuxing is done, press the "Clear finished items" button.

### Import HCU Templates

I prepared some templates for my classes at the HafenCity University Hamburg, everybody feel free to use them as your boilerplate.

For importing the files, download this repository, unpack and then go to "Scene Collection" > Import and select the hcu_templates/hcu_templates.json file.

After importing this you should see the following scenes. **One problem**: OBS stores all media as absolute paths, therefore, you need to reconnect all the media files i used. The media files are all located in hcu_templates/assets/... Simply double click the sources and reconnect. As all of you have different devices, you also need to set the Video Capture Device, as well as Secondary Screens and Windows. For those who know how to handle a JSON file, you can also quickly search-and-replace the paths to the media files.

#### Overview

![Grid view](./readme_graphics/obs-7-Grid.png)

All scenes have a hidden "Grid"-Source. OBS does not have guides or a grid, which makes aligning stuff hard. In order to make this easier, i have created a simple grid one can use to align and resize elements.

##### Intro

![Intro screens](./readme_graphics/obs-0-Intro-Line-1.png)

<img src="./readme_graphics/obs-0-Intro-Line-2.png" width="440"><img src="./readme_graphics/obs-0-Intro-Line-3.png" width="440">

<img src="./readme_graphics/obs-1-Intro-Shape-1.png" width="290"><img src="./readme_graphics/obs-1-Intro-Shape-2.png" width="290"><img src="./readme_graphics/obs-1-Intro-Shape-3.png" width="290">


Simple Screen for the starting of your lecture. Simply double-click Meta-Title, Title and Date, change to your likings. Exchange the Background-Image e.g. with a slide from your seminar. The intro comes in two flavours, the first has a color overlay on top of the background image, in order for making the text more readable. And then one of three outlines from the HCU corporate design. The second version uses the same outlines as masks.

#### Outro

![Outro screens](./readme_graphics/obs-6-Outro-1.png)

<img src="./readme_graphics/obs-6-Outro-2.png" width="440"><img src="./readme_graphics/obs-6-Outro-3.png" width="440">

This is the companion to the Intro screen. The outro is also using one of three outlines from the HCU corporate design. The outlines are shifted to the right, so that there is enough room for contact info, etc.

#### Webcam-Focus

![Webcam screen](./readme_graphics/obs-2-Webcam-Focus.png)

Webcam focus puts focus on the webcam input, i am using this for kicking off my lecture with some personal notes. Overview of topics on the right, coming from a text file and a preview of the slides following next in the upper right corner. If you want to use the live-text, don't forget to reconnect it your own text file, or the one from the assets folder.

#### Other screens

![Outro screens](./readme_graphics/obs-3-1-Screen-Focus.png)

<img src="./readme_graphics/obs-3-2-Screen-Full.png" width="440"><img src="./readme_graphics/obs-3-3-Screen-No-Extras.png" width="440">

The rest of the screens come in three different versions: Focus (Video-Content, Webcam, Notes and Logo), Full (Video-Content, Small Webcam and Logo), Full-No-Extras (Only Video-Content). The Mix of content is either a full screen capture, a window capture or browser content.

<img src="./readme_graphics/obs-4-1-Browser-Focus.png" width="290"><img src="./readme_graphics/obs-4-2-Browser-Full.png" width="290"><img src="./readme_graphics/obs-4-3-Browser-No-Extras.png" width="290">

<img src="./readme_graphics/obs-5-1-Window-Focus.png" width="290"><img src="./readme_graphics/obs-5-2-Window-Full.png" width="290"><img src="./readme_graphics/obs-5-3-Window-No-Extras.png" width="290">

### Zooming

As i will be doing software and coding tutorials mostly, an additional requirement for me is zooming onto elements in the software. OBS cannot do this out of the box. Windows and Mac both (and i am sure linux as well) have build in magnifiers. They are easy to use through hot keys. Following the setup for MacOS:

![Setting up zoom on osx](./readme_graphics/zoom-osx-1.png)

Go to settings.

![Setting up zoom on osx](./readme_graphics/zoom-osx-2.png)

Go to Accessibility > Zoom

![Setting up zoom on osx](./readme_graphics/zoom-osx-3.png)

Activate the hotkeys. At the bottom there are two options for how zoom works, either the whole screen is zoomed, or a small overlay acts as a magnifying glass.

## Copyright Notice
This explanation, as well as the templates themselves are available unter MIT license. The images and logos in the assets folder are property of the HCU and thereby protected.

# Deutsche Version

## Hinweis

Mein Mac ist auf englisch eingestellt, deshalb haben die Buttons und Menüs im deutschen entsprechend andere Bezeichnungen.
Dieses Dokument und die Templates sind noch in Bearbeitung und minimale Änderungen können noch folgen.

# Open Broadcaster Software (Studio)

## Einführung

Bedingt durch COVID19, wird sich die Art und Weise wie wir dieses Semester unterrichten verändern. Ich habe verschiedene Werkzeuge ausprobiert, um Video Inhalte und Video Streams für meine Studierenden zu produzieren. Schlussendlich habe ich mich für die Open Broadcaster Software (OBS) Studio entschieden. Zum einen deckt die Anwendung alle meine Anforderungen an solch eine Anwendung ab (Szenen, Webcam, Screencast, Text-Input, etc.), darüber hinaus handelt es sich bei OBS um eine freie Open Source Anwendung, welche unter Windows, Mac und Linux läuft. Im folgenden werde ich eine sehr knappe Einführung in die Anwendungen geben und die Templates vorstellen, welche ich für meine Lehre an der HCU erstellt habe.

Die Einführung fokussiert meinen Gebrauch der Anwendungen in der Lehre und ist sehr knapp gehalten. Es gibt jede Menge detaillierte Erläuterungen und Tutorials zu OBS, z.B.: https://streamshark.io/obs-guide/

## Was ist OBS

Die OBS Anwendung erlaubt das Aufnahmen und Streamen von Videoinhalten. Die Anwendung ist sehr rudimentär, aber genau deshalb auch sehr einfach zu bedienen. Man kann sogenannte Szenen anlegen, welche es einem erlauben verscheidene Kombinationen von Input-Quellen zu arrangieren (Bildschirmaufnahme, Webcam, Bilder, Text, Web-Inhalte, etc.). Man kann während der Aufnahme bequem zwischen diesen Szenen hin- und herwechseln (z.B. ein Wechsel von einer Großdarstellung der Webcam auf eine Ansicht der Bildschirmaufnahme).

OBS ist frei und open source. Das Projekt wird finanziell unterstützt von mehreren Firmen: twitch, facebook, nvidia, logitech xplit, games done quick und anderen.

## Anforderungen

Eigentlich benötigt man nur einen Computer, alle anderen Anforderungen sind optional. Ich persönlich würde aber folgendes Setup empfehlen: 
1. Ein zweiter Bildschirm: Mit einem zweiten Bildschirm hat man die Möglichkeit auf einem Bildschirm z.B. eine Präsentation zu zeigen oder ein Software-Tutorial durchzuführen, wähernd man auf dem anderen Bildschirm weiterhin die OBS Software einsehen kann und z.B. Szenenwechsel, etc. durchführt. Gerade wenn man Live-Streamen möchte, benötigt man den zweiten Bildschirm so oder so, um mit den Zuschauer*innen zu interagieren. 
2. Eine Webcam: Zwar haben die meisten Laptops mittlerweile eine eingebaute Kamera, diese ist aber in der regel in einem nicht idealen Winkel zum Sprecher positioniert. Mit einer externen Kamera, kann man diese optimal frontal positionieren. Auch auf das halbwegs gleichmäßige ausleuchten des Gesichts sollte man achten, um harte Schatten zu vermeiden.
3. Ein Mikrophon: Man sollte einen Test machen um auszuprobieren, ob das eingebaut Mikrophon des eigenen Computers ausreichend ist. Anderenfalls sollte man sich ein externes anschaffen.

## Los geht's

### Download the software

Software herunterladen und installieren [OBS website](https://obsproject.com/)

### Hinweis

Es gibt keine Rückgängig-Funktion 🤯!

### Initialler Start

Beim ersten Start der Anwendung, wird man durch ein Tutorial geleitet und Einstellungen festzulegen. Keine Sorge, diese kann man alle später einfach über das Menü wieder anpassen.

![Screen Overview](./readme_graphics/00-overview.png)

### Größe/Auflösung des Video Outputs

Ich persönlich nehme meine Videos bei einer vollen Auflösung von 1920*1080 (Full HD) auf. Die Auflösung sollte auch auf die Inhalte abgestimmt sein. Ich selber mache Software-Tutorials (QGIS), möchte also das auch kleinere Details später sichtbar sind. Die Auflösung die man auswählt, hängt auch von der einem zur Verfügung stehenden Bandbreite ab. Nutzer*innen mit langsamem Internet, sollte eine geringere Auflösung wählen. Um die entsprechenden Einstellungen vorzunehmen:

<img src="./readme_graphics/01-settings.png" width="410">

Auf "Settings" klicken.

![Video Settings](./readme_graphics/02-video-settings.png)

Zum "Video"-Tab gehen und die Einstellung einstellen. Bei langsamem Internet kann man auch die Frames pro Sekunde runterstellen (FPS).

### Inhalte (Quellen/Sources) hinzufügen

Es gibt verschiedene Inhaltstypen, um die Szenen für das eigene Seminar zu gestalten. Die wichtigsten sind u.a. Browser (Inhalte aus dem Internet zeigen, auch lokale Server), Display- oder Window-Capture (Bildschirmaufnahme), Bilder, Text und Video Capture Device (webcam). Um Inhalte hinzuzufügen, geht man zum "Sources"-Tab, klickt auf den "+"-Button und wählt den entsprechenden Inhalt aus. Die Einstellungen, welche man danach vornimmt, kann man später mit einem einfachen Doppel-Klick auf das Elemente in der "Sources"-Liste oder über Rechts-Klick > "Properties" vornehmen.

Was sehr praktisch ist, man kann einmal angelegte Inhalte mehrfach benutzen. Dieses Feature kann aber auch zum Problem werden. Fügt man beispielsweise ein Text-Element erneut ein und ändert den Text, dann ändert sich der Text auch bei allen anderen Instanzen. Man kann dies auch umgehen, in dem man ein Element dupliziert.

### Text hinzufügen > Text-Breite

Das einfügen und bearbeiten von Text ist relativ einfach. Man sollte dabei darauf achten, dass Text zwei Farben hat, welche man beide ändern muss, sonst bekommt man einen wenig ansehnlichen Verlauf in seiner Schrift. Wenn man einen längeren Text schreiben möchte, kann man am Ende der Text-Einstellungen eine Textbreite angeben und den automatischen Umbruch aktivieren.

![Text Settings](./readme_graphics/03-text.png)

Es gibt eine spezielle Funktion um Text in Echtzeit aus einer Textdatei einzulesen. Ändert sich der Text in der Datei, verändert sich der Text im Video automatisch. Hierfür muss man lediglich die Checkbox "Read from file" anklicken und dann eine entsprechende Datei auswählen. Es muss sich dabei um eine reine Textdatei handeln, kein formatierter Text wie z.B. eine Word-Datei.

### Inhalte skalieren

<img src="./readme_graphics/04-scaling.png" width="585">

Aus irgend einem Grund funktioniert das skalieren von Inhalten mit fixiertem Seitenverhältnis manchmal nicht und man verzerrt versehentlich Inhalte. Sollte dies passieren, kann man über einen Rechts-Klick auf das Elemente > "Transform" > "Edit Transform" > "Bounding Box" > "Scale to inner bound", das Problem lösen. Man kann nun das Rechteck beliebig skalieren und der Inhalt passt sich diesem an, ohne das Seitenverhältnis dabei zu verändern.

### Schriften

Bei meinen Tests hatte ich Probleme mit manchen Schriften bzw. Schriftstilen (fett, kursiv). Arial (auch wenn es nicht die hübscheste Schrift ist) schien sehr solide zu funktionieren. Für die Templates habe ich außerdem die Schrift Lato mit den den Assets-Order gepackt (assets/Lato2OFL), die Schrift ist unter einer Open Font License verfügbar (http://www.latofonts.com/).

### Präsentationen zeigen

Ich selber nutze einen PDF-Viewer (wie z.B. Acrobat) und lasse diesen in Vollbildmodus auf meinem zweiten Bildschirm laufen und übertrage diesen dann, auf dem anderen Bildschirm sehe ich weiterhin die OBS controls und kann dann durch die Präsentation klicken.

### Video Dateien exportieren

![Video Export](./readme_graphics/05-export.png)

Während man Videos aufzeichnet, werden diese (empfohlene Standardeinstellung) als MKV Dateien abgespeichert. Um diese in ein übliches Videoformat wie z.B. MP4 zu konvertieren, muss man im Menü "File" > "Remux Recordings" auswählen. Dort wählt man dann links die Dateien aus die konvertiert werden sollen. Dann einfach auf "Remux" klicken. Nachdem alles konvertiert wurde, die Liste mit "Clear finished items" leeren.

### HCU Vorlagen importieren

Ich habe ein paar Vorlagen für meine Lehre an der HafenCity Universität Hamburg vorbereitet, diese können als Grundlage von allen genutzt werden.

Um diese Vorlagen zu nutzen, einfach dieses Repository herunterladen, entpacken und dann unter "Scene Collection" > Import die folgende Datei auswählen: hcu_templates/hcu_templates.json.

Nachdem Import sollte man eine Reihe Szenen sehen, welche im Folgenden weiter erkärt werden. **Ein Problem**: OBS speichert alle Pfade absolut, deshalb müssen alle Medien erneut verknüpft werden. Die Beispielmedien befinden sich alle in folgendem Ordner: hcu_templates/assets/... Einfach auf die entsprechenden Ressourcen klicken und die entsprechende Datei auswählen. Da jeder unterschiedliche Geräte besitzt, muss man natürlich auch seine Webcam und seinen "Secondary Screen" erneut auswählen. Wer sich mit JSON auskennt kann auch schnell die Pfade durch suchen-ersetzen anpassen.

#### Übersicht

![Grid view](./readme_graphics/obs-7-Grid.png)

Alle Szenen haben eine ausgeblendete "Grid"-Source. OBS hat leider keine Hilfsmittel zum Ausrichten von Element. Um dies einfacher zu machen, habe ich ein simples Grid angelegt, welches man ein- und ausblenden kann.

##### Intro

![Intro screens](./readme_graphics/obs-0-Intro-Line-1.png)
![Intro screens](./readme_graphics/obs-0-Intro-Line-2.png)
![Intro screens](./readme_graphics/obs-0-Intro-Line-3.png)

![Intro screens](./readme_graphics/obs-1-Intro-Shape-1.png)
![Intro screens](./readme_graphics/obs-1-Intro-Shape-2.png)
![Intro screens](./readme_graphics/obs-1-Intro-Shape-3.png)

Ein einfacher Screen um seine Vorlesung zu starten. Einfach die "Sources" Meta-Title, Title und Daten Doppel-Klicken und anpassen. Das Hintergrundbild bei Bedarf durch ein Bild aus der Vorlesung austauschen. Um etwas Abwechslung in die Vorlesungen zu bringen, kann man verschiedene Grafiken über das Hintergrundbild legen. Einfach die "Line"-"Sources" ein- und ausschalten. In einer zweiten Version gibt es die Intro-Szenen auch mit einer Maske statt einer Umrisslinie.

#### Outro

![Outro screens](./readme_graphics/obs-6-Outro-1.png)
![Outro screens](./readme_graphics/obs-6-Outro-2.png)
![Outro screens](./readme_graphics/obs-6-Outro-3.png)

Das Depandant zur Intro-Szene. Hier gibt es auch wieder verschiedene Outlines zum Auswählen. Diese sind so positioniert, dass man links Platz für z.B. Kontaktdaten hat.

#### Webcam-Focus

![Webcam screen](./readme_graphics/obs-2-Webcam-Focus.png)

Der Webcam-Focus setzt die Webcam in den Mittelpunkt. Ich nutze diese Ansicht um meine Vorlesung mit ein paar persönlichen Worten zu beginnen. Rechts ist ein Live-Text integriert um den Ablauf der Vorlesung anzuzeigen. Wer den Live-Text nutzen möchte, darf nicht vergessen die Datei nach dem Import zu verknüpfen.

#### Andere Szenen

![Outro screens](./readme_graphics/obs-3-1-Screen-Focus.png)
![Outro screens](./readme_graphics/obs-3-2-Screen-Full.png)
![Outro screens](./readme_graphics/obs-3-3-Screen-No-Extras.png)

Die restlichen Szenen gibt es immer in drei Varianten: Focus (Video-Inhalt, Webcam, Live-Text, Logo), Full (Video-Inhalt, Kleine Webcam, Logo) und Full-no-Extras (nur Video-Inhalt). Diese Szenen gibt es für Screen-Sharing, Window-Sharing und Web-Inhalte.

<img src="./readme_graphics/obs-4-1-Browser-Focus.png" width="150">
<img src="./readme_graphics/obs-4-2-Browser-Full.png" width="150">
<img src="./readme_graphics/obs-4-3-Browser-No-Extras.png" width="150">

<img src="./readme_graphics/obs-5-1-Window-Focus.png" width="150">
<img src="./readme_graphics/obs-5-2-Window-Full.png" width="150">
<img src="./readme_graphics/obs-5-3-Window-No-Extras.png" width="150">

### Zooming

Da ich hauptsächlich Coding- und Software-Tutorials gebe, muss ich gelegentlich in den Bildschirm reinzoomen. OBS hat hierfür leider keine fertige Funktion. Windows und Mac haben beide aber entsprechende Anwendungen vorinstalliert (Linux bestimmt auch). Diese kann man über Short-Cuts entsprechend ein- und ausschalten. Folgend eine Anleitung für OSX:

![Setting up zoom on osx](./readme_graphics/zoom-osx-1.png)

Einstellungen öffnen.

![Setting up zoom on osx](./readme_graphics/zoom-osx-2.png)

Zu den Accessibility- / Barrierefreiheits-Eintellunge > Zoom

![Setting up zoom on osx](./readme_graphics/zoom-osx-3.png)

Hotkeys aktivieren. Am Ende der Einstellungen kann man zwei Optionen auswählen, welche beeinflussen wie die Lupe angezeigt wird, entweder als kleines Overlay, oder ein Zoom des gesamten Bildschirms.

## Copyright Hinweis
Die Anleitung, als auch die Vorlagen sind mit einer MIT license versehen. Die Bilder und Logos, welche sich im Assets-Order befinden, sind Eigentum der HCU und damit geschützt.