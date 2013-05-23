Misspell Fixer
==============

Utility to fix common misspellings in source codes.

### Synopsis
    
    misspell_fixer	[OPTION] ...target directories...

### Options

* `-d` Debug mode: shows the core logics all steps
* `-v` Verbose mode: shows the iterated files
* `-r` Real run mode: Overwrites the original files with the fixed one. Without this option the originals will be untouched.
* `-f` Fast mode: Faster mode with limited options. (`-v`, `-s` options are not supported) Works only with real run mode `-r`. This mode cannot make backups. (`-n` is also needed)
* `-s` Shows diffs of changes.
* `-i` Walk through source code management systems internal directories. (don't ignore `*.svn*`, `*.git*`)
* `-n` Disabling backups. (By default the modified files originals will be saved with the `.$$.BAK` suffix.)
* `-u` Enabling less safe rules. (Manual revise's need will be more probable.)
* `-h` Help. Displays this page.

### Sample usages

By default nothing import will happen

    $ misspell_fixer.sh targetdir

What you can track with -v

    $ misspell_fixer.sh -v targetdir

A real usage:

    $ misspell_fixer.sh -r -v targetdir

Show only the diff, don't modify the files:

    $ misspell_fixer.sh -s -v targetdir

Show everything and fix the files:

    $ misspell_fixer.sh -r -s -v targetdir

Fast mode example:

    $ misspell_fixer/misspell_fixer.sh -r -f -n .

It is based on the following common misspellings sources:

* http://www.how-do-you-spell.com/
* http://en.wikipedia.org/wiki/Commonly_misspelled_words
* http://www.wrongspelled.com/

### Dependencies

* bash
* find
* sed
* diff

### Author

Veres Lajos

### Original source

https://github.com/vlajos/misspell_fixer

Feel free to use!
