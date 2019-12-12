## AR Environment Setup 

### Problem Description: At first I run cmake and design the project on Xcode for AR exercise-1, but when I run the program it fed back error message "OpenCV 4.x+ requires enabled C++11 support" (I also tried Clion but got same error)

**Solution**
Using Clion, CLion -> Preferences -> Build, Execution, Development -> CMake -> add ```-DCMAKE_CXX_FLAGS="-std=c++11``` to CMake Options.

[Add flag on CLion](https://www.jetbrains.com/help/clion/how-to-switch-compilers-in-clion.html)

[Error Solution Website](https://github.com/BVLC/caffe/issues/6358)

## iMac Poweroff randomly

### Problem Description: The iMac at Lab Shut down randomly starting from 4/11/2019.

**Solution**
* Change cable
* Release stastic electricity
* Reset [NVRAM](https://support.apple.com/en-us/HT204063) (memory that Mac uses to store certain settings and access them quickly)
* Reset [SMC](https://support.apple.com/en-us/HT201295)

## Vim Basics

> Just the basics to get you up and running with Vim.

- [Quick start](#quick-start)
- [Commands](#commands)
- [Settings](#settings)
- [The `<Ctrl>` + `z` &ldquo;problem&rdquo;](#the-ctrl--z-problem)
- [See also](#see-also)

This guide assumes some familiarity with the terminal. (See [Unix Basics](https://github.com/yuanqing/unix-basics/blob/master/README.md) for a quick overview.)

## Quick start

1. Launch Vim via the terminal:

    ```sh
    $ vim Main.java
    ```

    You are now in Vim&rsquo;s ***Command*** mode.

    (You should see the contents of `Main.java` if the file already exists. Otherwise you will see an empty text editor window.)

2. You cannot type into or edit your file while in ***Command*** mode. To start typing into the file, you must switch to Vim&rsquo;s ***Insert*** mode. Press `i` to do so. You should see <code>--&nbsp;INSERT&nbsp;--</code> on the bottom-left hand corner of your window. Now you can type as you would with any other text editor.

3. When you&rsquo;re done typing, press `<Esc>` to go back to ***Command*** mode. (The `<Esc>` key is your friend! Hitting `<Esc>` will bring you back to ***Command*** mode.)

4. And&hellip; that&rsquo;s about it, really! Now type `:w` and `<Enter>` to save the file, followed by `:q!` and `<Enter>` to quit Vim.

## Commands

Almost all operations in Vim occur while in ***Command*** mode. Listed here are the more important commands that you should know.

### Switching between ***Command*** and ***Insert*** mode

Action | Keys
:--|:--
Switch to ***Command*** mode | `<Esc>`
Switch to ***Insert*** mode | `i`
Switch to ***Insert*** mode, moving the cursor to the end of the current line | `A`
Switch to ***Insert*** mode, adding a new line under the current line, and moving the cursor to the new line | `o`

### Moving the cursor around the file

Action | Keys
:--|:--
Page up | `<Ctrl>` + `u`
Page down | `<Ctrl>` + `d`
Move the cursor to the next word | `W`
Move the cursor to the previous word | `b`
Move the cursor to the start of the current line | `0`
Move the cursor to the end of the current line | `$`
Move the cursor to a particular line of the file (eg. line number 9) | `9G`

Of course, you can also move the cursor using any of the arrow keys (<code>&uarr;</code>, <code>&darr;</code>, <code>&larr;</code>, <code>&rarr;</code>), but it will be a lot faster to use the above commands.

### Delete/cut

Action | Keys
:--|:--
Delete the line under the cursor | `dd`
Delete the word under the cursor | `dw`
Delete the character under the cursor | `x`

Because whatever you delete is copied into Vim&rsquo;s clipboard, these 3 commands are akin to performing a cut.

### Copy and paste

Action | Keys
:--|:--
Copy the current line | `yy`
Copy a particular number of lines, starting from the current line (eg. 3 lines) | `3yy`
Paste | `p`

You can also specify the text to be copied using a text selection. It is a bit more involved, though:

1. While in ***Command*** mode, press `v` to switch to ***Visual*** mode. You should see <code>--&nbsp;VISUAL&nbsp;--</code> on the bottom-left hand corner of your window.
2. [Move the cursor](#moving-the-cursor-around-the-file) to adjust the text selection.
3. When you have selected the text that you want to copy, press `y`. This will bring you back to ***Command*** mode, and the selected text will have been copied into Vim&rsquo;s clipboard.

### Undo and redo

Action | Keys
:--|:--
Undo | `u`
Redo | `<Ctrl>` + `r`

### Fixing code indentation

Action | Keys
:--|:--
Fix the code indentation of the file | `gg=G`

### Save and quit

Action | Keys
:--|:--
Save the file | `:w` then `<Enter>`
Save the file then quit | `:wq` then `<Enter>`
Quit without saving the file | `:q!` then `<Enter>`

## Settings

These are some of the commands to customise the display:

Action | Keys
:--|:--
Enable syntax highlighting | `:syntax on` then `<Enter>`
Enable line numbers | `:set number` then `<Enter>`

Vim will look for a settings file named `.vimrc` in your home directory. You can avoid having to type the above settings for every new Vim session by putting the following in your `~/.vimrc`:

```viml
syntax on
set number
```

## The `<Ctrl>` + `z` &ldquo;problem&rdquo;

Remember that the command for undo is simply `u`, *not* `Ctrl` + `z`!

If you&rsquo;d accidentally pressed `Ctrl` + `z`, you will find yourself back in your terminal, where you will see something like the following:

```sh
[1]+  Stopped                 vim Main.java
```

A quick fix is to issue the `fg` command:

```sh
$ fg
```

This will bring us back to Vim, and all is well with the world.

(Explanation: Pressing `<Ctrl>` + `z` [places the currently-running program in the background](http://en.wikibooks.org/wiki/A_Quick_Introduction_to_Unix/Job_Control#Controlling_Jobs_in_Unix). Here, the currently-running program is Vim. The `fg` program simply brings the most recent &ldquo;backgrounded&rdquo; program back to the foreground.)

## See also

- [Unix Basics](https://github.com/yuanqing/unix-basics/blob/master/README.md)
- [Vim Commands Cheatsheet](http://www.fprintf.net/vimCheatSheet.html)


### Bar Chart

```chart
{
  "type": "bar",
  "data": {
  "labels": [
    "Red",
    "Blue",
    "Yellow",
    "Green",
    "Purple",
    "Orange"
  ],
  "datasets": [
    {
    "label": "# of Votes",
    "data": [
      12,
      19,
      3,
      5,
      2,
      3
    ],
    "backgroundColor": [
      "rgba(255, 99, 132, 0.2)",
      "rgba(54, 162, 235, 0.2)",
      "rgba(255, 206, 86, 0.2)",
      "rgba(75, 192, 192, 0.2)",
      "rgba(153, 102, 255, 0.2)",
      "rgba(255, 159, 64, 0.2)"
    ],
    "borderColor": [
      "rgba(255,99,132,1)",
      "rgba(54, 162, 235, 1)",
      "rgba(255, 206, 86, 1)",
      "rgba(75, 192, 192, 1)",
      "rgba(153, 102, 255, 1)",
      "rgba(255, 159, 64, 1)"
    ],
    "borderWidth": 1
    }
  ]
  },
  "options": {}
}
```
