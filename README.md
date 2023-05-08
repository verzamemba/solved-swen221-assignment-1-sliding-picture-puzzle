Download Link: https://assignmentchef.com/product/solved-swen221-assignment-1-sliding-picture-puzzle
<br>
In this assignment you will work with a simple program which implements a “Sliding Picture Puzzle”. This is a well-known style of game where an image is divided up into squares which are scrambled and need to be manipulated into the correct order:

https://en.wikipedia.org/wiki/Sliding_puzzle

The program in this assignment has a relatively simple class hierarchy. Nevertheless, understanding the flow of control through the program will still be challenging at times and will test your debugging skills.

<h1>Picture Puzzle</h1>

The picture puzzle game provides a simple GUI where you can load an image, choose the difficulty of the game (e.g. 3×3 vs 4×4) and then play the game. The puzzle is shown in the left panel, with the solution shown on the right:

The game is relatively straightforward to play, though there are some variations. In particular, we can <em>rotate </em>squares by right-clicking on them. This makes the game slightly harder to play, and also makes the program code more interesting (though also more complex).

<h1>Getting started</h1>

To get started, download the picturepuzzle.jar file from the lecture schedule on the course website. As usual, you can run the program from the command-line as follows:

java -jar picturepuzzle.jar

A simple GUI should appear on your screen, and you should be able to play the game. <em>Remember, however, that at this stage the game contains a number of bugs and missing features. </em>For example, pieces may not move in the direction you are expecting!

When you import the picturepuzzle.jar file, you should find the following Java packages:

<ul>

 <li>The swen221/picturepuzzle/gui/ package contains the graphical user interface and the main method. <strong>You do not need to understand the inner workings of this in order to complete the assignment. NOTE: </strong>you do not need to modify any code in this package.</li>

 <li>The swen221/picturepuzzle/model/ package contains the class Game encoding the logic of a game, and the class Board representing the current state of the board.</li>

 <li>The swen221/picturepuzzle/moves/ package contains a class for the two different kinds of move that can be made in the game (move and rotation). These contain code related to structuring a move, and ensuring it is valid.</li>

 <li>The swen221/picturepuzzle/tests/ packages contains many jUnit tests to check your implementation of the game. <strong>NOTE: </strong>To make the automatic marking possible, you can not modify the files already present in this folder, but you may add your tests in a separate file (e.g.</li>

</ul>

MyTests.java).

<h1>Part 1 — Small Boards</h1>

The first objective is to make sure the game correctly implements simple <em>moves </em>on small (i.e. 2 × 2) boards (for now, ignoring rotations). There is a simple <em>defect </em>in the Location class which you must identify and fix. Tests for this part is provided in swen221/picturepuzzle/tests/Part1Tests.java.

<h1>Part 2 — Big Boards</h1>

The second objective is to make sure the game correctly implements simple <em>moves </em>on larger (e.g. 3×3) boards (for now, still ignoring rotations). There are several defects spread across the Board and Move classes which you must identify and fix. Tests are provided in swen221/picturepuzzle/tests/Part2Tests.java.

<h1>Part 3 — Rotation Moves</h1>

The third objective is to implement the <em>rotation </em>move in the game. This is a tricky little algorithm to get right, though the test cases should help. You will need to implement the method Rotation.apply().

Tests for this part are provided in swen221/picturepuzzle/tests/Part3Tests.java.

<h1>Part 4 — Game Over</h1>

The final objective is to implement the test to determine when the game is over. This requires changes to the Board class. Tests are provided in swen221/picturepuzzle/tests/Part4Tests.java.