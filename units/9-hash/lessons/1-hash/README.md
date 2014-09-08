#Lesson 1 - Hashes

![image](http://i.imgur.com/FWOuXvf.jpg)

## Before class

### Objective

Students will be able to create, initialize, access, manipulate, and iterate through hashes.

### Key points

* Hashes, like arrays, are used to store data.
* Unlike arrays, hashes represent an unordered list through key-value pairs.
* Hashes can be stored inside hashes.

### Assessment

1. Write do-now based off of [assessments from previous lesson](../../../7-array-loop/lessons/1-array/assessments/).
2. Write exit-ticket based off [assessments from current lesson](assessments/).

Students will show progress toward reaching the objective based on their performance on the exit-ticket quiz.

### Vocabulary

* Curly brace
* Key-value pair
* For-in loop

### References

* http://www.javascriptkata.com/2007/03/29/how-to-use-javascript-hashes/

## During class

### Do-now

1. Attendance: Teacher takes student attendance at www.kinvolved.com
2. Return graded do-now and exit ticket from previous class
3. Do-now quiz

### Opening

Today we will learn about hashes. This is important because hashes are a tool that programmers use to store a large set of unordered data. It connects to what we've previously learned because we will be able to perform array like operations with hashes. 

Someone give me an example of an ordered list in real life. A recipe is an example. An instruction manual is another. Now give me an example of an unordered list in real life. A grocery list is one. A classroom contains a list of chairs in no particular order. Let's talk how about how we can represent these kind of lists in JavaScript.

### Introduction of new material ("I do")

####Create and initialize a hash

```
var animalSounds = {"cow": "Moo", "cat": "Meow", "dog": "Woof"};
```

Let's break this down right to left. Note the **open curly brace** (`{`) and **close curly brace** (`}`). These braces specify the beginning and end of the hash. This particular hash has three **key-value** pairs. Note that each key-value pair is separated by a comma. We then take this hash and store in a variable called `animalSounds`.

Let's talk about the key-value pairs more. In this hash, `cow`, `cat`, and `dog` represent keys. `"Moo"`, `"Meow"`, and `"Woof"` represent those keys' respective values. These values happen to be strings.

####Access and print an element of a hash

```
console.log(animalSounds["cat"]);
```

This prints out `Meow`. Here, `cat` is the key. Whereas with arrays we use indices to access elements, with hashes we use keys.

What if we want to access and print the value corresponding to the `dog` key of our hash?

```
console.log(animalSounds["dog"]);
``` 

This prints out `Woof`. 

And how about the value corresponding to the `cow` key?

```
console.log(console.log(animalSounds["cow"]);
```

This prints out `Moo`. 


####Change the value of a key-value pair in a hash

Let's change `cat`'s value:

```
animalSounds["cat"] = "Purr";
console.log(animalSounds["cat"]);
```

This prints out `Purr`.

####Add a key-value pair to the hash

What if we want to add another animal-sound pair to our hash? We can:

```
animalSounds["snake"] = "Hiss";
console.log(animalSounds["snake"]);
```

This prints out `Hiss`. 

####Iterate

What if we want to print every element in our hash? We can:

```
var animalSounds = {"cow": "Moo", "cat": "Meow", "dog": "Woof"};

for (key in animalSounds) 
{ 
  console.log("key: " + key + ", value: " + animalSounds[key]); 
}
```

This is an example of a **for-in** loop. It will print each key-value pair in the hash. The above prints:

```
key: cow, value: Moo
key: cat, value: Meow
key: dog, value: Woof
```

####Remove key-value pair

What if we want to remove a key-value pair from our cash? We can:

```
var animalSounds = {"cow": "Moo", "cat": "Meow", "dog": "Woof"};

delete animalSounds["dog"];

for (key in animalSounds) 
{ 
  console.log("key: " + key + ", value: " + animalSounds[key]); 
}
```

prints:

```
key: cow, value: Moo
key: cat, value: Meow
```

####Hash in a hash

Like Matryoshka dolls (see picture at top), we can store hashes inside of other hashes:

```
var animalSounds = 
{
  "cow": "Moo", 
  "cat": "Meow", 
  "dog": "Woof",
  "bird": {robin: "Chirp", swan: "Cry"}
};

var birdSounds = animalSounds["bird"]

console.log(birdSounds["swan"]); 
```

Here, the `bird` key has a value that is a hash. So we first unload that hash into its own variable. Then we access it like any other hash.

Think about why we used a hash inside a hash here. We could have just added two more key-value pairs to the `animalSounds` hash. But we didn't because we want to use the keys in that hash to represent *types* of animals, not specific kinds.

### Guided practice ("We do")

Now we're going to work with hashes together. 

``var worldCapitals = {"United States" : "Washington D.C.", "United Kingdom": "London", "China" : "Beijing", "Bangladesh" : "Dhaka"}``

1. How do I print out China's capital?
2. How do I change the United States' capital?
3. How do I add one country-capital pair to the hash?
4. How do I remove Bangladesh's key-value pair?
5. How do I print each capital in our hash without having to access each one individually?

### Independent practice ("You do")

Create a hash that has five key-value pairs. The hash can represent anything.

1. Print out each value without using a loop.
2. Change two of the values.
3. Add a key-value pair to your hash.
4. Remove a key-value pair from your hash (cannot be the one you added in step 3).
5. Print each key and value using a loop.

#### Exit ticket

Give exit-ticket quiz.

### Closing

Today you learned about hashes. This is important because hashes are used to represent unordered list. Next, we will learn about jQuery.

#### Homework

[Link to homework](homework/)

Remind students when homework is due and how it will be collected.

## After class

* Grade do-now & exit-ticket. Record in class spreadsheet.
* Prepare for next lesson / hand off to next volunteer in rotation.
