![image](https://user-images.githubusercontent.com/42554663/102692722-15203980-4237-11eb-8a4a-15cd8b40c4c9.png)

### LOCK ME

A simple screen locker which requires `imagemagick`, `xss-lock` and `i3lock` to be installed.


### Installation

Just copy the `lockme` script and put it somewhere in your `$PATH`.


I use `BSPWM` so in my `sxhkdrc`, I have this line to lock the screen using `lockme`.

```bash
...
# Lock the screen

super + x
    ~/.local/bin/lockme lock
...
```

To enable it on system startup so you will get screen locked once in-active for some minutes, you can use `lockme` with `xss-lock`. Put this in your `~/.xprofile.
I have `lockme` in my homedir `~/.local/bin/lockme`.

```bash
...
xset dpms 180 &
~/.local/bin/lockme start
...
```
