#### Addtional things added to the original massdrop configuration

- The function key row in layer 0 is <br>
<kbd>⎋ Escape</kbd> <kbd>☼ Screen Brightness ⬇︎ </kbd> <kbd>☼ Screen Brightness ⬆︎</kbd> <kbd>F3</kbd> <kbd>F4</kbd> <kbd>F5</kbd> <kbd>F6</kbd><kbd>Previous ⏩</kbd> <kbd>Play/Pause ⏯</kbd><kbd>Next ⏪</kbd><kbd>Mute 🔇</kbd><kbd>Volume Down 🔈</kbd><kbd>Volume up 🔊</kbd>
- The <kbd>Mod (1)</kbd> key is moved to <kbd>Insert</kbd>
- Last Modifer Row is <br>
<kbd>⌃ Control</kbd> <kbd>⌥ Option</kbd> <kbd>⌘ Command</kbd> <kbd>      Space      </kbd>
 <kbd>⌘ Command</kbd><kbd>⌥ Option</kbd><kbd>⌃ Control</kbd> <kbd>APP/Menu</kbd>
- Pressing <kbd>Mod (1)</kbd> + <kbd>Pause</kbd> sends <kbd>⌃ Control</kbd><kbd>⇧ Shift </kbd><kbd>Power</kbd> to the computer to turn off the monitors and lock the computer.
- LED Matrix is suspended when the computer sends USB suspend (sleeps). <i>Not to be confused with the above lock + monitor off.</i>


To create your firmware file: 
```
make massdrop/ctrl:pratyushtewari
```

To install it to your massdrop keyboard

- Copy the following files in the same folder
  ```
  1. massdrop_ctrl_pratyushtewari.bin
  2. applet-flash-samd51j18a.bin
  3. mdloader_mac
  ```
  You can find the `mdloader_mac` and `applet-flash-samd51j18a.bin` from [mdloader](https://github.com/Massdrop/mdloader)
- Put the keyboard in DFU Mode by pressing <kbd>Mod (1)</kbd> + <kbd>B</kbd>
- Run 
  ```
  ./mdloader_mac --first --download massdrop_ctrl_pratyushtewari.bin  --restart
  ```
More detailed instructions are at [mdloader](https://github.com/Massdrop/mdloader)