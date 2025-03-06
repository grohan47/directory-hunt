# directory-hunt
A small directory hunt created for an Escape Room event.

Instructions on how to use:

Overload the `cd` command in your `.bashrc` by appending the following function definition:

```
cd() {
    # Use the builtin cd to change directories.
    builtin cd "$@" || return

    # If a per-directory config file exists, source it.
    if [[ -f .cdrc ]]; then
        source .cdrc
    fi
}
```
This overloaded function will source the .cdrc file in each sub-directory and run the commands written within it (which are hints to aid you in your hunt!)

Do NOT attempt this directory hunt in the GUI-- It ruins any point of it!

### Dependencies:

`figlet`
`vlc`
