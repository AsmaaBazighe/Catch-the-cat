
# Catch The Cat

Catch the Cat is a simple yet engaging game where you must trap a cat within a board by strategically clicking on the panel to create barriers. This README file provides an overview of the game, gameplay instructions, and some code explanation :




## Overview :
The objective of Catch The Cat is to trap the cat within the board and prevent it from escaping. If the cat escapes, you lose the game. The game continues until you successfully trap the cat.

## Gameplay instructions:
1. **Create Barriers**: Use your mouse to click on the circles and create barriers to prevent the cat from escaping.
2. **Strategize**: Start by creating barriers farther away from the cat to increase your chances of trapping it.
3. **Observe**: Pay attention to the changing colors of the spots to gauge your proximity to trapping the cat.
4. **Trap the Cat**: Cover the last spots in the direction the cat is moving to trap it inside the board.



## Code explanation:
The provided code implements the game Catch The Cat using the Tkinter library for creating a graphical user interface. Below is an explanation of the main components and functionalities of the code:

#### Drawing the Game Board

Defines a function to draw the game board using Tkinter's Canvas widget. Green represents the border, and white represents the inner boxes. The function also initializes lists to store the coordinates of white and green boxes.

```bash
  def dessiner_plateau():
    # Drawing the board with green border and white inner boxes
    ...
```

#### Handling Mouse Clicks

Defines a function to handle mouse clicks. When a box is clicked, it checks if it's within the valid range of the board, not already checked, and white. If so, it adds the box's coordinates to the list of checked boxes and changes its color to red. It then calls the ***deplacer_cercle_minimax*** function to move the cat.

```bash
  def cocher_case(event):
    ...
```

#### Minimax Algorithm

Implements the minimax algorithm to determine the best move for the cat. It evaluates possible future states of the game and selects the move that maximizes the cat's chances of escaping or minimizes the player's chances of trapping it.

```bash
  def minimax(etat, profondeur, alpha, beta, maximizing):
    ...
```

#### Moving the Cat

Moves the cat according to the minimax algorithm's decision. It calculates the best move using minimax, updates the cat's position, and redraws it on the canvas. If the cat reaches a green box, it announces the cat's victory.

```bash
  def deplacer_cercle_minimax():
    ...
```

#### Creating the GUI

Creates a Tkinter window, sets up a canvas for drawing, draws the game board, binds mouse clicks to the ***cocher_case*** function, and starts the main event loop to handle user interactions.

```bash
  # Creating a Tkinter window and canvas
fenetre = tk.Tk()
canvas = tk.Canvas(fenetre, width=750, height=550)
canvas.pack()

# Drawing the game board
dessiner_plateau()

# Binding mouse clicks to the cocher_case function
canvas.bind("<Button-1>", cocher_case)

# Starting the main event loop
fenetre.mainloop()

```

## Author:
This project was carried out by [Asmaa Bazighe](https://github.com/AsmaaBazighe).

## Licence:
This project is licensed under [MIT License].
