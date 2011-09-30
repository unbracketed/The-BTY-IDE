The bitty IDE
=============

1. This is not an IDE.
2. bitty (BTY) IDE is more of a suggestion, if anything. 
3. bitty is meant to describe a common protocol for assembling minimal, powerful, portable, cross-platform* development environments based on common commands and tools. 
4. bitty is more like a personal subscription into a long-term plan. Much like learning to play an instrument, BTY is a willingness to commit a very small amount of time on a consistent basis in return for becoming very proficient over time.
5. As this system is intended to be 100% customizable to my workflow, I can confidently say that my development environment is Better Than Yours. 

The target environment is based on tmux and zsh with an emphasis on Python devevelopment. The author's primary text editor is vim so 
shortcuts are influenced by vim and vim-mode (key bindings supported by other CLI commands).

Philosophy
----------

BTY is intended to be usable as a working environment tailored toward Python development based on common, cross-platform tools; sprinkled
with some well-intentioned shortcuts that are geared toward common development workflows. That said, it should be treated more like
a tutorial or learning framework. For example, when learning a musical instrument one often starts with a structured set of lessons
and mnemonics which vary from mentor to mentor but whose purpose is to help our feeble brains learn the common foundational patterns. Generally,
if you persist in your efforts, these patterns will become second nature and you'll start adding your own flourishes as you 
develop your own style.


Getting Started
---------------

Install BTY

Requirements
------------

tmux
zsh
python
virtualenvwrapper 2.10


Providing your base config files
--------------------------------

People often keep their configuration files in a VCS. A common convention is to name this repo 'dotfiles'. 
BTY works well with this model and encourages you to keep manage your config files in one or more repositories. This makes it 
easy to switch between or try out other configurations and is hoped to encourage community developed templates for best practices.


Getting Familiar with the Environment
-------------------------------------

Crafting a proper piece of code is often the result of using a number of tools. By the time you've finished writing a small piece of code, 
you may have poked around a database, ran some snippets in an interactive Python shell, run tests, stepped through a debugger, checked some log
files, started a local WSGI server, and flushed a cache. My brain seems least stressed when I can manage all these tasks separately, but in
an easily accessible way. Huh? What I mean is, the following don't work well for me: 

1. Running every command in a single console window.
2. Running each command in a separate GUI tab in a console window. 

In the first case, you may quickly lose older output that exceeds the scroll buffer. Trying to parse through the output of many different
commands is tiring. You have to stop your development services (like Django runserver) in order to run other commands.
The second case fixes the last point, but eventually you hit The GUI Barrier.

To be fair, some may be perfectly productive using GUI tabs in a console window although I think everyone hits a limit where if you keep 
increasing the number of tabs the interface becomes cumbersome to use. I'll offer that using another solution provides the same 
functionality as well as offering more elegant and flexible ways to manage your tasks. 

Enter the Terminal Multiplexer

A terminal multiplexer will let you run virtual consoles within the same terminal. This is analagous to the tabs in terminal interface, but better.
A good terminal multiplexer will provide a lot of flexibility for managing each console/tab/window. You want the ability to be able to
move windows around, mix multiple windows into a single screen, and stash away windows that you're not actively using, but still want
available. 

Another nice feature of a terminal multiplexer is that you can detach from your running session and it will remain running. For example, you
detach, close your terminal window, and later you open a new terminal window and attach. I use this feature often to switch between computers. I
have a main work computer that I run my development environment in, but when I want to work from another machine I ssh to my work box and
attach to my session with everything exactly as I left it, and resume work. Some terminal multiplexers also allow for various multiuser modes -
great for team collaboration here, there, or anywhere.


Minimal intro to tmux...

Terminology

A Server is started.
A Server manages multiple Sessions
A Session is a collection of Windows
A Window can multiple Panes, each holding a link to a Window
A Client connects to the Server and is attached to a Session

It is worth browsing through the tmux man page, which provides more detail about the tmux operational model. Also notice the extensive
commands section. Many aspects of tmux behavior and appearance can be controlled in a consistent manner. 


List commands, shortcuts, aliases
Reloading config shortcuts for interactive tweaking


How the environment is constructed

virtualenvwrapper
rolling your own 


Example workflows
