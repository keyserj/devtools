
# Intro

Here are a few features that are useful in most dev workflows. Disclaimers:

-   Even the most commonly-used features are included here, so you may know of them already
-   Most of these features are shown using specific tools (e.g. VSCode, zsh plugins), but usually there are multiple tools that can provide the same feature - use what you like best

# IDE features

Tools specifically for working with a codebase

## Code navigation

### Fuzzy file search

Quickly search for files in a repository

-   use any characters from the file name (spaces => order doesn't matter)
-   filter by file extension

### File text search

Search for specific text in a repository

-   only include/exclude specific files/folders to search
-   regex text search (see what regex can do  [here](https://regex101.com/)!)
-   decent alternatives in terminal: ag/ripgrep

### Go to Definition/IntelliSense

Common set of features for understanding definitions:

-   Navigate to a definition from its use
-   Display info about the definition in the editor without jumping to it
-   Autocomplete based on definitions

Example families of tools:

-   Language server (e.g. VSCode  [Ruby](https://marketplace.visualstudio.com/items?itemName=rebornix.Ruby)  or  [Solargraph](https://marketplace.visualstudio.com/items?itemName=castwide.solargraph)  extensions)
    -   Awesome when it works, but only has partial support for Rails, so it doesn't work about ~half the time
-   Ctags ([ripper-tags](https://github.com/tmm1/ripper-tags)) seem to fill in most of the go-to language server gaps, but requires maintaining `tags` files
    -   Doesn't support intellisense or autocompletion
-   RubyMine: Does lots of things, but you have to use an IDE
-   Can just fall back to text search

## Git

VSCode's  [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)  provides all of these features

### Gutter git blame

Always display commit details for current line

### Open commit

See commit details to better understand the context for a change

-   commit message
-   all files changed in commit
-   linked to PR & Jira ticket
-   option to open commit/PR in browser

### Open file in browser

Opens file in GitHub, good for providing specific context for discussion

-   "y" from GitHub to get a commit link instead of branch link (branches can change, so line #'s can become out-of-date)

### Blame annotations

See all blame for a file; good for finding file SMEs, getting overview of file history by line

-   Open blame prior to this change
    -   Little buggy after jumping back more than once

### Line, File, Branch commit history

Click through the change history for a line, file, or branch

### Staged/unstaged management

-   View staged/unstaged changes
-   Diff minimap
-   Stage/unstage specific lines within a file

## Other

### Scratchpads

Being able to create temporary files very quickly is pretty useful.

Visual Studio Code extension [here](https://marketplace.visualstudio.com/items?itemName=buenon.scratchpads).

### UI interactive debugging

View all variables in scope, add breakpoints on the fly, code eval line by line

Pry is enough to get by, but this would be really helpful for quickly learning how unfamiliar parts of an app work.

# Terminal features

Features specifically for working with a terminal

Notes

-   these examples all use the  [zsh](https://zsh.sourceforge.io/)  shell. word on the street is the  [fish](https://fishshell.com/)  shell comes with a lot of these features out of the box! though it isn't POSIX compatible
-   [antigen](https://github.com/zsh-users/antigen)  is a useful plugin manager that makes it easy to install/manage zsh plugins

## Shell prompt

Customize your terminal prompt to show useful info

-   current directory
-   current branch
-   number of unstaged/staged files
-   current time & duration to execute command
-   many plugins that provide this,  [powerlevel10k](https://github.com/romkatv/powerlevel10k)  is one example for zsh,  [hydro](https://github.com/jorgebucaran/hydro)  for fish

## Syntax highlighting

Green = valid command Red = invalid command

-   also some other colorings e.g. yellow = quoted string
-   provided by the  [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)  plugin

## Autocomplete/search preview

Uses terminal history to display a muted preview; autocomplete with →/end

-   provided by the  [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)  plugin
-   may be an alternative for using aliases

## History search

Search through commands that you've run in your terminal

-   ctrl-r searches terminal history for the currently-typed text (useful over ssh where fzf isn't installed)
-   [fzf](https://github.com/junegunn/fzf)  provides a convenient interface and fuzzy-searching
-   [zsh-history-substring-search](https://github.com/zsh-users/zsh-history-substring-search)  provides searching by substring via up key

## Frecent directory navigation

Track directories you've been to, and jump to the most recent/frequent one that matches your search

-   provided by the  [zsh-z](https://github.com/agkozak/zsh-z)  plugin
    -   there are ports for bash/fish
