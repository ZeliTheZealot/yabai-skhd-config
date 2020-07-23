# chunkwm, yabai and skhd configs
My personal yabai and skhd configs

Inspired by [Julian-Heng](https://github.com/Julian-Heng/chunkwm-yabai-config).

NOTE: yabai requires System Integrity Protection to be disabled to work properly. See [here](https://github.com/koekeishiya/yabai/wiki/Disabling-System-Integrity-Protection) for more information.


## Installing for yabai
```sh
# Remove previous links
$ rm -f "${HOME}"/.{yabai,skhd}rc

# Install configs
$ git clone https://github.com/ZeliTheZealot/yabai-skhd-config.git "${HOME}"/.config/yabai
$ ln -s "${HOME}/.config/yabai/yabai/yabairc" "${HOME}/.yabairc"
$ ln -s "${HOME}/.config/yabai/yabai/skhdrc" "${HOME}/.skhdrc"
```

## Keyboard shortcuts
### Focus actions
#### Changing focus to a window in a given direction
<kbd>lalt</kbd> + <kbd>hjkl</kbd>

Assumes display 2 is above display 1.

#### Focus display (monitor)
<kbd>cmd</kbd> + <kbd>shift</kbd> + <kbd>m</kbd>

Focuses recent display.

#### Focus desktop (space)
| Action          | Key Combination           |
|-----------------|---------------------------|
| Cycle left      | <kbd>fn</kbd>+<kbd>h</kbd>|
| Cycle right     | <kbd>fn</kbd>+<kbd>l</kbd>|
| Go to space 2   | <kbd>fn</kbd>+<kbd>2</kbd>|

### Move actions

#### Move windows towards the given direction
<kbd>shift</kbd> + <kbd>alt</kbd> + <kbd>hjkl</kbd>

Assumes display 2 is above display 1.

#### Move window to another desktop

| Action                      | Key Combination                                    |
|-----------------------------|----------------------------------------------------|
| Send to last active desktop | <kbd>shift</kbd> + <kbd>lalt</kbd> + <kbd>m</kbd>   |
| Send to previous workplace  | <kbd>shift</kbd> + <kbd>lalt</kbd> + <kbd>p</kbd>   |
| Send to next workplace      | <kbd>shift</kbd> + <kbd>lalt</kbd> + <kbd>n</kbd>   |
| Send to workplace           | <kbd>shift</kbd> + <kbd>lalt</kbd> + <kbd>num</kbd> |

### Shape-shifting actions

#### Rotate windows

| Action               | Key Combination                                  |
|----------------------|--------------------------------------------------|
| Balance window tree  | <kbd>ralt</kbd> + <kbd>b</kbd>                   |
| Rotate anticlockwise | <kbd>ralt</kbd> + <kbd>r</kbd>                   |
| Flip on x-axis       | <kbd>ralt</kbd> + <kbd>x</kbd>                   |
| Flip on y-axis       | <kbd>ralt</kbd> + <kbd>y</kbd>                   |

#### Change window between floating and managed

| Action           | Key Combination                   |
|------------------|-----------------------------------|
| Floating         | <kbd>ralt</kbd> + <kbd>f</kbd>    |
| Managed          | <kbd>ralt</kbd> + <kbd>m</kbd>    |

#### Resize windows

| Action       | Key Combination                                  |
|--------------|--------------------------------------------------|
| Resize left  | <kbd>ralt</kbd> + <kbd>h</kbd> |
| Resize down  | <kbd>ralt</kbd> + <kbd>j</kbd> |
| Resize up    | <kbd>ralt</kbd> + <kbd>k</kbd> |
| Resize right | <kbd>ralt</kbd> + <kbd>l</kbd> |

#### Window actions

| Action            | Key Combination                                  |
|-------------------|--------------------------------------------------|
| Fullscreen        | <kbd>alt</kbd>  + <kbd>f</kbd>                   |
| Native fullscreen | <kbd>shift</kbd> + <kbd>alt</kbd> + <kbd>f</kbd> |
| Center window     | <kbd>shift</kbd> + <kbd>alt</kbd> + <kbd>c</kbd> |

### Choosing where to put next opened window

#### Insertion point

| Action                       | Key Combination                                                     |
|------------------------------|---------------------------------------------------------------------|
| Insert left                  | <kbd>shift</kbd> + <kbd>ralt</kbd> + <kbd>h</kbd> |
| Insert down                  | <kbd>shift</kbd> + <kbd>ralt</kbd> + <kbd>j</kbd> |
| Insert up                    | <kbd>shift</kbd> + <kbd>ralt</kbd> + <kbd>k</kbd> |
| Insert right                 | <kbd>shift</kbd> + <kbd>ralt</kbd> + <kbd>l</kbd> |

#### Window opacity

<kbd>alt</kbd> + <kbd>o</kbd> Set unfocused windows to be slightly less opaque
<kbd>alt</kbd> + <kbd>s</kbd> Set unfocused windows to be completely opaque

#### Misc

| Action          | Key Combination                                                     |
|-----------------|---------------------------------------------------------------------|
| Toggle float    | <kbd>shift</kbd> + <kbd>alt</kbd> + <kbd>space</kbd>                |
| Toggle gaps     | <kbd>alt</kbd> + <kbd>g</kbd>                    |
| Restart yabai   | <kbd>cmd</kbd> + <kbd>alt</kbd> + <kbd>shift</kbd> + <kbd>r</kbd> |

### Show information (non-Yabai)
#### Description
Uses `osascript` to show information like CPU, memory, battery, etc. The CPU script requires [osx-cpu-temp](https://github.com/lavoiesl/osx-cpu-temp) installed. The song script supports iTunes and cmus.

Click [here](scripts) to view the script folder

Note: May have to change the location of the scripts in skhdrc

#### Key Combination
<kbd>fn</kbd> + <kbd>lalt</kbd> + <kbd>num</kbd>

#### Screenshots
<img width="382" height="101" src="screenshots/cpu.png?raw=true"><img width="382" height="101" src="screenshots/mem.png?raw=true">
<img width="382" height="101" src="screenshots/bat.png?raw=true"><img width="382" height="101" src="screenshots/disk.png?raw=true">
<img width="382" height="101" src="screenshots/song.png?raw=true">

```
fn + lalt - 1 : /path/to/script
fn + lalt - 2 : /path/to/script
fn + lalt - 3 : /path/to/script
...
```

### Opening applications (non-Yabai)
#### Launch iTerm2
##### Description
Launches iTerm2 using like in i3-wm.

Click [here](scripts/open_iterm2.sh) to view the script

##### Key Combination
<kbd>alt</kbd> + <kbd>return</kbd>
