This is a simple LibreOffice calc file with macros (written in Libreoffice Basic) to import, edit and export m3u/m3u8 list (for IPTV).

Created with Libreoffice version 24.85.2 tested on Xubuntu 24.10 and Windows11.

The file's functionality should be quite intuitive. In any case, below is a list of the buttons and their function.

Command buttons:

* Import List: will prompt to select a m3u/m3u8 list to import.
* Export List: export the list of channels as m3u8 file
* Celar all: remove all channels and their information
* Sort Records: will prompt you to select a method for sorting records
* Remove Duplicates: remove duplicated records. The compare is made by name and by url, in case a duplicate is found only the first occurence will be keeped
* Assign chno: First of all check if the tag "tvg-chno" is present, if not, add it, then , for each channel, check evrey row in ChSheet (starting from column B).If the name is found the value in column A is assigned.Currently Chsheet is filled with a list of Italian channel, it can be modified with your own preferred list of channel to wich assign chno.
* Insert rows: to add channels records or basic tags (add the specified number of void rows)
* Add tags: to add tvg-tags or EXT directives
* Del Rows: to delete records or basic tags
* Delete Tags: to delete tvg tags or EXT directives
* Move ch up/down: move selected records (you must select a range containing the channel names) up and down. The range selected move up/down one position at a time, Keep the button pressed to continue the movement.
* Move tag left/right:move selected tags (tvg or EXT) left/right. You must select a range containg the tags row, and only one type of tags (tvg or EXT).

Disclaimer:
I am not an expert programmer. I have tested the functioning of the macros in different situations, however there may still be bugs with operations that I have not foreseen or with m3u files with syntax different from what I considered "standard" (syntax reference: https://github.com/HamzaBhf00/m3u-tags-iptv).

To avoid unintentional changes to the file structure that could compromise the functionality of the macros, the main sheet is protected (without a password). Only the values ​​of the cells in the channel and basic tags areas can be manually modified (see image below). For any other modification (adding/removing rows or tags, moving etc..) you can use the appropriate buttons.
![M3UEDITOR_SCREENSHOT1](https://github.com/user-attachments/assets/197bd0b1-5a78-45a0-aa9d-57455d879cce)

If you prefer to make changes manually (adding or deleting rows and columns) you can still remove the protection of the sheet. For the correct functioning of the macro, be careful not to edit in any way the lines from 1 to 9, the line with the tag headers and the last line (END LIST).
Also do not edit or remove the columns Index, Channel, group-title, url and source.
