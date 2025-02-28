# Model Pipeline dla klasyfikacji i regresji - PCA

## Wprowadzenie

Celem tego projektu jest zastosowanie redukcji wymiarowości PCA (Principal Component Analysis) w problemach klasyfikacji i regresji. Wykorzystujemy dwa różne zbiory danych:
1. **Diabetes Dataset** - do klasyfikacji, gdzie przewidujemy, czy pacjent ma cukrzycę.
2. **Daily Bike Share Dataset** - do regresji, gdzie przewidujemy liczbę wynajmów rowerów w danym dniu.

Projekt obejmuje eksplorację danych, przetwarzanie, zastosowanie PCA do redukcji wymiarowości oraz ocenę modeli klasyfikacyjnych i regresyjnych z PCA.

## Funkcjonalności

### 1. Eksploracja danych:
   - Podsumowanie statystyczne cech (średnia, odchylenie standardowe, itp.).
   - Sprawdzenie brakujących wartości i ich uzupełnienie.

### 2. Przygotowanie danych:
   - Obsługa brakujących wartości (wypełnienie medianą).
   - Standaryzacja cech numerycznych (`StandardScaler`).
   - Podział danych na zestawy treningowe i testowe (80/20).

### 3. Stworzenie Pipeline dla klasyfikacji:
   - PCA redukujące wymiarowość cech.
   - Model regresji logistycznej (`LogisticRegression`).
   - Ocena modelu za pomocą metryk klasyfikacyjnych: Accuracy, F1-score, Macierz pomyłek.
   - Porównanie wyników modelu z PCA i bez PCA.

### 4. Stworzenie Pipeline dla regresji:
   - PCA redukujące liczbę cech do optymalnej wartości.
   - Model regresji liniowej (`LinearRegression`).
   - Ocena modelu za pomocą metryk regresyjnych: R² Score, RMSE.
   - Wizualizacja wariancji wyjaśnionej przez komponenty PCA.
   - Porównanie wyników modelu z PCA i bez PCA.

## Wyniki i wnioski

- **Klasyfikacja (Diabetes Dataset):**
  - PCA pozwoliło na redukcję liczby cech przy zachowaniu akceptowalnej skuteczności modelu.
  - Otrzymano accuracy na poziomie ~78% oraz F1-score 64%.

- **Regresja (Daily Bike Share Dataset):**
  - RMSE było stosunkowo wysokie (~469), co sugeruje, że PCA może usuwać istotne informacje.
  - R² wyniósł ~43%, co oznacza, że model wyjaśnia 43% zmienności danych.
  - Testowano różne liczby komponentów PCA, co miało wpływ na dokładność modelu.

## Technologie

Projekt został stworzony z użyciem:
- **Python**: Język programowania użyty do analizy danych i uczenia modeli.
- **Scikit-learn**: Biblioteka do uczenia maszynowego i budowania pipeline.
- **Pandas**: Biblioteka do manipulacji i analizy danych.
- **Matplotlib/Seaborn**: Biblioteki do wizualizacji danych.

## Pliki projektu:
- `diabetes.csv`: Zbiór danych dla klasyfikacji.
- `daily-bike-share.csv`: Zbiór danych dla regresji.



