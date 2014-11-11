Create-Playlist.workflow
========================

An OSX Automator Workflow for creating relative-pathed m3u playlists from audio files in the selected folder.

Installation
------------

To install, simply `git clone https://github.com/bmatcuk/Create-Playlist.workflow.git ~/Library/Services/`.

To use, open a Finder window and locate a folder for which you want to create a playlist.
Right click on this folder and select Services, Create Playlist.
In a moment, a file will be created in the current folder with the same name as the folder you selected and the .m3u extension.
You can also select multiple folders.
Right click and select Services, Create Playlist as before and you'll get a .m3u file for each folder selected!

Why?
----

My car can read music off a USB keychain drive.
It seems to understand artists and albums from the MP3 headers, but it just ends up playing songs in alphabetic order by filename.
I could rename all my files so they'll end up playing in the order I'd like... but my car also understands m3u files.
It seemed easier to make this work =)
