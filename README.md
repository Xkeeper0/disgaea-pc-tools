# disgaea-pc-save-tools

Tools for decrypting and decompressing (soon: compressing?) Disgaea PC save files.

Written in PHP. Yes, I know. It works.


## Usage

`php test.php SAVE000.DAT`

This will decrypt, decompress, and write the internal save data to `SAVE000.DAT.bin`.
As of right now, there is no way to re-encode, but maybe in the future.

Possibly also in the future: Splitting the data into sensible values for editing and re-importing???

Most of the text in the save file is in Shift-JIS format, so have fun with that.


## Contributing

Please follow the style used in this (even if it isn't very good). Comments and documentation appreciated.
Maybe a text file describing how the format(s) work in the future.


## Components

* `chunky.php`: Basis for reading defined segments of a file
* `savefile.php`: Handles decrypting the save file itself
* `savedata.php`: Handles the save data chunk
* `ykcmp.php`: Decompresses `YKCMP_V1` data (like the ... save data)
* `test.php`: Hastily-made script to put all the above to work