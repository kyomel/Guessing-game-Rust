# Guessing Game

This is a simple command-line guessing game written in Rust. The game generates a random secret number between 1 and 100 (inclusive), and the player tries to guess the number. The game provides feedback on whether the guess is too small, too big, or correct.

## How to Play

1. Clone the repository or download the source code.
2. Make sure you have Rust installed on your system. If not, you can download and install Rust from the official website: [https://www.rust-lang.org/](https://www.rust-lang.org/)
3. Open a terminal and navigate to the project directory.
4. Run the following command to compile and run the game:
```
    cargo run
```
5. The game will display a message asking you to input your guess.
6. Enter a number between 1 and 100 and press Enter.
7. The game will provide feedback on your guess:
- If your guess is too small, it will display "Too small!"
- If your guess is too big, it will display "Too big!"
- If your guess is correct, it will display "You win!" and the game will end.
8. Keep guessing until you find the correct number.

## Code Overview

The code is written in Rust and consists of a single file, `src/main.rs`. Here's a brief overview of the code:

1. The necessary libraries are imported:
- `std::io` for input/output operations
- `rand` for generating random numbers
- `std::cmp::Ordering` for comparing the user's guess with the secret number
2. The `main` function is defined, which is the entry point of the program.
3. A random secret number between 1 and 100 (inclusive) is generated using the `rand::thread_rng().gen_range(1..=100)` function.
4. The game enters a loop where it prompts the user to input their guess.
5. The user's input is read from the standard input using `io::stdin().read_line(&mut guess)`.
6. The user's input is parsed as a `u32` integer using `guess.trim().parse()`. If the parsing fails, the loop continues to the next iteration.
7. The user's guess is compared with the secret number using `guess.cmp(&secret_number)`.
8. Based on the comparison result, an appropriate message is printed:
- If the guess is smaller than the secret number, "Too small!" is printed.
- If the guess is greater than the secret number, "Too big!" is printed.
- If the guess is equal to the secret number, "You win!" is printed, and the loop is exited using the `break` statement.
9. The game continues until the user guesses the correct number.

## Dependencies

The code relies on the following dependencies:

- `std::io`: Standard input/output library for reading user input.
- `rand`: Random number generation library for generating the secret number.
- `std::cmp::Ordering`: Comparison library for comparing the user's guess with the secret number.

These dependencies are part of the Rust standard library and are automatically included when you use Rust.

Feel free to explore the code and have fun playing the guessing game!
