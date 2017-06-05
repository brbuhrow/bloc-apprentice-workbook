# Module 1 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

## HTML

### Questions

1. What is HTML and what is it used for?
Hypertext Markup Language is used to create files on the internet.
2. What is the difference between an ID and a class?
ID refers to one element while class can cover a scope of elements.
3. What does it mean to write "semantic" HTML?
Writing semantic HTML creates the meaning to the elements rather than just the presentation. h1 gives meaning to all related "h1" headings.

### Exercises

1. Write a paragraph tag with a class of "highlight" and content "Watch out!".
<p class="highlight">Watch out!</p>
2. Write an HTML image tag to show an image called `profile-picture.jpg`.
<img src="profile-picture.jpg">
3. Write a link tag that links to http://google.com.
<a href="http://google.com"> </a>
5. Write an complete standard HTML document outline (including a DOCTYPE, and `<html>`, `<head>`, and `<body>` tags).

<!DOCTYPE html>
<html>
<head>

</head>
<body>

</body>
</html>

6. Inside of the code for the previous exercise, write the appropriate tag to link to a script file called `main.js`.

<!DOCTYPE html>
<html>
<head>
<script src="main.js"></script>
</head>
<body>

</body>
</html>

7. Inside of the code for the previous exercise, write the appropriate tag to link to a stylesheet file called `main.css`.


<!DOCTYPE html>
<html>
<head>
<script src="main.js"></script>
<link rel="stylesheet" href="main.css"/>
</head>
<body>

</body>
</html>

8. Write a numbered list in HTML and list three of your favorite books.

<ol>
<li>How to Win Friends and Influence People</li>
<li>The Obstacle is the Way</li>
<li>Onward</li>
</ol>

9. Fix the indentation of the following HTML sample:

  ```html
  <div>
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ul>
  </div>
  ```

## CSS

### Questions

1. What is CSS and what is it used for?
CSS stands for cascading style sheets and is used to create the presentation for which HTML is to be displayed.
2. What is the CSS box model?
This is a box that wraps around each element and is made up of the padding, margin, and border.
3. What's the difference between margin and padding?
Margin adjusts the outer space of an element while padding adjusts the inner space of the element. 

### Exercises

1. Write a CSS rule to make the text of all `h1` tags red.

h1 {
  color: #FF0000
}

2. Write a CSS rule to make the background color of the link with `class="btn"` blue:

  ```html
  <a href="#" class="btn">Learn more</a>
  ```
a.btn {
  background-color: #0000FF
  }

3. Write a CSS rule to give the first paragraph in the following HTML a font size of `20px`, but not the second paragraph.

  ```html
  <header class="jumbotron">
    <p>Hello, World!</p>
  </header>

  <p>Welcome to this awesome website!</p>
  ```
header.jumbotron p {
  font-size: 20px 
}

## JavaScript

### Questions

1. What is a function? What are they used for?
A function is something that uses a step-by-step process to do something repeatedly.
2. What is the difference between `==` and `===`?
== allows the compiler to ignore numbers and numbers in a string while === does not ignore numbers and numbers in a string.
3. What is the difference between global and local scope variables?
global scope variables are accessible throughout the entire code, while local scope vairables are only accessible within their function.
4. What is a boolean value?
A boolean value returns a value that is either true or false. Example would be: 3 > 2 :returns a true statement 
5. What is an array?
An array is a group of elements that are grouped together under a single location.
### Exercises

1. Write a line that declares a variable called `myName` and set its value to your name.
var myName = "Ben"

2. Write a loop that logs the numbers 1 through 10 to the console.
var number = 0
while (number >= 0 && number<= 10) {
  console.log(number);
  number++;
}

3. Translate the following pseudocode into JavaScript: if `score` is greater than `3` and `lives` is greater than `0`, alert "You win!".
var score = 0;
var lives = 0
if (score > 3 && lives > 0) {
alert("You win!");
}

4. Write a function `sayHello` that takes one argument, a name, and logs "Hello, <name>!" to the console. Then, call the function below the function definition and pass in your name as the argument.

var sayHello = function(name) {
console.log("Hello, " + name + "!");
};
sayHello("Ben")

5. What would the following script log to the console?

  ```javascript
  var currentSong = "Call Me Maybe";

  function setSong(song) {
    currentSong = song;
  }

  setSong("Friday, Friday");

  console.log(currentSong);
  ```
The console would log the current song as "Friday Friday" 

6. What would the following script log to the console?

  ```javascript
  var add = function(a, b) {
    return a + b;
  }

  var result = add(3, 7);

  console.log(result);
  ```
The console would log 10. 

7. What would the following script log to the console?

  ```javascript
  var helloGoodbye = function(name) {
    return sayHello(name) + " " + sayGoodbye(name);
  }

  var sayHello = function(name) {
    return "Hello " + name + "!";
  }

  var sayGoodbye = function(name) {
    return "Goodbye " + name + "!";
  }

 console.log(helloGoodbye("Sarah"));
  ```
This would log:  Hello Sarah! Goodbye Sarah!

8. Write a function `findLongestWord()` that takes an array of words and returns the length of the longest one.

function findLongestWord(wordArray) {
  var wordLength = 0;
  for (var index = 0; index < wordArray.length; index++) {
    if (wordArray[index].length > wordLength) {
      wordLength = wordArray[index].length;
    } 
  }
  console.log(wordLength);
  return wordLength;
  
}

findLongestWord(["Cat", "Banana", "Elephant", "Dog"]);

9. Define a function `sum()` that sums all the numbers in an array of numbers. For example, `sum([1,2,3,4])` should return 10.

var numbers = [5,2,9,32];
var totalAmount = 0;
for (var i = 0; i < numbers.length; i++) {
    totalAmount += numbers[i];
}  

console.log(totalAmount);

10. Write a function that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.

var vowelArray = ["a","e","i","o","u"];

var vowelFinder = function(letter) {
  for (var i = 0; i < vowelArray.length; i++) {
    if (letter == vowelArray[i]) {
      return true;
    }   
  }
  return false;
}
  
console.log(vowelFinder("z"));

11. Write the correct line to make `"Woof!"` show up in the console based on this script:

  ```javascript
  var pet = {
    name: "Charles",
    goodDog: true,
    speak: function() {
      console.log("Woof!");
    }
  };
  ```
pet.speak();

12. Using the same script as above, write the correct line to log the dog's name to the console.

var pet = {
    name: "Charles",
    goodDog: true,
    speak: function() {
      console.log("Woof!");
    }
  };
  
console.log(pet.name);  
  
## Command Line

### Questions

1. What is the command line and what is it used for?
The command line is used for navigating through a server.
2. What does the command `ls` do?
This command shows the list of files in the current, working directory.
3. What does the command `pwd` do?
shows the working directory that you are in. (Print working directory)
4. What does the following command do: `cd my-cool-project`
This changes the directory to "my-cool-project".

### Exercises

1. Write the command to make a new directory called "my-cool-project".
>mkdir my-cool-project
2. Write the command to create a file called "index.html".
> git touch "index.html"
3. Write the command to delete a file called "main.css".
> git rm "main.css"

## Git

### Questions

1. What is Git and what is it used for?
Git is a repository where information/code can be pushed into one location, allowing for callaboration and/or gobal accessibility to projects.
2. What's the difference between a local repository and a remote repository?
A local repository has data that is only accesible from a single location while a remote repository is accessible on a global level. 

### Exercises

1. Write the command that you would use to create a new local Git repository.
> git init
2. Write the command to stage a file called `index.html` to be committed.
> git add index.html
3. Write the command to view the current status of the git repository.
> git status
