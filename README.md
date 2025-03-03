# **IlmLang (ilm)**  

**IlmLang** is an Islamic-themed programming language created by **Masud Shafin Ahmed (@besaoct)** out of boredom. Written entirely in **Rust**, it merges programming concepts with **Islamic terminology**, making coding both **unique and enjoyable**.  

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
    milaf --enable language
    ```

    or,

    ```bash
     milaf -e language
     ```

    not workin'? use this:

    ```bash
     milaf -e language --force
    ```

- Installs the IlmLang VS Code extension for syntax highlighting and file icon.
- After running, restart VS Code to see `.ilm` files highlighted (e.g., comments dimmed, keywords colored).


Below, you'll find guides for different versions—read them and start coding with **IlmLang!**  

---

## **Guide v0.1**  
📖 **Read here:** [IlmLang v0.1 Guide](https://github.com/besaoct/ilm-release/blob/main/v0.1.md)  

---

## About the Author

IlmLang is a passion project by **Masud Shafin Ahmed** (@besaoct), created for fun and to explore programming with an Islamic twist. Follow the project on GitHub: [github.com/besaoct/ilm](https://github.com/besaoct/ilm) (private tho).

Jealousy Brings Out the Worst in Us. Happy coding! 🚀
