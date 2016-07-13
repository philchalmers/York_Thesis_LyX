York Thesis Class in LyX
========================

This is an example repository used for building thesis (Masters or PhD) in LyX, derived from the instructions located on the 
[technical requirements](http://gradstudies.yorku.ca/current-students/thesis-dissertation/organization/#section3c) page. 
When compiled, the bare-bones of this thesis template will look [like this](https://github.com/philchalmers/York_Thesis_LyX/blob/master/york-thesis.pdf), which gives you a general outline of 
how to start writting your thesis or disseration.  

LyX, like LaTeX, is a document preparation system built around the concept of defining the
*structure* of your document. For larger documents, such as a dissertation, this is
incredibly useful because the document is much easier to keep internally consistent
(e.g., figure and table labels will always be correct, even if you add or remove others 
at a later time). E.g., see 
[this blog post](https://amrys.wordpress.com/2013/01/16/why-your-should-latex-your-dissertation-or-why-you-dont-have-to-write-your-dissertation-in-word/) for a discussion. 

As well, it's very easy to turn a thesis written in LyX into published articles 
because the labels will always be consistent in new documents. Hence, you could create a 
new `apa6` manuscript file in LyX to copy-and-paste your way 
towards your next manuscript and publication. It really is that simple.

If you need some material to help understand the fundamentals of LyX, here are a few sources:

- [Visual Tour](http://www.lyx.org/VisualTour) from the main LyX website
- [Some fundamental elements](http://ocw.mit.edu/courses/nuclear-engineering/22-033-nuclear-systems-design-project-fall-2011/tools/MIT22_033F11_tools_lyx_tut.pdf) in pdf form
- [5-part YouTube video](https://www.youtube.com/watch?v=m4cEAVmLegg) primarily focused 
  on making math in LyX (if you know any LaTeX math commands, you are *way* ahead of the game here because typing
  math in LyX with a LaTeX flavor will make you extremely efficient)

Installation
========================

To use this template you'll need to meet the following requirements:

### Requirements: 

- Install the [LyX](http://www.lyx.org/) program for your OS 
- Install the `york-thesis` class through whatever TeX system you are using 
  (e.g., TeX-Live, MiKTeX, MacTeX)
- Follow the configuration instructions below

As well, if you want to go the extra mile (and you should!)

- Obtain a decent bibliography manager to edit `.bib` files. You could just use
  a text editor but a dedicated `.bib` manager is much nicer. If you installed
  [Jabref](http://jabref.sourceforge.net/) when installing LyX, 
  it has support to push references directly to LyX, and is overall a good reference manager
- Install [R](http://www.r-project.org/) and the `'knitr'` package. This
  is only required if you want to integrate LyX with R to evaluate R code within
  your document

### Configuration:

- Move the `'york-thesis.layout'` file in the `LyX_files/` directory 
   to LyX's `~/layouts` directory 
     - On Ubuntu, mine was located in `~/home/phil/.lyx/layouts`
     - Windows is probably in `C:/Program Files/LyX/layouts`
     - Mac is in the application itself (right click on `LyX.app` and go to
       `"show package contents"`, then inside that `Contents\Resources\layouts`)
- Open the LyX program and go to `'Tools -> Reconfigure'`. Now restart LyX.

Finally, pat yourself on the back because it should work now LyX! You can open `.lyx` files 
directly, or open them with `'File -> Open'` if you open LyX first.

How To Use LyX
========================

The way to understand how LyX (and LaTeX) behave is to think of files, figures, references, 
etc, as objects being 'pointed to' within some LyX file. A LyX file points to a figure, and this is 
included when the document is compiled to a PDF. Any external changes to said file will be included in 
the document the next time it is compiled; this has huge benefits when things have to be edited at a 
later time (unlike document systems like MS Word, in which if a figure has to be changed it has to be changed
in the document itself.....which can have horrible repercussions and overall is quite cumbersome). This same
philosophy works for references, chapters, appendices, etc, and helps to keep different document elements 
isolated and manageable.

The design of the LyX files for this York Thesis template is fairly simply: 

- There is one master file, `york-thesis.lyx`, which points to independent files (styles,
  front-matter, chapters, etc). This is the main file which links all the material together, and 
  essentially declares the structure of the final product.
- Chapters go into their own separate files in the main directory, and are included in the master 
  file as 'Children' using the LyX insert commands.
- Front-matter material has been put into the `front/` directory, containing LyX and LaTeX files.
  Edit these as you see fit. The only LaTeX file that you should edit directly (with a standard text
  editor) is the `preamble.tex` file, which contains information about your degree, committee, defense date, etc.
- Extra material, such as customized figures, tables, appendices, etc, go into other directories and are inserted
  with LyX `Input` methods. This goes for the bibliography as well, which is included in a `bibliography/`
  directory by default.

Finally, to compile the LyX file to a PDF, click on `Document -> View Master Document`, or use a suitable
keyboard shortcut (e.g., `Ctrl + Shift + R`). 

Additionally, some stylistic things to help keep you organized and efficient:

- In LyX, turn on things like continuous spell-checking and word completion. These are off by default.
- *Frequently label sections, tables, figures, etc, with meaningful labels*. 
  This will help you reference content later on, and are dynamically updated as you add more material. 
  Create a label with `Insert -> Label`, and reference any label with `Insert -> Cross-Reference`
- *Use external PDF's files for figures*. PDFs are extremely high quality (vector graphics), and look 
  the best in the final product.
- *Break additional content up into folders*. If it turns out you have lots of figures and tables, 
  you may want to break these up by chapter. So instead of putting all figures into `figures/`, 
  create new directories such as `figures/chapter-1/`, `figures/chapter-2/`, and so on, and put files in there.
- *Use BibTeX to manage your references*. If you need tools to convert your previous references into something more
  suitable, [here is a good start](http://www.snowelm.com/~t/doc/tips/makebib.en.html)

Extra
-----------------------

When compling the document to a pdf, if you are do not have the master file active (e.g., you currently have Chapter 3 active) then using `Ctrl + r` will not compile the entire document. Instead, use `Ctrl + Alt + r`, which for Linux and Windows is the *compile master document* keyboard hotkey. Note that this can be used to update the pdf file if it is already open, so use it as often as you like.


