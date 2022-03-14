# Bash
## What's bash ?
- Bash is a widely used shell, available in many platforms.
- Short for Bourne Again Shell, in reference to the earlier Bourne Shell.
- An Interactive command-line shell that also allows commands to be combined into scripts files, which can be run like programs.
- Combining commands into scripts saves time and reduce errors.
- Bash is preinstalled on most Linux systems.
- Bash is primaly used on Linux systems.
- Use Linux system, virtual machine, or cloud instance to learn Bash.
- The version of Bash on macOS is highly outdated. It needs to be updated.
- To run bash on Windows, use Git Bash or WSL (or a linux VM)

To check bash version in command line:
```bash
bash --version
```
To check bash path
```bash
echo $SHELL
```
To change path
```bash
chsh
```
## Pipes
- control the output
- the symbol is "|"
sample code:
```bash
ls -a | ws
```

## Redirections
- Control the output and the input
To create new file
```bash
ls -a > list.txt
```
To append onto the end of the existing file
```bash
ls -a >> list.txt
```
To create new file from output and error
```bash
ls /uncreatedfolder 1>output.txt 2>error.txt
```
To create input redirection
```bash
cat < list.txt
```
To use here document
```bash
cat << EndOfText
heredoc>Random string
heredoc>Random string2
heredoc>EndOfText
Random string
Random string2
EndOfText
```

Symbol | Function
:---: | ---
>|Output redirection (truncate)
>>|Output redirection (append)
<|Input redirection
<<|Here document
## Built-in Commands
- Bash includes built-in commands (Part of bash itself).
- Some bash built-in commands have the same name as other commands.
```bash
builtin echo hello 
```
## Other Commands
- Command that does not depend on Bash (separate software).
```bash
command echo hello
```
To check echo is a shell builtin.
```bash
command -V echo
```
To disabled and enabled shell builtin command.
```bash
enable -n echo
enable echo
```
## Parentheses, Braces, Brackets
- Bash uses these characters differently that other languages.
Character |Description
--- | ---
()|Parentheses/Circle Brackets 
{}|Braches/Curly Braces 
[]|Brackets/Square Brackets
## Expansion and substitutions
Representation | Name
--- | ---
~ | Brace expansion 
### Bash Expansions
### Bash Substitutions
### Brace Expansions
### Parameter Expansions
### Command Substitution
### Arithmetic Expansion
