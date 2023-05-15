# Caps Lock Bad

## Introduction

Tired of of accedentally pressing the capslock key, ruining your work and wasting your precious time? Well let's fix that and make the capslock key more useful in both windows and linux.

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
  
   *Now whenever you'll press h, j, k or l keys while holding capslock, they'll behave as left, down, up and right arrow keys respectively.*

#### Making the script run on startup

1. Open the folder where your AutoHotkey script is located.
2. Right-click on the script file and select "Create shortcut".
3. Press Win + R to open the Run dialog box.
4. Type `shell:startup` and press Enter. This will open the Startup folder.
5. Move the shortcut of your AutoHotkey script into the Startup folder.
6. Restart your computer.

## Remapping Caps Lock in Linux

### Coming Soon...
