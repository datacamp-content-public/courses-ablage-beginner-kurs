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
