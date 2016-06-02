# BLD

# Assignment 1: Big Data in Ihrem Umfeld (4 Punkte)
## 1.1 (2 Punkte)
> Schauen Sie sich in Ihrem Umfeld um. FH Technikum oder Ihr Job. Nennen Sie mindestens ein Beispiel für Daten, die schemalos (unstrukturiert) sind und mindestens ein Bespiel für Daten, die strukturiert (schematisch) sind.

unstrukturierte Daten: localStorage im Browser (teilweise), diverse Key-Value Stores, bestimmte Userdaten
strukturiert Daten: Speichern von relationalen Investitionsdaten, IIS Logs


## 1.2 (2 Punkte)
> Nennen Sie ein Beispiel für Daten in Ihrem Umfeld, die gestreamt verarbeitet werden, nennen Sie ein Beispiel für Daten in Ihrem Umfeld, die über Batchverarbeitung verarbeitet werden.

gestreamt: Email-Benachrichtungen bei HTTP 500 Fehlern
batch: Datenverarbeitungs-Routinen zum Laden neuer IST-Datenstände aus einer Schnittstelle


# Assignment 2: Big Data in Ihrem Umfeld (4 Punkte)
>Entscheiden Sie sich für eine Data Engineering Plattform. Apache Flink oder Apache Spark. Installieren Sie die auf Ihrem Arbeitsgerät.
* 1 Punkt: Erklären Sie ihre Entscheidung
* 2 Punkte: Schicken Sie einen Screenshot der installierten Umgebung mit
* 1 Punkt: Beschreiben Sie Ihre Toolchain, die Sie mit dem Framework nutzen würden (z.B:
IDE)

Ich habe mich für Apache Flink entschieden, da ich bereits Erfahrung mit SQL habe und diese Sxntax der teils sehr komplexen map-reduce Abfragen vorziehe.
Wenn ich allerdings doch map-reduce Code verwenden möchte, so unterstützt Flink diesen. Allerdings muss den Benutzern von Flink auch klar sein, dass man
damit nicht Hadoop ersetzen kann - das HDFS, YARN und MapReduce (das Framework) sind unabdingbar.

http://stackoverflow.com/questions/28082581/what-is-the-difference-between-apache-spark-and-apache-flink

Der Screenshot der Umgebung liegt im Repository unter `apache flink.png`

Als IDE würde ich Intellij IDEA + die bereits installierte Umgebung von Apache Flink sowie Maven verwenden.

http://dataartisans.github.io/flink-training/devSetup/handsOn.html

# Assignment 3: Big Data in Ihrem Umfeld (4 Punkte)
>Schreiben Sie ein simples Program mit dem Framework (z.B. Helloworld) und laden Sie es hoch.
* 2 Punkte für Programm
* 2 Punkte, wenn das Programm auch ausführbar ist.

Der Source Code zum Programm ist unter `flink-java-project`zu finden. Das .jar zum Upload für Apache Flink ist unter `flink-java-project/target/flink-java-project.jar` und muss folgendermaßen ausgeführt werden.


1. "Submit new Job" - http://localhost:8081/#/submit
2. "Add new" - Das .jar auswählen
3. Bei "Entry Class", `org.apache.flink.quickstart.WordCount` eintragen
4. Mit "Submit" den Task starten
