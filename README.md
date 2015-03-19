York Thesis Class in LyX
========================

This is an example repository used for building thesis (Masters or PhD) in LyX.

LyX, like LaTeX, is a document preperation system built around the concept of defining the
*structure* of your document. For larger documents, such as a dissertation, this is
incredibly useful because the document is much easier to keep internally consistent
(e.g., figure and table labels will always be correct, even if you add or remove others 
at a later time). E.g., see 
[this blog post](https://amrys.wordpress.com/2013/01/16/why-your-should-latex-your-dissertation-or-why-you-dont-have-to-write-your-dissertation-in-word/) for a discussion. 

As well, it's very easy to turn a thesis written in LyX into publised articles, 
because the labels will always be constently labelled. Hence, you could create a 
new `apa6` manuscript file in LyX to copy-and-paste your way 
towards your next publication. It really is that simple.

Installation
------------------------

To use this package you'll need to meet the following requirements:

### Requirements: 

- Install [LyX](http://www.lyx.org/), and (optionally) install the version
  of Jabref that comes with it
- Install [R](http://www.r-project.org/) and the `'knitr'` package 
- (Mac and Linux) Install the `york-thesis` class (if it wasn't shipped with
  the TeX manager in step 1) through TeX-live or whatever system you are using

As well, if you want to go the extra mile (and you should!)

- Obtain a decent `.bib` manager. You could just use
  a text editor but a dedicated `.bib` manager is much nicer. 
- If you installed [Jabref](http://jabref.sourceforge.net/) when installing LyX, 
  it has support to push references directly to LyX, and is overall a good bib manager

### Configure:

- Move the `'york-thesis.layout'` file in the `extra/` directory 
   to LyX's `~/layouts` directory 
     - On Ubuntu mine was located in `~/home/phil/.lyx/layouts`
     - Windows is probably in `C:/Program Files/LyX/layouts`
     - Mac is in the application itself (right click on `LyX.app` and go to
       `"show package contents"`, then inside that `Contents\Resources\layouts`)
- Open the LyX program and go to `'Tools -> Reconfigure'`. Now restart LyX.

Finally, pat yourself on the back because it should work now LyX! You can open `.lyx` files 
directly, or open them with `'File -> Open'` if you open LyX first


Extra
-----------------------

It might be a good idea to set up a keyboard shortcut or three for compiling the master file directly.
By default, LyX does not have an 'update master file' keyboard shortcut, though it does have a 
compile master file option (`Document -> View Master Documentation`), which for me was `Ctrl+Alt+R`. 

To add an update shortcut (so that your opened pdf stays on the same page after recompiled) use the 
following:

- Got to `Tools -> Preferences -> Editing -> Shortcuts`, and click `New`
- Give the command the name `master-buffer-update`, and a nice keyboard shortcut. 
  I gave it `Ctrl+Alt+Shift+R`. Click okay to finish.


