# 🐸 Projekt 2 – Pakiet Frog: Obsługa sklepu online Żabka

## 📘 Opis projektu

Celem projektu jest stworzenie pakietu `Frog`, który umożliwia zarządzanie zasobami nowo powstałego sklepu online Żabka. Aplikacja pozwala administratorowi (znającemu Pythona) na pełną kontrolę nad produktami spożywczymi oraz danymi klientów posiadających karty stałego klienta.

Projekt został zrealizowany w paradygmacie **funkcyjnym** i obejmuje zarówno obsługę zasobów, jak i interfejs graficzny ułatwiający pracę użytkownika.

---

## 📁 Struktura pakietu

```text
Frog/
├── main.py                 # Główny moduł (__main__)
├── customers.py            # Moduł zarządzania klientami
│
├── products.xlsx           # Baza danych produktów
├── customer.csv            # Dane klientów
├── address.csv             # Adresy klientów
├── admins.csv              # Dane adminów
│
└── DATABASE/               # Folder z zakupami klientów
    └── 2336.txt            # Dane zakupów konkretnego klienta (po ID)
    └── 4198.txt            # Dane zakupów konkretnego klienta (po ID)
    └── 7879.txt            # Dane zakupów konkretnego klienta (po ID)
    └── 8434.txt            # Dane zakupów konkretnego klienta (po ID)
│
└── Grafiki/                # Folder z grafikami
```
---

## 🔧 Technologie i biblioteki

- Python 3.11+
- `pandas` – obsługa danych w CSV i XLSX
- `openpyxl` – edycja plików Excel
- `tkinter` – GUI
- `datetime` – rejestrowanie dat zakupów
- `random` – generowanie unikalnych ID
- `functools` – dekoratory
- `os`, `csv`, `logging` – obsługa plików i wyjątków

---

## 🚀 Jak uruchomić projekt?

1. **Klonuj repozytorium:**
   ```bash
   git clone https://github.com/jp91422/ZabkaOnline
   cd frog-zabka

2. Zainstaluj wymagane biblioteki:
    ```bash
   pip install -r requirements.txt

3. Uruchom aplikację:
    ```bash
   python main.py

---

## 💡 Funkcjonalności
- Rejestracja nowych klientów (generowanie ID, tworzenie pliku zakupów)

- Usuwanie danych klientów (po ID lub nazwie)

- Dodawanie/usuwanie produktów (w products.xlsx)

- Zakupy klienta (obsługa wielu produktów jednocześnie)

- Monitoring: liczba klientów, dostępnych produktów, analiza zakupów

- Graficzny interfejs użytkownika (GUI)

---

## 📚 Dokumentacja (wybrane funkcje)
- register_customer(name: str, surname: str) -> None
Rejestruje nowego klienta. Generuje 4-cyfrowy ID, zapisuje dane do customer.csv i tworzy plik zakupowy w folderze DATABASE.

- purchase_products(customer_id: str, products: list[tuple]) -> None
Pozwala klientowi na jednoczesny zakup wielu produktów. Zapisuje dane zakupów do pliku klienta.

- @log_action
Dekorator dodający automatyczny zapis logów operacji administratora (np. rejestracja, zakupy).

---

## 🛡️ Obsługa wyjątków
- Błędny format danych wejściowych (np. brak ID, nieprawidłowe nazwy produktów)

- Próba zakupu nieistniejącego produktu

- Obsługa nieistniejącego klienta

---

## 🔐 Przyszłe rozszerzenia
- Logowanie i role użytkowników (admin/klient)

- Historia zakupów klienta w GUI

- Filtrowanie produktów (np. wg kategorii, daty ważności)

- API REST dla integracji mobilnej

---

## 👨‍🎓 Autorzy

Damian Modzelewski<br>
nr indeksu: 91454<br>
e-mail: dm91454@student.uwb.edu.pl<br>
<br>
Szymon Michaluk<br>
nr indeksu: 91425<br>
e-mail: sm91425@student.uwb.edu.pl<br>
<br>
Jakub Przeździecki<br>
nr indeksu: 91422<br>
e-mail: jp91422@student.uwb.edu.pl<br>

---

## 🗂 Repozytorium
Projekt dostępny publicznie na GitHub:
👉 https://github.com/jp91422/ZabkaOnline





















