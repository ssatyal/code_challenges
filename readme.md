a repo for reddit code challenges from dailyprogrammer

## challenge 1

prompt:
create a program that will ask the users name, age, and reddit username. have it tell them the information back, in the format:
your name is (blank), you are (blank) years old, and your username is (blank)

```js
var name = prompt("name?");
var age = prompt("age?");
var username = prompt("reddit username?");

alert("your name is "+name+", you are "+age+" years old, and your username is "+username);
```

##challenge 3

prompt:
write a program that can encrypt texts with an alphabetical caesar cipher. This cipher can ignore numbers, symbols, and whitespace.
for extra credit, add a "decrypt" function to your program!

```js
//solution without worrying about numbers, symbols, whitespace
//only input is string with letters

var letters = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z'];

var store = [];
var map = [];

var encrypt = function(word){
	store = word.split("");
	for (var i = 0; i<store.length; i++){
		var a = letters.indexOf(store[i]) - 1;
		map.push(letters[a]);
	}
	return map.join("");
}

encrypt("hello");
```

## challenge 8

prompt: write a program that will print the song "99 bottles of beer on the wall".

```js
for (var i = 99; i >= 0; i--){
	if (i===1){
		console.log(i + " bottle of beer on the wall, "+i+" bottle of beer, you take one down, pass it around, "+(i-1)+" bottles of beer on the wall.")
	}else if(i===0){
		console.log("Woops, no more bottles of beer on the wall. We are all drunk now.")
	}else{
	console.log(i + " bottles of beer on the wall, " + i+ " bottles of beer, you take one down, pass it around, " + (i-1)+ " bottles of beer on the wall.")
	}
}
```

## challenge 11

prompt: The program should take three arguments. The first will be a day, the second will be month, and the third will be year. Then, your program should compute the day of the week that date will fall on.
