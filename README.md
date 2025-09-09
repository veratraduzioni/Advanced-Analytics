# Progetto Titanic
Creare un modello di machine learning in grado di prevedere se un passeggero del Titanic sarebbe sopravvissuto o meno al tragico naufragio, in base a caratteristiche come età, sesso, classe di viaggio e altre variabili disponibili nel dataset.<br><br>
<b>Esplorazione del dataset:</b>
- Impostazione nuovo indice
- Controllo colonne con valori null
- Calcolo percentuali passeggeri sopravvissuti e non
- Heatmap delle correlazioni
- Analisi tipologie passeggeri sopravvissuti per sesso e classe di imbarco
- Analisi tipologie passeggeri sopravvissuti in base all’età e relative statistiche comparando l’età con le altre categorie
<br><br>
<b>Preprocessing dei dati:</b>
- Separazione features e target
- Split 1: train 75% e test 25%
X_train (668, 4)
X_test (223, 4)
y_train (668,)
y_test (223,)
- Split 2: validation 25% del train
X_train_sub (501, 4)
X_val (167, 4)
y_train_sub (501,)
y_val (167,)
- Sostituzione valori nulli colonna Embarked: scenario A con moda, scenario B con eliminazione dei valori null ⟶ column transformer, pipeline e cross validation con gridsearch CV
- Sostituzione valori nulli colonna Age: scenario A con mediana generale, scenario B con mediana raggruppata per Sex e Pclass ⟶ column transformer, pipeline e cross validation con gridsearch CV
- Encoding colonne con dati categorici in dati numerici
<br><br>
<b>Addestramento del modello:</b>
- Algoritmo: DecisionTreeClassifier
- Parametri testati profondità dell’albero: 2, 5, 10, 25, None
- Metrica di valutazione: Accuratezza
- Cross validation con GridSearch
- Addestramento del modello
- Validazione sull’albero con profondità 5

# Progetto Advanced Analytics con start2impact
Dataset sulle vendite effettuate da una catena di supermercati. Analisi dati per capire quali sono le città in cui potenzialmente effettuano più introiti, quali sono le categorie che portano maggior valore e se il sesso dell’acquirente fa differenza o meno, sviluppando un modello di machine learning che riesce a predire la redditività attesa di un determinato acquisto.<br>
Analisi verticale del prodotto delle mele: classificazione in base alla qualità e decidere quale potrebbe generare maggiori vendite.<br>
Analisi degli utili nel tempo e costruzione di un semplice modello per predirne l’evoluzione e capire qual è il trend di fondo: se il fatturato dell’azienda sta crescendo o meno, oppure se i profitti sono stazionari.<br><br>
<b>Passaggi del progetto:</b>
- Esplorazione del dataset: calcolo delle statistiche, distribuzione valori nella label
- Preprocessing: encoding variabili categoriche, feature scaling, training e test split
- Predizioni: linear regression, polynomial regression, logistic regression, decision tree, k-means clustering, time series
