# MP3Tag-AppleMusic-Deezer
Apple Music & Deezer Web Sources for [MP3Tag](https://www.mp3tag.de)

> Forked from https://github.com/ivadham/AppleMusicWebSources & https://github.com/romanoh/Mp3tag.

* ```https://github.com/ivadham/AppleMusicWebSources          ➧ Searches By Artist - Album in AppleMusic```

* ```https://github.com/romanoh/Mp3tag          ➧ Searches By Artist - Album in Deezer```

I modified them to search by Artist+Title & Filename.

### Download - https://github.com/Cenb9/MP3Tag-AppleMusic-Deezer/releases

---

### How to Use - 
Move src files (Tag sources) to folder - \AppData\Roaming\Mp3tag\data\sources

In MP3Tag
Alt+S	- Tag Sources or Ctrl+I	- Last used Tag Source

---

# Extras - 

● Shortcuts - 
```
Ctrl+D	Change directory
Ctrl+H	Add directory
Ctrl+N	Select next file
Ctrl+R	Remove tag
Ctrl+S	Save tag
Alt+Enter	File properties
Alt+T	Extended tags dialog
Alt+1	Tag - Filename
Alt + 2	Filename to Tag
Alt+Shift+1	Tag - Filename (Preview)
Alt+Shift+2	Filename - Tag (Preview)
Alt+6	Actions
Alt+S	Tag Sources
Ctrl+I	Last used Tag Source
```

● Separate multiple artists with \\ . Example - Artist Name 1\\Artist Name 2. For m4a & aac files use /

● Options > Tags > Mpeg > Set "Write" options to ID3v2.3 UTF-16.
To Remove ID3v1 ID3v2.3 (Double) tags - Check Remove: ID3V1, Uncheck ID3v2. After removing ID3V1 tags check ID3v2.

● Remove all extended tags - 
Actions > New > Type: Remove fields except
Fields: TITLE;ARTIST;ALBUM;ALBUM ARTIST;YEAR;TRACK;GENRE;COVER

● Bulk tagging workflow - 
1. Check if any files are ID3v1 only, exclude them and remove all ID3v1 ID3v2.3 tags
2. Remove extended tags
3. Filename to Tag

● Automatically fill the ALBUM tag with the TITLE value whenever the album field is empty - 
Actions > Action type: Format value
Field: ALBUM
Format string: $if2(%album%,%title%)
OR
$if($eql(%album%,),%title%,%album%)

● High Res cover art download - 

Download the COVIT.exe file from https://covers.musichoarders.xyz/ > Integration.
Go to File > Options > Tools & add the exe.
--address https://covers.musichoarders.xyz/ --input "%_path%" --primary-output "%_folderpath%cover" --primary-overwrite
Select a track and right-click > Tools > COVIT or Ctrl+1-0. It will open the query in default browser.
Click on a cover and it will be downloadeded
