# Schreibtischtest 

Der Schreibtischtest ist ein Verfahren, das im Bereich der Softwareentwicklung verwendet wird, um Algorithmen oder Routinen auf Richtigkeit zu prüfen. Der Schreibtischtest wird nicht mit Hilfe eines Rechners durchgeführt, sondern vielmehr im Kopf des Entwicklers. Dazu werden für einen deterministischen und terminierenden Programmablauf eine Eingabe- und eine mögliche Ausgabemenge festgelegt. Anschließend wird mit jedem Element der Eingabemenge durch schrittweises Durchrechnen die Korrektheit des Programmablaufs überprüft. Der gewählte Programmablauf verhält sich für das gewählte Eingabeelement genau dann korrekt, wenn das ausgegebene Element, also das Ergebnis, Teil der Ausgabemenge ist.

Die Tatsache, dass die Eingabemenge für einen Algorithmus beliebig groß sein kann, z. B. eine Untermenge der natürlichen Zahlen, erfordert vom Entwickler zur Überprüfung der Korrektheit des zu testenden Programms die schrittweise Durchrechnung mit allen Elementen der Eingabemenge. Gibt es für die Eingabemenge keine obere oder untere Schranke, dann kann der Schreibtischtest höchstens mit einigen plausiblen Eingaben ein Indiz dafür liefern, dass der Algorithmus richtig implementiert wurde.

Voraussetzungen für den Schreibtischtest sind also ein deterministischer und terminierender Programmablauf, die Kenntnis über plausible und sinnvolle Eingabeelemente, und die Kenntnis der zu den Eingabeelementen passenden Ausgabeelemente, um aus der jeweiligen Ausgabe auf die Richtigkeit schließen zu können. Das Ergebnis für die jeweilige Eingabe muss also bekannt sein.

