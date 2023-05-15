## Instrukcje warunkowe

Niektóre wydarzenia dzieją się tylko wtedy, gdy zostanie spełniony jakiś warunek. Np. woda zacznie wrzeć, gdy osiągnie temperaturę 100 stopni, a drzwi otworzysz tylko wtedy, gdy masz pasujący klucz. Podobnie dzieje się w języku JavaScript - instrukcja warunkowa wykonuje wybrany kod, w zależności od tego czy wartość danego wyrażenia jest logiczną prawdą \(true\) czy logicznym fałszem \(false\).

### if...else...

Jak wygląda instrukcja warunkowa? Kluczowym elementem jest wyrażenie **if:**

```js
if (warunek) {

    ...polecenie, które wykonuje się, gdy warunek jest spełniony
}
```

np.

```js
let x = 34;

if (x < 100) {
    console.log('Liczba jest mniejsza od 100');
}
```

```js
 if (x < 10) {
     console.log('Liczba jest mniejsza od 10');
 }
```

Kolejny element instrukcji warunkowej to **else**, czyli polecenie, które wykonuje się jeśli jednak warunek nie jest spełniony.

np.

```js
let x = 34;

if (x < 100) {
     console.log('Liczba jest mniejsza od 100');
} else {
     console.log('Liczba jest większa od 100');
}


if (x < 10) {
     console.log('Liczba jest mniejsza od 10');
} else {
     console.log('Liczba jest większa od 10');
}
```

Możemy też sprawdzać kilka warunków jeden po drugim. Służy do tego **else if**,

```js
if (x < 10) {
     console.log('Liczba jest mniejsza od 10');
}  else if (x > 10) {
     console.log('Liczba jest większa od 10');
} else {
     console.log('Liczba jest równa 10');
}
```

W swoim pliku JS stwórz dwie zmienne o nazwach a i b. Przypisz do nich dwie różne liczby. Następnie zapisz następujący warunek: jeśli a jest większe od b, w konsoli powinien ukazać się napis "a jest większe od b". Jeśli b jest większe, w konsoli powinnaś zobaczyć "b jest większe od a".

### switch

**Warunki można również sprawdzać za pomocą instrukcji switch.**

```js
let language = 'Spanish';

switch (language) {
    case 'English': 
        console.log('Hello!');
        break;
    case 'French':
        console.log('Salut');
        break;
    case 'Spanish':
        console.log('Hola!');
        break;
    case 'Polish':
        console.log('Cześć!');
        break;
    default:
        console.log(`I don't know this language`);
}
```

Zauważ, że każdy przypadek kończy się słowem **break.** Break przerywa wykonywanie instrukcji switch. Oznacza to, że jeśli któryś ze wskazanych przypadków zostanie spełniony, dalsze porówniania nie będą już wykonywane. Jeżeli pominiemy to słowo, wówczas nawet przy pomyślnym przyrównaniu zostaną wykonane kolejne sprawdzenia. Naszą instrukcję switch kończy specjalny przypadek **default**, który będzie wybierany, gdy wszystkie inne przypadki będą błędne.

### Zadanie:

Stwórz w swoim pliku JS zmienną o nazwie `weather` i przypisz do niej wartość "sun". Następnie, używając instrukcji `switch` spraw, aby w konsoli ukazał się następujący tekst:

* gdy zmienna `weather` jest równa "sun" - "It's sunny!"
* gdy zmienna `weather` jest równa "rain" = "It's raining!"
* gdy zmienna `weather` jest równa "wind" = "It's windy!"

Teraz przypisz do zmiennej `weather` wartość "rain" i zobacz, jak zmienia się tekst w konsoli. To samo sprawdź przypisując do niej wartość "wind".

**Instrukcja if..else... korzysta z operatorów porównania**

Nie zawsze wszystko jest albo większe albo mniejsze, albo równe. Może przecież być większe lub równe, mniejsze lub równe, itp. W JS mamy do dyspozycji następujące operatory porównania:

`let x = 34;`

| Operator | Opis | Równanie | Zwróci |
| :--- | :--- | :--- | :--- |
| == | równe | x == 56 | false |
| != | różne | x != 56 | true |
| === | równa wartość i taki sam typ danych | x === 34 | true |
|  |  |  |  |
|  |  | x === "34" | false |
| !== | różne wartości lub różny typ danych | x !== "34" | true |
|  |  | x !== 34 | false |
| &gt; | większe od | x &gt; 67 | false |
| &lt; | mniejsze od | x &lt; 67 | true |
| &gt;= | większe bądź równe od | x &gt;= 56 | false |
| &lt;= | mniejsze bądź równe od | x &lt;= 56 | true |

Zwróć uwagę, że w JS pojedynczy znak równości przypisuje wartość np. do zmiennej. Z kolei podwójny znak równania == to porównanie dwóch wartości, a dokładniej sprawdzenie, czy są takie same.

**Możemy też spotkać operatory logiczne:**

`let x = 34;`

`let y = 13;`

| Operator | Opis | Przykład | Wynik |
| :--- | :--- | :--- | :--- |
| && | and \(i\) | \(x &lt; 100 && y &gt; 10\) | Prawda \(x jest mniejsze od 100 **i **y jest większe od 10\) |
| II | or \(lub\) | \(x &gt; 80 II y &gt; 10\) | Prawda, bo x nie jest większe od 80, ale y jest większe od 10 |
| ^ | xor \(jeden z, ale nie dwa równocześnie\) | \(x === 34 ^ y === 13\) | Fałsz, bo obydwa są prawdziwe |
| ! | not \(negacja\) | !\(x == y\) | Prawda, bo negujemy to, że x == y |



