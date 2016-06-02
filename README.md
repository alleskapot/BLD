# BLD

# Assignment 1: Big Data in Ihrem Umfeld (4 Punkte)
## 1.1 (2 Punkte)
> Schauen Sie sich in Ihrem Umfeld um. FH Technikum oder Ihr Job. Nennen Sie mindestens ein Beispiel für Daten, die schemalos (unstrukturiert) sind und mindestens ein Bespiel für Daten, die strukturiert (schematisch) sind.

__unstrukturierte Daten__: localStorage im Browser (teilweise; zumindest Key-Value Prinzip), diverse Key-Value Stores

__strukturiert Daten__: Speichern von relationalen Daten, IIS Logs


## 1.2 (2 Punkte)
> Nennen Sie ein Beispiel für Daten in Ihrem Umfeld, die gestreamt verarbeitet werden, nennen Sie ein Beispiel für Daten in Ihrem Umfeld, die über Batchverarbeitung verarbeitet werden.

__gestreamt__: Auswertung von Nutzerstatistiken nach verschiedenen Kriterien

__batch__: Datenverarbeitungs-Routinen zum Laden neuer Datenstände aus einer Schnittstelle


# Assignment 2: Big Data in Ihrem Umfeld (4 Punkte)
>Entscheiden Sie sich für eine Data Engineering Plattform. Apache Flink oder Apache Spark. Installieren Sie die auf Ihrem Arbeitsgerät.
* 1 Punkt: Erklären Sie ihre Entscheidung
* 2 Punkte: Schicken Sie einen Screenshot der installierten Umgebung mit
* 1 Punkt: Beschreiben Sie Ihre Toolchain, die Sie mit dem Framework nutzen würden (z.B:
IDE)

Ich habe mich für Apache Flink entschieden, da ich bereits Erfahrung mit SQL habe und diese Syntax der teils sehr komplexen map-reduce Abfragen vorziehe.
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

# Data Science

## Assignment 1: Technologien (4 Punkte)
>
1. (2 Punkte)
Sie haben in der LVA zwei Frameworks kennengelernt (R und Python). Nennen Sie zwei weitere Technologien, um Daten zu analysieren (müssen nicht open source sein)
2. (2 Punkte)
Sie bekommen den Auftrag, sich mit einer Data Science Technologie zu arbeiten. Nennen Sie Technologie, die ihnen auf dem ersten Blick am besten für Sie ersscheint und begründen Sie das!

1. MATLAB, Julia
2. Ich würde mich auf R spezialisieren, da es im Jahr 2015 eine der am meisten verwendeten Technologien im Data Science Bereich ist. Daher wird die Community auch dementsprechend gut sein, sowie viele Plugins etc. zur Verfügung stehen. Siehe: http://www.datasciencecentral.com/profiles/blogs/what-technology-tool-skills-do-data-scientists-jobs-require

## Assignment 2: Technologien (4 Punkte)
>Entscheiden Sie sich für eine Data Science Plattform. R oder Python Installieren Sie die auf Ihrem Arbeitsgerät.
* 1. Punkt: Begründen Sie ihre Entscheidung (Warum ziehen Sie persönlich aus ihrer Ausgangssituation die eine Technologie der anderen vor).
* 2. Punkte: Schicken Sie einen Screenshot der installierten Umgebung mit
* 1. Punkt: Beschreiben Sie Ihre Toolchain, die Sie mit dem Framework nutzen (z.B. IDE)

1. Ich verwende Python, weil ich in dieser Sprache mehr Vorwissen habe und daher die Zeit zum Einlernen geringer ist. Zusätzlich dazu ist Python darauf bedacht komplexe Operationen in der Umsetzung sehr einfach zu halten, das finde ich sympathisch.
2. Zu finden unter `python.png`
3. Hier würde ich auf einen etwas abgespeckteren Editor wie Atom oder VS-Code zurückgreifen, die beide auch eine sehr gute Integration von Python (mittels Plugins) haben.

## Assignment 3: Big Science (4 Punkte)
>Der Cheatsheet auf http://scikit-learn.org/stable/tutorial/machine_learning_map/ ist eine einfache Anleitung, wie man den richtigen Algorithmus zum richtigen Data Science Problem findet.
Schauen Sie in Google nach und lernen Sie classificatiom, regression, clusting und dimensional reduction unterscheiden.
Nennen Sie ein Beispiel aus ihrem Umfeld, wo Sie mit dem Algorithmus zu tun haben. Das kann ein Beispiel sein, wie: Wenn Sie bei Amazon einkaufen. Wenn Sie von einem Marketinginstitut angerufen werden, etc.

* __classification__
  Hierbei werden diverse Inputs in zwei oder mehr Klassen unterteilt. Wenn diese Zuteilung nicht möglich ist, so muss dem System ein Model beigebracht werden, zum richten klassifizeren. Ein typisches Beispiel wären Spam-Emails.
* __regression__
  Hierbei handelt es sich ebenso um ein Problem, bei dem es einen "Lehrer" für das System benötigt. Es wird allerdings mit kontinuierlichen Daten gearbeitet. Ein Beispiel wäre ein Shop, der schon Läden in mehreren Städten hat, aber sich noch nicht sicher ist, wo sie den nächsten eröffnen sollen. Mit der Regression könnte man mit Eingabe von bestimmten Parametern den geschätzten Umsatz in der jeweiligen Stadt berechnen.
* __clustering__
  Hierbei werden diverse Inputs in Gruppen unterteilt. Im Unterschied zur calssification sind diese Gruppen zuvor nicht bekannt und dadurch ist hier kein "Lehrer" bzw. Supervisor notwendig. Ein Beispiel wäre eine Marktanalyse, welche bestimmte (persönliche oder globale) Trends während des Shoppens auf Amazon herausfindet.
* __dimensional reduction__
  Hierbei werden Inputs vereinfacht, indem sie in "einfachere" Dimensionen gemappt werden. Ein typisches Beispiel wäre, wenn ein bestimmter Text gegeben ist, einen ähnlichen zu finden.
