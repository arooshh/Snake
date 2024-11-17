This code implements a **Snake Game** in C. Below is the explanation of its functionalities and structure:

#### **1\. Header Files and Macros**

* Includes `stdio.h` for input/output operations.  
* Includes `stdlib.h` for functions like `rand()`.  
* Includes `time.h` for random number seeding.  
* Includes `conio.h` for keyboard input handling.  
* Includes `windows.h` for the `Sleep()` function.  
* Defines constants `WIDTH` and `HEIGHT` for the game area dimensions.

#### **2\. Global Variables**

* `gameOver`: Flag indicating the game state.  
* `x, y`: Snake's head position.  
* `fruitX, fruitY`: Fruit position.  
* `score`: Player's score.  
* `tailX[], tailY[]`: Arrays storing the snake's tail positions.  
* `nTail`: Length of the snake's tail.  
* `dir`: Direction of snake movement.

#### **3\. Enumerations**

* `enum eDirection`: Defines possible movement directions (`STOP`, `LEFT`, `RIGHT`, `UP`, `DOWN`).

#### **4\. Functions**

* **`Setup()`**: Initializes game variables, sets random fruit position, and resets the score and tail length.  
* **`Draw()`**:  
  * Clears the console.  
  * Draws the game board boundaries, snake (`O` for head, `o` for tail), and fruit (`F`).  
  * Displays the player's score.  
* **`Input()`**:  
  * Captures user input for snake movement (`w`, `a`, `s`, `d`) or exits the game (`o`).  
* **`Logic()`**:  
  * Updates the snake's tail position.  
  * Moves the snake based on the current direction.  
  * Handles screen wrapping for the snake's position.  
  * Checks for collisions with the snake's tail (ends the game) or fruit (increases score and tail length).

#### **5\. Main Function**

* Calls `Setup()` to initialize the game.  
* Runs a game loop that:  
  * Draws the game board.  
  * Processes user input.  
  * Updates game logic.  
  * Delays execution for smoother gameplay.

## **Prerequisites**

## \- A C compiler (e.g., GCC).

## \- Windows operating system (for compatibility with \`conio.h\` and \`windows.h\`).

## **How to Compile and Run**

## 1\. Save the code to a file named \`snake\_game.c\`.

## 2\. Open a terminal or command prompt and navigate to the file's location.

## 3\. Compile the program using:

##    gcc snake\_game.c \-o snake\_game

## **Controls**

| Key | Action |
| ----- | ----- |
| `W` | Move Up |
| `A` | Move Left |
| `S` | Move Down |
| `D` | Move Right |
| `O` | Exit Game |

## **Game Rules**

1. The snake starts at the center of the board.  
2. The goal is to collect as many fruits as possible to increase your score.  
3. The game ends if the snake collides with its own tail.

