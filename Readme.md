# Tmux Configuration 

This is a basic tmux configuration I use for my work/personal use. 
Tmux Plugin Manager (TPM) is used for this configuration, along with tmux-sensible and other small plugins/keybindings.

## Setup Steps:
1) Clone the TPM project: `git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`
2) Create `~/.config/tmux` if not already created
3) cd into the folder and clone this repo: `cd ~/.config/tmux && git clone ... .`
4) Launch Tmux, modify as needed

## Basic Intro to Tmux 
Tmux is a terminal multiplexer, as the name implies, it allows multiple concurrent terminal sessions, background sessions, etc.
There's lots of features and a few key jargon you need to know before starting.

- **Session** => Session is topmost layer of tmux which contains one or more windows.
There can be more than one session, but only one session is active at a time. Imagine a session as one browser instance. 

- **Window** => Window is the instance in the session that you manage, enter commands, etc. There might be (and often there is) multiple windows in a session. Imagine window like tabs inside a browser session. 
There can be multiple windows and you can change between each windows (common keybindings provided below). A window covers entire visible terminal screen and can contain multiple panes inside it.

- **Pane** => Panes are like multiple sections/divisions in a window. Its like a split view within a single tab. All panes within an active window is visible in the terminal, whereas there's only one active window visible at a time.
There's only one active pane at a time that you interact with.

**Basic Tmux Keybindings and Control** 
- To Enter commands to tmux pane: *prefix key*. (Default prefix is Ctrl+b)
- To create new window, *prefix+c*. 
- To switch between windows (list of windows is visible in bottom left bar) *prefix+window_num* (0,1,2,etc.)
- You can also cycle through windows by entering *prefix+n* or *prefix+p* (for next and previous) 
- To swap windows, *prefix + :swap-window -s x -t y*,(x and y are windows number to swap)
- To swap current window to be first window, *prefix + :swap-window -t 0*
- To kill/close and exit out of a window, *prefix + &*
- To exit from the tmux itself, type *exit* in the terminal (no prefix key or anything neeeded).
- To split a pane to two (horizontally), *prefix + %*
- To split verticaly, *prefix + "*
- Move around the panes by entering *prefix + arrow keys*
- Swap panes by using *prefix + curly braces*
- Toggle pane number *prefix+q*, move to subsequent pane
- Zoom in on one pane *prefix+z*
- Turn pane to window *prefix+!*
- Close a pane: *prefix+x*

- To create a session and attach *tmux new -s session_name* (From inside a session: new session_name)
- To list active sessions: *tmux ls* (fro inside: *prefix+s*)
- Preview session: *prefix+w* (attach by pressing enter)
- Attach a session from outside: *tmux attach -t session_name*

- Enter copy mode (similar to normal mode): *prefix+[*
- From normal mode, to navigate h,j,k,l to copy *Ctrl+v+space*
