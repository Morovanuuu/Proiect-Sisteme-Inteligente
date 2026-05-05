# Analiza si Predictia Succesului Canalelor YouTube (1M Global Stats)

## 1. Sursa Datelor

- **Dataset:** [YouTube 1M Global Creator Analytics](https://www.kaggle.com/datasets/ehsanzx/youtube-1m-global-creator-analytics)
- **Data descarcarii:** 20 Martie 2026
- **Descriere:** Set de date ce contine statistici detaliate despre aproximativ 1 milion de creatori de continut, incluzand categorii, numar de abonati, vizualizari si scoruri de sentiment.

---

## 2. Obiectivul Proiectului

Scopul acestui proiect este dezvoltarea unui sistem de analiza predictiva capabil sa estimeze performanta unui videoclip (**numarul de vizualizari**) pe baza indicatorilor de interactiune si a sentimentului publicului.

**Problema abordata:** Utilizarea algoritmilor de regresie pentru a prezice succesul unui canal in functie de variabile precum aprecierile (likes), comentariile, distribuirile si scorul de sentiment.

---

## 3. Etapele Procesarii Datelor

- **Curatare si Esantionare:** Pentru optimizarea performantei, s-a lucrat pe un esantion reprezentativ de 5.000 de inregistrari. S-au eliminat valorile lipsa si duplicatele.
- **Feature Engineering:** S-a generat metrica `engagement_rate` pentru a masura intensitatea interactiunii raportata la numarul de vizualizari.
- **Analiza Corelatiilor:** Utilizarea unei matrice de corelatie (Heatmap) a permis identificarea variabilelor cu impact major asupra vizualizarilor, evidentiind importanta statistica a numarului de likes.

---

## 4. Modelare si Evaluarea Performantei (Machine Learning)

S-au implementat si comparat 5 algoritmi de regresie pentru a identifica cel mai stabil model predictiv. Evaluarea a fost realizata folosind seturi de date de antrenare si testare (split 80/20).

### Rezultate Comparative:

| Model                 | Scor $R^2$ (Acuratete) | Eroare MAE  |
| :-------------------- | :--------------------: | :---------: |
| **Gradient Boosting** |       **0.8614**       | **2277.30** |
| Random Forest         |         0.8524         |   2371.16   |
| Regresie Liniara      |         0.8454         |   2549.02   |
| K-Nearest Neighbors   |         0.8150         |   2553.21   |
| Arbore de Decizie     |         0.7461         |   2961.62   |

> **Concluzie:** Modelul **Gradient Boosting** a obtinut cele mai bune rezultate, reusind sa explice peste 86% din variatia numarului de vizualizari.

---

## 5. Tehnologii Utilizate

- **Limbaj:** Python 3.12
- **Procesare Date:** `pandas`, `numpy`
- **Vizualizare:** `matplotlib`, `seaborn`
- **Machine Learning:** `scikit-learn` (Algoritmi: Linear, Tree, Forest, Boosting, KNN)
- **Mediu de lucru:** Visual Studio Code & Jupyter Notebooks

---

## 6. Structura Depozitului

- `analiza_youtube.ipynb`: Notebook-ul principal continand fluxul complet de lucru.
- `README.md`: Documentatia tehnica a proiectului.
- `.gitignore`: Fisier pentru excluderea mediului virtual si a fisierelor de date voluminoase.
