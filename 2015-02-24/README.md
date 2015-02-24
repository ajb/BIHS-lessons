## Objectives

- Students will be know how many parameters ("inputs") to pass to a function (this is something they have consistently gotten wrong)
- Students will have an improved understanding of "pseudo-code", and will be able to convert it to real code
- Students will be able to use `if` and `if...else` statements

## Do now

Define and call a function called "sayFriends":

  - The function has three inputs: "my name", "friend one" and "friend two"
  - The function should `return` a sentence that looks like this:
    "My name is MYNAME. My friends are FRIEND ONE and FRIEND TWO".

Hint: You'll need to use the `+` operator when creating your sentence.

### Discussion points

- What's the difference between defining and calling? How do we know which is which?
- Why do we use `+`? What would happen if we just put the variable inside the string?
- What is a string? Sequence of characters, a word, or multiple words

### Answer

```js
function sayFriends(myName, friendOne, friendTwo) {
  return 'My name is ' + myName + '. My friends are ' + friendOne + ' and ' + friendTwo + '.';
}

console.log( sayFriends('Adam', 'Manish', 'Becca') );
```

## I do

- I'm going to write a small program that plays a number game.
- It will choose a random number, between 1 and 5.
- It will then ask the user to choose a number
- If the numbers match, it will log "You win!"
- Otherwise, it will log "You lose! The number was NUMBER"

I heard generating random numbers is hard, so I found a function to do it for me:

```js
function getRandomNumber(min, max) {
  return '' + (Math.floor(Math.random() * (max + 1 - min)) + min);
}
```

- Now what am I going to do next... does anyone remember what pseudo-code is?
- Is there pseudo code anywhere on the screen? (yes)
- Now let's just follow the pseudo code we wrote:

```js
var randomNumber = getRandomNumber(1, 5);
var usersNumber = prompt("Choose a number...");
```

- Now here's the new part -- does anyone know how we can check if the numbers match?
- Yep, it's easy, it's called an "if" statement
- Two equals signs for _comparing_

```js
if (randomNumber == usersNumber) {
  console.log("You win!");
}
```

- What's the opposite of an "if"? (Else)

```js
else {
  console.log("You lose! The number was " + randomNumber);
}
```

- Let's put it together and run it... 

## We do

We're going to try a different one -- we gave this to you as homework, but I want to go back to it.

The function asks for the users name.
It then calculates the length of the name (what is length?)
If there are more than 6 characters, it says "Your name is long!"
Otherwise, it says "Your name is short!"

We'll start with the following code:

```js
function getLengthOfName(name) {
  return name.length;
}
```

Complete code:

```js
var name = prompt("What's your name?");
var nameLength = getLengthOfName(name);

if (nameLength > 6) {
  console.log("Your name is long!");
} else {
  console.log("Your name is short!");
}
```

## You do

Create this function:

- Generate a random number between 1 and 10 (you can use the function from earlier)
- As the user to guess *two* numbers
- If either of their guesses match, then log "You win"
- Otherwise, log "You lose"

Hint: you will need to use the `||` operator: See "logical operators" here: http://www.w3schools.com/js/js_comparisons.asp

## Homework

- Homework today is short, because I want everyone to complete it by Thursday:

Write a function that returns the result of the following equation: 5a^2 + 4b + c. 

- You should use the pow() function. 
- Your function should take in three parameters (a,b,c).
