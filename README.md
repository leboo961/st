# My Personal configuration of st - simple terminal

st is a simple terminal emulator for X which sucks less.

## Bindings


|**Action**                              | **shortcut**     |
|----------------------------------------|------------------|
|new terminal<br>in current directory    | Ctrl+Shift+Return|
|zoom in                                 | Ctrl+Shift+Pg_Up |
|zoom out                                | Ctrl+Shift+Pg_Dn |
|zoom reset                              | Ctrl+Shift+home  |
|copy                                    | Ctrl+Shift+c     |
|paste                                   | Ctrl+Shift+v     |
|scroll up                               | Shift+Pg_Up      |
|scroll down                             | Shift+Pg_dn      |
|follow & copy link                      | alt-l            |
|open url                                | alt-o            |
|vim Browse                              | alt-v            |

⚠ Mouse scrollback not supported in my configuration.

Default vim Browse Behavior:
---------------------------

The default behavior listed below can be adapted:

### Enter Vim Browse Mode:

    Alt+c

### Operations in Vim Browse Mode:

    Enter Visual Mode: V / v
    Enter Yank Mode: Y

### Motions in Vim Browse Mode:

+ Basic motions: j, k, h, l, H, M, L, 0, $ like in VIM
+ Word Move operators: w, W, e, E, b, B similar to VIM
+ Search Operators: /, ?, n, N for forward / backward search
+ Jump to the cursor position prior to entering Vim Browse Mode: G
+ Repeat last command string: .
+ in Visual Mode v: use t to toggle block selection mode
+ Commands like yiw and ya{ are implemented.
+ <Ctrl>f(one page 'down') <Ctrl>b (one page up) <Ctrl>u, <Ctrl>d for half page up/down.
+ . (repeat) last set of motions, and c to clear the last motion.

## Additional Patches

+ alpha - control transperancy with -A flag
+ alpha focus highlight - not adjustable with a flag
+ boxdraw
+ font2 - change font by using -f flag

## Requirements

In order to build st you need the Xlib header files.


## Installation

Start by cloning the repository

```git
git clone https://github.com/fjeh/st
```

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.


