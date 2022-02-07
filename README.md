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

<!-- Added by: shermanm, at: Tue Feb  1 16:58:13 EST 2022 -->

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
