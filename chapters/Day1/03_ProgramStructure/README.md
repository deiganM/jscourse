# 3. Program Structure

-   just writing expressions is not enough. We need a way to organize our code
-   we need a way to control the flow of our code, and make decisions

### Logic - If statements

If:
```js
if (something) {
  // do something...
}

```
If Else:
```js
if (something) {
  // do something...
} else {
  // otherwise, always do this thing
}
```

If, If Else, Else:
```js
if (something) {
  // do something...
} else if (somethingElse) {
  // else do this...
} else {
  // otherwise, always do this thing
}
```

```js
// Example if, if else, else scenario:
let num = Number(prompt("Pick a number"));

if (num < 10) {
  console.log("Small");
} else if (num < 100) {
  console.log("Medium");
} else {
  console.log("Large");
}
```

### Logic - Switch Statements

```js
switch (prompt("What is the weather like?")) {
  case "rainy":
    console.log("Remember to bring an umbrella.");
    break;
  case "sunny":
    console.log("Dress lightly.");
  case "cloudy":
    console.log("Go outside.");
    break;
  default:
    console.log("Unknown weather type!");
    break;
}
```

### Loops - Do While Loops
```js
let number = 0;
while (number <= 12) {
  console.log(number);
  number = number + 2;
}
```

### Loops - For Loops

##### For Loops
```js
for (let number = 0; number <= 10; number++) {
  console.log(number);
}
```
##### Incrementing a number
```js
let number = 1
number++ // this is now 2
```


### Representing data as a list
```js
const myNavigationList = [
  'About',
  'Services',
  'Contact us'
]

const myShoppingList = [
  'Bananas',
  'Apples',
  'Oranges'
]

const myProductList = [
  'Lite Plan',
  'Regular Plan',
  'Pro Plan'
]

const myProductListWithDetails = [
  {
    name: 'Lite Plan',
    price: 20
  },
  {
    name: 'Regular Plan',
    price: 40
  },
  {
    name: 'Pro Plan',
    price: 80
  }
]

const myOnlineClothingProducts = [
  {
    name: 'Shirt 1',
    price: 20
  },
  {
    name: 'Shirt 2',
    price: 40
  },
  {
    name: 'Jeans 1',
    price: 80
  }
]

const myProjectListForMyPortfolio = [
  {
    name: 'Blog',
    img: 'https://my-portfolio-assets.s3.amazonaws.com/img1/png',
    githubUrl: 'https://github.project1.com'
  },
  {
    name: 'Ecommerce Site',
    img: 'https://my-portfolio-assets.s3.amazonaws.com/img2/png',
    githubUrl: 'https://github.project2.com'
  },
  {
    name: 'ScoreBoard App',
    img: 'https://my-portfolio-assets.s3.amazonaws.com/img3/png',
    githubUrl: 'https://github.project3.com'
  }
]

```



### Looping - over data
```js
for (movie of movieData) {
    console.log(movie.title)
}
```

Examples of looping over a list
```js
let playerScores = [30, 40, 60]

for (score of playerScores) {
    console.log(score + ' points')
}
```

Examples of looping over a list with objects
```js
let players = [
    {
        name: 'John',
        score: 30
    },
    {
        name: 'James',
        score: 40
    },
    {
        name: 'Jessica',
        score: 60
    }
]

for (player of players) {
    console.log(player.score + ' points')
}
```

## Simple List Exercises

#### Exercise 1
```js
const todoList = [
  'Workout',
  'Buy Groceries',
  'Respond to Emails',
  'Water Plants'
]

```
Loop through the todo list above and console.log `listItem - DONE`

#### Exercise 2
```js
const todoList = [
  { 
    name: 'Workout',
    done: true
  },
  { 
    name: 'Buy Groceries',
    done: true
  },
  { 
    name: 'Respond to Emails',
    done: false
  },
  { 
    name: 'Water Plants',
    done: false
  }
]

```
Loop through the todo list above and console.log `listItemName - DONE` if the done property is true,
otherwise, just console.log the listItemName


## Movie Database Exercises
Download the MovieDatabase js file
- [Movie Data JS File](https://htmlbasicsresources.s3.amazonaws.com/movieData.js.zip)

Include this js file in a project with the following folder structure:
```
index.html
movieData.js
app.js
```

Use this as a starter for your index.html file:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <meta http-equiv="X-UA-Compatible" content="ie=edge" />
        <title>Document</title>
    </head>
    <body>
        <script src="./movieData.js"></script>
        <script src="./app.js"></script>
    </body>
</html>
```

To start working with the data in movieData.js, we can reference movieData as a variable in our app.js file. The reason we can reference this variable is because we defined that movieData variable in the first js file (which you downloaded), and that variable is available to you in the app.js file.

#### Exercise 1
- `console.log` all movies in 1919

(hint: if you are just trying to see what 1 item looks like, you can reference the first item of an array like this: `myList[0]`)

#### Exercise 2
- `console.log` the number of movies in 1919

#### Exercise 3
- If the movie title has the word `Prejudice` in it, console.log `movieTitle - 7/10`
- If the movie title has the word `Pride` in it, console.log `movieTitle - 8/10`
- If the movie title has the word `Pride` and `Prejudice` in it, console.log `movieTitle - 9/10`
- If the movie title has the word `Pride` and `Prejudice` and `Zombies` in it, console.log `movieTitle - 10/10`

(hint: there should be no duplicates in the result, there should be a total of 23 results)
(hint: googling `js string includes` might help)

#### Exercise 4
- If the movie has Benedict Cumberbatch in it, console.log `movieTitle - 8/10`
- If the movie has Robert Downey in it, console.log `movieTitle - 9/10`
- If the movie has Robert Downey and Benedict Cumberbatch in it, console.log `movieTitle - 10/10`

(hint: there should be a total of 61 results)


