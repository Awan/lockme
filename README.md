![lockme](https://user-images.githubusercontent.com/42554663/101631744-a7aa2700-3a46-11eb-9bd8-a71835992618.png)
![lockme](https://user-images.githubusercontent.com/42554663/101631805-c5778c00-3a46-11eb-9f7a-6bc8dd546043.png)

### LOCK ME

A simple screen locker which requires `imagemagick` and `i3lock` to be installed.
Captures the current screen using `import` from `imagemagick`, applies some effects and then uses `i3lock` to lock the screen. A padlock in the center of the blurred image.
No `dunst` notifications will be shown on the locked screen. (and that's the reason I wrote this.)
Once unlocked, `dunst` will be resumed.

### Installation

Just copy the `lockme` script and put it somewhere in your `$PATH`.


I use `BSPWM` so in my `sxhkdrc`, I have this line to lock the screen using `lockme`.

```bash
...
# Lock the screen

super + x
    ~/.local/bin/lockme 
...
```

To enable it on system startup so you will get screen locked once in-active for some minutes (3 minutes in my case), you can use `lockme` with `xss-lock`. Put this in your `~/.xprofile`.

```bash
...
xset dpms 180 &
xss-lock -- ~/.local/bin/lockme &
...
```
