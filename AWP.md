# Schreibtischtest 

Der Schreibtischtest ist ein Verfahren, das im Bereich der Softwareentwicklung verwendet wird, um Algorithmen oder Routinen auf Richtigkeit zu prüfen. Der Schreibtischtest wird nicht mit Hilfe eines Rechners durchgeführt, sondern vielmehr im Kopf des Entwicklers. Dazu werden für einen deterministischen und terminierenden Programmablauf eine Eingabe- und eine mögliche Ausgabemenge festgelegt. Anschließend wird mit jedem Element der Eingabemenge durch schrittweises Durchrechnen die Korrektheit des Programmablaufs überprüft. Der gewählte Programmablauf verhält sich für das gewählte Eingabeelement genau dann korrekt, wenn das ausgegebene Element, also das Ergebnis, Teil der Ausgabemenge ist.

Die Tatsache, dass die Eingabemenge für einen Algorithmus beliebig groß sein kann, z. B. eine Untermenge der natürlichen Zahlen, erfordert vom Entwickler zur Überprüfung der Korrektheit des zu testenden Programms die schrittweise Durchrechnung mit allen Elementen der Eingabemenge. Gibt es für die Eingabemenge keine obere oder untere Schranke, dann kann der Schreibtischtest höchstens mit einigen plausiblen Eingaben ein Indiz dafür liefern, dass der Algorithmus richtig implementiert wurde.

Voraussetzungen für den Schreibtischtest sind also ein deterministischer und terminierender Programmablauf, die Kenntnis über plausible und sinnvolle Eingabeelemente, und die Kenntnis der zu den Eingabeelementen passenden Ausgabeelemente, um aus der jeweiligen Ausgabe auf die Richtigkeit schließen zu können. Das Ergebnis für die jeweilige Eingabe muss also bekannt sein.

# UML Klassendiagramm

Attribute:

| Attribute   |
|-------------|
| +:public    |
| -:private   |
| #:protected |
| ~:package   |
| default: -  |

# Programmbibliotheken 

##Beschreibung:
In erweitertem Sinn gelten als Programmbibliotheken (zum Teil auch „Komponentenbibliothek“ oder „Klassenbibliothek“ genannt) alle Arten von Bibliotheken, die Programmcode(-bestandteile) bereitstellen/enthalten. Insofern unterscheidet man Programmbibliotheken u. a. nach dem Typ des Programmcodes, z. B. Quelltexte, Makros, Object- oder Bytecode, Maschinencode usw. Dementsprechend werden Bibliotheken zu unterschiedlichen Zeitpunkten benutzt, manche nur im Rahmen der Softwareentwicklung (von Werkzeugen der Entwicklungsumgebung), andere nur zur Ausführung von Programmen, wieder andere als Mischform von beiden. Solche Bibliotheken enthalten häufig nicht nur Unterprogramme, sondern Programmcodeteile aller Programm-Typen.

Manche proprietären Programmbibliotheken werden nicht im Quelltext veröffentlicht, da sie Firmengeheimnisse darstellen. Zum Schutz gegen Dekompilieren werden dann oft ein Obfuscator eingesetzt sowie alle Symbole (Variablen- und Sprungadressnamen) entfernt.

Mögliche Zugriffe auf Funktionen einer Programmbibliothek sind durch die Programmierschnittstelle (API) definiert. Dabei handelt es sich um die Gesamtheit der öffentlich verfügbaren Funktionen und Klassen; in Abgrenzung zu den privaten Einheiten der Bibliothek, die nicht zugänglich sind.

Eine besondere Form von Programmbibliotheken sind Frameworks.

##Speicherungsformen
Programmbibliotheken und ihre Inhalte können, abhängig vom Betriebssystem und der Entwicklungsumgebung, in unterschiedlichen Formen und Strukturen gespeichert werden, zum Beispiel:

Die Bibliothek ist ein Dateiverzeichnis, ihre Elemente/Komponenten sind einzelne Dateien.
Die Bibliothek ist eine Datei die darin enthaltenen Komponenten werden von den Programmen der Entwicklungsumgebung oder einer speziellen Bibliotheksverwaltungssoftware identifiziert und verarbeitet.
Beispiele: Eine sogenannte 'DLL' bei Microsoft oder eine PO-Datei bei IBM-Großrechnern als Bibliothek für Quelltexte, Objektmodule oder ausführbare Lademodule.
Unterschiedliche Arten von Bibliotheken werden in einer gemeinsamen Datei[ verwaltet, die Entwicklungsumgebung kann dies unterscheiden/verarbeiten. 

Beispiel: Eine 'MDB' bei MS Access enthält Bibliotheken mit Quellcode, Makros, vorübersetztem Pseudocode und anderen Codetypen.
Es existiert keine ‚Bibliothek‘, die Komponenten werden als einzelne Dateien gespeichert und ausgeführt, z. B. als „EXE-Dateien“.


##Statische Bibliotheken
„Statische Bibliothek“ wird eine Programmbibliothek genannt, die Module/Unterprogramme enthält, die durch einen so genannten Linker (von englisch „to link“: verknüpfen) mit dem Kompilat eines anderen Programms verbunden werden. Dabei erzeugt der Linker, in der Regel für ein Hauptprogramm, eine ausführbare Datei oder (je nach Betriebssystem) ein Lademodul in einer Ladebibliothek, in der die von diesem aufgerufenen Module fest (statisch) eingebunden/angehängt sind.

Ein optimierender Linker sucht aus den zugeordneten Objekt-Modulen (Bibliotheksdateien) nur jene Komponenten (Unterprogramme oder Daten) heraus, die vom Programm auch tatsächlich aufgerufen (referenziert) werden (und für die es im Programm keine überschreibende Implementierung gibt) und hängt sie dann an das Programm an. Die so entstehende Datei wird entsprechend größer. Einfache Linker fügen einfach das komplette Objekt-Modul bzw. die komplette Bibliothek hinzu und vergrößern das Programm dadurch noch mehr.

Eine statische Bibliothek ist im Allgemeinen selbst Ergebnis aus Quelltexten, aufgeteilt in mehrere Module, deren Kompilate (Objektmodule) dann vom Linker zu der Bibliothek zusammengefügt wurden.

##Dynamische Bibliotheken
Aus dynamischen Bibliotheken werden Komponenten erst während der Laufzeit eines Programms über einen sogenannten Lader in den Arbeitsspeicher geladen. Das geschieht entweder durch eine explizite Anweisung durch das Programm oder implizit durch einen so genannten Laufzeit-Lader, wenn das Programm dynamisch gebunden wurde. Heutzutage geschieht dies meist mit Betriebssystem-Unterstützung, da (siehe unten) dynamische Bibliotheken gesondert behandelt werden bzgl. Swapping und Einblendung in den Programm-Adressraum. Der Lader ist somit heute meist zu weiten Teilen eine Betriebssystem-Komponente.

Dynamisch gebundene Programme müssen sich um das Laden der benötigten dynamischen Komponenten nicht selbst kümmern. Beim dynamischen Binden werden Bibliothek und Kompilat nur lose verknüpft. Statt die notwendigen Symbole (Variablen- und Sprungadressnamen) zu kopieren, wie beim statischen Binden der Fall, werden sie nur referenziert. Um das Laden der dynamischen Bibliotheken und Suchen der Symbole kümmert sich ein sogenannter Laufzeit-Binder. Das Auflösen der referenzierten Symbole geschieht entweder sofort (noch vor Start des eigentlichen Programms bzw. beim Laden aus der Bibliothek) oder faul, bei der ersten Verwendung des Symbols.

Ein typischer Anwendungsfall dafür, Bibliotheken explizit zu öffnen (die Adresse von Symbolen nach deren Namen zu suchen, um das Symbol zu verwenden), sind Plug-in-Architekturen. Ein weiteres Szenario ist eine optionale Bibliothek, die verwendet wird, falls vorhanden, deren Fehlen aber keinen Fehler darstellt.

Ein Vorteil von dynamischen Bibliotheken ist, dass Programme, die eine dynamische Bibliothek verwenden, von Fehlerbehebungen in der Bibliothek profitieren, ohne neu übersetzt werden zu müssen. Wird beispielsweise ein Fehler in der OpenSSL-Bibliothek gefunden und behoben (die entsprechende Bibliothek wurde ersetzt), so genügt ein Neustart der Programme, die diese Bibliothek verwenden, um den Fehler auch in diesen Programmen zu beheben.

Da die Dateien, in denen dynamische Bibliotheken gespeichert werden, bei der Benutzung nur gelesen und ausgeführt, aber nicht verändert werden, müssen Betriebssysteme mit virtuellem Speicher dynamische Bibliotheken nur einmal laden und können sie dann in den Adressraum aller verwendenden Prozesse einblenden. Dies ist beispielsweise bei Multitasking-Systemen vorteilhaft, wenn die Bibliotheken insgesamt sehr groß sind und von vielen Prozessen gleichzeitig verwendet werden. (Sollte die DLL interne Zustände oder gespeicherte Daten besitzen, kann dies mit Copy-On-Write abgefangen werden.)

Viele moderne Betriebssysteme laden die DLLs jedoch nicht sofort, sondern blenden sie bei Bedarf direkt von der Festplatte aus ein – sie werden wie ausgelagerte Pages behandelt. Analog werden nicht benötigte Pages, die zu einer DLL gehören und nicht verändert wurden, einfach verworfen. Bei Bedarf können sie ja aus der Festplatte (der DLL-Datei) wieder geladen werden.


# Klassendiagramme

##Zweck

Klassendiagramme stellen die statische Struktur eines Systems dar. Sie zeigen die Klassen, die Eigenschaften der Klassen (Attribute), das Verhalten (Operationen) der Klassen und die Beziehungen zwischen den Klassen.

Sie sind der zentrale Diagrammtyp der UML und werden in allen Phasen der Soft­wareentwicklung eingesetzt.

##Klasse 

Ein Klasse kann als Rechteck dargestellt werden, das den Klassennamen enthält. Üblicherweise bestehen Klassen aus drei Bereichen; der obere Bereich enthält den Stereotyp, das Paket zu dem die Klasse gehört und den Namen. Im mittleren Bereich werden die Attribute angegeben und im unteren Bereich stehen die Opera­tionen der Klasse. Laut UML-Spezifikation kann die Darstellung einer Klasse zusätzliche Bereiche enthal­ten.

**Abstrakte Klasse** Der Name einer abstrakten Klasse wird kursiv ge­schrieben. Alternativ kann die Eigenschaft {abstract} angegeben werden. Abstrakte Klassen dienen der Strukturierung eines Modells. Sie sind nicht instanziierbar.    Parametrisierte Klasse auch Template oder Schablone genannt. Die parame­trisierte Klasse hat in der rechten, oberen Ecke ein das Klassensymbol überlappendes Rechteck, das die Scha­blonen-Parameter der Klasse enthält. Die Funktion, die den Parameter verwendet wird angegeben. Die Klasse, die den Parameter bindet, wird über eine gestrichelte Linie mit Pfeil an dem Template verbunden. Diese trägt die Bezeichnung <<bind>>.    

**Assoziation** Eine Linie zwischen den Klassen stellt eine Assoziati­on dar. Eine Assoziation ist eine Beziehung zwischen Klassen. Die Objekte der Klassen kommunizieren über die Assoziationen miteinander. Die Assoziation kann einen Namen haben. Ein Pfeil an dem Assoziations­namen gibt die Leserichtung des Namens an. An den Assoziationsenden können die Rollen der beteiligten Klassen und die Multiplizität angegeben werden. Die zweigliedrige Assoziation kann, wie die mehrgliedrige Assoziation, durch eine Raute markiert werden.    Gerichtete Assoziation

Mit einem Pfeil an der Assoziation kann die Naviga­tionsrichtung angegeben werden. Der Pfeil drückt die Zugriffsrichtung der Objekte aus. Objekt A greift auf B zu, B greift nie auf A zu.

**Vererbung** auch Generalisierung/Spezialisierung genannt. Verer­bungsbeziehungen werden mit einem Pfeil dargestellt. Die Pfeilspitze zeigt auf die Oberklasse. Die Ober­klasse vererbt ihre Eigenschaften an die Unterklassen.

**Aggregation**
Eine Aggregation drückt eine Teile-Ganzes-Beziehung aus. Das Ganze-Objekt besteht aus Teil-Objekten. Die Raute befindet sich an dem Ende des Ganzen. Die Aggregation ist eine spezielle Art der Assoziation. Da das Ganze die Teile enthält, sollten am Assoziations­ende der Teile ein Navigationspfeil stehen.

**Komposition**
Die Komposition ist auch eine Beziehung, die Teile zu einem Ganzen in Beziehung setzt. Die Teile und das Ganze sind bei dieser Beziehung existenzabhängig; die Teile können nicht ohne das Ganze existieren. Wird das Ganze gelöscht, so beenden auch die Teile ihre Existenz.

**Assoziationsklasse**
Ist eine Klasse von dem Vorhandensein einer Assozia­tion zwischen zwei Klassen abhängig, so kann dies durch eine Assoziationsklasse ausgedrückt werden. Die Assoziationsklasse beschreibt Eigenschaften, die keiner der an der Assoziation beteiligten Klassen sinn­voll zuordenbar sind. Die Assoziationsklasse wird über eine gestrichelte Linie mit der Assoziation, von der sie abhängt, verbunden. Hat die Assoziation einen Namen, dann muss die Assoziationsklasse den selben Namen erhalten. Die Assoziationsklasse ist ein Analy­sekonzept.

**Mehrgliedrige Assoziation** 
Eine mehrgliedrige Assoziation drückt eine Beziehung zwischen mehr als 2 gleichwertigen Klassen aus. Die Beziehung wird mit einer Raute markiert.


## Klassen

Objekte und Klassen sind die zentralen Elemente objektorientierter Modelle. Die gemeinsamen Eigenschaften konkreter Objekte werden zu Klassen abstrahiert. Die Klasse definiert die Struktur ihrer Objekte. Die UML 2.0 versteht unter einer Klasse ein Element, das eine Menge Objekte beschreibt, die die selbe Spezifikati­on der Merkmale, Einschränkungen und Semantik teilen. Eine Klasse hat Attribute und Operationen. Attribute und Operationen können in UML spezifiziert werden.

Die Syntax für die Deklaration von Attributen lautet: [Sichtbarkeit] [/] Name [:Typ] [=Wert]

Die Syntax für die Deklaration von Operationen lautet: [Sichtbarkeit] Name [(Parameterliste)] [: Returntyp]

Die Parameterliste ist definiert als:[Übergaberichtung] Name [: Typ] [ =Wert]

Die Syntaxelemente

**Sichtbarkeit**: 
gibt an, wie die Sichtbarkeit eines Elementes relativ zu seiner Umgebung ist. Die Sichtbarkeit gibt also an, welche Elemente auf ein Attribut, bzw. auf eine Operation zugreifen können. Der Zugriff auf ein Attribut definiert den lesenden und schreibenden Zugriff auf das Attribut; die Sichtbarkeit von Operationen gibt an, welche Elemente die Operation aufrufen können. Folgende Sicht­barkeitsmodi sind definiert.

* public: Jedes andere Element hat Zugriff.

* privat: Der Zugriff ist auf die Objekte der Klasse selbst beschränkt.

*protected : Zugriff besteht nur für die definierende Klasse und die Verer­bungslinien, die von ihr ausgehen.

* package: Das Element ist sichtbar für alle Klassen, die sich im selben Paket befinden.

*Der **Slash** [/] kennzeichnet ein abgeleitetes Element. Ein abgeleitetes Element kann aus einem anderen Modellelement berechnet werden.

**Name**: gibt den Namen des Attributs oder der Operation an.

Typ, Returntyp: gibt den Datentyp eines Attributs, eines Parameters oder Returns an. Die UML definiert einige Typen, wie Integer, String, u. a. Macht aber keine Ein­schränkungen zur Verwendung selbstdefinierter Typen. Es können alle Typen verwendet werden, die zur Lösung eines Problems benötigt werden.

**Wert**: Attribute und Parameter können mit einem Wert belegt werden.

**Übergaberichtung**: definiert die Richtung in die ein Parameter übergeben wird.

**IN**- Parameter wird an die Operation übergeben. Die Operation liest den Pa­rameter nur.

**OUT** - der Parameter wird von der Operation geschrieben, ohne dass sie sei­nen Inhalt vorher verarbeitet.

**INOUT** - die Operation liest einen Parameter, verarbeitet ihn und schreibt ihn erneut.

 

Anwendungsbereich

Klassendiagramme sind der zentrale Diagrammtyp der UML. Sie beschreiben die Klassen eines Systems, ihre Eigenschaften, Operationen und die Beziehungen zwischen den Klassen. Klassendiagramme werden in allen Phasen der Software­entwicklung eingesetzt. Die modellierten Inhalte und das verwendete Vokabular müssen sich an dem Know-how der beteiligten Personengruppen orientieren. Ein Klassendiagramm modelliert einen Teilausschnitt der realen Welt. Es werden nur die Klassen und Eigenschaften berücksichtigt, die zur Beschreibung des Problem­bereichs benötigt werden. Bei der Modellierung von Klassendiagrammen wird zwischen dem Analysemodell und dem Designmodell unterschieden.

Diese verschiedenen Sichten auf ein Klassenmodell können durch den Einsatz von Entwicklungswerkzeugen, wie z. B. Case-Tools verwaltet und konsistent gehalten werden.

 

## Klassendiagramm Analyse

Klassendiagramme in der Sichtweise der Analyse stellen dar, was das System aus Anwendersicht leisten soll. Sie bilden die Klassen, Attribute, Operationen und ihre Beziehungen ab, die das spätere Softwaresystems aus der Sicht des fachlichen Be­reiches, den es abdecken soll, enthalten muss.

Das Analysemodell beschreibt was die zukünftige Software aus fachlicher Sicht leisten soll.

Für die Informatikabteilung, die das geplante Produkt entwickeln soll, stellt das Analysemodell die Basis der zukünftigen Entwicklungsarbeit dar. Da Fehler in der Analyse sehr teuer sind, muss das Analysemodell sehr sorgfältig modelliert werden.

In der **Analyse** sollten sprechende Namen verwendet werden, die auch die betei­ligte Fachabteilung versteht. Die Deklaration von Attributen und Operationen wird in UML, nicht in der späteren Programmiersprache vorgenommen. Bei Ein­satz eines CASE-Tools können daraus die Deklarationen in der gewählten Pro­grammiersprache generiert werden.

## Klassendiagramm Design

Im Designmodell wird das Analysemodell auf die Implementierungstechnologie abgebildet. Klassendiagramme in der Sichtweise Design stellen dar, wie das Sys­tem technisch aufgebaut sein muss, damit es die in der Analyse geforderten Eigen­schaften realisieren kann. Die in der Systemanalyse erkannten und dokumentierten Strukturen werden um die Informationen, die nötig sind um das fachliche Modell zu implementieren, erweitert.

Im Design wird die Implementierungssprache festgelegt. Es wird definiert wie Assoziationen zu implementieren sind; die Art und Weise wie die Instanzen der Klassen verwaltet werden, wird festgelegt. Die Persistenzschicht wird modelliert, d. h. es wird definiert, wie die Klassen auf eine Datenbank abgebildet werden; die Datenbank wird ausgewählt. In der Regel werden bei der Implementierung eines Modells Klassenbibliotheken verwendet, deren Verwendung im Klassenmodell dokumentiert werden muss. Die Benutzeroberfläche muss eingeführt werden.

## Zusammenhang

Klassen werden in fast allen UML-Diagrammen verwendet. Die Klassen des Klassendiagramms wirken sich deshalb auf alle anderen Diagramme aus und sind mit den anderen Diagrammen eines Modells konsistent zu halten.


## Hinweise für die Praxis

## Klassen identifizieren

Die UML definiert eine umfangreiche Notation zur Modellierung von Software­systemen. Vor der Modellierung der Struktur von Softwaresystemen müssen je­doch aus natürlichsprachigen Dokumentationen der Anforderungen an Systeme die enthaltenen fachlichen Objekte identifiziert werden. Alle Klassen, die den Pro­blembereich für eine geplant Anwendung beschreiben, sind fachliche Klassen. Diese Klassen beschreiben die wichtigsten Merkmale der Anwendung.

Wie findet man die in einem Text die enthaltenen Klassen? Es gibt zwei Techniken, die hier kurz skizziert werden.

 

## Substantivmethode

Rumbaugh empfiehlt in die Substantiv-Methode zur Identifikation von Klassen. Aus den Anforderungsdefinitionen an ein geplantes System werden alle Substantive markiert. Diese Begriffe sind potenzielle Klassenkandidaten. Da­nach werden redundante Begriffe eliminiert. Alle Begriffe, die auf die technische Realisierung der Begriffe hindeuten werden beseitigt. Durch diese kritische Analyse der Texte erhält man eine Menge Begriffe, die als Klassen im geplanten System verwendet werden können.

 

## CRC-Methode

CRC bedeutet Class, Responsibility, Collaboration und bezeichnet eine Technik bei der für jede potenzielle Klasse eine Karteikarte angelegt wird, die drei Ab­schnitte enthält:

class – Klassennamen

resposibility – Zuständigkeit

collaboration - Zusammenarbeit

 

Für jede Klasse wird der Klassenname notiert. Im Abschnitt Zuständigkeit wird beschrieben für welchen Zweck die Klasse eingeführt wurde, und unter Zu­sammenarbeit wird angegeben mit welchen anderen Klassen sie zusammenarbei­tet.

Die Substantivmethode und die CRC-Methode können auch kombiniert verwendet werden, indem man die Substantivmethode zum Auffinden der Klassen verwendet und die Klasseneigenschaften danach mit CRC-Karten (oder einem Texteditor) beschreibt.

 

##Attribute identifizieren

Attribute sind die Eigenschaften der Klassen. Attribute sollten nur von der Klasse zu der sie gehören abhängig sein. Bei der Suche nach Attributen muss die Frage beantwortet werden: Was muss die Klasse über sich selbst wissen, damit sie arbei­ten kann? Die Adjektive in der Anforderungsdefinition sind Kandidaten für At­tribute.

 

##Operationen identifizieren

Operationen sind die öffentlich aufrufbaren Funktionen einer Klasse. Operationen sind die Schnittstellen einer Klasse, über die sie die Dienste, die sie implementiert, allen anderen Klassen des Systems anbietet.

 

##Assoziationen identifizieren

Objekte kommunizieren über Assoziationen miteinander. Bei der Suche nach Assoziationen muss die Frage gestellt werden: Welche Objekte kommunizieren miteinander? In einem Projekt sind aber nur die Assoziationen zu modellieren, die zur Lösung des gestellten Problems benötigt werden. Die Verben in der An­forderungsdefinition geben Hinweise auf mögliche Assoziationen.

 

##Vererbungsstrukturen identifizieren

Bei der Suche nach Vererbungsstrukturen sucht man gemeinsame Eigenschaften von Klassen, die in einer Oberklasse zusammengefasst werden können. Die Unter­klasse muss alle geerbten Eigenschaften verwenden. Vererbung liegt dann vor, wenn eine Klasse eine Speziallfall einer anderen Klasse ist. Zwischen Oberklasse und Unterklasse besteht immer eine "ist-ein" Beziehung.

 

##Style Guide

Vererbungshierarchien sollten von oben nach unten angeordnet werden. Unter­klassen sollten unterhalb ihrer Oberklasse stehen.

Kreuzungen zwischen Beziehung sollten minimiert werden.

Wird ein Klassendiagramm zu groß für eine Seite (einen Bildschirm), sollte es über mehrere Seiten in Teildiagramme verteilt werden. Für die Aufteilung der Klassen in Teildiagramme sollten fachliche Kriterien herangezogen werden.

Beispiel

Die nachfolgende Abbildung zeigt das Klassendiagramm zu dem Mensa-Beispiel. Die "MensaKarte" wird von einer abstrakten "H_Da_Karte" abgeleitet. Das Attribut "ID" der "H_Da_Karte" hat die Sichtbarkeit protected und wird an die "MensaKarte" vererbt. "MensaAutomat" und "Kasse" stehen jeweils über Aggregationen in Be­ziehung zu den angegebenen Klassen. "Display" und "Kartenleser" sind Teil von zwei Klassen. Da das Beispiel ein Analysemodell darstellt, sind nur Analyseeigenschaften dargestellt. Es sind keine Elemente modelliert, die sich auf die Implementierung beziehen.


#Top Down / Bottom up

##Top-Down-Entwurf

Bereits bei der Einführung der Algorithmen wurde angesprochen, dass eine Lösungsstrategie darin besteht, das Problem über mehrere Stufen immer wieder in Teilprobleme zu zerlegen, bis diese überschaubar werden und sich schließlich Lösungen finden lassen.
In der Informatik hat sich für diese Technik der Begriff "Top-Down-Entwurf" eingebürgert. Ausgedrückt wird diese Methode auch in dem bekannten Satz "teile und herrsche", also gewissermaßen **unterteile das Problem solange, bis du es beherrschst!**

Natürlich muss eine Programmiersprache hierfür Techniken bereitstellen, die es ermöglichen, ein Programm in Teile zu zerlegen. Genauer handelt es sich hier um Teilprogramme, die selbständig in einer evtl. nötigen Testumgebung geprüft werden können. Die anderen Teilprogramme werden für das einzelne Teilprogramm nicht benötigt.

Der Vorteil besteht darin, dass jedes Teilprogramm (Modul) für sich gestestet werden kann und beim "Zusammenbau" nur noch auf die Kommunikation der Module untereinander geachtet werden muss. Hierzu müssen Schnittstellen definiert werden, welche Daten und evtl. Anweisungen an das Modul weiterleiten und zurückliefern.

##Bottom up

Module bieten einen weiteren Vorteil:
Hat man einmal ein Problem gelöst und stelt sich dieses als Teil in einem anderen Problem, so kann auf das bereits erzeugte Modul zurückgegriffen werden. Man muss also ein bestimmtes (Teil-)Problem nicht mehrmals lösen.

Bereits vorhandene Module können also in andere Programme integriert werden. In deisem Fall spricht man auch vom "Bottum-Up-Entwurf".

Heute sorgt man dafür, dass ein Modul seine Daten selbst verwaltet, und ein Zugriff, sei es schreibend oder lesend, von außen nur über Kontrollmechanismen des Moduls selbst erfolgen kann.
Derartige Module nennt man auch Objekte.
In der objektorientierten Programmierung (OOP) beschäftigen wir uns mit dieser Technik. Die OOP geht allerdings weit über die reine Zerlegung eines Problems in Teilprobleme hinaus. **Das Augenmerk ist mehr auf die Wiederverwendbarkeit eines Objektes in beliebiger Umgebung gerichtet.
**



