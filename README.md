# Minishell

_As beautiful as a shell._

This project is about creating a simple shell — your very own little **Bash**.  
You will gain extensive knowledge about processes, file descriptors, signals, and command parsing.

---

## Mandatory Part

### Program Name
`minishell`

### Files to Turn In
- `Makefile`
- `*.h`
- `*.c`

### Makefile Rules
- `NAME`
- `all`
- `clean`
- `fclean`
- `re`

### External Functions Allowed
- `readline`, `rl_clear_history`, `rl_on_new_line`, `rl_replace_line`, `rl_redisplay`, `add_history`  
- `printf`, `malloc`, `free`, `write`, `access`, `open`, `read`, `close`  
- `fork`, `wait`, `waitpid`, `wait3`, `wait4`  
- `signal`, `sigaction`, `sigemptyset`, `sigaddset`, `kill`, `exit`  
- `getcwd`, `chdir`, `stat`, `lstat`, `fstat`, `unlink`, `execve`  
- `dup`, `dup2`, `pipe`  
- `opendir`, `readdir`, `closedir`  
- `strerror`, `perror`, `isatty`, `ttyname`, `ttyslot`, `ioctl`  
- `getenv`, `tcsetattr`, `tcgetattr`, `tgetent`, `tgetflag`, `tgetnum`, `tgetstr`, `tgoto`, `tputs`  

### Libft
✅ **Authorized**

### Requirements
Your shell must:  
- Display a prompt when waiting for a new command.  
- Have a working **history**.  
- Search and launch executables (using `$PATH`, relative or absolute paths).  
- Use **at most one global variable** to indicate a received signal (must only store the signal number).  
- Correctly handle quoting:  
  - `'single quotes'` → prevent interpretation of meta-characters.  
  - `"double quotes"` → prevent interpretation of meta-characters except `$`.  
- Implement **redirections**:  
  - `<` : redirect input.  
  - `>` : redirect output.  
  - `<<` : heredoc (delimiter-based input, does not update history).  
  - `>>` : append output redirection.  
- Implement **pipes** (`|`) between commands.  
- Handle **environment variables** (`$VAR`) and `$?`.  
- Correctly handle **Ctrl-C, Ctrl-D, Ctrl-\** like in Bash:  
  - `Ctrl-C` → new prompt on a new line.  
  - `Ctrl-D` → exit the shell.  
  - `Ctrl-\` → does nothing.  
- Implement the following **builtins**:  
  - `echo` (with `-n` option)  
  - `cd` (relative or absolute path only)  
  - `pwd` (no options)  
  - `export` (no options)  
  - `unset` (no options)  
  - `env` (no options or arguments)  
  - `exit` (no options)  

---

## Compilation
```bash
make
```

## Usage Example
```bash
./minishell
```

---
