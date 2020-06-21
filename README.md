# st - My fork of st (https://st.suckless.org/)
st is a simple terminal emulator for X which sucks less.


### Requirements
In order to build st you need the Xlib header files.
You also need dmenu installed for the prompts


### Installation
Edit config.mk to match your local setup (st is installed into the /usr/local namespace by default).
Afterwards enter the following command to build and install st (if necessary as root):
```
make clean install
```

### Additional stuff
* `Ctrl + Shift + u` will bring up `dmenu` with a list of all urls in the output. Selecting one will open the url with `xdg-open`
* `Ctrl + Shift + PageUp/PageDown` for scrolling through history. Mouse scroll is disabled but you can enable it by uncommenting a few lines under `mshortcuts` in `config.def.h`
* `Ctrl + Shift + Escape` to go into visual selection mode. The patch has been overridden to make the key bindings more vim like.
    - `v` to start selecting text
    - `y` to copy and exit visual selection
    - `g` to go to the top
    - `G` to go to the bottom
    - `Escape` or `Enter` or `i` to go to insert mode i.e. exit out of vim mode
    - `0` to go the start of the line
    - `$` to go the end of the line
    - `/` to search in window
    - `n/N` for next/prev search result


### Patches included in the fork

* Keyboard selection. (Altered the code after patching)
* Allow piping to external command from st
* Transparency
* Clipboard instead of primary
* Create a desktop entry on install
* Allow specifying secondary font
* Scrollback in history
* Cli option for specifying working directory
* Load values from .Xresources

