# Hangman Game in Assembly Language

---

## Title Page
  
Hangman Game – Assembly Language Edition

*Course:*  
[COAL]

*Instructor:*  
[UBAIDULLAH]

*Team Members:*  
- [EMAAN]  
- [TANISHA]


## Abstract

This project presents the development of a classic Hangman game implemented in *x86 Assembly Language, utilizing the **Irvine32.inc* library for system-level input/output operations.  
The game offers an interactive, menu-driven experience, focusing on low-level programming concepts like direct memory management, string manipulation, and structured control flow.  
The goal of this project was to reinforce Assembly programming skills while also applying logical thinking to create a creative, playable console game.

## Table of Contents

1. [Abstract](#abstract)  
2. [Introduction](#introduction)  
3. [Objectives](#objectives)  
4. [System Requirements](#system-requirements)  
5. [Methodology](#methodology)  
6. [Implementation Details](#implementation-details)  
7. [Challenges Faced](#challenges-faced)  
8. [Results and Testing](#results-and-testing)  
9. [Future Enhancements](#future-enhancements)  
10. [Conclusion](#conclusion)  
11. [References](#references)

---

## Introduction

Hangman is a classic word-guessing game where players attempt to guess a hidden word one letter at a time, with a limited number of incorrect attempts.  
By implementing Hangman in Assembly Language, the project provided an opportunity to strengthen understanding of low-level system programming concepts, including loops, procedures, memory addressing, and ASCII handling.  
It also challenged us to design clean, maintainable code in a language where small mistakes can easily cause errors.

## Objectives

- Develop a fully functioning Hangman game in *x86 Assembly Language*.
- Implement features such as a main menu, random word selection, graphical hangman display, and scoring system.
- Practice important Assembly concepts like loops, conditions, memory management, and modular code design.
- Deliver a polished, replayable game experience entirely in console mode using *Irvine32* library support.

---

## System Requirements

- *Programming Language:* x86 Assembly (32-bit)  
- *Assembler:* Microsoft Macro Assembler (MASM)  
- *Library:* Irvine32.inc  
- *Operating System:* Windows (32-bit or 64-bit compatible with 32-bit programs)  
- *Hardware:* Standard PC capable of running MASM programs

---

## Methodology

The project was divided into clear, manageable phases:

### 1. Planning
- Designed the project layout and functionality (menu system, gameplay loop, scoring, etc.).
- Finalized a list of random words categorized by length.

### 2. Development
- Built the menu and selection system.
- Implemented the word selection logic.
- Developed the core game loop for letter input, matching, and hangman drawing updates.

### 3. Testing
- Iteratively tested modules (menu, guessing logic, drawing updates).
- Handled edge cases like invalid input and repeated guesses.

### 4. Finalization
- Integrated all modules together.
- Performed debugging and polishing for a smooth gameplay experience.

---

## Implementation Details

### Modules Developed

- *main.asm*  
  Handles the entry point, menu display, user input for menu choices, and overall program control.

- *function_play.asm*  
  Controls the main gameplay loop, manages guesses, tracks wrong attempts, and updates the current word state.

- *function_howtoplay.asm*  
  Displays detailed game instructions to the player.

- *SelectWord.asm*  
  Contains the word bank and randomly selects a hidden word using random number generation.

- *display_hangman.asm*  
  Updates and displays the hangman figure in ASCII art based on the number of wrong guesses.

- *Helper Procedures*
  - Clear screen.
  - Validate and convert user input to lowercase.
  - Check guessed letters against the word.
  - Update the score based on wrong attempts.

---

### Key Game Features

- *Menu System:*  
  Play Game | How to Play | Exit Game

- *Gameplay Logic:*  
  - Random word selection.
  - Letter-by-letter guessing.
  - Dynamic hangman drawing.

- *Scoring System:*  
  - Start with 10 points.
  - Lose 1 point per incorrect guess.

- *Replayability:*  
  - Replay without restarting the program.

## Challenges Faced

- *String and Character Comparisons*  
  Assembly lacks high-level string handling, requiring manual looping and character-by-character comparison.

- *Random Number Generation*  
  Properly seeding and using randomness in Assembly required careful use of Irvine32 procedures.

- *Input Validation*  
  Preventing crashes from invalid user input was tricky; additional checks were added to only accept alphabetical characters.

- *Control Flow Management*  
  Dividing logic into clean procedures while avoiding spaghetti code was crucial and challenging at times.

- *Memory and Stack Management*  
  Managing multiple procedures and passing variables between them demanded careful use of registers and stack operations.


## Results and Testing

The final Hangman game achieved all major objectives:

- Smooth and intuitive menu navigation.  
- Randomized and varied gameplay experience with different words each time.  
- Functional hangman graphics that updated appropriately with wrong guesses.  
- Working score system encouraging efficient guessing.  
- No significant crashes or logical bugs during extended gameplay testing.

### Sample Test Cases

| Test Case | Expected Outcome | Result |
|:---------|:-----------------|:------:|
| Play and guess correctly | Win the game and display congratulations | Passed |
| Play and guess incorrectly 6 times | Lose and display full hangman | Passed |
| Select 'How to Play' from Menu | Display instructions | Passed |
| Invalid character input | Ignore input and reprompt | Passed |
| Replay after win/loss | Restart game without exiting | Passed |

## Future Enhancements

- *Difficulty Modes:*  
  Add Easy, Medium, and Hard levels.

- *Full Word Guessing:*  
  Allow players to guess the entire word.

- *High Score Leaderboard:*  
  Save scores across game sessions.

- *Expanded Word Themes:*  
  Movie names, countries, sports, etc.

- *Multiplayer Mode:*  
  Two players can compete by turn-based guessing.

## Conclusion

Developing the Hangman game in Assembly Language was a rewarding and educational experience.  
The project reinforced fundamental programming concepts like loops, conditions, procedures, stack management, and direct user interaction in a low-level language.  
By combining creativity with technical knowledge, this project made a classic game come to life at the system level, providing valuable hands-on learning and a deeper appreciation for programming close to the hardware.



## References

- Kip Irvine, "Assembly Language for x86 Processors," 7th Edition.  
- Irvine32.inc library documentation.  
- MASM (Microsoft Macro Assembler) Official Documentation.  
- Online resources for ASCII art and Hangman game mechanics.


