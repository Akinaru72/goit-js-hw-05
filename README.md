# Homework №5

## Instructions

- Create a repository **goit-js-hw-05** and clone it to your computer.
- In the `goit-js-hw-05` folder, create the project structure as shown in the diagram below.

![Project preview](assets/goit-js-05.jpg)

⚠️ **Attention!**  
File and folder names, as well as their nesting structure, must **exactly match** the specified scheme. Otherwise, the work will not be accepted.

- Read each task carefully and complete it in the corresponding file.
- Make sure the code is formatted using **Prettier**.
- When opening the live page, there should be no errors or warnings in the console.
- Submit the homework for review.

---

## Submission format

The homework must contain **two links**:

- a link to the source files (repository with the code);
- a link to the live page on **GitHub Pages**.

---

## Task 1. User names

**File:** `task-1.js`

Write an **arrow function** `getUserNames(users)` that takes one parameter `users` — an array of user objects.

The function should return an array of **all user names** (the `name` property) from the `users` array.

---

### Code for testing

Take the code below and paste it after declaring your function to check that it works correctly.  
The results of the function calls will be logged to the console.

```js
console.log(
  getUserNames([
    {
      name: "Moore Hensley",
      email: "moorehensley@indexia.com",
      balance: 2811,
    },
    {
      name: "Sharlene Bush",
      email: "sharlenebush@tubesys.com",
      balance: 3821,
    },
    {
      name: "Ross Vazquez",
      email: "rossvazquez@xinware.com",
      balance: 3793,
    },
    {
      name: "Elma Head",
      email: "elmahead@omatom.com",
      balance: 2278,
    },
    {
      name: "Carey Barr",
      email: "careybarr@nurali.com",
      balance: 3951,
    },
    {
      name: "Blackburn Dotson",
      email: "blackburndotson@furnigeer.com",
      balance: 1498,
    },
    {
      name: "Sheree Anthony",
      email: "shereeanthony@kog.com",
      balance: 2764,
    },
  ])
);
// ["Moore Hensley", "Sharlene Bush", "Ross Vazquez", "Elma Head", "Carey Barr", "Blackburn Dotson", "Sheree Anthony"]
```

Leave this code for the mentor to review.

---

## What the mentor will pay attention to during the review:

- The variable `getUserNames` is declared
- The variable `getUserNames` is assigned an **arrow function** with parameter `(users)`
- The `map()` method is used to iterate over the `users` parameter
- Calling the function with the specified array of users returns the array  
  `["Moore Hensley", "Sharlene Bush", "Ross Vazquez", "Elma Head", "Carey Barr", "Blackburn Dotson", "Sheree Anthony"]`
- Calling the function with random but valid arguments returns the correct value

---

## Task 2. Users with a friend

**File:** `task-2.js`

Write an **arrow function** `getUsersWithFriend(users, friendName)` that takes two parameters:

- `users` — an array of user objects
- `friendName` — the name of a friend to search for

The function should return an array of all users from the `users` array who have a friend with the name `friendName`.

Each user’s friends are stored in the `friends` property.

If there are no users with the specified friend, the function should return an **empty array**.

---

### Tips:

- You can use the `filter()` method to create a new array with elements that satisfy a condition
- Use the `includes()` method to check whether the `friends` array contains `friendName`

---

### Test code

Use the code below **after declaring your function** to check that it works correctly.  
The console will display the results of its execution.

```js
const allUsers = [
  {
    name: "Moore Hensley",
    friends: ["Sharron Pace"],
  },
  {
    name: "Sharlene Bush",
    friends: ["Briana Decker", "Sharron Pace"],
  },
  {
    name: "Ross Vazquez",
    friends: ["Marilyn Mcintosh", "Padilla Garrison", "Naomi Buckner"],
  },
  {
    name: "Elma Head",
    friends: ["Goldie Gentry", "Aisha Tran"],
  },
  {
    name: "Carey Barr",
    friends: ["Jordan Sampson", "Eddie Strong"],
  },
  {
    name: "Blackburn Dotson",
    friends: ["Jacklyn Lucas", "Linda Chapman"],
  },
  {
    name: "Sheree Anthony",
    friends: ["Goldie Gentry", "Briana Decker"],
  },
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

console.log(getUsersWithFriend(allUsers, "Adrian Cross")); // []
```

Leave this code for the mentor to review.

---

## What the mentor will pay attention to during the review:

- The variable `getUsersWithFriend` is declared
- The variable `getUsersWithFriend` is assigned an **arrow function** with parameters `(users, friendName)`
- The `filter()` method is used to iterate over the `users` parameter
- If the value of the `friendName` parameter is the string `"Briana Decker"`, the function returns an array of user objects with the names **Sharlene Bush** and **Sheree Anthony**
- If the value of the `friendName` parameter is the string `"Goldie Gentry"`, the function returns an array of user objects with the names **Elma Head** and **Sheree Anthony**
- If the value of the `friendName` parameter is the string `"Adrian Cross"`, the function returns an **empty array**
- Calling the function with random but valid arguments returns the correct result

---

## Task 3. Sorting by Number of Friends

**File:** `task-3.js`

Complete this task in the `task-3.js` file.

Write an **arrow function** `sortByDescendingFriendCount(users)` that takes one parameter `users` — an array of user objects.

The function should return an array of **all users**, sorted in **descending order** by the number of their friends (the `friends` property).

---

### Code for testing

Take the code below and paste it after declaring your function to verify that it works correctly.  
The results of its execution will be logged to the console.

```js
console.log(
  sortByDescendingFriendCount([
    {
      name: "Moore Hensley",
      friends: ["Sharron Pace"],
      gender: "male",
    },
    {
      name: "Sharlene Bush",
      friends: ["Briana Decker", "Sharron Pace"],
      gender: "female",
    },
    {
      name: "Ross Vazquez",
      friends: ["Marilyn Mcintosh", "Padilla Garrison", "Naomi Buckner"],
      gender: "male",
    },
    {
      name: "Elma Head",
      friends: ["Goldie Gentry", "Aisha Tran"],
      gender: "female",
    },
    {
      name: "Carey Barr",
      friends: ["Jordan Sampson", "Eddie Strong"],
      gender: "male",
    },
    {
      name: "Blackburn Dotson",
      friends: ["Jacklyn Lucas", "Linda Chapman"],
      gender: "male",
    },
    {
      name: "Sheree Anthony",
      friends: ["Goldie Gentry", "Briana Decker"],
      gender: "female",
    },
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

Leave this code for mentor review.

---

## What the mentor will pay attention to during the review:

- The variable `sortByDescendingFriendCount` is declared
- The variable `sortByDescendingFriendCount` is assigned an **arrow function** with the parameter `(users)`
- The `toSorted()` method is used to iterate over the `users` parameter
- Calling the function with the specified `users` array returns a **new array of users**, sorted **in descending order by the number of their friends**
- Calling the function with random but valid arguments returns the correct value

---

## Task 4. Total balance

Write an **arrow function** `getTotalBalanceByGender(users, gender)` that takes two parameters:

- `users` — an array of user objects;
- `gender` — a string that represents gender.

The function should **use a method chaining approach** and return the **total balance of users** (the `balance` property) whose gender (the `gender` property) matches the value of the `gender` parameter.

---

### Code for testing

Take the code below and paste it after declaring your function to verify that it works correctly.  
The results of its execution will be displayed in the console.

```js
const clients = [
  {
    name: "Moore Hensley",
    gender: "male",
    balance: 2811,
  },
  {
    name: "Sharlene Bush",
    gender: "female",
    balance: 3821,
  },
  {
    name: "Ross Vazquez",
    gender: "male",
    balance: 3793,
  },
  {
    name: "Elma Head",
    gender: "female",
    balance: 2278,
  },
  {
    name: "Carey Barr",
    gender: "male",
    balance: 3951,
  },
  {
    name: "Blackburn Dotson",
    gender: "male",
    balance: 1498,
  },
  {
    name: "Sheree Anthony",
    gender: "female",
    balance: 2764,
  },
];

console.log(getTotalBalanceByGender(clients, "male")); // 12053
console.log(getTotalBalanceByGender(clients, "female")); // 8863
```

Leave this code for the mentor to review.

---

## What the mentor will pay attention to during the review:

- The variable `getTotalBalanceByGender` is declared
- The variable `getTotalBalanceByGender` is assigned an **arrow function** with parameters `(users, gender)`
- A **method chaining** approach is used inside the function body in the correct order
- The value of the `users` parameter is **not mutated**
- If the value of the `gender` parameter is the string `"male"`, the function returns the number `12053`
- If the value of the `gender` parameter is the string `"female"`, the function returns the number `8863`
- Calling the function with random but valid arguments returns the **correct value**

---

**Live page: [GitHub Pages](https://akinaru72.github.io/goit-js-hw-05/)**
