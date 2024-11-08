# Zadanie domowe #5 - JavaScript

### Zadanie 1: Nazwy użytkowników

Napisz funkcję strzałkową `getUserNames(users)`, która przyjmuje jeden parametr `users` — tablicę obiektów użytkowników. Funkcja powinna zwrócić tablicę nazw wszystkich użytkowników (właściwość `name`) z tablicy `users`.



Weź poniższy kod i wklej go po deklaracji swojej funkcji, aby sprawdzić poprawność jej działania. W konsoli wyświetlone zostaną wyniki jej wywołań.
```
console.log(
  getUserNames([
  {
    name: "Moore Hensley",
    email: "moorehensley@indexia.com",
    balance: 2811
  },
  {
    name: "Sharlene Bush",
    email: "sharlenebush@tubesys.com",
    balance: 3821
  },
  {
    name: "Ross Vazquez",
    email: "rossvazquez@xinware.com",
    balance: 3793
  },
  {
    name: "Elma Head",
    email: "elmahead@omatom.com",
    balance: 2278
  },
  {
    name: "Carey Barr",
    email: "careybarr@nurali.com",
    balance: 3951
  },
  {
    name: "Blackburn Dotson",
    email: "blackburndotson@furnigeer.com",
    balance: 1498
  },
  {
    name: "Sheree Anthony",
    email: "shereeanthony@kog.com",
    balance: 2764
  },
])
); // ["Moore Hensley", "Sharlene Bush", "Ross Vazquez", "Elma Head", "Carey Barr", "Blackburn Dotson", "Sheree Anthony"]

```

### Zadanie 2. Użytkownicy ze znajomym
Napisz funkcję strzałkową `getUsersWithFriend(users, friendName)`, która przyjmuje dwa parametry:
* pierwszy parametr `users` — tablica obiektów użytkowników,
* drugi parametr `friendName` — nazwa znajomych do wyszukania.


Funkcja powinna zwrócić tablicę wszystkich użytkowników z tablicy `users`, którzy mają znajomego o nazwie `friendName`. Znajomi każdego użytkownika są przechowywani we właściwości `friends`. Jeśli nie ma użytkowników, którzy mają takiego znajomego, funkcja powinna zwrócić pustą tablicę.

Wskazówki:
* Metoda `filter()` może być użyta do utworzenia nowej tablicy z elementami spełniającymi określony warunek.
* Użyj metody `includes()`, aby sprawdzić czy tablica `friends` zawiera `friendName`.


Weź poniższy kod i wklej go po deklaracji swojej funkcji, aby sprawdzić, czy działa poprawnie. W konsoli wyświetlone zostaną wyniki jego działania.
```
const allUsers = [
  {
    name: "Moore Hensley",
    friends: ["Sharron Pace"]
  },
  {
    name: "Sharlene Bush",
    friends: ["Briana Decker", "Sharron Pace"]
  },
  {
    name: "Ross Vazquez",
    friends: ["Marilyn Mcintosh", "Padilla Garrison", "Naomi Buckner"]
  },
  {
    name: "Elma Head",
    friends: ["Goldie Gentry", "Aisha Tran"]
  },
  {
    name: "Carey Barr",
    friends: ["Jordan Sampson", "Eddie Strong"]
  },
  {
    name: "Blackburn Dotson",
    friends: ["Jacklyn Lucas", "Linda Chapman"]
  },
  {
    name: "Sheree Anthony",
    friends: ["Goldie Gentry", "Briana Decker"]
  }
];

console.log(getUsersWithFriend(allUsers, "Briana Decker")); 
// [
//   {
//     name: "Sharlene Bush",
//     friends: ["Briana Decker", "Sharron Pace"]
//   },
//   {
//     name: "Sheree Anthony",
//     friends: ["Goldie Gentry", "Briana Decker"]
//   }
// ]

console.log(getUsersWithFriend(allUsers, "Goldie Gentry"));
// [
//   {
//     name: "Elma Head",
//     friends: ["Goldie Gentry", "Aisha Tran"]
//   },
//   {
//     name: "Sheree Anthony",
//     friends: ["Goldie Gentry", "Briana Decker"]
//   }
// ]

console.log(getUsersWithFriend(allUsers, "Adrian Cross" )); // []
```

### Zadanie 3. Sortowanie według liczby znajomych

Napisz funkcję strzałkową `sortByDescendingFriendCount(users)`, która przyjmuje jeden parametr `users` — tablicę obiektów użytkowników.



Funkcja powinna zwrócić tablicę wszystkich użytkowników posortowanych według liczby znajomych w porządku malejącym (właściwość `friends`).



Weź poniższy kod i wklej go po deklaracji swojej funkcji, aby sprawdzić poprawność jej działania. Wyniki jego działania zostaną wyświetlone w konsoli.
```
console.log(
  sortByDescendingFriendCount([
    {
      name: "Moore Hensley",
      friends: ["Sharron Pace"],
      gender: "male"
    },
    {
      name: "Sharlene Bush",
      friends: ["Briana Decker", "Sharron Pace"],
      gender: "female"
    },
    {
      name: "Ross Vazquez",
      friends: ["Marilyn Mcintosh", "Padilla Garrison", "Naomi Buckner"],
      gender: "male"
    },
    {
      name: "Elma Head",
      friends: ["Goldie Gentry", "Aisha Tran"],
      gender: "female"
    },
    {
      name: "Carey Barr",
      friends: ["Jordan Sampson", "Eddie Strong"],
      gender: "male"
    },
    {
      name: "Blackburn Dotson",
      friends: ["Jacklyn Lucas", "Linda Chapman"],
      gender: "male"
    },
    {
      name: "Sheree Anthony",
      friends: ["Goldie Gentry", "Briana Decker"],
      gender: "female"
    }
  ])
);
// [
//   {
//     name: "Ross Vazquez",
//     friends: ["Marilyn Mcintosh", "Padilla Garrison", "Naomi Buckner"],
//     gender: "male"
//   },
//   {
//     name: "Sharlene Bush",
//     friends: ["Briana Decker", "Sharron Pace"],
//     gender: "female"
//   },
//   {
//     name: "Elma Head",
//     friends: ["Goldie Gentry", "Aisha Tran"],
//     gender: "female"
//   },
//   {
//     name: "Carey Barr",
//     friends: ["Jordan Sampson", "Eddie Strong"],
//     gender: "male"
//   },
//   {
//     name: "Blackburn Dotson",
//     friends: ["Jacklyn Lucas", "Linda Chapman"],
//     gender: "male"
//   },
//   {
//     name: "Sheree Anthony",
//     friends: ["Goldie Gentry", "Briana Decker"],
//     gender: "female"
//   },
//   {
//     name: "Moore Hensley",
//     friends: ["Sharron Pace"],
//     gender: "male"
//   }
// ]
```

### Zadanie 4. Saldo

Napisz funkcję strzałkową `getTotalBalanceByGender(users, gender)`, która przyjmuje dwa parametry:

* pierwszy parametr `users` — tablica obiektów użytkowników,
* drugi parametr `gender` — ciąg znaków przechowujący płeć.

Funkcja powinna używać łańcucha wywołań metod i zwracać saldo użytkowników (właściwość `balance`), których płeć (właściwość `gender`) odpowiada wartości parametru gender.



Weź poniższy kod i wklej go po deklaracji swojej funkcji, aby sprawdzić, czy działa poprawnie. Wyniki jego działania zostaną wyświetlone w konsoli.
```
const allUsers_2 = [
	{
    name: "Moore Hensley",
    gender: "male",
    balance: 2811
  },
  {
    name: "Sharlene Bush",
    gender: "female",
    balance: 3821
  },
  {
    name: "Ross Vazquez",
    gender: "male",
    balance: 3793
  },
  {
    name: "Elma Head",
    gender: "female",
    balance: 2278
  },
  {
    name: "Carey Barr",
    gender: "male",
    balance: 3951
  },
  {
    name: "Blackburn Dotson",
    gender: "male",
    balance: 1498
  },
  {
    name: "Sheree Anthony",
    gender: "female",
    balance: 2764
  }
];

console.log(getTotalBalanceByGender(allUsers_2, "male")); // 12053

console.log(getTotalBalanceByGender(allUsers_2, "female")); // 8863
```
