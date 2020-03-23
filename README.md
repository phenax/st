# phenax st - My fork of st (https://st.suckless.org/)
st is a simple terminal emulator for X which sucks less.


### Requirements
In order to build st you need the Xlib header files.
You also need rofi installed for the prompts


### Installation
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


### Additional stuff
* `Ctrl + Shift + u` will bring up a `rofi` menu with a list of all urls in the output. Selecting one will open the url with `xdg-open`
* `Shift + PageUp/PageDown` for scrolling through history
* `Ctrl + Shift + Escape` to go into visual selection mode. `s` to start selecting text


### Patches included in the fork

* Allow piping to external command from st
* Transparency
* Clipboard instead of primary
* Create a desktop entry on install
* Allow specifying secondary font
* Scrollback in history
* Cli option for specifying working directory
* Load values from .Xresources

