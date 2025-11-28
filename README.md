# Algorytmy Maturalne – C# (Console + WinForms)

To repozytorium zawiera implementacje najważniejszych algorytmów wymaganych w technikum oraz na maturze z informatyki.  
Projekt składa się z dwóch części:

- **wersja konsolowa** – prosta w obsłudze, idealna do nauki algorytmiki  
- **wersja .NET WinForms** – aplikacja z graficznym interfejsem, gdzie można zaznaczać dowolną liczbę algorytmów

Repozytorium służy jako materiał edukacyjny dla uczniów technikum informatycznego.

---

## 🎯 Cel projektu

Celem repozytorium jest:

- nauczyć najważniejszych algorytmów z zakresu matury i egzaminu zawodowego,
- pokazać przejrzyste implementacje w języku **C#**,
- umożliwić testowanie algorytmów w praktyce,
- ułatwić zrozumienie działania algorytmów (definicje + pseudokod + kod).

---

## 📚 Zawarte algorytmy

### **Algorytmy liczbowe**
- sprawdzanie liczby pierwszej  
- generowanie liczb pierwszych (Sito Eratostenesa)  
- rozkład liczby na czynniki pierwsze  
- silnia (iteracyjna i rekurencyjna)  
- ciąg Fibonacciego (iteracyjny i rekurencyjny)  
- potęgowanie szybkie (Fast Power)  
- odwrotność modulo (rozszerzony algorytm Euklidesa)

Każdy algorytm posiada:
- opis działania,  
- definicję matematyczną,  
- wersję w pseudokodzie,  
- implementację w języku C#.

---

## 🖥️ Wersje projektu

### **1. Wersja konsolowa (Console App)**

Interfejs tekstowy, w którym użytkownik wybiera algorytm z menu i wprowadza liczby.  
Program wyświetla wynik obliczeń.  
Idealne narzędzie do nauki krok po kroku.

---

### **2. Wersja WinForms (.NET)**

Aplikacja posiada:

- pola tekstowe do wpisywania danych,
- **checkboxy**, które pozwalają wybrać dowolną liczbę algorytmów,
- przycisk **„Oblicz”**,
- okno wynikowe wyświetlające wszystkie zaznaczone obliczenia.

Jest to praktyczna pomoc dla studentów na zajęciach laboratoryjnych.

---

## 🚀 Jak uruchomić projekt?

### **Konsola**
1. Otwórz projekt w Visual Studio  
2. Uruchom (`F5`)  
3. Postępuj zgodnie z instrukcjami wyświetlanymi na ekranie  

### **WinForms**
1. Otwórz folder `WinFormsAlgorithms`  
2. Uruchom projekt Visual Studio (`.sln`)  
3. Wprowadź liczby  
4. Zaznacz dowolne algorytmy  
5. Kliknij **„Oblicz”**

---

## 📖 Dla kogo jest to repozytorium?

Repozytorium jest przeznaczone dla:

- uczniów technikum informatycznego,  
- studentów poznających podstawy algorytmiki,  
- osób przygotowujących się do matury z informatyki,  
- osób uczących się C# i programowania proceduralnego.

---

## 🏆 Co zyska?

- zrozumie podstawowe algorytmy matematyczne,
- nauczy się implementować algorytmy w C#,
- zrozumie iterację i rekurencję,
- pozna podstawy programowania strukturalnego,
- oswoi się z WinForms i pracą z projektami .NET.

---

## 🤝 Wkład i rozwój projektu

Możesz rozszerzyć projekt o:

- dodatkowe algorytmy,
- testy jednostkowe,
- wersję w .NET MAUI / WPF,
- dokumentację HTML / PDF.

Pull requesty są mile widziane.

---


## 📦 Zestaw algorytmów (C#)

Poniżej znajdują się wszystkie algorytmy zawarte w projekcie — w pełnych, gotowych do użycia implementacjach C#.

---

### ✅ 1. Sprawdzanie liczby pierwszej

```csharp
bool CzyPierwsza(int n)
{
    if (n < 2) return false;

    for (int i = 2; i * i <= n; i++)
        if (n % i == 0)
            return false;

    return true;
}

