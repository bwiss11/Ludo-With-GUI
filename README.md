# Ludo with GUI

## Introduction
This application is a fully interactive four-player Ludo game with a graphical user interface. Each player will have four tokens.

This game was developed using Python, with Tkinter used for the GUI. It utilizes the 'random' and 'PIL' libraries.


## The Board
The Ludo board is shown below. We'll go into more details on gameplay later but first, the board. There are home areas (large colored circles) for each of the four players. Each player's home area starts out holding all four of their tokens (small colored circles). The player's tokens begin by moving out of their home area and onto the space containing their corresponding color and white arrow. The tokens navigate the board clockwise until they reach their home row (string of spaces matching their color in the middle of the board). A token's path is completed by reaching their victory space (triangular shape corresponding to their color in the middle of the board).
<p align="center">
<img width="733" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/be9c9d41-6228-4e1d-83cb-85b6e80917f5">
</p>

## Goal
The goal of the game is for a player to get all four of their tokens into the victory area (middle of the board) before the three other players. 


## Example Gameplay
Below is some example gameplay that will help explain the rules of the game.

We start with a clean board, with all four of each player's tokens in their home area. We click the "Roll the Dice!" button at the bottom of the screen and the game begins. The home area of the player currently taking their turn is highlighted and the dice roll is shown at the top of the screen. Rolling continues until someone rolls a 6 (the number needed to move out of the home area). Typically, a player gets one roll per turn. The exception is if a 6 is rolled, in which case the player may roll again. If another 6 is rolled, the player may roll again. After the third roll, no matter the value of the roll, the turn passes to the next player.

### Moving Out of Home
Here, the yellow player has rolled a 6 and now has an opportunity to move one token out of their home area, which can be done by clicking on the highlighted square [slide 1].
Clicking moves one of the yellow player's tokens out onto the board [slide 2]. Since a 6 was rolled, the yellow player gets to roll again. They roll a 5, and can again move their token to the highlighted cyan square [slide 3].

<img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/622566a0-7122-41c2-a791-1a969ad88a37"><img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/00a7a400-ba45-4275-b8f3-2c1f1416b4df"><img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/cb05bc3c-dd86-4a71-b5bf-89caa188e37c">

### Stacking Tokens
Players continue to roll, with the ability to move a token out of the home area by rolling a 6. Below we see an example of the blue player rolling a 6 and now having the opportunity to either advance the token already out six spaces, or bring another token out of the home area [slide 1]. They choose to bring another token out, and since two tokens of the same color are on the same space, they become stacked [slide 2] and will now move together [slide 3] (stacking can be done on any space, not just the home space).

<img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/37c68719-5680-4e61-a379-caa5c91d51d4"><img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/f9461949-5dab-4b57-a586-1aa610d5d412"><img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/b4fb4461-8742-4dd5-ac90-3f0be669aac6">

Stacking tokens is generally a good thing - you can now move much quicker by moving them together. Additionally, one player's tokens cannot jump over another player's stacked tokens (you may jump over your own stacked tokens). Notice the scenario below [slide 1] where the yellow player has rolled a 4, but can only move its bottom two tokens. The top token cannot move 4 spaces to attack (we'll cover that later) the single blue token because it is blocked by the stacked blue tokens.

<img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/629d9c2c-1196-4532-bd75-a43dc9100c67">

### Attacking Opponents
Players are able to attack opponents by rolling exactly the number needed to land on an opponent's token(s). See the example below where the blue player has rolled a 3 and has the option of attacking the red player's token [slide 1]. By clicking on the space that the red player is currently on, the blue token will take the red token's place, and the red token will be sent back to its home area [slide 2].

<img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/b911c050-7ee6-4087-9005-c22a64be63a0"><img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/8b3013d9-5914-47c9-ace1-f8c29a5a047d">

### The Home Row
Once a player gets into its home row, they must roll the exact number required to reach the triangular shaped piece of their color (victory space). For example, in the game below, the blue token in the home row must roll a 3 to reach its victory space [slide 1]. If a number higher than a 3 is rolled, the blue token will bounce back the additional the leftover roll beyond 3. For example, if blue rolls a 5, it will go the 3 spaces to the victory space, and then will bounce back into its home squares 2 spaces (5 - 3 = 2) [slide 2]. Once the player rolls the exact value (a 3 in this case), they can move their token into the victory area, and they have accomplished the goal for that token, and that token can no longer be moved [slide 3].

<img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/0e8df775-4edc-4b6a-94d8-dc5ec8f95d6d"><img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/c9edef53-f5d8-4fc1-9c87-bd00318f691c"><img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/fdcb70a7-2ea2-4637-889f-895995ff5297">

### Winning the Game
Once a player is able to move all four of their tokens into their victory space, they have won the game. The blue player has won the game below!

<img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/4a6961ae-7230-4708-ad1b-56623de06d15"><img width="320" alt="image" src="https://github.com/bwiss11/Ludo-with-GUI/assets/79183545/7813cbbc-a4cf-4b2f-9708-0d92474ae87e">


## Additional Information
Please see the 'Rules' section of [Wikipedia's Ludo page](https://en.wikipedia.org/wiki/Ludo) for more information on gameplay.
















