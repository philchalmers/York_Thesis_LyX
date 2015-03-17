York Thesis Class in LyX
========================

This is an example repository used for building thesis (Masters or PhD) in LyX.

Installation
------------------------

To use this package you'll need to meet the following requirements:

### Requirements: 

1) Install [LyX](http://www.lyx.org/), and (optionally) install the version
   of Jabref that comes with it
2) Install [R](http://www.r-project.org/) and the `'knitr'` package 
3) (Mac and Linux) Install the `york-thesis` class (if it wasn't shipped with
   the TeX manager in step 1) through TeX-live or whatever system you are using
4) (Optional) Obtain a decent `.bib` manager. You could just use
   a text editor but a dedicated .bib manager is much nicer. If you chose to
   install Jabref when installing LyX, it has support to push references 
   directly to LyX, and is overall a good bib manager

### Configure:

1) Move the `'york-thesis.layout'` file in the `Extra/` directory 
   to LyX's `~/layouts` directory (On Ubuntu mine was located in 
   `~/home/phil/.lyx/layouts`; Windows is probably in
   `C:/Program Files/LyX/layouts`; and Mac is in the application itself 
   (right click on `LyX.app` and go `"show package contents"`, then inside that
   `Contents\Resources\layouts`)
2) Open the LyX program and go to `'Tools -> Reconfigure'`. Restart LyX.
3) Pat yourself on the back because it should work now LyX! You can open 
   `.lyx` files directly, or open them with 'File -> Open' if you open LyX first


Extra
-----------------------

It might be a good idea to set up a keyboard shortcut or two for compiling the master file directly.
By default, LyX does not have an 'update master file' keyboard shortcut, though it does have a 
compile master file option (Document -> View Master Documentation), which for me was `Ctrl+Alt+R`. To 
add an update shortcut (so that your opened pdf stays on the same page after recompiled) use the 
following:

- Got to `Tools -> Preferences -> Editing -> Shortcuts`, and click 'New'
- Give the command the name 'master-buffer-update', and a nice keyboard shortcut. 
  I gave it `Ctrl+Alt+Shift+R`. Click okay to finish.


