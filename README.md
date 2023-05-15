# Caps Lock Bad

## Introduction

Tired of of accedentally pressing the capslock key, ruining your work and wasting your precious time? Well let's fix that and make the capslock key more useful in both windows and linux.

## Table of Contents

- [Remapping Caps Lock in Windows](#remapping-caps-lock-in-windows)
- [Remapping Caps Lock in Linux](#remapping-caps-lock-in-linux)

## Remapping Caps Lock in Windows

### Disabling the capslock feature of the Caps Lock button

1. Press Win + R to open the Run dialogue box.
2. Type `regedit` and press enter to open the registry editor.
3. Enter “`Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layout`” in the Registry Editor’s address bar.
4. Right-click on an empty space in the right pane and select “New > Binary Value”.
5. Name the new value “`Scancode Map`” and double-click on it.
6. Enter the following code into the “Value data” field:
   ```
   00 00 00 00 00 00 00 00
   02 00 00 00 3a 00 00 00
   00 00 3a 00 00 00 37 e0
   ```
7. Click OK and restart the Windows.

### Making the Button Useful

#### Creating the AutoHotkey script

1. Download and install the [AutoHotkey](https://autohotkey.com) utility.
2. Open notepad and type the following code:
   ```
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
4. Type shell:startup and press Enter. This will open the Startup folder.
5. Move the shortcut of your AutoHotkey script into the Startup folder.
6. Restart your computer.

## Remapping Caps Lock in Linux

### Coming Soon...
