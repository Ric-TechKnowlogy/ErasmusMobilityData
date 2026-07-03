# Analisi Mobilità Erasmus – Piano di Lavoro

 Durata totale: circa 20 minuti

---

## 0. Obbiettivo del progetto

Durata: 2 minuti

- Analisi della partecipazione degli universitari europei al progetto Erasmus+. Qui 20s su Erasmus+, poi dritto ai dati.

- Identificare il dataset di interesse:
  - Spiegare la fonte del dataset (European Commission) [https://erasmus-plus.ec.europa.eu/resources-and-tools/statistics-and-factsheets/statistics/for-researchers]
  - % di studenti rispetto al totale degli usufruitori di Erasmus+. (Pie chart)

- Porre le domande a cui vogliamo trovare risposta:
  - Salute del progetto Erasmus in contesto universitario(Come performa? Va espandendosi? Impatto di Covid-19?)
  - Atenei più partecipativi
  - Genere e istruzione superiore

perchè queste domande? Perchè possiamo replicarle su tutti i livelli.
---

## 1. Pulizia e Preparazione dei Dati

### Attività
Durata: 4 minuti

- Mostrare la struttura del dataset (piazzare un df.head / columns)

- Operazioni per pulizia dataset: 
  - Fare il merge dei dataset per gli ultimi 10 anni.
  - Droppare una serie di colonne.

- Filtraggio del dataset:
  - Filtrare per Activity, così da prendere solo per studenti universitari

- Standardizzazione:
  - Rinominare alcune colonne per aggiustare delle inconsistenze tra i dataset.
  - Identiicare sigle delle università di interesse (es. **UNIMI → UMIL**)
  - Ricondurre a dipartimenti le singole voci dei corsi

- Risultato della sezione: dataset pronto all'esplorazione ed alle visualizzazioni.

---

## 2. Analisi Esplorativa e Visualizzazione

Durata : 12 minuti

### 2.1 Livello europeo ~ 3 minuti

  - Analisi di alcune feature di interesse per le domande. (annessi plot) e.g Analisi temporale partecipazione al programma (line plot) - > Domanda 1
  - Confronto tra Paesi partecipanti (chloropath map) (dipendentemente da cosa confrotiamo, anche serie storiche con line plot) -> Feature specifica di questo livello
  - Mostrare i principali flussi tra **Paese di origine → Paese di destinazione** (connection map)
  - Atenei più partecipativi a livello europeo ((heatmap)[https://python-graph-gallery.com/heatmap/], distingue per ogni nazione il più attivo )-> Domanda 2
  - Gender e partecipazione lato europeo ((multi histogram) [https://python-graph-gallery.com/506-histogram-with-small-mutliples/]) -> Domanda 3


### 2.2 Livello italiano ~ 3 minuti

  - Analisi di alcune feature di interesse per le domande. (annessi plot) e.g Analisi temporale partecipazione al programma (line plot) - > Domanda 1
  - Confronto tra Atenei partecipanti (chloropath map) (dipendentemente da cosa confrotiamo, anche serie storiche con line plot) -> Feature specifica di questo livello
  - Atenei più partecipativi a livello italiano ((heatmap)[https://python-graph-gallery.com/heatmap/], distingue per ogni nazione il più attivo )-> Domanda 2
  - Gender e partecipazione lato italiano ((multi histogram) [https://python-graph-gallery.com/506-histogram-with-small-mutliples/]) -> Domanda 3


### 2.2 Livello UMIL ~ 2 minuti

  - Analisi di alcune feature di interesse per le domande. (annessi plot) e.g Analisi temporale partecipazione al programma (line plot), peso di UNIMI sul totale studenti Erasmus nazionali -> Domanda 1
  - Confronto tra i CdL partecipanti (histogram) -> Dobbiamo vedere quanti CdL diversi saltano fuori. Potremmo dover raggruppare per Facoltà
  - Mostrare i principali flussi tra **Paese di origine → Paese di destinazione** (connection map)
  - Gender e partecipazione lato ateneo (histogram) -> Domanda 3

Fare visualizzazioni sia con dati dell'ultimo anno che con i dati di tutti e 10 gli anni combinati.
Le valutazioni nell'arco temporale del programma useranno i dati cumulativi, quelle puntuali su domanda 2 e 3 useranno i dati dell'ultimo anno a nostra disposizione.

---

## 3 Conclusioni e Sviluppi Futuri

Durata : 2 minuti

- Resoconto dell'analisi effettuata
- Indicare eventuali criticità emerse come qualcosa su cui lavorare (e.g super stupido, Italia fa poco STEM)
- Indicare possibili espansioni dell'analisi (coff coff analisi CdL per tutti)
  - Analisi comparativa per corsi, distribuzione nazionale vs UNIMI
  - Analisi comparativa con altri atenei europei


---









## 2.3 Analisi Temporale

- Studiare l’evoluzione nel tempo (2019–2024)

### Attività
- Costruzione serie storica
- Analisi trend:
  - Evoluzione flussi
  - Identificazione paesi “migliori” e “peggiori”

- Approfondimenti:
  - Impatto del COVID-19 sulla crescita del progetto ERASMUS

- Visualizzazioni:
  - Serie temporali con linea di regressione

---

## 3. Visualizzazioni Chiave

- **Choropleth map (Italia)**
  - Evidenziare i **top 5 atenei** sulla mappa e confrontarli con UMIL

- Altri grafici:
  - Flussi
  - Distribuzioni per area di studio/dipartimento
  - Outlier rispetto al trend generale (e.g atenei che si distinguono per il dipartimento in cui ricevono più studenti)

---

## 4. Struttura del progetto

L'idea è di eseguire delle analisi e riproporle su diversi livelli, arricchendole con altre ad ogni discesa di livello:

- Globale
- Italia
- UNIMI (UMIL)

Uso di tecniche di visualizzazione differenti, quando opportuno.

---

## 5. Struttura della Presentazione

### 5.1 Introduzione
- Overview programma Erasmus
- Numeri principali
- Confronto tra paesi (IT, ES, FR, DE)
- Valutare la distribuzione dei corsi di laurea per paese
- Valutazione di elementi interessanti come  la durata rispetto al dipartimento, distribuzione dei sessi per corso di laurea

### 5.2 Italia
- Evoluzione nel tempo
- Mete preferite
- Dipartimenti più coinvolti

### 5.3 UNIMI
- Posizionamento
- Confronti con altri atenei italiani
- Insight principali
- I dati riportati da UNIMI son corretti? 
- Mostrare la differenza tra la distribuzione nazionale inter-corsi e quella in UNIMI
- Verificare l'impronta di Unimi sul totale degli studenti ERASMUS rispetto ad altre università italiane e/o milanesi.

---

## 6. Fasi di lavoro

### 1. Data Preparation
- Pulizia dati
- Merge dataset
- Feature engineering

### 2. Data Visualization
- Scelta metriche
- Progettazione visualizzazioni

### 3. Presentazione Finale
- Storytelling
- Costruzione slide
