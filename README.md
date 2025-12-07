# Evil-Hangman

An advanced C implementation of the classic "Evil Hangman" game that uses AVL trees and advanced data structures to make the game as difficult as possible for the player.

What is Evil Hangman?
Unlike traditional Hangman, Evil Hangman never commits to a specific word until forced to. Instead, it dynamically maintains the largest possible family of words that match the current game state, making it nearly impossible to win!

Features
- Dynamic Word Family Management: Uses AVL trees to efficiently group and track word families during gameplay
- Custom String Library: Built-from-scratch string manipulation functions without relying on <string.h>
- Generic Vector Implementation: Type-safe dynamic arrays using void pointers and function pointers
- Memory-Safe Operations: Proper memory management with no leaks
- Flexible Dictionary Support: Processes dictionaries with 127,000+ words
- Word Length Selection: Support for words from 2-29 characters (with some exclusions)
- Configurable Difficulty: Players choose the number of guesses

Architecture
The project demonstrates several advanced C programming concepts:

1. my_string.h/c - Custom string library with dynamic memory management

 - String initialization, concatenation, comparison
 - Push/pop operations
 - Memory-safe character access
 - File I/O operations


2. generic_vector.h/c - Generic dynamic array implementation

 - Type-agnostic storage using void pointers
 - Function pointer callbacks for assignment and destruction
 - Automatic capacity expansion


3. associative_array.h/c - AVL tree-based associative array

 - O(log n) insertion and lookup
 - Self-balancing for optimal performance
 - Efficient word family grouping


4. main.c - Game logic and user interaction

 - Input validation
 - Game state management
 - Word family computation


Getting Started

- GCC compiler (or any C99-compatible compiler)
- Make (optional, for build automation)
- A Unix-like environment (Linux, macOS, WSL)

How to Play

1. Choose Word Length: Enter a word length between 2-29 characters

 - Note: Lengths 23, 25, 26, and 27 are not available due to dictionary limitations

2. Set Number of Guesses: Choose how many incorrect guesses you're allowed
   
3. Make Your Guesses: Enter one letter at a time

The game shows you:

- Number of possible words remaining
- Guesses remaining
- Letters you've already used
- Current word pattern (with dashes for unknown letters)

4. Win or Lose:

 - Win: Reveal all letters before running out of guesses
 - Lose: Run out of guesses (the computer reveals the word it "chose")

Potential improvements:

- Add difficulty levels (word family selection strategies)
- Implement hint system
- GUI using ncurses or GTK
- Save/load game state
- Performance metrics and statistics tracking
- Custom dictionary support

Thank you for checking this out!
