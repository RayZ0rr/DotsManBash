# DotsManBash :- A collection of bash scripts to manage dotfiles locally and to git repositories

## What ?
Ever tired of going to dotfiles repository to commit and push changes ? Or Adding files to dotfiles repository and then symlinking it to their correct locations?
Here is a collection of scripts to manage all these tasks.
* `dotsgit` script handles interaction of private repository and public repository (more can be added) with git as well as with each other (using `dotsSync` script)
* `dotsinit` script handles creating/removing symlinks or copies from repositories to correct locations in home folder. 
* `dotsSync` manages interactions between local public and private reopsitories (sync, dry-sync)
* `myfonts` download,list,refresh fonts

## Dependencies
1. [Stow](https://www.gnu.org/software/stow/)
2. `find`
3. `rsync`

# Install
Just copy the script to anywhere in your _`PATH`_ ( `echo $PATH` ). Make sure the script is executable ( `chmod +x dots*` )

# Usage

* All the scripts starting with '`dots`' needs some variables (like repository directory path) to be set to work. Open the script with your favourite editor and add them.
* All the scripts need atleast one argument to do various tasks. Running the script without argument(s) or with invalid argument(s) will show the help menu. 
* `myfonts` script have some fonts specified in the script. If you want more, you can add it yourself.
* Open the scripts and look at the final `case statements` to view all available valid arguments.
* Make use of the [aliases](./aliases) file to create useful aliases.

## Examples
----------

### `dotsgit`
```sh
# Show both private and public repository status
dotsgit status 

# Show both private and public repository log
dotsgit logA 

# Commit to both private and public repository
dotsgit commitA "<commit message>"
```

### `dotsinit`
```sh
# Dry run of all symlinking operations
dotsinit dry

# Symlink files in home folder
dotsinit home

# Remove and symlink files in polybar and neofetch
dotsinit rm polybar neofetch
dotsinit config polybar neofetch
```
