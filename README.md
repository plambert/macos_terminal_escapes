# MacOS Terminal Escapes

Bash functions to set terminal excapes on MacOS's `/Applications/Utilities/Terminal.app`.

# Usage

All of the functions can easily be imported into your shell, or you can specify specific functions to import, or
you can call the functions as external programs.

## Making all functions available to your bash script

Sourcing `bin/macos_terminal_escapes` into your shell, as below, will make all of the functions available.

```bash
% source bin/macos_terminal_escapes
```

## Making specific functions available to your bash script

Sourcing `bin/macos_terminal_escapes` into your shell with the `import` argument will only install
the functions you specify.

```bash
% source bin/macos_terminal_escapes import term_working_directory term_document term_title
```

## Calling specific functions directly

You can run `bin/macos_terminal_escapes` directly with the function name and arguments, and it will
execute them.

```bash
% bin/macos_terminal_escapes term_working_directory "$(pwd)"
```

## Adding the functions to your $PATH

If the script is called via a symlink named for a function, then it will run that function with the given
arguments.  The `link` subcommand will create these links in the given bin directory.  For example:

```bash
% bin/macos_terminal_escapes link ~/bin
Created links in ~/bin:
  term_working_directory
  term_document
  term_title
  ...
```

# Known Limitations

* The version of `Terminal.app` is not checked, so some features may not be available.

# Contributing

Source is maintained at [github.com/plambert/macos_terminal_escapes][].  You can submit pull requests there, and open
issues for bug fixes and feature requests.

[github.com/plambert/macos_terminal_escapes]: https://github.com/plambert/macos_terminal_escapes
