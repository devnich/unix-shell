- <a href="#introducing-the-shell" id="toc-introducing-the-shell"><span class="toc-section-number">1</span> Introducing the shell</a>
  - <a href="#reasons-to-use-the-shell" id="toc-reasons-to-use-the-shell"><span class="toc-section-number">1.1</span> Reasons to use the shell</a>
  - <a href="#unix" id="toc-unix"><span class="toc-section-number">1.2</span> "Unix"</a>
  - <a href="#shell" id="toc-shell"><span class="toc-section-number">1.3</span> "Shell"</a>
  - <a href="#the-past-is-always-with-us" id="toc-the-past-is-always-with-us"><span class="toc-section-number">1.4</span> The past is always with us</a>
- <a href="#navigating-files-and-directories" id="toc-navigating-files-and-directories"><span class="toc-section-number">2</span> Navigating files and directories</a>
  - <a href="#file-system-layout" id="toc-file-system-layout"><span class="toc-section-number">2.1</span> File system layout</a>
  - <a href="#who-are-you" id="toc-who-are-you"><span class="toc-section-number">2.2</span> Who are you?</a>
  - <a href="#where-are-you" id="toc-where-are-you"><span class="toc-section-number">2.3</span> Where are you?</a>
  - <a href="#whats-in-this-directory" id="toc-whats-in-this-directory"><span class="toc-section-number">2.4</span> What's in this directory?</a>
  - <a href="#getting-help" id="toc-getting-help"><span class="toc-section-number">2.5</span> Getting help</a>
  - <a href="#exploring-other-directories" id="toc-exploring-other-directories"><span class="toc-section-number">2.6</span> Exploring other directories</a>
  - <a href="#relative-vs.-absolute-paths" id="toc-relative-vs.-absolute-paths"><span class="toc-section-number">2.7</span> Relative vs. absolute paths</a>
- <a href="#working-with-files-and-directories" id="toc-working-with-files-and-directories"><span class="toc-section-number">3</span> Working with files and directories</a>
  - <a href="#creating-directories" id="toc-creating-directories"><span class="toc-section-number">3.1</span> Creating directories</a>
  - <a href="#moving-files-and-directories" id="toc-moving-files-and-directories"><span class="toc-section-number">3.2</span> Moving files and directories</a>
  - <a href="#copying-files-and-directories" id="toc-copying-files-and-directories"><span class="toc-section-number">3.3</span> Copying files and directories</a>
  - <a href="#removing-files-and-directories" id="toc-removing-files-and-directories"><span class="toc-section-number">3.4</span> Removing files and directories</a>
  - <a href="#create-a-backup-archive" id="toc-create-a-backup-archive"><span class="toc-section-number">3.5</span> Create a backup archive</a>
  - <a href="#operations-with-multiple-files-and-directories" id="toc-operations-with-multiple-files-and-directories"><span class="toc-section-number">3.6</span> Operations with multiple files and directories</a>
- <a href="#pipes-and-filters" id="toc-pipes-and-filters"><span class="toc-section-number">4</span> Pipes and filters</a>
  - <a href="#motivating-example-with-wc" id="toc-motivating-example-with-wc"><span class="toc-section-number">4.1</span> Motivating example with <code>wc</code></a>
  - <a href="#capturing-output-from-commands" id="toc-capturing-output-from-commands"><span class="toc-section-number">4.2</span> Capturing output from commands</a>
  - <a href="#filtering-output" id="toc-filtering-output"><span class="toc-section-number">4.3</span> Filtering output</a>
  - <a href="#passing-output-to-another-command" id="toc-passing-output-to-another-command"><span class="toc-section-number">4.4</span> Passing output to another command</a>
  - <a href="#combining-multiple-commands" id="toc-combining-multiple-commands"><span class="toc-section-number">4.5</span> Combining multiple commands</a>
  - <a href="#history-and-pipes" id="toc-history-and-pipes"><span class="toc-section-number">4.6</span> History and pipes</a>
- <a href="#shell-scripts" id="toc-shell-scripts"><span class="toc-section-number">5</span> Shell scripts</a>
  - <a href="#creating-and-running-a-script" id="toc-creating-and-running-a-script"><span class="toc-section-number">5.1</span> Creating and running a script</a>
  - <a href="#generalize-your-script" id="toc-generalize-your-script"><span class="toc-section-number">5.2</span> Generalize your script</a>
  - <a href="#optional-text-processing-with-unix-tools" id="toc-optional-text-processing-with-unix-tools"><span class="toc-section-number">5.3</span> (Optional) Text processing with Unix tools</a>
  - <a href="#optional-language-interpreters-are-also-shell-commands" id="toc-optional-language-interpreters-are-also-shell-commands"><span class="toc-section-number">5.4</span> (Optional) Language interpreters are also shell commands</a>
- <a href="#loops" id="toc-loops"><span class="toc-section-number">6</span> Loops</a>
  - <a href="#a-basic-loop" id="toc-a-basic-loop"><span class="toc-section-number">6.1</span> A basic loop</a>
  - <a href="#simplify-your-loop-with-globs" id="toc-simplify-your-loop-with-globs"><span class="toc-section-number">6.2</span> Simplify your loop with globs</a>
  - <a href="#generalize-your-loop-with-unlimited-arguments" id="toc-generalize-your-loop-with-unlimited-arguments"><span class="toc-section-number">6.3</span> Generalize your loop with unlimited arguments</a>
  - <a href="#make-your-script-executable" id="toc-make-your-script-executable"><span class="toc-section-number">6.4</span> Make your script executable</a>
- <a href="#finding-things" id="toc-finding-things"><span class="toc-section-number">7</span> Finding things</a>
  - <a href="#find" id="toc-find"><span class="toc-section-number">7.1</span> Find</a>
  - <a href="#grep" id="toc-grep"><span class="toc-section-number">7.2</span> Grep</a>
- <a href="#shell-extras" id="toc-shell-extras"><span class="toc-section-number">8</span> Shell extras</a>
- <a href="#credits" id="toc-credits"><span class="toc-section-number">9</span> Credits</a>
- <a href="#references" id="toc-references"><span class="toc-section-number">10</span> References</a>
- <a href="#data-sources" id="toc-data-sources"><span class="toc-section-number">11</span> Data Sources</a>

# Introducing the shell

## Reasons to use the shell

1.  Automate basic tasks
2.  Underlies many other open source languages and applications and can be used to glue them together
3.  Essential for system administration, remote computing, and high-performance computing
4.  Many concise special-purpose tools that can make your life easier
5.  Complements more fully-featured application programming languages

## "Unix"

Powerpoint slides: Unix family tree

1.  Unix-like operation systems share a common architecture and layout
2.  Roughly compatible, with similar (or identical) shells and tools
3.  The environment in which most open-source software was written

## "Shell"

- Broadly speaking, there is a tension between making computer systems fast and making them easy to use.
- A common solution is to create a 2-layer architecture: A fast, somewhat opaque core surrounded by a more friendly scriptable interface (also referred to as "hooks" or an "API"). Examples of this include video games, Emacs and other highly customizable code editors, and high-level special-purpose languages like Stata and Mathematica.
- Unix shell is the scriptable **shell** around the operating system. It provides a simple interface for making the operating system do work, without having to know exactly how it accomplishes that work.

## The past is always with us

The design and terminology of modern computers is based on metaphors from a previous age.

1.  Files and folders
2.  Teletype input and output
3.  Modern touch devices don't expose the file system, so you may be less comfortable with navigating directory trees than people whose primary computing devices were desktop computers

# Navigating files and directories

## File system layout

Powerpoint slides: "Navigating files and directories"

## Who are you?

``` bash
whoami
```

## Where are you?

1.  Current working directory

    ``` bash
    pwd                             # Print Working Directory
    ```

2.  By default, this is probably your home directory (discuss how to view this in Finder or File Explorer)

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

## What's in this directory?

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

- You can navigate through the man page using the space bar and arrow keys
- Quit man with "q"
- Online references are available for Windows users who don't have man pages: <https://linux.die.net/>

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

3.  Now that you're "in" a new location, the context for your commands is different

    ``` bash
    pwd
    ls -F

    # This produces an error because the folder is in a different location
    # relative to the working directory
    cd shell-lesson-data
    ```

4.  Move up the directory tree `.` is shorthand for "current directory"; `..` is shorthand for "parent directory"

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

## Relative vs. absolute paths

1.  An absolute path specifies a location from the root of the file system.
2.  A relative path specifies a location starting from the current location.

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

3.  Create a text file. Note that everything is available through the file browser and the terminal.

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

Deletion is forever. Consider making a backup archive as part of your workflow.

1.  Create an archive with `tar` ("tape archive").

    ``` bash
    cd ~/Desktop/shell-lesson-data/exercise-data/

    # [c]reate a new archive with the given [f]ilename
    tar -cf writing.tar writing/
    ```

2.  Create a compressed (zipped) archive.

    ``` bash
    # [a]uto-compress the archive based on its file extension
    tar -acf writing.zip writing/

    # FYI, you may also see
    tar -a -cf writing.zip writing/

    # FYI, linux servers frequently use g[z]ip
    tar -z -cf writing.tgz writing/
    ```

    `tar` is an old utility and can be finicky about the order of flags.

3.  Extract your archive

    ``` bash
    mv writing writing_backup

    # e[x]tract the archive to get the original files back
    tar -xf writing.zip

    # Compare the old and restored directories
    ls writing
    ls writing_backup
    ```

4.  There are many useful utilities: <https://www.gnu.org/software/coreutils/manual/coreutils.html>

## Operations with multiple files and directories

1.  Copy with multiple file names

    ``` bash
    cd ~/Desktop/shell-lesson-data/exercise-data/

    cp creatures/minotaur.dat creatures/unicorn.dat creatures_backup/
    ```

2.  Copy using globs ("globals") You can match a single character with ? or unlimited characters with \*. This is an example of *shell expansion*.

    ``` bash
    mkdir proteins_backup

    # The shell expands *.pdb into the list of all matching files, then does `cp`
    cp proteins/*.pdb proteins_backup/
    ```

# Pipes and filters

The "Unix Philosophy" is to combine many small tools that do one job into a processing pipeline.

## Motivating example with `wc`

FYI, `.pdb` is the Protein Data Bank format

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

1.  The `sort` command runs the file input through a filter and returns the filtered result.

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

Pipe output from one command directly into a second command without creating an intermediate file. This is the cornerstone of Unix workflows.

``` bash
sort -n lengths.txt |  head -n 1
```

## Combining multiple commands

Daisy-chain your commands together. As long as the output of command X is a legitimate input for command Y, it will work.

``` bash
# Return to the beginning
wc -l *.pdb | sort -n

# Add additional commands
wc -l *.pdb | sort -n | head -n 1
```

## History and pipes

1.  The terminal saves your command history (typically 500 or 1000 commands)

    - You can see previous commands using the up/down arrows
    - You can edit the command that's currently visible and run it

2.  Once your command history gets big, you might want to search it:

    ``` bash
    history           # or `history -1000` in zsh on Mac
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

1.  Use a special variable to run the script on any file (`$1` returns the value of a variable; `""` ensures that it works if there are spaces.)

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

# Sort the values
cut -d , -f 2 animals.csv | sort

# Get unique values (`uniq` requires values to be adjacent to one another)
cut -d , -f 2 animals.csv | sort | uniq
```

## (Optional) Language interpreters are also shell commands

``` bash
# 1. Run a python script that produces a .csv as output
# 2. Extract the 2nd column of that .csv and get the unique values
python script.py | cut -d , -f 2 | sort | uniq
```

# Loops

Don't repeat yourself.

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

1.  Create a separate directory for your scripts so that you can find them

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

Grep is a powerful tool for matching text patterns by using *regular expressions*. You can find introductory documentation for regular expressions in the References section.

# Shell extras

Consult the Wooledge Bash Guide (see references below) for more on these topics:

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

1.  A list of command line utilities: <https://ss64.com/bash/>
2.  GNU core utilities: <https://www.gnu.org/software/coreutils/manual/coreutils.html>
3.  Bash guide: <https://mywiki.wooledge.org/BashGuide>
4.  Shell redirection operators(1): <https://www.redhat.com/sysadmin/linux-shell-redirection-pipelining>
5.  Shell redirection operators (2): <https://www.gnu.org/software/bash/manual/html_node/Redirections.html>
6.  Grep regular expressions: <https://www.gnu.org/software/grep/manual/html_node/Regular-Expressions.html>
7.  Using zsh on MacOS: <https://scriptingosx.com/2019/06/moving-to-zsh/>

# Data Sources

1.  Lesson data: <http://swcarpentry.github.io/shell-novice/data/shell-lesson-data.zip>
