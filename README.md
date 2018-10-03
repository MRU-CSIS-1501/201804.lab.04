# Lab-04

## WHAT WE'RE DOING

Time to up your game in Emacs!

Your instructor will show you some useful features of Emacs - feel free to follow along.

There will also be a number of tweaks you can make to your .emacs file written below that you might find useful.

---

## SOME USEFUL .emacs MODS

To do any of these, you need to edit the `.emacs` file that is in your home directory - add the lines shown to the bottom of the file and then save your work and exit from Emacs. From that point onward, Emacs will use your mods!

### LINE NUMBERS

If you want to see line numbers in your display:

<pre>
; add line numbers to display
(global-linum-mode 1)
(setq linum-format "%d ")
</pre>

_That "%d " in the last line should look familiar...I wonder if you could tweak it?...._

### 80 COLUMN RULE

Keeping your line length within 80 characters is considered by many to be a great rule of thumb (I'm not making this up - look it up).

Here's something you can use to color-code lines that go past that point:

<pre>
;; turn on whitespace mode and 80 column marking
(require 'whitespace)
(setq whitespace-style '(face empty lines-tail trailing))
(global-whitespace-mode t)
</pre>

### TRAILING SPACE REMOVER

<pre>
;; delete trailing whitespace on exit
(require 'package)
(add-to-list 'package-archives '("melpa" . "https://melpa.org/packages/"))
</pre>

### COLOR THEMES

If you just **have** to gussy up your color schemes, try `Alt-x color-theme-select`. You can then look through the different themes and try them out, when you find one you like, take note of the name and then add this to your .emacs:

<pre>
;; add a color theme by default
(require 'color-theme)
(color-theme-initialize)
(color-theme-blue-mood)
</pre>

Here, we're using the theme Blue Mood; note that in the .emacs file, it's all lower case and spaces are replaced with dashes!

---

## YOUR SKILL DRILLS

The following are due by 9AM on October 9th:

- lab-04 : banks, right?
- lab-04 : flag fun
- lab-04 : poison scoring
- lab-04 : menu handler
