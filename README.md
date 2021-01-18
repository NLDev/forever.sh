# forever.sh

<p align="center">
<img height="150" width="auto" src="https://raw.githubusercontent.com/NullDev/forever.sh/master/.img/forever.png" /><br>
:repeat: Bash script to managed multiple foreverjs instances at once.
</p>

## What does it do?

It starts multiple specified scripts at once with [foreverjs](https://github.com/foreverjs/forever).

## How?

```bash
src="app.js"
```
On [Line 5](https://github.com/NullDev/forever.sh/blob/master/forever.sh#L5) specifies the name of the script to execute in the directories mentioned below.

<hr>

```bash
declare -a arr=(
	"folder1"
	"folder2"
	"folder3"
	"and so on..."
)
```
From [Line 8 to Line 13](https://github.com/NullDev/forever.sh/blob/master/forever.sh#L8-L13) sets the name of the folders (in the current directory) in which the script (specified above) will get executed.

<hr>

```bash
declare -a abs=(
	"ExampleScript1 -c python /path/to/script.py"
	"ExampleScript2 /path/to/script.js"
	"and so on..."
)
```
From [Line 16 to Line 20](https://github.com/NullDev/forever.sh/blob/master/forever.sh#L16-L20) specifies other script. Whether they are in a different directory, are not [NodeJS](https://nodejs.org) or if they do not feature a script with the above specified name you can add them here. All paths are absolut!

<hr>

## Anything else?

The script features some **arguments**:

| Argument | Explanation |
|----------|-------------|
| `-s` or `--stop`    | Stops all scripts              |
| `-r` or `--restart` | Stops and restarts all scripts |

That's all :smile_cat:

<p align="center">
<br>
<strike>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</strike> Screenshot <strike>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</strike><br>
<br>
<img src="https://raw.githubusercontent.com/NullDev/forever.sh/master/.img/scr1.png" /><br>
</p>
