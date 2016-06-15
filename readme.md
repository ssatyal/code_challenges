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

```js
//month starts at 0 for Jan
var calc = function(year, month, day){
	var d = new Date(year, month, day);
	return d.getDay();
}

calc(2016, 5, 9);
```

##challenge 16

prompt: Write a function that takes two strings and removes from the first string any character that appears in the second string. For instance, if the first string is “Daily Programmer” and the second string is “aeiou ” the result is “DlyPrgrmmr”.
note: the second string has [space] so the space between "Daily Programmer" is removed

```js
var string1 = [];
var string2 = [];

var check = function(one, two){
	string1 = one.split("");
	string2 = two.split("");
	for (var i=0; i < string1.length; i++){
		for (var j=0; j < string2.length; j++){
			if (string1[i] == string2[j]){
				string1.splice(i, 1);
			}
		}
	}
	return string1.join("");
}

check("daily", "programmer");
```

## challenge 17

prompt: write an application which will print a triangle of stars of user-specified height, with each line having twice as many stars as the last. sample output:
@
@@
@@@@

```js
var str = '';
var makeIt = function(number){
	for (var i=1;i<=number; i++){
		console.log(str += "@");
	}
};

makeIt(10);
```
## challenge 20[i]
prompt: create a program that will take user input and tell them their age in months, days, hours, and minutes
```js
var check = function(years){
	var months = years * 12;
	var days = years * 365;
	var hours = years * 365 * 24;
	var minutes = years * 365 * 24 * 60;
	console.log("months: " + months + ", days: " + days + ", hours: "+hours+", and minutes: "+minutes);
}

check(18);
```
