# IlmLang (ilm)

**IlmLang** is an Islamic programming language created by Masud Shafin Ahmed (@besaoct) out of boredom. Written purely in Rust, it blends programming concepts with Islamic terminology, offering a unique and fun way to code. This is version `0.1`, an early but functional release.

## Features

IlmLang currently supports the following syntax:

```ilm
bismillah

    maktub real_name = "Shafin";  // Declare a variable
    maktub a = 4;                 // Integer variable
    maktub b = 2;

    // ignore this line          // Single line comment

    istima userName;              // Read user input into a variable
    
    qawl_("\nPrinting user input: $userName");  // Print with newline
    qawl_("$a, $b - ${a + b}, ${a * b}, ${a / b}, ${a % b}");  // Interpolation with expressions
    qawl_(" ${6+6}");             // Simple expression evaluation

    qawl_("Assalamu'Alaikum $real_name");  // Greeting with variable

    tajdid real_name = "Ahmed";   // Reassign a variable

    qawl("$real_name with new line without using qawl_\n");  // Print without newline function
    qawl("Assalamu'Alaikum $real_name");

    /*
      This is a
      comment block.
      It will not be executed.
    */

alhamdulillah
```

### Syntax Explanation

- **`bismillah`**: Marks the start of the program (like `main()` in other languages).
- **`maktub`**: Declares a variable (e.g., `maktub a = 4;` is like `let a = 4;` in Rust).
- **`istima`**: Reads user input into a variable.
- **`qawl`**: Prints output without a newline.
- **`qawl_`**: Prints output with a newline.
- **`${expression}`**: Evaluates expressions inside strings (e.g., `${a + b}`).
- **`tajdid`**: Reassigns a variable’s value.
- **`/* */`**: Block comments, ignored by the interpreter.
- **`//`**: Single line comment, ignored by the interpreter.
- **`alhamdulillah`**: Marks the end of the program.

This example demonstrates variable declaration, input/output, string interpolation, and comments.

## Prerequisites

Since IlmLang is written in pure Rust, you’ll need the following to run it:

- **Rust**: The Rust programming language and its package manager, Cargo.
  - Install Rust via [rustup](https://rustup.rs/):
  
    ```bash
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
    ```

    - Follow the prompts, then run:

      ```bash
      source $HOME/.cargo/env
      ```

    - Verify installation:
  
      ```bash
      rustc --version
      cargo --version
      ```

- **A Terminal**: Any terminal to execute commands (e.g., Terminal on macOS/Linux, Command Prompt/PowerShell on Windows).
- **VS Code (Optional)**: For syntax highlighting support (see commands below).

## Installation

To install IlmLang, use Cargo to fetch and build it from crates.io:

```bash
cargo install ilm
```

- This installs the `milaf` binary (version `0.1`) to `~/.cargo/bin/`.
- Ensure `~/.cargo/bin/` is in your PATH:

  ```bash
  echo $PATH
  ```

  - If not, add it (e.g., in `~/.bashrc` or `~/.zshrc`):
  
    ```bash
    export PATH="$HOME/.cargo/bin:$PATH"
    source ~/.bashrc  # or ~/.zshrc
    ```

Verify installation:

```bash
milaf -v
```

- Output: `0.1`

## Commands

IlmLang provides the following commands via the `milaf` CLI:

- **Run a Program**:

  ```bash
  milaf run <file.ilm>
  ```

  - Example:
  
    ```bash
    milaf run example.ilm
    ```

    - Runs the `.ilm` file and outputs the result (e.g., “Masha’Allah!” on success).

- **Check Version**:
  
  ```bash
  milaf -v
  ```

  - Output: `0.1`

- **Show Help**:
  
  ```bash
  milaf -h
  ```

  - Displays usage and available commands:
  
    ```bash
    milaf 0.1
    A command-line tool for running IlmLang programs

    USAGE:
        milaf [OPTIONS] [SUBCOMMAND]

    OPTIONS:
        -e, --enable <FEATURE>    Enable a feature (e.g., 'language' for VS Code support)
        -h, --help                Print help information
        -v, --version             Print version information

    SUBCOMMANDS:
        run    Run an IlmLang program
    ```

- **Enable VS Code Syntax Highlighting**:
  
  ```bash
  milaf -enable language
  ```

  - Installs the IlmLang VS Code extension for syntax highlighting and file icons.
  - After running, restart VS Code to see `.ilm` files highlighted (e.g., comments dimmed, keywords colored).

## Example Usage

1. Create a file `example.ilm` with the code above.
2. Run it:

   ```bash
   milaf run example.ilm
   ```

   - Sample interaction:
  
     ```bash
     > ilm

     <enter your name, e.g., "Ok!">
     Printing user input: Ok!
     4, 2 - 6, 8, 2, 0
      12
     Assalamu'Alaikum Shafin
     Ahmed with new line without using qawl_

     Assalamu'Alaikum Ahmed

     +---------------------------------+
     | Masha'Allah! Aiktamal altanfidh |
     +---------------------------------+
     0.002s
     ```

## About the Author

IlmLang is a passion project by **Masud Shafin Ahmed** (@besaoct), created for fun and to explore programming with an Islamic twist. Follow the project on GitHub: [github.com/besaoct/ilm](https://github.com/besaoct/ilm).
