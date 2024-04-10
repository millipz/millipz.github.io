# Very Advanced Tasks

## 1. find_most_nested

### Instructions

Find the most nested dictionary or list in a nested dictionary or list. It should return the result in a list. If there are multiple dictionaries/lists nested at the same depth, it should return a list of all of them.
    
_Hint: you may want to give your function more than one parameter._

### Example

```py
find_most_nested([]) # []
find_most_nested({}) # [{}]
find_most_nested({ "a": "hello" }) # [{"a": "hello"}]
find_most_nested({ "a": { "b": "hi" }, "c": { "d": "bye" }, "e": 1 }) # [{"b":"hi"}, {"d": "bye"}]

hell = {
  1: {
    2: {
      3: {
        4: {
          "a": "found me!",
        },
      },
    },
  },
}

find_most_nested(hell) # [{"a": "found me!"}]
```

## 2. bubble_sort

### Instructions

A [bubble sort](https://en.wikipedia.org/wiki/Bubble_sort) is an inefficient sorting algorithm that takes a list of numbers and iterates through them, comparing 2 neighbouring numbers at a time. If the first number is greater than the second number, the algorithm will switch their places and move on to the next pair. If the first number is less than the second number, the algorithm will move on to the next pair doing nothing. It will continue looping through the array until there are no more changes to make.

### Example

```py
initial_list = [1, 4, 2, 3]

# the algorithm starts at the beginning of the list
1 > 4? # no, move on
[1, 4, 3, 2]
4 > 3? # yes, switch them
[1, 3, 4, 2]
4 > 2? # yes, switch them
[1, 3, 2, 4]

# loop through again
1 > 3? # no, move on
[1, 3, 2, 4]
3 > 2? # yes, switch them
[1, 2, 3, 4]
3 > 4? # no, move on
[1, 2, 3, 4]

# no more changes to make
final_list = [1, 2, 3, 4]
```

Implement the function `bubble_sort` that will sort a list of numbers using this algorithm.

## 3. boggle

### Instructions

Write a function `boggle`. It should take a board (List) and word (String) and determine if the word is a valid guess as per the rules of the classic board game [Boggle](https://en.wikipedia.org/wiki/Boggle).

For the purposes of our game, the rules are as follows:

- A guess will contain at least one letter.
- A guess is valid if it can be formed by connecting adjacent characters without re-using any previously used positions.
- Letters are counted as adjacent horizontally, vertically or diagonally.
- The guess does not have to be an English word. Any sequence of characters will count as valid so long as it can be made from the board.
- Boards are represented by nested lists as below.

```py
board = [
  ["l", "e", "l"],
  ["p", "h", "l"],
  ["d", "i", "o"],
]
```

Valid words would include 'hello', 'hi', 'helio' or 'help'. 'plod' on the other hand would be invalid as it cannot be made from consecutive characters, despite all the letters being present.

### Example

```py
board = [
  ["e", "a", "r", "a"],
  ["n", "l", "e", "c"],
  ["i", "a", "i", "s"],
  ["b", "y", "o", "r"],
]

boggle(board, "ear"); # true
boggle(board, "ears"); # false
boggle(board, "rio"); # true
boggle(board, "cereal"); # false
boggle(board, "rscareioybailnea"); # true
```