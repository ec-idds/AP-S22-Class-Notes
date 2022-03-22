# Class Notes: Programming Directed Study Spring 2022

These are the notes from a directed study course in "Advanced Programming," written and maintained by:

* Mark Sherman <shermanm@emmanuel.edu>
* McKenzie Leahy <leahym@emmanuel.edu>

**Table of Contents**
<!--ts-->
   * [Class Notes: Programming Directed Study Spring 2022](#class-notes-programming-directed-study-spring-2022)
   * [Instructions](#instructions)
   * [Session 1 - January 20](#session-1---january-20)
   * [Session 2 - January 25](#session-2---january-25)
      * [Chapter 1 - Values](#chapter-1---values)
      * [Chapter 2 - Program Structure](#chapter-2---program-structure)
   * [Session 3 - January 27](#session-3---january-27)
      * [Chapter 3 - Functions](#chapter-3---functions)
   * [Session 4 - February 1](#session-4---february-1)
      * [Chapter 3 Cont.](#chapter-3-cont)

<!-- Added by: shermanm, at: Tue Feb  8 16:47:57 EST 2022 -->

<!--te-->
# Instructions
This is also a lesson in git workflow while working with a team. 

Getting Started: 

1. [Fork this repository](https://docs.github.com/en/get-started/quickstart/fork-a-repo) on github. The fork button is ↗️ on the [github page.](https://github.com/ec-idds/AP-S22-Class-Notes)
2. You could do your edits right in the github web interface, and that's probably easier. So let's focus on that for now. <!--You can also "clone" it to your computer and work on it in a text editor. So this step is, optionally, [Clone](https://docs.github.com/en/get-started/quickstart/fork-a-repo#cloning-your-forked-repository) your fork your computer. -->

Workflow:

1. Make sure your working copy has the latest updates from my "upstream" original repo. This is done with **Fetch upstream** button on the GitHub website. 
2. Edit the README.md file to add/fix notes. (This file!) You can also add image files and link them in to the README, like screenshots. 
	* The formatting "language" of the file is Markdown. Here's how to use it: <https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet>
	* While looking at the README file on the website, click the **Edit** button. It also has a preview feature!
3. Commit your changes. This adds them to git. 
	* [Working in Github website](https://docs.github.com/en/get-started/quickstart/hello-world#making-and-committing-changes)
4. Make a [pull request](https://docs.github.com/en/get-started/quickstart/hello-world#opening-a-pull-request) to submit your work back to me to merge into the "main" copy. 

Don't worry about the Table of Contents- I'll update that when I merge your changes! Also don't merge it yourself, let me do that. 


# Session 1 - January 20
* Programming Paradigms 
* Paradigm- categories/ classes of language features that define how a language is organizes and what it can do 
* In intro to programming you were taught one paradigm of 'imperative programming' which includes global state variables, and explicit sequence of commands that update state. 
* Paradigms often overlap ex. all languages have the ability to make variables 
* JavaScript is a 'multiparadigm' language, so any paradigm style is appropriate 
* Well known paradigms 
* Functional (applicative) programming 
	* Functions are a 'first class' data type 
	* When determining if the code is functional, ask yourself can a function be assigned to a variable? If yes, then it is functional code. 
	* Languages that are functional: JavaScript, Python (limited), Scheme, Lisp, Haskell 
	* Languages that are NOT functional: C, C++, Java
* Object Oriented (OO)
	* Organizes code into objects, uses instances 
	* Instance- is what actually runs, contains real data and can run functions 
	* Can make many different instances, and each separate instance will have the same structure, but are unique and can have different data.
	* Classes can have a structure of its parent class, but is a new class, and can inherit other things  
	* Maintains a strict organization, slower to write 
* Functional programming is faster to make a product 
* Object Oriented is harder to break, used for bigger problems 
* Organized Languages 
	* Compiled and dynamic: pretty much doesn't exist, compiled programs are pre-optimized and cannot change dynamically 
	* Interpretted and dynamic: JavaScript, Ada, Small Talk, Lisp, Scheme, Scratch 
	* Compiled and static: 'bread and butter' C, C++, Rust, OO
	* Interpretted and static: 'possibly rare' if you are already using an interpreter might as well go dynamic for more power
* Speed of different languages 
	* FAST (hard to write): Assembly, C, C++ 
	* AVERAGE: Java, Python
	* SLOW (easy to write): JavaScript (code running other code)
* Golden Rule
	* As programmers we want to write our code in the easiest language possible, until we need to make it faster.  

# Session 2 - January 25

Going over chapters 1 and 2, and took a bit of a side quest into the history of computing development. 
These notes are the highlights, focusing on what is new information beyond what we learned in Intro Programming.

## Chapter 1 - Values

* Numbers
	* Always 64-bit in JavaScript. Either *integer* or *floating point* format. 
	* Integer math is always precise. Floating point is always an approximation. 
* Strings
	* Both single and double quotes can delineate strings. This is useful if you want the quote character IN your string without ending it prematurely.
	* New thing: template strings!
		* Use backticks (lowercase ~)
		* allows expressions to be evaluated, and their return value be inserted into the string
		* `${}` inserts an expression to evaluate
* Special Values
	* Nothing: `null` and `undefined` (they mean the same, no value, but come from different mechanisms)
	* Not a Number, `NaN` - technically a number type, but usually returned to indicate an error
	* `Infinity` and `-Infinity`
* `typeof x` is a unary operator that returns what type the value of x is. 

## Chapter 2 - Program Structure

* Some History of Programming
	* Grace Hopper
		* Videos on Grace Hopper 
		* https://www.youtube.com/watch?v=QA33wW5LaNY4
		* https://www.youtube.com/watch?v=1LR6NPpFxw4
		* https://www.youtube.com/watch?v=Fg82iV-L8ZY
	* Ada Lovelace
		* Charles Babbage
	* Grace Hopper's literal "bug"
	* Alan Turing
* structure 
	* bindings - giving a name to a value 
	* let, var, const (binding operators) 
	* sub expressions -> decided value -> bound 
	* binds variable to result of the expression 
* garbage collector will come and clean up things (data) that are no longer being used
	* imperative to functional programming 
	* garbage collector makes things dynamic, so you do not need to be deleting things yourself 
* environment 
	* collection of bindings 
	* all functions that can be run
	* all different values that can be bound to that data
	* defines how we organize the code 
* functions 
	* defined with function as a keyword, it can be called, and applied/ invoked (defined and applied) 
	* console.long = print()
* every expression returns a value
* if nothing is returned, it returns undefined 
* side effect- anything a function does that is not reflected in the output 
* control flow
	* 1. rules are intuitive 
	* 2. largely universal 
	* "if" is a big control tool 
	* keyword "break" breaks you out of a "for" loop 
* Starship Troopers by Robert A Hynlind 
# Session 3 - January 27

We went over some of chapter 3 and worked on environment diagrams

## Chapter 3 - Functions 

* Functions 
	* expressions you can apply to a set of inputs 
	* maps the input to the correct output
	* `const` and `let` are used to bind to the block they are declared in 
	* a function doesn't always apply a name or binding to something, it can or does not need to
		* this returns the return value by skipping the name
	* functions are a value type 
	* when the function is the first word used on a new line it gets hoisted to the top of the list and it becomes a global function
	* the `=` allows for you to have all the control of where the function is, if you don't use the `=` then it gets moved to the top 

* Environment diagrams or memory diagrams 
	* when you make a binding it re-assigna the value as the old one gets deleted  
	* everything without an arrow back to the global will get deleted 

# Session 4 - February 1 
## Chapter 3 Cont. 
* Arrow function 
	* "=>" fat arrow, operator, syntax choice 
	* Used to point at the body of that function, applies body to the arguments of a function 
	* Allows for one off functions very quickly 
	* Can get rid of "return" in the body if there is only one body parameter 
* Call Stack 
	* When you call a function, it goes somewhere else to execute the function, and then it comes back to "return" a value of the function 
	* "Return" returning from previous contex 
	* Call stack is a piece of data in memory that keeps track of all the ins-and-outs 
	* Goal is to keep empyting 
	* Functions compile on top of each other until they are returned, and then the program will revert back to the beginning 
	* Control of the function can only be in one place at a time 
	* Some languages do not have callback, they go to the function and can never leave 
	* Callstack = breadcrumbs 
	* There is only one call stack 
	* The call stack will do one thing at a time, but marks where in the code it was as the code jumps around to execute the code, it keeps order 
* Call Stack Tiny People Analogy 
	* In a function, a tiny person comes out and takes the arguments of the function and places the arguments in their pockets 
	* The tiny person then goes and uses the arguments to exchange for the value of the function 
	* The same tiny person then hands the value from the functions back to the original tiny person that gave them the arguments 
	* This act of returning the value is important so then the other code can resume
* Recursion 
* https://www.youtube.com/watch?v=YZcO_jRhvxs
	* recursion is another way to do repetition 
	* looping is one way to do repetition 
	* thus recursion is another way to do looping 
	* the recursion part of a function is often hidden within another function 
	* In a recursion function, you can add in another function to create a hardwired start property/ value 
	* Groundhog Day metaphor
	* You change the arguments to have the most updated information for next time it runs 
	* the callstack tracks state 
* Functional Programming 
	* first type of programming designed in the 60s
	*  It evolved a lot sooner, was mathematically pure 
	*  then computers evolved the first time, and FP became obsolete 
	*  Once computers evolved again and became astronomically better, FP came back intro fruition 
* Two main properties/ pillars of FP 
	* 1.) Can stop somewhere in the code and resume it later 
	* 2.) Stay away from state variables, as FP is looking to reduce the mess they cause 
* Making change example for recursion 
	* If you start out with different coins, to make one dollar, the combination of change will vary 
	* This represents recursion, as different decisions are being made, and all of them play out to solution 
* Recursion is seen in GPS systems and classical AI trainings 


# Session 5 - February 3

# Session 6 - February 8
## Chapter 4 - Mutability 
* every value is mutable 
* mutable = changeable, maluable, moveable 
* relies on the concept of change through making an entire new one (new binding) and throwing away the other one 
* Two things can happen to the "old" item 
	* 1.) something else points at it or not 
	* 2.) if not pointed at, the garbage collector will take it away 
* In javaScript you never explicitely delete anything 
* computers are not inherently mutable 
* mutable data is messy and unpredictable 
* immutable data is what it is, and if you need a new one, you make it 
* over time no piece of data will ever change, because it cannot change 
* you can change bindings, but the actual data never changes 
* objects actually do change, because they have a lot of things within them 
* functions- pay attention to code terms 
* objects - pay attention to data terms 
* Closure: you create a function with data already in it (makeMultiplier example) 
	* closure ensures that you do not fall into changing numbers that you did not mean to change 
* Parallelism 
	* needed so FP can come back 
	* when you have parallelism, JS is always in one place, only doing one thing at a time 
	* ex. "Google Search" works across mutliple computers 
* Why FP works well with parallel systems 
	* 1.) immutable data: it tracks your changes across machines 
	* 2.) no global state, each machine is its own "global" state, and the variables do not maintain the same in each "global" system 
* state variables are very messy 
* communication between nodes is the hardest part 
* parallelization is useful in hardware failure and if you need to reboot/ update a node 
* node: a server/ computer 

Closures demonstration code:
```JavaScript
function setup() {
  createCanvas(400, 400);
  
  
  let makeMultiplier = function (n) {
    return function (b) {
      return b * n;
    }
  }
  
  let tripler = makeMultiplier(3);
  
  print(tripler(2));
  print(tripler(5));
  
  let quad = makeMultiplier(4);
  
  print(quad(2));
}
```

# Session 7 - February 10 
* Arrays: reduce, map, filter 
* reduce (higher order procedure): to accumulate all of the items in an array together
	* syntax: array name . reduce((total, num), start value)
* higher order function 
	* function that has to operate on other functions 
	* requires a function to be passed into it 
	* functions that talk to other functions 
	* functions are first class in JS, but not in all languages 
* MAP: makes a new array after applying opertions to the original array's values to form a new array 
	* puts the value in the original array at any time, and returns that value in its new array 
	* syntax: original array name. map((x) => whatever you want to do to the value) 
* Filter: akin to map, as it makes a new array but only includes some elements 
	* needs to test to decide whether to keep or ignore, makes things into a boolean 
	* syntax: array name . filter((x) => parameters of what variables you want included) 
* When reduce, map, and filter are used altogether, they help multiple things happen at once 
# Session 8 - February 15
* practiced reduce, map, and filter on codio 
# Session 9 - February 17 
* Objects 
	* overloaded words- multi definition, similar in vibe, mechanically different 
	* multiparadigm = multiple definitions 
	* entirely abstract, anything can be object a thing 
* Object oriented programming - way to divide program into objects, ways to organize programs as you develop them 
	* program is now a collect of objects that can talk to each other 
	* an individual object is responsible for its own code and its own parameters 
	* state variables should only be acquired to their objects 
	* objects have an internal state and internal code 
	* you can only access the states of code through reaching through accessories 
	* can create modules that work as interfaces 
	* responsible for managing its own state 
	* objects like reusable pieces 
	* the program can be local to the object and when outside that object you don't care how it works within the object 
* method, procedure, and function 
	* method: gets its content from the object it belongs to 
	* function in JS: technically a procedure - gets context from environment 
* Public vs. Private
	* 1. public- interfaces you can see outside of the object (what is on the menu)
	* 2. private- not accessible from outside, internal use only (what is behind the bar) 
* accessors: functions used to access private parts of the object 
	* JS cannot distinguish between the two 
	* used as a convention (ex. camelCase), as something used for humans to communicate, is an addition away from what the code does vs. actually means 
	* convention in JS/python= if something is an object you can name it with an underscore __ to make symbolize it is private 
	* if you accidently access it publicly, it will mess with the state, and the state will go inconsistent (BAD) 
	* in order to not have the state go inconsistent, you must USE ACCESSOR functions 
* objects oriented protects your state 
	* less severe, because you still feel consequences of direct mutation 
	* not actually changing, object changes it to maintain state, protects data from being 1/2 way processed when called 
* enforcing private vs private is based on honor system 
* methods: projects that hold function values 
* objects syntax: properties
	* object  
	* propertyName: propertyValue, 
	* propertyTwo: value2, 
* objects have their own little frame, and bindings to values 
* if you assign soemthing that doesn't exist, JS will make it exist in the object, making it easy to grow an object through many stages 
* ${line} only works with `` back tics, making it easy to change what a string says in the code 
* "this." refers to the object you are IN, how you get to properties of the object you are in 
	* when you are in an object, you do not necessarily know what it is named 
	* objects like functions don't necessarily have names 
	* it also does not know its name as it can change 
	* using this. is safer, as there is less searching in the environment, as the computer will never look for a new "this" 
	* => will use the bindings of wherever you already are 
	* every function in JS has a ".call", if you want to call that function with a different this. or in a different environment 
	* => adds this. to the frame its already in, how it is mechanically different from function 
* NOTES FOR FUTURE CLASS: skip speak.call* - just confusing, skip prototypes 
# Session 10 - March 1
* Object Oriented Classes and Inheritance 
	* objects: a way to modularize code/ programs/ state 
	* changes data as the program runs 
	* objects are stateful, hold data, that data can change is is mutable 
	* still not mutable globals 
	* code in the form of "methods"
	* obj.method() = method is a function that lives within that object 
	* class: template of a specific kind of object 
	* Instantiate: to make an instance of, an individual copy of a thing, using the blueprint for that object 
* Object syntax blueprint 
	* object classes are capitalized 
	* class of a car: 
		* var name 
		* var year 
		* var make 
		* Method: startCar 
		* Method: stopCar 
	* All objects within this class will have the above listed properties 
* Instantiation: creates space in active memory for all stuff described in the class
* A class is not an object, it is a template to create objects 
* to define a class you need to have a function called "constructor ()" 
* Constructor()
	* is where you give it the data to put into its stuff 
	* keyword "new" = instantiates a class into an object 
	* class constructors MUST be invoked within "new" 
	* with the class defined, making new ones is easy 
	* more organized and controlled way to make objects 
* Can get at things within an object using .dot operator 
* only thing you can put in the classes are methods 
* EX. 
	* let car = variable 
	* class Car = class 
	* let myCar = new Car('fiat', 2018) 
	* new constructs a new object that the function is owed to
	* "myCar" is in the global frame 
	* "fiat", "2018", and "Date" are placed within the object frame
	* "name: fiat", "year: 2018", "this.name: name" are made in the constructor frame, which will be disposed of by the garbage collector 
	* newDate() = instance when new operator is called 
	* adding stuff to this argument that was not initially an argument  
# Session 11 - March 15
* Abstraction 
	* Allow you to organize things, let you build things off of them 
	* encapsulation: objects, code/data = one unit 
	* encapsulation allows for "encryption" within an object 
	* programming language then evolved from pure extraction to including checks and balances 
	* the rules of programming are arbitrary, the rules will work if you stick to them
	* coding rules are arbitrary but when you follow them it maintains order and functionality 
* Objects 
	* Inheritance: when you have a class, and you want to change it to be more specific to a purpose and create a subclass 
	* A subclass has everything the parent class has (functions, methods, data templates) 
	* classes are used to derive other classes 
	* with subclasses you can change things in them without changing things within the parent class 
	* this concept ^ allows you to create NEW objects with all the features of the parent classes and previous subclasses 
	* classes are used a lot in GUIs 
	* classes allow you to not have to reinvent the wheel each time, different purpose similar structure 
	* classes allow you to maintain compatible features (ex. draw) 
	* can go the opposite way too and provide a more generic template to build off of 
* Jitterbug 
	* change the layout from using object orientation to classes 
	* use the "New" keyword to instantiate a new bug 
	* keyword "Extends" makes a new subclass 
* Example 
	* driver bug implements jitterbug 
	* everything new you define, and everything the parent class had 
	* 1. no reiventing the wheel
	* 2. build systems and frameworks of code 
	* need things to be able to interact with other stuff 
	* provide objects that you can sub class to organize 
	* Java- forces OO, "embarrasingly" enforces it 

# TERMS

* Paradigm: classes of language concepts and features that usually revolve around a central philosophy, an organizational tool to understand a collection of features 
* Functional Programming: (applicative) functions are "first-class" data type, passed as arguments and returned 
* Object-Oriented Programming: all code is organized into objects 
* Bits: any kind of two-value things, usually described as 1s and 0s 
* Values: chunks of bits ex. numbers, text, functions
* Overflow: end up with a number that did not fit into the given number of bits 
* Operators: +, *, -, /, %, >, <, >=, <=, ==, !=, &&, ||, ! 
* Unicode standard: assigns a number to virtually every character you would ever need 
* Boolean: which has just two values, true and false 
* Null and Undefined: denote the absence of meaningful value 
* Expression: fragment of code that produces a value 
* JS statement: full statement, compilation of expressions 
* Program: list of statments 
* Side effects: values of expressions that do not change the world 
* Variable: catches and holds values 
* Binding: creation of a variable to its value, = can be used to assign new values to a binding 
* Environment: collection of bindings and their values that exist at a given time 
* Function: piece of program wrapped in a value, have a set of parameters and a body, which maintains the statements to execute 
* Arguments: values given to functions 
