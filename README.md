# **Przewidywanie ocen uczniów na podstawie danych socjoekonomicznych i ich nawyków**

### **Cel projektu:**  
Celem projektu było **stworzenie modelu regresyjnego**, który **przewiduje wynik ucznia** na podstawie: 
- ilości snu
- liczby godzin nauki
- frekwencji
- statusu socjoekonomicznego

### **Projekt pozwala na oszacowanie przewidywanej oceny nowego ucznia w oparciu o powyższe dane wejściowe.**

### **Źródło danych:**  
Dane pochodzą z  platformy [Kaggle](https://www.kaggle.com/datasets/stealthtechnologies/predict-student-performance-dataset)  
Zbiór zawiera 1388 rekordów i 5 cech (4 niezależne + 1 zależna)

### **Wykorzystane narzędzia:**
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn (regresja liniowa, drzewo decyzyjne, cross-validation)
- Google Colab

### **Etapy projektu:**  
**1.	Eksploracyjna analiza danych (EDA):**
- Sprawdzenie struktury danych, typów zmiennych i brakujących wartości (których nie było)
- Przeanalizowanie rozkładów zmiennych, identyfikujących zmienne skośne i wartości odstające
- Zastosowanie transformacji logarytmicznych w celu zmniejszenia skośności i standaryzacji dla ujednolicenia skali zmiennych
- Podjęcie decyzji o nieusuwaniu wartości odstających oraz uzasadnienie ich ważnej i nieprzypadkowej obecności w kontekście danych

**2.	Podział danych:**
- Dane zostały podzielone na zbiór treningowy (80%) i testowy (20%)
- W ramach zbioru treningowego wydzielono zbiór walidacyjny (10%), aby uniknąć przeuczenia modelu

**3.	Budowa i ocena modeli:**
- Zaczęto od przetestowania regresji liniowej, która uznawana jest za najprostszy model regresyjny
- Następnie zastosowano drzewo decyzyjne, które znacznie poprawiło dokładność przewidywań
- Wybrano miary RMSE, MAE i R², aby ocenić jakość modeli
- Pomimo satysfakcjonujących wyników miar, przeprowadzono optymalizację hiperparametrów drzewa decyzyjnego za pomocą GridSearchCV w celu zwiększenia dokładności modelu

### **Wyniki:**
- Najlepszy wynik uzyskano przy użyciu modelu **drzewa decyzyjnego z dostrojonymi hiperparametrami**
- Model pozwala trafnie oszacować wynik ucznia na podstawie prostych danych wejściowych

Projekt stworzony przez **Julię Krężałek** w ramach nauki i budowy portfolio data science.
