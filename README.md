# minishell

A small Unix shell in C, modelled on bash. Made as part of the 42 curriculum at Codam.

## Build

You need `cc`, `make` and the `readline` library.

```sh
git clone https://github.com/rowanverschoor/minishell.git
cd minishell
make
./minishell
```

## Features

- Prompt with command history (readline)
- Runs programs from `PATH`, or by relative or absolute path
- Pipes `|`
- Redirections `<` `>` `>>`
- Heredoc `<<`
- Single and double quotes
- Environment variables `$VAR` and exit status `$?`
- Wildcard `*` for the current directory
- `Ctrl-C`, `Ctrl-D` and `Ctrl-\` behave like in bash

## Builtins

| Command | Notes |
| --- | --- |
| `echo` | with `-n` |
| `cd` | relative or absolute path |
| `pwd` | |
| `export` | |
| `unset` | |
| `env` | |
| `exit` | with optional exit code |

## Example

```sh
megashell>$ cat << EOF | grep hello > out.txt
> hello world
> bye
> EOF
megashell>$ echo $?
0
```

## Authors

- [roversch](https://github.com/rowanverschoor)
- [nhendrik](https://github.com/Nissey05)
