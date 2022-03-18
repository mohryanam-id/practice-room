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
--- | ---
> | Output redirection (truncate)
>> | Output redirection (append)
< | Input redirection
<< | Here document

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
() | Parentheses/Circle Brackets 
{} | Braches/Curly Braces 
[] | Brackets/Square Brackets
## Expansion and substitutions
Representation | Name  
--- | --- 
~ | Tilde expansion 
{...} | Brace expansion  
${...} | Parameter expansion
$(...) | Command substitution
$((...)) | Arithmetic expansion
 
- Represents the user's $HOME environment variable.
To echo tilde 
```bash
echo ~
``` 
add minus on tilde
```bash
echo ~-
```
### Brace Expansions
- Brace expansion creates sets or ranges. 
{a,b,c} {x..y..i}
To create sequentials number and letter
```bash
echo {1..10}
echo {10..1}
echo {a...z}
echo {a..z..2}
```
To combine brace expansion
```bash
echo test_{10..12}{a..d}
echo {a..b}_{1..4}
```
### Parameter Expansions
- Parameter expansion retrieves and transforms stored values.
${...}
To assign parameter
```bash
greeting="hello"
echo $greeting
```
Parameter with position
```bash
echo ${greeting:2:1}

```
To see manual bash
```bash
man bash
```
Parameter replace
```bash
echo ${greeting/ll/rr}
echo ${greeting//l/_}
```
Add paremeter
```bash
echo $greeting:4:3
```
### Command Substitution
- Command substitution put the output of one command inside another.
$(...) older representation `...`
sample
```bash
echo "$(python3 --version | tr [a-z] [A-z])"
```
### Arithmetic Expansion
- Arithmetic expansion does math.
$((...) older representation $[...]
```bash
echo $(( 10 + 2 ))
echo $(( 10 - 2 ))
echo $(( 10 * 2 ))
echo $(( 10 / 2 ))
```
