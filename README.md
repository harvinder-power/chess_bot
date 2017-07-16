# Chess - Machine Learning

## Introduction
This repository is designed to develop a machine learning algorithm for a chess player which learns from previous movements. In brief, the computer uses a partial lookup table which it uses to choose its next move. However, it will also use random exploration to ensure that it is able to search for better moves rather than perpetuate poor moves.

## Platforms
This code has been tested and verified on Mac OS. The code should be safe, and functional on Linux and Windows. If issues arise, please submit a pull request if the fix is known.

## Initialisation
The following python packages are required for this game - chess. This can be easily achieved through installing via pip in terminal, using the following commands:

```
>> sudo easy_install pip
>> pip install chess
```

Now all the relevant packages have been installed, you are ready to play.

As of 16th July 2017, the game currently exists in a iPython file format which can be used using Jupyter Notebook (see [Jupyter.org](http://jupyter.org) for more details on installation)

## Current State
- Game uses Stockfish chess engine for testing purposes
- Currently computer vs computer (can be changed to player vs computer, or player vs player) through modification of the following:

```
while board.is_game_over() == False:
    if board.turn == True:
        #This denotes white's turn to move
        engine.isready()
        computer_movement()
    if board.turn == False:
        #This denotes black's turn to move
        engine.isready()
        computer_movement()
```

`computer_movement()` can be changed to `player_movement()` to enable player interaction.

## Next Steps
- Generate reinforcement engine for moves
- Update board rather than print another board for each move
