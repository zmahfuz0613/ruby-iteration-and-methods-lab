# The Ruby Gauntlet Lab
![](https://media.giphy.com/media/10fBhxySxYZfHy/giphy.gif)

Let's get some practice with basic Ruby! This repository contains a series of mini labs challenging you to write basic Ruby programs to solve problems.

To get started, `mkdir` a folder called `ruby_practice` and `cd` into it. 

## Calculator
Let's warm up by making some methods to do basic math.
- In your `ruby_practice` folder, `touch` a file called `calculator.rb`
- Define a method called `add` that takes two numbers and adds them together. On the first line of this function, do the actual math; on the second line, use `puts` to print the expression and answer.
- Following this pattern, define methods for `subtract`, `multiply`, and `divide`. 
  - >Hint: Review how division works in Ruby...
- Define a method called `calculate`. This method will not need to take any parameters.
- Inside `compute` use `puts` to ask the user for the first and second number and `gets.chomp` let the user input those numbers and store those store them to variables. 
  - >Hint: Check the data type of your newly collected variables...
- Call `add`, `subtract`, `multiply`, and `divide` using the two numbers you just stored as the arguments for each.
- Make sure to end any open blocks and close the `calculate` method.
- Below your newly defined method, call `calculate`.
- Go back to the terminal and run the file you just created with `ruby calculator.rb`

The end result should look something like this when run in your terminal:
```
Enter first number:
5

Enter second number:
3

5 + 3 = 8
5 - 3 = 2
5 * 3 = 15
5 / 3 = 1.6666666666666667
```

If you're stuck, start by taking a look at how methods are defined and called in Ruby in our [intro lesson](https://git.generalassemb.ly/sei-nyc-pandas/ruby).


<details><summary>Help! I'm still stuck!</summary>
 The first method should look something like this:

```
def add(num1, num2)
  answer = num1 + num2
  puts "#{num1} + #{num2} = #{answer}"
end
```

</details>


<details><summary>I'm STILL stuck!</summary>
Here is the structure of calculate:

```
def calculate
  puts "Enter first number:"
  num1 = gets.chomp.to_i
  puts ""
  puts "Enter second number:"
  num2 = gets.chomp.to_i
  puts ""
  add(num1,num2)
  subtract(num1,num2)
  multiply(num1,num2)
  divide(num1,num2)
end

calculate
```

</details>

## Letter Guesser
- In your folder, `touch` a file called `letter.rb`.
- Define a method called `letter_guesser`.
- Inside your method, create an array from "a" to "z" using the `range` syntax and save this array to a variable.
- Using `rand`, generate a random number between 0 and the length of your alphabet array. Save this number to a variable.
- Use that random number as an index and select the correlating letter from your alphabet array.
- Using string interpolation, inform the user what letter they have received and ask them to guess the letter's index number.
- Save the user's answer to a variable with `gets.chomp`.
- Use conditional logic to check if the user's guess matches the actual index of the random letter. If it does, tell them that they're a genius at the alphabet; if it doesn't match, tell them that they need to learn their ABCs and use string interpolation to give them the correct answer.
- Make sure to close your `letter_guesser` method with `end`.
- Call `letter_guesser`.
- Go back to the terminal and run the file you just created with `ruby letter.rb`


The result should look something like this in your terminal:

```
Your letter is c. Guess c's index number.
2
Whoa! You're like a genius when it comes to the alphabet!
```

```
Your letter is z. Guess z's index number.
1 
You lose! Looks like you need to learn your ABC's. The index of z is actually 25.
```

## FizzBuzz in Ruby
Remember FizzBuzz? It's that puzzle where you iterate from 1 to 100, printing "Fizz" for every multiple of 3, "Buzz" for everything multiple of 5, and "FizzBuzz" for every multiple of 3 && 5. All other numbers should just print themselves.

Let's write a solution for FizzBuzz in Ruby using a method with conditional logic.

- In your folder, `touch` a file called `fizzbuzz.rb`
- Open this file in your text editor and define a method called `fizzbuzz`. This method will not need any parameters.
- OPTION A: Use the `.times do |num|` iterator to create a block where you iterate 100 times. Then use conditional logic to establish conditions for Fizz, Buzz, and FizzBuzz.
- OPTION B: Create a `range` from 1 to 100 and iterate through it with `.each do |num|`. Then use conditional logic to establish conditions for Fizz, Buzz, and FizzBuzz.
- Make sure to end any open blocks and close the method.
- Below your newly defined method, call `fizzbuzz`.
- Go back to the terminal and run the file you just created with `ruby fizzbuzz.rb`

The result should look something like this in your terminal:

```
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
(etc to 100)
```


## UNCLE writing ON facebook WALL app
- In your folder, create a file called `uncle_speak.rb`. 
- Open this file in your text editor and define a method called `uncle_speak`. This method will not need any parameters.
- Inside this method, use `puts` to ask the user to write a sentence.
- Capture the user's input with `gets.chomp` and save that input to a variable. 
- Find a string method that will divide that sentence into an array and save the resulting array as a new variable.
- User the `.each_with_index` method to iterate through the array.
- Inside this loop, use conditional logic and the modulus operator to puts each word, alternating between lower- and upper- case letters.
- Make sure to end any open blocks and close the method.
- Below your newly defined method, call `uncle_speak`.
- Go back to the terminal and run the file you just created with `ruby uncle_speak.rb`

The result should look something like this in your terminal:

```
Type a sentence:
Learning code is hard but it's also kind of fun!
LEARNING
code
IS
hard
BUT
it's
ALSO
kind
OF
fun!
```

## Sorting Hat
The Sorting Hat drank too much butterbeer last night and can't remember what house anyone's supposed to be in. Luckily, you have a backup copy in the form of an array of objects below. 

```
wizards = [
  {name: "Harry Potter", house: "Gryffindor"}, 
  {name: "Lord Voldomort", house: "Slytherin"}, 
  {name: "Cedric Diggory", house: "Hufflepuff"},
  {name: "Luna Lovegood", house: "Ravenclaw"},  
  {name: "Albus Dumbledor", house: "Gryffindor"}, 
  {name: "Merlin", house: "Slytherin"}, 
  {name: "Pomona Sprout", house: "HufflePuff"}, 
  {name: "Gilderoy Lockheart", house: "Ravenclaw"}, 
  {name: "Ron Weasley", house: "Gryffindor"}, 
  {name: "Severus Snape", house: "Slytherin"}, 
  {name: "Nymphadora Tonks", house: "Hufflepuff"}, 
  {name: "Padma Patil", house: "Ravenclaw"}, 
  {name: "Hermoine Granger", house: "Gryffindor"} 
 ]
```

Write a program that iterates through this array of objects and `puts` the names of wizards and witches with their houses. The Sorting Hat is having a pretty rough morning, so make it easy on him and print out the names one house at a time.
- In your `ruby_practice` folder, `touch` a file called `sorting_hat.rb`
- Define a method called `sorting_hat`. It should take 1 parameter.
- In your method, use `.each do |wizard|` loops to sort the wizards and witches by their houses.
- Make sure to end any open blocks and close the method.
- Below your newly defined method, call `sorting_hat` with the `wizards` array as its argument.
- Go back to the terminal and run the file you just created with `ruby sorting_hat.rb`

The end result should look something like this in your terminal:

```
Gryffindor:
Harry Potter
Albus Dumbledor
Ron Weasley
Hermoine Granger

Slytherin:
Lord Voldomort
Merlin
Severus Snape

(etc)
```

## D&D Dice Roll
You're playing Dungeons and Dragons, but you accidentally dropped your 20 sided dice underneath the couch before the final battle, and there's a tangled, sticky mess of Cheeto dust, maple syrup, and cat hair down there, so there's no way you're picking that thing up.  No worries, you can just go with the next best solution: writing a program in Ruby that can figure out your attack rolls for you!

- In your `ruby_practice` folder, `touch` a file called `dungeons.rb`
- Define a method called `fight`. It doesn't need to take any parameters.
- Use `puts` to ask the user the name of the monster they're fighting.
- Use `gets.chomp` to allow the user to input that monster's name and save it to a variable called `monster`.
- Do the same with the hero's name and save it to a variable called `hero`.
- Create variables for `monster_health` and `hero_health`. Set them both to `50`.
- Using a while loop, have the hero and monster attack each other until one of them has a health at or below 0. 
- Using `rand` and a range, generate a random number between 1 and 20  to decide if an attacker hits and for how much damage, using the following criteria:
  - If an attacker rolls a 1 or 2, they accidentally stab themselves for 5 damage.
  - If an attacker rolls between 3 and 10, they miss and do 0 damage. 
  - If an attacker rolls between 11 and 18, they hit and do 10 damage.
  - If an attacker rolls a 19 or 20, they get a critical hit and do 20 damage.
- Use `puts` with string interpolation after each attack to inform the user what happened and how much of each fighter's health remains.
- Continue the battle until one of the fighter's health has been reduced to zero. When this happens, use string interpolation to declare the winner and loser by name.
- Make sure to end any open blocks and close the method.
- Below your newly defined method, call `fight`.
- Go back to the terminal and run the file you just created with `ruby dungeons.rb`

The end result should look something like this in your terminal:
```
Name your hero:
David Magicbeard

Name the monster:
Hungover Bri-Guy

Hit! David Magicbeard strikes Hungover Bri-Guy!
Critical failure! Hungover Bri-Guy accidentally stabs self!
David Magicbeard has 50 hitpoints left. Hungover Bri-Guy has 35 hitpoints left.

David Magicbeard misses!
Hit! Hungover Bri-Guy strikes David Magicbeard!
David Magicbeard has 40 hitpoints left. Hungover Bri-Guy has 35 hitpoints left.

Hit! David Magicbeard strikes Hungover Bri-Guy!
Hit! Hungover Bri-Guy strikes David Magicbeard!
David Magicbeard has 30 hitpoints left. Hungover Bri-Guy has 25 hitpoints left.

Critical hit! David Magicbeard does double damage!
Hit! Hungover Bri-Guy strikes David Magicbeard!
David Magicbeard has 20 hitpoints left. Hungover Bri-Guy has 5 hitpoints left.

Hit! David Magicbeard strikes Hungover Bri-Guy!
Hit! Hungover Bri-Guy strikes David Magicbeard!
David Magicbeard has 10 hitpoints left. Hungover Bri-Guy has -5 hitpoints left.

Hungover Bri-Guy has lost to David Magicbeard. The world is safe!... for now.
```

## Finished Early?
Wow! Congrats for surviving the gauntlet! We're genuinely impressed! Let's pass your skills forward:

Create a new challenge and use Slack to send it to your instructor. We'll review it, and if it fits within the scope of our class's current Ruby knowledge, we'll add it to this list!
