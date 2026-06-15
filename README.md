# Recommendation-System
## Multimodal Real Estate Agent: BLIP & LangGraph Recommendation System

Questo repository ospita un sistema di raccomandazione multimodale avanzato per il settore immobiliare. Il progetto unisce la computer vision (tramite modelli BLIP fine-tuned) e l'intelligenza artificiale generativa agentica (tramite LangGraph e vettorizzazione) per analizzare annunci immobiliari, generare descrizioni accurate a partire dalle immagini e guidare l'utente nella scelta dell'immobile ideale attraverso un approccio "human-in-the-loop".

---

## 🚀 Panoramica del Progetto

Il sistema risolve uno dei problemi principali della ricerca immobiliare: la discrepanza tra le immagini di un annuncio e le reali preferenze stilistiche dell'utente (es. amanti del *minimalismo scandinavo* o dei toni neutri). 

L'architettura si divide in due macro-componenti:
1. **Image Captioning (Computer Vision):** Un modello BLIP (Bootstrapping Language-Image Pre-training) ottimizzato tramite fine-tuning per riconoscere stili architettonici, elementi di design d'interni, palette di colori e condizioni degli ambienti.
2. **Agentic Reasoning (LangGraph):** Un agente conversazionale basato su grafi che gestisce il flusso della conversazione, interroga un database vettoriale (Vector Similarity Search) contenente gli embeddings delle immagini e dei testi, e raffina le raccomandazioni in base ai feedback espliciti dell'utente.

---

## 🛠️ Architettura Tecnica e Stack Tecnologico

Il progetto è interamente sviluppato in **Python** e si articola sulle seguenti tecnologie chiave:

* **Modelli Multimodali:** Fine-tuning di modelli **BLIP** per l'estrazione di feature visive e la generazione di text captioning accurato.
* **Orchestrazione Agenti:** **LangGraph** (LangChain) per la progettazione del flusso logico dell'agente a stati, garantendo persistenza, gestione dei cicli di conversazione e decision-making robusto.
* **Vector Search:** Implementazione di una ricerca per similarità semantica (vettoriale) per combinare il testo delle query utente con le informazioni visive estratte dalle patch delle immagini.
* **Metodologia:** Approccio *Human-in-the-loop* per l'ottimizzazione del recupero delle informazioni e il perfezionamento dei risultati.

---

## 📂 Struttura della Repository

```text
├── real_estate_captioning_final.ipynb   # Notebook principale con pipeline di fine-tuning e agent log
├── README.md                             # Documentazione del progetto
└── (opzionale: requisiti/configurazioni)
