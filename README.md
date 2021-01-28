# Binder Badge
https://mybinder.org/v2/gh/eddide/unit-testing-and-logging/HEAD

# Dokumentation zur Ausführung
1. Aktivieren des Links zu Binder
2. Öffnen des Pyhton-Notebooks "In_Out_Unit Test Ansatz-LogReg"
3. In der Toolbar unter "Kernel" "Restart & Run All" aktivieren. --> Bestätigen des Pop-up Fensters mit "Restart and Run All Cells"
4. Ergebnisse von my_logger vergleichen
5. Ergebnisse von my_timer abgleichen

## Notebook Inhalt inkl. Einbindung des Input-Output Unit Tests
### Libraries Import
zuerst werden die relevanten Libraries importiert
- pandas
- numpy
- matplotlib
- seaborn
### Daten Import und Überprüfung
dann werden die Daten importiert und überprüft
- Anzeigen der Daten
- Information der Daten
- Beschreibung der Daten
### Explorative Datenanalyse
Verwendung unterschiedlicher Visualisierungen um die Daten zu erforschen
- Histogramm
- Jointplot
- Pairplot
## Erstellen der Dekoratoren
- Erstellen des Loggers **my_logger**, der für jede Funktion ein Dateiprotokoll erstellt, in dem jede Zeile die Parameter der Funktion enthält, jedes Mal, wenn die Funktion ausgeführt wird.
- Erstellen eines Loggers **my_timer**, der die Zeit protokolliert, die für die Ausführung der Funktion benötigt wurde.

### Aufsplitten der Daten in Trainings- und Testdaten:
Aufplitten der Daten mit train_test_split
- Trainingsdaten 66% des Datensatzes
- **Testdaten** 33% des Datensatzes
- Die Prädiktoren des Testdatensatzes sind somit in **X_test** und die Zielvariable in **Y_test** gespeichert

## Class TheAlgorithm
Implementierung des Algorithmus zur Anwendung der Dekoratoren in der logistischen Regression der Test-und Trainingsdaten
- bei "fit" wird die logistische Regression anhand der Trainingsdaten trainiert
- bei "predict" wird die logistische Regression auf die Testdaten angewendet

## Evaluation der Ergebnisse
- das fitten sollte in weniger als 0,1 Sekunden abgeschlossen sein
- die **Accuracy** des Modells auf die Trainingsdaten sollte bei ca. 90% liegen
- der **classification report** der Vorhersage der Testdaten sollte einen Recall von 96 und 85%, sowie einen F1 Score von 91 und 90% ausgeben
- ein Abgleich des classification reports mit demjenigen des herkömmlichen Ansatzes sollte keine, bzw. nur geringe Abweichungen anzeigen.
- die prediction sollte ebenfalls wie das fitten in weniger als 0,1 Sekunden abgeschlossen sein
- die **Accuracy** des Modells auf die Testdaten sollte bei ca. 91% liegen.
- die **confusion matrix** kann hier ebenfalls mit der confusion matrix des herkömmlichen Ansatzes überprüft werden --> hier sollte es keine, bzw. nur geringe Abweichungen geben.

## Bildschirmausgabe:

![Bildschirmausgabe](https://raw.githubusercontent.com/eddide/unit-testing-and-logging/main/Bildschirmausgabe.PNG)


### Logistische Regression nach dem herkömmlichen Ansatz:
Anwenden der logistischen Regression zur Vorhersage der Kategorie
- Trainieren und Fitten des Modells auf den Datensatz
### Evaluation der Vorhersage
Evaluierung über den classification report.
Es sollten ähnliche Ergebnisse wie diese angezeigt werden:
- accuracy: 91%
- reall: 96 und 85%
- f1-score: 91 und 90 %
