Create-Playlist.workflow
========================

An OSX Automator Workflow for creating relative-pathed m3u playlists from audio files in the selected folder.

Installation
------------

To install, simply `git clone https://github.com/bmatcuk/Create-Playlist.workflow.git ~/Library/Services/Create-Playlist.workflow`.
You may need to "open" the workflow to get it to appear in the Services menu.
To do that, just navigate to ~/Library/Services and double click Create-Playlist.workflow to open it in Automator.
You don't need to do anything here; just close Automator.

To use, open a Finder window and locate a folder for which you want to create a playlist.
Right click on this folder and select Services, Create-Playlist.
In a moment, a file will be created in the current folder with the same name as the folder you selected and the .m3u extension.
You can also select multiple folders.
Right click and select Services, Create Playlist as before and you'll get a .m3u file for each folder selected!
Note: There may be a limit to the number of folders the workflow can process at a time...

This script will find .mp3, .aac, .m4a, .wav, .wma, .flac, .ogg, .pcm, .aiff, and .alac files.
If there are any others you think it should support, file an Issue.

How Does it Work?
-----------------

This is an [Automator](http://macosxautomation.com/automator/) workflow that runs a simple shell script.
The script loops through the arguments (the selected folders, in this case), switches to that folder, and then searches for audio files recursively.
Whenever an audio file is found, it is appended to the m3u file using some appropriate formatting.

Why?
----

My car can read music off a USB keychain drive.
It seems to understand artists and albums from the MP3 headers, but it just ends up playing songs in alphabetic order by filename.
I could rename all my files so they'll end up playing in the order I'd like... but my car also understands m3u files.
It seemed easier to make this work =)
