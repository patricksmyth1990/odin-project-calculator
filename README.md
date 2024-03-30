====Description====

from here: https://www.theodinproject.com/lessons/foundations-calculator
An on-screen calculator using Javascript, HTML, and CSS.

----Use-cases----

"Your calculator is going to contain functions for all of the basic math operators you typically find on calculators, so start by creating functions for the following items and testing them in your browser’s console.
add
subtract
multiply
divide

A calculator operation will consist of a number, an operator, and another number. For example, 3 + 5. Create three variables for each of the parts of a calculator operation. Create a variable for the first number, the operator, and the second number. You’ll use these variables to update your display later.

Create a new function operate that takes an operator and 2 numbers and then calls one of the above functions on the numbers.

Create a basic HTML calculator with buttons for each digit, each of the above functions and an “Equals” key.
Do not worry about wiring up the JS just yet.
There should also be a display for the calculator. Go ahead and fill it with some dummy numbers so it looks correct.
Add a “clear” button.

Create the functions that populate the display when you click the number buttons. You should be storing the ‘display value’ in a variable somewhere for use in the next step.

Make the calculator work! You’ll need to store the first number and second number that are input into the calculator, utilize the operator that the user selects, and then operate() on the two numbers when the user presses the “=” key.
You should already have the code that can populate the display, so once operate() has been called, update the display with the ‘solution’ to the operation.
This is the hardest part of the project. You need to figure out how to store all the values and call the operate function with them. Don’t feel bad if it takes you a while to figure out the logic.

Gotchas: watch out for and fix these bugs if they show up in your code:
Users should be able to string together several operations and get the right answer, with each pair of numbers being evaluated at a time. For example, 12 + 7 - 5 * 3 = should yield 42. An example of the behavior we’re looking for would be this student solution.
Your calculator should not evaluate more than a single pair of numbers at a time. Example: you press a number button (12), followed by an operator button (+), a second number button (7), and finally a second operator button (-). Your calculator should then do the following: first, evaluate the first pair of numbers (12 + 7), second, display the result of that calculation (19), and finally, use that result (19) as the first number in your new calculation, along with the next operator (-).
You should round answers with long decimals so that they don’t overflow the screen.
Pressing = before entering all of the numbers or an operator could cause problems!
Pressing “clear” should wipe out any existing data.. make sure the user is really starting fresh after pressing “clear”
Display a snarky error message if the user tries to divide by 0… and don’t let it crash your calculator!"

----Extra credit----

"Users can get floating point numbers if they do the math required to get one, but they can’t type them in yet. Add a . button and let users input decimals! Make sure you don’t let them type more than one though: 12.3.56.5. It is hard to do math on these numbers. (disable the decimal button if there’s already one in the display)
Make it look nice! This is a great project to practice your CSS skills. At least make the operations a different color from the keypad buttons.
Add a “backspace” button, so the user can undo if they click the wrong number.
Add keyboard support!"

====Planning====

What does this project require?
- no more than a basic UI (I can make it look nicer later)
- needs to be able to add, subtract, multiply, and divide
- buttons for each digit, each of the above functions, and an equals key
- a 'clear' button
- a logic for storing the first number, the second number, then operating on the two stored numbers
- User-inputted data
	- numbers, operators, equals, clear -- all using buttons
	- equals should only work if a valid operation is input first
	- clear should remove all user-inputted data
	- decimal numbers need to be rounded to a certain number of digits 
	to prevent overflow
- Desired output: evaluated mathematical expressions (without using eval(), which is apparently dangerous) -- neither should I use "new Function()" to evaluate expressions

----Pseudocode----

When the user inputs a number, an operator, and a number
All three will be stored in separate variables
Which will be fed into an operate() function that calls one of the four operations (add, subtract, multiply, divide) on the numbers when the user presses the "=" button
The result will be displayed, rounded if necessary
This will require functions that populate the display with a 'display value' as the user presses numbers and operators (DOM manipulation), and then update the display value once operate() is successfully invoked

----Things to keep in mind----
- it needs to be able to string together several operations like "12 + 7 - 5 * 3 ="
- it SHOULD NOT evaluate more than a single pair of numbers at a time
- long decimals should be rounded, so they don't overflow
- pressing = may cause problems if the user didn't press an operator
- "clear" should wipe out all user-inputted data
- display an error if the user tries to divide by 0, and don't let it crash the site!