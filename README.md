## Prerequis

you need to install unrar and zip

```shell
sudo apt install unrar zip
```

## Installation

Put `cbr2cbz` in a folder in your PATH (or make a symbolic link to the file)

like in `~/.local/perso/bin` (create it if not, do as your want, you can use what you want)

Don't forget to `chmod +x cbr2cbz`

to extend your `$PATH`, edit your `.bashrc` file with somethint like :

```bash
## PATH
export PATH="/home/YOURNAME/.local/perso/bin:$PATH"
```

You can do the same thing with the scripts `delete-converted`, `convert-all`, `convert-all-replace` (meaning putting them in your perso/bin folder, and chmod +x them)

## Use

`cbr2cbz` only do a conversion for 1 file.

`cbr2cbz myold_file.cbr` will produce a CBZ, in a new folder, called "`Converted_comics`" in the same directory as the file

However, with the option -r (for REPLACE), it WILL replace your file (after a checking of the integrety of the newly zipped file).
Make some tests !

`cbr2cbz my_file.cbr -r` WILL replace your file (and renamming it by changing the extension in .cbz)

## For a full folders and sub-folders (recursively)

Use the `convert-all` (for testing)
It calls the `cbr2cbz` tool, with no -r, so it's safe, it will create new commics in `Converted_comics` folders, in all your tree of folders.)

It will recursively treat all the comics, down your CURRENT DIRECTORY.

You can delete those Converted_comics folders, after checking all is good, by using the `delete-converted` script / command

And, if you are happy with your testing, you can launch `convert-all-replace`.

Be CAREFULL !!! It will treat all your cbr/cbz files recursively and REPLACE the original ones.
