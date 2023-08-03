# Shell Terminal Implementation In C

This project is a custom shell terminal written in C language. It replicates several core functionalities of standard shell terminals and incorporates additional features for a smooth user experience.

## Features

- Command execution
- Input/output redirection
- Background processing
- Process management using system calls like `fork()`, `exec()`, `wait()` etc.
- Input/output operations managed effectively using file descriptors and redirection operators.

## Implementation

The project comprises several helper functions and a main function that is responsible for running the shell until the user decides to exit.

### Helper Functions

#### 1. `parseInput()`
This function parses the input string into multiple commands or a single command with arguments depending on the delimiter (&&, ##, >, or spaces).

#### 2. `get_commandArgs()`
This function breaks the isolated command strings into their constituent command and command arguments, and returns the array of strings.

#### 3. `executeCommand()`
This function forks a new process to execute a command.

#### 4. `executeCommandRedirection()`
This function runs a single command with output redirected to an output file specificed by user.

#### 5. `executeParallelCommands()`
This function runs multiple commands in parallel.

#### 6. `executeSequentialCommands()`
This function runs multiple commands sequentially.

### Signal Handling Functions

#### 1. `sigintHandler()`
This function handles the SIGINT (CTRL + C) signal.

#### 2. `sighandler()`
This function handles the SIGTSTP (CTRL + Z) signal.

### Main Function

This function runs the shell until the user decides to exit. It reads commands from the user, processes the commands, and calls the appropriate helper functions.

## How To Run

1. Clone the repository.
2. Compile the code using gcc: `gcc myshell.c -o myshell`
3. Run the shell: `./myshell`
4. Enter the commands.

## Notes

- While the shell terminal supports several core functionalities, some commands may not function as expected due to the custom nature of this shell implementation.
- Feel free to contribute and improve the functionality of this shell terminal.
