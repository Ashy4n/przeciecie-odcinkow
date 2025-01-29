# Aplikacja do wizualizacji przecięcia odcinków

## Opis

Aplikacja do wizualizacji odcinków w układzie współrzędnych. Główna funkcja `rysuj` umożliwia rysowanie dwóch odcinków,
zaznaczanie punktów przecięcia lub zakresów nachodzenia się odcinków.

## Wymagania

- **Python:** Wersja 3.6 lub wyższa
- **Biblioteki Python:**
    - `matplotlib`
    - `flask`

## Instalacja

1. **Sklonuj Repozytorium:**

```bash
  git clone https://github.com/Ashy4n/przeciecie-odcinkow.git
```

2. **Przejdź do Katalogu Projektu:**

```bash
cd przeciecie-odcinkow
```

3. **Zainstaluj Wymagane Biblioteki:**

```bash
pip install flask matplotlib
```

4. **Uruchom Aplikację:**

```bash
python app.py
```

5. **Otwórz Aplikację w Przeglądarce:**

Wejdź na podany adres URL w przeglądarce

```
http://127.0.0.1:5000
```

---

## Użycie

### Funkcja rysuj

#### Użycie:

```rysuj(odcinek1, odcinek2) -> str```

#### Opis:

    Rysuje dwa odcinki na wykresie, zaznacza ich punkt przecięcia lub zakres nachodzenia się. Zwraca wykres jako ciąg Base64.
    #### Parametry:
    odcinek1 (tuple): Krotka czterech liczb (x1, y1, x2, y2) opisujących pierwszy odcinek.
    odcinek2 (tuple): Krotka czterech liczb (x3, y3, x4, y4) opisujących drugi odcinek.

#### Zwraca:

    str: Ciąg Base64 reprezentujący wygenerowany wykres w formacie PNG.

---

## Integracja z Aplikacją Webową

Wykres zwrócony przez funkcję rysuj można wyświetlić w aplikacji webowej poprzez osadzenie obrazu Base64 w tagu HTML
```<img>```:

```<img src="data:image/png;base64,{{wykres_base64}}" alt="Wykres odcinków"/>```


