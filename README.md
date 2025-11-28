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

```csharp
## 🖥️ Pełny program konsolowy (C#)

Poniżej znajduje się kompletny program konsolowy zawierający menu i wszystkie algorytmy wymagane w projekcie.

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        while (true)
        {
            Console.Clear();
            Console.WriteLine("=== ALGORYTMY MATURALNE ===");
            Console.WriteLine("1. Sprawdzanie liczby pierwszej");
            Console.WriteLine("2. Sito Eratostenesa");
            Console.WriteLine("3. Rozkład na czynniki pierwsze");
            Console.WriteLine("4. Silnia (iteracyjnie i rekurencyjnie)");
            Console.WriteLine("5. Fibonacci (iteracyjnie i rekurencyjnie)");
            Console.WriteLine("6. Potęgowanie szybkie");
            Console.WriteLine("7. Odwrotność modulo");
            Console.WriteLine("0. Wyjście");
            Console.Write("Wybierz opcję: ");

            int opcja = int.Parse(Console.ReadLine());

            switch (opcja)
            {
                case 1: SprawdzPierwsza(); break;
                case 2: Sito(); break;
                case 3: Czynniki(); break;
                case 4: Silnia(); break;
                case 5: Fibonacci(); break;
                case 6: FastPower(); break;
                case 7: ModInverseProgram(); break;
                case 0: return;
                default: Console.WriteLine("Nie ma takiej opcji."); break;
            }

            Console.WriteLine("\nNaciśnij ENTER, aby kontynuować...");
            Console.ReadLine();
        }
    }

    // 1. Liczba pierwsza
    static void SprawdzPierwsza()
    {
        Console.Write("Podaj liczbę: ");
        int n = int.Parse(Console.ReadLine());

        bool pierwsza = CzyPierwsza(n);
        Console.WriteLine(pierwsza ? "Liczba pierwsza" : "Nie jest pierwsza");
    }
    static bool CzyPierwsza(int n)
    {
        if (n < 2) return false;
        for (int i = 2; i * i <= n; i++)
            if (n % i == 0) return false;
        return true;
    }

    // 2. Sito
    static void Sito()
    {
        Console.Write("Podaj n: ");
        int n = int.Parse(Console.ReadLine());

        var primes = SitoEratostenesa(n);
        Console.WriteLine("Liczby pierwsze:");
        Console.WriteLine(string.Join(", ", primes));
    }
    static List<int> SitoEratostenesa(int n)
    {
        bool[] p = new bool[n + 1];
        for (int i = 2; i <= n; i++) p[i] = true;

        for (int i = 2; i * i <= n; i++)
            if (p[i])
                for (int j = i * i; j <= n; j += i)
                    p[j] = false;

        List<int> wynik = new List<int>();
        for (int i = 2; i <= n; i++)
            if (p[i]) wynik.Add(i);

        return wynik;
    }

    // 3. Czynniki
    static void Czynniki()
    {
        Console.Write("Podaj liczbę: ");
        int n = int.Parse(Console.ReadLine());

        List<int> wynik = Rozklad(n);
        Console.WriteLine("Czynniki: " + string.Join(" * ", wynik));
    }
    static List<int> Rozklad(int n)
    {
        List<int> w = new List<int>();
        for (int i = 2; i * i <= n; i++)
            while (n % i == 0)
            {
                w.Add(i);
                n /= i;
            }
        if (n > 1) w.Add(n);
        return w;
    }

    // 4. Silnia
    static void Silnia()
    {
        Console.Write("Podaj n: ");
        int n = int.Parse(Console.ReadLine());

        Console.WriteLine($"Silnia iteracyjnie: {SilniaIter(n)}");
        Console.WriteLine($"Silnia rekurencyjnie: {SilniaRek(n)}");
    }
    static long SilniaIter(int n)
    {
        long w = 1;
        for (int i = 1; i <= n; i++) w *= i;
        return w;
    }
    static long SilniaRek(int n)
    {
        if (n <= 1) return 1;
        return n * SilniaRek(n - 1);
    }

    // 5. Fibonacci
    static void Fibonacci()
    {
        Console.Write("Podaj n: ");
        int n = int.Parse(Console.ReadLine());

        Console.WriteLine($"Fib iteracyjnie: {FibIter(n)}");
        Console.WriteLine($"Fib rekurencyjnie: {FibRek(n)}");
    }
    static long FibIter(int n)
    {
        if (n == 0) return 0;
        if (n == 1) return 1;

        long a = 0, b = 1;
        for (int i = 2; i <= n; i++)
        {
            long c = a + b;
            a = b;
            b = c;
        }
        return b;
    }
    static long FibRek(int n)
    {
        if (n < 2) return n;
        return FibRek(n - 1) + FibRek(n - 2);
    }

    // 6. Fast Power
    static void FastPower()
    {
        Console.Write("Podaj a: ");
        long a = long.Parse(Console.ReadLine());
        Console.Write("Podaj n (wykładnik): ");
        long n = long.Parse(Console.ReadLine());

        Console.WriteLine($"a^n = {FastPow(a, n)}");
    }
    static long FastPow(long a, long n)
    {
        long wynik = 1;
        while (n > 0)
        {
            if ((n & 1) == 1)
                wynik *= a;
            a *= a;
            n >>= 1;
        }
        return wynik;
    }

    // 7. Odwrotność modulo m
    static void ModInverseProgram()
    {
        Console.Write("Podaj a: ");
        int a = int.Parse(Console.ReadLine());
        Console.Write("Podaj m: ");
        int m = int.Parse(Console.ReadLine());

        try
        {
            int inv = ModInverse(a, m);
            Console.WriteLine($"Odwrotność modulo = {inv}");
        }
        catch
        {
            Console.WriteLine("Brak odwrotności modulo!");
        }
    }

    static (int x, int y, int d) ExtendedGcd(int a, int b)
    {
        if (b == 0) return (1, 0, a);

        var r = ExtendedGcd(b, a % b);
        int x = r.y;
        int y = r.x - r.y * (a / b);
        return (x, y, r.d);
    }

    static int ModInverse(int a, int m)
    {
        var (x, y, d) = ExtendedGcd(a, m);
        if (d != 1) throw new Exception();
        return (x % m + m) % m;
    }
}


```



