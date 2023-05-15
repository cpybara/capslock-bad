# Caps-Lock Bad

## Introduction

Tired of of accedentally pressing the Caps-Lock key again and again, ruining your work and wasting your precious time? Well let's fix that and make the capslock key more useful for both windows and linux.

## Table of Contents

- [Remapping Caps Lock in Windows](#remapping-caps-lock-in-windows)
- [Remapping Caps Lock in Linux](#remapping-caps-lock-in-linux)

## Remapping Caps Lock in Windows

#### Creating an AutoHotkey script

1. Download and install the [AutoHotkey](https://autohotkey.com) utility.
2. Open notepad and type the following code:
   ```
   Capslock::return
   
   Capslock & h::Send {Left}
   Capslock & j::Send {Down}
   Capslock & k::Send {Up}
   Capslock & l::Send {Right}
   ```
3. Save the file to wherever you want with .ahk extention. Example: `capsutil.ahk`
  
   *Now while the script is running whenever you'll press h, j, k or l keys while holding capslock, they'll behave as left, down, up and right arrow keys respectively.*

#### Making the script run on startup

1. Open the folder where your AutoHotkey script is located.
2. Right-click on the script file and select "Create shortcut".
3. Press Win + R to open the Run dialog box.
4. Type `shell:startup` and press Enter. This will open the Startup folder.
5. Move the shortcut of your AutoHotkey script into the Startup folder.
6. Restart your computer.

## Remapping Caps Lock in Linux

### Using keyd to remap and repurpose the utility of the Caps-Lock key

1. Install the [keyd](https://github.com/rvaiya/keyd) utility using your preffered package manager.
2. create a `default.conf` file in the "/etc/keyd/" directory if it doesn't exist already
3. open the default.conf file using your preffered text editor and add the following lines:
   ```
   [ids]
   
   *
   
   [main]
   
   capslock = overload(capslock_layer,esc)
   
   [capslock_layer]
   
   h = left
   j = down
   k = up
   l = right
   ```
   *this will map the Caps-Lock key to the Escape key and to the arrow keys when pressed with combination to h, j, k and l keys*
4. Now enter the following line in the terminal for the changes to take effect:
   ```
   sudo systemctl restart keyd && sudo systemctls enable keyd && sudo systemctl start keyd
   ``` 
