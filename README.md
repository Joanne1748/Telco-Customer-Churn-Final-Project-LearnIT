# Telco Customer Churn — analiza i przewidywanie odejść klientów

## Charakter projektu

Projekt edukacyjny zrealizowany w ramach kursu LearnIT "Data Science + AI". Wyniki mają charakter analityczny i nie stanowią gotowego, wdrożonego systemu do podejmowania decyzji biznesowych.

## Opis projektu

Projekt poświęcony jest analizie danych klientów operatora telekomunikacyjnego oraz przewidywaniu rezygnacji z usług (*customer churn*).

Celem jest sprawdzenie, czy informacje o klientach, używanych przez nich usługach, rodzaju umowy i opłatach mogą pomóc w identyfikacji klientów, którzy rezygnują z usług. W projekcie przeprowadzono analizę eksploracyjną danych (EDA), przygotowanie danych, budowę modeli klasyfikacyjnych oraz porównanie ich skuteczności.

## Cele projektu

- Poznanie struktury i jakości zbioru danych.
- Przeprowadzenie analizy eksploracyjnej (EDA).
- Przygotowanie danych do modelowania.
- Zbudowanie i porównanie modeli klasyfikacyjnych.
- Ocena modeli za pomocą różnych metryk, z uwzględnieniem błędów klasyfikacji.
- Sformułowanie wniosków i rekomendacji biznesowych.

## Zbiór danych

W projekcie wykorzystano zbiór **Telco Customer Churn**, udostępniony na platformie Kaggle.

**Źródło:** [Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

Zbiór zawiera 7043 rekordy i 21 kolumn opisujących klientów, ich usługi, rodzaje umów oraz opłaty. Zmienna docelowa `Churn` określa, czy klient zrezygnował z usług.

W trakcie przygotowania danych przekonwertowano kolumnę `TotalCharges` na typ liczbowy. Wykryte 11 brakujących wartości dotyczyło klientów ze stażem wynoszącym zero. Zostały one uzupełnione zerami zgodnie z przyjętym założeniem. Kolumnę `customerID` wyłączono z cech wejściowych modelu.

## Technologie

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Visual Studio Code

## Uruchomienie projektu

1. Sklonuj repozytorium lub pobierz jego pliki.
2. Przygotuj środowisko Python.
3. Zainstaluj wymagane biblioteki:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

4. Pobierz zbiór danych z [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn).
5. Umieść plik `WA_Fn-UseC_-Telco-Customer-Churn.csv` w katalogu `data/` w strukturze projektu.
6. Otwórz notebook w Jupyter Notebook lub Visual Studio Code.
7. Uruchom komórki od początku.

Notebook oczekuje pliku CSV pod ścieżką `data/WA_Fn-UseC_-Telco-Customer-Churn.csv`, względem katalogu projektu.

## Metodologia

Projekt obejmuje następujące etapy:

1. Wczytanie danych i kontrola ich jakości.
2. Analiza eksploracyjna rozkładów zmiennych i zależności między cechami a odejściami klientów.
3. Podział danych na zbiory treningowy (80%) i testowy (20%), z zachowaniem proporcji klas.
4. Przygotowanie cech numerycznych i kategorycznych z wykorzystaniem `StandardScaler`, `OneHotEncoder`, `ColumnTransformer` i `Pipeline`.
5. Zbudowanie modelu bazowego oraz czterech modeli klasyfikacyjnych.
6. Porównanie wyników na podstawie metryk i macierzy pomyłek.
7. Interpretacja cech oraz sformułowanie wniosków biznesowych.

### Porównywane modele

- Dummy Classifier — model bazowy.
- Regresja logistyczna (*Logistic Regression*).
- Random Forest.
- Decision Tree.
- Gradient Boosting.
