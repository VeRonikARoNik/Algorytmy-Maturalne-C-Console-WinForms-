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
## 📘 Teoria — proste wyjaśnienia wszystkich algorytmów

Poniżej znajduje się proste i zrozumiałe omówienie wszystkich algorytmów użytych w projekcie.  
Opis jest przygotowany specjalnie dla uczniów technikum — tak, aby każdy mógł łatwo zrozumieć działanie algorytmów bez wcześniejszej wiedzy akademickiej.

---

### 🔹 1. Sprawdzanie liczby pierwszej

Liczba jest **pierwsza**, jeśli:
- dzieli się tylko przez **1** i **siebie samą**,
- **nie ma innych dzielników**.

Przykłady:
- 7 → liczba pierwsza  
- 9 → nie jest pierwsza (dzieli się przez 3)

Algorytm działa tak:
- próbujemy dzielić liczbę przez liczby od 2 do **pierwiastka z n**,  
- jeśli znajdziemy dzielnik → liczba NIE jest pierwsza,  
- jeśli nie znajdziemy → liczba JEST pierwsza.

---

### 🔹 2. Sito Eratostenesa

To szybki sposób znajdowania wszystkich liczb pierwszych do n.

Działa w kilku krokach:
1. Zaznaczamy wszystkie liczby od 2 do n jako „możliwe pierwsze”.  
2. Zaczynamy od 2 i skreślamy jej wielokrotności: 4, 6, 8…  
3. Przechodzimy do następnej liczby (3) i znów skreślamy jej wielokrotności.  
4. To samo z 5, 7 itd.  
5. Liczby, które **nie zostały skreślone**, są pierwsze.

Przykład dla n = 10:  
→ liczby pierwsze to **2, 3, 5, 7**

---

### 🔹 3. Rozkład liczby na czynniki pierwsze

Każdą liczbę naturalną można zapisać jako **mnożenie liczb pierwszych**.

Przykłady:
- 12 → 2 × 2 × 3  
- 36 → 2 × 2 × 3 × 3

Jak działa algorytm?
- dzielimy liczbę kolejno przez 2, 3, 4, 5…  
- za każdym razem, gdy liczba się dzieli, zapisujemy dzielnik,  
- dzielimy dalej, aż nie będzie już czego dzielić.

---

### 🔹 4. Silnia (n!)

Silnia to:
> „pomnóż wszystkie liczby od **1 do n**”.

Przykład:
- **5! = 1×2×3×4×5 = 120**

Silnię liczymy na dwa sposoby:

#### ✔ Iteracyjnie
- zwykła pętla od 1 do n  
- mnożymy wszystko po kolei  

#### ✔ Rekurencyjnie
- funkcja, która wywołuje samą siebie:  
  **n! = n × (n−1)!**

---

### 🔹 5. Ciąg Fibonacciego

To ciąg liczb, w którym każda następna liczba jest **sumą dwóch poprzednich**.

Początek ciągu: 
0, 1, 1, 2, 3, 5, 8, 13, ...


Czyli:  
0+1=1,  
1+1=2,  
1+2=3,  
2+3=5, itd.

Można to policzyć:
- **iteracyjnie** — szybciej, w pętli  
- **rekurencyjnie** — wolniej, ale łatwiej wygląda

---

### 🔹 6. Potęgowanie szybkie (Fast Power)

Służy do szybkiego obliczenia potęgi:

\[
a^n
\]

Zamiast mnożyć a przez siebie **n razy**, robimy to dużo szybciej:

- jeśli wykładnik jest nieparzysty → wynik mnożymy przez a  
- podnosimy a do kwadratu  
- wykładnik dzielimy przez 2  

Dzięki temu zamiast n operacji jest ich około **log₂(n)**.

Przykład:  
Zamiast 13 mnożeń przy 4¹³ → zaledwie 4 mnożenia.

---

### 🔹 7. Odwrotność modulo

Odwrotność modulo to liczba x taka, że:

a * x ≡ 1 (mod m)


To coś jak „dzielenie” w arytmetyce modulo.

Odwrotność istnieje tylko wtedy, gdy:
- **a i m nie mają wspólnych dzielników**,  
czyli **NWD(a, m) = 1**.

Przykład:
- odwrotność 3 modulo 7 to **5**,  
bo 3 × 5 = 15, a **15 mod 7 = 1**.

Do obliczania używa się:
- **rozszerzonego algorytmu Euklidesa**.

---

## 🧠 Podsumowanie w bardzo prostych słowach

| Algorytm | O co w nim chodzi? |
|---------|----------------------|
| Liczba pierwsza | sprawdzamy, czy liczba dzieli się tylko przez 1 i siebie |
| Sito Eratostenesa | wykreślamy wielokrotności, zostają liczby pierwsze |
| Rozkład na czynniki | rozbijamy liczbę na mnożenie liczb pierwszych |
| Silnia | mnożymy liczby od 1 do n |
| Fibonacci | każda liczba to suma dwóch poprzednich |
| Fast Power | podnosimy do potęgi bardzo szybko, dzieląc wykładnik |
| Odwrotność modulo | „dzielenie” w modulo – tylko gdy NWD = 1 |

---



---
```csharp
bool CzyPierwsza(int n)
{
    if (n < 2) return false;

    for (int i = 2; i * i <= n; i++)
        if (n % i == 0)
            return false;

    return true;
}
```
### 2. Sito Eratostenesa (generowanie liczb pierwszych)
```
bool CzyPierwsza(int n)
{
    if (n < 2) return false;

    for (int i = 2; i * i <= n; i++)
        if (n % i == 0)
            return false;

    return true;
}

```
### 3. Rozkład liczby na czynniki pierwsze
```
List<int> Rozklad(int n)
{
    List<int> wynik = new List<int>();

    for (int i = 2; i * i <= n; i++)
        while (n % i == 0)
        {
            wynik.Add(i);
            n /= i;
        }

    if (n > 1)
        wynik.Add(n);

    return wynik;
}

```

### 4. Silnia
### Iteracyjnie
```
long SilniaIter(int n)
{
    long wynik = 1;

    for (int i = 1; i <= n; i++)
        wynik *= i;

    return wynik;
}


```

### Rekurencyjnie
```
long SilniaRek(int n)
{
    if (n <= 1)
        return 1;

    return n * SilniaRek(n - 1);
}

```
### 5. Fibonacci (iteracyjnie i rekurencyjnie)
### Iteracyjnie
```
long FibIter(int n)
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

```

### Rekurencyjnie
```
long FibRek(int n)
{
    if (n < 2)
        return n;

    return FibRek(n - 1) + FibRek(n - 2);
}

```

### 6. Potęgowanie szybkie (Fast Power)
```
long FastPow(long a, long n)
{
    long wynik = 1;

    while (n > 0)
    {
        if ((n & 1) == 1)
            wynik *= a;

        a *= a;
        n >>= 1; // dzielenie przez 2
    }

    return wynik;
}

```

### Rozszerzony algorytm Euklidesa
```
(int x, int y, int d) ExtendedGcd(int a, int b)
{
    if (b == 0)
        return (1, 0, a);

    var r = ExtendedGcd(b, a % b);

    int x = r.y;
    int y = r.x - r.y * (a / b);

    return (x, y, r.d);
}


```

### Odwrotność modulo
```
int ModInverse(int a, int m)
{
    var (x, y, d) = ExtendedGcd(a, m);

    if (d != 1)
        throw new Exception("Odwrotność nie istnieje (NWD ≠ 1)");

    return (x % m + m) % m;
}

```



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




## 🪟 WinForms – pełny kod aplikacji (.NET C#)

Poniżej znajduje się kompletny kod obsługi formularza WinForms zawierającego:

- `textBox1` – liczba a  
- `textBox2` – liczba b  
- `labelWynik` – pole wyświetlania wyników  
- `button1` – przycisk „Oblicz”  
- `checkBox1` – liczba pierwsza  
- `checkBox2` – sito Eratostenesa  
- `checkBox3` – rozkład na czynniki  
- `checkBox4` – silnia  
- `checkBox5` – Fibonacci  
- `checkBox6` – potęgowanie szybkie  
- `checkBox7` – odwrotność modulo  

### ✔ Kod Form1.cs

```csharp
using System;
using System.Collections.Generic;
using System.Windows.Forms;

namespace AlgorytmyMaturalne
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            labelWynik.Text = ""; // Czyścimy pole wyników

            int.TryParse(textBox1.Text, out int a);
            int.TryParse(textBox2.Text, out int b);

            // 1. Liczba pierwsza
            if (checkBox1.Checked)
            {
                bool pierwsza = CzyPierwsza(a);
                labelWynik.Text += $"Czy {a} jest liczbą pierwszą? → {pierwsza}\n";
            }

            // 2. Sito Eratostenesa
            if (checkBox2.Checked)
            {
                var list = SitoEratostenesa(a);
                labelWynik.Text += $"Liczby pierwsze do {a}:\n{string.Join(", ", list)}\n";
            }

            // 3. Rozkład liczby na czynniki
            if (checkBox3.Checked)
            {
                var cz = Rozklad(a);
                labelWynik.Text += $"Rozkład liczby {a}: {string.Join(" * ", cz)}\n";
            }

            // 4. Silnia
            if (checkBox4.Checked)
            {
                labelWynik.Text += $"Silnia {a}! iteracyjnie: {SilniaIter(a)}\n";
                labelWynik.Text += $"Silnia {a}! rekurencyjnie: {SilniaRek(a)}\n";
            }

            // 5. Fibonacci
            if (checkBox5.Checked)
            {
                labelWynik.Text += $"Fibonacci iteracyjnie: {FibIter(a)}\n";
                labelWynik.Text += $"Fibonacci rekurencyjnie: {FibRek(a)}\n";
            }

            // 6. Fast Power
            if (checkBox6.Checked)
            {
                long p = FastPow(a, b);
                labelWynik.Text += $"{a}^{b} = {p}\n";
            }

            // 7. Odwrotność modulo
            if (checkBox7.Checked)
            {
                try
                {
                    int inv = ModInverse(a, b);
                    labelWynik.Text += $"Odwrotność {a} modulo {b} = {inv}\n";
                }
                catch
                {
                    labelWynik.Text += $"Brak odwrotności modulo dla {a} i {b}\n";
                }
            }
        }

        // ==========================
        // ALGORYTMY
        // ==========================

        bool CzyPierwsza(int n)
        {
            if (n < 2) return false;
            for (int i = 2; i * i <= n; i++)
                if (n % i == 0) return false;
            return true;
        }

        List<int> SitoEratostenesa(int n)
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

        List<int> Rozklad(int n)
        {
            List<int> w = new List<int>();

            for (int i = 2; i * i <= n; i++)
                while (n % i == 0)
                {
                    w.Add(i);
                    n /= i;
                }

            if (n > 1)
                w.Add(n);

            return w;
        }

        long SilniaIter(int n)
        {
            long w = 1;
            for (int i = 1; i <= n; i++)
                w *= i;
            return w;
        }

        long SilniaRek(int n)
        {
            if (n <= 1) return 1;
            return n * SilniaRek(n - 1);
        }

        long FibIter(int n)
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

        long FibRek(int n)
        {
            if (n < 2) return n;
            return FibRek(n - 1) + FibRek(n - 2);
        }

        long FastPow(long a, long n)
        {
            long w = 1;

            while (n > 0)
            {
                if ((n & 1) == 1)
                    w *= a;

                a *= a;
                n >>= 1; // dzielenie przez 2
            }

            return w;
        }

        (int x, int y, int d) ExtendedGcd(int a, int b)
        {
            if (b == 0) return (1, 0, a);

            var r = ExtendedGcd(b, a % b);

            int x = r.y;
            int y = r.x - r.y * (a / b);

            return (x, y, r.d);
        }

        int ModInverse(int a, int m)
        {
            var (x, y, d) = ExtendedGcd(a, m);

            if (d != 1)
                throw new Exception("Brak odwrotności modulo!");

            return (x % m + m) % m;
        }
    }
}


```

Zadanie Samodzielne.
Zrealizuj minimum 2 algorytmy  w aplikacji desktopowej.
Wybierz dowolne jakich nie było z listy. 



