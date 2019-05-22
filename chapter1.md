---
title: 'Chapter Title Here'
description: 'Chapter description goes here.'
---

## Rechnen mit R

```yaml
type: NormalExercise
key: 660cfa4cd9
xp: 100
```

Rechnen mit R:
In seiner grundlegendsten Form kann R als ein einfacher Rechner verwendet werden. Beachten Sie folgende Rechenoperatoren:	
	
    Addition: +
    Subtraktion: -
    Multiplikation: *
    Division: /
    Potenzierung: ^
    Modulo: %%

Die letzten beiden Operatoren benötigen eine Erklärung:

	Der Potenzierungs-Operator (^) steigert die linke Zahl durch die Größe der rechten Zahl: Zum Beispiel 4^2 ist 16.
    Der Operator Modulo (%%) liefert den Rest durch die Division der linken Zahl durch die rechte Zahl, zum Beispiel 7 %% 2 ist 1.

Behalten Sie diese Informationen im Hinterkopf und befolgen Sie sie in den nachstehenden Aufgaben, um die Übung erfolgreich abzuschließen.

`@instructions`
1. Summieren Sie die Zahlen 23 46
2. Ziehen Sie von der Zahl 234 64 ab.
3. Multiplizieren Sie die Zahlen 222 und 59
4. Dividieren Sie 465 durch 3
5. Potenzieren Sie 2 hoch 5
6. Berechnen Sie 119 Modulo 13.
    
Klicken Sie nach dem Programmieren auf 'Submit Answer' und schauen Sie sich die R-Ausgabe in der Konsole an. 
Beachten Sie, wie das '#' Symbol in den R-Codes verwendet wird.

`@hint`
1. Achten Sie bitte auf die richtigen Operatoren und mögliche Tippfehler, da diese als Fehler ausgegeben werden.
2. Ein weiteres Beispiel für den Modulo Operator ist: 9 %% 2 gleich 1.

`@pre_exercise_code`
```{r}
#1 Addition

#2 Subtraktion

#3 Multiplikation

#4 Division

#5 Potenzierung

#6 Modulo

```

`@sample_code`
```{r}
#1 Addition

#2 Subtraktion

#3 Multiplikation

#4 Division

#5 Potenzierung

#6 Modulo
```

`@solution`
```{r}
#1 Addition
69
#2 Subtraktion
170
#3 Multiplikation
13098
#4 Division
155
#5 Potenzierung
32
#6 Modulo
2
```

`@sct`
```{r}
codeaddition <- c("23+46", "23+46")
codesubtraktion <- c("234-64")
codemultiplikation <- c("222*59")
codedivision <- c("465/3")
codepotenzierung <- c("2^5", "2*2*2*2*2")
codemodulo <- c("119%%13", "119-9*13")
ex() %>% check_code(c(codeaddition, codesubtraktion, codemultiplikation, codedivision, codepotenzierung, codemodulo), fixed = TRUE)
success_msg("Gute Arbeit! Yeah richtig gut gemacht!")
```

---

## Erzeugen von Vektoren

```yaml
type: NormalExercise
key: 89e5f5a7f6
xp: 100
```

Vektoren erzeugen und kombinieren:
- Ein Vektor ist die einfachste Datenstruktur in R. Als "einzelnes Objekt, das aus einer Ansammlung von Dingen besteht" wird ein Vektor im R-Handbuch definiert. Es ist die kleinstmögliche Dateneinheit in R (de Vries/Meys 2018). Wir behandeln hier zum Einstieg numerische Vektoren, also Vektoren, die alle Arten von Zahlen enthalten können.

Vektoren erzeugen: 

Um einen Vektor mit einer Folge von Zahlen von 1 bis 3 zu erzeugen und ihn zuzuweisen:  c(1,2,3) oder kürzer c(1:3)
- first_vec <- c(1:3).

`@instructions`
1. Erstellen Sie einen Vektor, der die Zahlen von 1 bis 6 beinhaltet und weisen Sie ihm bitte den Namen open.vec zu. Die Zahlen stehen jeweils für einen Verkaufstag (1= Montag).
2. In dem Vektor sell.time ist die Verkaufszeit für jeden Verkaufstag hinterlegt. Lassen Sie sich bitte den Vektor ausgeben, um zu bestimmen, welcher Verkaufstag der zeitlich längste ist.
3. Am Freitag wurden 5103 Euro Umsatz generiert. Wie viel wurde pro Stunde umgesetzt?
4. Berechnen Sie bitte die tägliche durchschnittliche (mean) Verkaufszeit pro Verkaufstag.

`@hint`
Schauen Sie sich die Beispiele an. Verwenden Sie diese Schreibweise: Variable <- (Zahl:Zahl)

`@pre_exercise_code`
```{r}
sell.time <- c(8,8,8,8,9,6)
```

`@sample_code`
```{r}

```

`@solution`
```{r}
#1. Erstellen Sie einen Vektor, der die Zahlen von 1 bis 6 beinhaltet und weisen Sie ihm bitten den Namen open.vec zu:
open.vec <- c(1,2,3,4,5,6)

#2. Berechnen Sie den Durchschnitt (mean) des Vektors sell.time und weisen Sie ihm bitte mean_time zu:
mean_time <- mean(sell.time)
```

`@sct`
```{r}
ex() %>% check_object("open.vec") %>% check_equal("c(1,2,3,4,5)", "c(1:5)")
ex() %>% check_object("mean_time") %>% check_equal("mean(sell.time)")
ex() %>% check_object("mean_time") %>% check_equal(8)
success_msg("Ja, genau - es sieht so aus als hätten Sie das Erzeugen von Vektoren verstanden! Die durschnittliche Arbeitszeit an den Arbeitstagen beträgt 7h") 
```

---

## Variablenzuweisung

```yaml
type: NormalExercise
key: 075b9b30a8
xp: 100
```

Variablenzuweisung

Ein grundlegendes Konzept in der (statistischen) Programmierung sind Variablen.

Eine Variable ermöglicht es einen Wert (z.B. 5) oder ein Objekt (z.B. Funktionsbeschreibung) in R zu speichern. Später können Sie den Namen der Variable nutzen, um einfach auf den Wert oder das Objekt zuzugreifen, die innerhalb dieser Variablen hinterlegt sind.

So können Sie der Variable my_var den Wert 5 zuweisen: **my_var <- 5**

`@instructions`
Ihre Aufgabe: 
Vervollständigen Sie bitte den Code im Editor, sodass der Variable x der Wert 105 zugeordnet wird. Schicken Sie dann die Antwort ab. 
Wenn Sie R nach x fragen, wird der vorher zu gewiesene Wert angezeigt.

`@hint`
Der Variable my_var wurde im Beispiel der Wert 5 zugeteilt. Orientieren Sie sich einfach an dieser Vorgehensweise.

`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}

```

`@solution`
```{r}
# Weisen Sie x den Wert 105 zu
x <- 105
# Geben Sie den Wert der Variable x aus
x
```

`@sct`
```{r}
ex() %>% check_object("x") %>% check_equal(105)
ex() %>% check_code(c("print(x)", "x"))
ex() %>% check_output("105", fixed=TRUE, missing_msg="So ist das nicht ganz richtig!")
success_msg("Ja, genau: x <- 105 erzeugt keine Ausgabe, weil R davon ausgeht, dass Sie diese Variable in der Zukunft benötigen! Gehen Sie bitte zur nächsten Aufgabe")
```

---

## Basisdatentypen in R

```yaml
type: NormalExercise
key: 9e06fa7a5f
xp: 100
```

R arbeitet mit zahlreichen Datentypen und ist sensitiv auf Groß-/Kleinschreibung. Einige der grundlegendsten Datentypen sind:

- Boolesche Werte oder auch als Wahrheitswerte bezeichnet (TRUE oder FALSE) werden auch 'Logical' genannt.
- Dezimalwerte (z.B. 3.4) werden 'numeric' genannt (z.B. )
- Zeichenketten und Buchstaben (Strings) ("Hallo") werden auch als 'character' bezeichnet.
- Kategorien (A,B,C) werden auch als 'factor' bezeichnet.

**Wichtig:** Zeichenketten werden in "Anführungszeichen" gesetzt.

`@instructions`
Von einer kleineren Tochtergesellschaft, die neu eröffnet hat, hat Herr Müller einen Kundendatensatz zugeschickt bekommen. Ihr Chef Herr Müller sagt, dass die Mitarbeiter dort noch nicht vertraut mit den Datentypen seien und Sie sich deswegen genau mit den Basisdatentypen beschäftigen müssen, damit die Mitarbeiter von Ihnen eine Vorlage bekommen können. 

1. Geben Sie den Wert von Anzahl_Mitarbeiter aus.
 
	Ändern Sie die Werte von:
 2. Variable my_numeric zu 13.
 3. Variable my_character zu der Zeichenkette universe.
 4. Variable my_logical zu FALSE.

`@hint`
```
1. Kommen Sie, einfach die Variable reinschreiben oder mit dem Operator print(Variable) ausgeben lassen.
```
```
2. Ersetzen Sie die Werte im Editor mit den Werten, die bei der Anweisung vorgegeben sind. 
Zum Beispiel: my_numeric <- 13 , um der Variable my_numeric den Wert 13 zuzuweisen.
```

`@pre_exercise_code`
```{r}
Anzahl_Mitarbeiter <- "Schmidt, Klaus"
Termin <- 2019-09-21
```

`@sample_code`
```{r}
# Ausgabe Anzahl_Mitarbeiter:

# Weisen Sie der Variablen Anzahl_Mitarbeiter den Wert 17 zu:

# Bennen Sie my_office mit der Zeichenkette Nordwand:

# Überprüfen Sie, ob Begrueßungstermin eine Datumsangabe ist:

```

`@solution`
```{r}
# Die Anzahl der Mitarbeiter müsste eine numerische Zahl. Überprüfen Sie dies bitte: 
is.numeric(Anzahl_Mitarbeiter)
# Ausgabe Anzahl_Mitarbeiter:
#print(Anzahl_Mitarbeiter)
# Weisen Sie der Variablen Anzahl_Mitarbeiter den Wert 17 zu:
#Anzahl_Mitarbeiter <- 17
# Weisen Sie my_office die Zeichenkette Nordwand zu:
#my_office <- "Nordwand"
# Überprüfen Sie, ob Begrueßungstermin eine Datumsangabe ist:
#is.Date(Begrueßungstermin)
```

`@sct`
```{r}
#ex() %>% check_code(c("print(my_nummerus)", "my_nummerus"), fixed = TRUE)
#ex() %>% check_output("3", fixed=TRUE, missing_msg="Da stimmt etwas nicht!")
#ex() %>% check_object("my_numeric")   %>% check_equal(54)
#ex() %>% check_object("my_character") %>% check_equal("universe")
#ex() %>% check_object("my_logical")   %>% check_equal("FALSE")
#success_msg("Ja, genau - es sieht so aus als hätten Sie die Basisdatentypen verstanden!")
```

---

## Matrizen

```yaml
type: NormalExercise
key: 8b667bb5d4
xp: 100
```

Matrizen sind rechteckige, zweidimensionale Anordnungen (Tabelle) von Elementen. In R können komplexe Matrixoperationen einfach und effizient durchgeführt werden. In der Statistik werden häufig Matrixberechnungen angewandt (de Vries/Meys 2018).
Anhand von Matrizen können Sie im Gegensatz zu Vektoren nun mehrere Zeilen in ein und derselben Tabelle (Matrix) speichern.

Vektoren in eine Matrix zusammenführen: 
- **rbind():** Funktion mit der Vektoren zu Zeilen ein und derselbe Matrix zusammengefügt werden können.
- *Matrix <- rbind(Vektor, Vektor)
- **cbind():** Funktion mit der Vektoren als Spalten einer Matrix zusammengefügt werden.

Um die Übersicht zu behalten und damit auch andere die Ergebnisse nachvollziehen können. Zeilen- und Spaltennamen sinnvoll verändern: 
- Zeilennamen verändern: Beispiel **rownames(Matrix)** <- c("Region", "Umsätze")
- Spaltennamen verändern: Beispiel **colnames(Matrix)** <- c("Januar", "Februar")

Werte einer Matrix ersetzen:
- Um den Wert in der dritten Zeile und zweiten Spalte der Matrix matrix.eins zu 5 zu ändern: matrix.eins[3,2] <- 5

`@instructions`
Herr Müller bittet Sie einen report.wochenverkaeufe für die Tochterfirma zu erstellen.

1. Ihre Aufgabe ist es eine Tabelle (Matrix) aus den Vektoren **sell.time und revenue.day** zu erstellen und der Variablen **report.wochenverkaeufe** zuzuordnen. Testen Sie, ob Sie es richtig gemacht haben mit der Ausgabe in der Console.

2.Sie haben den Report bei Herrn Müller abgeben. Er kommt auf Sie zu und entgegnet Ihnen, ob Ihnen aufgefallen sei, dass sich noch ein Zahlenfehler eingeschlichen hat. Kontrollieren Sie dies und ändern Ihn bitte ab.

- 2.1 Lassen Sie sich die Matrix report.wochenverkaeufe ausgeben.

- 2.2 Ändern Sie einen Fehler ab.

`@hint`


`@pre_exercise_code`
```{r}
#report.wochenverkaeufe <- matrix(1:18, ncol=6)
#sell.day <- c("Montag", "Dienstag", "Mittwoch", "Donnerstag", "Freitag", "Samstag")
sell.time <- c(8,18,8,8,9,6)
revenue.day <- c(2700, 3500, 4200, 4700, 5103, 3300)
average.byday <- c(2700/8, 3500/8, 4200/8, 4700/8, 5103/9, 3300/6)
```

`@sample_code`
```{r}
# report.wochenverkaeufe

# Ausgabe

# Änderung vornehmen

```

`@solution`
```{r}
#report.wochenverkaeufe <- matrix(1:18, ncol=6)
report.wochenverkaeufe <- rbind(sell.time, revenue.day)
# Ausgabe
print(report.wochenverkaeufe)
# Änderung vornehmen
report.wochenverkaeufe[1,2] <- 8
```

`@sct`
```{r}
ex() %>% check_code("report.wochenverkaeufe <- rbind(sell.time, revenue.day)", fixed=TRUE, missing_msg="Verwenden Sie bitte die Funktionen aus der Kontextbeschreibung!") 
success_msg("Ja, genau - Schauen Sie sich gern Ihre selbst erstellte Tabelle an!")
ex() %>% check_code("report.wochenverkaeufe[1,2] <- 8", fixed=TRUE, missing_msg="Sie haben den Fehler noch nicht richtig ausgebessert!") 
success_msg("Ja, genau - sonst wären falsche Umsatzzahlen an die Verkaufsniederlassung weitergegeben worden!")
```

---

## Data Frames

```yaml
type: NormalExercise
key: 80479aab8d
xp: 100
```

Bislang war immer von einem Vektor die Rede. Des Weiteren gibt es noch Matrizen, die sehr häufig Anwendung finden. Aufgrund der Kürze der Einführung in diesem Kurs kommen wir direkt zu **Data Frames**:

Datensätze bestehen sehr häufig aus unterschiedlichen Datentypen (Produktnamen, Preis, Datum der Herstellung). In eine Matrix bekommen Sie die Daten nur, wenn Sie alles in Text umwandeln, was die Auswertung erschwert. Geeigneter sind da Data Frames, ein Datenobjekt, in dem Sie alle Daten unterschielichen Typs speichern können (de Vries/Meys 2018).

- Struktur und Datentyp anzeigen lassen: **str()**
- Anzahl der Zeilen bzw. Spalten ausgeben lassen: **nrow() bzw. ncol()**

`@instructions`
Der Datensatz aus dem Unternehmen Bambergus, der aus der zentralen Kundendatenbank stammt, enthält verschiedene Kundeninformationen.
Der Datensatz wurde schon eingelesen und ist der Variable **Kundendaten** zugewiesen worden.

1. Was beinhaltet der Datensatz an Informationen, bzw. welchen Datentypen kommen vor?
2. Wie viele Kunden sind im Kundendatensatz aufgelistet, wenn Sie davon ausgehen, dass es keine doppelten Kunden gibt?

`@hint`


`@pre_exercise_code`
```{r}
Kundendaten <- read.csv2("https://assets.datacamp.com/production/repositories/5032/datasets/59b8181ca10c38e979057892346adb33736a2198/dataApr-1-2019.csv")
```

`@sample_code`
```{r}

```

`@solution`
```{r}

```

`@sct`
```{r}

```
