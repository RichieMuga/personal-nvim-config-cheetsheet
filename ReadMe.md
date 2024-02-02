# Editing Text
`dd` or `:d` deletes the current line

`yy` or :y or `Y` "Yank" (cut) the current line

`p` Paste the text you yanked or deleted. This will put characters after the cursor and put lines below the current line depending on what you yanked. To paste above the current line, use `P`.

`x` delete the character underneath the cursor

`Nx` delete the N characters under and following the cursor (e.g. 3x deletes the 3 characters under and following the cursor).

# Undo/Redo
`u` undo the last action

`U` undo all recent changes made to the current line

`ctrl-r` redo

# Saving a file in nvim
Press `Esc` key and type == `w` to save a file in vim.
One can press Esc and type `:wq` to save changes to a file and exit from vim
Another option is to press `:x`


# This has ever happend to me and I really dont want to repeat this mistake father lord!
## I got the message "Found a swap file."
I spent days trying to fix this

if you lose I connection to myth while editing a file. (It can also happen if you try to edit the same file in two terminal windows; you shouldn't do this.)

Here's the recommended process for resolving it: First, hit o for "open read-only". This shows you the version of the file that was last saved. Look through it. Does it have your most recent changes?

#### Yes, this is the latest version of the file: Great! To clean up the swap file, :q out, then run vim on the file again. This time, hit d to delete the swap file. (Warning: you can't undo this.)

#### No, some of my changes are missing: OK, don't panic. Quit out of vim, and start it again. This time, hit r for "recover." This will show you the version of the file from the interrupted session. If that's (closer to) the version you want to keep, save it, then follow the steps above to clean up the swap file.

#### How do I avoid the above issue coming up next time? Make sure you exit nvim cleanly. Don't just hit the "X" button on your terminal. Also, don't close your laptop lid while nvim is open (more generally, putting your laptop to sleep while connected to myth could lead to other problems, because it generally turns off your internet connection).
