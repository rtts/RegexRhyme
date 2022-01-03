RegexRhyme
===========

*Find words in the [Dutch wordlist from OpenTaal](https://github.com/OpenTaal/opentaal-wordlist)
that end with a given regular expression.*

This repository contains the deceptively simple Bash one-liner that I
use every year to write my Sinterklaasgedichten. It works on Windows,
macOS, and GNU/Linux.

How to use
----------

Just drop the files from this repository anywhere in your `PATH` and
you will be able to use the `rr` command. Here are some examples:

    rr aas               # words that rhyme with Sinterklaas
    rr [^o]ol            # words that rhyme with oliebol
    rr '(o|eau)'         # words that rhyme with kado/cadeau
    rr '[^o](ei|ij)[td]' # words that rhyme with bloementapijt

By default the output will be piped to `less` for easy viewing, but
feel free to redirect anywhere else. For example, this is how to
redirect the output to the clipboard:

    rr aas | clip.exe    # Windows
    rr aas | pbcopy      # macOS
    rr aas | xclip       # GNU/Linux
