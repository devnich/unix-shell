-   [Introducing the shell](#introducing-the-shell)
    -   [Reasons to use the shell](#reasons-to-use-the-shell)
    -   [\"Unix\"](#unix)
    -   [\"Shell\"](#shell)
    -   [The past is always with us](#the-past-is-always-with-us)
-   [Navigating files and
    directories](#navigating-files-and-directories)
    -   [File system layout](#file-system-layout)
    -   [Who are you?](#who-are-you)
    -   [Where are you?](#where-are-you)
    -   [What\'s in this directory?](#whats-in-this-directory)
    -   [Getting help](#getting-help)
    -   [Exploring other directories](#exploring-other-directories)
    -   [Relative vs. absolute paths](#relative-vs.-absolute-paths)
-   [Working with files and
    directories](#working-with-files-and-directories)
    -   [Creating directories](#creating-directories)
    -   [Moving files and directories](#moving-files-and-directories)
    -   [Copying files and directories](#copying-files-and-directories)
    -   [Removing files and
        directories](#removing-files-and-directories)
    -   [Create a backup archive](#create-a-backup-archive)
    -   [Operations with multiple files and
        directories](#operations-with-multiple-files-and-directories)
-   [Pipes and filters](#pipes-and-filters)
    -   [Motivating example with `wc`](#motivating-example-with-wc)
    -   [Capturing output from
        commands](#capturing-output-from-commands)
    -   [Filtering output](#filtering-output)
    -   [Passing output to another
        command](#passing-output-to-another-command)
    -   [Combining multiple commands](#combining-multiple-commands)
    -   [History and pipes](#history-and-pipes)
-   [Shell scripts](#shell-scripts)
    -   [Creating and running a script](#creating-and-running-a-script)
    -   [Generalize your script](#generalize-your-script)
    -   [(Optional) Text processing with Unix
        tools](#optional-text-processing-with-unix-tools)
-   [Loops](#loops)
    -   [A basic loop](#a-basic-loop)
    -   [Simplify your loop with globs](#simplify-your-loop-with-globs)
    -   [Generalize your loop with unlimited
        arguments](#generalize-your-loop-with-unlimited-arguments)
    -   [Make your script executable](#make-your-script-executable)
-   [Finding things](#finding-things)
    -   [Find](#find)
    -   [Grep](#grep)
-   [Shell extras](#shell-extras)
-   [Credits](#credits)
-   [References](#references)
-   [Data Sources](#data-sources)

# Introducing the shell

## Reasons to use the shell

1.  Automate basic tasks
2.  Underlies many other open source languages and applications and can
    be used to glue them together
3.  Essential for system administration, remote computing, and
    high-performance computing
4.  Many concise special-purpose tools that can make your life easier
5.  Complements more fully-featured application programming languages

## \"Unix\"

Powerpoint slides: Unix family tree

1.  Unix-like operation systems share a common architecture and layout
2.  Roughly compatible, with similar (or identical) shells and tools
3.  The environment in which most open-source software was written

## \"Shell\"

-   Broadly speaking, there is a tension between making computer systems
    fast and making them easy to use.
-   A common solution is to create a 2-layer architecture: A fast,
    somewhat opaque core surrounded by a more friendly scriptable
    interface (also referred to as \"hooks\" or an \"API\"). Examples of
    this include video games, Emacs and other highly customizable code
    editors, and high-level special-purpose languages like Stata and
    Mathematica.
-   Unix shell is the scriptable **shell** around the operating system.
    It provides a simple interface for making the operating system do
    work, without having to know exactly how it accomplishes that work.

## The past is always with us

The design and terminology of modern computers is based on metaphors
from a previous age.

1.  Files and folders
2.  Teletype input and output
3.  Modern touch devices don\'t expose the file system, so you may be
    less comfortable with navigating directory trees than people whose
    primary computing devices were desktop computers

# Navigating files and directories

## File system layout

Powerpoint slides: \"Navigating files and directories\"

## Who are you?

``` bash
whoami
```

## Where are you?

1.  Current working directory

    ``` bash
    pwd                             # Print Working Directory
    ```

2.  By default, this is probably your home directory (discuss how to
    view this in Finder or File Explorer)

    1.  Linux

        ``` example
        /home/nelle
        ```

    2.  Mac OS

        ``` example
        /Users/nelle
        ```

    3.  Windows

        ``` example
        C:\Users\nelle
        ```

## What\'s in this directory?

1.  List the contents of the directory

    ``` bash
    ls                              # List directory contents
    ```

2.  Command flags modify what a command does

    ``` bash
    ls -F     # show category markers
    ```

## Getting help

``` bash
ls --help                       # In-line help info; should work in Windows
man ls                          # Manual for "ls"
```

-   You can navigate through the man page using the space bar and arrow
    keys
-   Quit man with \"q\"
-   Online references are available for Windows users who don\'t have
    man pages: <https://linux.die.net/>

## Exploring other directories

1.  When a command is followed by an argument, it acts on that argument.

    ``` bash
    ls -F Desktop                   # get contents of folder
    ls -F Desktop/shell-lesson-data # get contents of subfolder
    ```

2.  Move down the directory tree

    ``` bash
    cd Desktop
    cd shell-lesson-data
    cd exercise-data
    ```

3.  Now that you\'re \"in\" a new location, the context for your
    commands is different

    ``` bash
    pwd
    ls -F

    # This produces an error because the folder is in a different location
    # relative to the working directory
    cd shell-lesson-data
    ```

4.  Move up the directory tree `.` is shorthand for \"current
    directory\"; `..` is shorthand for \"parent directory\"

    ``` bash
    # Show hidden files, including current and parent directories
    ls -a

    # You can combine flags
    ls -Fa

    # Move to parent directory
    cd ..
    ```

5.  Shortcuts

    ``` bash
    cd ~   # go to home directory
    cd -   # go back to previous directory
    ```

## Relative vs. absolute paths

1.  An absolute path specifies a location from the root of the file
    system.
2.  A relative path specifies a location starting from the current
    location.

# Working with files and directories

## Creating directories

1.  See where we are and what we have

    ``` bash
    pwd
    cd exercise-data/writing  # traverse several layers at once
    ls -F
    ```

2.  Create a directory

    ``` bash
    # Make a subdirectory
    mkdir thesis
    ls -F

    # Make multiple directories; create intermediate dirs as required
    mkdir -p ../project/data ../project/results

    # Show all directory contents recursively
    ls -FR ../project
    ```

3.  Create a text file. Note that everything is available through the
    file browser and the terminal.

    ``` bash
    cd thesis
    nano draft.txt
    ```

    ``` example
    This is my first draft
    boop beep boop
    ```

4.  Edit with Notepad / TextEdit, then re-edit with nano.

## Moving files and directories

1.  Move our file to a new location

    ``` bash
    cd ~/Desktop/shell-lesson-data/exercise-data/writing

    # Rename the file by moving it
    mv thesis/draft.txt thesis/quotes.txt

    # Verify the new file name
    ls thesis

    # You can also specify the exact file name
    ls thesis/quotes.txt
    ```

2.  Move our file to the current working directory

    ``` bash
    mv thesis/quotes.txt .
    ls thesis/quotes.txt # Not here anymore
    ls                   # now here
    ```

## Copying files and directories

1.  Copy a single file

    ``` bash
    cp quotes.txt thesis/quotations.txt
    ls thesis
    ls

    # Alternatively
    ls quotes.txt thesis/quotations.txt
    ```

2.  Copy a directory recursively

    ``` bash
    cp -r thesis thesis_backup
    ls thesis thesis_backup
    ```

## Removing files and directories

1.  Remove a file

    ``` bash
    rm quotes.txt
    ls quotes.txt
    ```

2.  Remove a file interactively Deletion is forever!

    ``` bash
    rm -i thesis_backup/quotations.txt
    ```

3.  Remove a directory and its contents

    ``` bash
    rm thesis      # This gives un an error
    rm -ri thesis  # Remove recursively
    ```

## Create a backup archive

Deletion is forever. Consider making a backup archive as part of your
workflow.

1.  Create an archive with `tar` (\"tape archive\").

    ``` bash
    cd ~/Desktop/shell-lesson-data/exercise-data/

    # [c]reate a new archive with the given [f]ilename
    tar -cf writing.tar writing/
    ```

2.  Create a compressed (zipped) archive `tar` is an old utility and can
    be finicky about the order of flags.

    ``` bash
    # [a]uto-compress the archive based on its file extension
    tar -acf writing.zip writing/

    # FYI, you may also see
    tar -a -cf writing.zip writing/

    # FYI, linux servers frequently use g[z]ip
    tar -z -cf writing.tgz writing/
    ```

3.  Extract your archive

    ``` bash
    mv writing writing_backup

    # e[x]tract the archive to get the original files back
    tar -xf writing.zip

    # Compare the old and restored directories
    ls writing
    ls writing_backup
    ```

4.  There are many useful utilities:
    <https://www.gnu.org/software/coreutils/manual/coreutils.html>

## Operations with multiple files and directories

1.  Copy with multiple file names

    ``` bash
    cd ~/Desktop/shell-lesson-data/exercise-data/

    cp creatures/minotaur.dat creatures/unicorn.dat creatures_backup/
    ```

2.  Copy using globs (\"globals\") You can match a single character with
    ? or unlimited characters with \*. This is an example of *shell
    expansion*.

    ``` bash
    mkdir proteins_backup

    # The shell expands *.pdb into the list of all matching files, then does `cp`
    cp proteins/*.pdb proteins_backup/
    ```

# Pipes and filters

The \"Unix Philosophy\" is to combine many small tools that do one job
into a processing pipeline.

## Motivating example with `wc`

FYI, .pdb is Protein Data Bank format

1.  Count words in a file using `wc`

    ``` bash
    cd ~/Desktop/shell-lesson-data/exercise-data/proteins/
    ls

    # Inspect cubane.pdb
    cat cubane.pdb

    # [w]ord [c]ount for cubane.pdb
    wc cubane.pdb
    ```

2.  Run `wc` for all files

    ``` bash
    # Run the command with default options
    wc *.pdb


    wc -l *.pdb # lines
    wc -c *.pdb # characters
    wc -w *.pdb # words
    ```

## Capturing output from commands

``` bash
# Redirect output to file
wc -l *.pdb > lengths.txt
ls lengths.txt
cat lengths.txt       # Inspect contents
head -n 1 lengths.txt # Inspect 1st line
less lengths.txt      # Inspect with pager
```

## Filtering output

1.  The `sort` command run the file input through a filter and returns
    the filtered result.

    ``` bash
    sort lengths.txt    # alphanumeric sort (i.e. text)
    sort -n lengths.txt # numeric sort
    ```

2.  Send filtered output to new file

    ``` bash
    sort -n lengths.txt > sorted_lengths.txt
    cat sorted_lengths.txt
    ```

3.  (Optional) Append to the end of a file using `>>`

    ``` bash
    cd ~/Desktop/shell-lesson-data/exercise-data/animal-counts/

    # Create new file
    head -n 3 animals.csv > animals-subset.csv

    # Append to that file
    tail -n 2 animals.csv >> animals-subset.csv
    ```

## Passing output to another command

Pipe output from one command directly into a second command without
creating an intermediate file. This is the cornerstone of Unix
workflows.

``` bash
sort -n lengths.txt |  head -n 1
```

## Combining multiple commands

Daisy-chain your commands together. As long as the output of command X
is a legitimate input for command Y, it will work.

``` bash
# Return to the beginning
wc -l *.pdb | sort -n

# Add additional commands
wc -l *.pdb | sort -n | head -n 1
```

## History and pipes

1.  The terminal saves your command history (typically 500 or 1000
    commands)

    -   You can see previous commands using the up/down arrows
    -   You can edit the command that\'s currently visible and run it

2.  Once your command history gets big, you might want to search it:

    ``` bash
    history           # or history -1000 in zsh on Mac
    history | grep ls # pipe the output of history into search
    ```

# Shell scripts

We should save this stuff and reuse it.

## Creating and running a script

1.  Create a new script

    ``` bash
    cd proteins
    nano middle.sh
    ```

2.  Edit the script file and save

    ``` bash
    # Get lines 11-15
    head -n 15 octane.pdb | tail -n 5
    ```

3.  Execute the script

    ``` bash
    bash middle.sh
    ```

## Generalize your script

1.  Use a special variable to run the script on any file (`$1` returns
    the value of a variable; `""` ensures that it works if there are
    spaces.)

    ``` bash
    nano middle.sh
    ```

    ``` bash
    # Use the 1st argument as your input.
    head -n 15 "$1" | tail -n 5
    ```

    ``` bash
    bash middle.sh octane.pdb
    bash middle.sh pentane.pdb
    ```

2.  Use additional ordered arguments

    ``` bash
    nano middle.sh
    ```

    ``` bash
    # Select lines from the middle of a file.
    # Usage: bash middle.sh filename end_line num_lines
    head -n "$2" "$1" | tail -n "$3"
    ```

    ``` bash
    bash middle.sh pentane.pdb 15 5
    ```

3.  Use unlimited arguments

    ``` bash
    nano sorted.sh
    ```

    ``` bash
    # Sort files by their length.
    # Usage: bash sorted.sh one_or_more_filenames
    wc -l "$@" | sort -n
    ```

    ``` bash
    bash sorted.sh *.pdb ../creatures/*.dat
    ```

## (Optional) Text processing with Unix tools

``` bash
cd ~/Desktop/shell-lesson-data/exercise-data/animal-counts/

# Get the second column of the CSV
cut -d , -f 2 animals.csv

# Get the unique values
cut -d , -f 2 animals.csv | uniq

# Sort them
cut -d , -f 2 animals.csv | uniq
```

# Loops

Don\'t repeat yourself.

## A basic loop

``` bash
cd ~/Desktop/shell-lesson-data/exercise-data/creatures/
nano latin.sh
```

``` bash
for filename in basilisk.dat minotaur.dat unicorn.dat
do
    # Extract second line of file
    head -n 2 $filename | tail -n 1
done
```

``` bash
bash latin.sh
```

## Simplify your loop with globs

``` bash
nano latin.sh
```

``` bash
for filename in *.dat
do
    # Extract second line of file
    head -n 2 $filename | tail -n 1
done
```

``` bash
bash latin.sh
```

## Generalize your loop with unlimited arguments

1.  Create a separate directory for your scripts so that you can find
    them

    ``` bash
    cd ~/Desktop/shell-lesson-data/exercise-data/
    mkdir scripts
    cd scripts
    nano aggregate.sh
    ```

2.  Write a script that takes arbitrary arguments

    ``` bash
    for filename in "$@"
    do
        echo $filename
    done
    ```

3.  Run the script against the contents of a different directory

    ``` bash
    bash aggregate.sh ../proteins/*.pdb
    ```

4.  Do work in the script

    ``` bash
    nano aggregate.sh
    ```

    ``` bash
    for filename in "$@"
    do
        echo $filename
        cat $filename >> alkanes.pdb
    done
    ```

    ``` bash
    bash aggregate.sh ../proteins/*.pdb
    ```

## Make your script executable

``` bash
# List file in long format to show current permissions
ls -l aggregate.sh

# Change file mode (i.e. permissions)
# User can read/write/execute, Group and Other can read
chmod u=rwx,go=r aggregate.sh

# Show changed permissions
ls -l aggregate.sh

# Invoke script
./aggregate.sh ../proteins/*.pdb
```

# Finding things

## Find

### Find everything

``` bash
cd ~/Desktop/shell-lesson-data/exercise-data/
find .
```

### Find by type

``` bash
# List all directories
find . -type d

# List all files
find . -type f
```

### Find files

``` bash
# Do shell expansion, then run command
find . -name *.txt

# Prevent shell expansion and match wildcard
find . -name "*.txt"
```

## Grep

TBD

# Shell extras

Consult the Wooledge Bash Guide (see references below) for more on these
topics:

1.  SSH
2.  Permissions
3.  Job control
4.  Aliases and bash customization
5.  Shell variables
6.  Mini-languages (grep, sed, AWK)
7.  Shell expansion
8.  Conditional tests

# Credits

1.  The Unix Shell: <https://swcarpentry.github.io/shell-novice/>

# References

1.  Instructor notes for \"The Unix Shell\":
    <https://swcarpentry.github.io/shell-novice/guide/>
2.  A list of command line utilities: <https://ss64.com/bash/>
3.  GNU core utilities:
    <https://www.gnu.org/software/coreutils/manual/coreutils.html>
4.  Bash guide: <https://mywiki.wooledge.org/BashGuide>
5.  Shell redirection operators(1):
    <https://www.redhat.com/sysadmin/linux-shell-redirection-pipelining>
6.  Shell redirection operators (2):
    <https://www.gnu.org/software/bash/manual/html_node/Redirections.html>

# Data Sources

1.  Lesson data:
    <http://swcarpentry.github.io/shell-novice/data/shell-lesson-data.zip>
