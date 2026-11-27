# Operating Systems - Assignment 2

**Basic Forks and C Style Development**

**Student Name:** Shaimaa Mohamed Kotit  
**Student ID:** 24100570  
**Course:** CSE233 - Operating Systems  
**University:** Alamein International University

## Description

This assignment demonstrates three basic operating system concepts using C and Linux. It is based on the examples in Lab 5 (Process Management).

- **Process creation:** Create a child process using `fork()` and display the process IDs.
- **Linker:** Compile and link two C files into one executable program.
- **Loader:** Use `ldd` to list the shared library dependencies of an executable.

## Installation

### Requirements

- Linux Ubuntu
- GCC compiler
- GNU Make
- `ldd` (normally available on Linux)
- Git (optional, for cloning the repository)

Install the required build tools on Ubuntu or Linux Mint if they are not already installed:

```bash
sudo apt update
sudo apt install gcc make
```

Download and extract the project ZIP file, or clone the repository:

```bash
git clone https://github.com/shaimaakotit-29/OS-Assignment.git
cd OS-Assignment
```

## Usage

Open a terminal in the project directory and compile all three examples:

```bash
make
```

### 1. Process Creation

```bash
./process_creation
```

The program prints the parent and child process IDs. Example output:

```text
This is the parent process. PID: 1234
This is the child process. PID: 1235
```

The actual IDs and the order of the messages may change each time.

### 2. Linker

```bash
./output_program
```

Expected output:

```text
Hello from file1!
```

### 3. Loader

```bash
./simple_program
ldd simple_program
```

Expected program output:

```text
This is a simple program.
```

The `ldd` command lists the shared library dependencies. The exact library paths and addresses depend on the system.

### Clean the project

```bash
make clean
```

This removes the generated executable files.

## Visuals (Screenshots)

### Process Creation and Compilation

![Compilation and process creation](screenshots/process_creation.png)

### Linker Output

![Linker program output](screenshots/linker.png)

### Loader Output

![Loader program output and shared libraries](screenshots/loader.png)

## Project Structure

| File or directory | Description |
| --- | --- |
| `process_creation.c` | Demonstrates process creation using `fork()`. |
| `file1.c` | Defines the `hello()` function. |
| `file2.c` | Declares and calls the `hello()` function. |
| `simple_program.c` | Prints a message and provides an executable for inspecting dependencies. |
| `Makefile` | Builds all three executables and removes them using the clean target. |
| `answers.txt` | Explains the C files, Makefile, linker, loader and process control commands. |
| `screenshots/` | Contains compilation and execution screenshots. |
| `README.md` | Explains the project and how to use it. |
| `LICENSE` | Contains the MIT license. |

For the theory answers and code explanations, see [answers.txt](answers.txt).

## Support

For technical issues with the repository, use the [GitHub Issues page](https://github.com/shaimaakotit-29/OS-Assignment/issues), if enabled. For questions about the assignment requirements, refer to the course instructor.

## Contributing

This repository is for an individual course assignment. Any contributions or changes must follow the course rules. To check a change locally, run `make clean`, `make`, and the three examples described in the Usage section.

## Authors and Acknowledgments

- **Student submitting the assignment:** Shaimaa Mohamed Kotit (24100570).
- **Code reference:** CSE233 Lab 5 - Process Management, Alamein International University.

## License

See the [MIT License](LICENSE). It applies to original contributions that the copyright holder is entitled to license.
Third-party course materials and any reused code remain subject to their original rights and applicable permissions.

## Project Status

This repository contains the examples and documentation prepared for Assignment 2.
