# minishell

This project is a simplified version of a Unix shell.

It has basic shell features: displaying a prompt, handling command history, and executing programs based on the PATH environment variable.

It also requires has a few built-in commands like echo, cd, pwd, export, unset, env, and exit.

Additionally, the shell deals with signal handling, specifically for ctrl-C, ctrl-D, and ctrl-\\.

## Requirements 

The project is written in C and requires gcc for compilation, standard C libraries, and the GNU readline library to run

## Get Started

To get started, clone the repo and run 'make' in your terminal

## Features

- **Prompt Display:** Displays a prompt when waiting for new commands.
- **Command History:** Maintains a working history of commands.
- **Executable Search:** Searches and launches executables based on PATH or given paths.
- **Special Characters:** Does not interpret unclosed quotes or non-essential special characters like `\` or `;`.
- **Quotes Handling:**
  - Single quotes `'` prevent meta-character interpretation.
  - Double quotes `"` prevent meta-character interpretation except for `$`.
- **Redirections:**
  - `<`: Redirects input.
  - `>`: Redirects output.
  - `<<`: Heredoc, reads input until a line containing the given delimiter.
  - `>>`: Redirects output in append mode.
- **Pipes:** Implements pipes (`|`) where output of one command is piped as input to the next.
- **Environment Variables:** Handles expansion of environment variables (`$`).
- **Exit Status:** `$?` expands to the exit status of the most recently executed foreground pipeline.
- **Signal Handling:**
  - `ctrl-C`: Displays a new prompt on a new line.
  - `ctrl-D`: Exits the shell.
  - `ctrl-\`: No action.
- **Builtins:**
  - `echo` with `-n` as a possible option
  - `cd` with relative or absolute path
  - `pwd` with no options
  - `export` with no options
  - `unset` with no options
  - `env` with no options or arguments
  - `exit` with no options
