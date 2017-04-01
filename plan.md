# Thoughts on Objects
- Board object with 2D array, similar to TTT
- BoardSpace object that has lots of instances inside the Board array
- Player object can also be the same as TTT

[
  [BoardSpace, BoardSpace, ...],
  [BoardSpace, BoardSpace, ...],
]

# Tips
- ONLY create these classes as you need them, and DON'T copy paste
- Unit test each object as you create it


# Order of Operations
- Create the main.rb
- Think through the first user steps of playing the game (i.e. seeing stuff printed to the screen, etc...)
  - Actual first step: Requesting player names, creating PLayer object, unit testing it
- Possilbe next thing: user seeing the board
- That means we need a board and a print method!
  - Create a board object
  - Unit test a print and an initialize method
- Come back to main.rb and use that board objects

Once we get to the actual gameplay:
- We definitely need a WHILE loop of some sort. Ultimately, it should keep going as long as the board doesn't have a winner yet (which will be a future method), but for right now use a stand-in.
- Go through the process of the player choosing a slot (this is where it gets real)

Example code for choosing a slot:

```
def place_piece(column)
  chosen_space = lowest_slot(column)
  chosen_place.player = player
end

def lowest_slot(column)

end
```

# Thoughts on finding a winner

```
class Board
def initialize
  ...
  @winner = nil
end

# call this method in our WHILE loop to see if we're done
def game_over?
  # is winner something other than nil?
end

# call this method from main.rb after each turn
def check_for_winner
  check_for_horizontal_winner
  check_for_vertical_winner
  # check_for_diagonal_winner
end

def check_for_horizontal_winner
  # loop through each row of the board looking for a horizontal win
    # if we find one, assign @winner to the player who got four squares in a row
end
```
