# Online Retail EDA - Customers \& Sales Analysis



## Obiettivi:

Questo progetto analizza le transazioni di un e-commerce inglese, realizzate tra il 01/12/2010 e il 09/12/2011, con l'obiettivo di comprendere l'andamento delle vendite, il comportamento dei clienti e i prodotti più richiesti sul mercato.

In particolare, vengono analizzate:

* le transazioni effettuate, con un focus su quantità richieste, prezzi unitari e valore medio di spesa
* l'impatto delle vendite nel tempo
* la distribuzione del fatturato per nazione e continente
* i prodotti più venduti
* la clientela, attraverso Pareto Analysis e RFM Score



## Dataset:

Il dataset utilizzato è Online Retail.xlsx e si compone di:

* 541.909 righe, 8 colonne
* 1.454 valori mancanti in *Description* e 135.080 in *CustomerID*
* 5.268 righe duplicate
* Le colonne *Quantity* e *UnitPrice* presentano valori negativi e outlier

Nella sezione Data Cleaning:

* è stata creata una copia del dataset
* sono state eliminate le righe duplicate
* i valori mancanti nella colonna *Description* sono stati sostituiti con *MISSING*
* sono state escluse le righe con *Quantity* e *UnitPrice* entrambe negative

Successivamente, sono state create nuove colonne, quali *Continent*, *TotalPrice*, *Year*, *Month*, *Day* e *DayName*, per integrare le feature necessarie all'analisi del dataset.



## Risultati principali:

Durante il periodo oggetto di analisi, l'azienda ha fatturato quasi 11 milioni di sterline, ha registrato circa 4.500 clienti, ha emesso meno di 21.000 fatture e ha venduto circa 3.900 prodotti diversi. Dall'analisi aggregata delle varie transazioni, viene fuori una distribuzione fortemente asimmetrica a destra, in quanto l'azienda ha emesso tante fatture con bassi importi.

Nel mese di novembre 2011 le vendite registrano un picco significativo, con un aumento progressivo dal mese di ottobre. A livello settimanale, si evidenza che l'attività lavorativa è costante nei giorni lavorativi, è minore, seppure presente, di domenica e risulta assente il sabato.

L'attività dell'azienda si focalizza nel proprio paese di origine, dove si concentra l'85% del fatturato prodotto e dove risiedono il 90% degli acquirenti. Tuttavia, dall'analisi della spesa media per nazione, emerge che l'Inghilterra è al 20° posto nella classifica, superata significativamente da Irlanda, Paesi Bassi, Singapore e Australia.

L'analisi condotta sui prodotti non evidenzia best seller degni di nota: si pensi che i top 10 prodotti più venduti per quantità e fatturato incidono per un 10% sul fatturato globale dell'azienda.

Lato clientela, l'analisi dei top 10 spender ha evidenziato che realizzano meno del 20% del fatturato globale. La distribuzione delle vendite per cliente è anch'essa asimmetricamente positiva, con una lunga coda a destra dove si ritrova quel ristretto numero di clienti con livelli di spesa significativamente superiori alla media. Dalla Pareto Analysis, viene fuori che l'80% del fatturato è generato dal 25-30% dei clienti.

L'ultima analisi condotta è stata quella inerente al RFM Score, dove ogni cliente è stato classificato per frequenza d'ordine, volume di acquisto e capacità di spesa. Sono 11 le categorie riconosciute, e vanno da *Champion* (quella con lo score più alto) a *Lost* (ossia quei clienti ormai persi).



## Approfondimenti chiave:

* Il fatturato presenta una distribuzione right-skewed, con una prevalenza di fatture di importo contenuto e pochi ordini di valore elevato
* L'85% del fatturato è prodotto dal mercato locale (Regno Unito)
* Nonostante la concentrazione nel Regno Unito, l'Irlanda risulta essere il paese con la più alta spesa media per cliente, mentre l'Inghilterra si colloca alla 20° posizione
* Il fatturato è fortemente concentrato: lo 0,2% dei clienti genera circa il 17% del fatturato totale
* L'80% del fatturato complessivo è prodotto da circa il 25-30% della clientela
* 540 clienti risultano classificati come *Champion* secondo il modello RFM



## Tools:

* Python
* Pandas
* NumPy
* Matplotlib
* Jupyter Notebook



## Struttura del repository:

```

online-retail-eda/

├── data/

│   └─ Online Retail.xlsx

│

├── notebooks

│   └─ online\_retail\_eda.ipynb

│

├── .gitignore

├── README.md

└── requirements.txt

```
